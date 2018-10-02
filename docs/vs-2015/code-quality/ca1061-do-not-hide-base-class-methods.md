---
title: CA1061： 不要隐藏基类方法 |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- CA1061
- DoNotHideBaseClassMethods
helpviewer_keywords:
- DoNotHideBaseClassMethods
- CA1061
ms.assetid: 0bda9dc8-87b4-4038-ab9d-563298387466
caps.latest.revision: 11
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: f018abbb864533e5c9d7b598638a4006a69ab2f3
ms.sourcegitcommit: 99d097d82ee4f9eff6f588e5ebb6b17d8f724b04
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/24/2018
ms.locfileid: "47587499"
---
# <a name="ca1061-do-not-hide-base-class-methods"></a>CA1061：不要隐藏基类方法
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[CA1061： 不要隐藏基类方法](https://docs.microsoft.com/visualstudio/code-quality/ca1061-do-not-hide-base-class-methods)。

|||
|-|-|
|TypeName|DoNotHideBaseClassMethods|
|CheckId|CA1061|
|类别|Microsoft.Design|
|是否重大更改|重大|

## <a name="cause"></a>原因
 派生的类型声明的方法具有相同名称和具有相同数量的参数作为某一基方法;一个或多个参数是基方法; 中的相应参数的基类型和任何剩余的参数具有相同基方法中的相应参数的类型。

## <a name="rule-description"></a>规则说明
 只是在将较弱派生的基方法的参数签名中的对应类型相比的类型不同的派生方法的参数签名时，将由派生类型中具有相同名称方法隐藏基类型中的方法。

## <a name="how-to-fix-violations"></a>如何解决冲突
 若要修复此规则的冲突，请删除或重命名方法，或更改的参数签名，以便该方法不会隐藏基方法。

## <a name="when-to-suppress-warnings"></a>何时禁止显示警告
 不禁止显示此规则发出的警告。

## <a name="example"></a>示例
 下面的示例显示了与该规则冲突的方法。

 [!code-csharp[FxCop.Design.HideBaseMethod#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.HideBaseMethod/cs/FxCop.Design.HideBaseMethod.cs#1)]


