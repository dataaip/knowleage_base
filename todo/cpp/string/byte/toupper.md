# std::toupper

From cppreference.com
< cpp‎ | string‎ | byte
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

Null-terminated byte strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Character classification | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | isalnum | | | | | | isalpha | | | | | | islower | | | | | | isupper | | | | | | isdigit | | | | | | isxdigit | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isblank(C++11) | | | | | | iscntrl | | | | | | isgraph | | | | | | isspace | | | | | | isprint | | | | | | ispunct | | | | | |
| Character manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tolower | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****toupper**** | | | | | |
| Conversions to numeric formats | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | atof | | | | | | atoiatolatoll(C++11) | | | | | | strtolstrtoll(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strtoulstrtoull(C++11) | | | | | | strtofstrtodstrtold(C++11)(C++11) | | | | | | strtoimaxstrtouimax(C++11)(C++11) | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcpy | | | | | | strncpy | | | | | | strxfrm | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcat | | | | | | strncat | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlen | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtok | | | | | |  | | | | | |
| Character array functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpy | | | | | | memmove | | | | | |  | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strerror | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cctype>` |  |  |
| int toupper( int ch ); |  |  |
|  |  |  |

Converts the given character to uppercase according to the character conversion rules defined by the currently installed C locale.

In the default "C" locale, the following lowercase letters `abcdefghijklmnopqrstuvwxyz` are replaced with respective uppercase letters `ABCDEFGHIJKLMNOPQRSTUVWXYZ`.

### Parameters

|  |  |  |
| --- | --- | --- |
| ch | - | character to be converted. If the value of ch is not representable as unsigned char and does not equal EOF, the behavior is undefined. |

### Return value

Converted character or ch if no uppercase version is defined by the current C locale.

### Notes

Like all other functions from <cctype>, the behavior of `std::toupper` is undefined if the argument's value is neither representable as unsigned char nor equal to EOF. To use these functions safely with plain chars (or signed chars), the argument should first be converted to unsigned char:

```
char my_toupper(char ch)
{
    return static_cast<char>(std::toupper(static_cast<unsigned char>(ch)));
}

```

Similarly, they should not be directly used with standard algorithms when the iterator's value type is char or signed char. Instead, convert the value to unsigned char first:

```
std::string str_toupper(std::string s)
{
    std::transform(s.begin(), s.end(), s.begin(),
                // static_cast<int(*)(int)>(std::toupper)         // wrong
                // [](int c){ return std::toupper(c); }           // wrong
                // [](char c){ return std::toupper(c); }          // wrong
                   [](unsigned char c){ return std::toupper(c); } // correct
                  );
    return s;
}

```

### Example

Run this code

```
#include <cctype>
#include <climits>
#include <clocale>
#include <iostream>
#include <ranges>
 
int main()
{
    for (auto bd{0}; unsigned char lc : std::views::iota(0, UCHAR_MAX))
        if (unsigned char uc = std::toupper(lc); uc != lc)
            std::cout << lc << uc << (13 == ++bd ? '\n' : ' ');
    std::cout << "\n\n";
 
    unsigned char c = '\xb8'; // the character ž in ISO-8859-15
                              // but ¸ (cedilla) in ISO-8859-1
 
    std::setlocale(LC_ALL, "en_US.iso88591");
    std::cout << std::hex << std::showbase;
    std::cout << "in iso8859-1, toupper('0xb8') gives " << std::toupper(c) << '\n';
    std::setlocale(LC_ALL, "en_US.iso885915");
    std::cout << "in iso8859-15, toupper('0xb8') gives " << std::toupper(c) << '\n';
}

```

Output:

```
aA bB cC dD eE fF gG hH iI jJ kK lL mM
nN oO pP qQ rR sS tT uU vV wW xX yY zZ
 
in iso8859-1, toupper('0xb8') gives 0xb8
in iso8859-15, toupper('0xb8') gives 0xb4

```

### See also

|  |  |
| --- | --- |
| tolower | converts a character to lowercase   (function) |
| toupper(std::locale) | converts a character to uppercase using the ctype facet of a locale   (function template) |
| towupper | converts a wide character to uppercase   (function) |
| C documentation for toupper | |

### External links

|  |  |
| --- | --- |
| 1. | ISO/IEC 8859-1. From Wikipedia. |
| 2. | ISO/IEC 8859-15. From Wikipedia. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/byte/toupper&oldid=178559>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 December 2024, at 13:19.