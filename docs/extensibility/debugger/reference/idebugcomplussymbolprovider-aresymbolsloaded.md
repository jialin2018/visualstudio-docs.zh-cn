---
title: IDebugComPlusSymbolProvider：： AreSymbolsLoaded |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- AreSymbolsLoaded
- IDebugComPlusSymbolProvider::AreSymbolsLoaded
ms.assetid: bbf8707d-f89c-4177-b019-d519f1ec6f4a
author: acangialosi
ms.author: anthc
manager: jmartens
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: df11531cc90081aad45b887066ce0799af771747
ms.sourcegitcommit: ae6d47b09a439cd0e13180f5e89510e3e347fd47
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2021
ms.locfileid: "99928713"
---
# <a name="idebugcomplussymbolprovideraresymbolsloaded"></a>IDebugComPlusSymbolProvider::AreSymbolsLoaded
确定给定应用程序域标识符是否为指定模块加载调试符号。

## <a name="syntax"></a>语法

```cpp
HRESULT AreSymbolsLoaded (
    ULONG32 ulAppDomainID,
    GUID    guidModule
);
```

```csharp
int AreSymbolsLoaded (
    uint ulAppDomainID,
    Guid guidModule
);
```

## <a name="parameters"></a>parameters
`ulAppDomainID`\
中应用程序域的标识符。

`guidModule`\
中模块的唯一标识符。

## <a name="return-value"></a>返回值
如果已加载调试符号，则返回 `S_OK` ; 否则返回 `S_FALSE` 。

## <a name="example"></a>示例
下面的示例演示如何为公开 [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md)接口的 **CDebugSymbolProvider** 对象实现此方法。

```cpp
HRESULT CDebugSymbolProvider::AreSymbolsLoaded(
    ULONG32 ulAppDomainID,
    GUID guidModule
)
{
    HRESULT hr = S_OK;
    CComPtr<CModule> pModule;
    Module_ID idModule(ulAppDomainID, guidModule);

    METHOD_ENTRY( CDebugSymbolProvider::AreSymbolsLoaded );

    IfFalseGo( GetModule( idModule, &pModule ) == S_OK, S_FALSE );
Error:

    METHOD_EXIT( CDebugSymbolProvider::AreSymbolsLoaded, hr );
    return hr;
}
```

## <a name="see-also"></a>另请参阅
- [IDebugComPlusSymbolProvider](../../../extensibility/debugger/reference/idebugcomplussymbolprovider.md)
