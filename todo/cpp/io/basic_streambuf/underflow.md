# std::basic_streambuf<CharT,Traits>::underflow

From cppreference.com
< cpp‎ | io‎ | basic streambuf
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

std::basic_streambuf

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Public member functions | | | | | | basic_streambuf::~basic_streambuf | | | | | | Locales | | | | | | basic_streambuf::pubimbue | | | | | | basic_streambuf::getloc | | | | | | Positioning | | | | | | basic_streambuf::pubsetbuf | | | | | | basic_streambuf::pubseekoff | | | | | | basic_streambuf::pubseekpos | | | | | | basic_streambuf::pubsync | | | | | | Get area | | | | | | basic_streambuf::in_avail | | | | | | basic_streambuf::snextc | | | | | | basic_streambuf::sbumpc | | | | | | basic_streambuf::sgetc | | | | | | basic_streambuf::sgetn | | | | | | Put area | | | | | | basic_streambuf::sputc | | | | | | basic_streambuf::sputn | | | | | | Putback | | | | | | basic_streambuf::sputbackc | | | | | | basic_streambuf::sungetc | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Protected member functions | | | | | | basic_streambuf::basic_streambuf | | | | | | basic_streambuf::operator=(C++11) | | | | | | basic_streambuf::swap(C++11) | | | | | | Locales | | | | | | basic_streambuf::imbue | | | | | | Positioning | | | | | | basic_streambuf::setbuf | | | | | | basic_streambuf::seekoff | | | | | | basic_streambuf::seekpos | | | | | | basic_streambuf::sync | | | | | | Get area | | | | | | basic_streambuf::showmanyc | | | | | | ****basic_streambuf::underflow**** | | | | | | basic_streambuf::uflow | | | | | | basic_streambuf::xsgetn | | | | | | basic_streambuf::ebackbasic_streambuf::gptrbasic_streambuf::egptr | | | | | | basic_streambuf::gbump | | | | | | basic_streambuf::setg | | | | | | Put area | | | | | | basic_streambuf::xsputn | | | | | | basic_streambuf::overflow | | | | | | basic_streambuf::pbasebasic_streambuf::pptrbasic_streambuf::epptr | | | | | | basic_streambuf::pbump | | | | | | basic_streambuf::setp | | | | | | Putback | | | | | | basic_streambuf::pbackfail | | | | | |

|  |  |  |
| --- | --- | --- |
| protected:  virtual int_type underflow(); |  |  |
|  |  |  |

Ensures that at least one character is available in the input area by updating the pointers to the input area (if needed) and reading more data in from the input sequence (if applicable). Returns the value of that character (converted to `int_type` with Traits::to_int_type(c)) on success or Traits::eof() on failure.

The function may update `gptr`, `egptr` and `eback` pointers to define the location of newly loaded data (if any). On failure, the function ensures that either gptr() == nullptr or gptr() == egptr.

The base class version of the function does nothing. The derived classes may override this function to allow updates to the get area in the case of exhaustion.

### Parameters

(none)

### Return value

The value of the character pointed to by the **get pointer** after the call on success, or Traits::eof() otherwise.

The base class version of the function returns traits::eof().

### Note

The public functions of std::streambuf call this function only if gptr() == nullptr or gptr() >= egptr().

### Example

Run this code

```
#include <iostream>
#include <sstream>
 
class null_filter_buf : public std::streambuf
{
    std::streambuf* src;
    char ch; // single-byte buffer
protected:
    int underflow()
    {
        traits_type::int_type i;
        while ((i = src->sbumpc()) == '\0')
            ; // skip zeroes
        if (!traits_type::eq_int_type(i, traits_type::eof()))
        {
            ch = traits_type::to_char_type(i);
            setg(&ch, &ch, &ch+1); // make one read position available
        }
        return i;
    }
public:
    null_filter_buf(std::streambuf* buf) : src(buf)
    {
        setg(&ch, &ch + 1, &ch + 1); // buffer is initially full
    }
};
 
void filtered_read(std::istream& in)
{
    std::streambuf* orig = in.rdbuf();
    null_filter_buf buf(orig);
    in.rdbuf(&buf);
    for (char c; in.get(c);)
        std::cout << c;
    in.rdbuf(orig);
}
 
int main()
{
    char a[] = "This i\0s \0an e\0\0\0xample";
    std::istringstream in(std::string(std::begin(a), std::end(a)));
    filtered_read(in);
}

```

Output:

```
This is an example

```

### See also

|  |  |
| --- | --- |
| uflow[virtual] | reads characters from the associated input sequence to the get area and advances the next pointer   (virtual protected member function) |
| overflow[virtual] | writes characters to the associated output sequence from the put area   (virtual protected member function) |
| underflow[virtual] | reads from the associated file   (virtual protected member function of `std::basic_filebuf<CharT,Traits>`) |
| underflow[virtual] | returns the next character available in the input sequence   (virtual protected member function of `std::basic_stringbuf<CharT,Traits,Allocator>`) |
| underflow[virtual] | reads a character from the input sequence without advancing the next pointer   (virtual protected member function of `std::strstreambuf`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_streambuf/underflow&oldid=124722>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 December 2020, at 18:41.