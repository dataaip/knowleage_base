# mbrlen

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstowcsmbstowcs_s(C11) | | | | | | btowc(C95) | | | | | | mbrtowc(C95) | | | | | | mbsrtowcsmbsrtowcs_s(C95)(C11) | | | | | | mbrtoc8(C23) | | | | | | c8rtomb(C23) | | | | | | mbrtoc16(C11) | | | | | | c16rtomb(C11) | | | | | | c32rtomb(C11) | | | | | | mbrtoc32(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbtowc | | | | | | wctombwctomb_s(C11) | | | | | | wcstombswcstombs_s(C11) | | | | | | wctob(C95) | | | | | | wcrtombwcrtomb_s(C95)(C11) | | | | | | wcsrtombswcsrtombs_s(C95)(C11) | | | | | | ****mbrlen****(C95) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstate_t(C95) | | | | | | char8_t(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | char16_t(C11) | | | | | | char32_t(C11) | | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_CUR_MAX | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<wchar.h>` |  |  |
| size_t mbrlen( const char\* s, size_t n, mbstate_t\* ps ); |  | (since C95)  (until C99) |
| size_t mbrlen( const char\* restrict s, size_t n, mbstate_t\* restrict ps ); |  | (since C99) |
|  |  |  |

Determines the size, in bytes, of the representation of a multibyte character.

This function is equivalent to the call mbrtowc(NULL, s, n, ps ? ps : &internal) for some hidden object internal of type mbstate_t, except that the expression ps is evaluated only once.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to an element of a multibyte character string |
| n | - | limit on the number of bytes in s that can be examined |
| ps | - | pointer to the variable holding the conversion state |

### Return value

The first of the following that applies:

- ​0​ if the next n or fewer bytes complete the null character or if s is a null pointer. Both cases reset the conversion state.
- the number of bytes [1...n] that complete a valid multibyte character
- (size_t)-2 if the next n bytes are part of a possibly valid multibyte character, which is still incomplete after examining all n bytes
- (size_t)-1 if encoding error occurs. The value of errno is EILSEQ; the conversion state is unspecified.

### Example

Run this code

```
#include <locale.h>
#include <stdio.h>
#include <string.h>
#include <wchar.h>
 
int main(void)
{
    // allow mbrlen() to work with UTF-8 multibyte encoding
    setlocale(LC_ALL, "en_US.utf8");
 
    // UTF-8 narrow multibyte encoding
    const char* str = "水";
    size_t sz = strlen(str);
 
    mbstate_t mb;
    memset(&mb, 0, sizeof mb);
    int len1 = mbrlen(str, 1, &mb);
    if (len1 == -2)
        printf("The first 1 byte of %s is an incomplete multibyte char"
               " (mbrlen returns -2)\n", str);
 
    int len2 = mbrlen(str + 1, sz - 1, &mb);
    printf("The remaining %zu  bytes of %s hold %d bytes of the multibyte"
           " character\n", sz - 1, str, len2);
 
    printf("Attempting to call mbrlen() in the middle of %s while in initial"
           " shift state returns %zd\n", str, mbrlen(str + 1, sz - 1, &mb));
}

```

Output:

```
The first 1 byte of 水 is an incomplete multibyte char (mbrlen returns -2)
The remaining 2  bytes of 水 hold 2 bytes of the multibyte character
Attempting to call mbrlen() in the middle of 水 while in initial shift state returns -1

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.29.6.3.1 The mbrlen function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.29.6.3.1 The mbrlen function (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.29.6.3.1 The mbrlen function (p: 442)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.24.6.3.1 The mbrlen function (p: 388)

### See also

|  |  |
| --- | --- |
| mbrtowc(C95) | converts the next multibyte character to wide character, given state   (function) |
| mblen | returns the number of bytes in the next multibyte character   (function) |
| C++ documentation for mbrlen | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/multibyte/mbrlen&oldid=176729>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 October 2024, at 15:19.