# operator==,!=,<,<=,>,>=,<=>(std::sub_match)

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
| sub_match::compare | | | | |
| sub_match::swap | | | | |
| Non-member functions | | | | |
| ****operator==operator!=operator<<operator<=operator>operator>=operator<=>****(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| operator<< | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<regex>` |  |  |
| Direct comparison |  |  |
| template< class BidirIt >  bool operator== ( const std::sub_match<BidirIt>& lhs, const std::sub_match<BidirIt>& rhs ); | (1) | (since C++11) |
| template< class BidirIt >  bool operator!= ( const std::sub_match<BidirIt>& lhs, const std::sub_match<BidirIt>& rhs ); | (2) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator<  ( const std::sub_match<BidirIt>& lhs, const std::sub_match<BidirIt>& rhs ); | (3) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator<= ( const std::sub_match<BidirIt>& lhs, const std::sub_match<BidirIt>& rhs ); | (4) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator>  ( const std::sub_match<BidirIt>& lhs, const std::sub_match<BidirIt>& rhs ); | (5) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator>= ( const std::sub_match<BidirIt>& lhs, const std::sub_match<BidirIt>& rhs ); | (6) | (since C++11)  (until C++20) |
| template< class BidirIt >  auto operator<=>( const std::sub_match<BidirIt>& lhs, const std::sub_match<BidirIt>& rhs ); | (7) | (since C++20) |
| Comparing with a std::basic_string |  |  |
| template< class BidirIt, class Traits, class Alloc >  bool operator== ( const std::sub_match<BidirIt>& lhs,                    const std::basic_string</\*value-type-of\*/<BidirIt>,                                           Traits, Alloc>& str ); | (8) | (since C++11) |
| template< class BidirIt, class Traits, class Alloc >  bool operator!= ( const std::sub_match<BidirIt>& lhs,                    const std::basic_string</\*value-type-of\*/<BidirIt>,                                           Traits, Alloc>& str ); | (9) | (since C++11)  (until C++20) |
| template< class BidirIt, class Traits, class Alloc >  bool operator<  ( const std::sub_match<BidirIt>& lhs,                    const std::basic_string</\*value-type-of\*/<BidirIt>,                                           Traits, Alloc>& str ); | (10) | (since C++11)  (until C++20) |
| template< class BidirIt, class Traits, class Alloc >  bool operator<= ( const std::sub_match<BidirIt>& lhs,                    const std::basic_string</\*value-type-of\*/<BidirIt>,                                           Traits, Alloc>& str ); | (11) | (since C++11)  (until C++20) |
| template< class BidirIt, class Traits, class Alloc >  bool operator>  ( const std::sub_match<BidirIt>& lhs,                    const std::basic_string</\*value-type-of\*/<BidirIt>,                                           Traits, Alloc>& str ); | (12) | (since C++11)  (until C++20) |
| template< class BidirIt, class Traits, class Alloc >  bool operator>= ( const std::sub_match<BidirIt>& lhs,                    const std::basic_string</\*value-type-of\*/<BidirIt>,                                           Traits, Alloc>& str ); | (13) | (since C++11)  (until C++20) |
| template< class BidirIt, class Traits, class Alloc >  auto operator<=>( const std::sub_match<BidirIt>& lhs,                    const std::basic_string</\*value-type-of\*/<BidirIt>,                                           Traits, Alloc>& str ); | (14) | (since C++20) |
| template< class BidirIt, class Traits, class Alloc >  bool operator== ( const std::basic_string</\*value-type-of\*/<BidirIt>,                                            Traits, Alloc>& str, const std::sub_match<BidirIt>& rhs ); | (15) | (since C++11)  (until C++20) |
| template< class BidirIt, class Traits, class Alloc >  bool operator!= ( const std::basic_string</\*value-type-of\*/<BidirIt>,                                            Traits, Alloc>& str, const std::sub_match<BidirIt>& rhs ); | (16) | (since C++11)  (until C++20) |
| template< class BidirIt, class Traits, class Alloc >  bool operator<  ( const std::basic_string</\*value-type-of\*/<BidirIt>,                                            Traits, Alloc>& str, const std::sub_match<BidirIt>& rhs ); | (17) | (since C++11)  (until C++20) |
| template< class BidirIt, class Traits, class Alloc >  bool operator<= ( const std::basic_string</\*value-type-of\*/<BidirIt>,                                            Traits, Alloc>& str, const std::sub_match<BidirIt>& rhs ); | (18) | (since C++11)  (until C++20) |
| template< class BidirIt, class Traits, class Alloc >  bool operator>  ( const std::basic_string</\*value-type-of\*/<BidirIt>,                                            Traits, Alloc>& str, const std::sub_match<BidirIt>& rhs ); | (19) | (since C++11)  (until C++20) |
| template< class BidirIt, class Traits, class Alloc >  bool operator>= ( const std::basic_string</\*value-type-of\*/<BidirIt>,                                            Traits, Alloc>& str, const std::sub_match<BidirIt>& rhs ); | (20) | (since C++11)  (until C++20) |
| Comparing with a C-style string |  |  |
| template< class BidirIt >  bool operator== ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>\* s ); | (21) | (since C++11) |
| template< class BidirIt >  bool operator!= ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>\* s ); | (22) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator<  ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>\* s ); | (23) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator<= ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>\* s ); | (24) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator>  ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>\* s ); | (25) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator>= ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>\* s ); | (26) | (since C++11)  (until C++20) |
| template< class BidirIt >  auto operator<=>( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>\* s ); | (27) | (since C++20) |
| template< class BidirIt >  bool operator== ( const /\*value-type-of\*/<BidirIt>\* s, const std::sub_match<BidirIt>& rhs ); | (28) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator!= ( const /\*value-type-of\*/<BidirIt>\* s, const std::sub_match<BidirIt>& rhs ); | (29) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator<  ( const /\*value-type-of\*/<BidirIt>\* s, const std::sub_match<BidirIt>& rhs ); | (30) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator<= ( const /\*value-type-of\*/<BidirIt>\* s, const std::sub_match<BidirIt>& rhs ); | (31) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator>  ( const /\*value-type-of\*/<BidirIt>\* s, const std::sub_match<BidirIt>& rhs ); | (32) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator>= ( const /\*value-type-of\*/<BidirIt>\* s, const std::sub_match<BidirIt>& rhs ); | (33) | (since C++11)  (until C++20) |
| Comparing with a single character |  |  |
| template< class BidirIt >  bool operator== ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>& ch ); | (34) | (since C++11) |
| template< class BidirIt >  bool operator!= ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>& ch ); | (35) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator<  ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>& ch ); | (36) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator<= ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>& ch ); | (37) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator>  ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>& ch ); | (38) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator>= ( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>& ch ); | (39) | (since C++11)  (until C++20) |
| template< class BidirIt >  auto operator<=>( const std::sub_match<BidirIt>& lhs, const /\*value-type-of\*/<BidirIt>& ch ); | (40) | (since C++20) |
| template< class BidirIt >  bool operator== ( const /\*value-type-of\*/<BidirIt>& ch, const std::sub_match<BidirIt>& rhs ); | (41) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator!= ( const /\*value-type-of\*/<BidirIt>& ch, const std::sub_match<BidirIt>& rhs ); | (42) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator<  ( const /\*value-type-of\*/<BidirIt>& ch, const std::sub_match<BidirIt>& rhs ); | (43) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator<= ( const /\*value-type-of\*/<BidirIt>& ch, const std::sub_match<BidirIt>& rhs ); | (44) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator>  ( const /\*value-type-of\*/<BidirIt>& ch, const std::sub_match<BidirIt>& rhs ); | (45) | (since C++11)  (until C++20) |
| template< class BidirIt >  bool operator>= ( const /\*value-type-of\*/<BidirIt>& ch, const std::sub_match<BidirIt>& rhs ); | (46) | (since C++11)  (until C++20) |
| Helper type aliases |  |  |
| template< class BidirIt >  using /\*value-type-of\*/ = typename std::iterator_traits<BidirIt>::value_type; | (47) | (exposition only\*) |
| template< class BidirIt >  using /\*cat-type-of\*/ =      std::compare_three_way_result_t <std::basic_string</\*value-type-of\*/<BidirIt>>>; | (48) | (since C++20)  (exposition only\*) |
|  |  |  |

Compares a `sub_match` to another `sub_match`, a std::string, a C-style string or a single character.

1-7) Compares two `sub_match` directly.8-20) Compares a `sub_match` with a std::basic_string.21-33) Compares a `sub_match` with a C-style string.34-46) Compares a `sub_match` with a single character.

|  |  |
| --- | --- |
| The `<`, `<=`, `>`, `>=`, and `!=` operators are synthesized from operator<=> and operator== respectively. | (since C++20) |

47) `value-type-of` ﻿<BidirIt> is the value type of `BidirIt`.48) `cat-type-of` ﻿<BidirIt> is the result type of three-way comparison of std::sub_match<BidirIt>.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | a `sub_match` to compare |
| str | - | a std::basic_string to compare |
| s | - | a pointer to a C-style string to compare |
| ch | - | a character to compare |

### Return value

Let target be the following values:

1-7) rhs8-20) typename std::sub_match<BidirIt>::string_type(str.data(), str.size())21-33) s34-46) typename std::sub_match<BidirIt>::string_type(1, ch)

The return values are defined as follows:

| Operator | Return value | |
| --- | --- | --- |
| Overloads (1-14,21-27,34-40) (overloads with parameter lhs) | Overloads (15-20,28-33,41-46)       (overloads without parameter lhs) |
| `==` | lhs.compare(target) == 0 | rhs.compare(target) == 0 |
| `!=` | lhs.compare(target) != 0 | rhs.compare(target) != 0 |
| `<` | lhs.compare(target) < 0 | rhs.compare(target) > 0 |
| `<=` | lhs.compare(target) <= 0 | rhs.compare(target) >= 0 |
| `>` | lhs.compare(target) > 0 | rhs.compare(target) < 0 |
| `>=` | lhs.compare(target) >= 0 | rhs.compare(target) <= 0 |
| `<=>` | static_cast<`cat-type-of` ﻿<BidirIt>> (lhs.compare(target) <=> 0) | N/A |

### Notes

The return type of operator<=> is guaranteed to be a comparison category type. If `value-type-of` ﻿<BidirIt> is char, wchar_t, char8_t, char16_t, or char32_t, the return type of `operator<=>` is std::strong_ordering.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2217 | C++11 | for comparisons with std::string, the argument of `compare()` was str.c_str() | the argument is string_type(str.data(), str.size())) |

### See also

|  |  |
| --- | --- |
| compare | compares matched subsequence (if any)   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/regex/sub_match/operator_cmp&oldid=177695>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 November 2024, at 17:16.