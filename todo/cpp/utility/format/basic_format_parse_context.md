# std::basic_format_parse_context

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
| range_formatter(C++23) | | | | |
| enable_nonlocking_formatter_optimization(C++23) | | | | |
| ****basic_format_parse_contextformat_parse_contextwformat_parse_context****(C++20)(C++20)(C++20) | | | | |
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
| template< class CharT >  class basic_format_parse_context; |  | (since C++20) |
|  |  |  |

Provides access to the format string parsing state consisting of the format string range being parsed and the argument counter for automatic indexing.

A `std::basic_format_parse_context` instance is passed to Formatter when parsing the format specification.

A program that declares an explicit or partial specialization of `std::basic_format_parse_context` is ill-formed, no diagnostic required.

Several typedefs for common character types are provided:

|  |  |
| --- | --- |
| Defined in header `<format>` | |
| Type | Definition |
| `std::format_parse_context` | std::basic_format_parse_context<char> |
| `std::wformat_parse_context` | std::basic_format_parse_context<wchar_t> |

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `char_type` | `CharT` |
| `iterator` | std::basic_string_view<CharT>::const_iterator |
| `const_iterator` | std::basic_string_view<CharT>::const_iterator |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `std::basic_format_parse_context` instance from format string and argument count   (public member function) |
| operator=[deleted] | `std::basic_format_parse_context` is not copyable   (public member function) |
| begin | returns an iterator to the beginning of the format string range   (public member function) |
| end | returns an iterator to the end of the format string range   (public member function) |
| advance_to | advances the begin iterator to the given position   (public member function) |
| next_arg_id | enters automatic indexing mode, and returns the next argument index   (public member function) |
| check_arg_id | enters manual indexing mode, checks if the given argument index is in range   (public member function) |
| check_dynamic_spec(C++26) | checks if the type of the corresponding format argument with the given argument index is in the given type template arguments   (public member function) |
| check_dynamic_spec_integral(C++26) | checks if the type of the corresponding format argument with the given argument index is an integral type   (public member function) |
| check_dynamic_spec_string(C++26) | checks if the type of the corresponding format argument with the given argument index is a string type   (public member function) |

## std::basic_format_parse_context::basic_format_parse_context

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| constexpr explicit   basic_format_parse_context( std::basic_string_view<CharT> fmt, std::size_t num_args = 0 ) noexcept; |  | (until C++26) |
| constexpr explicit   basic_format_parse_context( std::basic_string_view<CharT> fmt ) noexcept; |  | (since C++26) |
|  |  |  |
| --- | --- | --- |
| basic_format_parse_context( const basic_format_parse_context& ) = delete; | (2) |  |
|  |  |  |

1) Constructs a `std::basic_format_parse_context` instance. Initializes the format string range to ``fmt.begin()`,`fmt.end()`)`, and the argument count to num_args(until C++26)​0​(since C++26).

|  |  |
| --- | --- |
| Any call to `next_arg_id`, `check_arg_id`, or `check_dynamic_spec` on an instance of `std::basic_format_parse_context` initialized using this constructor is not a core constant expression. | (since C++26) |

2) The copy constructor is deleted. `std::basic_format_parse_context` is not copyable.

## std::basic_format_parse_context::begin

|  |  |  |
| --- | --- | --- |
| constexpr const_iterator begin() const noexcept; |  |  |
|  |  |  |

Returns an iterator to the beginning of the format string range.

## std::basic_format_parse_context::end

|  |  |  |
| --- | --- | --- |
| constexpr const_iterator end() const noexcept; |  |  |
|  |  |  |

Returns an iterator to the end of the format string range.

## std::basic_format_parse_context::advance_to

|  |  |  |
| --- | --- | --- |
| constexpr void advance_to( const_iterator it ); |  |  |
|  |  |  |

Sets the beginning of the format string range to it. After a call to `advance_to()`, subsequent calls to `begin()` will return a copy of it.

The behavior is undefined if end() is not [reachable from it.

## std::basic_format_parse_context::next_arg_id

|  |  |  |
| --- | --- | --- |
| constexpr std::size_t next_arg_id(); |  |  |
|  |  |  |

Enters automatic argument indexing mode, and returns the next argument index, starting from 0.

If \*this has already entered manual argument indexing mode, throws std::format_error.

If the next argument index is larger than or equal to the num_args provided in the constructor, the call is not a core constant expression.

## std::basic_format_parse_context::check_arg_id

|  |  |  |
| --- | --- | --- |
| constexpr void check_arg_id( std::size_t id ); |  |  |
|  |  |  |

Enters manual argument indexing mode.

If \*this has already entered automatic argument indexing mode, throws std::format_error.

If id is larger than or equal to the num_args provided in the constructor, the call is not a core constant expression.

## std::basic_format_parse_context::check_dynamic_spec

|  |  |  |
| --- | --- | --- |
| template< class... Ts >  constexpr void check_dynamic_spec( std::size_t id ) noexcept; |  | (since C++26) |
|  |  |  |

If id is larger than or equal to the num_args provided in the constructor or the type of the corresponding format argument (after conversion to std::basic_format_arg) is not one of the types in Ts..., the call is not a core constant expression. A call to check_dynamic_spec has no effect at runtime.

The program is ill-formed unless sizeof...(Ts) >= 1, the types in Ts... are unique, and each type is one of bool, char_type, int, unsigned int, long long int, unsigned long long int, float, double, long double, const char_type\*, std::basic_string_view<char_type>, or const void\*.

## std::basic_format_parse_context::check_dynamic_spec_integral

|  |  |  |
| --- | --- | --- |
| constexpr void check_dynamic_spec_integral( std::size_t id ) noexcept; |  | (since C++26) |
|  |  |  |

Equivalent to call check_dynamic_spec<int, unsigned int, long long int, unsigned long long int>(id). A call to check_dynamic_spec_integral has no effect at runtime.

## std::basic_format_parse_context::check_dynamic_spec_string

|  |  |  |
| --- | --- | --- |
| constexpr void check_dynamic_spec_string( std::size_t id ) noexcept; |  | (since C++26) |
|  |  |  |

Equivalent to call check_dynamic_spec<const char_type\*, std::basic_string_view<char_type>>(id). A call to check_dynamic_spec_string has no effect at runtime.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3825 | C++20 | `check_arg_id` has a compile-time argument id check, but `next_arg_id` did not have | added |
| LWG 3975 | C++20 | user specialization of `basic_format_parse_context` was allowed | disallowed |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/basic_format_parse_context&oldid=178349>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 December 2024, at 03:38.