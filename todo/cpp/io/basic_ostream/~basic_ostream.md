# std::basic_ostream<CharT,Traits>::~basic_ostream

From cppreference.com
< cpp‎ | io‎ | basic ostream
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

std::basic_ostream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Global objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | coutwcout | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cerrwcerr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clogwclog | | | | | |
| Member functions | | | | |
| basic_ostream::basic_ostream | | | | |
| ****basic_ostream::~basic_ostream**** | | | | |
| basic_ostream::operator=(C++11) | | | | |
| Formatted output | | | | |
| basic_ostream::operator<< | | | | |
| Unformatted output | | | | |
| basic_ostream::put | | | | |
| basic_ostream::write | | | | |
| Positioning | | | | |
| basic_ostream::tellp | | | | |
| basic_ostream::seekp | | | | |
| Miscellaneous | | | | |
| basic_ostream::flush | | | | |
| basic_ostream::swap(C++11) | | | | |
| Member classes | | | | |
| basic_ostream::sentry | | | | |
| Non-member functions | | | | |
| operator<<(std::basic_ostream) | | | | |
| print(std::ostream)(C++23) | | | | |
| println(std::ostream)(C++23) | | | | |
| vprint_unicode(std::ostream)(C++23) | | | | |
| vprint_nonunicode(std::ostream)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| virtual ~basic_ostream(); |  |  |
|  |  |  |

Destroys the `basic_ostream` object. This destructor does not perform any operation on the underlying streambuffer (`rdbuf()`): the destructors of the derived output streams such as std::basic_ofstream and std::basic_ostringstream are responsible for calling the destructors of the stream buffers.

### Example

Run this code

```
#include <iostream>
#include <sstream>
 
void add_words(std::streambuf* p)
{
    std::ostream buf(p); // buf shares the buffer with s
    buf << " is the answer";
} // calls the destructor of buf. p remains unaffected
 
int main()
{
    std::ostringstream s;
    s << 42;
    add_words(s.rdbuf());
    s << ".";
    std::cout << s.str() << '\n';
}

```

Output:

```
42 is the answer.

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ostream/%7Ebasic_ostream&oldid=158548>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 September 2023, at 08:39.