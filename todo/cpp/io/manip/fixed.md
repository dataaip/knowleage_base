# std::fixed, std::scientific, std::hexfloat, std::defaultfloat

From cppreference.com
< cpp‎ | io‎ | manip
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

Input/output manipulators

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Floating-point formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showpointnoshowpoint | | | | | | setprecision | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****fixedscientifichexfloatdefaultfloat****(C++11)(C++11) | | | | | |
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

|  |  |  |
| --- | --- | --- |
| Defined in header `<ios>` |  |  |
| std::ios_base& fixed( std::ios_base& str ); | (1) |  |
| std::ios_base& scientific( std::ios_base& str ); | (2) |  |
| std::ios_base& hexfloat( std::ios_base& str ); | (3) | (since C++11) |
| std::ios_base& defaultfloat( std::ios_base& str ); | (4) | (since C++11) |
|  |  |  |

Modifies the default formatting for floating-point output.

1) Sets the `floatfield` of the stream str to `fixed` as if by calling str.setf(std::ios_base::fixed, std::ios_base::floatfield).2) Sets the `floatfield` of the stream str to `scientific` as if by calling str.setf(std::ios_base::scientific, std::ios_base::floatfield).3) Sets the `floatfield` of the stream str to `fixed` and `scientific` simultaneously as if by calling str.setf(std::ios_base::fixed | std::ios_base::scientific, std::ios_base::floatfield). This enables hexadecimal floating-point formatting.4) Sets the `floatfield` of the stream str to zero, as if by calling str.unsetf(std::ios_base::floatfield). This enables the default floating-point formatting, which is different from fixed and scientific.

This is an I/O manipulator, it may be called with an expression such as out << std::fixed for any `out` of type std::basic_ostream (or with an expression such as in >> std::scientific for any `in` of type std::basic_istream).

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | reference to I/O stream |

### Return value

str (reference to the stream after manipulation).

### Notes

Hexadecimal floating-point formatting ignores the stream precision specification, as required by the specification of std::num_put::do_put.

These manipulators do not affect floating-point parsing.

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <sstream>
 
enum class cap { title, middle, end };
 
void print(const char* text, double num, cap c)
{
    if (c == cap::title)
        std::cout <<
            "┌──────────┬────────────┬──────────────────────────┐\n"
            "│  number  │   iomanip  │      representation      │\n"
            "├──────────┼────────────┼──────────────────────────┤\n";
    std::cout << std::left
         << "│ " << std::setw(8) << text <<      " │ fixed      │ "
         << std::setw(24) << std::fixed  << num <<            " │\n"
         << "│ " << std::setw(8) << text <<      " │ scientific │ "
         << std::setw(24) << std::scientific << num <<        " │\n"
         << "│ " << std::setw(8) << text <<      " │ hexfloat   │ "
         << std::setw(24) << std::hexfloat << num <<          " │\n"
         << "│ " << std::setw(8) << text <<      " │ default    │ "
         << std::setw(24) << std::defaultfloat << num <<      " │\n";
    std::cout << (c != cap::end ?
            "├──────────┼────────────┼──────────────────────────┤\n" :
            "└──────────┴────────────┴──────────────────────────┘\n");
}
 
int main()
{
    print("0.0", 0.0, cap::title);
    print("0.01", 0.01, cap::middle);
    print("0.00001", 0.00001, cap::end);
 
    // Note; choose clang for correct output
    double f;
    std::istringstream("0x1.8p+0") >> f;
    std::cout << "Parsing 0x1.8p+0 gives " << f << '\n';
 
    std::istringstream("0x1P-1022") >> f;
    std::cout << "Parsing 0x1P-1022 gives " << f << '\n';
}

```

Output:

```
┌──────────┬────────────┬──────────────────────────┐
│  number  │   iomanip  │      representation      │
├──────────┼────────────┼──────────────────────────┤
│ 0.0      │ fixed      │ 0.000000                 │
│ 0.0      │ scientific │ 0.000000e+00             │
│ 0.0      │ hexfloat   │ 0x0p+0                   │
│ 0.0      │ default    │ 0                        │
├──────────┼────────────┼──────────────────────────┤
│ 0.01     │ fixed      │ 0.010000                 │
│ 0.01     │ scientific │ 1.000000e-02             │
│ 0.01     │ hexfloat   │ 0x1.47ae147ae147bp-7     │
│ 0.01     │ default    │ 0.01                     │
├──────────┼────────────┼──────────────────────────┤
│ 0.00001  │ fixed      │ 0.000010                 │
│ 0.00001  │ scientific │ 1.000000e-05             │
│ 0.00001  │ hexfloat   │ 0x1.4f8b588e368f1p-17    │
│ 0.00001  │ default    │ 1e-05                    │
└──────────┴────────────┴──────────────────────────┘
Parsing 0x1.8p+0 gives 1.5
Parsing 0x1P-1022 gives 2.22507e-308

```

### See also

|  |  |
| --- | --- |
| setprecision | changes floating-point precision   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/manip/fixed&oldid=159201>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 September 2023, at 10:08.