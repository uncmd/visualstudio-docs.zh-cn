---
title: 组元素 |微软文档
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, Groups
- Groups element (VSCT XML schema)
ms.assetid: 740ca4ec-79fa-4b98-8f9a-2a137f9f7f98
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a6383c3c7a28f9aa7778fddcbfe36b237d21323f
ms.sourcegitcommit: 16a4a5da4a4fd795b46a0869ca2152f2d36e6db2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2020
ms.locfileid: "80711179"
---
# <a name="groups-element"></a>Groups 元素
包含定义 VSPackage 的命令组的条目。

## <a name="syntax"></a>语法

```xml
<Groups>
  <Group>... </Group>
  <Group>... </Group>
</Groups>
```

## <a name="attributes-and-elements"></a>特性和元素
 下列各节描述了特性、子元素和父元素。

### <a name="attributes"></a>特性

|特性|描述|
|---------------|-----------------|
|条件|可选。 请参阅[条件属性](../extensibility/vsct-xml-schema-conditional-attributes.md)。|

### <a name="child-elements"></a>子元素

|元素|描述|
|-------------|-----------------|
|[组元素](../extensibility/group-element.md)|表示单个命令组。|
|[组元素](../extensibility/groups-element.md)|包含定义 VSPackage 的命令组的条目。|

### <a name="parent-elements"></a>父元素

|元素|描述|
|-------------|-----------------|
|[命令元素](../extensibility/commands-element.md)|表示 VSPackage 工具栏上的命令集合。|

## <a name="example"></a>示例

```xml
<Groups>
  <Group guid="cmdSetGuidWidgetCommands" id="groupIDFileEdit">
    <Parent guid="guidSHLMainMenu" id="IDM_VS_TOOL_MAINMENU"/>
  </Group>
</Groups>
```

## <a name="see-also"></a>请参阅
- [VS包如何添加用户界面元素](../extensibility/internals/how-vspackages-add-user-interface-elements.md)
- [命令、菜单和工具栏](../extensibility/internals/commands-menus-and-toolbars.md)
