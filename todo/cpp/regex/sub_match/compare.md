# std::sub_match<BidirIt>::compare

From cppreference.com
< cpp‎ | regex‎ | sub match
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

Regular expressions library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| basic_regex(C++11) | | | | |
| sub_match(C++11) | | | | |
| match_results(C++11) | | | | |
| Algorithms | | | | |
| regex_match(C++11) | | | | |
| regex_search(C++11) | | | | |
| regex_replace(C++11) | | | | |
| Iterators | | | | |
| regex_iterator(C++11) | | | | |
| regex_token_iterator(C++11) | | | | |
| Exceptions | | | | |
| regex_error(C++11) | | | | |
| Traits | | | | |
| regex_traits(C++11) | | | | |
| Constants | | | | |
| syntax_option_type(C++11) | | | | |
| match_flag_type(C++11) | | | | |
| error_type(C++11) | | | | |
| Regex Grammar | | | | |
| Modified ECMAScript-262(C++11) | | | | |

std::sub_match

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| sub_match::sub_match | | | | |
| sub_match::length | | | | |
| sub_match::strsub_match::operator string_type | | | | |
| ****sub_match::compare**** | | | | |
| sub_match::swap | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| operator<< | | | | |

|  |  |  |
| --- | --- | --- |
| int compare( const sub_match& m ) const; | (1) | (since C++11) |
| int compare( const string_type& s ) const; | (2) | (since C++11) |
| int compare( const value_type\* c ) const; | (3) | (since C++11) |
|  |  |  |

1) Compares two `sub_match`es directly by comparing their underlying character sequences. Equivalent to str().compare(m.str()).2) Compares a `sub_match` with a std::basic_string. Equivalent to str().compare(s).3) Compares a `sub_match` with a null-terminated sequence of the underlying character type pointed to by s. Equivalent to str().compare(c).

### Parameters

|  |  |  |
| --- | --- | --- |
| m | - | a reference to another sub_match |
| s | - | a reference to a string to compare to |
| c | - | a pointer to a null-terminated character sequence of the underlying `value_type` to compare to |

### Return value

A value less than zero if this `sub_match` is **less** than the other character sequence, zero if the both underlying character sequences are equal, greater than zero if this `sub_match` is **greater** than the other character sequence.

### Notes

This function is infrequently used directly by application code. Instead, one of the non-member comparison operators is used.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| compare | compares two strings   (public member function of `std::basic_string<CharT,Traits,Allocator>`) |
| stroperator string_type | converts to the underlying string type   (public member function) |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(removed in C++20)(C++20) | compares a `sub_match` with another `sub_match`, a string, or a character   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/sub_match/compare&oldid=178362>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 December 2024, at 06:21.