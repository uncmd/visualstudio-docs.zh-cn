---
title: DA0005：频繁进行 GC2 收集 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.DA0005
- vs.performance.rules.DAManyGC2Collections
- vs.performance.5
- vs.performance.rules.DA0005
ms.assetid: 8d3f267c-8a74-4cf4-91a5-0b06a76dc2bd
caps.latest.revision: 16
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 31a59bf1f53e2757aa5b26019c36f578cbc3f3c3
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47472256"
---
# <a name="da0005-frequent-gc2-collections"></a>DA0005：频繁进行 GC2 收集
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[DA0005： 频繁进行 GC2 收集](https://docs.microsoft.com/visualstudio/profiling/da0005-frequent-gc2-collections)。  
  
RuleId |DA0005 |  
|类别 |。NET Framework 使用情况 |  
|分析方法 |.NET 内存 |  
|消息 |很多对象被收集在第 2 代垃圾回收。 |  
|消息类型 |警告 |  
  
## <a name="cause"></a>原因  
 第 2 代垃圾回收期间回收大量的 .NET 内存对象。  
  
## <a name="rule-description"></a>规则说明  
 Microsoft .NET 公共语言运行时 (CLR) 提供自动内存管理机制，该机制使用垃圾回收器从应用程序不再使用的对象回收内存。 垃圾回收器是面向生成的，基于大量分配为短期分配的假设。 例如，局部变量应是短期的。 新创建的对象在 0 代中启动，如果在垃圾回收后它们仍然存在，则将提升到 1 代，如果应用程序仍使用它们，则最后将过渡到 2 代。  
  
 收集 0 代中的对象时，通常频率和效率都较高。 收集 1 代中的对象时，通常频率和效率都较低。 最后，应以更低的频率收集 2 代中生存期较长的对象。 2 代回收是完整的垃圾回收运行，也是成本最高的操作。  
  
 第 2 代垃圾回收比例过高时将触发此规则。 如果过多生存期相对较短的对象在第 1 代回收中未被回收，但在 2 代回收中被回收，那么内存管理的成本将很容易过高。 有关详细信息，请参阅 MSDN 网站上 Rico Mariani 关于性能问题的见解的 [Mid-life crisis](http://go.microsoft.com/fwlink/?LinkId=177835)（中年危机）一文。  
  
## <a name="how-to-investigate-a-warning"></a>如何调查警告  
 查看 [.NET 内存数据视图](../profiling/dotnet-memory-data-views.md)报告，了解应用程序的内存分配模式。 使用[对象生存期视图](../profiling/object-lifetime-view.md)来确定哪些程序的数据对象可通过第 2 代，然后被回收。 使用[分配视图](../profiling/dotnet-memory-allocations-view.md)确定这些分配的执行路径。  
  
 有关如何提高垃圾回收性能的信息，请参阅 Microsoft 网站上的 [Garbage Collector Basics and Performance Hints](http://go.microsoft.com/fwlink/?LinkId=148226)（垃圾回收器基础知识和性能提示）。 有关自动垃圾回收的开销的信息，请参阅[大型对象堆揭密](http://go.microsoft.com/fwlink/?LinkId=177836)。


