---
title: __if_exists 语句
ms.date: 11/04/2016
f1_keywords:
- __if_exists_cpp
helpviewer_keywords:
- identifiers, testing for existence
- symbols, testing for existence
- __if_exists keyword [C++]
ms.assetid: d3eb34b6-f3a9-4063-a286-b62a28c0c7fa
ms.openlocfilehash: 9d5a0b24bb08a9485b2d212058fa8f0bd82e5842
ms.sourcegitcommit: 1819bd2ff79fba7ec172504b9a34455c70c73f10
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/09/2018
ms.locfileid: "51326623"
---
# <a name="ifexists-statement"></a>__if_exists 语句

**__If_exists**语句测试是否存在指定的标识符。 如果该标识符存在，则执行指定的语句块。

## <a name="syntax"></a>语法

```
__if_exists ( identifier ) {
statements
};
```

#### <a name="parameters"></a>参数

|参数|描述|
|---------------|-----------------|
|*identifier*|要测试其存在性的标识符。|
|*语句*|一个或多个时要执行的语句*标识符*存在。|

## <a name="remarks"></a>备注

> [!CAUTION]
>  若要实现最可靠的结果，请使用 **__if_exists**以下约束条件下的语句。

- 将应用 **__if_exists**语句仅简单类型，而不是模板。

- 将应用 **__if_exists**到的内部或外部类标识符的语句。 不适用于 **__if_exists**到本地变量的语句。

- 使用 **__if_exists**仅在函数体中的语句。 在函数体外部区域 **__if_exists**语句可以测试仅完全定义的类型。

- 在测试重载函数时，不能测试特定形式的重载。

对补充 **__if_exists**语句是[__if_not_exists](../cpp/if-not-exists-statement.md)语句。

## <a name="example"></a>示例

请注意，此示例使用了模板，不建议这样做。

```cpp
// the__if_exists_statement.cpp
// compile with: /EHsc
#include <iostream>

template<typename T>
class X : public T {
public:
   void Dump() {
      std::cout << "In X<T>::Dump()" << std::endl;

      __if_exists(T::Dump) {
         T::Dump();
      }

      __if_not_exists(T::Dump) {
         std::cout << "T::Dump does not exist" << std::endl;
      }
   }
};

class A {
public:
   void Dump() {
      std::cout << "In A::Dump()" << std::endl;
   }
};

class B {};

bool g_bFlag = true;

class C {
public:
   void f(int);
   void f(double);
};

int main() {
   X<A> x1;
   X<B> x2;

   x1.Dump();
   x2.Dump();

   __if_exists(::g_bFlag) {
      std::cout << "g_bFlag = " << g_bFlag << std::endl;
   }

   __if_exists(C::f) {
      std::cout << "C::f exists" << std::endl;
   }

   return 0;
}
```

## <a name="output"></a>输出

```Output
In X<T>::Dump()
In A::Dump()
In X<T>::Dump()
T::Dump does not exist
g_bFlag = 1
C::f exists
```

## <a name="see-also"></a>请参阅

[选择语句](../cpp/selection-statements-cpp.md)<br/>
[关键字](../cpp/keywords-cpp.md)<br/>
[__if_not_exists 语句](../cpp/if-not-exists-statement.md)