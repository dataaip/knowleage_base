# std::basic_ostream<CharT,Traits>::seekp

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
| ****basic_ostream::seekp**** | | | | |
| Miscellaneous | | | | |
| basic_ostream::flush | | | | |
| basic_ostream::swap(C++11) | | | | |
| Member classes | | | | |
| basic_ostream::sentry | | | | |
| Non-member functions | | | | |
| operator<<(std::basic_ostream) | | | | |
| print(std::ostream)(C++23) | | | | |
| println(std::ostream)(C++23) | | | | |
| vprint_unicode(std::ostream)(C++23) | | | | |
| vprint_nonunicode(std::ostream)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_ostream& seekp( pos_type pos ); | (1) |  |
| basic_ostream& seekp( off_type off, std::ios_base::seekdir dir ); | (2) |  |
|  |  |  |

Sets the output position indicator of the current associated `streambuf` object.

|  |  |
| --- | --- |
| Behaves as UnformattedOutputFunction (except without actually performing output). After constructing and checking the sentry object, | (since C++11) |

1) if fail() != true, sets the output position indicator to absolute (relative to the beginning of the file) value pos by calling rdbuf()->pubseekpos(pos, std::ios_base::out). In case of failure, calls setstate(std::ios_base::failbit).2) if fail() != true, sets the output position indicator to offset off relative to dir by calling rdbuf()->pubseekoff(off, dir, std::ios_base::out). In case of failure, calls setstate(std::ios_base::failbit).

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | absolute position to set the output position indicator to |
| off | - | relative position (positive or negative) to set the output position indicator to |
| dir | - | defines base position to apply the relative offset to. It can be one of the following constants:  |  |  | | --- | --- | | Constant | Explanation | | beg | the beginning of a stream | | end | the ending of a stream | | cur | the current position of stream position indicator | |

### Return value

\*this

### Exceptions

1,2) May throw std::ios_base::failure in case of failure, if exceptions() & failbit != 0.

### Example

Run this code

```
#include <iostream>
#include <sstream>
 
int main()
{
    std::ostringstream os("hello, world");
    os.seekp(7);
    os << 'W';
    os.seekp(0, std::ios_base::end);
    os << '!';
    os.seekp(0);
    os << 'H';
    std::cout << os.str() << '\n';
}

```

Output:

```
Hello, World!

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 129 | C++98 | there was no way to indicate a failure | sets `failbit` on failure |
| LWG 136 | C++98 | `seekp` could set the input stream | only sets the output stream |
| LWG 537 | C++98 | 1. the type of pos was `pos_type&` 2. the type of off was `off_type&` | 1. corrected to `pos_type` 2. corrected to `off_type` |
| LWG 2341 | C++98 | the resolution of LWG issue 129 for overload (2) was removed | restored |

### See also

|  |  |
| --- | --- |
| tellp | returns the output position indicator   (public member function) |
| tellg | returns the input position indicator   (public member function of `std::basic_istream<CharT,Traits>`) |
| seekg | sets the input position indicator   (public member function of `std::basic_istream<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ostream/seekp&oldid=158551>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 September 2023, at 08:57.