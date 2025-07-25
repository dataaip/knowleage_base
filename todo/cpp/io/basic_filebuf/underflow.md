# std::basic_filebuf<CharT,Traits>::underflow

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
| basic_filebuf::basic_filebuf | | | | |
| basic_filebuf::~basic_filebuf | | | | |
| basic_filebuf::operator=(C++11) | | | | |
| basic_filebuf::swap(C++11) | | | | |
| basic_filebuf::native_handle(C++26) | | | | |
| basic_filebuf::is_open | | | | |
| basic_filebuf::open | | | | |
| basic_filebuf::close | | | | |
| Protected member functions | | | | |
| basic_filebuf::showmanyc | | | | |
| ****basic_filebuf::underflow**** | | | | |
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
| protected:  virtual int_type underflow() |  |  |
|  |  |  |

Reads more data into the input area.

Behaves like the base class std::basic_streambuf::underflow, except that to read the data from the associated character sequence (the file) into the get area, first reads the bytes from the file into a temporary buffer (allocated as large as necessary), then uses std::codecvt::in of the imbued locale to convert the external (typically, multibyte) representation to the internal form which is then used to populate the get area. The conversion may be skipped if the locale's std::codecvt::always_noconv returns true.

### Parameters

(none)

### Return value

Traits::to_int_type(\*gptr()) (the first character of the pending sequence) in case of success, or Traits::eof() in case of failure.

### Example

Run this code

```
#include <fstream>
#include <iostream>
 
struct mybuf : std::filebuf
{
    int underflow()
    {
         std::cout << "Before underflow(): size of the get area is "
                   << egptr()-eback() << " with "
                   << egptr()-gptr() << " read positions available\n";
         int rc = std::filebuf::underflow();
         std::cout << "underflow() returns " << rc << ".\nAfter the call, "
                   << "size of the get area is "
                   << egptr()-eback() << " with "
                   << egptr()-gptr() << " read positions available\n";
        return rc;
    }
};
 
int main()
{
    mybuf buf;
    buf.open("test.txt", std::ios_base::in);
    std::istream stream(&buf);
    while (stream.get()) ;
}

```

Possible output:

```
Before underflow(): size of the get area is 0 with 0 read positions available
underflow() returns 73.
After the call, size of the get area is 110 with 110 read positions available
Before underflow(): size of the get area is 110 with 0 read positions available
underflow() returns -1.
After the call, size of the get area is 0 with 0 read positions available

```

### See also

|  |  |
| --- | --- |
| underflow[virtual] | reads characters from the associated input sequence to the get area   (virtual protected member function of `std::basic_streambuf<CharT,Traits>`) |
| underflow[virtual] | returns the next character available in the input sequence   (virtual protected member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| underflow[virtual] | reads a character from the input sequence without advancing the next pointer   (virtual protected member function of `std::strstreambuf`) |
| uflow[virtual] | reads from the associated file and advances the next pointer in the get area   (virtual protected member function) |
| overflow[virtual] | writes characters to the associated file from the put area   (virtual protected member function) |
| sgetc | reads one character from the input sequence without advancing the sequence   (public member function of `std::basic_streambuf<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_filebuf/underflow&oldid=158144>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 September 2023, at 23:54.