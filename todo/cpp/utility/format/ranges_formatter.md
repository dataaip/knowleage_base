# std::formatter<**range**>

From cppreference.com
< cpp‎ | utility‎ | format
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

Formatting library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Standard format specification | | | | |
| Formatting functions | | | | |
| format(C++20) | | | | |
| format_to(C++20) | | | | |
| format_to_n(C++20) | | | | |
| formatted_size(C++20) | | | | |
| vformat(C++20) | | | | |
| vformat_to(C++20) | | | | |
| Format strings | | | | |
| basic_format_stringformat_stringwformat_string(C++20)(C++20)(C++20) | | | | |
| runtime_format(C++26) | | | | |
| Formatting concepts | | | | |
| formattable(C++23) | | | | |
| Formatter | | | | |
| formatter(C++20) | | | | |
| formatter<**pair-or-tuple**>(C++23) | | | | |
| ****formatter<**range**>****(C++23) | | | | |
| range_formatter(C++23) | | | | |
| enable_nonlocking_formatter_optimization(C++23) | | | | |
| basic_format_parse_contextformat_parse_contextwformat_parse_context(C++20)(C++20)(C++20) | | | | |
| basic_format_contextformat_contextwformat_context(C++20)(C++20)(C++20) | | | | |
| range_format(C++23) | | | | |
| format_kind(C++23) | | | | |
| Formatting arguments | | | | |
| basic_format_arg(C++20) | | | | |
| basic_format_arg::handle(C++20) | | | | |
| basic_format_argsformat_argswformat_args(C++20)(C++20)(C++20) | | | | |
| visit_format_arg(C++20) (deprecated in C++26) | | | | |
| make_format_argsmake_wformat_args(C++20)(C++20) | | | | |
| Format error | | | | |
| format_error(C++20) | | | | |

****std::formatter<**range**>****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| **range-default-formatter** specializations | | | | |
| **range-default-formatter**<std::range_format::sequence> | | | | |
| **range-default-formatter**<std::range_format::map> | | | | |
| **range-default-formatter**<std::range_format::set> | | | | |
| **range-default-formatter**<std::range_format::string> **range-default-formatter**<std::range_format::debug_string> | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<format>` |  |  |
| template< ranges::input_range R, class CharT >      requires (std::format_kind<R> != std::range_format::disabled) &&                std::formattable<ranges::range_reference_t<R>, CharT> struct formatter<R, CharT>; |  | (since C++23) |
| Helper templates |  |  |
| template< std::range_format K, ranges::input_range R, class CharT >  struct /\*range-default-formatter\*/; |  | (exposition only\*) |
|  |  |  |

The template specialization of std::formatter for the range types allows users to convert a range to its textual representation as a collection of elements or a string using formatting functions.

The specialization is derived from `range-default-formatter`<std::format_kind<R>, R, CharT>.

The specialization is enabled if R satisfies `input_range`, std::format_kind<R> is not std::range_format::disabled, and std::formattable<ranges::range_reference_t<R>, CharT> is true.

This specialization meets the Formatter requirements if const R models `input_range` and ranges::range_reference_t<const R> models std::formattable<CharT>. It always meets the BasicFormatter requirements.

### Format specification

The syntax of range-format-spec is:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| range-fill-and-align ﻿(optional) width ﻿(optional) `n`(optional) range-type ﻿(optional) range-underlying-spec ﻿(optional) |  |  |
|  | | | | | | | | | |

The syntax is fully described in range format specification.

For specializations of `std::formatter` where std::format_kind<R> is either std::range_format::string or std::range_format::debug_string, the format-spec is std-format-spec instead of range-format-spec (which uses std::formatter<std::basic_string<CharT>, CharT> as the underlying formatter).

### Specializations of `range-default-formatter`

|  |  |
| --- | --- |
| **range-default-formatter**<std::range_format::sequence>(C++23) | formatting utility for ranges in sequence form   (class template specialization) |
| **range-default-formatter**<std::range_format::map>(C++23) | formatting utility for ranges in map form   (class template specialization) |
| **range-default-formatter**<std::range_format::set>(C++23) | formatting utility for ranges in set form   (class template specialization) |
| **range-default-formatter**<std::range_format::string>**range-default-formatter**<std::range_format::debug_string>(C++23) | formatting utility for ranges in string or escaped string form   (class template specialization) |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: example |

### See also

|  |  |
| --- | --- |
| formatter(C++20) | defines formatting rules for a given type   (class template) |
| range_formatter(C++23) | class template that helps implementing std::formatter specializations for range types   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/ranges_formatter&oldid=176663>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 October 2024, at 13:26.