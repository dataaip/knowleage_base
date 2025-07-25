# std::wcsncmp

From cppreference.com
< cpp‎ | string‎ | wide
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

Null-terminated wide strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Character classification | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iswalnum | | | | | | iswalpha | | | | | | iswlower | | | | | | iswupper | | | | | | iswdigit | | | | | | iswxdigit | | | | | | wctype | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iswblank(C++11) | | | | | | iswctype | | | | | | iswcntrl | | | | | | iswgraph | | | | | | iswspace | | | | | | iswprint | | | | | | iswpunct | | | | | |
| Character manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | towlower | | | | | | towupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | towctrans | | | | | | wctrans | | | | | |
| Conversions to numeric formats | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcstolwcstoll(C++11) | | | | | | wcstofwcstodwcstold(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcstoulwcstoull(C++11) | | | | | | wcstoimaxwcstouimax(C++11)(C++11) | | | | | |  | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcslen | | | | | | wcscmp | | | | | | wcscoll | | | | | | ****wcsncmp**** | | | | | | wcschr | | | | | | wcsrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcspbrk | | | | | | wcsspn | | | | | | wcscspn | | | | | | wcsstr | | | | | | wcstok | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcscpy | | | | | | wcsncpy | | | | | | wcsxfrm | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wcscat | | | | | | wcsncat | | | | | |  | | | | | |
| Array manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | wmemcpy | | | | | | wmemmove | | | | | | wmemcmp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | wmemchr | | | | | | wmemset | | | | | |  | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Types | | | | | | wctrans_t | | | | | | wctype_t | | | | | | wint_t | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Macros | | | | | | WCHAR_MIN WCHAR_MAX WEOF | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cwchar>` |  |  |
| int wcsncmp( const wchar_t\* lhs, const wchar_t\* rhs, std::size_t count ); |  |  |
|  |  |  |

Compares at most count wide characters of two null-terminated wide strings. The comparison is done lexicographically.

The sign of the result is the sign of the difference between the values of the first pair of wide characters that differ in the strings being compared.

The behavior is undefined if lhs or rhs are not pointers to null-terminated strings.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | pointers to the null-terminated wide strings to compare |
| count | - | maximum number of characters to compare |

### Return value

Negative value if lhs appears before rhs in lexicographical order.

Zero if lhs and rhs compare equal.

Positive value if lhs appears after rhs in lexicographical order.

### Example

Run this code

```
#include <clocale>
#include <cwchar>
#include <iostream>
#include <locale>
 
void demo(const wchar_t* lhs, const wchar_t* rhs, int sz)
{
    int rc = std::wcsncmp(lhs, rhs, sz);
    if (rc == 0)
        std::wcout << "First " << sz << " characters of ["
                   << lhs << "] equal [" << rhs << "]\n";
    else if (rc < 0)
        std::wcout << "First " << sz << " characters of ["
                   << lhs << "] precede [" << rhs << "]\n";
    else if (rc > 0)
        std::wcout << "First " << sz << " characters of ["
                   << lhs << "] follow [" << rhs << "]\n";
}
 
int main()
{
    const wchar_t str1[] = L"안녕하세요";
    const wchar_t str2[] = L"안녕히 가십시오";
 
    std::setlocale(LC_ALL, "en_US.utf8");
    std::wcout.imbue(std::locale("en_US.utf8"));
    demo(str1, str2, 5);
    demo(str2, str1, 8);
    demo(str1, str2, 2);
}

```

Output:

```
First 5 characters of [안녕하세요] precede [안녕히 가십시오]
First 8 characters of [안녕히 가십시오] follow [안녕하세요]
First 2 characters of [안녕하세요] equal [안녕히 가십시오]

```

### See also

|  |  |
| --- | --- |
| strncmp | compares a certain number of characters from two strings   (function) |
| wcscmp | compares two wide strings   (function) |
| wmemcmp | compares a certain amount of wide characters from two arrays   (function) |
| wcscoll | compares two wide strings in accordance to the current locale   (function) |
| C documentation for wcsncmp | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/wide/wcsncmp&oldid=153113>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 June 2023, at 09:02.