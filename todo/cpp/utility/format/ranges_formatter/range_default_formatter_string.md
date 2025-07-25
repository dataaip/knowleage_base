# std::**range-default-formatter**<std::range_format::string>, std::**range-default-formatter**<std::range_format::debug_string>

From cppreference.com
< cpp‎ | utility‎ | format‎ | ranges formatter
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
| formatter<**range**>(C++23) | | | | |
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

std::formatter<**range**>

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| **range-default-formatter** specializations | | | | |
| **range-default-formatter**<std::range_format::sequence> | | | | |
| **range-default-formatter**<std::range_format::map> | | | | |
| **range-default-formatter**<std::range_format::set> | | | | |
| ******range-default-formatter**<std::range_format::string> **range-default-formatter**<std::range_format::debug_string>**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<format>` |  |  |
| template< std::range_format K, ranges::input_range R, class CharT >      requires (K == std::range_format::string || K == std::range_format::debug_string) struct /\*range-default-formatter\*/<K, R, CharT>; |  | (since C++23)  (exposition only\*) |
|  |  |  |

The class template /\*range-default-formatter\*/ for range types is specialized for formatting range as a string or an escaped string if std::format_kind<R> is either std::range_format::string or std::range_format::debug_string.

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| `underlying_` (private) | the underlying formatter of type std::formatter<std::basic_string<CharT>, CharT> (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor)(implicitly declared) | constructs a `range-default-formatter`   (public member function) |
| parse | parses the format specifier as specified by **std-format-spec**   (public member function) |
| format | writes the formatted output as specified by **std-format-spec**   (public member function) |

## std::**range-default-formatter**<std::range_format::string>::parse std::**range-default-formatter**<std::range_format::debug_string>::parse

|  |  |  |
| --- | --- | --- |
| template< class ParseContext >  constexpr auto parse( ParseContext& ctx ) -> ParseContext::iterator; |  |  |
|  |  |  |

Equivalent to:

auto i = underlying_.parse(ctx);  
if constexpr (K == std::range_format::debug_string)  
    underlying_.set_debug_format();  
return i;

Returns an iterator past the end of the **std-format-spec**.

## std::**range-default-formatter**<std::range_format::string>::format std::**range-default-formatter**<std::range_format::debug_string>::format

|  |  |  |
| --- | --- | --- |
| template< class FormatContext >  auto format( /\* see below \*/& r, FormatContext& ctx ) const -> FormatContext::iterator; |  |  |
|  |  |  |

If ranges::input_range<const R> is true, the type of r is const R&. Otherwise, the type is R&.

Let s be a std::basic_string<CharT> as if by constructing s with std::basic_string<CharT>(std::from_range, r) such that ranges::equal(s, r) is true.

Equivalent to return underlying_.format(s, ctx);.

Returns an iterator past the end of the output range.

### See also

|  |  |
| --- | --- |
| formatter(C++20) | defines formatting rules for a given type   (class template) |
| range_formatter(C++23) | class template that helps implementing std::formatter specializations for range types   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/ranges_formatter/range_default_formatter_string&oldid=176186>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 September 2024, at 14:33.