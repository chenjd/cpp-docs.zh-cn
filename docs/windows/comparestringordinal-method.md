---
title: CompareStringOrdinal 方法
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::Details::CompareStringOrdinal
ms.assetid: ffa997fd-8cd7-40a5-b9e7-f55d40b072f4
ms.openlocfilehash: 61ca0cb6d8afc07b73e33a2e5bc3dc10daacc210
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50593366"
---
# <a name="comparestringordinal-method"></a>CompareStringOrdinal 方法

支持 WRL 基础结构，不应在代码中直接使用。

## <a name="syntax"></a>语法

```cpp
inline INT32 CompareStringOrdinal(
   HSTRING lhs,
   HSTRING rhs)
```

### <a name="parameters"></a>参数

*lhs*<br/>
第一个要比较的 HSTRING。

*rhs*<br/>
要比较的第二个 HSTRING。

## <a name="return-value"></a>返回值

|“值”|条件|
|-----------|---------------|
|-1|*lhs*是小于*rhs*。|
|0|*lhs*等于*rhs*。|
|1|*lhs*大于*rhs*。|

## <a name="remarks"></a>备注

比较两个指定的 HSTRING 对象并返回一个整数，指示二者在排序顺序中的相对位置。

## <a name="requirements"></a>要求

**标头：** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers::Details

## <a name="see-also"></a>请参阅

[Microsoft::WRL::Wrappers::Details 命名空间](../windows/microsoft-wrl-wrappers-details-namespace.md)