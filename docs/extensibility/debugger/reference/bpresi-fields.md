---
title: BPRESI_FIELDS |微软文档
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BPRESI_FIELDS
helpviewer_keywords:
- BPRESI_FIELDS enumeration
ms.assetid: 99f17b1e-3e67-4f85-89d6-5c6cf45c8008
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 837bb7d25ab8dea2b146a98cc65d320b58162685
ms.sourcegitcommit: 16a4a5da4a4fd795b46a0869ca2152f2d36e6db2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2020
ms.locfileid: "80737721"
---
# <a name="bpresi_fields"></a>BPRESI_FIELDS
指定要检索的信息，说明断点的成功解析。

## <a name="syntax"></a>语法

```cpp
enum enum_BPRESI_FIELDS {
    BPRESI_BPRESLOCATION = 0x0001,
    BPRESI_PROGRAM       = 0x0002,
    BPRESI_THREAD        = 0x0004,
    BPRESI_ALLFIELDS     = 0xffffffff
};
typedef DWORD BPRESI_FIELDS;
```

```csharp
public enum enum_BPRESI_FIELDS {
    BPRESI_BPRESLOCATION = 0x0001,
    BPRESI_PROGRAM       = 0x0002,
    BPRESI_THREAD        = 0x0004,
    BPRESI_ALLFIELDS     = 0xffffffff
};
```

## <a name="fields"></a>字段
`BPRESI_BPRESLOCATION`\
初始化/使用`bpResLocation`[BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md)结构的（断点分辨率位置）字段。

`BPRESI_PROGRAM`\
初始化/使用`pProgram`结构字段。 `BP_RESOLUTION_INFO`

`BPRESI_THREAD`\
初始化/使用`pThread`结构字段。 `BP_RESOLUTION_INFO`

`BPRESI_ALLFIELDS`\
指定所有字段。

## <a name="remarks"></a>备注
传递给[GetResolutionInfo](../../../extensibility/debugger/reference/idebugbreakpointresolution2-getresolutioninfo.md)方法，指示要初始化[BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md)结构的字段。

这些标志还用于指示在返回该结构时使用`BP_RESOLUTION_INFO`结构的字段并有效。

这些值可以稍微结合`OR`。

## <a name="requirements"></a>要求
标题： msdbg.h

命名空间：微软.VisualStudio.调试器.互通

程序集：微软.VisualStudio.调试器.Interop.dll

## <a name="see-also"></a>请参阅
- [枚举](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md)
- [GetResolutionInfo](../../../extensibility/debugger/reference/idebugbreakpointresolution2-getresolutioninfo.md)
