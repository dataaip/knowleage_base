# std::char_traits<char>::length, std::char_traits<wchar_t>::length, std::char_traits<char8_t>::length, std::char_traits<char16_t>::length, std::char_traits<char32_t>::length

From cppreference.com
< cpp‎ | string‎ | char traits
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

Strings library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| basic_string | | | | |
| basic_string_view(C++17) | | | | |
| char_traits | | | | |

std::char_traits

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| char_traits::assign | | | | |
| char_traits::eqchar_traits::lt | | | | |
| char_traits::move | | | | |
| char_traits::copy | | | | |
| char_traits::compare | | | | |
| ****char_traits::length**** | | | | |
| char_traits::find | | | | |
| char_traits::to_char_type | | | | |
| char_traits::to_int_type | | | | |
| char_traits::eq_int_type | | | | |
| char_traits::eof | | | | |
| char_traits::not_eof | | | | |

|  |  |  |
| --- | --- | --- |
| static std::size_t length( const char_type\* s ); |  | (constexpr since C++17) |
|  |  |  |

Returns the length of the character sequence pointed to by s, that is, the position of the terminating null character (char_type()).

See CharTraits for the general requirements on character traits for `X::length`.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to a character sequence to return length of |

### Return value

The length of character sequence pointed to by s.

### Complexity

Linear.

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <string>
 
void print(const char* str)
{
    std::cout << std::quoted(str) << " has length = "
              << std::char_traits<char>::length(str) << '\n';
}
 
int main()
{
    print("foo");
 
    std::string s{"booo"};
    print(s.c_str());
}

```

Output:

```
"foo" has length = 3
"booo" has length = 4

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/char_traits/length&oldid=158861>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 September 2023, at 01:25.