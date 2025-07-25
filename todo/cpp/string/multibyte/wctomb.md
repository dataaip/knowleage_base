# std::wctomb

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | Wide/multibyte examination | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbrlen | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbsinit | | | | | |  | | | | | | | Multibyte/wide conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbtowc | | | | | | mbstowcs | | | | | | btowc | | | | | | mbrtowc | | | | | | mbsrtowcs | | | | | | ****wctomb**** | | | | | | wcstombs | | | | | | wctob | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcrtomb | | | | | | wcsrtombs | | | | | | mbrtoc8(C++20) | | | | | | mbrtoc16(C++11) | | | | | | mbrtoc32(C++11) | | | | | | c8rtomb(C++20) | | | | | | c16rtomb(C++11) | | | | | | c32rtomb(C++11) | | | | | | |
| Types | | | | |
| mbstate_t | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX MB_CUR_MAX | | | | | | __STDC_UTF_16__ __STDC_UTF_32__(C++11)(C++11) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstdlib>` |  |  |
| int wctomb( char\* s, wchar_t wc ); |  |  |
|  |  |  |

Converts a wide character wc to multibyte encoding and stores it (including any shift sequences) in the char array whose first element is pointed to by s. No more than MB_CUR_MAX characters are stored. The conversion is affected by the current locale's LC_CTYPE category.

If wc is the null character, the null byte is written to s, preceded by any shift sequences necessary to restore the initial shift state.

If s is a null pointer, resets the global conversion state and determines whether shift sequences are used.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to the character array for output |
| wc | - | wide character to convert |

### Return value

If s is not a null pointer, returns the number of bytes that are contained in the multibyte representation of wc or -1 if wc is not a valid character.

If s is a null pointer, resets its internal conversion state to represent the initial shift state and returns ​0​ if the current multibyte encoding is not state-dependent (does not use shift sequences) or a non-zero value if the current multibyte encoding is state-dependent (uses shift sequences).

### Notes

Each call to `wctomb` updates the internal global conversion state (a static object of type std::mbstate_t, only known to this function). If the multibyte encoding uses shift states, this function is not reentrant. In any case, multiple threads should not call `wctomb` without synchronization: std::wcrtomb may be used instead.

### Example

Run this code

```
#include <clocale>
#include <cstdlib>
#include <iomanip>
#include <iostream>
#include <string>
 
void print_wide(const std::wstring& wstr)
{
    bool shifts = std::wctomb(nullptr, 0); // reset the conversion state
    std::cout << "shift sequences are " << (shifts ? "" : "not" )
              << " used\n" << std::uppercase << std::setfill('0');
    for (const wchar_t wc : wstr)
    {
        std::string mb(MB_CUR_MAX, '\0');
        const int ret = std::wctomb(&mb[0], wc);
        const char* s = ret > 1 ? "s" : "";
        std::cout << "multibyte char '" << mb << "' is " << ret
                  << " byte" << s << ": [" << std::hex;
        for (int i{0}; i != ret; ++i)
        {
            const int c = 0xFF & mb[i];
            std::cout << (i ? " " : "") << std::setw(2) << c;
        }
        std::cout << "]\n" << std::dec;
    }
}
 
int main()
{
    std::setlocale(LC_ALL, "en_US.utf8");
    // UTF-8 narrow multibyte encoding
    std::wstring wstr = L"z\u00df\u6c34\U0001d10b"; // or L"zß水𝄋"
    print_wide(wstr);
}

```

Output:

```
shift sequences are not used
multibyte char 'z' is 1 byte: [7A]
multibyte char 'ß' is 2 bytes: [C3 9F]
multibyte char '水' is 3 bytes: [E6 B0 B4]
multibyte char '𝄋' is 4 bytes: [F0 9D 84 8B]

```

### See also

|  |  |
| --- | --- |
| mbtowc | converts the next multibyte character to wide character   (function) |
| wcrtomb | converts a wide character to its multibyte representation, given state   (function) |
| do_out[virtual] | converts a string from `InternT` to `ExternT`, such as when writing to file   (virtual protected member function of `std::codecvt<InternT,ExternT,StateT>`) |
| C documentation for wctomb | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/multibyte/wctomb&oldid=153684>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 June 2023, at 14:23.