---
title: 编译器错误 C3510
ms.date: 11/04/2016
f1_keywords:
- C3510
helpviewer_keywords:
- C3510
ms.assetid: c48387bc-0300-4a4d-97f7-3fb90f82a451
ms.openlocfilehash: dbb65628aa6e0da94a91a59724ca8e1cd5b56491
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50620871"
---
# <a name="compiler-error-c3510"></a>编译器错误 C3510

找不到依赖类型库 type_lib

[no_registry](../../preprocessor/no-registry.md)并[auto_search](../../preprocessor/auto-search.md)传递给`#import`但编译器找不到引用的类型库。

若要解决此错误，请确保所有类型库和被引用的类型库都都可用于编译器。

下面的示例生成 C3510:

假设以下两个类型库生成，并且 C3510a.tlb 已被删除或不在路径上。

```
// C3510a.idl
[uuid("f87070ba-c6d9-405c-a8e4-8cd9ca25c12b")]
library C3510aLib
{
   [uuid("f87070ba-c6d9-405c-a8e4-8cd9ca25c12c")]
   enum E_C3510
   {
      one, two, three
   };
};
```

然后第二个类型库的源代码：

```
// C3510b.idl
// post-build command: del /f C3510a.tlb
[uuid("f87070ba-c6d9-405c-a8e4-8cd9ca25c12e")]
library C3510bLib
{
   importlib ("C3510a.tlb");
   [uuid("f87070ba-c6d9-405c-a8e4-8cd9ca25c12d")]
   struct S_C3510 {
      enum E_C3510 e;
   };
};
```

然后客户端代码：

```
// C3510.cpp
#import "c3510b.tlb" no_registry auto_search   // C3510
int main() {
   C3510aLib::S_C4336 ccc;
}
```