---
title: IDebugMethodField：： EnumArguments |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugMethodField::EnumArguments
helpviewer_keywords:
- IDebugMethodField::EnumArguments method
ms.assetid: 3ab55488-2437-4ff6-a9ae-78ea6d7b23a8
author: acangialosi
ms.author: anthc
manager: jmartens
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 6b86fbdb87c0191ea8b43c64a542c37177a8ef1f
ms.sourcegitcommit: ae6d47b09a439cd0e13180f5e89510e3e347fd47
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2021
ms.locfileid: "99900195"
---
# <a name="idebugmethodfieldenumarguments"></a>IDebugMethodField::EnumArguments
为调用方法所需的每个参数的类型创建一个枚举数。

## <a name="syntax"></a>语法

```cpp
HRESULT EnumArguments( 
   IEnumDebugFields** ppParams
);
```

```csharp
int EnumArguments(
   out IEnumDebugFields ppParams
);
```

## <a name="parameters"></a>parameters
`ppParams`\
弄返回一个 [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) 对象，该对象表示参数类型的列表。 如果没有参数，则返回 null 值。

## <a name="return-value"></a>返回值
 如果成功，则返回 S_OK 或返回 S_FALSE （如果没有参数）。 否则，返回错误代码。

## <a name="remarks"></a>备注
 每个元素都是一个 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) 对象，表示每个参数的类型。 调用 [GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md) 方法以检索有关每个参数类型的信息。

 如果参数名称与类型一起需要，请调用 [EnumParameters](../../../extensibility/debugger/reference/idebugmethodfield-enumparameters.md) 方法。

## <a name="see-also"></a>另请参阅
- [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)
- [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [EnumParameters](../../../extensibility/debugger/reference/idebugmethodfield-enumparameters.md)
