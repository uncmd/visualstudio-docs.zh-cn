---
title: 错误：Web 服务器找不到请求的资源 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
ms.assetid: 1ceeaf30-918c-42bb-ace1-96944530fef3
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 555bb56ee84b7bc48f6b6453c11daef366f97e49
ms.sourcegitcommit: c150d0be93b6f7ccbe9625b41a437541502560f5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/10/2020
ms.locfileid: "75845122"
---
# <a name="error-the-web-server-could-not-find-the-requested-resource"></a>错误：Web 服务器未能找到请求的资源
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

为了安全起见，IIS 已返回泛型错误。  
  
 一个可能的原因是服务器的安全配置。 IIS 6.0 和早期版本使用名为 URLScan 的外接程序来筛选出可疑请求和格式不正确的请求。 IIS 7.0 具有用于实现同一目的的内置请求筛选。 在这两种情况下，过度限制性请求筛选可防止 Visual Studio 调试服务器。  
  
 导致此错误的可能原因有很多。 几个最常见的原因包括：文件系统中的 IIS 安装或配置、网站配置或权限有问题。 您可以尝试使用浏览器访问资源。 根据 IIS 的配置方式，您可能必须在服务器上使用本地浏览器或检查 IIS 错误日志以获取详细的错误消息。  
  
 有关 IIS 的疑难解答的详细信息，请参阅 [IIS 管理](https://www.iis.net/learn/manage/provisioning-and-managing-iis/iis-management-and-administration)。  
  
## <a name="see-also"></a>请参阅  
 [UrlScan 安全工具](/iis/extensions/working-with-urlscan/urlscan-3-reference)   
 [错误：Web 服务器已被锁定，并阻止 DEBUG 谓词](../debugger/error-the-web-server-has-been-locked-down-and-is-blocking-the-debug-verb.md)
