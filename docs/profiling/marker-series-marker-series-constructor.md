---
title: marker_series::marker_series 构造函数 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- cvmarkersobj/Concurrency, diagnostic::marker_series::marker_series
helpviewer_keywords:
- Concurrency, diagnostic::marker_series constructor
ms.assetid: 042c7d23-f1d8-4e09-9e76-a21c30243790
author: mikejo5000
ms.author: mikejo
manager: jmartens
ms.workload:
- multiple
ms.openlocfilehash: afb15ceed45389d1c442c18cf14e8eaf4150631f
ms.sourcegitcommit: ae6d47b09a439cd0e13180f5e89510e3e347fd47
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2021
ms.locfileid: "99917650"
---
# <a name="marker_seriesmarker_series-constructor"></a>marker_series::marker_series 构造函数
初始化 `marker_series` 类的新实例。

## <a name="syntax"></a>语法

```cpp
marker_series();
marker_series(
   _In_ LPCTSTR _SeriesName
);
marker_series(
   _In_ const GUID* _ProviderGuid
);
marker_series(
   _In_ const GUID* _ProviderGuid,
   _In_ LPCTSTR _SeriesName
);
```

#### <a name="parameters"></a>参数
 `_SeriesName` 要创建的系列的名称。

 `_ProviderGuid` 系列提供程序的 GUID。

## <a name="requirements"></a>要求
 **Header:** *cvmarkersobj.h*

 **命名空间：** Concurrency::diagnostic

## <a name="see-also"></a>请参阅
- [marker_series 类](../profiling/marker-series-class.md)