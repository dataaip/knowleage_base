# mbrtoc8

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstowcsmbstowcs_s(C11) | | | | | | btowc(C95) | | | | | | mbrtowc(C95) | | | | | | mbsrtowcsmbsrtowcs_s(C95)(C11) | | | | | | ****mbrtoc8****(C23) | | | | | | c8rtomb(C23) | | | | | | mbrtoc16(C11) | | | | | | c16rtomb(C11) | | | | | | c32rtomb(C11) | | | | | | mbrtoc32(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbtowc | | | | | | wctombwctomb_s(C11) | | | | | | wcstombswcstombs_s(C11) | | | | | | wctob(C95) | | | | | | wcrtombwcrtomb_s(C95)(C11) | | | | | | wcsrtombswcsrtombs_s(C95)(C11) | | | | | | mbrlen(C95) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbstate_t(C95) | | | | | | char8_t(C23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | char16_t(C11) | | | | | | char32_t(C11) | | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_CUR_MAX | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<uchar.h>` |  |  |
| size_t mbrtoc8( char8_t \* restrict pc8, const char \* restrict s,                  size_t n, mbstate_t \* restrict ps ); |  | (since C23) |
|  |  |  |

Converts a narrow multibyte character to UTF-8 encoding.

If `s` is not a null pointer, inspects at most `n` bytes of the multibyte character string, beginning with the byte pointed to by `s` to determine the number of bytes necessary to complete the next multibyte character (including any shift sequences). If the function determines that the next multibyte character in `s` is complete and valid, converts it to UTF-8 and stores the first UTF-8 code unit in \*pc8 (if `pc8` is not null).

If UTF-8 encoding of the multibyte character in `*s` consists of more than one UTF-8 code unit, then after the first call to this function, `*ps` is updated in such a way that the next call to `mbrtoc8` will write out the additional UTF-8 code units, without considering `*s`.

If `s` is a null pointer, the values of `n` and `pc8` are ignored and the call is equivalent to mbrtoc8(nullptr, "", 1, ps).

If UTF-8 code unit produced is u8'\0', the conversion state \*ps represents the initial shift state.

The multibyte encoding used by this function is specified by the currently active C locale.

### Parameters

|  |  |  |
| --- | --- | --- |
| pc8 | - | pointer to the location where the resulting UTF-8 code units will be written |
| s | - | pointer to the multibyte character string used as input |
| n | - | limit on the number of bytes in s that can be examined |
| ps | - | pointer to the conversion state object used when interpreting the multibyte string |

### Return value

The first of the following that applies:

- ​0​ if the character converted from `s` (and stored in \*pc8 if non-null) was the null character
- the number of bytes [1...n] of the multibyte character successfully converted from `s`
- (size_t)-3 if the next UTF-8 code unit from a character whose encoding consists of multiple code units has now been written to \*pc8. No bytes are processed from the input in this case.
- (size_t)-2 if the next `n` bytes constitute an incomplete, but so far valid, multibyte character. Nothing is written to \*pc8.
- (size_t)-1 if encoding error occurs. Nothing is written to `*pc8`, the value EILSEQ is stored in errno and the value of \*ps is unspecified.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| c8rtomb(C23) | converts UTF-8 string to narrow multibyte encoding   (function) |
| C++ documentation for mbrtoc8 | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/multibyte/mbrtoc8&oldid=146481>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 January 2023, at 08:21.