# std::basic_streambuf<CharT,Traits>::sputn, std::basic_streambuf<CharT,Traits>::xsputn

From cppreference.com
< cpp‎ | io‎ | basic streambuf
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

std::basic_streambuf

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Public member functions | | | | | | basic_streambuf::~basic_streambuf | | | | | | Locales | | | | | | basic_streambuf::pubimbue | | | | | | basic_streambuf::getloc | | | | | | Positioning | | | | | | basic_streambuf::pubsetbuf | | | | | | basic_streambuf::pubseekoff | | | | | | basic_streambuf::pubseekpos | | | | | | basic_streambuf::pubsync | | | | | | Get area | | | | | | basic_streambuf::in_avail | | | | | | basic_streambuf::snextc | | | | | | basic_streambuf::sbumpc | | | | | | basic_streambuf::sgetc | | | | | | basic_streambuf::sgetn | | | | | | Put area | | | | | | basic_streambuf::sputc | | | | | | ****basic_streambuf::sputn**** | | | | | | Putback | | | | | | basic_streambuf::sputbackc | | | | | | basic_streambuf::sungetc | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Protected member functions | | | | | | basic_streambuf::basic_streambuf | | | | | | basic_streambuf::operator=(C++11) | | | | | | basic_streambuf::swap(C++11) | | | | | | Locales | | | | | | basic_streambuf::imbue | | | | | | Positioning | | | | | | basic_streambuf::setbuf | | | | | | basic_streambuf::seekoff | | | | | | basic_streambuf::seekpos | | | | | | basic_streambuf::sync | | | | | | Get area | | | | | | basic_streambuf::showmanyc | | | | | | basic_streambuf::underflow | | | | | | basic_streambuf::uflow | | | | | | basic_streambuf::xsgetn | | | | | | basic_streambuf::ebackbasic_streambuf::gptrbasic_streambuf::egptr | | | | | | basic_streambuf::gbump | | | | | | basic_streambuf::setg | | | | | | Put area | | | | | | ****basic_streambuf::xsputn**** | | | | | | basic_streambuf::overflow | | | | | | basic_streambuf::pbasebasic_streambuf::pptrbasic_streambuf::epptr | | | | | | basic_streambuf::pbump | | | | | | basic_streambuf::setp | | | | | | Putback | | | | | | basic_streambuf::pbackfail | | | | | |

|  |  |  |
| --- | --- | --- |
| std::streamsize sputn( const char_type\* s, std::streamsize count ); | (1) |  |
| protected:  virtual std::streamsize xsputn( const char_type\* s, std::streamsize count ); | (2) |  |
|  |  |  |

1) Calls xsputn(s, count) of the most derived class.2) Writes count characters to the output sequence from the character array whose first element is pointed to by s. The characters are written as if by repeated calls to sputc(). Writing stops when either count characters are written or a call to sputc() would have returned Traits::eof().

If the put area becomes full (pptr() == epptr()), it is unspecified whether overflow() is actually called or its effect is achieved by other means.

### Parameters

(none)

### Return value

The number of characters successfully written.

### Notes

"achieved by other means" permits bulk I/O without intermediate buffering: that is how std::ofstream::write() simply passes the pointer to the suitable system call in some implementations.

### Example

Run this code

```
#include <iostream>
#include <sstream>
 
int main()
{
    std::ostringstream s1;
    std::streamsize sz = s1.rdbuf()->sputn("This is a test", 14);
    s1 << '\n';
    std::cout << "The call to sputn() returned " << sz << '\n'
              << "The output sequence contains " << s1.str();
 
    std::istringstream s2;
    sz = s2.rdbuf()->sputn("This is a test", 14);
    std::cout << "The call to sputn() on an input stream returned " << sz << '\n';
}

```

Output:

```
The call to sputn() returned 14
The output sequence contains This is a test
The call to sputn() on an input stream returned 0

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 565 | C++98 | `xsputn()` always called overflow() if pptr() == epptr() | it does not actually need to be called |

### See also

|  |  |
| --- | --- |
| sgetn | invokes xsgetn()   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_streambuf/sputn&oldid=148677>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 February 2023, at 01:40.