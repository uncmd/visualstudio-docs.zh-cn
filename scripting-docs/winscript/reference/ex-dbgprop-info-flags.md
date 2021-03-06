---
title: EX_DBGPROP_INFO_FLAGS | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- EX_DBGPROP_INFO_FLAGS
apilocation:
- scrobj.dll
helpviewer_keywords:
- EX_DBGPROP_INFO_FLAGS
ms.assetid: ee309dfe-9432-4dff-8756-7a8d677f9dcc
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0094d49a7e528d312dc8206b02599651f192c6fb
ms.sourcegitcommit: 184e2ff0ff514fb980724fa4b51e0cda753d4c6e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2019
ms.locfileid: "72575845"
---
# <a name="ex_dbgprop_info_flags"></a>EX_DBGPROP_INFO_FLAGS
用于指定 `ExtendedDebugPropertyInfo` 字段。  
  
## <a name="syntax"></a>语法  
  
```cpp
enum {  
   EX_DBGPROP_INFO_ID  =0x0100,  
   EX_DBGPROP_INFO_NTYPE  =0x0200,  
   EX_DBGPROP_INFO_NVALUE  =0x0400,  
   EX_DBGPROP_INFO_LOCKBYTES  =0x0800,  
   EX_DBGPROP_INFO_DEBUGEXTPROP  =0x1000  
};  
```  
  
## <a name="members"></a>Members  
 EX_DBGPROP_INFO_ID  
 初始化属性的标识符。  
  
 EX_DBGPROP_INFO_NTYPE  
 初始化属性的类型。  
  
 EX_DBGPROP_INFO_NVALUE  
 初始化属性的值。  
  
 EX_DBGPROP_INFO_LOCKBYTES  
 初始化 `plb` 字段。  
  
 EX_DBGPROP_INFO_DEBUGEXTPROP  
 初始化包含 `IDebugExtendedProperty` 接口的 `pDebugExtProp` 字段。  
  
## <a name="see-also"></a>另请参阅  
 [ExtendedDebugPropertyInfo 结构](../../winscript/reference/extendeddebugpropertyinfo-structure.md)   
 [IDebugExtendedProperty 接口](../../winscript/reference/idebugextendedproperty-interface.md)