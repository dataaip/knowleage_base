# std::basic_spanbuf<CharT,Traits>::seekpos

From cppreference.com
< cpp‎ | io‎ | basic spanbuf
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

std::basic_spanbuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| basic_spanbuf::basic_spanbuf(C++23) | | | | |
| basic_spanbuf::operator=(C++23) | | | | |
| basic_spanbuf::swap(C++23) | | | | |
| basic_spanbuf::span(C++23) | | | | |
| Protected member functions | | | | |
| basic_spanbuf::setbuf(C++23) | | | | |
| basic_spanbuf::seekoff(C++23) | | | | |
| ****basic_spanbuf::seekpos****(C++23) | | | | |
| Non-member functions | | | | |
| swap(std::basic_spanbuf)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| protected:  pos_type seekpos( pos_type sp, std::ios_base::openmode which = std::ios_base::in | std::ios_base::out ) override; |  | (since C++23) |
|  |  |  |

Repositions the next pointer to the get and/or put area, if possible, to the position indicated by `sp`.

Equivalent to return seekoff(off_type(sp), std::ios_base::beg, which);.

### Parameters

|  |  |  |
| --- | --- | --- |
| sp | - | stream position, such as one obtained by seekoff() or `seekpos()` |
| which | - | defines whether the input sequences, the output sequence, or both are affected. It can be one or a combination of the following constants:  |  |  | | --- | --- | | Constant | Explanation | | in | affect the input sequence | | out | affect the output sequence | |

### Return value

`sp` on success or pos_type(off_type(-1)) on failure.

### Notes

`seekpos()` is called by std::basic_streambuf::pubseekpos(), which is called by the single-argument versions of std::basic_istream::seekg() and std::basic_ostream::seekp().

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| pubseekpos | invokes seekpos()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| seekpos[virtual] | repositions the next pointer in the input sequence, output sequence, or both using absolute addressing   (virtual protected member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| seekpos[virtual] | repositions the next pointer in the input sequence, output sequence, or both using absolute addressing   (virtual protected member function of `std::strstreambuf`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_spanbuf/seekpos&oldid=130778>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 June 2021, at 10:36.