# std::basic_syncbuf

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
| basic_stringbuf | | | | |
| basic_spanbuf(C++23) | | | | |
| strstreambuf(C++98/26\*) | | | | |
| ****basic_syncbuf****(C++20) | | | | |
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

****std::basic_syncbuf****

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
| swap(std::basic_syncbuf)(C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<syncstream>` |  |  |
| template<  class CharT,      class Traits = std::char_traits<CharT>,      class Allocator = std::allocator<CharT> > class basic_syncbuf : public std::basic_streambuf<CharT, Traits> |  | (since C++20) |
|  |  |  |

`std::basic_syncbuf` is a wrapper for a std::basic_streambuf (provided at construction time as a pointer). It accumulates output in its own internal buffer, and atomically transmits its entire contents to the wrapped buffer on destruction and when explicitly requested, so that they appear as a contiguous sequence of characters. It guarantees that there are no data races and no interleaving of characters sent to the wrapped buffer as long as all other outputs made to the same buffer are made through, possibly different, instances of `std::basic_syncbuf`.

Typical implementation of `std::basic_syncbuf` holds a pointer to the wrapped std::basic_streambuf, a boolean flag indicating whether the buffer will transmit its contents to the wrapped buffer on sync (flush), a boolean flag indicating a pending flush when the policy is to not emit on sync, an internal buffer that uses `Allocator` (such as std::string), and a pointer to a mutex used to synchronize emit between multiple threads accessing the same wrapped stream buffer (these mutexes may be in a hash map with pointers to std::basic_streambuf objects used as keys).

Like other streambuf classes, `std::basic_syncbuf` is normally only accessed through the corresponding stream, std::osyncstream, not directly.

Several typedefs for common character types are provided:

|  |  |
| --- | --- |
| Defined in header `<syncstream>` | |
| Type | Definition |
| `std::syncbuf` | std::basic_syncbuf<char> |
| `std::wsyncbuf` | std::basic_syncbuf<wchar_t> |

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
| `streambuf_type` | std::basic_streambuf<CharT, Traits> |

### Member functions

|  |  |
| --- | --- |
| Public member functions | |
| (constructor) | constructs a `basic_syncbuf` object   (public member function) |
| operator= | assigns a `basic_syncbuf` object   (public member function) |
| swap | swaps two `basic_syncbuf` objects   (public member function) |
| (destructor) | destroys the `basic_syncbuf` and emits its internal buffer   (public member function) |
| emit | atomically transmits the entire internal buffer to the wrapped streambuf   (public member function) |
| get_wrapped | retrieves the wrapped streambuf pointer   (public member function) |
| get_allocator | retrieves the allocator used by this `basic_syncbuf`   (public member function) |
| set_emit_on_sync | changes the current emit-on-sync policy   (public member function) |
| Protected member functions | |
| sync | either emits, or records a pending flush, depending on the current emit-on-sync policy   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| std::swap(std::basic_syncbuf)(C++20) | specializes the std::swap algorithm   (function template) |

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

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_syncbuf` | `201803L` | (C++20) | Synchronized buffered ostream (`std::syncbuf`, std::osyncstream) and manipulators |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_syncbuf&oldid=148138>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 February 2023, at 18:23.