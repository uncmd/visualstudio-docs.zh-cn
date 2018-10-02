---
title: Groups 元素 |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- VSCT XML schema elements, Groups
- Groups element (VSCT XML schema)
ms.assetid: 740ca4ec-79fa-4b98-8f9a-2a137f9f7f98
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 6780c8827b1ac7df021cb556f58cd6705d9b7061
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47484630"
---
# <a name="groups-element"></a>Groups 元素
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[Groups 元素](https://docs.microsoft.com/visualstudio/extensibility/groups-element)。  
  
包含定义 VSPackage 的命令组的条目。  
  
## <a name="syntax"></a>语法  
  
```  
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
|[Group 元素](../extensibility/group-element.md)|表示单个命令组。|  
|[Groups 元素](../extensibility/groups-element.md)|包含定义 VSPackage 的命令组的条目。|  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[Commands 元素](../extensibility/commands-element.md)|表示 VSPackage 工具栏上的命令的集合。|  
  
## <a name="example"></a>示例  
  
```  
<Groups>  
  <Group guid="cmdSetGuidWidgetCommands" id="groupIDFileEdit">  
    <Parent guid="guidSHLMainMenu" id="IDM_VS_TOOL_MAINMENU"/>  
  </Group>  
</Groups>  
```  
  
## <a name="see-also"></a>请参阅  
 [Vspackage 如何添加用户界面元素](../extensibility/internals/how-vspackages-add-user-interface-elements.md)   
 [命令、菜单和工具栏](../extensibility/internals/commands-menus-and-toolbars.md)
