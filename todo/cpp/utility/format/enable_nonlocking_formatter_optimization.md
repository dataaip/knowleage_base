# std::enable_nonlocking_formatter_optimization

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
| ****enable_nonlocking_formatter_optimization****(C++23) | | | | |
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
| template< class T >  constexpr bool enable_nonlocking_formatter_optimization = false; |  | (since C++23) |
|  |  |  |

This template can be used by implementations to enable efficient implementations of std::print and std::println.

If `std::enable_nonlocking_formatter_optimization<T>` is true, printing an argument of type `T` can be performed in a more efficient way (see std::print for details). `std::enable_nonlocking_formatter_optimization` specializations can be true in the following cases:

- `T` is one of the types where std::formatter<T, CharT> is a basic standard specialization or standard specialization for a library type (see below).
- A program may specialize this template for any cv-unqualified program-defined type `T`. Such specializations must be usable in constant expressions and have type const bool.

### Basic standard specializations

In the following list, `CharT` is either char or wchar_t, `ArithmeticT` is any cv-unqualified arithmetic type other than char, wchar_t, char8_t, char16_t, or char32_t:

|  |  |  |
| --- | --- | --- |
| Nonlocking flag for character formatters |  |  |
| template<>  constexpr bool enable_nonlocking_formatter_optimization<CharT> = true; | (1) |  |
| Nonlocking flag for string formatters |  |  |
| template<>  constexpr bool enable_nonlocking_formatter_optimization<CharT\*> = true; | (2) |  |
| template<>  constexpr bool enable_nonlocking_formatter_optimization<const CharT\*> = true; | (3) |  |
| template< std::size_t N >  constexpr bool enable_nonlocking_formatter_optimization<CharT[N]> = true; | (4) |  |
| template< class Traits, class Alloc >  constexpr bool enable_nonlocking_formatter_optimization <std::basic_string<CharT, Traits, Alloc>> = true; | (5) |  |
| template< class Traits >  constexpr bool enable_nonlocking_formatter_optimization <std::basic_string_view<CharT, Traits>> = true; | (6) |  |
| Nonlocking flag for arithmetic formatters |  |  |
| template<>  constexpr bool enable_nonlocking_formatter_optimization<ArithmeticT> = true; | (7) |  |
| Nonlocking flag for pointer formatters |  |  |
| template<>  constexpr bool enable_nonlocking_formatter_optimization<std::nullptr_t> = true; | (8) |  |
| template<>  constexpr bool enable_nonlocking_formatter_optimization<void\*> = true; | (9) |  |
| template<>  constexpr bool enable_nonlocking_formatter_optimization<const void\*> = true; | (10) |  |
|  |  |  |

### Standard specializations for library types

Specializations of `enable_nonlocking_formatter_optimization` for all specializations of the following standard templates are defined as true:

- std::chrono::zoned_time when its template parameter type `TimeZonePtr` is const std::chrono::time_zone\*

Specializations of `enable_nonlocking_formatter_optimization` for all specializations of the following standard templates are defined as conditionally true:

- std::pair
- std::tuple
- std::chrono::duration

Specialization of `enable_nonlocking_formatter_optimization` for all formattable range types are always defined as false for which the range format kind is not std::range_format::disabled.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_print` | `202403L` | (C++26) (DR23) | Formatted output with stream locking |
| `202406L` | (C++26) (DR23) | Enabling nonlocking formatter optimization for more formattable types |

### See also

|  |  |
| --- | --- |
| formatter(C++20) | defines formatting rules for a given type   (class template) |
| print(C++23) | prints to stdout or a file stream using formatted representation of the arguments   (function template) |
| println(C++23) | same as std::print except that each print is terminated by additional new line   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/enable_nonlocking_formatter_optimization&oldid=177396>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 October 2024, at 19:50.