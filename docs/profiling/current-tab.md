---
title: “当前”选项卡 | Microsoft Docs
description: 选择线程视图的“当前”选项卡以查看 CPU 线程段或阻塞段的调用堆栈。 还提供了有关 DirectX 段的信息。
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.reportnav.current
helpviewer_keywords:
- Concurrency Visualizer, Callstack at Selection Point
ms.assetid: 2c7b1ae5-3756-4795-bc59-f6bb113f2ba5
author: mikejo5000
ms.author: mikejo
manager: jmartens
ms.workload:
- multiple
ms.openlocfilehash: 4125a40ea0be18cceb99e7f3a8118a10d26a5437
ms.sourcegitcommit: ae6d47b09a439cd0e13180f5e89510e3e347fd47
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2021
ms.locfileid: "99955861"
---
# <a name="current-tab"></a>“当前”选项卡
如果选择一个 CPU 线程段，则通过单击“当前”选项卡，可以查看时间线中最接近当前选择点的调用堆栈（如果有）。  在这种情况下，选择点由时间线上方的黑色箭头或插入符号来表示。 选择阻塞段时，将不显示插入符号，因为没有任何执行操作。 但是，仍会突出显示该段，并显示调用堆栈。

 “当前”选项卡还显示有关 DirectX 活动段、标记和 I/O 访问的信息。  对于 DirectX 活动段，将会显示有关硬件队列如何处理 DMA 数据包的信息。  对于标记，将会显示有关说明和标记类型的信息。  对于 I/O 访问，将会显示有关文件和读取或写入字节数的信息。

## <a name="see-also"></a>请参阅
- [线程视图](../profiling/threads-view-parallel-performance.md)