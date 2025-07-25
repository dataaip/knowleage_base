# Input/output manipulators

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
| ****I/O manipulators**** | | | | |
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

****Input/output manipulators****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Floating-point formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showpointnoshowpoint | | | | | | setprecision | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fixedscientifichexfloatdefaultfloat(C++11)(C++11) | | | | | |
| Integer formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbase | | | | | | showbasenoshowbase | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | dechexoct | | | | | |
| Boolean formatting | | | | |
| boolalphanoboolalpha | | | | |
| Field width and fill control | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setfill | | | | | | setw | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | internalleftright | | | | | |
| Other formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showposnoshowpos | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uppercasenouppercase | | | | | |
| Whitespace processing | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ws | | | | | | ends | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | skipwsnoskipws | | | | | |
| Output flushing | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | flush | | | | | | endl | | | | | | flush_emit(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | unitbufnounitbuf | | | | | | emit_on_flushnoemit_on_flush(C++20)(C++20) | | | | | |
| Status flags manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | resetiosflags | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setiosflags | | | | | |
| Time and money I/O | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | get_money(C++11) | | | | | | get_time(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | put_money(C++11) | | | | | | put_time(C++11) | | | | | |
| Quoted manipulator | | | | |
| quoted(C++14) | | | | |

Manipulators are helper functions that make it possible to control input/output streams using operator<< or operator>>.

The manipulators that are invoked without arguments (e.g. std::cout << std::boolalpha; or std::cin >> std::hex;) are implemented as functions that take a reference to a stream as their only argument. The special overloads of basic_ostream::operator<< and basic_istream::operator>> accept pointers to these functions. These functions (or instantiations of function templates) are the only addressable functions in the standard library.(since C++20)

The manipulators that are invoked with arguments (e.g. std::cout << std::setw(10);) are implemented as functions returning objects of unspecified type. These manipulators define their own `operator<<` or `operator>>` which perform the requested manipulation.

|  |  |
| --- | --- |
| Defined in header `<ios>` | |
| boolalphanoboolalpha | switches between textual and numeric representation of booleans   (function) |
| showbasenoshowbase | controls whether prefix is used to indicate numeric base   (function) |
| showpointnoshowpoint | controls whether decimal point is always included in floating-point representation   (function) |
| showposnoshowpos | controls whether the `+` sign used with non-negative numbers   (function) |
| skipwsnoskipws | controls whether leading whitespace is skipped on input   (function) |
| uppercasenouppercase | controls whether uppercase characters are used with some output formats   (function) |
| unitbufnounitbuf | controls whether output is flushed after each operation   (function) |
| internalleftright | sets the placement of fill characters   (function) |
| dechexoct | changes the base used for integer I/O   (function) |
| fixedscientifichexfloatdefaultfloat(C++11)(C++11) | changes formatting used for floating-point I/O   (function) |
|  | |
| Defined in header `<istream>` | |
| ws | consumes whitespace   (function template) |
|  | |
| Defined in header `<ostream>` | |
| ends | outputs '\0'   (function template) |
| flush | flushes the output stream   (function template) |
| endl | outputs '\n' and flushes the output stream   (function template) |
| emit_on_flushnoemit_on_flush(C++20) | controls whether a stream's basic_syncbuf emits on flush   (function template) |
| flush_emit(C++20) | flushes a stream and emits the content if it is using a basic_syncbuf   (function template) |
|  | |
| Defined in header `<iomanip>` | |
| resetiosflags | clears the specified ios_base flags   (function) |
| setiosflags | sets the specified `ios_base` flags   (function) |
| setbase | changes the base used for integer I/O   (function) |
| setfill | changes the fill character   (function template) |
| setprecision | changes floating-point precision   (function) |
| setw | changes the width of the next input/output field   (function) |
| get_money(C++11) | parses a monetary value   (function template) |
| put_money(C++11) | formats and outputs a monetary value   (function template) |
| get_time(C++11) | parses a date/time value of specified format   (function template) |
| put_time(C++11) | formats and outputs a date/time value according to the specified format   (function template) |
| quoted(C++14) | inserts and extracts quoted strings with embedded spaces   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/manip&oldid=165311>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 December 2023, at 10:17.