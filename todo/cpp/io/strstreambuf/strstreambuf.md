# std::strstreambuf::strstreambuf

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
| ****strstreambuf::strstreambuf**** | | | | |
| strstreambuf::~strstreambuf | | | | |
| strstreambuf::freeze | | | | |
| strstreambuf::str | | | | |
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
|  | (1) |  |
| explicit strstreambuf( std::streamsize alsize = 0 ); |  | (deprecated in C++98) (until C++11) |
| strstreambuf() : strstreambuf(0) {}  explicit strstreambuf( std::streamsize alsize ); |  | (since C++11)(removed in C++26) |
|  |  |  |
| --- | --- | --- |
| strstreambuf( void\* (\*palloc)(std::size_t), void (\*pfree)(void\*) ); | (2) | (deprecated in C++98)  (removed in C++26) |
| strstreambuf( char\* gnext, std::streamsize n, char\* pbeg = 0 ); | (3) | (deprecated in C++98)  (removed in C++26) |
| strstreambuf( signed char\* gnext, std::streamsize n, signed char\* pbeg = 0 ); | (4) | (deprecated in C++98)  (removed in C++26) |
| strstreambuf( unsigned char\* gnext, std::streamsize n, unsigned char\* pbeg = 0 ); | (5) | (deprecated in C++98)  (removed in C++26) |
| strstreambuf( const char\* gnext, std::streamsize n ); | (6) | (deprecated in C++98)  (removed in C++26) |
| strstreambuf( const signed char\* gnext, std::streamsize n ); | (7) | (deprecated in C++98)  (removed in C++26) |
| strstreambuf( const unsigned char\* gnext, std::streamsize n ); | (8) | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

1) Constructs a `std::strstreambuf` object: initializes the base class by calling the default constructor of std::streambuf, initializes the buffer state to "dynamic" (the buffer will be allocated as needed), initializes allocated size to the provided alsize, initializes the allocation and the deallocation functions to null (will use new[] and delete[]).2) Constructs a `std::strstreambuf` object: initializes the base class by calling the default constructor of std::streambuf, initializes the buffer state to "dynamic" (the buffer will be allocated as needed), initializes allocated size to unspecified value, initializes the allocation function to palloc and the deallocation function to pfree.3-5) Constructs a `std::strstreambuf` object in following steps:a) Initializes the base class by calling the default constructor of std::streambuf.b) Initializes the buffer state to "constant" (the buffer is a user-provided fixed-size buffer).c) Determines the number of elements in the user-provided array as follows: if n is greater than zero, n is used. If n is zero, std::strlen(gnext) is executed to determine the buffer size. If n is negative, INT_MAX is used.d) Configures the std::basic_streambuf pointers as follows: If pbeg is a null pointer, calls setg(gnext, gnext, gnext + N). If pbeg is not a null pointer, executes setg(gnext, gnext, pbeg) and setp(pbeg, pbeg + N), where N is the number of elements in the array as determined earlier.6-8) Same as strstreambuf((char\*)gnext, n), except the "constant" bit is set in the buffer state bitmask (output to this buffer is not allowed).

### Parameters

|  |  |  |
| --- | --- | --- |
| alsize | - | the initial size of the dynamically allocated buffer |
| palloc | - | pointer to user-provided allocation function |
| pfree | - | pointer to user-provided deallocation function |
| gnext | - | pointer to the start of the get area in the user-provided array |
| pbeg | - | pointer to the start of the put area in the user-provided array |
| n | - | the number of bytes in the get area (if pbeg is null) or in the put area (if pbeg is not null) of the user-provided array |

### Notes

These constructors are typically called by the constructors of std::strstream.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P0935R0 | C++11 | default constructor was explicit | made implicit |

### Example

Run this code

```
#include <iostream>
#include <strstream>
 
int main()
{
    std::strstreambuf dyn; // dynamic
    std::strstream dyn_s; // equivalent stream
    dyn_s << 1.23 << std::ends;
    std::cout << dyn_s.str() << '\n';
    dyn_s.freeze(false);
 
    char buf[10];
    std::strstreambuf user(buf, 10, buf); // user-provided output buffer
    std::ostrstream user_s(buf, 10); // equivalent stream
    user_s << 1.23 << std::ends;
    std::cout << buf << '\n';
 
    std::strstreambuf lit("1 2 3", 5); // constant
    std::istrstream lit_s("1 2 3"); // equivalent stream
    int i, j, k;
    lit_s >> i >> j >> k;
    std::cout << i << ' ' << j << ' ' << k << '\n';
}

```

Output:

```
1.23
1.23
1 2 3

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a `strstream` object, optionally allocating the buffer   (public member function of `std::strstream`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/strstreambuf/strstreambuf&oldid=170644>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 06:15.