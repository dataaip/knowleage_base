# std::c32rtomb

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | Wide/multibyte examination | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbrlen | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbsinit | | | | | |  | | | | | | | Multibyte/wide conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbtowc | | | | | | mbstowcs | | | | | | btowc | | | | | | mbrtowc | | | | | | mbsrtowcs | | | | | | wctomb | | | | | | wcstombs | | | | | | wctob | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcrtomb | | | | | | wcsrtombs | | | | | | mbrtoc8(C++20) | | | | | | mbrtoc16(C++11) | | | | | | mbrtoc32(C++11) | | | | | | c8rtomb(C++20) | | | | | | c16rtomb(C++11) | | | | | | ****c32rtomb****(C++11) | | | | | | |
| Types | | | | |
| mbstate_t | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX MB_CUR_MAX | | | | | | __STDC_UTF_16__ __STDC_UTF_32__(C++11)(C++11) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cuchar>` |  |  |
| std::size_t c32rtomb( char\* s, char32_t c32, std::mbstate_t\* ps ); |  | (since C++11) |
|  |  |  |

Converts a UTF-32 character to its narrow multibyte representation.

If s is not a null pointer, the function determines the number of bytes necessary to store the multibyte character representation of c32 (including any shift sequences, and taking into account the current multibyte conversion state \*ps), and stores the multibyte character representation in the character array whose first element is pointed to by s, updating \*ps as necessary. At most MB_CUR_MAX bytes can be written by this function.

If s is a null pointer, the call is equivalent to std::c32rtomb(buf, U'\0', ps) for some internal buffer `buf`.

If c32 is the null wide character U'\0', a null byte is stored, preceded by any shift sequence necessary to restore the initial shift state and the conversion state parameter \*ps is updated to represent the initial shift state.

The multibyte encoding used by this function is specified by the currently active C locale.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to narrow character array where the multibyte character will be stored |
| c32 | - | the 32-bit character to convert |
| ps | - | pointer to the conversion state object used when interpreting the multibyte string |

### Return value

On success, returns the number of bytes (including any shift sequences) written to the character array whose first element is pointed to by s. This value may be ​0​, e.g. when processing the first char32_t in multi-char32_t-character sequence (does not occur in UTF-32).

On failure (if c32 is not a valid 32-bit character), returns -1, stores EILSEQ in errno, and leaves \*ps in unspecified state.

### Example

Run this code

```
#include <climits>
#include <clocale>
#include <cuchar>
#include <iomanip>
#include <iostream>
#include <string_view>
 
int main()
{
    std::setlocale(LC_ALL, "en_US.utf8");
    std::u32string_view strv = U"zß水🍌"; // or z\u00df\u6c34\U0001F34C
    std::cout << "Processing " << strv.size() << " UTF-32 code units: [ ";
    for (char32_t c : strv)
        std::cout << std::showbase << std::hex << static_cast<int>(c) << ' ';
    std::cout << "]\n";
 
    std::mbstate_t state{};
    char out[MB_LEN_MAX]{};
    for (char32_t c : strv)
    {
        std::size_t rc = std::c32rtomb(out, c, &state);
        std::cout << static_cast<int>(c) << " converted to [ ";
        if (rc != (std::size_t) - 1)
            for (unsigned char c8 : std::string_view{out, rc})
                std::cout << +c8 << ' ';
        std::cout << "]\n";
    }
}

```

Output:

```
Processing 4 UTF-32 code units: [ 0x7a 0xdf 0x6c34 0x1f34c ]
0x7a converted to [ 0x7a ]
0xdf converted to [ 0xc3 0x9f ]
0x6c34 converted to [ 0xe6 0xb0 0xb4 ]
0x1f34c converted to [ 0xf0 0x9f 0x8d 0x8c ]

```

### See also

|  |  |
| --- | --- |
| mbrtoc32(C++11) | converts a narrow multibyte character to UTF-32 encoding   (function) |
| do_out[virtual] | converts a string from `InternT` to `ExternT`, such as when writing to file   (virtual protected member function of `std::codecvt<InternT,ExternT,StateT>`) |
| C documentation for c32rtomb | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/multibyte/c32rtomb&oldid=177819>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 November 2024, at 14:46.