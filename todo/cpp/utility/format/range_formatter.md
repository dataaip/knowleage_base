# std::range_formatter

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
| formatter<**range**>(C++23) | | | | |
| ****range_formatter****(C++23) | | | | |
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

|  |  |  |
| --- | --- | --- |
| Defined in header `<format>` |  |  |
| template< class T, class CharT = char >      requires std::same_as<std::remove_cvref_t<T>, T> && std::formattable<T, CharT> class range_formatter; |  | (since C++23) |
|  |  |  |

`std::range_formatter` is a helper class template for implementing range std::formatter specializations.

### Range format specification

The syntax of range-format-spec is:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| range-fill-and-align ﻿(optional) width ﻿(optional) `n`(optional) range-type ﻿(optional) range-underlying-spec ﻿(optional) |  |  |
|  | | | | | | | | | |

The range-fill-and-align is interpreted the same way as a fill-and-align except that the fill in range-fill-and-align is any character other than `{`, `}`, or `:`.

The width is described in standard format width specification.

The `n` option causes the range to be formatted without the opening and closing brackets.

```
assert(std::format("{}", views::iota(1, 5)) == "[1, 2, 3, 4]");
assert(std::format("{:n}", views::iota(1, 5)) == "1, 2, 3, 4");

```

The format-spec in a range-underlying-spec (its syntax is equivalent to `:` format-spec), if any, is interpreted by the range element formatter `std::formatter<T, CharT>`.

```
std::array ints{12, 10, 15, 14};
 
assert(std::format("{}", ints) == "[12, 10, 15, 14]");
assert(std::format("{::X}", ints) == "[C, A, F, E]");
assert(std::format("{:n:_^4}", ints) == "_12_, _10_, _15_, _14_");

```

The range-type changes the way a range is formatted, with certain options only valid with certain argument types.

The available range presentation types are:

- `m`: Indicates that the opening bracket should be "{", the closing bracket should be "}", the separator should be ", ", and each range element should be formatted as if `m` were specified for its tuple-type (in tuple-format-spec).

:   - If `m` is chosen as the range-type, the program is ill-formed unless `T` is either a specialization of:

    :   - std::pair, or
        - std::tuple such that std::tuple_size_v<T> == 2 is true.

```
std::array char_pairs
{
    std::pair{'A', 5}, std::pair{'B', 10}, std::pair{'C', 12}
};
 
assert(std::format("{}", char_pairs) == "[('A', 5), ('B', 10), ('C', 12)]");
assert(std::format("{:m}", char_pairs) == "{'A': 5, 'B': 10, 'C': 12}");

```

- `s`: Indicates that the range should be formatted as a string.
- `?s`: Indicates that the range should be formatted as an escaped string.

:   - If `s` or `?s` is chosen as the range-type, both `n` option and range-underlying-spec should not be included in the format specifier, and
    - the program is ill-formed unless `T` is `CharT`.

```
std::array star{'S', 'T', 'A', 'R'};
 
assert(std::format("{}", star) == "['S', 'T', 'A', 'R']");
assert(std::format("{:s}", star) == "STAR");
assert(std::format("{:?s}", star) == "\"STAR\"");

```

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| std::formatter<T, CharT> `underlying_` (private) | the underlying formatter for elements (exposition-only member object\*) |
| std::basic_string_view<CharT> `separator_` (private) | a string representing the separator of the range formatted result. The default separator is ", ". (exposition-only member object\*) |
| std::basic_string_view<CharT> `opening-bracket_` (private) | a string representing the opening bracket of the range formatted result. The default opening bracket is "". (exposition-only member object\*) |
| [std::basic_string_view<CharT> `closing-bracket_` (private) | a string representing the closing bracket of the range formatted result. The default closing bracket is "]". (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| set_separator | sets a specified separator for the range formatted result   (public member function) |
| set_brackets | sets a specified opening and closing brackets for the range formatted result   (public member function) |
| underlying | returns the underlying formatter   (public member function) |
| parse | parses the format specifier as specified by range-format-spec   (public member function) |
| format | writes the range formatted output as specified by range-format-spec   (public member function) |

## std::range_formatter::set_separator

|  |  |  |
| --- | --- | --- |
| constexpr void set_separator( std::basic_string_view<CharT> sep ) noexcept; |  |  |
|  |  |  |

Assigns sep to `separator_`.

## std::range_formatter::set_brackets

|  |  |  |
| --- | --- | --- |
| constexpr void set_brackets( std::basic_string_view<CharT> opening,                               std::basic_string_view<CharT> closing ) noexcept; |  |  |
|  |  |  |

Assigns opening and closing to `opening-bracket_` and `closing-bracket_`, respectively.

## std::range_formatter::underlying

|  |  |  |
| --- | --- | --- |
| constexpr std::formatter<T, CharT>& underlying(); | (1) |  |
| constexpr const std::formatter<T, CharT>& underlying() const; | (2) |  |
|  |  |  |

Returns `underlying_` (the underlying formatter).

## std::range_formatter::parse

|  |  |  |
| --- | --- | --- |
| template< class ParseContext >  constexpr auto parse( ParseContext& ctx ) -> ParseContext::iterator; |  |  |
|  |  |  |

Parses the format specifiers as a range-format-spec and stores the parsed specifiers in the current object.

Calls `underlying_`.parse(ctx) to parse format-spec in range-format-spec or, if the latter is not present, an empty format-spec.

If range-type or the `n` option is present, the values of `opening-bracket_`, `closing-bracket_`, and `separator_` are modified as required.

It calls `underlying_`.set_debug_format() if:

- the range-type is neither `s` nor `?s`,
- `underlying_`.set_debug_format() is a valid expression, and
- there is no range-underlying-spec.

Returns an iterator past the end of the range-format-spec.

## std::range_formatter::format

|  |  |  |
| --- | --- | --- |
| template< ranges::input_range R, class FormatContext >    requires std::formattable<ranges::range_reference_t<R>, CharT> &&             std::same_as<std::remove_cvref_t<ranges::range_reference_t<R>>, T> auto format( R&& r, FormatContext& ctx ) const -> FormatContext::iterator; |  |  |
|  |  |  |

If the range-type was either `s` or `?s`, it writes the formatted std::basic_string<CharT>(std::from_range, r) as a string or an escaped string, respectively, into ctx.out().

Otherwise, it writes the following into ctx.out() as specified by range-format-spec, in order:

- `opening-bracket_`,
- for each formattable element e of the range r:

:   - the result of writing e via `underlying_`, and
    - `separator_`, unless e is the last element of r, and

- `closing-bracket_`.

Returns an iterator past the end of the output range.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3892 | C++23 | the formatting of nested ranges was incorrect | corrected |

### See also

|  |  |
| --- | --- |
| formatter(C++20) | defines formatting rules for a given type   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/range_formatter&oldid=178385>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 December 2024, at 16:21.