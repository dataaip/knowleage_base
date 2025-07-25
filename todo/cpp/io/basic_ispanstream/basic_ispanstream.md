# std::basic_ispanstream<CharT,Traits>::basic_ispanstream

From cppreference.com
< cpp‎ | io‎ | basic ispanstream
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

std::basic_ispanstream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****basic_ispanstream::basic_ispanstream****(C++23) | | | | |
| basic_ispanstream::operator=(C++23) | | | | |
| basic_ispanstream::swap(C++23) | | | | |
| basic_ispanstream::rdbuf(C++23) | | | | |
| Underlying buffer operations | | | | |
| basic_ispanstream::span(C++23) | | | | |
| Non-member functions | | | | |
| swap(std::basic_ipanstream)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| explicit basic_ispanstream( std::span<CharT> s, std::ios_base::openmode mode =                                  std::ios_base::in ); | (1) | (since C++23) |
| template< class ROS >  explicit basic_ispanstream( ROS&& r ); | (2) | (since C++23) |
| basic_ispanstream( basic_ispanstream&& rhs ); | (3) | (since C++23) |
| basic_ispanstream( const basic_ispanstream& ) = delete; | (4) | (since C++23) |
|  |  |  |

Constructs a new `basic_ispanstream`.

1) Uses the storage referenced by s as initial underlying buffer of the wrapped std::basic_spanbuf device. The wrapped std::basic_spanbuf object is constructed as basic_spanbuf<Char, Traits>(s, mode | std::ios_base::in).2) Uses the storage referenced by r after converted to std::span<const CharT> as initial underlying buffer of the wrapped std::basic_spanbuf device. The wrapped std::basic_spanbuf object is opened in mode std::ios_base::in. This overload participates in overload resolution only if `ROS` models `borrowed_range`, std::convertible_to<ROS, std::span<CharT>> is false, and std::convertible_to<ROS, std::span<const CharT>> is true.3) Move constructor. Move constructs the std::basic_istream base subobject and the wrapped std::basic_spanbuf from those of rhs, and then calls set_rdbuf with the address of the wrapped std::basic_spanbuf in \*this to install it.4) Copy constructor is deleted. `basic_ispanstream` is not copyable.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | std::span referencing the storage to be use as initial underlying buffer of stream |
| r | - | `borrowed_range` to be use as initial underlying buffer of stream |
| mode | - | specifies stream open mode. Following constants and bit-wise OR between them may be used:  |  |  | | --- | --- | | Constant | Explanation | | app | seek to the end of stream before each write | | binary | open in binary mode | | in | open for reading | | out | open for writing | | trunc | discard the contents of the stream when opening | | ate | seek to the end of stream immediately after open | | noreplace (C++23) | open in exclusive mode | |
| other | - | another `basic_ispanstream` to be moved from |

### Exceptions

May throw implementation-defined exceptions.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_spanbuf` object   (public member function of `std::basic_spanbuf<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ispanstream/basic_ispanstream&oldid=130841>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 June 2021, at 05:49.