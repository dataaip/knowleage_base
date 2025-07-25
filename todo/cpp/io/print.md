# std::print

From cppreference.com
< cpp‎ | io
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

Input/output library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| I/O manipulators | | | | |
| Print functions (C++23) | | | | |
| C-style I/O | | | | |
| Buffers | | | | |
| basic_streambuf | | | | |
| basic_filebuf | | | | |
| basic_stringbuf | | | | |
| basic_spanbuf(C++23) | | | | |
| strstreambuf(C++98/26\*) | | | | |
| basic_syncbuf(C++20) | | | | |
| Streams | | | | |
| Abstractions | | | | |
| ios_base | | | | |
| basic_ios | | | | |
| basic_istream | | | | |
| basic_ostream | | | | |
| basic_iostream | | | | |
| File I/O | | | | |
| basic_ifstream | | | | |
| basic_ofstream | | | | |
| basic_fstream | | | | |
| String I/O | | | | |
| basic_istringstream | | | | |
| basic_ostringstream | | | | |
| basic_stringstream | | | | |
| Array I/O | | | | |
| basic_ispanstream(C++23) | | | | |
| basic_ospanstream(C++23) | | | | |
| basic_spanstream(C++23) | | | | |
| istrstream(C++98/26\*) | | | | |
| ostrstream(C++98/26\*) | | | | |
| strstream(C++98/26\*) | | | | |
| Synchronized Output | | | | |
| basic_osyncstream(C++20) | | | | |
| Types | | | | |
| streamoff | | | | |
| streamsize | | | | |
| fpos | | | | |
| Error category interface | | | | |
| iostream_category(C++11) | | | | |
| io_errc(C++11) | | | | |

 Print functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Print functions | | | | |
| ****print****(C++23) | | | | |
| println(C++23) | | | | |
| vprint_unicodevprint_unicode_buffered(C++23)(C++23) | | | | |
| vprint_nonunicodevprint_nonunicode_buffered(C++23)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<print>` |  |  |
| template< class... Args >  void print( std::format_string<Args...> fmt, Args&&... args ); | (1) | (since C++23) |
| template< class... Args >  void print( std::FILE\* stream, std::format_string<Args...> fmt, Args&&... args ); | (2) | (since C++23) |
|  |  |  |

Format args according to the format string fmt, and print the result to an output stream.

1) Equivalent to std::print(stdout, fmt, std::forward<Args>(args)...).2) If the ordinary literal encoding is UTF-8, equivalent to (std::enable_nonlocking_formatter_optimization<std::remove_cvref_t<Args>> && ...)  
    ? std::vprint_unicode(stream, fmt.str, std::make_format_args(args...))  
    : std::vprint_unicode_buffered(stream, fmt.str, std::make_format_args(args...));. Otherwise, equivalent to (std::enable_nonlocking_formatter_optimization<std::remove_cvref_t<Args>> && ...)  
    ? std::vprint_nonunicode(stream, fmt.str, std::make_format_args(args...))  
    : std::vprint_nonunicode_buffered(stream, fmt.str, std::make_format_args(args...));.

If std::formatter<Ti, char> does not meet the BasicFormatter requirements for any `Ti` in `Args` (as required by std::make_format_args), the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| stream | - | output file stream to write to |
| fmt | - | an object that represents the format string. The format string consists of  - ordinary characters (except { and }), which are copied unchanged to the output, - escape sequences {{ and }}, which are replaced with { and } respectively in the output, and - replacement fields.   Each replacement field has the following format:   |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | |  | | | | | | | | | | | `{` arg-id (optional) `}` | (1) |  | |  | | | | | | | | | | | `{` arg-id (optional) `:` format-spec `}` | (2) |  | |  | | | | | | | | | |  1) replacement field without a format specification2) replacement field with a format specification  |  |  |  | | --- | --- | --- | | arg-id | - | specifies the index of the argument in `args` whose value is to be used for formatting; if it is omitted, the arguments are used in order. The arg-id ﻿s in a format string must all be present or all be omitted. Mixing manual and automatic indexing is an error. | | format-spec | - | the format specification defined by the std::formatter specialization for the corresponding argument. Cannot start with }. |      - For basic types and standard string types, the format specification is interpreted as standard format specification. - For chrono types, the format specification is interpreted as chrono format specification.  |  |  | | --- | --- | | - For range types, the format specification is interpreted as range format specification. - For std::pair and std::tuple, the format specification is interpreted as tuple format specification. - For std::thread::id and std::stacktrace_entry, see thread id format specification and stacktrace entry format specification. - For std::basic_stacktrace, no format specifier is allowed. | (since C++23) |  |  |  | | --- | --- | | - For std::filesystem::path, see path format specification. | (since C++26) |  - For other formattable types, the format specification is determined by user-defined `formatter` specializations. |
| args... | - | arguments to be formatted |

### Exceptions

- std::bad_alloc on allocation failure.
- std::system_error, if writing to the stream fails.
- Propagates any exception thrown by used formatters, e.g. std::format_error.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_print` | `202207L` | (C++23) | Formatted output |
| `202403L` | (C++26) (DR23) | Unbuffered formatted output |
| `202406L` | (C++26) (DR23) | Enabling unbuffered formatted output for more formattable types |
| `__cpp_lib_format` | `202207L` | (C++23) | Exposing std::basic_format_string |

### Example

Run this code

```
#include <cstdio>
#include <filesystem>
#include <print>
 
int main()
{
    std::print("{0} {2}{1}!\n", "Hello", 23, "C++");  // overload (1)
 
    const auto tmp {std::filesystem::temp_directory_path() / "test.txt"};
 
    if (std::FILE* stream{std::fopen(tmp.c_str(), "w")})
    {
        std::print(stream, "File: {}", tmp.string()); // overload (2)
        std::fclose(stream);
    }
}

```

Output:

```
Hello C++23!

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P3107R5 | C++23 | only buffered printing operations can be performed | can perform unbuffered printing operations |
| P3235R3 | C++23 | the names of the functions added by P3107R5 were misleading | changed the function names |

### See also

|  |  |
| --- | --- |
| println(C++23) | same as std::print except that each print is terminated by additional new line   (function template) |
| print(std::ostream)(C++23) | outputs formatted representation of the arguments   (function template) |
| format(C++20) | stores formatted representation of the arguments in a new string   (function template) |
| format_to(C++20) | writes out formatted representation of its arguments through an output iterator   (function template) |
| printffprintfsprintfsnprintf(C++11) | prints formatted output to stdout, a file stream or a buffer   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/print&oldid=180268>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 February 2025, at 23:20.