# std::basic_stringbuf<CharT,Traits,Allocator>::basic_stringbuf

From cppreference.com
< cpp‎ | io‎ | basic stringbuf
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

std::basic_stringbuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| ****basic_stringbuf::basic_stringbuf**** | | | | |
| basic_stringbuf::operator=(C++11) | | | | |
| basic_stringbuf::swap(C++11) | | | | |
| basic_stringbuf::str | | | | |
| basic_stringbuf::get_allocator(C++20) | | | | |
| basic_stringbuf::view(C++20) | | | | |
| Protected member functions | | | | |
| basic_stringbuf::underflow | | | | |
| basic_stringbuf::pbackfail | | | | |
| basic_stringbuf::overflow | | | | |
| basic_stringbuf::setbuf | | | | |
| basic_stringbuf::seekoff | | | | |
| basic_stringbuf::seekpos | | | | |
| Non-member functions | | | | |
| swap(std::basic_stringbuf)(C++11) | | | | |
| Exposition-only member functions | | | | |
| basic_stringbuf::**init_buf_ptrs** | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| explicit basic_stringbuf( std::ios_base::openmode which =                                std::ios_base::in | std::ios_base::out ); |  | (until C++11) |
| explicit basic_stringbuf( std::ios_base::openmode which ); |  | (since C++11) |
|  |  |  |
| --- | --- | --- |
| basic_stringbuf()      : basic_stringbuf( std::ios_base::in | std::ios_base::out ) {} | (2) | (since C++11) |
| explicit      basic_stringbuf( const std::basic_string<CharT, Traits, Allocator>& s,                       std::ios_base::openmode which = std::ios_base::in | std::ios_base::out ); | (3) |  |
| explicit basic_stringbuf( std::basic_string<CharT, Traits, Allocator>&& s,  std::ios_base::openmode which = std::ios_base::in | std::ios_base::out ); | (4) | (since C++20) |
| basic_stringbuf( std::ios_base::openmode which, const Allocator& a ); | (5) | (since C++20) |
| explicit basic_stringbuf( const Allocator& a )      : basic_stringbuf( std::ios_base::in | std::ios_base::out, a ) {} | (6) | (since C++20) |
| template< class SAlloc >  explicit basic_stringbuf( const std::basic_string<CharT, Traits, SAlloc>& s,                            std::ios_base::openmode which = std::ios_base::in | std::ios_base::out ); | (7) | (since C++20) |
| template< class SAlloc >  basic_stringbuf( const std::basic_string<CharT, Traits, SAlloc>& s, std::ios_base::openmode which, const Allocator& a ); | (8) | (since C++20) |
| template< class SAlloc >  basic_stringbuf( const std::basic_string<CharT, Traits, SAlloc>& s,                   const Allocator& a ) : basic_stringbuf( s, std::ios_base::in | std::ios_base::out, a ) {} | (9) | (since C++20) |
| template< class StringViewLike >  explicit basic_stringbuf( const StringViewLike& t,                            std::ios_base::openmode which = std::ios_base::in | std::ios_base::out ); | (10) | (since C++26) |
| template< class StringViewLike >  basic_stringbuf( const StringViewLike& t, std::ios_base::openmode which, const Allocator& a ); | (11) | (since C++26) |
| template< class StringViewLike >  basic_stringbuf( const StringViewLike& t, const Allocator& a ); | (12) | (since C++26) |
| basic_stringbuf( basic_stringbuf&& rhs ); | (13) | (since C++11) |
| basic_stringbuf( basic_stringbuf&& rhs, const Allocator& a ); | (14) | (since C++20) |
| basic_stringbuf( const basic_stringbuf& rhs ) = delete; | (15) | (since C++11) |
|  |  |  |

The std::basic_streambuf base and the exposition-only data members `buf` and `mode` are initialized as follows.

After initializing these subobjects, overloads (3-12) initialize the input and output sequences as if by calling `init_buf_ptrs()`.

| Overload | std::basic_streambuf base | `buf` | `mode` |
| --- | --- | --- | --- |
| (1) | default-initialized | implementation-defined (see below) | which |
| (2) | std::ios_base::in |     std::ios_base::out |
| (3) | s | which |
| (4) | std::move(s) |
| (5) | a |
| (6) | std::ios_base::in |     std::ios_base::out |
| (7) | s | which |
| (8) | {s, a} |
| (9) | std::ios_base::in |     std::ios_base::out |
| (10) | {sv, Allocator()} | which |
| (11) | {sv, a} |
| (12) | std::ios_base::in |     std::ios_base::out |
| (13) | rhs (copy constructed) | std::move(rhs).str() | rhs.mode |
| (14) | {std::move(rhs).str(), a} |

