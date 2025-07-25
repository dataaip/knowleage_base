# std::format_to

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
| ****format_to****(C++20) | | | | |
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

|  |  |  |
| --- | --- | --- |
| Defined in header `<format>` |  |  |
| template< class OutputIt, class... Args >  OutputIt format_to( OutputIt out, std::format_string<Args...> fmt, Args&&... args ); | (1) | (since C++20) |
| template< class OutputIt, class... Args >  OutputIt format_to( OutputIt out, std::wformat_string<Args...> fmt, Args&&... args ); | (2) | (since C++20) |
| template< class OutputIt, class... Args >  OutputIt format_to( OutputIt out, const std::locale& loc, std::format_string<Args...> fmt, Args&&... args ); | (3) | (since C++20) |
| template< class OutputIt, class... Args >  OutputIt format_to( OutputIt out, const std::locale& loc, std::wformat_string<Args...> fmt, Args&&... args ); | (4) | (since C++20) |
|  |  |  |

Format args according to the format string fmt, and write the result to the output iterator out. If present, loc is used for locale-specific formatting.

Equivalent to:

1) return std::vformat_to(std::move(out), fmt.str, std::make_format_args(args...));2) return std::vformat_to(std::move(out), fmt.str, std::make_wformat_args(args...));3) return std::vformat_to(std::move(out), loc, fmt.str, std::make_format_args(args...));4) return std::vformat_to(std::move(out), loc, fmt.str, std::make_wformat_args(args...));.

Let `CharT` be char for overloads (1,3), wchar_t for overloads (2,4).

These overloads participate in overload resolution only if `OutputIt` satisfies the concept std::output_iterator<const CharT&>.

If any of the following conditions is satisfied, the behavior is undefined:

- `OutputIt` does not model std::output_iterator<const CharT&>.
- std::formatter<Ti, CharT> does not meet the BasicFormatter requirements (as required by std::make_format_args and std::make_wformat_args) for some `Ti` in `Args`.

### Parameters

|  |  |  |
| --- | --- | --- |
| out | - | iterator to the output buffer |
| fmt | - | an object that represents the format string. The format string consists of  - ordinary characters (except { and }), which are copied unchanged to the output, - escape sequences {{ and }}, which are replaced with { and } respectively in the output, and - replacement fields.   Each replacement field has the following format:   |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | |  | | | | | | | | | | | `{` arg-id (optional) `}` | (1) |  | |  | | | | | | | | | | | `{` arg-id (optional) `:` format-spec `}` | (2) |  | |  | | | | | | | | | |  1) replacement field without a format specification2) replacement field with a format specification  |  |  |  | | --- | --- | --- | | arg-id | - | specifies the index of the argument in `args` whose value is to be used for formatting; if it is omitted, the arguments are used in order. The arg-id ﻿s in a format string must all be present or all be omitted. Mixing manual and automatic indexing is an error. | | format-spec | - | the format specification defined by the std::formatter specialization for the corresponding argument. Cannot start with }. |      - For basic types and standard string types, the format specification is interpreted as standard format specification. - For chrono types, the format specification is interpreted as chrono format specification.  |  |  | | --- | --- | | - For range types, the format specification is interpreted as range format specification. - For std::pair and std::tuple, the format specification is interpreted as tuple format specification. - For std::thread::id and std::stacktrace_entry, see thread id format specification and stacktrace entry format specification. - For std::basic_stacktrace, no format specifier is allowed. | (since C++23) |  |  |  | | --- | --- | | - For std::filesystem::path, see path format specification. | (since C++26) |  - For other formattable types, the format specification is determined by user-defined `formatter` specializations. |
| args... | - | arguments to be formatted |
| loc | - | std::locale used for locale-specific formatting |

### Return value

Iterator past the end of the output range.

### Exceptions

Propagates any exception thrown by formatter or iterator operations.

### Notes

As of P2216R3, it is an error if the format string is not a constant expression. std::vformat_to or std::runtime_format(since C++26) can be used in this case.

### Example

Run this code

```
#include <format>
#include <iostream>
#include <iterator>
#include <string>
 
int main()
{
    std::string buffer;
 
    std::format_to
    (
        std::back_inserter(buffer), // < OutputIt
        "Hello, C++{}!\n",          // < fmt
        "20"                        // < arg
    );
    std::cout << buffer;
    buffer.clear();
 
    std::format_to
    (
        std::back_inserter(buffer), // < OutputIt
        "Hello, {0}::{1}!{2}",      // < fmt
        "std",                      // < arg {0}
        "format_to()",              // < arg {1}
        "\n",                       // < arg {2}
        "extra param(s)..."         // < unused
    );
    std::cout << buffer << std::flush;
 
    std::wstring wbuffer;
    std::format_to
    (
        std::back_inserter(wbuffer),// < OutputIt
        L"Hello, {2}::{1}!{0}",     // < fmt
        L"\n",                      // < arg {0}
        L"format_to()",             // < arg {1}
        L"std",                     // < arg {2}
        L"...is not..."             // < unused
        L"...an error!"             // < unused
    );
    std::wcout << wbuffer;
}

```

Output:

```
Hello, C++20!
Hello, std::format_to()!
Hello, std::format_to()!

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3539 | C++20 | out could not be a move-only iterator | it can be |
| P2216R3 | C++20 | throws std::format_error for invalid format string | results in compile-time error instead |
| P2418R2 | C++20 | objects that are neither const-usable nor copyable (such as generator-like objects) are not formattable | allow formatting these objects |
| P2508R1 | C++20 | there's no user-visible name for this facility | the name `basic_format_string` is exposed |

### See also

|  |  |
| --- | --- |
| format(C++20) | stores formatted representation of the arguments in a new string   (function template) |
| format_to_n(C++20) | writes out formatted representation of its arguments through an output iterator, not exceeding specified size   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/format/format_to&oldid=179715>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 January 2025, at 16:48.