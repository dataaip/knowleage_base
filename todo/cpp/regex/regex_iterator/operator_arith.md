# std::regex_iterator<BidirIt,CharT,Traits>::operator++, operator++(int)

From cppreference.com
< cpp‎ | regex‎ | regex iterator
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

std::regex_iterator

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| regex_iterator::regex_iterator | | | | |
| regex_iterator::operator= | | | | |
| Comparisons | | | | |
| regex_iterator::operator==regex_iterator::operator!=(until C++20) | | | | |
| Observers | | | | |
| regex_iterator::operator\*regex_iterator::operator-> | | | | |
| Modifiers | | | | |
| ****regex_iterator::operator++regex_iterator::operator++(int)**** | | | | |

|  |  |  |
| --- | --- | --- |
| regex_iterator& operator++(); |  | (since C++11) |
| regex_iterator operator++( int ); |  | (since C++11) |
|  |  |  |

Advances the iterator on the next match.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: explain better |

At first, a local variable of type `BidirIt` is constructed with the value of match[0].second.

If the iterator holds a zero-length match and start == end, \*this is set to end-of-sequence iterator and the function returns.

Otherwise, if the iterator holds a zero-length match the operator invokes the following:

regex_search(start, end, match, \*pregex,   
             flags | regex_constants::match_not_null |   
                     regex_constants::match_continuous);

If the call returns true, the function returns.

Otherwise the operator increments `start` and continues as if the most recent match was not a zero-length match.

If the most recent match was not a zero-length match, the operator sets `flags` to flags | regex_constants::match_prev_avail and invokes the following:

regex_search(start, end, match, \*pregex, flags);

If the call returns false, the iterator sets \*this to the end-of-sequence iterator, the function returns.

In all cases in which the call to regex_search returns true, match.prefix().first will be equal to the previous value of match[0].second and for each index i in the range `[`​0​`,`match.size()`)` for which match[i].matched is true, match[i].position() will return distance(begin, match[i].first).

This means that match[i].position() gives the offset from the beginning of the target sequence, which is often not the same as the offset from the sequence passed in the call to regex_search.

It is unspecified how the implementation makes these adjustments. This means that a compiler may call an implementation-specific search function, in which case a user-defined specialization of regex_search will not be called.

The behavior is undefined if the iterator is end-of-sequence iterator.

### Parameters

(none)

### Return value

1) \*this2) The previous value of the iterator.
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/regex_iterator/operator_arith&oldid=161037>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 October 2023, at 06:55.