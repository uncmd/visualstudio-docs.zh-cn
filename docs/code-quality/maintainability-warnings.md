---
title: 维护性警告
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.codeanalysis.maintainabilityrules
helpviewer_keywords:
- warnings, maintainability
- managed code analysis warnings, maintainability warnings
- maintainability warnings
ms.assetid: 537e70ca-a88c-49df-bfc7-0ee63bbe4f16
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fcb1165ea00d407f5b4840358cc270eb299ba198
ms.sourcegitcommit: da5ebc29544fdbdf625ab4922c9777faf2bcae4a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/29/2020
ms.locfileid: "82586213"
---
# <a name="maintainability-warnings"></a>维护性警告

可维护性警告支持库和应用程序维护。

## <a name="in-this-section"></a>在本节中

| 规则 | 描述 |
|-----------|-----------------------------------|
| [CA1500:变量名不应与字段名相同](../code-quality/ca1500.md) | 实例方法声明的参数或本地变量的名称与声明类型的实例字段匹配，这将导致错误。 |
| [CA1501:避免过度继承](../code-quality/ca1501.md) | 类型在继承层次结构中的深度超过四级。 深度嵌套的类型层次结构可能很难遵循、理解和维护。 |
| [CA1502:避免过度复杂](../code-quality/ca1502.md) | 此规则通过方法来测量线性独立的路径的数量，该数量是由条件分支的数量和复杂度决定的。 |
| [CA1504:检查令人误解的字段名](../code-quality/ca1504.md) | 实例字段的名称以 "s_" 开头，或静态（在中[!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]为共享）字段的名称以 "m_" 开头。 |
| [CA1505:避免使用无法维护的代码](../code-quality/ca1505.md) | 类型或方法具有较低的可维护性索引值。 如果可维护性指数较低，则表示类型或方法可能难以维护，最好重新进行设计。 |
| [CA1506:避免过度类耦合度](../code-quality/ca1506.md) | 此规则通过计算类型或方法包含的唯一类型引用的个数来衡量类耦合。 |
| [CA1507：使用 nameof 代替字符串](../code-quality/ca1507.md) | 字符串文本用作参数，可在其中使用`nameof`表达式。 |
| [CA1508：避免死条件代码](../code-quality/ca1508.md) | 方法具有始终计算为`true`或`false`在运行时的条件代码。 这会导致条件的`false`分支中的代码停滞。 |
| [CA1509：代码度量值配置文件中的条目无效](../code-quality/ca1509.md) | 代码度量规则（如[CA1501](ca1501.md)、 [CA1502](ca1502.md)、 [CA1505](ca1505.md)和[CA1506](ca1506.md)）提供了名为`CodeMetricsConfig.txt`的配置文件，该文件具有无效条目。 |

## <a name="see-also"></a>请参阅

- [测量托管代码的复杂性和可维护性](../code-quality/code-metrics-values.md)
