---
title: AutoMark | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: c4de965e-0364-4f78-9936-1f509e85df74
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 4fb849b43e21010d9183f53e31ccf6bbc70736b6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MTE95
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2019
ms.locfileid: "68157186"
---
# <a name="automark"></a>AutoMark
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

“AutoMark”选项指定两次 Windows 软件性能计数器事件收集相隔的毫秒数  。 在“WinCounter”选项中指定 Windows 性能计数器  。  
  
 命令行上只能指定一个“AutoMark”选项  。 请注意，由“AutoMark”指定的 WinCounter 采样间隔独立于主采样间隔   。  
  
## <a name="syntax"></a>语法  
  
```  
VSPerfCmd.exe /Start:Method /WinCounter:Path /AutoMark:Milliseconds  
```  
  
#### <a name="parameters"></a>参数  
 `Milliseconds`  
 指定两次 Windows 性能计数器事件收集相隔的毫秒数。  
  
## <a name="required-options"></a>必需选项  
 WinCounter：  `Path`  
 指定要收集的 Windows 性能计数器。 使用检测方法时，可以指定多个 Windows 计数器。 使用采样方法时，只可指定一个软件计数器。 “WinCounter”选项必须在包含“Start”选项的命令行中进行指定   。  
  
## <a name="example"></a>示例  
 在此示例中，为两个 Windows 性能计数器设置了 1000 毫秒的采样间隔。  
  
```  
VSPerfCmd.exe /Start:Trace /Output:TestApp.exe.vsp /WinCounter:"\Process(*)\% Processor Time" /WinCounter:"\ASP.NET\Pages/sec" /AutoMark:1000  
VSPerfCmd.exe /Launch:TestApp.exe  
```  
  
## <a name="see-also"></a>另请参阅  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [分析独立应用程序](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [分析 ASP.NET Web 应用程序](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [分析服务](../profiling/command-line-profiling-of-services.md)
