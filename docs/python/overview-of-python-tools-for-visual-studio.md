---
title: "Visual Studio (Windows) 中的 Python 支持概述 | Microsoft Docs"
description: "概述了 Visual Studio 中适用于 Python 的功能（亦称为“针对 Visual Studio 的 Python 工具 (PTVS)”），包括跨 Visual Studio 版本的问题和解答 (FAQ) 以及功能支持矩阵。"
ms.custom: 
ms.date: 01/09/2018
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-python
ms.devlang: python
ms.tgt_pltfrm: 
ms.topic: hero-article
caps.latest.revision: 
author: kraigb
ms.author: kraigb
manager: ghogen
ms.workload:
- python
- data-science
ms.openlocfilehash: 4d2033e8912d6010adc8e83108a8b9ece1aa4b0e
ms.sourcegitcommit: ba29e4d37db92ec784d4acf9c6e120cf0ea677e9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2018
---
# <a name="working-with-python-in-visual-studio-windows"></a>在 Visual Studio (Windows) 中使用 Python

Python 是一种受欢迎的编程语言，它可靠、灵活、易于学习、可在所有操作系统上免费使用，并且强大的开发人员社区和很多免费库都支持它。 Python 支持所有开发方式，包括 Web 应用程序、Web 服务、桌面应用、脚本编写和科学计算，许多高校人员、科学家、业余和专业开发人员都在使用 Python。 可以在 [python.org](https://www.python.org) 和 [Python for Beginners](https://www.python.org/about/gettingstarted/)（面向初学者的 Python）中了解有关该语言的详细信息。

Windows 上的 Visual Studio 通过 Python 开发和数据科学工作负载 (Visual Studio 2017) 和免费的针对 Visual Studio 的 Python 工具扩展（Visual Studio 2015 及更早版本），为 Python 语言提供[开源代码](https://github.com/Microsoft/ptvs)支持。 Python 目前不支持在 Visual Studio for Mac 中使用，但可通过 Visual Studio Code 在 Mac 和 Linux 上使用（请参阅[问题和解答](#questions-and-answers)）。

若要开始使用 Python，请执行以下操作：

- 按照[安装说明](installing-python-support-in-visual-studio.md)安装 Python 工作负载
- 阅读一个或多个指导如何创建项目的快速入门教程。 如果不确定，可先从[从模板创建项目](quickstart-02-python-in-visual-studio-project-from-template.md)开始。
- 按照[在 Visual Studio 中使用 Python](tutorial-working-with-python-in-visual-studio-step-01-create-project.md) 教程操作，获得完整的端到端体验。
- 然后使用下表中的链接了解与 Python 相关的功能，以及 Visual Studio 本身的功能。

| 功能 | 说明 | Visual Studio 常规文档 |
| --- | --- | --- |
| [Visual Studio 项目系统](managing-python-projects-in-visual-studio.md) | 隐式选取 Python 代码的文件夹结构，同时允许显式控制以便标识应用代码、测试代码、网页、JavaScript、生成脚本等等。 | [Visual Studio 中的解决方案和项目](../ide/solutions-and-projects-in-visual-studio.md) |
| [项目模板](managing-python-projects-in-visual-studio.md#project-templates) | 快速创建用于控制台、Web、Azure、数据科学和其他类型项目的项目结构 | [Visual Studio 模板](../ide/creating-project-and-item-templates.md#visual-studio-templates) |
| 多个解释器支持 | 支持各种版本的 CPython 和 IronPython。 | n/a |
| IPython 支持 | 包括对内联图的 REPL 中的 IPython/Jupyter 的支持以及对.NET 和 Windows Presentation Foundation (WPF) 的支持。 | n/a |
| [多种多样的编辑、IntelliSense 和代码理解](editing-python-code-in-visual-studio.md) | 包括语法着色、跨所有代码和库的自动完成、[代码格式设置](formatting-python-code.md)、签名帮助、类视图、转到定义、查找所有引用、代码片段、[重构](refactoring-python-code.md)、[PyLint](linting-python-code.md)等等。 | [在代码和文本编辑器中编写代码](../ide/writing-code-in-the-code-and-text-editor.md) |
| [交互窗口](python-interactive-repl-in-visual-studio.md) | 能够轻松突出显示代码的某一部分，然后将其发送到交互窗口，为 Python 提供快速的 REPL 体验。 | n/a |
| [功能完备的调试](debugging-python-in-visual-studio.md) | 无论有没有 Visual Studio 项目，均可完成调试，包括可对现有可执行文件进行调试、[Python/C++ 混合模式调试](debugging-mixed-mode-c-cpp-python-in-visual-studio.md)、对 Windows/Linux/Mac 的 [Linux 进行远程调试](debugging-python-code-on-remote-linux-machines.md)、[对 Azure 进行远程调试](debugging-remote-python-code-on-azure.md)，以及在交互窗口中进行调试。 | [在 Visual Studio 中进行调试](../debugger/debugging-in-visual-studio.md) |
| [具有丰富报表的分析工具](profiling-python-code-in-visual-studio.md) | 了解应用程序中所用的时间，包括比较不同分析运行之间的性能差异。 | [分析工具](../profiling/profiling-tools.md)（并非所有 Visual Studio 分析功能都可用于 Python） |
| [单元测试工具](unit-testing-python-in-visual-studio.md) | 在 Visual Studio 测试资源管理器中发现、运行和管理测试，并且可轻松调试单元测试。 | [单元测试代码](../test/unit-test-your-code.md) |

Python 工作负载还包括[用于 Python 的 Azure SDK](azure-sdk-for-python.md)，它用于简化从 Windows、Mac OS X 和 Linux 应用使用 Azure 服务的过程。

有关视频介绍，请观看 Microsoft Virtual Academy 上的短期课程[针对 Visual Studio 的 Python 工具](https://mva.microsoft.com/en-US/training-courses/python-tools-for-visual-studio-2017-18121)（总共 22 分钟左右）。 

> [!VIDEO https://mva.microsoft.com/en-US/training-courses-embed/python-tools-for-visual-studio-2017-18121/Video-Installing-Visual-Studio-Python-Support-go1id3LWE_1705918567]

## <a name="questions-and-answers"></a>问题和解答

**问：是否可通过 Visual Studio for Mac 获得 Python 支持？**

答： 此次不行，尽管是在 [UserVoice](https://visualstudio.uservoice.com/forums/563332-visual-studio-for-mac/suggestions/18670291-python-tools-for-visual-studio-mac) 上提出请求的。 [Visual Studio for Mac](/visualstudio/mac/) 文档会标识当前支持的开发类型。 同时，Windows、Mac 和 Linux 上的 Visual Studio Code 可[通过可用扩展与 Python 配合工作](https://code.visualstudio.com/docs/languages/python)。

**问：构建 Python UI 可以使用什么工具？**

答： 该领域的主要产品是 [Qt 项目](https://www.qt.io/qt-for-application-development/)，其中与 Python 的绑定称为 [PySide（官方绑定）](http://wiki.qt.io/PySide)（另请参阅 [PySide 下载](https://download.qt.io/official_releases/pyside/.)）和 [PyQt](https://wiki.python.org/moin/PyQt)。 目前，Visual Studio 中的 Python 支持不包括用于 UI 开发的任何特定工具。

**问：Python 项目是否可以生成独立的可执行文件？**

答： Python 通常是一种解释型语言，其代码在适合 Python 功能的环境（如 Visual Studio 和 Web 服务器）中按需运行。 目前，Visual Studio 本身不提供创建独立可执行文件的方法，它本质上是一个具有嵌入式 Python 解释器的程序。 但是，如 [StackOverflow](http://stackoverflow.com/questions/5458048/how-to-make-a-python-script-standalone-executable-to-run-without-any-dependency) 所述，Python 社区中有多种方法可以创建可执行文件。 如博客文章 [Using CPython's Embeddable Zip File](https://blogs.msdn.microsoft.com/pythonengineering/2016/04/26/cpython-embeddable-zip-file/)（使用 CPython 可嵌入 zip 文件）中所述，CPython 还支持嵌入到本机应用程序中。

## <a name="features-matrix"></a>功能矩阵

如[安装指南](installing-python-support-in-visual-studio.md)所述，可在以下版本的 Visual Studio 中安装 Python 支持：

- [Visual Studio 2017（所有版本）](https://www.visualstudio.com/vs/)
- [Visual Studio 2015（所有版本）](https://www.visualstudio.com/zh-cn/downloads/visual-studio-2015-downloads-vs)
- Visual Studio 2013 Community Edition
- Visual Studio 2013 Express for Web 和 Update 2 或更高版本
- Visual Studio 2013 Express for Desktop 和 Update 2 或更高版本
- Visual Studio 2013（Pro 或更高版本）
- Visual Studio 2012（Pro 或更高版本）
- Visual Studio 2010 SP1（Pro 或更高版本；需要 .NET 4.5）

Visual Studio 各版本支持的功能：

| Python 支持 | 2017 | 2015 | 2013 Comm | 2013 Desktop | 2013 Web | 2013 Pro+ | 2012 Pro+ | 2010 SP1 Pro+ |
| --- | --- | --- | --- | --- | --- | --- | --- | ---|
| 多个解释器管理 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 自动检测热门解释器 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 添加自定义解释器 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 虚拟环境 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| Pip/易于安装 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
<br/>

| 项目系统 | 2017 | 2015 | 2013 Comm | 2013 Desktop | 2013 Web | 2013 Pro+ | 2012 Pro+ | 2010 SP1 Pro+ |
| --- | --- | --- | --- | --- | --- | --- | --- | ---|
| 根据现有代码新建项目 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 显示所有文件 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 源代码管理 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| Git 集成 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004;<sup>1</sup> | &#10007; |
<br/>

| 编辑 | 2017 | 2015 | 2013 Comm | 2013 Desktop | 2013 Web | 2013 Pro+ | 2012 Pro+ | 2010 SP1 Pro+ |
| --- | --- | --- | --- | --- | --- | --- | --- | ---|
| 语法突出显示 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 自动完成 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 签名帮助 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 快速信息 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 对象浏览器/类视图 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 导航栏 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 转到定义 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 导航到 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 查找所有引用 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 自动缩进 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 代码格式设置 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 重构 - 重命名 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 重构 - 提取方法 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 重构 - 添加/删除导入 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| PyLint | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
<br/>

| 交互窗口 | 2017 | 2015 | 2013 Comm | 2013 Desktop | 2013 Web | 2013 Pro+ | 2012 Pro+ | 2010 SP1 Pro+ |
| --- | --- | --- | --- | --- | --- | --- | --- | ---|
| 交互窗口 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 具有内联关系图的 IPython | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
<br/>

| 桌面 | 2017 | 2015 | 2013 Comm | 2013 Desktop | 2013 Web | 2013 Pro+ | 2012 Pro+ | 2010 SP1 Pro+ |
| --- | --- | --- | --- | --- | --- | --- | --- | ---|
| 控制台/Windows 应用程序 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| IronPython WPF（带 XAML 设计器） | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| IronPython Windows 窗体 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
<br/>

| Web | 2017 | 2015 | 2013 Comm | 2013 Desktop | 2013 Web | 2013 Pro+ | 2012 Pro+ | 2010 SP1 Pro+ |
| --- | --- | --- | --- | --- | --- | --- | --- | ---|
| Django Web 项目 | &#10004; | &#10004; | &#10004; | &#10007; | &#10004; | &#10004; | &#10004; | &#10004; |
| Bottle Web 项目 | &#10004; | &#10004; | &#10004; | &#10007; | &#10004; | &#10004; | &#10004; | &#10004; |
| Flask Web 项目 | &#10004; | &#10004; | &#10004; | &#10007; | &#10004; | &#10004; | &#10004; | &#10004; |
| Generic Web 项目 | &#10004; | &#10004; | &#10004; | &#10007; | &#10004; | &#10004; | &#10004; | &#10004; |
<br/>

| Azure | 2017 | 2015 | 2013 Comm | 2013 Desktop | 2013 Web | 2013 Pro+ | 2012 Pro+ | 2010 SP1 Pro+ |
| --- | --- | --- | --- | --- | --- | --- | --- | ---|
| 对网站的部署 | &#10004; | &#10004; | &#10004; | &#10007; | &#10004; | &#10004; | &#10004; | &#10004;<sup>2</sup> |
| 对 Web 角色的部署 | &#10004; | &#10004; | &#10004; | &#10007; | &#10004;<sup>4</sup> | &#10004;<sup>4</sup> | &#10004;<sup>3</sup> | &#10007; |
| 对辅助角色的部署 | ? | ? | ? | &#10007; | &#10004;<sup>4</sup> | &#10004;<sup>4</sup> | &#10004;<sup>3</sup> | &#10007; |
| 在 Azure 仿真程序中运行 | ? | ? | ? | &#10007; | &#10004;<sup>4</sup> | &#10004;<sup>4</sup> | &#10004;<sup>3</sup> | &#10007; |
| 远程调试 | &#10004; | &#10004; | &#10004; | &#10007; | &#10004;<sup>6</sup> | &#10004;<sup>8</sup> | &#10004;<sup>8</sup> | &#10007; |
| 服务器资源管理器附加 | &#10004; | &#10004; | &#10004; | &#10007; | &#10004;<sup>7</sup> | &#10004;<sup>7</sup> | &#10007; | &#10007; |
<br/>

| Django 模板 | 2017 | 2015 | 2013 Comm | 2013 Desktop | 2013 Web | 2013 Pro+ | 2012 Pro+ | 2010 SP1 Pro+ |
| --- | --- | --- | --- | --- | --- | --- | --- | ---|
| 调试 | &#10004; | &#10004; | &#10004; | &#10007; | &#10004; | &#10004; | &#10004; | &#10004; |
| 自动完成 | &#10004; | &#10004; | &#10004; | &#10007; | &#10004;<sup>5</sup> | &#10004;<sup>5</sup> | &#10004; | &#10004; |
| CSS 和 JavaScript 的自动完成 | &#10004; | &#10004; | &#10004; | &#10007; | &#10004;<sup>5</sup> | &#10004;<sup>5</sup> | &#10007; | &#10007; |
<br/>

| 调试 | 2017 | 2015 | 2013 Comm | 2013 Desktop | 2013 Web | 2013 Pro+ | 2012 Pro+ | 2010 SP1 Pro+ |
| --- | --- | --- | --- | --- | --- | --- | --- | ---|
| 调试 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 不含项目进行调试 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
| 调试 - 附加到编辑 | &#10004; | &#10004; | &#10004; | &#10004; | &#10007; | &#10004; | &#10004; | &#10004; |
| 混合模式调试 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10007; |
| 远程调试（Windows、Mac OS X、Linux） | &#10004; | &#10004; | &#10004; | &#10004; | &#10007; | &#10004; | &#10004; | &#10004; |
| 调试交互窗口 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; |
<br/>

| 分析 | 2017 | 2015 | 2013 Comm | 2013 Desktop | 2013 Web | 2013 Pro+ | 2012 Pro+ | 2010 SP1 Pro+ |
| --- | --- | --- | --- | --- | --- | --- | --- | ---|
| 分析 | &#10004; | &#10004; | &#10004; | &#10007; | &#10007; | &#10004; | &#10004; | &#10004; |
<br/>

| 测试 | 2017 | 2015 | 2013 Comm | 2013 Desktop | 2013 Web | 2013 Pro+ | 2012 Pro+ | 2010 SP1 Pro+ |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 测试资源管理器 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10007; |
| 运行测试 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10007; |
| 调试测试 | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10004; | &#10007; |
<br/>

1. Visual Studio Tools for Git 扩展中提供了对 Visual Studio 2012 的 Git 支持，可从 [Visual Studio 库](http://visualstudiogallery.msdn.microsoft.com/abafc7d6-dcaa-40f4-8a5e-d6724bdb980c)中获得。

1. 部署到 Azure 网站需要 [Azure SDK for .NET 2.1 - Visual Studio 2010 SP1](http://go.microsoft.com/fwlink/?LinkId=313855)。 更高版本不支持 Visual Studio 2010。

1. 对 Azure Web 角色和辅助角色的支持需要[用于 .NET 2.3 - VS 2012 的 Azure SDK](http://go.microsoft.com/fwlink/?LinkId=323511) 或更高版本。

1. 对 Azure Web 角色和辅助角色的支持需要[用于 .NET 2.3 - VS 2013 的 Azure SDK](http://go.microsoft.com/fwlink/?LinkId=323510) 或更高版本。

1. Visual Studio 2013 中的 Django 模板编辑器具有一些已知问题，可通过安装 Update 2 解决。

1. 需要 Windows 8 或更高版本。 Visual Studio 2013 Express for Web 没有“附加到进程”对话框，但 Azure 网站远程调试仍然可能在服务器资源管理器中使用附加调试器 (Python) 命令。 远程调试需要安装 [Azure SDK for .NET 2.3 - Visual Studio 2013](http://go.microsoft.com/fwlink/?LinkId=323510) 或更高版本。

1. 需要 Windows 8 或更高版本。 使用服务器资源管理器中的附加调试器 (Python) 命令需要 [Azure SDK for .NET 2.3 - Visual Studio 2013](http://go.microsoft.com/fwlink/?LinkId=323510) 或更高版本。

1. 需要 Windows 8 或更高版本。

## <a name="additional-resources"></a>其他资源

- [IIS 和 Python 之间 WFastCGI 桥](https://pypi.python.org/pypi/wfastcgi) (python.org)
- [Microsoft Virtual Academy 上的免费 Phthon 课程](https://mva.microsoft.com/search/SearchResults.aspx#!q=python)
- [Microsoft Virtual Academy 上的“Python 最常见问题”](https://aka.ms/mva-top-python-questions)