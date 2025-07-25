# std::strstreambuf::str

From cppreference.com
< cpp‎ | io‎ | strstreambuf
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

std::strstreambuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| strstreambuf::strstreambuf | | | | |
| strstreambuf::~strstreambuf | | | | |
| strstreambuf::freeze | | | | |
| ****strstreambuf::str**** | | | | |
| strstreambuf::pcount | | | | |
| Protected member functions | | | | |
| strstreambuf::underflow | | | | |
| strstreambuf::pbackfail | | | | |
| strstreambuf::overflow | | | | |
| strstreambuf::setbuf | | | | |
| strstreambuf::seekoff | | | | |
| strstreambuf::seekpos | | | | |

|  |  |  |
| --- | --- | --- |
| char\* str(); |  | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

Calls freeze(), then returns a copy of start pointer of the get area, std::streambuf::eback().

The start of the get area, for all writeable `std::strstreambuf` objects constructed through the interface provided by std::strstream, is also the start of the put area.

### Parameters

(none)

### Return value

A copy of eback(), which may be a null pointer.

### Notes

This function is typically called through the std::strstream interface.

The call to freeze() guarantees that the returned pointer remains valid until the next explicit call to freeze(false): otherwise (on a dynamic buffer) any output operation could trigger buffer reallocation which would invalidate the pointer. It also causes a memory leak in the destructor of `std::strstreambuf`, unless freeze(false) is called before the buffer (or, more commonly, the std::strstream that manages it) is destroyed.

### Example

Run this code

```
#include <iostream>
#include <strstream>
 
int main()
{
    std::strstream dyn; // dynamically-allocated read/write buffer
    dyn << "Test: " << 1.23 << std::ends;
    std::strstreambuf* buf = dyn.rdbuf();
    std::cout << "R/W buffer holds [" << buf->str() // or dyn.str()
              << "]\n";
    dyn.freeze(false); // after calling .str() on a dynamic strstream
 
    char arr[10];
    std::ostrstream user(arr, 10); // fixed-size write-only buffer
    buf = user.rdbuf();
    user << 1.23 << std::ends;
    std::cout << "Write-only buffer holds [" << buf->str() // or user.str()
              << "]\n";
 
    std::istrstream lit("1 2 3"); // fixed-size read-only buffer
    buf = lit.rdbuf();
    std::cout << "Read-only buffer holds [" << buf->str() // or lit.str()
              << "]\n";
}

```

Output:

```
R/W buffer holds [Test: 1.23]
Write-only buffer holds [1.23]
Read-only buffer holds [1 2 31 2 3]

```

### See also

|  |  |
| --- | --- |
| str | accesses the output buffer   (public member function of `std::strstream`) |
| str | accesses the output buffer   (public member function of `std::ostrstream`) |
| str | accesses the output buffer   (public member function of `std::istrstream`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/strstreambuf/str&oldid=170647>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 06:32.