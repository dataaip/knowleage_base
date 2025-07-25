# std::basic_osyncstream<CharT,Traits,Allocator>::basic_osyncstream

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
| ****basic_osyncstream::basic_osyncstream****(C++20) | | | | |
| basic_osyncstream::operator=(C++20) | | | | |
| basic_osyncstream::~basic_osyncstream(C++20) | | | | |
| basic_osyncstream::rdbuf(C++20) | | | | |
| basic_osyncstream::get_wrapped(C++20) | | | | |
| basic_osyncstream::emit(C++20) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_osyncstream( streambuf_type\* buf, const Allocator& a ); | (1) |  |
| explicit basic_osyncstream( streambuf_type\* buf ); | (2) |  |
| basic_osyncstream( std::basic_ostream<CharT, Traits>& os, const Allocator& a ); | (3) |  |
| explicit basic_osyncstream( std::basic_ostream<CharT, Traits>& os ); | (4) |  |
| basic_osyncstream( std::basic_osyncstream&& other ) noexcept; | (5) |  |
|  |  |  |

Constructs new synchronized output stream.

1-4) Constructs the private member std::basic_syncbuf using the buffer and the allocator provided, and initializes the base class with a pointer to the member std::basic_streambuf.5) Move constructor. Move-constructs the std::basic_ostream base and the std::basic_syncbuf member from the corresponding subobjects of other, then calls set_rdbuf with the pointer to the newly-constructed underlying std::basic_syncbuf to complete the initialization of the base. After this move constructor, other.get_wrapped() returns nullptr and destruction of other produces no output.

### Parameters

|  |  |  |
| --- | --- | --- |
| buf | - | pointer to the std::basic_streambuf that will be wrapped |
| os | - | reference to a std::basic_ostream, whose rdbuf() will be wrapped |
| a | - | the allocator to pass to the constructor of the member std::basic_syncbuf |
| other | - | another osyncstream to move from |

### Example

Run this code

```
#include <iostream>
#include <string_view>
#include <syncstream>
#include <thread>
 
void worker(const int id, std::ostream &os)
{
    std::string_view block;
    switch (id)
    {
        default: [[fallthrough]];
        case 0: block = "██";
                break;
        case 1: block = "▓▓";
                break;
        case 2: block = "▒▒";
                break;
        case 3: block = "░░";
                break;
    }
    for (int i = 1; i <= 50; ++i)
        os << block << std::flush;
    os << std::endl;
}
 
int main()
{
    std::cout << "Synchronized output should not cause any interference:" << std::endl;
    {
        auto scout1 = std::osyncstream{std::cout};
        auto scout2 = std::osyncstream{std::cout};
        auto scout3 = std::osyncstream{std::cout};
        auto scout4 = std::osyncstream{std::cout};
        auto w1 = std::jthread{worker, 0, std::ref(scout1)};
        auto w2 = std::jthread{worker, 1, std::ref(scout2)};
        auto w3 = std::jthread{worker, 2, std::ref(scout3)};
        auto w4 = std::jthread{worker, 3, std::ref(scout4)};
    }
 
    std::cout << "\nLack of synchronization may cause some interference on output:"
              << std::endl;
    {
        auto w1 = std::jthread{worker, 0, std::ref(std::cout)};
        auto w2 = std::jthread{worker, 1, std::ref(std::cout)};
        auto w3 = std::jthread{worker, 2, std::ref(std::cout)};
        auto w4 = std::jthread{worker, 3, std::ref(std::cout)};
    }
}

```

Possible output:

```
Synchronized output should not cause any interference:
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓
████████████████████████████████████████████████████████████████████████████████████████████████████
 
Lack of synchronization may cause some interference on output:
████▓▓██▒▒▒▒▓▓██░░▒▒██░░▒▒░░░░▒▒░░▓▓▒▒██░░████████████▓▓██████▓▓▒▒▓▓██░░████▓▓▓▓██▒▒░░░░░░░░▓▓░░▓▓██▒▒▒▒▒▒▒▒▓▓██▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒░░▒▒▒▒░░▒▒▒▒▒▒▒▒▒▒▓▓▒▒▒▒▒▒▒▒▒▒▒▒██░░░░░░░░▓▓▓▓▓▓▓▓▓▓▓▓▓▓░░▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓████████▓▓▓▓▓▓▓▓▓▓▓▓░░▓▓▓▓
▒▒▒▒██░░██████████████████████████░░░░░░░░░░░░░░██░░▒▒░░░░░░██████████████████
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒░░▒▒░░░░░░░░░░░░░░░░░░░░░░░░░░░░▒▒▒▒▒▒
░░░░░░

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a `basic_syncbuf` object   (public member function of `std::basic_syncbuf<CharT,Traits,Allocator>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_osyncstream/basic_osyncstream&oldid=158552>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 September 2023, at 09:09.