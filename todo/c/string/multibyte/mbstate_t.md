# mbstate_t

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****mbstate_t****(C95) | | | | | | char8_t(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | char16_t(C11) | | | | | | char32_t(C11) | | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_CUR_MAX | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<uchar.h>` |  | (since C11) |
| Defined in header `<wchar.h>` |  |  |
| struct mbstate_t; |  | (since C95) |
|  |  |  |

The type `mbstate_t` is a trivial non-array type that can represent any of the conversion states that can occur in an implementation-defined set of supported multibyte character encoding rules. Zero-initialized value of `mbstate_t` represents the initial conversion state, although other values of `mbstate_t` may exist that also represent the initial conversion state.

Possible implementation of `mbstate_t` is a struct type holding an array representing the incomplete multibyte character, an integer counter indicating the number of bytes in the array that have been processed, and a representation of the current shift state.

The following functions should not be called from multiple threads without synchronization with the mbstate_t\* argument of a null pointer due to possible data races: mbrlen, mbrtowc, mbsrtowcs, mbtowc, wcrtomb, wcsrtombs, wctomb.

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.29.1/2 Introduction (p: 402)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.24.1/2 Introduction (p: 348)

### See also

|  |  |
| --- | --- |
| mbsinit(C95) | checks if the mbstate_t object represents initial shift state   (function) |
| C++ documentation for mbstate_t | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/multibyte/mbstate_t&oldid=119771>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 June 2020, at 20:13.