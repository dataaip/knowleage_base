# std::strstreambuf::pbackfail

From cppreference.com
< cpp‎ | io‎ | strstreambuf
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

std::strstreambuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| strstreambuf::strstreambuf | | | | |
| strstreambuf::~strstreambuf | | | | |
| strstreambuf::freeze | | | | |
| strstreambuf::str | | | | |
| strstreambuf::pcount | | | | |
| Protected member functions | | | | |
| strstreambuf::underflow | | | | |
| ****strstreambuf::pbackfail**** | | | | |
| strstreambuf::overflow | | | | |
| strstreambuf::setbuf | | | | |
| strstreambuf::seekoff | | | | |
| strstreambuf::seekpos | | | | |

|  |  |  |
| --- | --- | --- |
| protected:  virtual int_type pbackfail( int_type c = EOF ); |  | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

This protected virtual function is called by the public functions basic_streambuf::sungetc and basic_streambuf::sputbackc (which, in turn, are called by basic_istream::unget and basic_istream::putback).

1) The caller is requesting that the get area is backed up by one character (`pbackfail()` is called with no arguments or with EOF as the argument)a) First, checks if there is a putback position, and if there really isn't, fails (`strstreambuf` has no external character source to re-read).b) If the caller was wrong and the putback position is in fact available, simply decrements basic_streambuf::gptr(), e.g. by calling gbump(-1).2) The caller attempts to putback a different character from the one retrieved earlier (`pbackfail()` is called with the character that needs to be put back), in which casea) First, checks if there is a putback position, and if there isn't, fails.b) Then checks what character is in the putback position. If the character held there is already equal to (char)c, then simply decrements basic_streambuf::gptr().c) Otherwise, if the buffer is unmodifiable (this strstreambuf was constructed with a string literal or some other const array), fails.d) Otherwise, decrements basic_streambuf::gptr() and writes c to the location pointed to gptr() after adjustment.

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | the character to put back, or Traits::eof() to indicate that backing up of the get area is requested |

### Return value

c on success except if c was EOF, in which case unspecified value other than EOF is returned.

EOF on failure.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| pbackfail[virtual] | puts a character back into the input sequence, possibly modifying the input sequence   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| sungetc | moves the next pointer in the input sequence back by one   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| sputbackc | puts one character back in the input sequence   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| unget | unextracts a character   (public member function of `std::basic_istream<CharT,Traits>`) |
| putback | puts a character into input stream   (public member function of `std::basic_istream<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/strstreambuf/pbackfail&oldid=170650>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 06:42.