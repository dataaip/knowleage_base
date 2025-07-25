# std::basic_stringstream::operator=

From cppreference.com
< cpp‎ | io‎ | basic stringstream
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

std::basic_stringstream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| basic_stringstream::basic_stringstream | | | | |
| ****basic_stringstream::operator=**** | | | | |
| basic_stringstream::swap(C++11) | | | | |
| basic_stringstream::rdbuf | | | | |
| String operations | | | | |
| basic_stringstream::str | | | | |
| basic_stringstream::view(C++20) | | | | |
| Non-member functions | | | | |
| swap(std::basic_stringstream)(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_stringstream& operator=( basic_stringstream&& other ); |  | (since C++11) |
|  |  |  |

Move assigns the string stream other to \*this, effectively move-assigning both the std::basic_iostream base class and the associated std::basic_stringbuf.

Note that the base class move assignment swaps all stream state variables (except for rdbuf) between \*this and other.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | string stream to move from |

### Return value

\*this

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| swap(C++11) | swaps two string streams   (public member function) |
| operator=(C++11) | assigns a `basic_stringbuf` object   (public member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| operator=(C++11) | move-assigns another `basic_iostream`   (protected member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_stringstream/operator%3D&oldid=43406>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 November 2012, at 18:39.