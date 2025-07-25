# std::char_traits<char>::find, std::char_traits<wchar_t>::find, std::char_traits<char8_t>::find, std::char_traits<char16_t>::find, std::char_traits<char32_t>::find

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
| char_traits::length | | | | |
| ****char_traits::find**** | | | | |
| char_traits::to_char_type | | | | |
| char_traits::to_int_type | | | | |
| char_traits::eq_int_type | | | | |
| char_traits::eof | | | | |
| char_traits::not_eof | | | | |

|  |  |  |
| --- | --- | --- |
| static const char_type\*      find( const char_type\* ptr, std::size_t count, const char_type& ch ); |  | (constexpr since C++17) |
|  |  |  |

Searches for character ch within the first count characters of the sequence pointed to by ptr.

See CharTraits for the general requirements on character traits for `X::find`.

### Parameters

|  |  |  |
| --- | --- | --- |
| ptr | - | pointer to a character string to search |
| count | - | the number of characters to analyze |
| ch | - | the character to search for |

### Return value

A pointer to the first character in the range specified by ``ptr`,`ptr + count`)` that compares equal to ch, or a null pointer if not found.

### Complexity

Linear in count.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/char_traits/find&oldid=158862>"

##### Navigation

- [Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 September 2023, at 01:28.