# std::ios_base::pword

From cppreference.com
< cpp‎ | io‎ | ios base
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

std::ios_base

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ios_base::ios_base | | | | |
| ios_base::~ios_base | | | | |
| ios_base::operator= | | | | |
| Formatting | | | | |
| ios_base::flags | | | | |
| ios_base::setf | | | | |
| ios_base::unsetf | | | | |
| ios_base::precision | | | | |
| ios_base::width | | | | |
| Locales | | | | |
| ios_base::imbue | | | | |
| ios_base::getloc | | | | |
| Internal extensible array | | | | |
| ios_base::xalloc | | | | |
| ios_base::iword | | | | |
| ****ios_base::pword**** | | | | |
| Miscellaneous | | | | |
| ios_base::register_callback | | | | |
| ios_base::sync_with_stdio | | | | |
| Member classes | | | | |
| ios_base::failure | | | | |
| ios_base::Init | | | | |
| Member types | | | | |
| ios_base::openmode | | | | |
| ios_base::fmtflags | | | | |
| ios_base::iostate | | | | |
| ios_base::seekdir | | | | |
| ios_base::event | | | | |
| ios_base::event_callback | | | | |

|  |  |  |
| --- | --- | --- |
| void\*& pword( int index ); |  |  |
|  |  |  |

First, allocates or resizes the private storage (dynamic array of void\* or another indexable data structure) sufficiently to make index a valid index, then returns a reference to the void\* element of the private storage with the index index.

The reference may be invalidated by any operation on this `ios_base` object, including another call to `pword()`, but the stored values are retained, so that reading from pword(index) with the same index later will produce the same value until the next call to std::basic_ios::copyfmt(). The value can be used for any purpose. The index of the element must be obtained by xalloc(), otherwise the behavior is undefined. New elements are initialized to a null pointer.

If the function fails (possibly caused by an allocation failure) and \*this is a base class subobject of a `basic_ios<>` object or subobject, calls std::basic_ios<>::setstate(badbit) which may throw std::ios_base::failure.

### Parameters

|  |  |  |
| --- | --- | --- |
| index | - | index value of the element |

### Return value

A reference to the element.

### Exceptions

May throw std::ios_base::failure when setting the badbit.

### Notes

If the pointers stored in `pword` require management, register_callback() may be used to install handlers that execute deep copy or deallocation as needed.

### Example

Uses base class pword storage for runtime type identification of derived stream objects.

Run this code

```
#include <iostream>
 
template<class CharT, class Traits = std::char_traits<CharT>>
class mystream : public std::basic_ostream<CharT, Traits>
{
public:
    static const int xindex;
 
    mystream(std::basic_ostream<CharT, Traits>& ostr) :
        std::basic_ostream<CharT, Traits>(ostr.rdbuf())
    {
        this->pword(xindex) = this;
    }
 
    void myfn()
    {
        *this << "[special handling for mystream]";
    }
};
 
// Each specialization of mystream obtains a unique index from xalloc()
template<class CharT, class Traits>
const int mystream<CharT, Traits>::xindex = std::ios_base::xalloc();
 
// This I/O manipulator will be able to recognize ostreams that are mystreams
// by looking up the pointer stored in pword
template<class CharT, class Traits>
std::basic_ostream<CharT, Traits>& mymanip(std::basic_ostream<CharT, Traits>& os)
{
    if (os.pword(mystream<CharT, Traits>::xindex) == &os)
        static_cast<mystream<CharT, Traits>&>(os).myfn();
    return os;
}
 
int main()
{
    std::cout << "cout, narrow-character test " << mymanip << '\n';
 
    mystream<char> myout(std::cout);
    myout << "myout, narrow-character test " << mymanip << '\n';
 
    std::wcout << "wcout, wide-character test " << mymanip << '\n';
 
    mystream<wchar_t> mywout(std::wcout);
    mywout << "mywout, wide-character test " << mymanip << '\n';
}

```

Output:

```
cout, narrow-character test
myout, narrow-character test [special handling for mystream]
wcout, wide-character test
mywout, wide-character test [special handling for mystream]

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 36 | C++98 | the stored value might not be retained if the reference is invalidated | the stored value is retained until the next call of `copyfmt()` |
| LWG 41 | C++98 | the function set badbit by itself on failure, but `ios_base` does not provide such interface | badbit is set by `basic_ios` (if \*this is its base class subobject) |

### See also

|  |  |
| --- | --- |
| iword | resizes the private storage if necessary and access to the long element at the given index   (public member function) |
| xalloc[static] | returns a program-wide unique integer that is safe to use as index to ****pword()**** and iword()   (public static member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/ios_base/pword&oldid=159117>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 September 2023, at 11:19.