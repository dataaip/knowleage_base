# std::swap(std::basic_syncbuf)

From cppreference.com
< cpp‎ | io‎ | basic syncbuf
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

std::basic_syncbuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| basic_syncbuf::basic_syncbuf(C++20) | | | | |
| basic_syncbuf::operator=(C++20) | | | | |
| basic_syncbuf::~basic_syncbuf(C++20) | | | | |
| basic_syncbuf::swap(C++20) | | | | |
| basic_syncbuf::emit(C++20) | | | | |
| basic_syncbuf::get_wrapped(C++20) | | | | |
| basic_syncbuf::get_allocator(C++20) | | | | |
| basic_syncbuf::set_emit_on_sync(C++20) | | | | |
| Protected member functions | | | | |
| basic_syncbuf::sync(C++20) | | | | |
| Non-member functions | | | | |
| ****swap(std::basic_syncbuf)****(C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| template< class CharT, class Traits, class Allocator >  void swap( std::basic_syncbuf<CharT, Traits, Allocator>& lhs, std::basic_syncbuf<CharT, Traits, Allocator>& rhs ); |  | (since C++20) |
|  |  |  |

Overloads the std::swap algorithm for std::basic_syncbuf. Exchanges the state of lhs with that of rhs. Effectively calls lhs.swap(rhs).

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | std::basic_syncbuf objects whose states to swap |

### Return value

(none)

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| swap | swaps two `basic_syncbuf` objects   (public member function) |
| swap | swaps the values of two objects   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_syncbuf/swap2&oldid=156843>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 August 2023, at 08:56.