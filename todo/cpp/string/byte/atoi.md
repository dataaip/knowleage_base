# std::atoi, std::atol, std::atoll

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | atof | | | | | | ****atoiatolatoll****(C++11) | | | | | | strtolstrtoll(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strtoulstrtoull(C++11) | | | | | | strtofstrtodstrtold(C++11)(C++11) | | | | | | strtoimaxstrtouimax(C++11)(C++11) | | | | | |
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
| Defined in header `<cstdlib>` |  |  |
| int       atoi( const char\* str ); | (1) |  |
| long      atol( const char\* str ); | (2) |  |
| long long atoll( const char\* str ); | (3) | (since C++11) |
|  |  |  |

Interprets an integer value in a byte string pointed to by str. The implied radix is always 10.

Discards any whitespace characters until the first non-whitespace character is found, then takes as many characters as possible to form a valid integer number representation and converts them to an integer value. The valid integer value consists of the following parts:

- (optional) plus or minus sign
- numeric digits

If the value of the result cannot be represented, i.e. the converted value falls out of range of the corresponding return type, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the null-terminated byte string to be interpreted |

### Return value

Integer value corresponding to the contents of str on success.

If no conversion can be performed, ​0​ is returned.

### Possible implementation

|  |
| --- |
| ```text template<typename T> T atoi_impl(const char* str) {     while (std::isspace(static_cast<unsigned char>(*str)))         ++str;       bool negative = false;       if (*str == '+')         ++str;     else if (*str == '-')     {         ++str;         negative = true;     }       T result = 0;     for (; std::isdigit(static_cast<unsigned char>(*str)); ++str)     {         int digit = *str - '0';         result *= 10;         result -= digit; // calculate in negatives to support INT_MIN, LONG_MIN,..     }       return negative ? result : -result; }   int atoi(const char* str) {     return atoi_impl<int>(str); }   long atol(const char* str) {     return atoi_impl<long>(str); }   long long atoll(const char* str) {     return atoi_impl<long long>(str); } ``` |

Actual C++ library implementations fall back to C library implementations of `atoi`, `atoil`, and `atoll`, which either implement it directly (as in MUSL libc) or delegate to strtol/strtoll (as in GNU libc).

### Example

Run this code

```
#include <cstdlib>
#include <iostream>
 
int main()
{
    const auto data =
    {
        "42",
        "0x2A", // treated as "0" and junk "x2A", not as hexadecimal
        "3.14159",
        "31337 with words",
        "words and 2",
        "-012345",
        "10000000000" // note: out of int32_t range
    };
 
    for (const char* s : data)
    {
        const int i{std::atoi(s)};
        std::cout << "std::atoi('" << s << "') is " << i << '\n';
        if (const long long ll{std::atoll(s)}; i != ll)
            std::cout << "std::atoll('" << s << "') is " << ll << '\n';
    }
}

```

Possible output:

```
std::atoi('42') is 42
std::atoi('0x2A') is 0
std::atoi('3.14159') is 3
std::atoi('31337 with words') is 31337
std::atoi('words and 2') is 0
std::atoi('-012345') is -12345
std::atoi('10000000000') is 1410065408
std::atoll('10000000000') is 10000000000

```

### See also

|  |  |
| --- | --- |
| stoistolstoll(C++11)(C++11)(C++11) | converts a string to a signed integer   (function) |
| stoulstoull(C++11)(C++11) | converts a string to an unsigned integer   (function) |
| strtolstrtoll(C++11) | converts a byte string to an integer value   (function) |
| strtoulstrtoull(C++11) | converts a byte string to an unsigned integer value   (function) |
| strtoimaxstrtoumax(C++11)(C++11) | converts a byte string to std::intmax_t or std::uintmax_t   (function) |
| from_chars(C++17) | converts a character sequence to an integer or floating-point value   (function) |
| C documentation for atoi, atol, atoll | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/byte/atoi&oldid=152810>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 June 2023, at 08:33.