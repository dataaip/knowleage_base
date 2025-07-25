# std::ios_base::openmode

From cppreference.com
< cpp‎ | io‎ | ios base
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

std::ios_base

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ios_base::ios_base | | | | |
| ios_base::~ios_base | | | | |
| ios_base::operator= | | | | |
| Formatting | | | | |
| ios_base::flags | | | | |
| ios_base::setf | | | | |
| ios_base::unsetf | | | | |
| ios_base::precision | | | | |
| ios_base::width | | | | |
| Locales | | | | |
| ios_base::imbue | | | | |
| ios_base::getloc | | | | |
| Internal extensible array | | | | |
| ios_base::xalloc | | | | |
| ios_base::iword | | | | |
| ios_base::pword | | | | |
| Miscellaneous | | | | |
| ios_base::register_callback | | | | |
| ios_base::sync_with_stdio | | | | |
| Member classes | | | | |
| ios_base::failure | | | | |
| ios_base::Init | | | | |
| Member types | | | | |
| ****ios_base::openmode**** | | | | |
| ios_base::fmtflags | | | | |
| ios_base::iostate | | | | |
| ios_base::seekdir | | | | |
| ios_base::event | | | | |
| ios_base::event_callback | | | | |

|  |  |  |
| --- | --- | --- |
| typedef /\* implementation defined \*/ openmode; |  |  |
| static constexpr openmode app       = /\* implementation defined \*/;  static constexpr openmode binary    = /\* implementation defined \*/;  static constexpr openmode in        = /\* implementation defined \*/;  static constexpr openmode out       = /\* implementation defined \*/;  static constexpr openmode trunc     = /\* implementation defined \*/; static constexpr openmode ate       = /\* implementation defined \*/; |  |  |
| static constexpr openmode noreplace = /\* implementation defined \*/; |  | (since C++23) |
|  |  |  |

Specifies available file open flags. It is a BitmaskType, the following constants are defined:

|  |  |
| --- | --- |
| Constant | Explanation |
| ****app**** | seek to the end of stream before each write |
| ****binary**** | open in binary mode |
| ****in**** | open for reading |
| ****out**** | open for writing |
| ****trunc**** | discard the contents of the stream when opening |
| ****ate**** | seek to the end of stream immediately after open |
| ****noreplace**** (C++23) | open in exclusive mode |

### Example

Run this code

```
#include <fstream>
#include <iostream>
#include <string>
 
int main()
{
    const char* fname = "unique_name.txt";
 
    // write to a temporary stream object
    std::fstream(fname, std::ios::out | std::ios::trunc) << "Hi";
 
    std::string s;
    std::fstream(fname, std::ios::in) >> s;
    std::cout << s << '\n';
}

```

Output:

```
Hi

```

### See also

|  |  |
| --- | --- |
| open | opens a file and configures it as the associated character sequence   (public member function of `std::basic_filebuf<CharT,Traits>`) |
| (constructor) | constructs a `basic_stringbuf` object   (public member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/ios_base/openmode&oldid=155274>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 July 2023, at 17:43.