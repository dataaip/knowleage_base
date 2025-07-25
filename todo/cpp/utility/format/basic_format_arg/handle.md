# std::basic_format_arg<Context>::handle

From cppreference.com
< cpp‎ | utility‎ | format‎ | basic format arg
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
| ****basic_format_arg::handle****(C++20) | | | | |
| basic_format_argsformat_argswformat_args(C++20)(C++20)(C++20) | | | | |
| visit_format_arg(C++20) (deprecated in C++26) | | | | |
| make_format_argsmake_wformat_args(C++20)(C++20) | | | | |
| Format error | | | | |
| format_error(C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<format>` |  |  |
| template< class Context >  class basic_format_arg<Context>::handle; |  | (since C++20) |
|  |  |  |

A type-erased wrapper that allows formatting an object of a user-defined type.

`handle` objects are typically created by std::make_format_args and accessed through std::visit_format_arg or the `visit` member functions of std::basic_format_arg(since C++26).

### Data members

A typical implementation of `handle` is TriviallyCopyable and only stores two non-static data members:

- a const void\* pointer to the object to be formatted, and
- a void (\*)(std::basic_format_parse_context<Context::char_type>&, Context&, const void\*) function pointer to the function performing needed operations in the `format` member function (see below).

### Member functions

|  |  |
| --- | --- |
| format(C++20) | formats the referenced object with the given contexts   (public member function) |

## std::basic_format_arg<Context>::handle::format

|  |  |  |
| --- | --- | --- |
| void format( std::basic_format_parse_context<Context::char_type>& parse_ctx,               Context& format_ctx ) const; |  | (since C++20) |
|  |  |  |

Let

- `T` be the type of the formatting argument,
- `TD` be std::remove_const_t<T>,
- `TQ` be const TD if const TD satisfies **__formattable_with**<Context> or `TD` otherwise, and
- `ref` be a reference to the formatting argument.

Equivalent to:
typename Context::template formatter_type<TD> f;  
parse_ctx.advance_to(f.parse(parse_ctx));  
format_ctx.advance_to(f.format(const_cast<TQ&>(static_cast<const TD&>(ref)), format_ctx));

### Notes

A `handle` has reference semantics for the formatted argument and does not extend its lifetime. It is the programmer's responsibility to ensure that the argument outlives the `handle`. Usually, a `handle` is only used within formatting functions.

### See also

|  |  |
| --- | --- |
| basic_format_arg(C++20) | class template that provides access to a formatting argument for user-defined formatters   (class template) |
| make_format_argsmake_wformat_args(C++20)(C++20) | creates a type-erased object referencing all formatting arguments, convertible to `format_args`   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/basic_format_arg/handle&oldid=158164>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 September 2023, at 06:32.