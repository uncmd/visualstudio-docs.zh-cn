---
title: CA1810：以内联方式初始化引用类型的静态字段 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- InitializeReferenceTypeStaticFieldsInline
- CA1810
helpviewer_keywords:
- InitializeReferenceTypeStaticFieldsInline
- CA1810
ms.assetid: e9693118-a914-4efb-9550-ec659d8d97d2
caps.latest.revision: 23
author: jillre
ms.author: jillfra
manager: wpickett
ms.openlocfilehash: 9032ac105477370477b13554afe4ee65bd7cd733
ms.sourcegitcommit: a8e8f4bd5d508da34bbe9f2d4d9fa94da0539de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/19/2019
ms.locfileid: "72609020"
---
# <a name="ca1810-initialize-reference-type-static-fields-inline"></a>CA1810：以内联方式初始化引用类型的静态字段
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|InitializeReferenceTypeStaticFieldsInline|
|CheckId|CA1810|
|类别|Microsoft. 性能|
|是否重大更改|不间断|

## <a name="cause"></a>原因
 引用类型声明显式静态构造函数。

## <a name="rule-description"></a>规则说明
 当一个类型声明显式静态构造函数时，实时 (JIT) 编译器会向该类型的每个静态方法和实例构造函数中添加一项检查，以确保之前已调用该静态构造函数。 当访问任何静态成员或创建类型的实例时，将触发静态初始化。 但是，如果您声明一个类型的变量，但不使用它，则不会触发静态初始化，如果初始化更改全局状态，这可能很重要。

 当所有静态数据都以内联方式初始化并且未声明显式静态构造函数时，Microsoft 中间语言（MSIL）编译器会将 `beforefieldinit` 标志和用于初始化静态数据的隐式静态构造函数添加到 MSIL 类型定义. 当 JIT 编译器遇到 `beforefieldinit` 标志时，大多数情况下不会添加静态构造函数检查。 在访问静态方法之前，但在调用静态方法或实例构造函数之前，不能保证静态初始化在访问任何静态字段之前发生。 请注意，在声明类型的变量后，可能会随时发生静态初始化。

 静态构造函数检查会降低性能。 通常，静态构造函数仅用于初始化静态字段，在这种情况下，必须仅确保在首次访问静态字段之前发生静态初始化。 @No__t_0 行为适用于这些类型和大多数其他类型。 仅当静态初始化影响全局状态并且满足以下任一条件时，它才是不适当的：

- 全局状态的影响非常昂贵，如果未使用该类型，则不需要这样做。

- 可以在不访问类型的任何静态字段的情况下访问全局状态效果。

## <a name="how-to-fix-violations"></a>如何解决冲突
 要修复与该规则的冲突，请在声明它时初始化所有静态数据并移除静态构造函数。

## <a name="when-to-suppress-warnings"></a>何时禁止显示警告
 如果性能不是问题，则可以安全地禁止显示此规则发出的警告;或者，如果静态初始化导致的全局状态更改很昂贵，或者必须保证在调用类型的静态方法或创建类型的实例之前发生。

## <a name="example"></a>示例
 下面的示例显示了一个与该规则冲突的类型 `StaticConstructor`）和一个类型，`NoStaticConstructor`，它将静态构造函数替换为内联初始化以满足此规则。

 [!code-csharp[FxCop.Performance.RefTypeStaticCtor#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Performance.RefTypeStaticCtor/cs/FxCop.Performance.RefTypeStaticCtor.cs#1)]
 [!code-vb[FxCop.Performance.RefTypeStaticCtor#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Performance.RefTypeStaticCtor/vb/FxCop.Performance.RefTypeStaticCtor.vb#1)]

 请注意，在 `NoStaticConstructor` 类的 MSIL 定义上添加了 `beforefieldinit` 标志。

 **。类公共自动 Ansi StaticConstructor** **扩展了 [mscorlib] system.object** 
 **{** 
 **}//类 StaticConstructor** 
 的结尾 **。类公共自动 ansi beforefieldinit NoStaticConstructor** **扩展 [mscorlib.dll] System.object** 
 **{** 1 **}//NoStaticConstructor 类的结尾**
## <a name="related-rules"></a>相关规则
 [CA2207：以内联方式初始化值类型的静态字段](../code-quality/ca2207-initialize-value-type-static-fields-inline.md)
