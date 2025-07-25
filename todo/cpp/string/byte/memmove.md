# std::memmove

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpy | | | | | | ****memmove**** | | | | | |  | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strerror | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstring>` |  |  |
| void\* memmove( void\* dest, const void\* src, std::size_t count ); |  |  |
|  |  |  |

Copies count characters from the object pointed to by src to the object pointed to by dest. Both objects are reinterpreted as arrays of unsigned char.

The objects may overlap: copying takes place as if the characters were copied to a temporary character array and then the characters were copied from the array to dest.

If either dest or src is an invalid or null pointer, the behavior is undefined, even if count is zero.

If the objects are potentially-overlapping or not TriviallyCopyable, the behavior of `memmove` is not specified and may be undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| dest | - | pointer to the memory location to copy to |
| src | - | pointer to the memory location to copy from |
| count | - | number of bytes to copy |

### Return value

dest

### Notes

`std::memmove` may be used to implicitly create objects in the destination buffer.

Despite being specified "as if" a temporary buffer is used, actual implementations of this function do not incur the overhead of double copying or extra memory. For small count, it may load up and write out registers; for larger blocks, a common approach (glibc and bsd libc) is to copy bytes forwards from the beginning of the buffer if the destination starts before the source, and backwards from the end otherwise, with a fall back to std::memcpy when there is no overlap at all.

Where strict aliasing prohibits examining the same memory as values of two different types, `std::memmove` may be used to convert the values.

### Example

Run this code

```
#include <cstring>
#include <iostream>
 
int main()
{
    char str[] = "1234567890";
    std::cout << str << '\n';
    std::memmove(str + 4, str + 3, 3); // copies from [4, 5, 6] to [5, 6, 7]
    std::cout << str << '\n';
}

```

Output:

```
1234567890
1234456890

```

### See also

|  |  |
| --- | --- |
| memcpy | copies one buffer to another   (function) |
| memset | fills a buffer with a character   (function) |
| wmemmove | copies a certain amount of wide characters between two, possibly overlapping, arrays   (function) |
| copycopy_if(C++11) | copies a range of elements to a new location   (function template) |
| copy_backward | copies a range of elements in backwards order   (function template) |
| is_trivially_copyable(C++11) | checks if a type is trivially copyable   (class template) |
| C documentation for memmove | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/byte/memmove&oldid=161336>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 25 October 2023, at 08:04.