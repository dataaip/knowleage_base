# std::basic_ios<CharT,Traits>::good

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
| ****basic_ios::good**** | | | | |
| basic_ios::eof | | | | |
| basic_ios::fail | | | | |
| basic_ios::bad | | | | |
| basic_ios::operator! | | | | |
| basic_ios::operator bool | | | | |
| basic_ios::rdstate | | | | |
| basic_ios::setstate | | | | |
| basic_ios::clear | | | | |
| Formatting | | | | |
| basic_ios::copyfmt | | | | |
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
| bool good() const; |  |  |
|  |  |  |

Returns true if the most recent I/O operation on the stream completed successfully. Specifically, returns result of rdstate() == 0.

See ios_base::iostate for the list of conditions that set the stream status bits.

### Parameters

(none)

### Return value

true if the stream error flags are all false, false otherwise.

### Example

Run this code

```
#include <cstdlib>
#include <fstream>
#include <iostream>
 
int main()
{
    const char* fname = "/tmp/test.txt";
    std::ofstream ofile{fname};
    ofile << "10 " << "11 " << "12 " << "non-int";
    ofile.close();
 
    std::ifstream file{fname};
    if (!file.good())  
    {  
        std::cout << "#1. Opening file test.txt failed - "
                     "one of the error flags is true\n";
        return EXIT_FAILURE;
    }
 
    // typical C++ I/O loop uses the return value of the I/O function
    // as the loop controlling condition, operator bool() is used here
    for (int n; file >> n;)
        std::cout << n << ' ';
    std::cout << '\n';
 
    if (file.bad()) 
    {
        std::cout << "#2. I/O error while reading - badbit is true\n";
        return EXIT_FAILURE;
    } 
    else if (file.eof())
        std::cout << "#3. End of file reached successfully - eofbit is true\n"
            "This is fine even though file.good() is false\n"; 
    else if (file.fail())
        std::cout << "#4. Non-integer data encountered - failbit is true\n";
}

```

Possible output:

```
10 11 12 
#4. Non-integer data encountered - failbit is true

```

### See also

The following table shows the value of basic_ios accessors (****good()****, fail(), etc.) for all possible combinations of ios_base::iostate flags:

|  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ios_base::iostate flags | | | `basic_ios` accessors | | | | | |
| `eofbit` | `failbit` | `badbit` | ****good()**** | fail() | bad() | eof() | operator bool | operator! |
| false | false | false | true | false | false | false | true | false |
| false | false | true | false | true | true | false | false | true |
| false | true | false | false | true | false | false | false | true |
| false | true | true | false | true | true | false | false | true |
| true | false | false | false | false | false | true | true | false |
| true | false | true | false | true | true | true | false | true |
| true | true | false | false | true | false | true | false | true |
| true | true | true | false | true | true | true | false | true |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ios/good&oldid=158184>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 September 2023, at 01:59.