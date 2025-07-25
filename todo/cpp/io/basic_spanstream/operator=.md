# std::basic_spanstream<CharT,Traits>::operator=

From cppreference.com
< cpp‎ | io‎ | basic spanstream
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

std::basic_spanstream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| basic_spanstream::basic_spanstream(C++23) | | | | |
| ****basic_spanstream::operator=****(C++23) | | | | |
| basic_spanstream::swap(C++23) | | | | |
| basic_spanstream::rdbuf(C++23) | | | | |
| Underlying buffer operations | | | | |
| basic_spanstream::span(C++23) | | | | |
| Non-member functions | | | | |
| swap(std::basic_spanstream)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_spanstream& operator=( basic_spanstream&& other ); | (1) | (since C++23) |
| basic_spanstream& operator=( const basic_spanstream& ) = delete; | (2) | (since C++23) |
|  |  |  |

1) Move assigns the other to \*this, effectively move-assigning both the std::basic_iostream base class subobject and the wrapped std::basic_spanbuf.2) Copy assignment operator is deleted. `basic_spanstream` is not copy assignable.

Note that move assignment operator of the base class swaps all stream state variables (except for `rdbuf()`) between \*this and other.

It is implementation-defined whether the std::basic_spanbuf wrapped in other still holds an underlying buffer after the move assignment.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another stream to move from |

### Return value

\*this

### Exceptions

May throw implementation-defined exceptions.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| operator= | assigns a `basic_spanbuf` object   (public member function of `std::basic_spanbuf<CharT,Traits>`) |
| operator=(C++11) | move-assigns another `basic_iostream`   (protected member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_spanstream/operator%3D&oldid=130849>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 June 2021, at 06:57.