# std::basic_ostream<CharT,Traits>::basic_ostream

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
| ****basic_ostream::basic_ostream**** | | | | |
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
| vprint_unicode(std::ostream)(C++23) | | | | |
| vprint_nonunicode(std::ostream)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| explicit basic_ostream( std::basic_streambuf<CharT, Traits>\* sb ); | (1) |  |
| protected:  basic_ostream( const basic_ostream& rhs ) = delete; | (2) | (since C++11) |
| protected:  basic_ostream( basic_ostream&& rhs ); | (3) | (since C++11) |
|  |  |  |

1) Constructs the `basic_ostream` object, assigning initial values to the base class by calling basic_ios::init(sb).2) The copy constructor is protected, and is deleted. Output streams are not copyable.3) The move constructor uses basic_ios<CharT, Traits>::move(rhs) to move all `basic_ios` members, except for the `rdbuf()`, from rhs into \*this. This move constructor is protected: it is called by the move constructors of movable output stream classes std::basic_ofstream and std::basic_ostringstream, which know how to correctly move the associated streambuffer.

### Parameters

|  |  |  |
| --- | --- | --- |
| sb | - | streambuffer to use as output sequence |
| rhs | - | basic_ostream to initialize from |

### Notes

Because basic_ios::init(sb) sets `badbit` when sb is a null pointer, and because basic_ostream::sentry does nothing if the stream is already in a failed state, writing to a stream constructed from a null pointer sb is a no-op.

### Example

Run this code

```
#include <iostream>
#include <sstream>
#include <utility>
 
int main()
{
    // ERROR: copy ctor is deleted
//  std::ostream myout(std::cout);
 
    // OK: shares buffer with cout
    std::ostream myout(std::cout.rdbuf());
 
    // ERROR: move constructor is protected
//  std::ostream s2(std::move(std::ostringstream() << 7.1));
 
    // OK: move ctor called through the derived class
    std::ostringstream s2(std::ostringstream() << 7.1);
    myout << s2.str() << '\n';
 
    std::ostream dev_null{nullptr}; // see Notes above
    dev_null << "no-op";
}

```

Output:

```
7.1

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ostream/basic_ostream&oldid=158549>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 September 2023, at 08:45.