# std::basic_istream<CharT,Traits>::getline

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
| ****basic_istream::getline**** | | | | |
| basic_istream::ignore | | | | |
| basic_istream::read | | | | |
| basic_istream::readsome | | | | |
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
| basic_istream& getline( char_type\* s, std::streamsize count ); | (1) |  |
| basic_istream& getline( char_type\* s, std::streamsize count, char_type delim ); | (2) |  |
|  |  |  |

Extracts characters from stream until end of line or the specified delimiter delim.

The first overload is equivalent to getline(s, count, widen('\n')).

Behaves as UnformattedInputFunction. After constructing and checking the sentry object, extracts characters from \*this and stores them in successive locations of the array whose first element is pointed to by s, until any of the following occurs (tested in the order shown):

1. end of file condition occurs in the input sequence.
2. the next available character c is the delimiter, as determined by Traits::eq(c, delim). The delimiter is extracted (unlike `basic_istream::get()`) and counted towards gcount(), but is not stored.
3. count is non-positive, or count - 1 characters have been extracted (setstate(failbit) is called in this case).

If the function extracts no characters, ​`failbit` is set in the local error state before setstate() is called.

In any case, if count > 0, it then stores a null character CharT() into the next successive location of the array and updates gcount().

### Notes

Because condition #2 is tested before condition #3, the input line that exactly fits the buffer does not trigger `failbit`.

Because the terminating character is counted as an extracted character, an empty input line does not trigger `failbit`.

### Parameters

|  |  |  |
| --- | --- | --- |
| s | - | pointer to the character string to store the characters to |
| count | - | size of character string pointed to by s |
| delim | - | delimiting character to stop the extraction at. It is extracted but not stored. |

### Return value

\*this

### Exceptions

failure if an error occurred (the error state flag is not goodbit) and exceptions() is set to throw for that state.

If an internal operation throws an exception, it is caught and badbit is set. If exceptions() is set for `badbit`, the exception is rethrown.

### Example

Run this code

```
#include <array>
#include <iostream>
#include <sstream>
#include <vector>
 
int main()
{
    std::istringstream input("abc|def|gh");
    std::vector<std::array<char, 4>> v;
 
    // note: the following loop terminates when std::ios_base::operator bool()
    // on the stream returned from getline() returns false
    for (std::array<char, 4> a; input.getline(&a[0], 4, '|');)
        v.push_back(a);
 
    for (auto& a : v)
        std::cout << &a[0] << '\n';
}

```

Output:

```
abc
def
gh

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 531 | C++98 | `std::getline` could not handle the case where count is non-positive | no character is extracted in this case |

### See also

|  |  |
| --- | --- |
| getline | read data from an I/O stream into a string   (function template) |
| operator>> | extracts formatted data   (public member function) |
| get | extracts characters   (public member function) |
| read | extracts blocks of characters   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_istream/getline&oldid=167716>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 December 2023, at 04:36.