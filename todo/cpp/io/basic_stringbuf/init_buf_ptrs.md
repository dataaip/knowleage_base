# std::basic_stringbuf<CharT,Traits,Allocator>::**init_buf_ptrs**

From cppreference.com
< cpp‎ | io‎ | basic stringbuf
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

std::basic_stringbuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| basic_stringbuf::basic_stringbuf | | | | |
| basic_stringbuf::operator=(C++11) | | | | |
| basic_stringbuf::swap(C++11) | | | | |
| basic_stringbuf::str | | | | |
| basic_stringbuf::get_allocator(C++20) | | | | |
| basic_stringbuf::view(C++20) | | | | |
| Protected member functions | | | | |
| basic_stringbuf::underflow | | | | |
| basic_stringbuf::pbackfail | | | | |
| basic_stringbuf::overflow | | | | |
| basic_stringbuf::setbuf | | | | |
| basic_stringbuf::seekoff | | | | |
| basic_stringbuf::seekpos | | | | |
| Non-member functions | | | | |
| swap(std::basic_stringbuf)(C++11) | | | | |
| Exposition-only member functions | | | | |
| ****basic_stringbuf::**init_buf_ptrs****** | | | | |

|  |  |  |
| --- | --- | --- |
| void init_buf_ptrs(); |  | (exposition only\*) |
|  |  |  |

Initializes the input and output sequences from buf according to mode. buf and mode are exposition-only data members of \*this.

Immediately after this function returns:

- If std::ios_base::out is set in mode, pbase() points to buf.front() and epptr() >= pbase() + buf.size() is true;
  - in addition, if std::ios_base::ate is set in mode, pptr() == pbase() + buf.size() is true,
  - otherwise pptr() == pbase() is true.
- If std::ios_base::in is set in mode, eback() points to buf.front(), and gptr() == eback() && egptr() == eback() + buf.size() is true.

### Notes

For efficiency reasons, stream buffer operations can violate invariants of buf while it is held encapsulated in the `std::basic_stringbuf`, e.g., by writing to characters in the range ``buf.data() + buf.size()`,`buf.data() + buf.capacity()`)`.

All operations retrieving a [std::basic_string from buf ensure that the std::basic_string invariants hold on the returned value.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 1448 | C++98 | calling `init_buf_ptrs()` made pptr() == pbase() + buf.data() for streams that are both input and output streams | makes pptr() == pbase() + buf.size() for append streams |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_stringbuf/init_buf_ptrs&oldid=158134>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 September 2023, at 18:18.