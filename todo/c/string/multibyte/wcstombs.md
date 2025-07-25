# wcstombs, wcstombs_s

From cppreference.com
< c‎ | string‎ | multibyte
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 Strings library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Null-terminated byte strings | | | | |
| Null-terminated multibyte strings | | | | |
| Null-terminated wide strings | | | | |

 Null-terminated multibyte strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Wide/multibyte conversions | | | | |
| mbsinit(C95) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstowcsmbstowcs_s(C11) | | | | | | btowc(C95) | | | | | | mbrtowc(C95) | | | | | | mbsrtowcsmbsrtowcs_s(C95)(C11) | | | | | | mbrtoc8(C23) | | | | | | c8rtomb(C23) | | | | | | mbrtoc16(C11) | | | | | | c16rtomb(C11) | | | | | | c32rtomb(C11) | | | | | | mbrtoc32(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbtowc | | | | | | wctombwctomb_s(C11) | | | | | | ****wcstombswcstombs_s****(C11) | | | | | | wctob(C95) | | | | | | wcrtombwcrtomb_s(C95)(C11) | | | | | | wcsrtombswcsrtombs_s(C95)(C11) | | | | | | mbrlen(C95) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstate_t(C95) | | | | | | char8_t(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | char16_t(C11) | | | | | | char32_t(C11) | | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_CUR_MAX | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdlib.h>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| size_t wcstombs( char          \*dst, const wchar_t          \*src, size_t len ); |  | (until C99) |
| size_t wcstombs( char \*restrict dst, const wchar_t \*restrict src, size_t len ); |  | (since C99) |
|  |  |  |
| --- | --- | --- |
| errno_t wcstombs_s( size_t \*restrict retval, char \*restrict dst, rsize_t dstsz,                      const wchar_t \*restrict src, rsize_t len ); | (2) | (since C11) |
|  |  |  |

1) Converts a sequence of wide characters from the array whose first element is pointed to by `src` to its narrow multibyte representation that begins in the initial shift state. Converted characters are stored in the successive elements of the char array pointed to by `dst`. No more than `len` bytes are written to the destination array. Each character is converted as if by a call to wctomb, except that the wctomb's conversion state is unaffected. The conversion stops if: \* The null character L'\0' was converted and stored. The bytes stored in this case are the unshift sequence (if necessary) followed by '\0', \* A wchar_t was found that does not correspond to a valid character in the current C locale. \* The next multibyte character to be stored would exceed `len`. If `src` and `dst` overlap, the behavior is unspecified.2) Same as (1), except that \* conversion is as-if by wcrtomb, not wctomb \* the function returns its result as an out-parameter `retval` \* if the conversion stops without writing a null character, the function will store '\0' in the next byte in `dst`, which may be `dst[len]` or `dst[dstsz]`, whichever comes first (meaning up to len+1/dstsz+1 total bytes may be written). In this case, there may be no unshift sequence written before the terminating null. \* if `dst` is a null pointer, the number of bytes that would be produced is stored in \*retval \* the function clobbers the destination array from the terminating null and until `dstsz` \* If `src` and `dst` overlap, the behavior is unspecified. \* the following errors are detected at runtime and call the currently installed constraint handler function:

:   - `retval` or `src` is a null pointer
    - `dstsz` or `len` is greater than RSIZE_MAX (unless `dst` is null)
    - `dstsz` is not zero (unless `dst` is null)
    - `len` is greater than `dstsz` and the conversion does not encounter null or encoding error in the `src` array by the time `dstsz` is reached (unless `dst` is null)
:   As with all bounds-checked functions, `wcstombs_s` is only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <stdlib.h>.

### Notes

In most implementations, `wcstombs` updates a global static object of type mbstate_t as it processes through the string, and cannot be called simultaneously by two threads, wcsrtombs or `wcstombs_s` should be used in such cases.

POSIX specifies a common extension: if `dst` is a null pointer, this function returns the number of bytes that would be written to `dst`, if converted. Similar behavior is standard for wcsrtombs and `wcstombs_s`.

### Parameters

|  |  |  |
| --- | --- | --- |
| dst | - | pointer to narrow character array where the multibyte character will be stored |
| src | - | pointer to the first element of a null-terminated wide string to convert |
| len | - | number of bytes available in the array pointed to by dst |
| dstsz | - | max number of bytes that will be written (size of the `dst` array) |
| retval | - | pointer to a size_t object where the result will be stored |

### Return value

1) On success, returns the number of bytes (including any shift sequences, but excluding the terminating '\0') written to the character array whose first element is pointed to by `dst`. On conversion error (if invalid wide character was encountered), returns (size_t)-1.2) Returns zero on success (in which case the number of bytes excluding terminating zero that were, or would be written to `dst`, is stored in \*retval), non-zero on error. In case of a runtime constraint violation, stores (size_t)-1 in \*retval (unless `retval` is null) and sets dst[0] to '\0' (unless `dst` is null or `dstmax` is zero or greater than RSIZE_MAX)

### Example

Run this code

```
#include <stdio.h>
#include <stdlib.h>
#include <locale.h>
 
int main(void)
{
    // 4 wide characters
    const wchar_t src[] = L"z\u00df\u6c34\U0001f34c";
    // they occupy 10 bytes in UTF-8
    char dst[11];
 
    setlocale(LC_ALL, "en_US.utf8");
    printf("wide-character string: '%ls'\n",src);
    for (size_t ndx=0; ndx < sizeof src/sizeof src[0]; ++ndx)
        printf("   src[%2zu] = %#8x\n", ndx, src[ndx]);
 
    int rtn_val = wcstombs(dst, src, sizeof dst);
    printf("rtn_val = %d\n", rtn_val);
    if (rtn_val > 0)
        printf("multibyte string:  '%s'\n",dst);
    for (size_t ndx=0; ndx<sizeof dst; ++ndx)
        printf("   dst[%2zu] = %#2x\n", ndx, (unsigned char)dst[ndx]);
}

```

Output:

```
wide-character string: 'zß水🍌'
   src[ 0] =     0x7a
   src[ 1] =     0xdf
   src[ 2] =   0x6c34
   src[ 3] =  0x1f34c
   src[ 4] =        0
rtn_val = 10
multibyte string:  'zß水🍌'
   dst[ 0] = 0x7a
   dst[ 1] = 0xc3
   dst[ 2] = 0x9f
   dst[ 3] = 0xe6
   dst[ 4] = 0xb0
   dst[ 5] = 0xb4
   dst[ 6] = 0xf0
   dst[ 7] = 0x9f
   dst[ 8] = 0x8d
   dst[ 9] = 0x8c
   dst[10] =  0

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.22.8.2 The wcstombs function (p: 360)

:   - K.3.6.5.2 The wcstombs_s function (p: 612-614)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.20.8.2 The wcstombs function (p: 324)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.10.8.2 The wcstombs function

### See also

|  |  |
| --- | --- |
| wcsrtombswcsrtombs_s(C95)(C11) | converts a wide string to narrow multibyte character string, given state   (function) |
| mbstowcsmbstowcs_s(C11) | converts a narrow multibyte character string to wide string   (function) |
| C++ documentation for wcstombs | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/multibyte/wcstombs&oldid=101815>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 April 2018, at 15:43.