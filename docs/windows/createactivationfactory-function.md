---
title: CreateActivationFactory 函数
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::CreateActivationFactory
helpviewer_keywords:
- CreateActivationFactory function
ms.assetid: a1a53e04-6757-4faf-a4c8-ecf06e43b959
ms.openlocfilehash: dc8bfebffcb8970876e38e8424cab5e780a13341
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50532413"
---
# <a name="createactivationfactory-function"></a>CreateActivationFactory 函数

创建为可由 Windows 运行时激活的指定类生成实例的工厂。

## <a name="syntax"></a>语法

```cpp
template<typename Factory>
   inline HRESULT STDMETHODCALLTYPE CreateActivationFactory(
      _In_ unsigned int *flags,        _In_ const CreatorMap* entry,
      REFIID riid,
   _Outptr_ IUnknown **ppFactory) throw();
```

### <a name="parameters"></a>参数

*flags*<br/>
一个或多个组合[RuntimeClassType](../windows/runtimeclasstype-enumeration.md)枚举值。

*entry*<br/>
指向[CreatorMap](../windows/creatormap-structure.md)包含有关参数的初始化和注册信息*riid*。

*riid*<br/>
引用接口 id。

*ppFactory*<br/>
如果此操作成功，完成到激活工厂的指针。

## <a name="return-value"></a>返回值

如果成功，则为 S_OK；否则为指示错误的 HRESULT。

## <a name="remarks"></a>备注

如果发出断言错误模板参数*工厂*不会派生自接口`IActivationFactory`。

## <a name="requirements"></a>要求

**标头：** module.h

**命名空间：** Microsoft::WRL

## <a name="see-also"></a>请参阅

[Microsoft::WRL::Wrappers::Details 命名空间](../windows/microsoft-wrl-wrappers-details-namespace.md)