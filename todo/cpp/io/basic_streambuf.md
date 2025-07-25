# std::basic_streambuf

From cppreference.com
< cpp‎ | io
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
| ****basic_streambuf**** | | | | |
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

****std::basic_streambuf****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Public member functions | | | | | | basic_streambuf::~basic_streambuf | | | | | | Locales | | | | | | basic_streambuf::pubimbue | | | | | | basic_streambuf::getloc | | | | | | Positioning | | | | | | basic_streambuf::pubsetbuf | | | | | | basic_streambuf::pubseekoff | | | | | | basic_streambuf::pubseekpos | | | | | | basic_streambuf::pubsync | | | | | | Get area | | | | | | basic_streambuf::in_avail | | | | | | basic_streambuf::snextc | | | | | | basic_streambuf::sbumpc | | | | | | basic_streambuf::sgetc | | | | | | basic_streambuf::sgetn | | | | | | Put area | | | | | | basic_streambuf::sputc | | | | | | basic_streambuf::sputn | | | | | | Putback | | | | | | basic_streambuf::sputbackc | | | | | | basic_streambuf::sungetc | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Protected member functions | | | | | | basic_streambuf::basic_streambuf | | | | | | basic_streambuf::operator=(C++11) | | | | | | basic_streambuf::swap(C++11) | | | | | | Locales | | | | | | basic_streambuf::imbue | | | | | | Positioning | | | | | | basic_streambuf::setbuf | | | | | | basic_streambuf::seekoff | | | | | | basic_streambuf::seekpos | | | | | | basic_streambuf::sync | | | | | | Get area | | | | | | basic_streambuf::showmanyc | | | | | | basic_streambuf::underflow | | | | | | basic_streambuf::uflow | | | | | | basic_streambuf::xsgetn | | | | | | basic_streambuf::ebackbasic_streambuf::gptrbasic_streambuf::egptr | | | | | | basic_streambuf::gbump | | | | | | basic_streambuf::setg | | | | | | Put area | | | | | | basic_streambuf::xsputn | | | | | | basic_streambuf::overflow | | | | | | basic_streambuf::pbasebasic_streambuf::pptrbasic_streambuf::epptr | | | | | | basic_streambuf::pbump | | | | | | basic_streambuf::setp | | | | | | Putback | | | | | | basic_streambuf::pbackfail | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<streambuf>` |  |  |
| template<   class CharT,       class Traits = std::char_traits<CharT> > class basic_streambuf; |  |  |
|  |  |  |

The class `basic_streambuf` controls input and output to a character sequence. It includes and provides access to

1. The **controlled character sequence**, also called the **buffer**, which may contain **input sequence** (also called **get area**) for buffering the input operations and/or **output sequence** (also called **put area**) for buffering the output operations.
2. The **associated character sequence**, also called **source** (for input) or **sink** (for output). This may be an entity that is accessed through OS API (file, TCP socket, serial port, other character device), or it may be an object (std::vector, array, string literal), that can be interpreted as a character source or sink.

The I/O stream objects std::basic_istream and std::basic_ostream, as well as all objects derived from them (std::ofstream, std::stringstream, etc), are implemented entirely in terms of `std::basic_streambuf`.

The controlled character sequence is an array of `CharT` which, at all times, represents a subsequence, or a "window" into the associated character sequence. Its state is described by three pointers:

1. The **beginning pointer**, always points at the lowest element of the buffer.
2. The **next pointer**, points at the element that is the next candidate for reading or writing.
3. The **end pointer**, points one past the end of the buffer.

A `basic_streambuf` object may support input (in which case the buffer described by the beginning, next, and end pointers is called **get area**), output (**put area**), or input and output simultaneously. In latter case, six pointers are tracked, which may all point to elements of the same character array or two individual arrays.

If the next pointer is less than the end pointer in the put area, a **write position** is available. The next pointer can be dereferenced and assigned to.

If the next pointer is less than the end pointer in the get area, a **read position** is available. The next pointer can be dereferenced and read from.

If the next pointer is greater than the beginning pointer in a get area, a **putback position** is available, and the next pointer may be decremented, dereferenced, and assigned to, in order to put a character back into the get area.

The character representation and encoding in the controlled sequence may be different from the character representations in the associated sequence, in which case a std::codecvt locale facet is typically used to perform the conversion. Common examples are UTF-8 (or other multibyte) files accessed through std::wfstream objects: the controlled sequence consists of wchar_t characters, but the associated sequence consists of bytes.

Typical implementation of the `std::basic_streambuf` base class holds only the six `CharT*` pointers and a copy of std::locale as data members. In addition, implementations may keep cached copies of locale facets, which are invalidated whenever `imbue()` is called. The concrete buffers such as std::basic_filebuf or std::basic_stringbuf are derived from `std::basic_streambuf`.

!std-streambuf.svg

Several typedefs for common character types are provided:

|  |  |
| --- | --- |
| Defined in header `<streambuf>` | |
| Type | Definition |
| `std::streambuf` | std::basic_streambuf<char> |
| `std::wstreambuf` | std::basic_streambuf<wchar_t> |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `char_type` | `CharT` |
| `traits_type` | `Traits`; the program is ill-formed if `Traits::char_type` is not `CharT`. |
| `int_type` | `Traits::int_type` |
| `pos_type` | `Traits::pos_type` |
| `off_type` | `Traits::off_type` |

### Member functions

|  |  |
| --- | --- |
| (destructor)[virtual] | destructs the `basic_streambuf` object   (virtual public member function) |
| Locales | |
| pubimbue | changes the associated locale and invokes imbue()   (public member function) |
| getloc | obtains a copy of the associated locale   (public member function) |
| Positioning | |
| pubsetbuf | invokes setbuf()   (public member function) |
| pubseekoff | invokes seekoff()   (public member function) |
| pubseekpos | invokes seekpos()   (public member function) |
| pubsync | invokes sync()   (public member function) |
| Get area | |
| in_avail | obtains the number of characters immediately available in the get area   (public member function) |
| snextc | advances the input sequence, then reads one character without advancing again   (public member function) |
| sbumpcstossc(removed in C++17) | reads one character from the input sequence and advances the sequence   (public member function) |
| sgetc | reads one character from the input sequence without advancing the sequence   (public member function) |
| sgetn | invokes xsgetn()   (public member function) |
| Put area | |
| sputc | writes one character to the put area and advances the next pointer   (public member function) |
| sputn | invokes xsputn()   (public member function) |
| Putback | |
| sputbackc | puts one character back in the input sequence   (public member function) |
| sungetc | moves the next pointer in the input sequence back by one   (public member function) |
| Protected member functions | |
| (constructor) | constructs a `basic_streambuf` object   (protected member function) |
| operator=(C++11) | replaces a `basic_streambuf` object   (protected member function) |
| swap(C++11) | swaps two `basic_streambuf` objects   (protected member function) |
| Locales | |
| imbue[virtual] | reacts to a change of the associated locale   (virtual protected member function) |
| Positioning | |
| setbuf[virtual] | replaces the buffer with user-defined array, if permitted   (virtual protected member function) |
| seekoff[virtual] | repositions the next pointer in the input sequence, output sequence, or both, using relative addressing   (virtual protected member function) |
| seekpos[virtual] | repositions the next pointer in the input sequence, output sequence, or both using absolute addressing   (virtual protected member function) |
| sync[virtual] | synchronizes the buffers with the associated character sequence   (virtual protected member function) |
| Get area | |
| showmanyc[virtual] | obtains the number of characters available for input in the associated input sequence, if known   (virtual protected member function) |
| underflow[virtual] | reads characters from the associated input sequence to the get area   (virtual protected member function) |
| uflow[virtual] | reads characters from the associated input sequence to the get area and advances the next pointer   (virtual protected member function) |
| xsgetn[virtual] | reads multiple characters from the input sequence   (virtual protected member function) |
| ebackgptregptr | returns a pointer to the beginning, current character and the end of the get area   (protected member function) |
| gbump | advances the next pointer in the input sequence   (protected member function) |
| setg | repositions the beginning, next, and end pointers of the input sequence   (protected member function) |
| Put area | |
| xsputn[virtual] | writes multiple characters to the output sequence   (virtual protected member function) |
| overflow[virtual] | writes characters to the associated output sequence from the put area   (virtual protected member function) |
| pbasepptrepptr | returns a pointer to the beginning, current character and the end of the put area   (protected member function) |
| pbump | advances the next pointer of the output sequence   (protected member function) |
| setp | repositions the beginning, next, and end pointers of the output sequence   (protected member function) |
| Putback | |
| pbackfail[virtual] | puts a character back into the input sequence, possibly modifying the input sequence   (virtual protected member function) |

### See also

|  |  |
| --- | --- |
| FILE | object type, capable of holding all information needed to control a C I/O stream   (typedef) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_streambuf&oldid=165210>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 December 2023, at 04:14.