# std::istrstream::istrstream

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
| ****istrstream::istrstream**** | | | | |
| istrstream::~istrstream | | | | |
| istrstream::rdbuf | | | | |
| istrstream::str | | | | |

|  |  |  |
| --- | --- | --- |
| explicit istrstream( const char\* s ); | (1) | (deprecated in C++98)  (removed in C++26) |
| explicit istrstream( char\* s ); | (2) | (deprecated in C++98)  (removed in C++26) |
| istrstream( const char\* s, std::streamsize n ); | (3) | (deprecated in C++98)  (removed in C++26) |
| istrstream( char\* s, std::streamsize n ); | (4) | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

Constructs new std::istrstream and its underlying std::strstreambuf.

1,2) Constructs the underlying std::strstreambuf by calling strstreambuf(s, 0) and initializes the base class with the address of the `strstreambuf`. The behavior is undefined if s is not pointing at an element of a null-terminated array.3,4) Constructs the underlying std::strstreambuf by calling strstreambuf(s, n) and initializes the base class with the address of the `strstreambuf`. The behavior is undefined if s is not pointing at an element of an array whose length is at least n elements.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | C-string or char array to use as the contents of the stream |
| n | - | size of the array |

### Example

Run this code

```
#include <iostream>
#include <strstream>
 
int main()
{
    std::istrstream s1("1 2 3"); // string literal
    int n1, n2, n3;
    if (s1 >> n1 >> n2 >> n3)
        std::cout << n1 << ", " << n2 << ", " << n3 << '\n';
 
    char arr[] = {'4', ' ', '5', ' ', '6'};
    std::istrstream s2(arr, sizeof arr);
    if (s2 >> n1 >> n2 >> n3)
        std::cout << n1 << ", " << n2 << ", " << n3 << '\n';
}

```

Output:

```
1, 2, 3
4, 5, 6

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a `strstreambuf` object   (public member function of `std::strstreambuf`) |
| (constructor) | constructs an `ostrstream` object, optionally allocating the buffer   (public member function of `std::ostrstream`) |
| (constructor) | constructs a `strstream` object, optionally allocating the buffer   (public member function of `std::strstream`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/istrstream/istrstream&oldid=170636>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 05:39.