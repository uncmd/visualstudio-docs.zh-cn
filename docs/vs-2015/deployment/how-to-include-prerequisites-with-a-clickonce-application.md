---
title: 如何：在 ClickOnce 应用程序中包含先决条件 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
ms.assetid: c66bf0a5-8c93-4e68-a224-3b29ac36fe4d
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 9639da1f735095f6d04a59d1f2302f822423e006
ms.sourcegitcommit: bf2e9d4ff38bf5b62b8af3da1e6a183beb899809
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/22/2020
ms.locfileid: "77557678"
---
# <a name="how-to-include-prerequisites-with-a-clickonce-application"></a>如何：将必备组件与 ClickOnce 应用程序包括在一起
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

你必须先将必备软件的安装程序包下载到开发计算机上，然后才能使用 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 应用程序分发这些软件。 当发布应用程序并选择 **"从与我的应用程序相同的位置下载系统必备组件**" 时，如果安装程序包不在 "**包**" 文件夹中，则会发生错误。  
  
> [!NOTE]
> 若要为 .NET Framework 添加安装程序包，请参阅面向[开发人员 .NET Framework 部署指南](/dotnet/framework/deployment/deployment-guide-for-developers)。  
  
## <a name="Package"></a> 使用 Package.xml 添加安装程序包  
  
1. 在文件资源管理器中，打开“包”文件夹。  
  
     默认情况下，路径为 C:\Program Files\Microsoft Visual Studio 14.0\SDK\Bootstrapper\Packages（32 位系统）和 C:\Program Files (x86)\Microsoft Visual Studio 14.0\SDK\Bootstrapper\Packages（64 位系统）。  
  
2. 为要添加的系统必备组件打开文件夹，然后为已安装的 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 版本打开语言文件夹（例如，“en”用于英语）。  
  
3. 在记事本中，打开“Package.xml”文件。  
  
4. 找到包含 `http://go.microsoft.com/fwlink`的 "**名称**" 元素，并复制 URL。 包括“LinkID”部分。  
  
    > [!NOTE]
    > 如果没有**名称**元素包含 `http://go.microsoft.com/fwlink`，请打开必备组件的根文件夹**中的 fwlink 文件，** 并找到 "  " 字符串。  
  
    > [!IMPORTANT]
    > 某些系统必备组件具有多个安装程序包（例如，用于 32 位或 64 位系统）。 如果多个“名称”元素包含“fwlink”，则必须对每个元素重复剩余步骤。  
  
5. 将该 URL 粘贴到浏览器的地址栏中，然后在系统提示运行或保存时，选择“保存”。  
  
     此步骤将安装程序文件下载到你的计算机中。  
  
6. 将此文件复制到系统必备组件的根文件夹中。  
  
     例如，对于 Windows Installer 4.5 系统必备组件，请将此文件复制到 \Packages\WindowsInstaller4_5 文件夹中。  
  
     现在你可以将安装程序包与你的应用程序一起分发。  
  
## <a name="see-also"></a>另请参阅  
 [如何：与 ClickOnce 应用程序一起安装系统必备组件](../deployment/how-to-install-prerequisites-with-a-clickonce-application.md)
