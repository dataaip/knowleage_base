# std::strstreambuf::freeze

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
| ****strstreambuf::freeze**** | | | | |
| strstreambuf::str | | | | |
| strstreambuf::pcount | | | | |
| Protected member functions | | | | |
| strstreambuf::underflow | | | | |
| strstreambuf::pbackfail | | | | |
| strstreambuf::overflow | | | | |
| strstreambuf::setbuf | | | | |
| strstreambuf::seekoff | | | | |
| strstreambuf::seekpos | | | | |

|  |  |  |
| --- | --- | --- |
| void freeze( bool freezefl = true ); |  | (deprecated in C++98)  (removed in C++26) |
|  |  |  |

If the buffer uses dynamic allocation, sets the frozen status of the stream to freezefl.

While the stream is frozen, overflow() will not reallocate the buffer and the `destructor` will not deallocate the buffer (thereby causing a memory leak).

### Parameters

|  |  |  |
| --- | --- | --- |
| freezefl | - | new value to set the freeze status to |

### Return value

(none)

### Notes

Every call to str() freezes the stream to preserve the validity of the pointer it returns. To allow the destructor to deallocate the buffer, freeze(false) needs to be called explicitly.

### Example

In this example, initial allocation of the underlying array was for 16 bytes.

Run this code

```
#include <iostream>
#include <strstream>
 
int main()
{
    {
        std::strstream dyn; // dynamically-allocated read/write buffer
        dyn << "Test: " << 1.23; // note: no std::ends to demonstrate append behavior
        std::cout << "dynamic buffer holds " << dyn.pcount() << " characters: '";
        std::cout.write(dyn.str(), dyn.pcount()) << "'\n";
        // the buffer is now frozen, further output will not make the buffer grow
        dyn << "more output, hopefully enough to run out of the allocated space"
            << std::ends;
        std::cout << "After more output, it holds "
                  << dyn.pcount() << " characters: '" << dyn.str() << "'\n";
        dyn.freeze(false); // unfreeze before destructor
    } // memory freed by the destructor
 
    {
        char arr[20];
        std::ostrstream st(arr, sizeof arr); // fixed-size buffer
        st << 1.23; // note: no std::ends to demonstrate append behavior
        std::cout << "static buffer holds "
                  << st.pcount() << " characters: '";
        std::cout.write(st.str(), st.pcount());
        std::cout << "'\n";
        st << "more output, hopefully enough to run out of the allocated space"
           << std::ends;
        std::cout << "static buffer holds "
                  << st.pcount() << " characters: '";
        std::cout.write(st.str(), st.pcount());
        std::cout << "'\n";
    } // nothing to deallocate, no need to unfreeze,
}

```

Output:

```
dynamic buffer holds 10 characters: 'Test: 1.23'
After more output, it holds 16 characters: 'Test: 1.23more o'
static buffer holds 4 characters: '1.23'
static buffer holds 20 characters: '1.23more output, hop'

```

### See also

|  |  |
| --- | --- |
| freeze | disables/enables automatic reallocation   (public member function of `std::strstream`) |
| freeze | disables/enables automatic reallocation   (public member function of `std::ostrstream`) |
| (destructor)[virtual] | destructs a `strstreambuf` object, optionally deallocating the character array   (virtual public member function) |
| overflow[virtual] | appends a character to the output sequence, may reallocate or initially allocate the buffer if dynamic and not frozen   (virtual protected member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/strstreambuf/freeze&oldid=170646>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 April 2024, at 06:27.