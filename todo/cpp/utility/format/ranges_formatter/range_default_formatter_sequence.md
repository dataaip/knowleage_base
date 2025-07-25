# std::**range-default-formatter**<std::range_format::sequence>

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
| ******range-default-formatter**<std::range_format::sequence>**** | | | | |
| **range-default-formatter**<std::range_format::map> | | | | |
| **range-default-formatter**<std::range_format::set> | | | | |
| **range-default-formatter**<std::range_format::string> **range-default-formatter**<std::range_format::debug_string> | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<format>` |  |  |
| template< ranges::input_range R, class CharT >  struct /\*range-default-formatter\*/<range_format::sequence, R, CharT>; |  | (since C++23)  (exposition only\*) |
|  |  |  |

The class template /\*range-default-formatter\*/ for range types is specialized for formatting range as a sequence of elements if std::format_kind<R> is std::range_format::sequence.

### Member types

|  |  |
| --- | --- |
| Member | Definition |
| `maybe-const-r` (private) | `fmt-maybe-const`<R, CharT> (exposition-only member type\*) |

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| `underlying_` (private) | the underlying formatter of type: std::range_formatter<std::remove_cvref_t< ranges::range_reference_t<`maybe-const-r`>>, CharT> (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor)(implicitly declared) | constructs a /\*range-default-formatter\*/   (public member function) |
| set_separator | sets a specified separator for the range formatted result   (public member function) |
| set_brackets | sets a specified opening and closing brackets for the range formatted result   (public member function) |
| parse | parses the format specifier as specified by range-format-spec   (public member function) |
| format | writes the range formatted output as specified by range-format-spec   (public member function) |

## std::**range-default-formatter**<std::range_format::sequence>::set_separator

|  |  |  |
| --- | --- | --- |
| constexpr void set_separator( std::basic_string_view<CharT> sep ) noexcept; |  |  |
|  |  |  |

Equivalent to a call to underlying_.set_separator(sep).

## std::**range-default-formatter**<std::range_format::sequence>::set_brackets

|  |  |  |
| --- | --- | --- |
| constexpr void set_brackets( std::basic_string_view<CharT> opening,                               std::basic_string_view<CharT> closing ) noexcept; |  |  |
|  |  |  |

Equivalent to a call to underlying_.set_brackets(opening, closing).

## std::**range-default-formatter**<std::range_format::sequence>::parse

|  |  |  |
| --- | --- | --- |
| template< class ParseContext >  constexpr auto parse( ParseContext& ctx ) -> ParseContext::iterator; |  |  |
|  |  |  |

Equivalent to return underlying_.parse(ctx);.

Returns an iterator past the end of the **range-format-spec**.

## std::**range-default-formatter**<std::range_format::sequence>::format

|  |  |  |
| --- | --- | --- |
| template< class FormatContext >  auto format( /\*maybe-const-r\*/& elems, FormatContext& ctx ) const -> FormatContext::iterator; |  |  |
|  |  |  |

Equivalent to return underlying_.format(elems, ctx);.

Returns an iterator past the end of the output range.

### See also

|  |  |
| --- | --- |
| formatter(C++20) | defines formatting rules for a given type   (class template) |
| range_formatter(C++23) | class template that helps implementing std::formatter specializations for range types   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/ranges_formatter/range_default_formatter_sequence&oldid=176664>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 October 2024, at 13:31.