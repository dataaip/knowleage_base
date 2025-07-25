# std::istrstream::~istrstream

From cppreference.com
< cpp‎ | io‎ | istrstream
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

std::istrstream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| istrstream::istrstream | | | | |
| ****istrstream::~istrstream**** | | | | |
| istrstream::rdbuf | | | | |
| istrstream::str | | | | |

|  |  |  |
| --- | --- | --- |
| virtual ~istrstream(); |  | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

Destroys a `std::istrstream` object, which also destroys the member std::strstreambuf.

### Parameters

(none)

### Notes

The constructors of std::istrstream do not create the underlying std::strstreambuf in dynamically allocated mode, so the memory leaks that are possible with std::ostrstream::~ostrstream or std::strstream::~strstream do not apply.

### Example

Run this code

```
#include <iostream>
#include <strstream>
 
int main()
{
    {
        std::istrstream s("1.234");
        double d;
        s >> d;
        std::cout << d << '\n';
    } // destructor called
}

```

Output:

```
1.234

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/istrstream/%7Eistrstream&oldid=170637>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 05:41.