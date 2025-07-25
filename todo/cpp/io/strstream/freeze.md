# std::strstream::freeze

From cppreference.com
< cpp‎ | io‎ | strstream
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

std::strstream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| strstream::strstream | | | | |
| strstream::~strstream | | | | |
| strstream::rdbuf | | | | |
| strstream::str | | | | |
| strstream::pcount | | | | |
| ****strstream::freeze**** | | | | |

|  |  |  |
| --- | --- | --- |
| void freeze( bool flag = true ); |  | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

If the stream is using a dynamically-allocated array for output, disables (flag == true) or enables (flag == false) automatic allocation/deallocation of the buffer. Effectively calls rdbuf()->freeze(flag).

### Notes

After a call to str(), dynamic streams become frozen automatically. A call to freeze(false) is required before exiting the scope in which this strstream object was created, otherwise the destructor will leak memory. Also, additional output to a frozen stream may be truncated once it reaches the end of the allocated buffer.

### Parameters

|  |  |  |
| --- | --- | --- |
| flag | - | desired status |

### Return value

(none)

### Example

Run this code

```
#include <iostream>
#include <strstream>
 
int main()
{
    std::strstream dyn; // dynamically-allocated output buffer
    dyn << "Test: " << 1.23; // note: no std::ends to demonstrate appending
    std::cout << "The output stream contains \"";
    std::cout.write(dyn.str(), dyn.pcount()) << "\"\n";
    // the stream is now frozen due to str()
    dyn << " More text"; // output to a frozen stream may be truncated
    std::cout << "The output stream contains \"";
    std::cout.write(dyn.str(), dyn.pcount()) << "\"\n";
    dyn.freeze(false); // freeze(false) must be called or the  destructor will leak
 
    std::strstream dyn2; // dynamically-allocated output buffer
    dyn2 << "Test: " << 1.23; // note: no std::ends
    std::cout << "The output stream contains \"";
    std::cout.write(dyn2.str(), dyn2.pcount()) << "\"\n";
    dyn2.freeze(false);   // unfreeze the stream after str()
    dyn2 << " More text" << std::ends; // output will not be truncated (buffer grows)
    std::cout << "The output stream contains \"" << dyn2.str() << "\"\n";
    dyn2.freeze(false); // freeze(false) must be called or the  destructor will leak 
}

```

Possible output:

```
The output stream contains "Test: 1.23"
The output stream contains "Test: 1.23 More "
The output stream contains "Test: 1.23"
The output stream contains "Test: 1.23 More text"

```

### See also

|  |  |
| --- | --- |
| freeze | sets/clears the frozen state of the buffer   (public member function of `std::strstreambuf`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/strstream/freeze&oldid=105233>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 July 2018, at 03:42.