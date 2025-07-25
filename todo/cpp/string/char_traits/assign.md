# std::char_traits<char>::assign, std::char_traits<wchar_t>::assign, std::char_traits<char8_t>::assign, std::char_traits<char16_t>::assign, std::char_traits<char32_t>::assign

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
| ****char_traits::assign**** | | | | |
| char_traits::eqchar_traits::lt | | | | |
| char_traits::move | | | | |
| char_traits::copy | | | | |
| char_traits::compare | | | | |
| char_traits::length | | | | |
| char_traits::find | | | | |
| char_traits::to_char_type | | | | |
| char_traits::to_int_type | | | | |
| char_traits::eq_int_type | | | | |
| char_traits::eof | | | | |
| char_traits::not_eof | | | | |

|  |  |  |
| --- | --- | --- |
| static void assign( char_type& c1, const char_type& c2 ); | (1) | (noexcept since C++11) (constexpr since C++17) |
| static char_type\* assign( char_type\* ptr, std::size_t count, char_type c2 ); | (2) | (constexpr since C++20) |
|  |  |  |

1) Assigns c2 to c1, behaves identically to c1 = c2.2) Assigns c2 to each character in count characters in the character sequence pointed to by ptr.

See CharTraits for the general requirements on character traits for `X::assign`.

### Parameters

|  |  |  |
| --- | --- | --- |
| c1 | - | character to assign to |
| c2 | - | character value to assign |
| ptr | - | pointer to a character sequence to assign to |
| count | - | the length of the character sequence |

### Return value

1) (none)2) ptr

### Complexity

1) Constant.2) Linear in count.
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/char_traits/assign&oldid=171370>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 April 2024, at 15:27.