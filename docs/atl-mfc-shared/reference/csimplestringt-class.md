---
title: CSimpleStringT 类
ms.date: 10/18/2018
f1_keywords:
- CSimpleStringT
- ATLSIMPSTR/ATL::CSimpleStringT
- ATLSIMPSTR/ATL::CSimpleStringT::PCXSTR
- ATLSIMPSTR/ATL::CSimpleStringT::PXSTR
- ATLSIMPSTR/ATL::CSimpleStringT::CSimpleStringT
- ATLSIMPSTR/ATL::CSimpleStringT::Append
- ATLSIMPSTR/ATL::CSimpleStringT::AppendChar
- ATLSIMPSTR/ATL::CSimpleStringT::CopyChars
- ATLSIMPSTR/ATL::CSimpleStringT::CopyCharsOverlapped
- ATLSIMPSTR/ATL::CSimpleStringT::Empty
- ATLSIMPSTR/ATL::CSimpleStringT::FreeExtra
- ATLSIMPSTR/ATL::CSimpleStringT::GetAllocLength
- ATLSIMPSTR/ATL::CSimpleStringT::GetAt
- ATLSIMPSTR/ATL::CSimpleStringT::GetBuffer
- ATLSIMPSTR/ATL::CSimpleStringT::GetBufferSetLength
- ATLSIMPSTR/ATL::CSimpleStringT::GetLength
- ATLSIMPSTR/ATL::CSimpleStringT::GetManager
- ATLSIMPSTR/ATL::CSimpleStringT::GetString
- ATLSIMPSTR/ATL::CSimpleStringT::IsEmpty
- ATLSIMPSTR/ATL::CSimpleStringT::LockBuffer
- ATLSIMPSTR/ATL::CSimpleStringT::Preallocate
- ATLSIMPSTR/ATL::CSimpleStringT::ReleaseBuffer
- ATLSIMPSTR/ATL::CSimpleStringT::ReleaseBufferSetLength
- ATLSIMPSTR/ATL::CSimpleStringT::SetAt
- ATLSIMPSTR/ATL::CSimpleStringT::SetManager
- ATLSIMPSTR/ATL::CSimpleStringT::SetString
- ATLSIMPSTR/ATL::CSimpleStringT::StringLength
- ATLSIMPSTR/ATL::CSimpleStringT::Truncate
- ATLSIMPSTR/ATL::CSimpleStringT::UnlockBuffer
helpviewer_keywords:
- shared classes, CSimpleStringT
- strings [C++], ATL class
- CSimpleStringT class
ms.assetid: 15814fcb-5b8f-4425-a97e-3b61fc9b48d8
ms.openlocfilehash: 93cb3ae0b2f358f64f0d6de26899d1b08f275b7b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50579278"
---
# <a name="csimplestringt-class"></a>CSimpleStringT 类

此类表示`CSimpleStringT`对象。

## <a name="syntax"></a>语法

```
template <typename BaseType>
class CSimpleStringT
```

### <a name="parameters"></a>参数

*BaseType*<br/>
字符串类的字符类型。 可以是以下各项之一：

- **char** （适用于 ANSI 字符串）。

- **wchar_t** （适用于 Unicode 字符串）。

- TCHAR （针对 ANSI 和 Unicode 字符串）。

## <a name="members"></a>成员

### <a name="public-typedefs"></a>公共 Typedef

