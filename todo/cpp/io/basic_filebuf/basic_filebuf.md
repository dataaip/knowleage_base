# std::basic_filebuf<CharT,Traits>::basic_filebuf

From cppreference.com
< cpp‎ | io‎ | basic filebuf
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

std::basic_filebuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| ****basic_filebuf::basic_filebuf**** | | | | |
| basic_filebuf::~basic_filebuf | | | | |
| basic_filebuf::operator=(C++11) | | | | |
| basic_filebuf::swap(C++11) | | | | |
| basic_filebuf::native_handle(C++26) | | | | |
| basic_filebuf::is_open | | | | |
| basic_filebuf::open | | | | |
| basic_filebuf::close | | | | |
| Protected member functions | | | | |
| basic_filebuf::showmanyc | | | | |
| basic_filebuf::underflow | | | | |
| basic_filebuf::uflow | | | | |
| basic_filebuf::pbackfail | | | | |
| basic_filebuf::overflow | | | | |
| basic_filebuf::setbuf | | | | |
| basic_filebuf::seekoff | | | | |
| basic_filebuf::seekpos | | | | |
| basic_filebuf::sync | | | | |
| basic_filebuf::imbue | | | | |
| Non-member functions | | | | |
| swap(std::basic_filebuf)(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_filebuf(); | (1) |  |
| basic_filebuf( const std::basic_filebuf& rhs ) = delete; | (2) | (since C++11) |
| basic_filebuf( std::basic_filebuf&& rhs ); | (3) | (since C++11) |
|  |  |  |

Constructs new `std::basic_filebuf` object.

1) Constructs a `std::basic_filebuf` object, initializing the base class by calling the default constructor of std::basic_streambuf. The created `basic_filebuf` is not associated with a file, and is_open() returns false.2) The copy constructor is deleted; `std::basic_filebuf` is not CopyConstructible.3) Move-constructs a `std::basic_filebuf` object by moving all contents from another `std::basic_filebuf` object rhs, including the buffers, the associated file, the locale, the openmode, the is_open variable, and all other state. After move, rhs is not associated with a file and rhs.is_open() == false. The member pointers of the base class std::basic_streambuf of rhs and of the base class of \*this are guaranteed to point to different buffers (unless null).

### Parameters

|  |  |  |
| --- | --- | --- |
| rhs | - | another `basic_filebuf` |

### Notes

Typically called by the constructor of std::basic_fstream.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| operator=(C++11) | assigns a `basic_filebuf` object   (public member function) |
| (destructor)[virtual] | destructs a `basic_filebuf` object and closes the file if it is open   (virtual public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_filebuf/basic_filebuf&oldid=160450>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 October 2023, at 09:15.