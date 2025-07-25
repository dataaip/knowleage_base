# std::basic_osyncstream<CharT,Traits,Allocator>::operator=

From cppreference.com
< cpp‎ | io‎ | basic osyncstream
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

std::basic_osyncstream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| basic_osyncstream::basic_osyncstream(C++20) | | | | |
| ****basic_osyncstream::operator=****(C++20) | | | | |
| basic_osyncstream::~basic_osyncstream(C++20) | | | | |
| basic_osyncstream::rdbuf(C++20) | | | | |
| basic_osyncstream::get_wrapped(C++20) | | | | |
| basic_osyncstream::emit(C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_osyncstream& operator=( std::basic_osyncstream&& other ); |  | (since C++20) |
|  |  |  |

Move-assigns a synchronized output stream:

Move-assigns the wrapped std::basic_syncbuf from the corresponding member of other (after this move-assignment, other.get_wrapped() returns a null pointer and destruction of other produces no output; any pending buffered output will be emitted) and move-assigns the base std::basic_ostream (this swaps all stream state variables except for `rdbuf` between \*this and other)

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another synchronized output stream to move from |

### Return value

\*this

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <sstream>
#include <syncstream>
#include <utility>
 
int main()
{
    std::osyncstream out(std::cout);
    out << "test\n";
    std::ostringstream str_out;
    std::osyncstream{str_out} = std::move(out); // Note that out is emitted here
    std::cout << "str_out = " << std::quoted(str_out.view()) << '\n';
}

```

Output:

```
test
str_out = ""

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3867 | C++20 | the move assignment operator was noexcept, but std::basic_syncbuf's move assignment operator is not | removed noexcept |

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_osyncstream` object   (public member function) |
| (destructor) | destroys the `basic_osyncstream` and emits its internal buffer   (public member function) |
| emit | calls emit() on the underlying `basic_syncbuf` to transmit its internal data to the final destination   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_osyncstream/operator%3D&oldid=157268>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 August 2023, at 04:26.