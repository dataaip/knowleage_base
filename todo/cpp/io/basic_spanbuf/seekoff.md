# std::basic_spanbuf<CharT,Traits>::seekoff

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
| ****basic_spanbuf::seekoff****(C++23) | | | | |
| basic_spanbuf::seekpos(C++23) | | | | |
| Non-member functions | | | | |
| swap(std::basic_spanbuf)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| protected:  pos_type seekoff( off_type off, std::ios_base::seekdir dir,                    std::ios_base::openmode which = std::ios_base::in | std::ios_base::out ) override; |  | (since C++23) |
|  |  |  |

Repositions the next pointer to get and/or put area, if possible, to the position that corresponds to exactly `off` characters from beginning, end, or current position of the get and/or put area of the buffer.

Let `n` be the number of `CharT` elements in underlying buffer, or ​0​ when there is no underlying buffer, this function fails if

- the next pointer to the get and/or put area to reposition is null and the computed `newoff` (see below) is not zero, which may occur if there is no underlying buffer, or the \*this is not opened in the mode required by `which`, or
- `dir` is std::ios_base::cur and both std::ios_base::in and std::ios_base::out are set in `which`, or
- the computed `newoff` is not representable in `off_type`, less than zero, or greater than `n`.

`newoff` is computed as below:

- If `dir` is std::ios_base::beg, `newoff` is `off`.
- If `dir` is std::ios_base::cur, `newoff` is
  - pptr() - pbase() + off if std::ios_base::out is set in `which`, or
  - gptr() - eback() + off if std::ios_base::in is set in `which`.
- If `dir` is std::ios_base::end, `newoff` is
  - pptr() - pbase() + off if std::ios_base::out but not std::ios_base::in is set in the open mode of \*this,
  - otherwise, off + n.

This function repositions the next pointer to get and/or put area to pbuf + newoff on success if std::ios_base::in and/or std::ios_base::out is correspondingly set in `which`, where `pbuf` is the pointer to the beginning of the underlying buffer, or the null pointer value if there is no underlying buffer.

### Parameters

|  |  |  |
| --- | --- | --- |
| off | - | relative position to set the next pointer(s) to |
| dir | - | defines base position to apply the relative offset to. It can be one of the following constants:  |  |  | | --- | --- | | Constant | Explanation | | beg | the beginning of a stream | | end | the ending of a stream | | cur | the current position of stream position indicator | |
| which | - | defines whether the input sequences, the output sequence, or both are affected. It can be one or a combination of the following constants:  |  |  | | --- | --- | | Constant | Explanation | | in | affect the input sequence | | out | affect the output sequence | |

### Return value

pos_type(newoff) on success, pos_type(off_type(-1)) on failure.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| seekoff[virtual] | repositions the next pointer in the input sequence, output sequence, or both, using relative addressing   (virtual protected member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| seekoff[virtual] | repositions the next pointer in the input sequence, output sequence, or both, using relative addressing   (virtual protected member function of `std::strstreambuf`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_spanbuf/seekoff&oldid=130785>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 June 2021, at 11:35.