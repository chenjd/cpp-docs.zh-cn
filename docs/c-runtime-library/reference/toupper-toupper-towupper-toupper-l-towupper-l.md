---
title: toupper、_toupper、towupper、_toupper_l、_towupper_l
ms.date: 11/04/2016
apiname:
- _toupper_l
- towupper
- toupper
- _towupper_l
- _toupper
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-string-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- towupper
- _toupper
- _totupper
- toupper
helpviewer_keywords:
- _toupper function
- towupper function
- uppercase, converting strings to
- totupper function
- string conversion, to different characters
- towupper_l function
- toupper_l function
- string conversion, case
- _toupper_l function
- _towupper_l function
- _totupper function
- case, converting
- characters, converting
- toupper function
ms.assetid: cdef1b0f-b19c-4d11-b7d2-cf6334c9b6cc
ms.openlocfilehash: 7e0ae3f1c69b0e5f77ea2ed8141a93867fd43b33
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50608852"
---
# <a name="toupper-toupper-towupper-toupperl-towupperl"></a>toupper、_toupper、towupper、_toupper_l、_towupper_l

将字符转换为大写。

## <a name="syntax"></a>语法

```C
int toupper(
   int c
);
int _toupper(
   int c
);
int towupper(
   wint_t c
);
int _toupper_l(
   int c ,
   _locale_t locale
);
int _towupper_l(
   wint_t c ,
   _locale_t locale
);
```

### <a name="parameters"></a>参数

*c*<br/>
要转换的字符。

*locale*<br/>
要使用的区域设置。

## <a name="return-value"></a>返回值

每个例程将转换的副本*c*，如果可能，并返回结果。

如果*c*是宽字符为其**iswlower**为非零值，并且没有为其相应的宽字符[iswupper](isupper-isupper-l-iswupper-iswupper-l.md)不为零， **towupper**返回相应的宽字符;否则为**towupper**返回*c*不变。

没有保留任何返回值以指示错误。

为了使**toupper**来提供预期的结果[__isascii](isascii-isascii-iswascii.md)并[islower](islower-iswlower-islower-l-iswlower-l.md)必须均返回非零值。

## <a name="remarks"></a>备注

如果可行且恰当，则其中的各个例程将指定小写字母转换为大写字母。 大小写转换**towupper**是特定于区域设置的。 只改变与当前区域设置相关的字符的大小写。 功能而无需 **_l**后缀使用当前设置的区域设置。 使用这些函数的版本 **_l**后缀将区域设置用作参数并使用它而不是当前设置的区域设置。 有关详细信息，请参阅 [Locale](../../c-runtime-library/locale.md)。

为了使**toupper**来提供预期的结果[__isascii](isascii-isascii-iswascii.md)并[isupper](isupper-isupper-l-iswupper-iswupper-l.md)必须均返回非零值。

[数据转换例程](../../c-runtime-library/data-conversion.md)

### <a name="generic-text-routine-mappings"></a>一般文本例程映射

|TCHAR.H 例程|未定义 _UNICODE 和 _MBCS|已定义 _MBCS|已定义 _UNICODE|
|---------------------|------------------------------------|--------------------|-----------------------|
|**_totupper**|**toupper**|**_mbctoupper**|**towupper**|
|**_totupper_l**|**_toupper_l**|**_mbctoupper_l**|**_towupper_l**|

> [!NOTE]
> **_toupper_l**并 **_towupper_l**没有区域设置相关性，并且不应直接调用。 它们提供供内部使用 **_totupper_l**。

## <a name="requirements"></a>要求

|例程所返回的值|必需的标头|
|-------------|---------------------|
|**toupper**|\<ctype.h>|
|**_toupper**|\<ctype.h>|
|**towupper**|\<ctype.h 1> 或 \<wchar.h 1>|

有关其他兼容性信息，请参阅 [兼容性](../../c-runtime-library/compatibility.md)。

## <a name="example"></a>示例

请参阅 [to 函数](../../c-runtime-library/to-functions.md)中的示例。

## <a name="see-also"></a>请参阅

[is、isw 例程](../../c-runtime-library/is-isw-routines.md)<br/>
[to 函数](../../c-runtime-library/to-functions.md)<br/>
[区域设置](../../c-runtime-library/locale.md)<br/>
[多字节字符序列的解释](../../c-runtime-library/interpretation-of-multibyte-character-sequences.md)<br/>