|名称|描述|
|----------|-----------------|
|[CSimpleStringT::PCXSTR](#pcxstr)|指向常量字符串的指针。|
|[CSimpleStringT::PXSTR](#pxstr)|指向字符串的指针。|

### <a name="public-constructors"></a>公共构造函数

|名称|描述|
|----------|-----------------|
|[CSimpleStringT::CSimpleStringT](#ctor)|构造`CSimpleStringT`以各种方式的对象。|
|[CSimpleStringT:: ~ CSimpleStringT](#dtor)|析构函数。|

### <a name="public-methods"></a>公共方法

|名称|描述|
|----------|-----------------|
|[CSimpleStringT::Append](#append)|将追加`CSimpleStringT`到现有对象`CSimpleStringT`对象。|
|[CSimpleStringT::AppendChar](#appendchar)|将字符追加到现有`CSimpleStringT`对象。|
|[CSimpleStringT::CopyChars](#copychars)|将一个字符复制到另一个字符串。|
|[CSimpleStringT::CopyCharsOverlapped](#copycharsoverlapped)|将一个字符复制到另一个缓冲区与重叠的字符串。|
|[CSimpleStringT::Empty](#empty)|强制的长度为零的字符串。|
|[CSimpleStringT::FreeExtra](#freeextra)|释放以前分配的字符串对象的任何额外内存。|
|[CSimpleStringT::GetAllocLength](#getalloclength)|检索已分配的长度`CSimpleStringT`对象。|
|[CSimpleStringT::GetAt](#getat)|返回位于给定位置处的字符。|
|[CSimpleStringT::GetBuffer](#getbuffer)|返回一个指向的字符`CSimpleStringT`。|
|[CSimpleStringT::GetBufferSetLength](#getbuffersetlength)|返回一个指向的字符`CSimpleStringT`、 截断为指定的长度。|
|[CSimpleStringT::GetLength](#getlength)|返回中的字符数`CSimpleStringT`对象。|
|[CSimpleStringT::GetManager](#getmanager)|检索的内存管理器`CSimpleStringT`对象。|
|[CSimpleStringT::GetString](#getstring)|检索字符字符串|
|[CSimpleStringT::IsEmpty](#isempty)|测试是否`CSimpleStringT`对象不包含任何字符。|
|[CSimpleStringT::LockBuffer](#lockbuffer)|禁用引用计数，并可保护在缓冲区中的字符串。|
|[CSimpleStringT::Preallocate](#preallocate)|为字符缓冲区分配特定量的内存。|
|[CSimpleStringT::ReleaseBuffer](#releasebuffer)|返回的缓冲区的控制权`GetBuffer`。|
|[CSimpleStringT::ReleaseBufferSetLength](#releasebuffersetlength)|返回的缓冲区的控制权`GetBuffer`。|
|[CSimpleStringT::SetAt](#setat)|给定位置处设置一个字符。|
|[CSimpleStringT::SetManager](#setmanager)|设置内存管理器的`CSimpleStringT`对象。|
|[CSimpleStringT::SetString](#setstring)|设置的字符串`CSimpleStringT`对象。|
|[CSimpleStringT::StringLength](#stringlength)|返回指定字符串中的字符数。|
|[CSimpleStringT::Truncate](#truncate)|将截断到指定长度的字符串。|
|[CSimpleStringT::UnlockBuffer](#unlockbuffer)|使引用计数并释放缓冲区中的字符串。|

### <a name="public-operators"></a>公共运算符

|名称|描述|
|----------|-----------------|
|[CSimpleStringT::operator PCXSTR](#operator_pcxstr)|直接访问存储在字符`CSimpleStringT`对象作为 C 样式字符串。|
|[CSimpleStringT::operator\[\]](#operator_at)|返回位于给定位置处的字符 — 运算符替换为`GetAt`。|
|[CSimpleStringT::operator + =](#operator_add_eq)|连接到现有字符串的末尾的新字符串。|
|[CSimpleStringT::operator =](#operator_eq)|将一个新值赋给`CSimpleStringT`对象。|

### <a name="remarks"></a>备注

`CSimpleStringT` 是由 Visual c + + 支持的各种字符串类的基类。 它提供对基本缓冲区操作的字符串对象的内存管理的最小支持。 对于更高级的字符串对象，请参阅[CStringT 类](../../atl-mfc-shared/reference/cstringt-class.md)。

### <a name="requirements"></a>要求

**标头：** atlsimpstr.h

## <a name="append"></a> CSimpleStringT::Append

将追加`CSimpleStringT`到现有对象`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
void Append(const CSimpleStringT& strSrc);
void Append(PCXSTR pszSrc, int nLength);
void Append(PCXSTR pszSrc);
```

#### <a name="parameters"></a>参数

*strSrc*<br/>
`CSimpleStringT`要追加的对象。

*pszSrc*<br/>
指向包含要追加的字符的字符串的指针。

*nLength*<br/>
要追加的字符数。

### <a name="remarks"></a>备注

调用此方法要追加的现有`CSimpleStringT`对象和另一个`CSimpleStringT`对象。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::Append` 的用法。

```cpp
CSimpleString str1(pMgr), str2(pMgr);
str1.SetString(_T("Soccer is"));
str2.SetString(_T(" an elegant game"));
str1.Append(str2);
ASSERT(_tcscmp(str1, _T("Soccer is an elegant game")) == 0);
```

##  <a name="appendchar"></a> CSimpleStringT::AppendChar

将字符追加到现有`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
void AppendChar(XCHAR ch);
```

#### <a name="parameters"></a>参数

*ch*<br/>
要追加的字符

### <a name="remarks"></a>备注

调用此函数可将指定的字符追加到现有的最终`CSimpleStringT`对象。

##  <a name="copychars"></a> CSimpleStringT::CopyChars

将复制的字符或字符`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
static void CopyChars(
    XCHAR* pchDest,
    const XCHAR* pchSrc,
    int nChars) throw();
```

#### <a name="parameters"></a>参数

*pchDest*<br/>
指向字符字符串的指针。

*pchSrc*<br/>
指向包含要复制的字符的字符串的指针。

*nChars*<br/>
数*pchSrc*要复制的字符。

### <a name="remarks"></a>备注

调用此方法来复制中的字符*pchSrc*到*pchDest*字符串。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::CopyChars` 的用法。

```cpp
CSimpleString str(_T("xxxxxxxxxxxxxxxxxxx"), 20, pMgr);
TCHAR* pszSrc = _T("Hello world!");
_tprintf_s(_T("%s\n"), str);
str.CopyChars(str.GetBuffer(), pszSrc, 12);
_tprintf_s(_T("%s\n"), str);
```

##  <a name="copycharsoverlapped"></a>  CSimpleStringT::CopyCharsOverlapped

将复制的字符或字符`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
static void CopyCharsOverlapped(
    XCHAR* pchDest,
    const XCHAR* pchSrc,
    int nChars) throw();
```

#### <a name="parameters"></a>参数

*pchDest*<br/>
指向字符字符串的指针。

*pchSrc*<br/>
指向包含要复制的字符的字符串的指针。

*nChars*<br/>
数*pchSrc*要复制的字符。

### <a name="remarks"></a>备注

调用此方法来复制中的字符*pchSrc*到*pchDest*字符串。 与不同`CopyChars`，`CopyCharsOverlapped`提供用于从可能重叠的字符缓冲区复制的安全方法。

### <a name="example"></a>示例

有关示例，请参阅[CSimpleStringT::CopyChars](#copychars)，或为源代码`CSimpleStringT::SetString`（位于 atlsimpstr.h）。

##  <a name="ctor"></a>  CSimpleStringT::CSimpleStringT

构造 `CSimpleStringT` 对象。

### <a name="syntax"></a>语法

```
CSimpleStringT(const XCHAR* pchSrc, int nLength, IAtlStringMgr* pStringMgr);
CSimpleStringT(PCXSTR pszSrc, IAtlStringMgr* pStringMgr);
CSimpleStringT(const CSimpleStringT& strSrc);
explicit CSimpleStringT(IAtlStringMgr* pStringMgr) throw();
```

#### <a name="parameters"></a>参数

*strSrc*<br/>
将现有`CSimpleStringT`复制到此对象`CSimpleStringT`对象。

*pchSrc*<br/>
指向数组的长度的字符的指针*nLength*，null 终止。

*pszSrc*<br/>
以 null 结尾的字符串复制到此`CSimpleStringT`对象。

*nLength*<br/>
中的字符数的计数`pch`。

*pStringMgr*<br/>
指向的内存管理器的`CSimpleStringT`对象。 有关详细信息`IAtlStringMgr`和内存管理`CSimpleStringT`，请参阅[内存管理和 CStringT](../memory-management-with-cstringt.md)。

### <a name="remarks"></a>备注

构造一个新`CSimpleStringT`对象。 因为构造函数将输入的数据复制到新的已分配存储，可能会导致内存异常。

### <a name="example"></a>示例

下面的示例演示如何将`CSimpleStringT::CSimpleStringT`通过使用 ATL **typedef** `CSimpleString`。 `CSimpleString` 是常用的类模板专用化`CSimpleStringT`。

```cpp
CSimpleString s1(pMgr);
// Empty string
CSimpleString s2(_T("cat"), pMgr);
// From a C string literal

CSimpleString s3(s2);
// Copy constructor
CSimpleString s4(s2 + _T(" ") + s3);

// From a string expression
CSimpleString s5(_T("xxxxxx"), 6, pMgr);
// s5 = "xxxxxx"
```

##  <a name="empty"></a>  CSimpleStringT::Empty

这样，您`CSimpleStringT`对象为空字符串，并释放相应的内存。

### <a name="syntax"></a>语法

```
void Empty() throw();
```

### <a name="remarks"></a>备注

有关详细信息，请参阅[字符串： CString 异常清理](../cstring-exception-cleanup.md)。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::Empty` 的用法。

```cpp
CSimpleString s(pMgr);
ASSERT(s.IsEmpty());
```

##  <a name="freeextra"></a>  CSimpleStringT::FreeExtra

释放以前分配的字符串，但不再需要任何额外内存。

### <a name="syntax"></a>语法

```
void FreeExtra();
```

### <a name="remarks"></a>备注

这应减少字符串对象占用的内存开销。 该方法将重新分配到返回的确切长度的缓冲区[GetLength](#getlength)。

### <a name="example"></a>示例

```cpp
CAtlString basestr;
IAtlStringMgr* pMgr;

pMgr= basestr.GetManager();
ASSERT(pMgr != NULL);

// Create a CSimpleString with 28 characters
CSimpleString str(_T("Many sports are fun to play."), 28, pMgr);
_tprintf_s(_T("Alloc length is %d, String length is %d\n"),
   str.GetAllocLength(), str.GetLength());

// Assigning a smaller string won't cause CSimpleString to free its
// memory, because it assumes the string will grow again anyway.
str = _T("Soccer is best!");
_tprintf_s(_T("Alloc length is %d, String length is %d\n"),
   str.GetAllocLength(), str.GetLength());

// This call forces CSimpleString to release the extra
// memory it doesn't need.
str.FreeExtra();
_tprintf_s(_T("Alloc length is %d, String length is %d\n"),
   str.GetAllocLength(), str.GetLength());
```

### <a name="remarks"></a>备注

此示例的输出如下所示：

```Output
Alloc length is 1031, String length is 1024
Alloc length is 1031, String length is 15
Alloc length is 15, String length is 15
```

##  <a name="getalloclength"></a>  CSimpleStringT::GetAllocLength

检索已分配的长度`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
int GetAllocLength() const throw();
```

### <a name="return-value"></a>返回值

分配给此对象的字符数。

### <a name="remarks"></a>备注

调用此方法来确定此分配的字符数`CSimpleStringT`对象。 请参阅[FreeExtra](#freeextra)有关调用此函数的示例。

##  <a name="getat"></a>  CSimpleStringT::GetAt

返回从一个字符`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
XCHAR GetAt(int iChar) const;
```

#### <a name="parameters"></a>参数

*iChar*<br/>
中的字符的从零开始索引`CSimpleStringT`对象。 *IChar*参数必须是大于或等于 0 且小于返回的值[GetLength](#getlength)。 否则为`GetAt`将生成一个异常。

### <a name="return-value"></a>返回值

`XCHAR` ，其中包含的字符在字符串中指定的位置。

### <a name="remarks"></a>备注

调用此方法以返回由指定的一个字符*iChar*。 重载的下标 (**[]**) 运算符是的方便别名`GetAt`。 Null 终止符是可寻址的而不会生成异常使用`GetAt`。 但是，不计入`GetLength`，并且返回的值为 0。

### <a name="example"></a>示例

下面的示例演示如何使用`CSimpleStringT::GetAt`。

```cpp
CSimpleString s(_T("abcdef"), pMgr);
ASSERT(s.GetAt(2) == _T('c'));
```

##  <a name="getbuffer"></a>  CSimpleStringT::GetBuffer

将指针返回到的内部字符缓冲区`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
PXSTR GetBuffer(int nMinBufferLength);
PXSTR GetBuffer();
```

#### <a name="parameters"></a>参数

*nMinBufferLength*<br/>
最小字符缓冲区可以容纳的字符数。 此值不包括 null 终止符的占用空间。

如果*nMinBufferLength*大于当前缓冲区的长度`GetBuffer`销毁当前缓冲区、 替换请求的大小的缓冲区并将对象引用计数重置为零。 如果您以前称为[LockBuffer](#lockbuffer)上此缓冲区，则会丢失缓冲区锁。

### <a name="return-value"></a>返回值

`PXSTR`指向的对象 （以 null 结尾） 字符缓冲区的指针。

### <a name="remarks"></a>备注

调用此方法返回的缓冲区内容`CSimpleStringT`对象。 返回`PXSTR`不是常量，从而允许直接修改`CSimpleStringT`内容。

如果使用返回的指针`GetBuffer`若要更改字符串内容，必须调用[ReleaseBuffer](#releasebuffer)在使用任何其他之前`CSimpleStringT`成员方法。

返回的地址`GetBuffer`可能不是有效的调用后`ReleaseBuffer`因为其他`CSimpleStringT`操作可能会导致`CSimpleStringT`要重新分配缓冲区。 如果不更改的长度，不重新分配缓冲区`CSimpleStringT`。

缓冲区内存将自动释放时`CSimpleStringT`对象被销毁。

如果您跟踪字符串长度自己，您不应追加终止 null 字符。 但是，必须指定最终的字符串长度，在您发布了具有缓冲区`ReleaseBuffer`。 如果您执行追加终止 null 字符，则应传递长度为-1 （默认值）。 `ReleaseBuffer` 然后确定缓冲区长度。

如果没有足够的内存来满足`GetBuffer`请求时，此方法将引发 CMemoryException *。

### <a name="example"></a>示例

```cpp
CSimpleString s(_T("abcd"), pMgr);
LPTSTR pBuffer = s.GetBuffer(10);
int sizeOfBuffer = s.GetAllocLength();

// Directly access CSimpleString buffer
_tcscpy_s(pBuffer, sizeOfBuffer, _T("Hello"));
ASSERT(_tcscmp(s, _T("Hello")) == 0);
s.ReleaseBuffer();
```

##  <a name="getbuffersetlength"></a>  CSimpleStringT::GetBufferSetLength

将指针返回到的内部字符缓冲区`CSimpleStringT`对象，截断或如有必要以完全匹配中指定的长度不断增加其长度*nLength*。

### <a name="syntax"></a>语法

```
PXSTR GetBufferSetLength(int nLength);
```

#### <a name="parameters"></a>参数

*nLength*<br/>
确切大小`CSimpleStringT`以字符为单位的字符缓冲区。

### <a name="return-value"></a>返回值

一个`PXSTR`指向的对象 （以 null 结尾） 字符缓冲区的指针。

### <a name="remarks"></a>备注

调用此方法以检索指定的内部缓冲区的长度`CSimpleStringT`对象。 返回`PXSTR`指针不是**const**从而可以直接修改`CSimpleStringT`内容。

如果使用返回的指针[GetBufferSetLength](#getbuffersetlength)若要更改字符串内容，请调用`ReleaseBuffer`若要更新的内部状态`CsimpleStringT`然后才能使用任何其他`CSimpleStringT`方法。

返回的地址`GetBufferSetLength`可能不是有效的调用后`ReleaseBuffer`因为其他`CSimpleStringT`操作可能会导致`CSimpleStringT`要重新分配缓冲区。 如果不更改的长度，不重新分配缓冲区`CSimpleStringT`。

缓冲区内存将自动释放时`CSimpleStringT`对象被销毁。

如果您跟踪字符串长度自己，不要将追加终止 null 字符。 当使用释放缓冲区时，必须指定最终的字符串长度`ReleaseBuffer`。 如果在调用时，执行追加终止 null 字符`ReleaseBuffer`，将为-1 （默认值） 传递到长度`ReleaseBuffer`，并`ReleaseBuffer`将执行`strlen`上要确定其长度的缓冲区。

有关引用计数的详细信息，请参阅以下文章：

- [管理对象生存期通过引用计数](/windows/desktop/com/managing-object-lifetimes-through-reference-counting)Windows SDK 中。

- [实现引用计数](/windows/desktop/com/implementing-reference-counting)Windows SDK 中。

- [用于管理引用计数规则](/windows/desktop/com/rules-for-managing-reference-counts)Windows SDK 中。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::GetBufferSetLength` 的用法。

```cpp
CSimpleString str(pMgr);
LPTSTR pstr = str.GetBufferSetLength(3);
pstr[0] = _T('C');
pstr[1] = _T('u');
pstr[2] = _T('p');

// No need for trailing zero or call to ReleaseBuffer()
// because GetBufferSetLength() set it for us.

str += _T(" soccer is best!");
ASSERT(_tcscmp(str, _T("Cup soccer is best!")) == 0);
```

##  <a name="getlength"></a>  CSimpleStringT::GetLength

返回中的字符数`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
int GetLength() const throw();
```

### <a name="return-value"></a>返回值

在字符串中字符数。

### <a name="remarks"></a>备注

调用此方法返回的对象中的字符数。 计数不包括 null 终止符。

对于多字节字符集 (MBCS)`GetLength`一个多字节字符中的每个 8 位字符; 即，为潜在顾客和线索字节计为两个字节的计数。 请参阅[FreeExtra](#freeextra)有关调用此函数的示例。

##  <a name="getmanager"></a>  CSimpleStringT::GetManager

检索的内存管理器`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
IAtlStringMgr* GetManager() const throw();
```

### <a name="return-value"></a>返回值

指向的内存管理器的`CSimpleStringT`对象。

### <a name="remarks"></a>备注

调用此方法以检索内存管理器使用的`CSimpleStringT`对象。 有关内存管理器和字符串对象的详细信息，请参阅[内存管理和 CStringT](../memory-management-with-cstringt.md)。

##  <a name="getstring"></a>  CSimpleStringT::GetString

检索字符字符串。

### <a name="syntax"></a>语法

```
PCXSTR GetString() const throw();
```

### <a name="return-value"></a>返回值

指向以 null 结尾的字符串的指针。

### <a name="remarks"></a>备注

调用此方法以检索与关联的字符字符串`CSimpleStringT`对象。

> [!NOTE]
>  返回`PCXSTR`指针是**const** ，并且不允许直接修改`CSimpleStringT`内容。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::GetString` 的用法。

```cpp
CSimpleString str(pMgr);
str += _T("Cup soccer is best!");
_tprintf_s(_T("%s"), str.GetString());
```

##  <a name="isempty"></a>  CSimpleStringT::IsEmpty

测试`CSimpleStringT`空条件的对象。

### <a name="syntax"></a>语法

```
bool IsEmpty() const throw();
```

### <a name="return-value"></a>返回值

返回 true; 否则`CSimpleStringT`对象具有 0 长度; 否则为 FALSE。

### <a name="remarks"></a>备注

调用此方法来确定对象是否包含空字符串。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::IsEmpty` 的用法。

```cpp
CSimpleString s(pMgr);
ASSERT(s.IsEmpty());
```

##  <a name="lockbuffer"></a>  CSimpleStringT::LockBuffer

禁用引用计数，并可保护在缓冲区中的字符串。

### <a name="syntax"></a>语法

```
PXSTR LockBuffer();
```

### <a name="return-value"></a>返回值

一个指向`CSimpleStringT`对象或以 null 结尾的字符串。

### <a name="remarks"></a>备注

调用此方法可锁定的缓冲区`CSimpleStringT`对象。 通过调用`LockBuffer`，使用引用计数为-1，则创建字符串的副本。 当引用计数值为-1 时，缓冲区中的字符串被视为可"锁定"状态。 处于锁定状态，该字符串是受保护的两种方式：

- 任何其他字符串可以在锁定的字符串中，不获取对数据的引用，即使该字符串分配给已锁定的字符串。

- 锁定的字符串永远不会将引用另一个字符串，即使该其他字符串复制到锁定的字符串。

通过锁定缓冲区中的字符串，可确保缓冲区的字符串的排他暂停状态将保持不变。

您用完后`LockBuffer`，调用[UnlockBuffer](#unlockbuffer)引用计数重置为 1。

> [!NOTE]
>  如果您调用[GetBuffer](#getbuffer)上锁定的缓冲区，并设置`GetBuffer`参数`nMinBufferLength`为大于当前缓冲区的长度，你将失去缓冲区锁。 此类调用到`GetBuffer`销毁当前缓冲区、 替换请求的大小的缓冲区并将引用计数重置为零。

有关引用计数的详细信息，请参阅以下文章：

- [管理对象生存期通过引用计数](/windows/desktop/com/managing-object-lifetimes-through-reference-counting)Windows SDK 中

- [实现引用计数](/windows/desktop/com/implementing-reference-counting)Windows SDK 中

- [用于管理引用计数规则](/windows/desktop/com/rules-for-managing-reference-counts)Windows SDK 中

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::LockBuffer` 的用法。

```cpp
CSimpleString str(_T("Hello"), pMgr);
TCHAR ch;

str.LockBuffer();
ch = str.GetAt(2);
_tprintf_s(_T("%c"), ch);
str.UnlockBuffer();
```

##  <a name="operator_at"></a>  CSimpleStringT::operator\[\]

调用此函数可访问的字符数组的单个字符。

### <a name="syntax"></a>语法

```
XCHAR operator[](int iChar) const;
```

#### <a name="parameters"></a>参数

*iChar*<br/>
字符串中字符的从零开始索引。

### <a name="remarks"></a>备注

重载的下标 (**[]**) 运算符将返回指定的从零开始的索引中的单个字符*iChar*。 此运算符是一个便捷替代[GetAt](#getat)成员函数。

> [!NOTE]
>  您可以使用下标 (**[]**) 运算符来获取的值中的字符`CSimpleStringT`，但不能使用它来更改中的字符值`CSimpleStringT`。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::operator []` 的用法。

```cpp
CSimpleString s(_T("abc"), pMgr);
ASSERT(s[1] == _T('b'));
```

## <a name="operator_at"></a>  CSimpleStringT::operator \[\]

调用此函数可访问的字符数组的单个字符。

### <a name="syntax"></a>语法

```
XCHAR operator[](int iChar) const;
```

### <a name="parameters"></a>参数

*iChar*<br/>
字符串中字符的从零开始索引。

### <a name="remarks"></a>备注

重载的下标 (**[]**) 运算符将返回指定的从零开始的索引中的单个字符*iChar*。 此运算符是一个便捷替代[GetAt](#getat)成员函数。

> [!NOTE]
>  您可以使用下标 (**[]**) 运算符来获取的值中的字符`CSimpleStringT`，但不能使用它来更改中的字符值`CSimpleStringT`。

##  <a name="operator_add_eq"></a>  CSimpleStringT::operator + =

联接到现有字符串的末尾的新字符串或字符。

### <a name="syntax"></a>语法

```
CSimpleStringT& operator +=(PCXSTR pszSrc);
CSimpleStringT& operator +=(const CSimpleStringT& strSrc);
template<int t_nSize>
CSimpleStringT& operator+=(const CStaticString< XCHAR, t_nSize >& strSrc);
CSimpleStringT& operator +=(char ch);
CSimpleStringT& operator +=(unsigned char ch);
CSimpleStringT& operator +=(wchar_t ch);
```

#### <a name="parameters"></a>参数

*pszSrc*<br/>
指向以 null 结尾的字符串的指针。

*strSrc*<br/>
一个指向现有`CSimpleStringT`对象。

*ch*<br/>
要追加的字符。

### <a name="remarks"></a>备注

运算符可接受另一个`CSimpleStringT`对象或字符。 请注意，内存可能会发生异常，每当你使用此串联运算符，因为可能会分配新存储的字符添加到此`CSimpleStringT`对象。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::operator +=` 的用法。

```cpp
CSimpleString str(_T("abc"), pMgr);
ASSERT(_tcscmp((str += _T("def")), _T("abcdef")) == 0);
```

##  <a name="operator_eq"></a>  CSimpleStringT::operator =

将一个新值赋给`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
CSimpleStringT& operator =(PCXSTR pszSrc);
CSimpleStringT& operator =(const CSimpleStringT& strSrc);
```

#### <a name="parameters"></a>参数

*pszSrc*<br/>
指向以 null 结尾的字符串的指针。

*strSrc*<br/>
一个指向现有`CSimpleStringT`对象。

### <a name="remarks"></a>备注

如果目标字符串 （左侧） 已足够空间来存储新数据，会不执行任何新的内存分配。 请注意，内存可能会发生异常，每当你使用赋值运算符，因为通常分配新存储，用于保存所生成`CSimpleStringT`对象。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::operator =` 的用法。

```cpp
CSimpleString s1(pMgr), s2(pMgr);
// Empty CSimpleStringT objects

s1 = _T("cat");
// s1 = "cat"
ASSERT(_tcscmp(s1, _T("cat")) == 0);

s2 = s1;               // s1 and s2 each = "cat"
ASSERT(_tcscmp(s2, _T("cat")) == 0);

s1 = _T("the ") + s1;
// Or expressions
ASSERT(_tcscmp(s1, _T("the cat")) == 0);

s1 = _T("x");
// Or just individual characters
ASSERT(_tcscmp(s1, _T("x")) == 0);
```

##  <a name="operator_pcxstr"></a>  CSimpleStringT::operator PCXSTR

直接访问存储在字符`CSimpleStringT`对象作为 C 样式字符串。

### <a name="syntax"></a>语法

```
operator PCXSTR() const throw();
```

### <a name="return-value"></a>返回值

指向字符串的数据的字符指针。

### <a name="remarks"></a>备注

任何字符被不复制;只有指针返回。 谨慎使用此运算符。 如果更改`CString`对象获取的字符指针后，你可能会导致重新分配的内存，使指针无效。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::operator PCXSTR` 的用法。

```cpp
// If the prototype of a function is known to the compiler,
// the PCXSTR cast operator may be invoked implicitly.

CSimpleString strSports(L"Soccer is Best!", pMgr);
WCHAR sz[1024];

wcscpy_s(sz, strSports);

// If the prototype isn't known or is a va_arg prototype,
// you must invoke the cast operator explicitly. For example,
// the va_arg part of a call to swprintf_s() needs the cast:

swprintf_s(sz, 1024, L"I think that %s!\n", (PCWSTR)strSports);

// While the format parameter is known to be an PCXSTR and
// therefore doesn't need the cast:

swprintf_s(sz, 1024, strSports);

// Note that some situations are ambiguous. This line will
// put the address of the strSports object to stdout:

wcout << strSports;

// while this line will put the content of the string out:

wcout << (PCWSTR)strSports;
```

##  <a name="pcxstr"></a>  CSimpleStringT::PCXSTR

指向常量字符串的指针。

### <a name="syntax"></a>语法

```
typedef ChTraitsBase< BaseType >::PCXSTR PCXSTR;
```

##  <a name="preallocate"></a>  CSimpleStringT::Preallocate

分配的字节数的特定量`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
void Preallocate( int nLength);
```

#### <a name="parameters"></a>参数

*nLength*<br/>
确切大小`CSimpleStringT`以字符为单位的字符缓冲区。

### <a name="remarks"></a>备注

调用此方法来分配的特定的缓冲区大小`CSimpleStringT`对象。

`CSimpleStringT` 如果无法为字符缓冲区的分配空间，则生成 STATUS_NO_MEMORY 异常。 默认情况下，内存分配执行由 WIN32 API 函数`HeapAlloc`或`HeapReAlloc`。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::Preallocate` 的用法。

```cpp
CSimpleString str(pMgr);
_tprintf_s(_T("Allocated length: %d\n"), str.GetAllocLength());
str.Preallocate(100);
_tprintf_s(_T("Allocated length: %d\n"), str.GetAllocLength());
```

##  <a name="pxstr"></a>  CSimpleStringT::PXSTR

指向字符串的指针。

### <a name="syntax"></a>语法

```
typedef ChTraitsBase< BaseType >::PXSTR PXSTR;
```

##  <a name="releasebuffer"></a>  CSimpleStringT::ReleaseBuffer

释放控件分配的缓冲区[GetBuffer](#getbuffer)。

### <a name="syntax"></a>语法

```
void ReleaseBuffer(int nNewLength = -1);
```

#### <a name="parameters"></a>参数

*nNewLength*<br/>
以字符为单位，不包括 null 终止符的字符串的新长度。 如果字符串为 null 终止，则为-1 默认值设置`CSimpleStringT`大小到字符串的当前长度。

### <a name="remarks"></a>备注

调用此方法以重新分配或释放的缓冲区的字符串对象。 如果您知道，在缓冲区中的字符串以 null 终止，则可以省略*nNewLength*参数。 如果您的字符串不为 null 终止，则使用*nNewLength*来指定它的长度。 返回的地址[GetBuffer](#getbuffer)无效调用后面`ReleaseBuffer`或任何其他`CSimpleStringT`操作。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::ReleaseBuffer` 的用法。

```cpp
const int bufferSize = 1024;
CSimpleString s(_T("abc"), pMgr);
LPTSTR p = s.GetBuffer(bufferSize);
_tcscpy_s(p, bufferSize, _T("abc"));

// use the buffer directly
ASSERT(s.GetLength() == 3);

// String length = 3
s.ReleaseBuffer();

// Surplus memory released, p is now invalid.
ASSERT(s.GetLength() == 3);

// Length still 3
```

##  <a name="releasebuffersetlength"></a>  CSimpleStringT::ReleaseBufferSetLength

释放控件分配的缓冲区[GetBuffer](#getbuffer)。

### <a name="syntax"></a>语法

```
void ReleaseBufferSetLength(int nNewLength);
```

#### <a name="parameters"></a>参数

*nNewLength*<br/>
发布字符串的长度

### <a name="remarks"></a>备注

此函数是功能上类似于[ReleaseBuffer](#releasebuffer)只不过必须传递的字符串对象的有效长度。

##  <a name="setat"></a>  CSimpleStringT::SetAt

设置中的单个字符`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
void SetAt(int iChar, XCHAR ch);
```

#### <a name="parameters"></a>参数

*iChar*<br/>
中的字符的从零开始索引`CSimpleStringT`对象。 *IChar*参数必须是大于或等于 0 且小于返回的值[GetLength](#getlength)。

*ch*<br/>
新字符。

### <a name="remarks"></a>备注

调用此方法来覆盖位于处的字符*iChar*。 此方法将不会增大该字符串，如果*iChar*超出了现有字符串的界限。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::SetAt` 的用法。

```cpp
CSimpleString s(_T("abcdef"), pMgr);
s.SetAt(1, _T('a'));
ASSERT(_tcscmp(s, _T("aacdef")) == 0);
```

##  <a name="setmanager"></a>  CSimpleStringT::SetManager

指定的内存管理器`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
void SetManager(IAtlStringMgr* pStringMgr);
```

#### <a name="parameters"></a>参数

*pStringMgr*<br/>
指向新内存管理器的指针。

### <a name="remarks"></a>备注

调用此方法，以指定新的内存管理器使用的`CSimpleStringT`对象。 有关内存管理器和字符串对象的详细信息，请参阅[内存管理和 CStringT](../memory-management-with-cstringt.md)。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::SetManager` 的用法。

```cpp
CSimpleString s(pMgr);
s.SetManager(pCustomMgr);
```

##  <a name="setstring"></a>  CSimpleStringT::SetString

设置的字符串`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
void SetString(PCXSTR pszSrc, int nLength);
void SetString(PCXSTR pszSrc);
```

#### <a name="parameters"></a>参数

*pszSrc*<br/>
指向以 null 结尾的字符串的指针。

*nLength*<br/>
中的字符数的计数*pszSrc*。

### <a name="remarks"></a>备注

复制到字符串`CSimpleStringT`对象。 `SetString` 将覆盖缓冲区中的较旧字符串数据。

这两个版本`SetString`检查是否*pszSrc*是 null 指针，并且如果是，引发 E_INVALIDARG 错误。

单参数版本`SetString`预期*pszSrc*为指向以 null 结尾的字符串。

两个参数版本`SetString`还预期*pszSrc*为以 null 结尾的字符串。 它使用*nLength*按字符串长度除非首先遇到 null 终止符。

两个参数版本`SetString`还会检查是否*pszSrc*指向当前缓冲区中的位置`CSimpleStringT`。 在此特殊情况下，`SetString`使用不会覆盖的字符串数据，并在返回到其缓冲区复制的字符串数据的内存复制函数。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::SetString` 的用法。

```cpp
CSimpleString s(_T("abcdef"), pMgr);
ASSERT(_tcscmp(s, _T("abcdef")) == 0);
s.SetString(_T("Soccer"), 6);
ASSERT(_tcscmp(s, _T("Soccer")) == 0);
```

##  <a name="stringlength"></a>  CSimpleStringT::StringLength

返回指定字符串中的字符数。

### <a name="syntax"></a>语法

```
ATL_NOINLINE static int StringLength(PCXSTR psz) throw();
```

#### <a name="parameters"></a>参数

*psz*<br/>
指向以 null 结尾的字符串的指针。

### <a name="return-value"></a>返回值

中的字符数*psz*; 不包括 null 终止符。

### <a name="remarks"></a>备注

调用此方法来检索指向字符串中的字符数*psz*。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::StringLength` 的用法。

```cpp
ASSERT(CSimpleString::StringLength(_T("soccer")) == 6);
```

##  <a name="truncate"></a>  CSimpleStringT::Truncate

将截断为新的长度的字符串。

### <a name="syntax"></a>语法

```
void Truncate(int nNewLength);
```

#### <a name="parameters"></a>参数

*nNewLength*<br/>
新字符串的长度。

### <a name="remarks"></a>备注

调用此方法来截断为新的长度的字符串的内容。

> [!NOTE]
>  这不会影响已分配缓冲区的长度。 若要减小或增大当前缓冲区，请参阅[FreeExtra](#freeextra)并[Preallocate](#preallocate)。

### <a name="example"></a>示例

以下示例演示了 `CSimpleStringT::Truncate` 的用法。

```cpp
CSimpleString str(_T("abcdefghi"), pMgr);
_tprintf_s(_T("Allocated length: %d\n"), str.GetLength());
_tprintf_s(_T("Contents: %s\n"), str);
str.Truncate(4);
_tprintf_s(_T("Allocated length: %d\n"), str.GetLength());
_tprintf_s(_T("Contents: %s\n"), str);
```

##  <a name="unlockbuffer"></a>  CSimpleStringT::UnlockBuffer

解锁的缓冲区的`CSimpleStringT`对象。

### <a name="syntax"></a>语法

```
void UnlockBuffer() throw();
```

### <a name="remarks"></a>备注

调用此方法以字符串的引用计数重置为 1。

`CSimpleStringT`析构函数自动调用`UnlockBuffer`以确保调用的析构函数时未锁定缓冲区。 此方法的示例，请参阅[LockBuffer](#lockbuffer)。

##  <a name="dtor"></a>  CSimpleStringT:: ~ CSimpleStringT

销毁 `CSimpleStringT` 对象。

### <a name="syntax"></a>语法

```
~CSimpleStringT() throw();
```

### <a name="remarks"></a>备注

调用此方法来销毁`CSimpleStringT`对象。

## <a name="see-also"></a>请参阅

[层次结构图](../../mfc/hierarchy-chart.md)<br/>
[ATL/MFC 共享类](../../atl-mfc-shared/atl-mfc-shared-classes.md)