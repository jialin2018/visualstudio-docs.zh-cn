---
title: NotifyDebuggerOfWaitCompletion 方法 |Microsoft Docs
description: 了解 NotifyDebuggerOfWaitCompletion 方法，该方法是调试器使用的占位符作为断点目标。
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- NotifyDebuggerOfWaitCompletion method, Task class [.NET Framework debug engines]
ms.assetid: 841c5908-4f3f-400b-a7b0-96a95f362817
author: acangialosi
ms.author: anthc
manager: jmartens
ms.workload:
- vssdk
ms.openlocfilehash: b62b613950f9fd6c8ce18969c126a6e74a154b58
ms.sourcegitcommit: ae6d47b09a439cd0e13180f5e89510e3e347fd47
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2021
ms.locfileid: "99851291"
---
# <a name="notifydebuggerofwaitcompletion-method"></a>NotifyDebuggerOfWaitCompletion 方法
调试器使用的占位符方法作为断点目标。 此方法不能内联或优化。

 **命名空间：** <xref:System.Threading.Tasks?displayProperty=fullName>

 **Assembly：** mscorlib (*mscorlib.dll*) 

## <a name="syntax"></a>语法

```vb
private void NotifyDebuggerOfWaitCompletion()
```

## <a name="remarks"></a>备注
 如果设置了调试器通知位，则与任务的所有联接操作都应调用此方法。

## <a name="requirements"></a>要求

## <a name="see-also"></a>另请参阅
- [Task 类](../../extensibility/debugger/task-class-internal-members.md)
