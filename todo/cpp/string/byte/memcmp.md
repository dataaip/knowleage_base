# std::memcmp

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlen | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtok | | | | | |  | | | | | |
| Character array functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | ****memcmp**** | | | | | | memset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpy | | | | | | memmove | | | | | |  | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strerror | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstring>` |  |  |
| int memcmp( const void\* lhs, const void\* rhs, std::size_t count ); |  |  |
|  |  |  |

Reinterprets the objects pointed to by lhs and rhs as arrays of unsigned char and compares the first count bytes of these arrays. The comparison is done lexicographically.

The sign of the result is the sign of the difference between the values of the first pair of bytes (both interpreted as unsigned char) that differ in the objects being compared.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | pointers to the memory buffers to compare |
| count | - | number of bytes to examine |

### Return value

Negative value if the first differing byte (reinterpreted as unsigned char) in lhs is less than the corresponding byte in rhs.

​0​ if all count bytes of lhs and rhs are equal.

Positive value if the first differing byte in lhs is greater than the corresponding byte in rhs.

### Notes

This function reads object representations, not the object values, and is typically meaningful for only trivially-copyable objects that have no padding. For example, `memcmp()` between two objects of type std::string or std::vector will not compare their contents, `memcmp()` between two objects of type struct { char c; int n; } will compare the padding bytes whose values may differ when the values of c and n are the same, and even if there were no padding bytes, the `int` would be compared without taking into account endianness.

### Example

Run this code

```
#include <cstring>
#include <iostream>
 
void demo(const char* lhs, const char* rhs, std::size_t sz)
{
    std::cout << std::string(lhs, sz);
    const int rc = std::memcmp(lhs, rhs, sz);
    if (rc < 0)
        std::cout << " precedes ";
    else if (rc > 0)
        std::cout << " follows ";
    else
        std::cout << " compares equal to ";
    std::cout << std::string(rhs, sz) << " in lexicographical order\n";
}
 
int main()
{
    char a1[] = {'a', 'b', 'c'};
    char a2[sizeof a1] = {'a', 'b', 'd'};
 
    demo(a1, a2, sizeof a1);
    demo(a2, a1, sizeof a1);
    demo(a1, a1, sizeof a1);
}

```

Output:

```
abc precedes abd in lexicographical order
abd follows abc in lexicographical order
abc compares equal to abc in lexicographical order

```

### See also

|  |  |
| --- | --- |
| strcmp | compares two strings   (function) |
| strncmp | compares a certain number of characters from two strings   (function) |
| C documentation for memcmp | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/byte/memcmp&oldid=154666>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 July 2023, at 03:19.