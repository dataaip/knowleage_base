# std::char_traits<char>::eof, std::char_traits<wchar_t>::eof, std::char_traits<char8_t>::eof, std::char_traits<char16_t>::eof, std::char_traits<char32_t>::eof

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
| ****char_traits::eof**** | | | | |
| char_traits::not_eof | | | | |

|  |  |  |
| --- | --- | --- |
| static int_type eof(); |  | (constexpr since C++11) (noexcept since C++11) |
|  |  |  |

Returns a value not equivalent to any valid value of type `char_type`.

See CharTraits for the general requirements on character traits for `X::eof`.

### Parameters

(none)

### Return value

| `char_type` | eof() |
| --- | --- |
| char | EOF |
| wchar_t | WEOF |
| char8_t | an implementation-defined constant that cannot appear as a valid UTF-8 code unit |
| char16_t | an implementation-defined constant that cannot appear as a valid UTF-16 code unit |
| char32_t | an implementation-defined constant that cannot appear as a Unicode code point |

### Complexity

Constant.

### See also

|  |  |
| --- | --- |
| not_eof[static] | checks whether a character is **eof** value   (public static member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/char_traits/eof&oldid=171376>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 April 2024, at 15:40.