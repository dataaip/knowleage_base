# std::mbsrtowcs

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | Wide/multibyte examination | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbrlen | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbsinit | | | | | |  | | | | | | | Multibyte/wide conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbtowc | | | | | | mbstowcs | | | | | | btowc | | | | | | mbrtowc | | | | | | ****mbsrtowcs**** | | | | | | wctomb | | | | | | wcstombs | | | | | | wctob | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcrtomb | | | | | | wcsrtombs | | | | | | mbrtoc8(C++20) | | | | | | mbrtoc16(C++11) | | | | | | mbrtoc32(C++11) | | | | | | c8rtomb(C++20) | | | | | | c16rtomb(C++11) | | | | | | c32rtomb(C++11) | | | | | | |
| Types | | | | |
| mbstate_t | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX MB_CUR_MAX | | | | | | __STDC_UTF_16__ __STDC_UTF_32__(C++11)(C++11) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cwchar>` |  |  |
| std::size_t mbsrtowcs( wchar_t\* dst,  const char\*\* src,                         std::size_t len, std::mbstate_t\* ps ); |  |  |
|  |  |  |

Converts a null-terminated multibyte character sequence, which begins in the conversion state described by \*ps, from the array whose first element is pointed to by \*src to its wide character representation. If dst is not null, converted characters are stored in the successive elements of the wchar_t array pointed to by dst. No more than len wide characters are written to the destination array.

Each multibyte character is converted as if by a call to std::mbrtowc. The conversion stops if:

- The multibyte null character was converted and stored. src is set to a null pointer and `*ps` represents the initial shift state.
- An invalid multibyte character (according to the current C locale) was encountered. src is set to point at the beginning of the first unconverted multibyte character.
- The next wide character to be stored would exceed len. src is set to point at the beginning of the first unconverted multibyte character. This condition is not checked if dst is a null pointer.

### Parameters

|  |  |  |
| --- | --- | --- |
| dst | - | pointer to wide character array where the results will be stored |
| src | - | pointer to pointer to the first element of a null-terminated multibyte string |
| len | - | number of wide characters available in the array pointed to by dst |
| ps | - | pointer to the conversion state object |

### Return value

On success, returns the number of wide characters, excluding the terminating L'\0', written to the character array. If dst is a null pointer, returns the number of wide characters that would have been written given unlimited length.

On conversion error (if invalid multibyte character was encountered), returns static_cast<std::size_t>(-1), stores EILSEQ in errno, and leaves \*ps in unspecified state.

### Notes

This function moves the src pointer to the end of the converted multibyte string. This doesn't happen if dst is a null pointer.

### Example

Run this code

```
#include <clocale>
#include <cwchar>
#include <iostream>
#include <vector>
 
void print_as_wide(const char* mbstr)
{
    std::mbstate_t state = std::mbstate_t();
    std::size_t len = 1 + std::mbsrtowcs(nullptr, &mbstr, 0, &state);
    std::vector<wchar_t> wstr(len);
    std::mbsrtowcs(&wstr[0], &mbstr, wstr.size(), &state);
    std::wcout << "Wide string: " << &wstr[0] << '\n'
               << "The length, including '\\0': " << wstr.size() << '\n';
}
 
int main()
{
    std::setlocale(LC_ALL, "en_US.utf8");
    const char* mbstr = "z\u00df\u6c34\U0001f34c"; // or u8"zß水🍌"
    print_as_wide(mbstr);
}

```

Output:

```
Wide string: zß水🍌
The length, including '\0': 5

```

### See also

|  |  |
| --- | --- |
| mbrtowc | converts the next multibyte character to wide character, given state   (function) |
| wcsrtombs | converts a wide string to narrow multibyte character string, given state   (function) |
| do_in[virtual] | converts a string from `ExternT` to `InternT`, such as when reading from file   (virtual protected member function of `std::codecvt<InternT,ExternT,StateT>`) |
| C documentation for mbsrtowcs | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/multibyte/mbsrtowcs&oldid=153084>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 June 2023, at 22:28.