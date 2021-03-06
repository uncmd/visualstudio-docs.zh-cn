---
title: LC 任务 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#LC
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, LC task
- LC task [MSBuild]
ms.assetid: d5a53472-6f2a-42b8-a6db-593ca99c9790
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0bbc6463247142ecde20fb2d054d9bd59304c4ec
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MTE95
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "65694113"
---
# <a name="lc-task"></a>LC 任务
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

包装 LC.exe 文件，它可从 .licx 文件生成 .license 文件。 有关 LC.exe 的详细信息，请参阅 [Lc.exe (License Compiler)](https://msdn.microsoft.com/library/2de803b8-495e-4982-b209-19a72aba0460)（Lc.exe（许可证编译器））。  
  
## <a name="parameters"></a>参数  
 下表描述了 `LC` 任务的参数。  
  
|参数|说明|  
|---------------|-----------------|  
|`LicenseTarget`|必选 <xref:Microsoft.Build.Framework.ITaskItem> 参数。<br /><br /> 指定将为其生成 .licenses 文件的可执行文件。|  
|`NoLogo`|可选 `Boolean` 参数。<br /><br /> 取消显示 Microsoft 启动版权标志。|  
|`OutputDirectory`|可选 `String` 参数。<br /><br /> 指定用来放置输出 .licenses 文件的目录。|  
|`OutputLicense`|可选 <xref:Microsoft.Build.Framework.ITaskItem> 输出参数。<br /><br /> 指定 .licenses 文件的名称。 如果不指定名称，则会使用 .licx 文件的名称，且 .licenses 文件会放在包含此 .licx 文件的目录中。|  
|`ReferencedAssemblies`|可选 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 参数。<br /><br /> 指定要在生成 .licenses 文件时加载的引用组件。|  
|`SdkToolsPath`|可选 `String` 参数。<br /><br /> 指定 SDK 工具（例如 resgen.exe）的路径。|  
|`Sources`|必选 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 参数。<br /><br /> 指定包含许可使用的组件的项，这些组件将要包含在 .licenses 文件中。 有关详细信息，请参阅 [Lc.exe (License Compiler)](https://msdn.microsoft.com/library/2de803b8-495e-4982-b209-19a72aba0460)（Lc.exe（许可证编译器））中的 `/complist` 开关的文档。|  
  
 除上面列出的参数外，此任务还从 <xref:Microsoft.Build.Tasks.ToolTaskExtension> 类继承参数，后者自身继承自 <xref:Microsoft.Build.Utilities.ToolTask> 类。 有关这些其他参数及其说明的列表，请参阅 [ToolTaskExtension 基类](../msbuild/tooltaskextension-base-class.md)。  
  
## <a name="example"></a>示例  
 下例使用 `LC` 任务来编译许可证。  
  
```  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
<!-- Item declarations, etc -->  
  
    <Target Name="CompileLicenses">  
        <LC  
            Sources="@(LicxFile)"  
            LicenseTarget="$(TargetFileName)"  
            OutputDirectory="$(IntermediateOutputPath)"  
            OutputLicenses="$(IntermediateOutputPath)$(TargetFileName).licenses"  
            ReferencedAssemblies="@(ReferencePath);@(ReferenceDependencyPaths)">  
  
            <Output  
                TaskParameter="OutputLicenses"  
                ItemName="CompiledLicenseFile"/>  
        </LC>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>请参阅  
 [任务](../msbuild/msbuild-tasks.md)   
 [任务参考](../msbuild/msbuild-task-reference.md)
