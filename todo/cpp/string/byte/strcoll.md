# std::strcoll

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | tolower | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | toupper | | | | | |
| Conversions to numeric formats | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | atof | | | | | | atoiatolatoll(C++11) | | | | | | strtolstrtoll(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strtoulstrtoull(C++11) | | | | | | strtofstrtodstrtold(C++11)(C++11) | | | | | | strtoimaxstrtouimax(C++11)(C++11) | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcpy | | | | | | strncpy | | | | | | strxfrm | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcat | | | | | | strncat | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlen | | | | | | strcmp | | | | | | strncmp | | | | | | ****strcoll**** | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtok | | | | | |  | | | | | |
| Character array functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpy | | | | | | memmove | | | | | |  | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strerror | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstring>` |  |  |
| int strcoll( const char\* lhs, const char\* rhs ); |  |  |
|  |  |  |

Compares two null-terminated byte strings according to the current locale as defined by the LC_COLLATE category.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | pointers to the null-terminated byte strings to compare |

### Return value

- Negative value if lhs is **less than** (precedes) rhs.
- ​0​ if lhs is **equal to** rhs.
- Positive value if lhs is **greater than** (follows) rhs.

### Notes

Collation order is the dictionary order: the position of the letter in the national alphabet (its **equivalence class**) has higher priority than its case or variant. Within an equivalence class, lowercase characters collate before their uppercase equivalents and locale-specific order may apply to the characters with diacritics. In some locales, groups of characters compare as single **collation units**. For example, "ch" in Czech follows "h" and precedes "i", and "dzs" in Hungarian follows "dz" and precedes "g".

### Example

Run this code

```
#include <clocale>
#include <cstring>
#include <iostream>
 
int main()
{
    std::setlocale(LC_COLLATE, "cs_CZ.utf8");
    // Alternatively, ISO-8859-2 (a.k.a. Latin-2)
    // may also work on some OS:
    // std::setlocale(LC_COLLATE, "cs_CZ.iso88592");
 
    const char* s1 = "hrnec";
    const char* s2 = "chrt";
 
    std::cout << "In the Czech locale: ";
    if (std::strcoll(s1, s2) < 0)
        std::cout << s1 << " before " << s2 << '\n';
    else
        std::cout << s2 << " before " << s1 << '\n';
 
    std::cout << "In lexicographical comparison: ";
    if (std::strcmp(s1, s2) < 0)
        std::cout << s1 << " before " << s2 << '\n';
    else
        std::cout << s2 << " before " << s1 << '\n';
}

```

Output:

```
In the Czech locale: hrnec before chrt
In lexicographical comparison: chrt before hrnec

```

### See also

|  |  |
| --- | --- |
| wcscoll | compares two wide strings in accordance to the current locale   (function) |
| do_compare[virtual] | compares two strings using this facet's collation rules   (virtual protected member function of `std::collate<CharT>`) |
| strxfrm | transform a string so that `strcmp` would produce the same result as `strcoll`   (function) |
| C documentation for strcoll | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/byte/strcoll&oldid=160647>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 October 2023, at 11:48.