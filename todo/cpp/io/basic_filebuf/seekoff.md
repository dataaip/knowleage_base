# std::basic_filebuf<CharT,Traits>::seekoff

From cppreference.com
< cpp‎ | io‎ | basic filebuf
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

std::basic_filebuf

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Public member functions | | | | |
| basic_filebuf::basic_filebuf | | | | |
| basic_filebuf::~basic_filebuf | | | | |
| basic_filebuf::operator=(C++11) | | | | |
| basic_filebuf::swap(C++11) | | | | |
| basic_filebuf::native_handle(C++26) | | | | |
| basic_filebuf::is_open | | | | |
| basic_filebuf::open | | | | |
| basic_filebuf::close | | | | |
| Protected member functions | | | | |
| basic_filebuf::showmanyc | | | | |
| basic_filebuf::underflow | | | | |
| basic_filebuf::uflow | | | | |
| basic_filebuf::pbackfail | | | | |
| basic_filebuf::overflow | | | | |
| basic_filebuf::setbuf | | | | |
| ****basic_filebuf::seekoff**** | | | | |
| basic_filebuf::seekpos | | | | |
| basic_filebuf::sync | | | | |
| basic_filebuf::imbue | | | | |
| Non-member functions | | | | |
| swap(std::basic_filebuf)(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| protected:  virtual pos_type seekoff( off_type off,                            std::ios_base::seekdir dir, std::ios_base::openmode which = std::ios_base::in | std::ios_base::out ); |  |  |
|  |  |  |

Repositions the file pointer, if possible, to the position that corresponds to exactly off characters from beginning, end, or current position of the file (depending on the value of dir).

If the associated file is not open (is_open() == false), fails immediately.

If the multibyte character encoding is state-dependent (codecvt::encoding() returned -1) or variable-length (`codecvt::encoding()` returned ​0​) and the offset off is not ​0​, fails immediately: this function cannot determine the number of bytes that correspond to off characters.

If dir is not std::basic_ios::cur or the offset off is not ​0​, and the most recent operation done on this filebuf object was output (that is, either the put buffer is not empty, or the most recently called function was overflow()), then calls std::codecvt::unshift to determine the unshift sequence necessary, and writes that sequence to the file by calling overflow().

Then converts the argument dir to a value whence of type int as follows:

|  |  |
| --- | --- |
| value of dir | value of whence |
| std::basic_ios::beg | SEEK_SET |
| std::basic_ios::end | SEEK_END |
| std::basic_ios::cur | SEEK_CUR |

Then, if the character encoding is fixed-width (`codecvt::encoding()` returns some positive number width), moves the file pointer as if by std::fseek(file, width\*off, whence).

Otherwise, moves the file pointer as if by std::fseek(file, 0, whence).

The `openmode` argument, required by the base class function signature, is usually ignored, because `std::basic_filebuf` maintains only one file position.

### Parameters

|  |  |  |
| --- | --- | --- |
| off | - | relative position to set the position indicator to |
| dir | - | defines base position to apply the relative offset to. It can be one of the following constants:  |  |  | | --- | --- | | Constant | Explanation | | beg | the beginning of a stream | | end | the ending of a stream | | cur | the current position of stream position indicator | |
| which | - | defines which of the input and/or output sequences to affect. It can be one or a combination of the following constants:  |  |  | | --- | --- | | Constant | Explanation | | in | affect the input sequence | | out | affect the output sequence | |

### Return value

A newly constructed object of type pos_type which stores the resulting file position, or pos_type(off_type(-1)) on failure.

### Notes

`seekoff()` is called by std::basic_streambuf::pubseekoff, which is called by std::basic_istream::seekg, std::basic_ostream::seekp, std::basic_istream::tellg, and std::basic_ostream::tellp.

### Example

Run this code

```
#include <fstream>
#include <iostream>
#include <locale>
 
template<typename CharT>
int get_encoding(const std::basic_istream<CharT>& stream)
{
    using Facet = std::codecvt<CharT, char, std::mbstate_t>;
    return std::use_facet<Facet>(stream.getloc()).encoding();
}
 
int main()
{
    // prepare a 10-byte file holding 4 characters ("zß水𝄋") in UTF-8
    std::ofstream("text.txt") << "\x7a\xc3\x9f\xe6\xb0\xb4\xf0\x9d\x84\x8b";
 
    // open using a non-converting encoding
    std::ifstream f1("text.txt");
    std::cout << "f1's locale's encoding() returns "
              << get_encoding(f1) << '\n'
              << "pubseekoff(3, beg) returns "
              << f1.rdbuf()->pubseekoff(3, std::ios_base::beg) << '\n'
              << "pubseekoff(0, end) returns "
              << f1.rdbuf()->pubseekoff(0, std::ios_base::end) << '\n';
 
    // open using UTF-8
    std::wifstream f2("text.txt");
    f2.imbue(std::locale("en_US.UTF-8"));
    std::cout << "f2's locale's encoding() returns "
              << get_encoding(f2) << '\n'
              << "pubseekoff(3, beg) returns "
              << f2.rdbuf()->pubseekoff(3, std::ios_base::beg) << '\n'
              << "pubseekoff(0, end) returns "
              << f2.rdbuf()->pubseekoff(0, std::ios_base::end) << '\n';
}

```

Output:

```
f1's locale's encoding() returns 1
pubseekoff(3, beg) returns 3
pubseekoff(0, end) returns 10
f2's locale's encoding() returns 0
pubseekoff(3, beg) returns -1
pubseekoff(0, end) returns 10

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 55 | C++98 | `seekoff` returned an undefined invalid stream position on failure | pos_type(off_type(-1)) is returned on failure |

### See also

|  |  |
| --- | --- |
| pubseekoff | invokes seekoff()   (public member function of `std::basic_streambuf<CharT,Traits>`) |
| seekpos[virtual] | repositions the file position, using absolute addressing   (virtual protected member function) |
| fseek | moves the file position indicator to a specific location in a file   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_filebuf/seekoff&oldid=158142>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 September 2023, at 22:45.