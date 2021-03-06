---
title: 如何：手动运行托管代码的代码分析
ms.date: 11/04/2019
ms.topic: conceptual
helpviewer_keywords:
- code analysis, running
- run code analysis
ms.assetid: 5086d228-f92e-4515-9708-c5b89b9e9a03
author: mavasani
ms.author: jillfra
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 5fdeb56a0c0f4c5904a00ec53d64dae87aa4e9a5
ms.sourcegitcommit: 92361aac3665a934faa081e1d1ea89a067b01c5b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/17/2020
ms.locfileid: "79431379"
---
# <a name="how-to-run-code-analysis-manually-for-managed-code-requires-visual-studio-2019-version-165-or-later"></a>如何：手动运行托管代码的代码分析（需要 Visual Studio 2019 版本 16.5 或更高版本）
默认情况下，.NET 编译器平台 （"Roslyn"） 代码分析器通过执行实时分析以及生成期间，在键入时分析 C# 或 Visual Basic 代码。 因此，您通常不需要手动触发代码分析。 但是，在某些情况下，您可能需要手动触发代码分析：

- 默认情况下，实时代码分析仅针对 Visual Studio 中的打开文件执行分析器。 但是，您可能有兴趣查看特定项目或解决方案中所有文件的代码分析警告。 如果是这样，您需要在项目或解决方案上触发一次代码分析。 或者，您可以启用连续实时代码分析，以便对整个解决方案执行。 有关详细信息，请参阅[如何：为托管代码配置实时代码分析范围](./configure-live-code-analysis-scope-managed-code.md)。
- 与连续实时分析或生成时间分析，您可能更喜欢按需代码分析执行工作流。 如果是这样，您可以在实时分析和/或生成期间禁用分析器执行。 有关禁用分析的信息，请参阅[如何禁用源代码分析](disable-code-analysis.md)。 然后，您希望在项目或解决方案上手动触发一次代码分析。 

### <a name="run-code-analysis-manually"></a>手动运行代码分析

1. 在**解决方案资源管理器中**，单击项目。

2. 在 **"分析"** 菜单上，单击"*在项目名称***上运行代码分析**"。

代码分析将在后台开始执行。 您应该在面向左下角的可视化工作室状态栏中看到项目 **>运行代码分析\<** 消息。 完成代码分析后，状态消息将更改为**完成\<>项目的代码分析**。 使用所有代码分析诊断，错误列表将很快刷新。
