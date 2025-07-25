# std::wcrtomb

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | Wide/multibyte examination | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mblen | | | | | | mbrlen | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbsinit | | | | | |  | | | | | | | Multibyte/wide conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mbtowc | | | | | | mbstowcs | | | | | | btowc | | | | | | mbrtowc | | | | | | mbsrtowcs | | | | | | wctomb | | | | | | wcstombs | | | | | | wctob | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****wcrtomb**** | | | | | | wcsrtombs | | | | | | mbrtoc8(C++20) | | | | | | mbrtoc16(C++11) | | | | | | mbrtoc32(C++11) | | | | | | c8rtomb(C++20) | | | | | | c16rtomb(C++11) | | | | | | c32rtomb(C++11) | | | | | | |
| Types | | | | |
| mbstate_t | | | | |
| Macros | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | MB_LEN_MAX MB_CUR_MAX | | | | | | __STDC_UTF_16__ __STDC_UTF_32__(C++11)(C++11) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cwchar>` |  |  |
| std::size_t wcrtomb( char\* s, wchar_t wc, std::mbstate_t\* ps ); |  |  |
|  |  |  |

Converts a wide character to its narrow multibyte representation.

If s is not a null pointer, the function determines the number of bytes necessary to store the multibyte character representation of wc (including any shift sequences, and taking into account the current multibyte conversion state \*ps), and stores the multibyte character representation in the character array whose first element is pointed to by s, updating \*ps as necessary. At most MB_CUR_MAX bytes can be written by this function.

If s is a null pointer, the call is equivalent to std::wcrtomb(buf, L'\0', ps) for some internal buffer `buf`.

If wc is the null wide character L'\0', a null byte is stored, preceded by any shift sequence necessary to restore the initial shift state and the conversion state parameter \*ps is updated to represent the initial shift state.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to narrow character array where the multibyte character will be stored |
| wc | - | the wide character to convert |
| ps | - | pointer to the conversion state object used when interpreting the multibyte string |

### Return value

On success, returns the number of bytes (including any shift sequences) written to the character array whose first element is pointed to by s.

On failure (if wc is not a valid wide character), returns static_cast<std::size_t>(-1), stores EILSEQ in errno, and leaves \*ps in unspecified state.

### Example

Run this code

```
#include <clocale>
#include <cwchar>
#include <iostream>
#include <string>
 
void print_wide(const std::wstring& wstr)
{
    std::mbstate_t state{};
    for (wchar_t wc : wstr)
    {
        std::string mb(MB_CUR_MAX, '\0');
        std::size_t ret = std::wcrtomb(&mb[0], wc, &state);
        std::cout << "multibyte char " << mb << " is " << ret << " bytes\n";
    }
}
 
int main()
{
    std::setlocale(LC_ALL, "en_US.utf8");
    std::wstring wstr = L"z\u00df\u6c34\U0001f34c"; // or L"zß水🍌"
    print_wide(wstr);
}

```

Output:

```
multibyte char z is 1 bytes
multibyte char ß is 2 bytes
multibyte char 水 is 3 bytes
multibyte char 🍌 is 4 bytes

```

### See also

|  |  |
| --- | --- |
| wctomb | converts a wide character to its multibyte representation   (function) |
| mbrtowc | converts the next multibyte character to wide character, given state   (function) |
| do_out[virtual] | converts a string from `InternT` to `ExternT`, such as when writing to file   (virtual protected member function of `std::codecvt<InternT,ExternT,StateT>`) |
| C documentation for wcrtomb | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/multibyte/wcrtomb&oldid=153087>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 June 2023, at 22:40.