---
description: 了解详细信息： _strncoll、_wcsncoll、_mbsncoll、_strncoll_l、_wcsncoll_l、_mbsncoll_l
title: _strncoll、_wcsncoll、_mbsncoll、_strncoll_l、_wcsncoll_l、_mbsncoll_l
ms.date: 4/2/2020
api_name:
- _strncoll
- _mbsncoll_l
- _wcsncoll
- _wcsncoll_l
- _mbsncoll
- _strncoll_l
- _o__mbsncoll
- _o__mbsncoll_l
- _o__strncoll
- _o__strncoll_l
- _o__wcsncoll
- _o__wcsncoll_l
api_location:
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
- api-ms-win-crt-multibyte-l1-1-0.dll
- api-ms-win-crt-string-l1-1-0.dll
- api-ms-win-crt-private-l1-1-0.dll
api_type:
- DLLExport
topic_type:
- apiref
f1_keywords:
- mbsncoll_l
- strncoll
- _wcsncoll
- _tcsnccoll
- _ftcsnccoll
- wcsncoll
- _mbsncoll
- wcsncoll_l
- strncoll_l
- _ftcsncoll
- _strncoll
- _tcsncoll
- mbsncoll
helpviewer_keywords:
- _strncoll_l function
- code pages, using for string comparisons
- _strncoll function
- _mbsncoll function
- ftcsncoll function
- strncoll function
- _ftcsncoll function
- strncoll_l function
- wcsncoll function
- mbsncoll function
- _tcsncoll function
- _tcsnccoll function
- wcsncoll_l function
- tcsnccoll function
- mbsncoll_l function
- _mbsncoll_l function
- tcsncoll function
- _wcsncoll function
- strings [C++], comparing by code page
- _ftcsnccoll function
- ftcsnccoll function
- _wcsncoll_l function
ms.assetid: e659a5a4-8afe-4033-8e72-17ffd4bdd8e9
ms.openlocfilehash: 71f37511ab531def178926d77e61978190fce817
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97306113"
---
# <a name="_strncoll-_wcsncoll-_mbsncoll-_strncoll_l-_wcsncoll_l-_mbsncoll_l"></a>_strncoll、_wcsncoll、_mbsncoll、_strncoll_l、_wcsncoll_l、_mbsncoll_l

使用特定于区域设置的信息比较字符串。

> [!IMPORTANT]
> 不能在 Windows 运行时中执行的应用程序中使用 **_mbsncoll** 和 **_mbsncoll_l** 。 有关详细信息，请参阅[通用 Windows 平台应用中不支持的 CRT 函数](../../cppcx/crt-functions-not-supported-in-universal-windows-platform-apps.md)。

## <a name="syntax"></a>语法

```C
int _strncoll(
   const char *string1,
   const char *string2,
   size_t count
);
int _wcsncoll(
   const wchar_t *string1,
   const wchar_t *string2,
   size_t count
);
int _mbsncoll(
   const unsigned char *string1,
   const unsigned char *string2,
   size_t count
);
int _strncoll_l(
   const char *string1,
   const char *string2,
   size_t count,
   _locale_t locale
);
int _wcsncoll_l(
   const wchar_t *string1,
   const wchar_t *string2,
   size_t count,
   _locale_t locale
);
int _mbsncoll_l(
   const unsigned char *string1,
   const unsigned char *string2,
   size_t count,
   _locale_t locale
);
```

### <a name="parameters"></a>parameters

*string1*、 *string2*<br/>
要比较的 null 终止的字符串。

*计数*<br/>
要比较的字符数。

*locale*<br/>
要使用的区域设置。

## <a name="return-value"></a>返回值

其中每个函数返回一个值，该值指示 *string1* 和 *string2* 的子字符串的关系，如下所示。

|返回值|string1 与 string2 的关系|
|------------------|----------------------------------------|
|< 0|*string1* 小于 *string2*。|
|0|*string1* 与 *string2* 相同。|
|> 0|*string1* 大于 *string2*。|

