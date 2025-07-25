# std::regex_traits<CharT>::translate

From cppreference.com
< cpp‎ | regex‎ | regex traits
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

std::regex_traits

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| regex_traits::regex_traits | | | | |
| regex_traits::length | | | | |
| ****regex_traits::translate**** | | | | |
| regex_traits::translate_nocase | | | | |
| regex_traits::transform | | | | |
| regex_traits::transform_primary | | | | |
| regex_traits::lookup_collatename | | | | |
| regex_traits::lookup_classname | | | | |
| regex_traits::isctype | | | | |
| regex_traits::value | | | | |
| regex_traits::imbue | | | | |
| regex_traits::getloc | | | | |

|  |  |  |
| --- | --- | --- |
| CharT translate( CharT c ) const; |  |  |
|  |  |  |

Obtains the comparison key for the character c, such that all characters that are equivalent to this character in the imbued locale produce the same key.

When the regex library needs to match two characters `c1` and `c2` and the flag std::regex_constants::collate is true, it executes regex_traits<>::translate(c1) == regex_traits<>::translate(c2).

Standard library specializations of std::regex_traits return c unmodified.

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | character that needs to be examined for equivalence |

### Return value

The comparison key for c in the currently imbued locale.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/regex_traits/translate&oldid=161054>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 October 2023, at 09:20.