---
title: ExistsInCollection &lt;T &gt; 活动设计器 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.ExistsInCollection`1.UI
ms.assetid: 0acf9a13-caf5-4bb4-ba22-ec37d2b7267a
caps.latest.revision: 6
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: 08aabbcb7dbef2df9a3affa8589a9c6d4205ac58
ms.sourcegitcommit: a8e8f4bd5d508da34bbe9f2d4d9fa94da0539de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/19/2019
ms.locfileid: "72656735"
---
# <a name="existsincollectionlttgt-activity-designer"></a>ExistsInCollection &lt;T &gt; 活动设计器
**ExistsInCollection \<T >** 活动设计器用于创建和配置 <xref:System.Activities.Statements.ExistsInCollection%601> 活动。

## <a name="the-existsincollectiont-activity"></a>ExistsInCollection \<T > 活动
 <xref:System.Activities.Statements.ExistsInCollection%601> 活动确定特定集合中是否存在指定项。

### <a name="using-the-existsincollectiont-activity-designer"></a>使用 ExistsInCollection \<T > 活动设计器
 **ExistsInCollection \<T >** 活动设计器可在 "**工具箱**" 的 "**集合**" 类别中找到，可通过单击 [!INCLUDE[wfd2](../includes/wfd2-md.md)] 的 "**工具箱**" 选项卡（或者 **，从**"**视图**" 菜单或 CTRL + ALT + X。）

 可以将 " **ExistsInCollection" \<T >** 活动设计器从 "**工具箱**" 拖放到 [!INCLUDE[wfd2](../includes/wfd2-md.md)] 图面上通常放置活动的任何位置，例如在 <xref:System.Activities.Statements.Sequence> 中。 这将创建一个 <xref:System.Activities.Statements.ExistsInCollection%601> 活动，其中默认 <xref:System.Activities.Activity.DisplayName%2A> 为 ExistsInCollection \<Int32 >。 （默认情况下， *TypeArgument*为**Int32**。 可以在属性网格中更改该属性。） 可以在**ExistsInCollection \<T >** 活动设计器的标头中或在属性网格的 " **DisplayName** " 框中编辑 <xref:System.Activities.Activity.DisplayName%2A> 值。 其他属性必须在属性网格上编辑。

### <a name="the-existsincollectiont-properties"></a>ExistsInCollection \<T > 属性
 下表列出 <xref:System.Activities.Statements.ExistsInCollection%601> 属性并说明如何在设计器中使用它们。

|属性名|必需|用法|
|-------------------|--------------|-----------|
|<xref:System.Activities.Activity.DisplayName%2A>|False|<xref:System.Activities.Statements.ExistsInCollection%601> 活动的友好名称。 默认值为 ExistsInCollection \<Int32 >。 虽然 <xref:System.Activities.Activity.DisplayName%2A> 值不是绝对必需的，但最好使用该属性值。|
|<xref:System.Activities.Statements.ExistsInCollection%601.Item%2A>|True|要添加到集合中的项 \<T >。 此项的类型为*T* ，类型为*TypeArgument*。 若要指定项，请在属性网格中键入 Visual Basic 表达式。|
|<xref:System.Activities.Statements.ExistsInCollection%601.Collection%2A>|True|项应添加到的集合。 此集合的类型为**ICollection \<TypeArgument >。** 若要指定集合，请在属性网格中键入 Visual Basic 表达式。|
|*TypeArgument*|True|包含在 <xref:System.Collections.Generic.ICollection%601> 中的项的类型 T。 默认情况下，此*TypeArgument*类型设置为**Int32**。 若要更改类型，请在属性网格的组合框中更改 " *TypeArgument* " 的值。|
|<xref:System.Activities.Activity%601.Result%2A>|False|一个指示集合中是否存在指定项的值。 若要指定要绑定到结果的变量，请在属性网格中键入 Visual Basic 变量。|

## <a name="see-also"></a>请参阅
 [Collection](../workflow-designer/collection-activity-designers.md) [AddToCollection \<T >](../workflow-designer/addtocollection-t-activity-designer.md) [ClearCollection \<T >](../workflow-designer/clearcollection-t-activity-designer.md) [RemoveFromCollection \<T >](../workflow-designer/removefromcollection-t-activity-designer.md)