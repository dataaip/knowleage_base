# std::basic_ios<CharT,Traits>::copyfmt

From cppreference.com
< cpp‎ | io‎ | basic ios
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

std::basic_ios

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| basic_ios::basic_ios | | | | |
| basic_ios::~basic_ios | | | | |
| State functions | | | | |
| basic_ios::good | | | | |
| basic_ios::eof | | | | |
| basic_ios::fail | | | | |
| basic_ios::bad | | | | |
| basic_ios::operator! | | | | |
| basic_ios::operator bool | | | | |
| basic_ios::rdstate | | | | |
| basic_ios::setstate | | | | |
| basic_ios::clear | | | | |
| Formatting | | | | |
| ****basic_ios::copyfmt**** | | | | |
| basic_ios::fill | | | | |
| Miscellaneous | | | | |
| basic_ios::exceptions | | | | |
| basic_ios::imbue | | | | |
| basic_ios::rdbuf | | | | |
| basic_ios::tie | | | | |
| basic_ios::narrow | | | | |
| basic_ios::widen | | | | |
| Protected member functions | | | | |
| basic_ios::init | | | | |
| basic_ios::move(C++11) | | | | |
| basic_ios::swap(C++11) | | | | |
| basic_ios::set_rdbuf(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_ios& copyfmt( const basic_ios& other ); |  |  |
|  |  |  |

If other refers to the same object as \*this, has no effects. Otherwise, copies the state of the stream other into \*this. This is done in the following sequence:

1) Calls every callback registered by register_callback() passing erase_event as parameter.2) Copies all member objects from other to \*this except for rdstate(), the exception mask, and rdbuf(). In particular, makes copies of the locale, the formatting flags, the contents of the arrays std::ios_base::iword and std::ios_base::pword (but not the `iword` and `pword` pointers themselves), the callbacks, and the tied stream.3) Calls every callback registered by register_callback() passing copyfmt_event as parameter.4) Copies the exception mask from other to \*this as if by calling exceptions(other.exceptions()).

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another stream to use as source |

### Return value

\*this

### Notes

The second pass through the callbacks may be used to deep-copy the user-defined objects pointed to by the pointers in std::ios_base::pword.

`copyfmt()` may be used to save and restore the state of a stream. Boost provides a more fine-grained I/O state savers library for the same purpose.

### Example

Makes the std::ofstream object "out" behave exactly like std::cout, including formatting, `tie()` to std::cin, etc.

Run this code

```
#include <bitset>
#include <climits>
#include <fstream>
#include <iostream>
 
int main()
{
    std::ofstream out;
 
    out.copyfmt(std::cout); // copy everything except rdstate and rdbuf
    out.clear(std::cout.rdstate()); // copy rdstate
    out.basic_ios<char>::rdbuf(std::cout.rdbuf()); // share the buffer
 
    out << "Hello, world\n";
 
    auto bin = [](std::ios_base::fmtflags f)
    {
        return std::bitset<sizeof(std::ios_base::fmtflags) * CHAR_BIT>
            { static_cast<unsigned long long>(f) };
    };
    std::ofstream out2;
    std::cout << "1) out2.flags(): " << bin(out2.flags()) << '\n';
    std::cout << "2) cout.flags(): " << bin(std::cout.flags()) << '\n';
    std::cout.setf(std::ios::hex | std::ios::fixed | std::ios::boolalpha);
    std::cout << "3) cout.flags(): " << bin(std::cout.flags()) << '\n';
    out2.copyfmt(std::cout); // copy everything except rdstate and rdbuf
    std::cout << "4) out2.flags(): " << bin(out2.flags()) << '\n';
}

```

Possible output:

```
Hello, world
1) out2.flags(): 00000000000000000001000000000010
2) cout.flags(): 00000000000000000001000000000010
3) cout.flags(): 00000000000000000001000000001111
4) out2.flags(): 00000000000000000001000000001111

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 256 | C++98 | step 3 called the registered callbacks with the event type `copy_event`, which is not defined | corrected to copyfmt_event |
| LWG 292 | C++98 | if other refers to the same object as \*this, the member objects were still copied and the registered callbacks were still called | do nothing in this case |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ios/copyfmt&oldid=158804>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 September 2023, at 10:58.