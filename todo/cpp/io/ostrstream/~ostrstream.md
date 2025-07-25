# std::ostrstream::~ostrstream

From cppreference.com
< cpp‎ | io‎ | ostrstream
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

std::ostrstream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ostrstream::ostrstream | | | | |
| ****ostrstream::~ostrstream**** | | | | |
| ostrstream::rdbuf | | | | |
| ostrstream::str | | | | |
| ostrstream::freeze | | | | |
| ostrstream::pcount | | | | |

|  |  |  |
| --- | --- | --- |
| virtual ~ostrstream(); |  | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

Destroys a std::ostrstream object, which also destroys the member std::strstreambuf, which may call the deallocation function if the underlying buffer was dynamically-allocated and not frozen.

### Parameters

(none)

### Notes

If str() was called on a dynamic `ostrstream` and `freeze(false)` was not called after that, this destructor leaks memory.

### Example

Run this code

```
#include <iostream>
#include <strstream>
 
int main()
{
    {
        std::ostrstream s; // dynamic buffer 
        s << 1.23;
        std::cout << s.str() << '\n';
        s.freeze(false);
    } // destructor called, buffer deallocated 
 
    {
        std::ostrstream s;
        s << 1.23;
        std::cout << s.str() << '\n';
//      buf.freeze(false);
    } // destructor called, memory leaked
}

```

Output:

```
1.23
1.23

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/ostrstream/%7Eostrstream&oldid=170640>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 05:54.