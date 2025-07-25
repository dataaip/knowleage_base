# std::c8rtomb

From cppreference.com
< cpp‎ | string‎ | multibyte
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Freestanding and hosted | | | | |
| Language | | | | |
| Standard library | | | | |
| Standard library headers | | | | |
| Named requirements | | | | |
| Feature test macros (C++20) | | | | |
| Language support library | | | | |
| Concepts library (C++20) | | | | |
| Diagnostics library | | | | |
| Memory management library | | | | |
| Metaprogramming library (C++11) | | | | |
| General utilities library | | | | |
| Containers library | | | | |
| Iterators library | | | | |
| Ranges library (C++20) | | | | |
| Algorithms library | | | | |
| Strings library | | | | |
| Text processing library | | | | |
| Numerics library | | | | |
| Date and time library | | | | |
| Input/output library | | | | |
| Filesystem library (C++17) | | | | |
| Concurrency support library (C++11) | | | | |
| Execution support library (C++26) | | | | |
| Technical specifications | | | | |
| Symbols index | | | | |
| External libraries | | | | |

Text processing library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Localization library | | | | |
| Regular expressions library (C++11) | | | | |
| Formatting library (C++20) | | | | |
| Null-terminated sequence utilities | | | | |
| Byte strings | | | | |
| Multibyte strings | | | | |
| Wide strings | | | | |
| Primitive numeric conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_chars(C++17) | | | | | | to_chars_result(C++17) | | | | | | from_chars(C++17) | | | | | | from_chars_result(C++17) | | | | | | chars_format(C++17) | | | | | |
| Text encoding identifications | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | text_encoding(C++26) | | | | | |

Null-terminated multibyte strings

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | Wide/multibyte examination | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbrlen | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbsinit | | | | | |  | | | | | | | Multibyte/wide conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbtowc | | | | | | mbstowcs | | | | | | btowc | | | | | | mbrtowc | | | | | | mbsrtowcs | | | | | | wctomb | | | | | | wcstombs | | | | | | wctob | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcrtomb | | | | | | wcsrtombs | | | | | | mbrtoc8(C++20) | | | | | | mbrtoc16(C++11) | | | | | | mbrtoc32(C++11) | | | | | | ****c8rtomb****(C++20) | | | | | | c16rtomb(C++11) | | | | | | c32rtomb(C++11) | | | | | | |
| Types | | | | |
| mbstate_t | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX MB_CUR_MAX | | | | | | __STDC_UTF_16__ __STDC_UTF_32__(C++11)(C++11) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cuchar>` |  |  |
| std::size_t c8rtomb( char\* s, char8_t c8, std::mbstate_t\* ps ); |  | (since C++20) |
|  |  |  |

Converts a single code point from UTF-8 to a narrow multibyte character representation.

If s is not a null pointer and c8 is the last code unit in a valid UTF-8 encoding of a code point, the function determines the number of bytes necessary to store the multibyte character representation of that code point (including any shift sequences, and taking into account the current multibyte conversion state \*ps), and stores the multibyte character representation in the character array whose first element is pointed to by s, updating \*ps as necessary. At most MB_CUR_MAX bytes can be written by this function.

If c8 is not the final UTF-8 code unit in a representation of a code point, the function does not write to the array pointed to by s, only \*ps is updated.

If s is a null pointer, the call is equivalent to std::c8rtomb(buf, u8'\0', ps) for some internal buffer `buf`.

If c8 is the null character u8'\0', a null byte is stored, preceded by any shift sequence necessary to restore the initial shift state and the conversion state parameter \*ps is updated to represent the initial shift state.

The multibyte encoding used by this function is specified by the currently active C locale.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to narrow character array where the multibyte character will be stored |
| c8 | - | the UTF-8 code unit to convert |
| ps | - | pointer to the conversion state object used when interpreting the multibyte string |

### Return value

The number of bytes stored in the array object (including any shift sequences). This may be zero when c8 is not the final code unit in the UTF-8 representation of a code point.

If c8 is invalid (does not contribute to a sequence of char8_t corresponding to a valid multibyte character), the value of the macro EILSEQ is stored in errno, static_cast<std::size_t>(-1) is returned, and the conversion state is unspecified.

### Notes

Calls to `c8rtomb` with a null pointer argument for s may introduce a data race with other calls to `c8rtomb` with a null pointer argument for s.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| mbrtoc8(C++20) | converts a narrow multibyte character to UTF-8 encoding   (function) |
| c16rtomb(C++11) | converts a UTF-16 character to narrow multibyte encoding   (function) |
| C documentation for c8rtomb | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/multibyte/c8rtomb&oldid=177815>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 November 2024, at 14:39.