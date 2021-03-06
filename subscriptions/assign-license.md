---
title: 将许可证分配给 Visual Studio 订阅 | Microsoft Docs
author: evanwindom
ms.author: lank
manager: lank
ms.assetid: 4e529a43-7aed-4eee-895d-862a631952df
ms.date: 03/02/2020
ms.topic: conceptual
description: 了解管理员如何将许可证分配给订阅者
ms.openlocfilehash: 0810cf9d24f6ac218db59eea87a1c092abaa2a3f
ms.sourcegitcommit: 1b7412f1a5b039b2b294c6001013f399ea7aa5bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/29/2020
ms.locfileid: "82564155"
---
# <a name="assign-licenses-in-the-visual-studio-subscriptions-administration-portal"></a>在 Visual Studio 订阅管理门户中分配许可证
作为 Visual Studio 订阅管理员，你可以使用管理门户为个人用户和用户组分配订阅。

对于用户组，你可以选择分配订阅的方式。  
- 可以一次分配一个订阅。
- 也可以使用 [批量添加](assign-license-bulk.md)功能快速轻松地上传订阅者列表及其订阅信息。
- 如果你的组织使用 Microsoft Azure Active Directory (Azure AD)，则可以使用 Azure AD 组将订阅分配给用户组。  （此功能正在分阶段部署，你的组织可能无法立即使用。）


## <a name="add-a-single-subscriber"></a>添加单个订阅者
下面介绍如何为新用户分配 Visual Studio 订阅，以便他们可以访问订阅权益。

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4vpPh]


1. 登录[管理门户](https://manage.visualstudio.com)。
2. 要为单个 Visual Studio 订阅者分配许可证，请在表的顶部选择“添加”  ，然后选择“单个订阅者”  。
   > [!div class="mx-imgBorder"]
   > ![添加单个订阅者](_img/assign-license-add/add-subscriber-individual.png)
3. 在表单域中输入新订阅者的信息。 如果你的组织使用 Azure Active Directory，则“姓名”字段可充当搜索功能，用于查找当前目录中的用户，以便从搜索结果中选择正确的用户  。 当你选择该用户后，系统会自动填充登录电子邮件和通知电子邮件。
   > [!div class="mx-imgBorder"]
   > ![订阅者详细信息](_img/assign-license-add/subscriber-details.png)

    如果希望此订阅者在登录 [Visual Studio 订阅门户](https://my.visualstudio.com?wt.mc_id=o~msft~docs)时可以访问软件下载，请务必将“下载设置”部分中的下载切换保持启用状态  。 如果选择禁用下载，用户将无法访问软件下载，但仍可访问订阅中包含的所有其他权益。
   > [!div class="mx-imgBorder"]
   > ![下载的访问权限](media/access-to-downloads.png)

    如果要向订阅添加自己的引用说明，则可以在“添加引用”部分执行操作  。
   > [!div class="mx-imgBorder"]
   > ![向每个订阅添加自己的引用说明](media/add-subscriber-reference-notes.png)

    完成选择选项和输入订阅者数据后，选择“添加订阅者”弹出窗口底部的“添加”   。
   > [!div class="mx-imgBorder"]
   > ![选择“添加”按钮](media/add-button.png)

## <a name="resend-assignment-emails"></a>重新发送分配电子邮件
添加订阅者后，系统会向新订阅者自动发送一封分配电子邮件，为其提供进一步说明。 通过选中订阅者和单击顶部菜单中的“重新发送”按钮，可以随时再次发送分配电子邮件。   若要向多个用户重新发送电子邮件，请在选择订阅者时按住 Ctrl  键。  单击“重新发送”  按钮后，会看到一个对话框，要求确认是否要向这些订阅者重新发送。  

## <a name="see-also"></a>请参阅
- [Visual Studio 文档](https://docs.microsoft.com/visualstudio/)
- [Azure DevOps 文档](https://docs.microsoft.com/azure/devops/)
- [Azure 文档](https://docs.microsoft.com/azure/)
- [Microsoft 365 文档](https://docs.microsoft.com/microsoft-365/)


## <a name="next-steps"></a>后续步骤
- 有很多用户要添加？  了解如何将订阅分配给[多个订阅者](assign-license-bulk.md)。
- 需要帮助？  联系 [Visual Studio 管理和订阅支持](https://visualstudio.microsoft.com/support/support-overview-vs)。


