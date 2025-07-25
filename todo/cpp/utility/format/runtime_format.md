# std::runtime_format

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
| ****runtime_format****(C++26) | | | | |
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

|  |  |  |
| --- | --- | --- |
| Defined in header `<format>` |  |  |
| /\*runtime-format-string\*/<char> runtime_format( std::string_view fmt ) noexcept; | (1) | (since C++26) |
| /\*runtime-format-string\*/<wchar_t> runtime_format( std::wstring_view fmt ) noexcept; | (2) | (since C++26) |
|  |  |  |

Returns an object that stores a runtime format string directly usable in user-oriented formatting functions and can be implicitly converted to `std::basic_format_string`.

### Parameters

|  |  |  |
| --- | --- | --- |
| fmt | - | a string view |

### Return value

An object holding the runtime format string of the exposition-only type:

## ****Class template**** `runtime-format-string` `<CharT>`

|  |  |  |
| --- | --- | --- |
| template< class CharT >  struct /\*runtime-format-string\*/; |  | (exposition only\*) |
|  |  |  |

#### Member objects

The returned object contains an exposition-only non-static data member `str` of type std::basic_string_view<CharT>.

#### Constructors and assignments

|  |  |  |
| --- | --- | --- |
| /\*runtime-format-string\*/( std::basic_string_view<CharT> s ) noexcept; | (1) |  |
| /\*runtime-format-string\*/( const /\*runtime-format-string\*/& ) = delete; | (2) |  |
| /\*runtime-format-string\*/& operator=( const /\*runtime-format-string\*/& ) = delete; | (3) |  |
|  |  |  |

1) Initializes `str` with `s`.2) Copy constructor is explicitly deleted. The type is neither copyable nor movable.3) The assignment is explicitly deleted.

### Notes

Since the return type of `runtime_format` is neither copyable nor movable, an attempt of passing runtime_fmt as glvalue inhibits the construction of std::basic_format_string which results in program ill-formed. To construct `std::basic_format_string` with `runtime_format`, the returned value of `runtime_format` is passed directly on `std::basic_format_string` as prvalue where copy elision is guaranteed.

```
auto runtime_fmt = std::runtime_format("{}");
 
auto s0 = std::format(runtime_fmt, 1); // error
auto s1 = std::format(std::move(runtime_fmt), 1); // still error
auto s2 = std::format(std::runtime_format("{}"), 1); // ok

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_format` | `202311L` | (C++26) | Runtime format strings |

### Example

Run this code

```
#include <format>
#include <print>
#include <string>
#include <string_view>
 
int main()
{
    std::print("Hello {}!\n", "world");
 
    std::string fmt;
    for (int i{}; i != 3; ++i)
    {
        fmt += "{} "; // constructs the formatting string
        std::print("{} : ", fmt);
        std::println(std::runtime_format(fmt), "alpha", 'Z', 3.14, "unused");
    }
}

```

Output:

```
Hello world!
{}  : alpha
{} {}  : alpha Z
{} {} {}  : alpha Z 3.14

```

### See also

|  |  |
| --- | --- |
| format(C++20) | stores formatted representation of the arguments in a new string   (function template) |
| vformat(C++20) | non-template variant of std::format using type-erased argument representation   (function) |
| basic_format_stringformat_stringwformat_string(C++20)(C++20)(C++20) | class template that performs compile-time format string checks at construction time   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/runtime_format&oldid=173449>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 July 2024, at 03:45.