1,2) Overload (1)(until C++11)(2)(since C++11) is the default constructor. It is implementation-defined whether the sequence pointers (eback(), gptr(), egptr(), pbase(), pptr(), epptr()) are initialized to null pointers.5,6) When the construction is complete, str.empty() is true.7) This overload participates in overload resolution only if std::is_same_v<SAlloc, Allocator> is false.10-12) Implicitly converts t to a string view sv as if by std::basic_string_view<CharT, Traits> sv = t;, then it is used as above in the table. These overloads participate in overload resolution only if std::is_convertible_v<const StringViewLike&,  
                      std::basic_string_view<CharT, Traits>> is true.13,14) Overload (13) is the move constructor. It is implementation-defined whether the six sequence pointers in \*this obtain the values which rhs had. When the construction is complete, rhs is empty but usable, and

- Let rhs_p refer to the state of rhs just prior to this construction, the following expressions will evaluate to true:

:   - str() == rhs_p.str()
    - getloc() == rhs_p.getloc()
    - gptr() - eback() == rhs_p.gptr() - rhs_p.eback()
    - egptr() - eback() == rhs_p.egptr() - rhs_p.eback()
    - pptr() - pbase() == rhs_p.pptr() - rhs_p.pbase()
    - epptr() - pbase() == rhs_p.epptr() - rhs_p.pbase()

- Let rhs_a refer to the state of rhs just after this construction, the following expressions will evaluate to true:

:   - !eback() || eback() != rhs_a.eback()
    - !gptr() || gptr() != rhs_a.gptr()
    - !egptr() || egptr() != rhs_a.egptr()
    - !pbase() || pbase() != rhs_a.pbase()
    - !pptr() || pptr() != rhs_a.pptr()
    - !epptr() || epptr() != rhs_a.epptr()

15) The copy constructor is deleted; `std::basic_stringbuf` is not CopyConstructible.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | a std::basic_string used to initialize the buffer |
| t | - | an object (convertible to std::basic_string_view) used to initialize the buffer |
| a | - | another allocator used to construct the internal std::basic_string |
| rhs | - | another `basic_stringbuf` |
| which | - | specifies stream open mode. It is bitmask type, the following constants are defined:  |  |  | | --- | --- | | Constant | Explanation | | app | seek to the end of stream before each write | | binary | open in binary mode | | in | open for reading | | out | open for writing | | trunc | discard the contents of the stream when opening | | ate | seek to the end of stream immediately after open | | noreplace (C++23) | open in exclusive mode | |

### Notes

Typically called by the constructor of std::basic_stringstream.

The level of support for the open modes other than std::ios_base::in and std::ios_base::out varies among implementations. C++11 explicitly specifies the support for std::ios_base::ate in str() and in this constructor, but std::ios_base::app, std::ios_base::trunc, and std::ios_base::binary have different effects on different implementations.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_sstream_from_string_view` | `202306L` | (C++26) | Interfacing string streams with std::string_view |

### Example

Demonstrates calling the constructor of `std::basic_stringbuf` directly:

Run this code

```
#include <iostream>
#include <sstream>
 
int main()
{
    // default constructor (mode = in | out)
    std::stringbuf buf1;
    buf1.sputc('1');
    std::cout << &buf1 << '\n';
 
    // string constructor in at-end mode (C++11)
    std::stringbuf buf2("test", std::ios_base::in
                              | std::ios_base::out
                              | std::ios_base::ate);
    buf2.sputc('1');
    std::cout << &buf2 << '\n';
 
    // append mode test (results differ among compilers)
    std::stringbuf buf3("test", std::ios_base::in
                              | std::ios_base::out
                              | std::ios_base::app);
    buf3.sputc('1');
    buf3.pubseekpos(1);
    buf3.sputc('2');
    std::cout << &buf3 << '\n';
}

```

Output:

```
1
test1
est12 (Sun Studio) 2st1 (GCC)

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 432 | C++98 | 1. overload (1) allocated no array object 2. overload (3) did not specify how the input     and output sequences are initialized | 1. removed the limitation 2. specified |
| LWG 562 | C++98 | overload (3) set epptr() to point one past the last underlying character if bool(which & std::ios_base::out) == true | epptr() can be set beyond that position |
| P0935R0 | C++11 | the default constructor was explicit | made implicit |

### See also

|  |  |
| --- | --- |
| (constructor) | constructs the string stream   (public member function of `std::basic_stringstream<CharT,Traits,Allocator>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_stringbuf/basic_stringbuf&oldid=158136>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 September 2023, at 18:36.