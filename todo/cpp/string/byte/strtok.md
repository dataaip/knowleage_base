# std::strtok

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlen | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | ****strtok**** | | | | | |  | | | | | |
| Character array functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpy | | | | | | memmove | | | | | |  | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strerror | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstring>` |  |  |
| char\* strtok( char\* str, const char\* delim ); |  |  |
|  |  |  |

Finds the next token in a null-terminated byte string pointed to by str. The separator characters are identified by null-terminated byte string pointed to by delim.

This function is designed to be called multiple times to obtain successive tokens from the same string.

- If str is not a null pointer, the call is treated as the first call to `strtok` for this particular string. The function searches for the first character which is **not** contained in delim.

:   - If no such character was found, there are no tokens in str at all, and the function returns a null pointer.
    - If such character was found, it is the **beginning of the token**. The function then searches from that point on for the first character that **is** contained in delim.

    :   - If no such character was found, str has only one token, and the future calls to `strtok` will return a null pointer.
        - If such character was found, it is **replaced** by the null character '\0' and the pointer to the following character is stored in a static location for subsequent invocations.

    - The function then returns the pointer to the beginning of the token.

- If str is a null pointer, the call is treated as a subsequent call to `strtok`: the function continues from where it left in previous invocation. The behavior is the same as if the previously stored pointer is passed as str.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the null-terminated byte string to tokenize |
| delim | - | pointer to the null-terminated byte string identifying delimiters |

### Return value

Pointer to the beginning of the next token or a nullptr if there are no more tokens.

### Notes

This function is destructive: it writes the '\0' characters in the elements of the string str. In particular, a string literal cannot be used as the first argument of `std::strtok`.

Each call to this function modifies a static variable: is not thread safe.

Unlike most other tokenizers, the delimiters in `std::strtok` can be different for each subsequent token, and can even depend on the contents of the previous tokens.

### Possible implementation

|  |
| --- |
| ```text char* strtok(char* str, const char* delim) {     static char* buffer;       if (str != nullptr)         buffer = str;       buffer += std::strspn(buffer, delim);       if (*buffer == '\0')         return nullptr;       char* const tokenBegin = buffer;       buffer += std::strcspn(buffer, delim);       if (*buffer != '\0')         *buffer++ = '\0';       return tokenBegin; } ``` |

Actual C++ library implementations of this function delegate to the C library, where it may be implemented directly (as in MUSL libc), or in terms of its reentrant version (as in GNU libc).

### Example

Run this code

```
#include <cstring>
#include <iomanip>
#include <iostream>
 
int main() 
{
    char input[] = "one + two * (three - four)!";
    const char* delimiters = "! +- (*)";
    char* token = std::strtok(input, delimiters);
    while (token)
    {
        std::cout << std::quoted(token) << ' ';
        token = std::strtok(nullptr, delimiters);
    }
 
    std::cout << "\nContents of the input string now:\n\"";
    for (std::size_t n = 0; n < sizeof input; ++n)
    {
        if (const char c = input[n]; c != '\0')
            std::cout << c;
        else
            std::cout << "\\0";
    }
    std::cout << "\"\n";
}

```

Output:

```
"one" "two" "three" "four" 
Contents of the input string now:
"one\0+ two\0* (three\0- four\0!\0"

```

### See also

|  |  |
| --- | --- |
| strpbrk | finds the first location of any character from a set of separators   (function) |
| strcspn | returns the length of the maximum initial segment that consists of only the characters not found in another byte string   (function) |
| strspn | returns the length of the maximum initial segment that consists of only the characters found in another byte string   (function) |
| ranges::split_viewviews::split(C++20) | a `view` over the subranges obtained from splitting another `view` using a delimiter (class template) (range adaptor object) |
| C documentation for strtok | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/byte/strtok&oldid=161089>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 October 2023, at 23:00.