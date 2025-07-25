# std::basic_istream<CharT,Traits>::readsome

From cppreference.com
< cpp‎ | io‎ | basic istream
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

std::basic_istream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Global objects | | | | |
| cinwcin | | | | |
| Member functions | | | | |
| basic_istream::basic_istream | | | | |
| basic_istream::~basic_istream | | | | |
| basic_istream::operator=(C++11) | | | | |
| Formatted input | | | | |
| basic_istream::operator>> | | | | |
| Unformatted input | | | | |
| basic_istream::get | | | | |
| basic_istream::peek | | | | |
| basic_istream::unget | | | | |
| basic_istream::putback | | | | |
| basic_istream::getline | | | | |
| basic_istream::ignore | | | | |
| basic_istream::read | | | | |
| ****basic_istream::readsome**** | | | | |
| basic_istream::gcount | | | | |
| Positioning | | | | |
| basic_istream::tellg | | | | |
| basic_istream::seekg | | | | |
| Miscellaneous | | | | |
| basic_istream::sync | | | | |
| basic_istream::swap(C++11) | | | | |
| Member classes | | | | |
| basic_istream::sentry | | | | |
| Non-member functions | | | | |
| operator>>(std::basic_istream) | | | | |

|  |  |  |
| --- | --- | --- |
| std::streamsize readsome( char_type\* s, std::streamsize count ); |  |  |
|  |  |  |

Extracts up to count immediately available characters from the input stream. The extracted characters are stored into the character array pointed to by s.

Behaves as UnformattedInputFunction. After constructing and checking the sentry object,

- If rdbuf()->in_avail() == -1, calls setstate(eofbit) and extracts no characters.

- If rdbuf()->in_avail() == 0, extracts no characters.

- If rdbuf()->in_avail() > 0, extracts std::min(rdbuf()->in_avail(), count) characters and stores them into successive locations of the character array whose first element is pointed to by s.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to the character array to store the characters to |
| count | - | maximum number of characters to read |

### Return value

The number of characters actually extracted.

### Exceptions

failure if an error occurred (the error state flag is not goodbit) and exceptions() is set to throw for that state.

If an internal operation throws an exception, it is caught and badbit is set. If exceptions() is set for `badbit`, the exception is rethrown.

### Notes

The behavior of this function is highly implementation-specific. For example, using `readsome()` with std::ifstream leads to significant, implementation-specific outcomes. Some library implementations fill the underlying `filebuf` with data as soon as std::ifstream opens a file, which means `readsome()` always reads data and could even read the entire file. With other implementations, std::ifstream only reads from a file when an input operation is invoked, which means calling `readsome()` immediately after opening the file never extracts any characters. Similarly, calling std::cin.readsome() may return all pending, unprocessed console input or may always return zero and extract no characters.

### Example

Run this code

```
#include <cassert>
#include <iostream>
#include <sstream>
 
int main()
{
    char c[10] = "*********"; // c[9] == '\0'
 
    // std::stringbuf makes its entire buffer available for unblocking read
    std::istringstream input("This is sample text.");
 
    auto r = input.readsome(c, 5); // reads 'This ' and stores in c[0] .. c[4]
    assert(r == 5);
    std::cout << c << '\n';
 
    r = input.readsome(c, 9); // reads 'is sample' and stores in c[0] .. c[8]
    assert(r == 9);
    std::cout << c << '\n';
}

```

Output:

```
This ****
is sample

```

### See also

|  |  |
| --- | --- |
| read | extracts blocks of characters   (public member function) |
| in_avail | obtains the number of characters immediately available in the get area   (public member function of `std::basic_streambuf<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_istream/readsome&oldid=176673>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 October 2024, at 05:21.