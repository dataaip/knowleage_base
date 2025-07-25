# std::wcsrtombs

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | Wide/multibyte examination | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbrlen | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbsinit | | | | | |  | | | | | | | Multibyte/wide conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbtowc | | | | | | mbstowcs | | | | | | btowc | | | | | | mbrtowc | | | | | | mbsrtowcs | | | | | | wctomb | | | | | | wcstombs | | | | | | wctob | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcrtomb | | | | | | ****wcsrtombs**** | | | | | | mbrtoc8(C++20) | | | | | | mbrtoc16(C++11) | | | | | | mbrtoc32(C++11) | | | | | | c8rtomb(C++20) | | | | | | c16rtomb(C++11) | | | | | | c32rtomb(C++11) | | | | | | |
| Types | | | | |
| mbstate_t | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX MB_CUR_MAX | | | | | | __STDC_UTF_16__ __STDC_UTF_32__(C++11)(C++11) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cwchar>` |  |  |
| std::size_t wcsrtombs( char\* dst,  const wchar_t\*\* src,                         std::size_t len, std::mbstate_t\* ps ); |  |  |
|  |  |  |

Converts a sequence of wide characters from the array whose first element is pointed to by \*src to its narrow multibyte representation that begins in the conversion state described by \*ps. If dst is not null, converted characters are stored in the successive elements of the char array pointed to by dst. No more than len bytes are written to the destination array.

Each character is converted as if by a call to std::wcrtomb. The conversion stops if:

- The null character was converted and stored. src is set to a null pointer and \*ps represents the initial shift state.
- A wchar_t was found that does not correspond to a valid character in the current C locale. src is set to point at the first unconverted wide character.
- The next multibyte character to be stored would exceed len. src is set to point at the first unconverted wide character. This condition is not checked if dst is a null pointer.

### Parameters

|  |  |  |
| --- | --- | --- |
| dst | - | pointer to narrow character array where the multibyte characters will be stored |
| src | - | pointer to pointer to the first element of a null-terminated wide string |
| len | - | number of bytes available in the array pointed to by dst |
| ps | - | pointer to the conversion state object |

### Return value

On success, returns the number of bytes (including any shift sequences, but excluding the terminating '\0') written to the character array whose first element is pointed to by dst. If dst is a null pointer, returns the number of bytes that would have been written (again, excluding the terminating null character '\0').

On conversion error (if invalid wide character was encountered), returns static_cast<std::size_t>(-1), stores EILSEQ in errno, and leaves \*ps in unspecified state.

### Example

Run this code

```
#include <clocale>
#include <cwchar>
#include <iostream>
#include <string>
#include <vector>
 
void print_wide(const wchar_t* wstr)
{
    std::mbstate_t state = std::mbstate_t();
    std::size_t len = 1 + std::wcsrtombs(nullptr, &wstr, 0, &state);
    std::vector<char> mbstr(len);
    std::wcsrtombs(&mbstr[0], &wstr, mbstr.size(), &state);
    std::cout << "multibyte string: " << &mbstr[0] << '\n'
              << "Length, including '\\0': " << mbstr.size() << '\n';
}
 
int main()
{
    std::setlocale(LC_ALL, "en_US.utf8");
    // UTF-8 narrow multibyte encoding
    const wchar_t* wstr = L"z\u00df\u6c34\U0001d10b"; // or L"zß水𝄋"
    print_wide(wstr);
}

```

Output:

```
multibyte string: zß水𝄋
Length, including '\0': 11

```

### See also

|  |  |
| --- | --- |
| wcrtomb | converts a wide character to its multibyte representation, given state   (function) |
| mbsrtowcs | converts a narrow multibyte character string to wide string, given state   (function) |
| do_out[virtual] | converts a string from `InternT` to `ExternT`, such as when writing to file   (virtual protected member function of `std::codecvt<InternT,ExternT,StateT>`) |
| C documentation for wcsrtombs | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/multibyte/wcsrtombs&oldid=153088>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 June 2023, at 22:44.