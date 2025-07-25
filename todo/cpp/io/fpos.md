# std::fpos

From cppreference.com
< cpp‎ | io
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
| ****fpos**** | | | | |
| Error category interface | | | | |
| iostream_category(C++11) | | | | |
| io_errc(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ios>` |  |  |
| template< class State >  class fpos; |  |  |
|  |  |  |

Specializations of the class template `std::fpos` identify absolute positions in a stream or in a file. Each object of type `fpos` holds the byte position in the stream (typically as a private member of type std::streamoff) and the current shift state, a value of type `State` (typically std::mbstate_t).

The following typedef names for std::fpos<std::mbstate_t> are provided (although they are spelled differently in the standard, they denote the same type):

|  |  |
| --- | --- |
| Defined in header `<iosfwd>` | |
| Type | Definition |
| `std::streampos` | std::fpos<std::char_traits<char>::state_type> |
| `std::wstreampos` | std::fpos<std::char_traits<wchar_t>::state_type> |
| `std::u8streampos`(C++20) | std::fpos<std::char_traits<char8_t>::state_type> |
| `std::u16streampos` (C++11) | std::fpos<std::char_traits<char16_t>::state_type> |
| `std::u32streampos` (C++11) | std::fpos<std::char_traits<char32_t>::state_type> |

All specializations of `fpos` meet the DefaultConstructible, CopyConstructible, CopyAssignable, Destructible, and EqualityComparable requirements.

If `State` is trivially copy constructible, `fpos` has a trivial copy constructor.
If `State` is trivially copy assignable, `fpos` has a trivial copy assignment operator.
If `State` is trivially destructible, `fpos` has a trivial destructor.

### Template parameter

|  |  |  |
| --- | --- | --- |
| State | - | the type representing the shift state |
| Type requirements | | |
| -`State` must meet the requirements of Destructible, CopyAssignable, CopyConstructible and DefaultConstructible. | | |

### Member functions

|  |  |
| --- | --- |
| state | gets/sets the value of the shift state   (public member function) |

In addition, member and non-member functions are provided to support the following operations:

- A default constructor that stores an offset of zero and value-initializes the state object.

- A non-explicit constructor that accepts an argument of type (possibly const) std::streamoff, which stores that offset and value-initializes the state object. This constructor must also accept the special value std::streamoff(-1): the `std::fpos` constructed in this manner is returned by some stream operations to indicate errors.

- Explicit conversion from (possibly const) `fpos` to std::streamoff. The result is the stored offset.

- operator== and operator!= that compare two objects of type (possibly const) `std::fpos` and return a bool prvalue. p != q is equivalent to !(p == q).

- operator+ and operator- such that, for an object p of type (possibly const) `fpos<State>` and an object o of type (possibly const) std::streamoff

:   - p + o has type `fpos<State>` and stores an offset that is the result of adding o to the offset of p.
    - o + p has a type convertible to `fpos<State>` and the result of the conversion is equal to p + o.
    - p - o has type `fpos<State>` and stores an offset that is the result of subtracting o from the offset of p.

- operator+= and operator-= which can accept a (possibly const) std::streamoff and adds/subtracts it from the stored offset, respectively.

- operator- which can subtract two objects of type (possibly const) `std::fpos` producing an std::streamoff, such that for two such objects p and q, p == q + (p - q).

### Notes

Some of the I/O streams member functions return and manipulate objects of member typedef `pos_type`. For streams, these member typedefs are provided by the template parameter `Traits`, which defaults to std::char_traits, which define their `pos_type`s to be specializations of `std::fpos`. The behavior of the I/O streams library is implementation-defined when `Traits::pos_type` is not std::fpos<std::mbstate_t> (aka `std::streampos`, `std::wstreampos`, etc.).

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 57 | C++98 | `streampos` and `wstreampos` were contradictionally allowed to be different while required to be the same | clarified to be the same |
| P0759R1 | C++98 | specification was unclear and incomplete | cleaned up |
| P1148R0 | C++11 | unclear what and in which header the definitions `u16streampos` and `u32streampos` are | made clear |
| LWG 2114 (P2167R3) | C++98 | non-bool return types of equality comparisons were allowed | disallowed |

### See also

|  |  |
| --- | --- |
| streamoff | represents relative file/stream position (offset from fpos), sufficient to represent any file size   (typedef) |
| tellp | returns the output position indicator   (public member function of `std::basic_ostream<CharT,Traits>`) |
| seekp | sets the output position indicator   (public member function of `std::basic_ostream<CharT,Traits>`) |
| fgetpos | gets the file position indicator   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/fpos&oldid=175940>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 September 2024, at 23:07.