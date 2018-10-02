---
title: 筛选节点 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f7cae2dc-e9a7-49d4-8be5-58b79868624e
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 2789676505588c2041abfd876a228fc456ee3607
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47471596"
---
# <a name="filter-nodes"></a>筛选节点
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[筛选器节点](https://docs.microsoft.com/visualstudio/designers/filter-nodes)。  
  
在着色器设计器中，筛选节点会将输入（如颜色或纹理样本）转换为形象的颜色值。 这些形象的颜色值通常用于非真实感渲染或用作其他视觉效果的分量。  
  
## <a name="filter-node-reference"></a>筛选节点引用  
  
|节点|详细信息|属性|  
|----------|-------------|----------------|  
|**模糊**|通过高斯函数模糊纹理中的像素。<br /><br /> 它可用于减少纹理中的颜色细节或干扰。<br /><br /> **输入：**<br /><br /> `UV`: `float2`<br /> 要测试的纹素坐标。<br /><br /> **输出：**<br /><br /> `Output`: `float4`<br /> 经过模糊处理的颜色值。|**纹理**<br /> 与模糊过程中使用的采样器关联的纹理寄存器。|  
|**去除饱和度**|减少指定颜色的颜色量。<br /><br /> 删除颜色后，该颜色值将近似于其灰度等效值。<br /><br /> **输入：**<br /><br /> `RGB`: `float3`<br /> 要去除饱和度的颜色。<br /><br /> `Percent`: `float`<br /> 要删除的颜色百分比，以范围 [0, 1] 中的标准值表示。<br /><br /> **输出：**<br /><br /> `Output`: `float3`<br /> 去除饱和度的颜色。|**亮度**<br /> 为红色、绿色和蓝色分量指定的权重。|  
|**边缘检测**|使用 Canny 边缘检测程序检测纹理中的边缘。 边缘像素输出为白色；非边缘像素输出为黑色。<br /><br /> 它可用于识别纹理中的边缘，以便可使用其他效果处理边缘像素。<br /><br /> **输入：**<br /><br /> `UV`: `float2`<br /> 要测试的纹素坐标。<br /><br /> **输出：**<br /><br /> `Output`: `float4`<br /> 如果纹素位于边缘，则为白色；否则为黑色。|**纹理**<br /> 与边缘检测过程中使用的采样器关联的纹理寄存器。|  
|**锐化**|锐化纹理。<br /><br /> 它可用于突出显示纹理中的细节。<br /><br /> **输入：**<br /><br /> `UV`: `float2`<br /> 要测试的纹素坐标。<br /><br /> **输出：**<br /><br /> `Output`: `float4`<br /> 经过模糊处理的颜色值。|**纹理**<br /> 与锐化过程中使用的采样器关联的纹理寄存器。|


