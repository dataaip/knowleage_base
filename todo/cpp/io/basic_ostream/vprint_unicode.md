# std::vprint_unicode(std::ostream)

From cppreference.com
< cpp‎ | io‎ | basic ostream
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

std::basic_ostream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Global objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | coutwcout | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cerrwcerr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clogwclog | | | | | |
| Member functions | | | | |
| basic_ostream::basic_ostream | | | | |
| basic_ostream::~basic_ostream | | | | |
| basic_ostream::operator=(C++11) | | | | |
| Formatted output | | | | |
| basic_ostream::operator<< | | | | |
| Unformatted output | | | | |
| basic_ostream::put | | | | |
| basic_ostream::write | | | | |
| Positioning | | | | |
| basic_ostream::tellp | | | | |
| basic_ostream::seekp | | | | |
| Miscellaneous | | | | |
| basic_ostream::flush | | | | |
| basic_ostream::swap(C++11) | | | | |
| Member classes | | | | |
| basic_ostream::sentry | | | | |
| Non-member functions | | | | |
| operator<<(std::basic_ostream) | | | | |
| print(std::ostream)(C++23) | | | | |
| println(std::ostream)(C++23) | | | | |
| ****vprint_unicode(std::ostream)****(C++23) | | | | |
| vprint_nonunicode(std::ostream)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ostream>` |  |  |
| void vprint_unicode( std::ostream& os,                       std::string_view fmt, std::format_args args ); |  | (since C++23) |
|  |  |  |

Format args according to the format string fmt, and writes the result to the output stream os. Behaves as FormattedOutputFunction of os, except that some details of error reporting differ.

Performs the following operations in order:

1. First, the function constructs and checks the sentry object.
2. Initializes an automatic variable as if by std::string out = std::vformat(os.getloc(), fmt, args);.
3. Writes out to os:

:   - If os refers to a terminal that is only capable of displaying Unicode via a native Unicode API, flushes os and writes out to the terminal using the native Unicode API.
    - Otherwise, inserts the character sequence ``out.begin()`,`out.end()`)` into os.

If writing to the terminal or inserting into os fails, calls os.setstate([std::ios_base::badbit).

If out contains invalid Unicode code units when the native Unicode API is used, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| os | - | output stream to insert data into |
| fmt | - | an object that represents the format string. The format string consists of  - ordinary characters (except { and }), which are copied unchanged to the output, - escape sequences {{ and }}, which are replaced with { and } respectively in the output, and - replacement fields.   Each replacement field has the following format:   |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | |  | | | | | | | | | | | `{` arg-id (optional) `}` | (1) |  | |  | | | | | | | | | | | `{` arg-id (optional) `:` format-spec `}` | (2) |  | |  | | | | | | | | | |  1) replacement field without a format specification2) replacement field with a format specification  |  |  |  | | --- | --- | --- | | arg-id | - | specifies the index of the argument in `args` whose value is to be used for formatting; if it is omitted, the arguments are used in order. The arg-id ﻿s in a format string must all be present or all be omitted. Mixing manual and automatic indexing is an error. | | format-spec | - | the format specification defined by the std::formatter specialization for the corresponding argument. Cannot start with }. |      - For basic types and standard string types, the format specification is interpreted as standard format specification. - For chrono types, the format specification is interpreted as chrono format specification.  |  |  | | --- | --- | | - For range types, the format specification is interpreted as range format specification. - For std::pair and std::tuple, the format specification is interpreted as tuple format specification. - For std::thread::id and std::stacktrace_entry, see thread id format specification and stacktrace entry format specification. - For std::basic_stacktrace, no format specifier is allowed. | (since C++23) |  |  |  | | --- | --- | | - For std::filesystem::path, see path format specification. | (since C++26) |  - For other formattable types, the format specification is determined by user-defined `formatter` specializations. |
| args | - | arguments to be formatted |

### Exceptions

- std::bad_alloc on allocation failure.
- Propagate any exception thrown by any formatter, e.g. std::format_error, without regard to the value of os.exceptions() and without turning on ios_base::badbit in the error state of os.
- May throw ios_base::failure caused by os.setstate(ios_base::badbit) which is called if an insertion into os fails.

### Notes

If invoking the native Unicode API requires transcoding, the invalid code units are substituted with `U+FFFD` REPLACEMENT CHARACTER (see "The Unicode Standard - Core Specification", Chapter 3.9).

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_print` | `202207L` | (C++23) | Formatted output |
| `__cpp_lib_format` | `202207L` | (C++23) | Exposing std::basic_format_string |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 4044 | C++23 | the native Unicode API was always used if the terminal referred to by os can display Unicode | only used if the terminal can only use the native Unicode API to display Unicode |

### See also

|  |  |
| --- | --- |
| vprint_nonunicode(std::ostream)(C++23) | outputs character data using type-erased argument representation   (function) |
| print(std::ostream)(C++23) | outputs formatted representation of the arguments   (function template) |
| operator<<(std::basic_ostream) | inserts character data or insert into rvalue stream   (function template) |
| vprint_unicodevprint_unicode_buffered(C++23) | prints to Unicode capable stdout or a file stream using type-erased argument representation   (function) |
| format(C++20) | stores formatted representation of the arguments in a new string   (function template) |

### External links

|  |  |
| --- | --- |
| 1. | Unicode |
| 2. | The Unicode Standard Version 14.0 - Core Specification |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ostream/vprint_unicode&oldid=180266>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 February 2025, at 22:27.