其中每个函数都将返回 **_NLSCMPERROR**。 若要使用 **_NLSCMPERROR**，请包含 STRING .H 或 mbstring.h。 如果 *string1* 或 *string2* 包含归类序列域之外的宽字符代码，则 **_wcsncoll** 可能失败。 出现错误时， **_wcsncoll** 可能会将 **Errno** 设置为 **EINVAL**。 若要检查对 **_wcsncoll** 的调用是否有错误，请将 **errno** 设置为0，然后在调用 **_wcsncoll** 后检查 **errno** 。

## <a name="remarks"></a>备注

其中每个函数根据当前使用的代码页，对 *string1* 和 *string2* 中的第一个 *计数* 字符执行区分大小写的比较。 仅在以下情况下使用这些函数：代码页中的字符集顺序和字典字符顺序存在差异，以及此差异对于字符串比较很有用。 字符集顺序与区域设置相关。 这些不带 **_l** 后缀的函数的版本使用当前区域设置，但具有 **_l** 后缀的版本使用传入的区域设置。 有关详细信息，请参阅 [Locale](../../c-runtime-library/locale.md)。

所有这些函数都验证其参数。 如果 *string1* 或 *string2* 是 null 指针，或者 *count* 大于 **INT_MAX**，则将调用无效参数处理程序，如 [参数验证](../../c-runtime-library/parameter-validation.md)中所述。 如果允许执行继续，则这些函数将返回 **_NLSCMPERROR** ，并将 **Errno** 设置为 **EINVAL**。

默认情况下，此函数的全局状态的作用域限定为应用程序。 若要更改此项，请参阅 [CRT 中的全局状态](../global-state.md)。

### <a name="generic-text-routine-mappings"></a>一般文本例程映射

|TCHAR.H 例程|未定义 _UNICODE 和 _MBCS|已定义 _MBCS|已定义 _UNICODE|
|---------------------|------------------------------------|--------------------|-----------------------|
|**_tcsnccoll**|**_strncoll**|**_mbsncoll**|**_wcsncoll**|
|**_tcsncoll**|**_strncoll**|[_mbsnbcoll](mbsnbcoll-mbsnbcoll-l-mbsnbicoll-mbsnbicoll-l.md)|**_wcsncoll**|

## <a name="requirements"></a>要求

|例程所返回的值|必需的标头|
|-------------|---------------------|
|**_strncoll**， **_strncoll_l**|\<string.h>|
|**_wcsncoll**， **_wcsncoll_l**|\<wchar.h> 或 \<string.h>|
|**_mbsncoll**， **_mbsncoll_l**|\<mbstring.h>|

有关其他兼容性信息，请参阅[兼容性](../../c-runtime-library/compatibility.md)。

## <a name="see-also"></a>请参阅

[区域设置](../../c-runtime-library/locale.md)<br/>
[字符串操作](../../c-runtime-library/string-manipulation-crt.md)<br/>
[strcoll 函数](../../c-runtime-library/strcoll-functions.md)<br/>
[localeconv](localeconv.md)<br/>
[_mbsnbcoll、_mbsnbcoll_l、_mbsnbicoll、_mbsnbicoll_l](mbsnbcoll-mbsnbcoll-l-mbsnbicoll-mbsnbicoll-l.md)<br/>
[setlocale、_wsetlocale](setlocale-wsetlocale.md)<br/>
[strcmp、wcscmp、_mbscmp](strcmp-wcscmp-mbscmp.md)<br/>
[_stricmp、_wcsicmp、_mbsicmp、_stricmp_l、_wcsicmp_l、_mbsicmp_l](stricmp-wcsicmp-mbsicmp-stricmp-l-wcsicmp-l-mbsicmp-l.md)<br/>
[strncmp、wcsncmp、_mbsncmp、_mbsncmp_l](strncmp-wcsncmp-mbsncmp-mbsncmp-l.md)<br/>
[_strnicmp、_wcsnicmp、_mbsnicmp、_strnicmp_l、_wcsnicmp_l、_mbsnicmp_l](strnicmp-wcsnicmp-mbsnicmp-strnicmp-l-wcsnicmp-l-mbsnicmp-l.md)<br/>
[strxfrm、wcsxfrm、_strxfrm_l、_wcsxfrm_l](strxfrm-wcsxfrm-strxfrm-l-wcsxfrm-l.md)<br/>
