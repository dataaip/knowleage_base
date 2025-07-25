# std::strstreambuf::overflow

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
| strstreambuf::pbackfail | | | | |
| ****strstreambuf::overflow**** | | | | |
| strstreambuf::setbuf | | | | |
| strstreambuf::seekoff | | | | |
| strstreambuf::seekpos | | | | |

|  |  |  |
| --- | --- | --- |
| protected:  virtual int_type overflow( int_type c = EOF ); |  | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

Appends the character c to the put area of the buffer, reallocating if possible.

1) If c == EOF, does nothing.2) Otherwise, if the put area has a write position available (pptr() < epptr()), stores the character as if by \*pptr()++ = c.3) Otherwise, if the stream buffer mode is not dynamic or the stream buffer is currently frozen, the function fails and returns EOF.4) Otherwise, the function reallocates (or initially allocates) a dynamic array large enough to hold the contents of the current dynamic array (if any) plus at least one additional write position. If a pointer to the allocating function `palloc` was used in the constructor, that function is called with (\*palloc)(n) where `n` is the number of bytes to allocate, otherwise new char[n] is used. If a pointer to the deallocating function `pfree` was used in the constructor, that function is called with (\*pfree)(p) to deallocate the previous array, if needed, otherwise delete[] p is used. If allocation fails, the function fails and returns EOF.

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | the character to store in the put area |

### Return value

If c == EOF, returns some value other than EOF. Otherwise, returns (unsigned char)(c) on success, EOF on failure.

### Example

Run this code

```
#include <iostream>
#include <strstream>
 
struct mybuf : std::strstreambuf
{
    int_type overflow(int_type c) 
    {
        std::cout << "Before overflow(): size of the put area is " << epptr()-pbase()
                  << " with " << epptr()-pptr() << " write positions available\n";
        int_type rc = std::strstreambuf::overflow(c);
        std::cout << "After overflow(): size of the put area is " << epptr()-pbase()
                  << " with " << epptr()-pptr() << " write positions available\n";
        return rc;
    }
};
 
int main()
{
    mybuf sbuf; // read-write dynamic strstreambuf
    std::iostream stream(&sbuf);
 
    stream << "Sufficiently long string to overflow the initial allocation, at least "
           << " on some systems.";
}

```

Possible output:

```
Before overflow(): size of the put area is 16 with 0 write positions available
After overflow(): size of the put area is 32 with 15 write positions available
Before overflow(): size of the put area is 32 with 0 write positions available
After overflow(): size of the put area is 64 with 31 write positions available
Before overflow(): size of the put area is 64 with 0 write positions available
After overflow(): size of the put area is 128 with 63 write positions available

```

### See also

|  |  |
| --- | --- |
| overflow[virtual] | writes characters to the associated output sequence from the put area   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| overflow[virtual] | appends a character to the output sequence   (virtual protected member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| overflow[virtual] | writes characters to the associated file from the put area   (virtual protected member function of `std::basic_filebuf<CharT,Traits>`) |
| sputc | writes one character to the put area and advances the next pointer   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| put | inserts a character   (public member function of `std::basic_ostream<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/strstreambuf/overflow&oldid=170651>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 06:44.