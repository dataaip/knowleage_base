# std::basic_ospanstream<CharT,Traits>::span

From cppreference.com
< cpp‎ | io‎ | basic ospanstream
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

std::basic_ospanstream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| basic_ospanstream::basic_ospanstream(C++23) | | | | |
| basic_ospanstream::operator=(C++23) | | | | |
| basic_ospanstream::swap(C++23) | | | | |
| basic_ospanstream::rdbuf(C++23) | | | | |
| Underlying buffer operations | | | | |
| ****basic_ospanstream::span****(C++23) | | | | |
| Non-member functions | | | | |
| swap(std::basic_ospanstream)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| std::span<CharT> span() const noexcept; | (1) | (since C++23) |
| void span( std::span<CharT> s ) noexcept; | (2) | (since C++23) |
|  |  |  |

1) Gets a `span` referencing the written area if std::ios_base::out is set in the open mode of the wrapped std::basic_spanbuf, or a `span` referencing the underlying buffer otherwise.2) Makes the wrapped std::basic_spanbuf perform I/O on the buffer referenced by s.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | std::span referencing the storage to be use as the new underlying buffer of stream |

### Return value

1) A std::span referencing the underlying buffer or written area, depending on the open mode of the wrapped std::basic_spanbuf.2) (none)

### Example

Run this code

```
#include <cassert>
#include <iostream>
#include <span>
#include <spanstream>
 
int main()
{
    char out_buf[16];
    std::ospanstream ost{std::span<char>{out_buf}};
    ost << "C++" << ' ' << 23 << '\0'; // note explicit null-termination
    auto sp = ost.span();
    assert(
        sp[0] == 'C' && sp[1] == '+' && sp[2] == '+' &&
        sp[3] == ' ' && sp[4] == '2' && sp[5] == '3' &&
        sp[6] == '\0'
    );
    std::cout << "sp.data(): [" << sp.data() << "]\n";
    std::cout << "out_buf: [" << out_buf << "]\n";
    // spanstream uses out_buf as internal storage, no allocations
    assert(static_cast<char*>(out_buf) == sp.data());
 
    const char in_buf[] = "X Y 42";
    std::ispanstream ist{std::span<const char>{in_buf}};
    assert(static_cast<const char*>(in_buf) == ist.span().data());
    char c;
    ist >> c;
    assert(c == 'X');
    ist >> c;
    assert(c == 'Y');
    int i;
    ist >> i;
    assert(i == 42);
    ist >> i; // buffer is exhausted
    assert(!ist);
}

```

Output:

```
sp.data(): [C++ 23]
out_buf: [C++ 23]

```

### See also

|  |  |
| --- | --- |
| span | obtains or initializes an underlying buffer according to mode   (public member function of `std::basic_spanbuf<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ospanstream/span&oldid=130878>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 June 2021, at 08:57.