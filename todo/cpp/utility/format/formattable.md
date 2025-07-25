# std::formattable

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
| ****formattable****(C++23) | | | | |
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

|  |  |  |
| --- | --- | --- |
| Defined in header `<format>` |  |  |
| template< class T, class CharT >  concept formattable = /\* formattable_with \*/<    std::remove_reference_t<T>,    std::basic_format_context</\* fmt_iter_for \*/<CharT>, CharT> >; | (1) | (since C++23) |
| Helper templates |  |  |
| template< class CharT >  using /\* fmt_iter_for \*/ = /\* unspecified \*/; | (2) | (exposition only\*) |
| template< class T, class Context,   class Formatter =                typename Context::template                    formatter_type<std::remove_const_t<T>> >  concept /\* formattable_with \*/ =     std::semiregular<Formatter> &&    requires (Formatter& f, const Formatter& cf, T&& t, Context fc,               std::basic_format_parse_context<                  typename Context::char_type              > pc) {      { f.parse(pc) } -> std::same_as<typename decltype(pc)::iterator>;      { cf.format(t, fc) } -> std::same_as<typename Context::iterator>; }; | (3) | (exposition only\*) |
|  |  |  |

The concept `formattable` specifies that std::formatter<std::remove_cvref_t<T>, CharT> meets the requirements of BasicFormatter and Formatter (if std::remove_reference_t<T> is const-qualified).

The exposition-only alias template /\* fmt_iter_for \*/ yields an unspecified type that satisfies std::output_iterator<const CharT&>.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3925 | C++23 | the second template argument of std::basic_format_context was not provided | provided |

### See also

|  |  |
| --- | --- |
| formatter(C++20) | defines formatting rules for a given type   (class template) |
| BasicFormatter(C++20) | abstracts formatting operations for a given formatting argument type and character type (named requirement) |
| Formatter(C++20) | defines functions used by the formatting library (named requirement) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/formattable&oldid=162178>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 November 2023, at 18:02.