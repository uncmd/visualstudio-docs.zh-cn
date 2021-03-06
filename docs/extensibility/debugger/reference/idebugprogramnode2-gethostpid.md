---
title: IDebugProgramnode2：：获取HostPid |微软文档
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramNode2::GetHostPid
helpviewer_keywords:
- IDebugProgramNode2::GetHostPid
ms.assetid: e65b4b15-46d8-4ca7-9456-2b4c078f7cf9
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 1257bda23bcdfaceb58d1d087ae2848be8f969b1
ms.sourcegitcommit: 16a4a5da4a4fd795b46a0869ca2152f2d36e6db2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2020
ms.locfileid: "80722033"
---
# <a name="idebugprogramnode2gethostpid"></a>IDebugProgramNode2::GetHostPid
获取承载程序的进程的系统进程标识符。

## <a name="syntax"></a>语法

```cpp
HRESULT GetHostPid ( 
   AD_PROCESS_ID * pdwHostPid
);
```

```csharp
int GetHostPid ( 
   out AD_PROCESS_ID pdwHostPid
);
```

## <a name="parameters"></a>参数
`pdwHostPid`\
[出]返回托管进程的系统进程标识符。

## <a name="return-value"></a>返回值
 如果成功，返回`S_OK`;否则，返回错误代码。

## <a name="example"></a>示例
 下面的示例演示如何实现[IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)接口`CProgram`的简单对象实现此方法。

```cpp
HRESULT CProgram::GetHostPid(AD_PROCESS_ID* pdwHostPid) {
   // Check for valid argument.
   if (pdwHostPid == NULL)
     return E_INVALIDARG;

   // Get the process identifier of the calling process.
   pdwHostPid->ProcessIdType = AD_PROCESS_ID_SYSTEM;
   pdwHostPid->ProcessId.dwProcessId = GetCurrentProcessId();
   return S_OK;
}
```

## <a name="see-also"></a>请参阅
- [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)
