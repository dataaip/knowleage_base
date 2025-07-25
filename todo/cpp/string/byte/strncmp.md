# std::strncmp

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlen | | | | | | strcmp | | | | | | ****strncmp**** | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtok | | | | | |  | | | | | |
| Character array functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpy | | | | | | memmove | | | | | |  | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strerror | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstring>` |  |  |
| int strncmp( const char\* lhs, const char\* rhs, std::size_t count ); |  |  |
|  |  |  |

Compares at most count characters of two possibly null-terminated arrays. The comparison is done lexicographically. Characters following the null character are not compared.

The sign of the result is the sign of the difference between the values of the first pair of characters (both interpreted as unsigned char) that differ in the arrays being compared.

The behavior is undefined when access occurs past the end of either array lhs or rhs. The behavior is undefined when either lhs or rhs is the null pointer.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | pointers to the possibly null-terminated arrays to compare |
| count | - | maximum number of characters to compare |

### Return value

Negative value if lhs appears before rhs in lexicographical order.

Zero if lhs and rhs compare equal, or if count is zero.

Positive value if lhs appears after rhs in lexicographical order.

### Notes

This function is not locale-sensitive, unlike std::strcoll and std::strxfrm.

### Example

Run this code

```
#include <cstring>
#include <iostream>
 
void demo(const char* lhs, const char* rhs, int sz)
{
    const int rc = std::strncmp(lhs, rhs, sz);
    if (rc < 0)
        std::cout << "First " << sz << " chars of ["
                  << lhs << "] precede [" << rhs << "]\n";
    else if (rc > 0)
        std::cout << "First " << sz << " chars of ["
                  << lhs << "] follow [" << rhs << "]\n";
    else
        std::cout << "First " << sz << " chars of ["
                  << lhs << "] equal [" << rhs << "]\n";
}
 
int main()
{
    demo("Hello, world!", "Hello, everybody!", 13);
    demo("Hello, everybody!", "Hello, world!", 13);
    demo("Hello, everybody!", "Hello, world!", 7);
    demo("Hello, everybody!" + 12, "Hello, somebody!" + 11, 5);
}

```

Output:

```
First 13 chars of [Hello, world!] follow [Hello, everybody!]
First 13 chars of [Hello, everybody!] precede [Hello, world!]
First 7 chars of [Hello, everybody!] equal [Hello, world!]
First 5 chars of [body!] equal [body!]

```

### See also

|  |  |
| --- | --- |
| strcmp | compares two strings   (function) |
| wcsncmp | compares a certain amount of characters from two wide strings   (function) |
| memcmp | compares two buffers   (function) |
| strcoll | compares two strings in accordance to the current locale   (function) |
| C documentation for strncmp | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/byte/strncmp&oldid=153458>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 June 2023, at 15:55.