---
title: IDebugPortEvents2：： Event |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortEvents2::Event
helpviewer_keywords:
- IDebugPortEvents2::Event
ms.assetid: 5cc813f7-04a1-4462-9ea7-fbddcf0e0143
author: acangialosi
ms.author: anthc
manager: jmartens
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: bcf8a827f09c1b8d0e83b92f7729635cbb0f7f18
ms.sourcegitcommit: ae6d47b09a439cd0e13180f5e89510e3e347fd47
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2021
ms.locfileid: "99896170"
---
# <a name="idebugportevents2event"></a>IDebugPortEvents2::Event
此方法发送表示在端口上创建和销毁进程和程序的事件。

## <a name="syntax"></a>语法

```cpp
HRESULT Event(
   IDebugCoreServer2* pServer,
   IDebugPort2*       pPort,
   IDebugProcess2*    pProcess,
   IDebugProgram2*    pProgram,
   IDebugEvent2*      pEvent,
   REFIID             riidEvent
);
```

```csharp
int Event(
   IDebugCoreServer2 pServer,
   IDebugPort2       pPort,
   IDebugProcess2    pProcess,
   IDebugProgram2    pProgram,
   IDebugEvent2      pEvent,
   ref Guid          riidEvent
);
```

## <a name="parameters"></a>parameters
`pMachine`\
中表示 (调试服务器的 [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md) 对象，该对象针对发生事件的) 的每个实例都有一个 [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] 。

`pPort`\
中一个 [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) 对象，该对象表示发生事件的端口。

`pProcess`\
中一个 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) 对象，该对象表示发生事件的进程。

`pProgram`\
中一个 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) 对象，该对象表示发生事件的程序。

`pEvent`\
中标识事件的 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) 对象。 可能的事件如下所示：

- [IDebugProcessCreateEvent2](../../../extensibility/debugger/reference/idebugprocesscreateevent2.md)

- [IDebugProcessDestroyEvent2](../../../extensibility/debugger/reference/idebugprocessdestroyevent2.md)

- [IDebugProgramCreateEvent2](../../../extensibility/debugger/reference/idebugprogramcreateevent2.md)

- [IDebugProgramDestroyEvent2](../../../extensibility/debugger/reference/idebugprogramdestroyevent2.md)

`riidEvent`\
中事件的 GUID。 由于在调用此方法之前该事件会强制转换为 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) ，因此，此标识符可以更轻松地确定要发送的事件。

## <a name="return-value"></a>返回值
 如果成功， `S_OK` 则返回; 否则返回错误代码。

## <a name="see-also"></a>另请参阅
- [IDebugPortEvents2](../../../extensibility/debugger/reference/idebugportevents2.md)
- [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)
