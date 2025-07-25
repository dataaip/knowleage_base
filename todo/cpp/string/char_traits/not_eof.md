# std::char_traits<char>::not_eof, std::char_traits<wchar_t>::not_eof, std::char_traits<char8_t>::not_eof, std::char_traits<char16_t>::not_eof, std::char_traits<char32_t>::not_eof

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
| char_traits::find | | | | |
| char_traits::to_char_type | | | | |
| char_traits::to_int_type | | | | |
| char_traits::eq_int_type | | | | |
| char_traits::eof | | | | |
| ****char_traits::not_eof**** | | | | |

|  |  |  |
| --- | --- | --- |
| static int_type not_eof( int_type e ); |  | (constexpr since C++11) (noexcept since C++11) |
|  |  |  |

Given e, produces a suitable value that is not equivalent to `eof`.

This function is typically used when a value other than `eof` needs to be returned, such as in implementations of std::basic_streambuf::overflow().

See CharTraits for the general requirements on character traits for `X::not_eof`.

### Parameters

|  |  |  |
| --- | --- | --- |
| e | - | value to analyze |

### Return value

e if e and `eof` value are not equivalent, or some other non-eof value otherwise.

### Complexity

Constant.

### See also

|  |  |
| --- | --- |
| eof[static] | returns an **eof** value   (public static member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/char_traits/not_eof&oldid=171377>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 April 2024, at 15:43.