---
title: 编译器错误 C3273
ms.date: 11/04/2016
f1_keywords:
- C3273
helpviewer_keywords:
- C3273
ms.assetid: 1d2ce9d9-222b-4cab-94e2-d2c1a9f5ebe0
ms.openlocfilehash: 466a9d6687dd5bfdab80ce1dfc9096ef7540ebaa
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50511665"
---
# <a name="compiler-error-c3273"></a>编译器错误 C3273

__finally 不能用于非托管代码中的异常块。

下面的示例生成 C3273：

```
// C3273.cpp
// compile with: /GX
int main()
{
   try
   {
   }
   catch (int)
   {
   }
   __finally   // C3273, remove __finally clause
   {
   }
}
```