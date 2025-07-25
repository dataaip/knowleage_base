# char32_t

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstowcsmbstowcs_s(C11) | | | | | | btowc(C95) | | | | | | mbrtowc(C95) | | | | | | mbsrtowcsmbsrtowcs_s(C95)(C11) | | | | | | mbrtoc8(C23) | | | | | | c8rtomb(C23) | | | | | | mbrtoc16(C11) | | | | | | c16rtomb(C11) | | | | | | c32rtomb(C11) | | | | | | mbrtoc32(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbtowc | | | | | | wctombwctomb_s(C11) | | | | | | wcstombswcstombs_s(C11) | | | | | | wctob(C95) | | | | | | wcrtombwcrtomb_s(C95)(C11) | | | | | | wcsrtombswcsrtombs_s(C95)(C11) | | | | | | mbrlen(C95) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstate_t(C95) | | | | | | char8_t(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | char16_t(C11) | | | | | | ****char32_t****(C11) | | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_CUR_MAX | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<uchar.h>` |  |  |
| typedef uint_least32_t char32_t; |  | (since C11) |
|  |  |  |

char32_t is an unsigned integer type used for 32-bit wide characters and is the same type as uint_least32_t.

### Notes

On any given platform, by the definition of uint_least32_t, the width of type char32_t can be greater than 32 bits, but the actual values stored in an object of type char32_t will always have a width of 32 bits.

### Example

Run this code

```
#include <stdio.h>
#include <uchar.h>
 
int main(void)
{
    const char32_t wc[] = U"zß水🍌"; // or "z\u00df\u6c34\U0001f34c"
    const size_t wc_sz = sizeof wc / sizeof *wc;
    printf("%zu UTF-32 code units: [ ", wc_sz);
    for (size_t n = 0; n < wc_sz; ++n)
        printf("%#x ", wc[n]);
    printf("]\n");
}

```

Possible output:

```
5 UTF-32 code units: [ 0x7a 0xdf 0x6c34 0x1f34c 0 ]

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.28 Unicode utilities <uchar.h> (p: 292)

:   - 7.20.1.2 Minimum-width integer types (p: 212-213)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.28 Unicode utilities <uchar.h> (p: 398)

:   - 7.20.1.2 Minimum-width integer types (p: 290)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.18.1.2 Minimum-width integer types (p: 256)

### See also

|  |  |
| --- | --- |
| C++ documentation for Fundamental types | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/multibyte/char32_t&oldid=149703>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 March 2023, at 09:36.