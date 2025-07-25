# std::basic_stringbuf

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
| basic_streambuf | | | | |
| basic_filebuf | | | | |
| ****basic_stringbuf**** | | | | |
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

****std::basic_stringbuf****

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
| basic_stringbuf::**init_buf_ptrs** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<sstream>` |  |  |
| template<  class CharT,      class Traits = std::char_traits<CharT>,      class Allocator = std::allocator<CharT>  > class basic_stringbuf : public std::basic_streambuf<CharT, Traits> |  |  |
|  |  |  |

`std::basic_stringbuf` is a std::basic_streambuf whose associated character sequence is a memory-resident sequence of arbitrary characters, which can be initialized from or made available as an instance of std::basic_string.

Typical implementations of `std::basic_stringbuf` hold an object of type std::basic_string or equivalent resizable sequence container directly as a data member and use it as both the controlled character sequence (the array where the six pointers of std::basic_streambuf are pointing to) and as the associated character sequence (the source of characters for all input operations and the target for the output).

In addition, a typical implementation holds a data member of type std::ios_base::openmode to indicate the I/O mode of the associated stream (input-only, output-only, input/output, at-end, etc).

|  |  |
| --- | --- |
| If over-allocation strategy is used by overflow(), an additional high-watermark pointer may be stored to track the last initialized character. | (since C++11) |

Several typedefs for common character types are provided:

|  |  |
| --- | --- |
| Defined in header `<sstream>` | |
| Type | Definition |
| `std::stringbuf` | std::basic_stringbuf<char> |
| `std::wstringbuf` | std::basic_stringbuf<wchar_t> |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `char_type` | `CharT` |
| `traits_type` | `Traits`; the program is ill-formed if `Traits::char_type` is not `CharT`. |
| `int_type` | `Traits::int_type` |
| `pos_type` | `Traits::pos_type` |
| `off_type` | `Traits::off_type` |
| `allocator_type` | `Allocator` |

### Exposition-only members

|  |  |
| --- | --- |
| `buf` | the std::basic_string<CharT, Traits, Allocator> used as the underlying buffer (exposition-only member object\*) |
| `mode` | the std::ios_base::openmode of the associated stream (exposition-only member object\*) |
| **init_buf_ptrs** | initializes the input and output sequences (exposition-only member function\*) |

### Public member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_stringbuf` object   (public member function) |
| operator=(C++11) | assigns a `basic_stringbuf` object   (public member function) |
| swap(C++11) | swaps two `basic_stringbuf` objects   (public member function) |
| (destructor)[virtual] (implicitly declared) | destructs a `basic_stringbuf` object and the string it holds   (virtual public member function) |
| str | replaces or obtains a copy of the associated character string   (public member function) |
| get_allocator(C++20) | obtains a copy of the allocator associated with the internal sequence container   (public member function) |
| view(C++20) | obtains a view over the underlying character sequence   (public member function) |

### Protected member functions

|  |  |
| --- | --- |
| underflow[virtual] | returns the next character available in the input sequence   (virtual protected member function) |
| pbackfail[virtual] | puts a character back into the input sequence   (virtual protected member function) |
| overflow[virtual] | appends a character to the output sequence   (virtual protected member function) |
| setbuf[virtual] | attempts to replace the controlled character sequence with an array   (virtual protected member function) |
| seekoff[virtual] | repositions the next pointer in the input sequence, output sequence, or both, using relative addressing   (virtual protected member function) |
| seekpos[virtual] | repositions the next pointer in the input sequence, output sequence, or both using absolute addressing   (virtual protected member function) |

### Non-member functions

|  |  |
| --- | --- |
| std::swap(std::basic_stringbuf)(C++11) | specializes the std::swap algorithm   (function template) |

## Inherited from std::basic_streambuf

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
| (destructor)[virtual] | destructs the `basic_streambuf` object   (virtual public member function of `std::basic_streambuf<CharT,Traits>`) |
| Locales | |
| pubimbue | changes the associated locale and invokes imbue()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| getloc | obtains a copy of the associated locale   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| Positioning | |
| pubsetbuf | invokes setbuf()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| pubseekoff | invokes seekoff()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| pubseekpos | invokes seekpos()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| pubsync | invokes sync()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| Get area | |
| in_avail | obtains the number of characters immediately available in the get area   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| snextc | advances the input sequence, then reads one character without advancing again   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sbumpcstossc(removed in C++17) | reads one character from the input sequence and advances the sequence   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sgetc | reads one character from the input sequence without advancing the sequence   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sgetn | invokes xsgetn()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| Put area | |
| sputc | writes one character to the put area and advances the next pointer   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sputn | invokes xsputn()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| Putback | |
| sputbackc | puts one character back in the input sequence   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sungetc | moves the next pointer in the input sequence back by one   (public member function of `std::basic_streambuf<CharT,Traits>`) |

### Protected member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_streambuf` object   (protected member function) |
| operator=(C++11) | replaces a `basic_streambuf` object   (protected member function) |
| swap(C++11) | swaps two `basic_streambuf` objects   (protected member function) |
| Locales | |
| imbue[virtual] | reacts to a change of the associated locale   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| Positioning | |
| setbuf[virtual] | replaces the buffer with user-defined array, if permitted   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| seekoff[virtual] | repositions the next pointer in the input sequence, output sequence, or both, using relative addressing   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| seekpos[virtual] | repositions the next pointer in the input sequence, output sequence, or both using absolute addressing   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| sync[virtual] | synchronizes the buffers with the associated character sequence   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| Get area | |
| showmanyc[virtual] | obtains the number of characters available for input in the associated input sequence, if known   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| underflow[virtual] | reads characters from the associated input sequence to the get area   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| uflow[virtual] | reads characters from the associated input sequence to the get area and advances the next pointer   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| xsgetn[virtual] | reads multiple characters from the input sequence   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| ebackgptregptr | returns a pointer to the beginning, current character and the end of the get area   (protected member function) |
| gbump | advances the next pointer in the input sequence   (protected member function) |
| setg | repositions the beginning, next, and end pointers of the input sequence   (protected member function) |
| Put area | |
| xsputn[virtual] | writes multiple characters to the output sequence   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| overflow[virtual] | writes characters to the associated output sequence from the put area   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| pbasepptrepptr | returns a pointer to the beginning, current character and the end of the put area   (protected member function) |
| pbump | advances the next pointer of the output sequence   (protected member function) |
| setp | repositions the beginning, next, and end pointers of the output sequence   (protected member function) |
| Putback | |
| pbackfail[virtual] | puts a character back into the input sequence, possibly modifying the input sequence   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_stringbuf&oldid=158040>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 September 2023, at 23:01.