# std::match_results<BidirIt,Alloc>::length

From cppreference.com
< cpp‎ | regex‎ | match results
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

std::match_results

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| match_results::match_results | | | | |
| match_results::~match_results | | | | |
| match_results::operator= | | | | |
| match_results::get_allocator | | | | |
| State | | | | |
| match_results::ready | | | | |
| Element access | | | | |
| match_results::size | | | | |
| match_results::max_size | | | | |
| match_results::empty | | | | |
| ****match_results::length**** | | | | |
| match_results::position | | | | |
| match_results::str | | | | |
| [match_results::operator[]](operator_at.html "cpp/regex/match results/operator at") | | | | |
| match_results::prefix | | | | |
| match_results::suffix | | | | |
| Iterators | | | | |
| match_results::beginmatch_results::cbegin | | | | |
| match_results::endmatch_results::cend | | | | |
| Format | | | | |
| match_results::format | | | | |
| Modifiers | | | | |
| match_results::swap | | | | |
| Non-member functions | | | | |
| operator==operator!=(until C++20) | | | | |
| swap(std::match_results) | | | | |

|  |  |  |
| --- | --- | --- |
| difference_type length( size_type n = 0 ) const; |  | (since C++11) |
|  |  |  |

Returns the length of the specified sub-match.

If n == 0, the length of the entire matched expression is returned.

If n > 0 && n < size(), the length of nth sub-match is returned.

if n >= size(), a length of the unmatched match is returned.

The call is equivalent to (\*this)[n].length().

`ready()` must be true. Otherwise, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| n | - | integral number specifying which match to examine |

### Return value

The length of the specified match or sub-match.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| [operator[]](operator_at.html "cpp/regex/match results/operator at") | returns specified sub-match   (public member function) |
| length | returns the length of the match (if any)   (public member function of `std::sub_match<BidirIt>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/match_results/length&oldid=179529>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 January 2025, at 14:11.