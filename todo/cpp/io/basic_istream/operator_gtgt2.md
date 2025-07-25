# operator>>(std::basic_istream)

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
| ****operator>>(std::basic_istream)**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<istream>` |  |  |
| template< class CharT, class Traits >  basic_istream<CharT, Traits>&      operator>>( basic_istream<CharT, Traits>& st, CharT& ch );    template< class Traits >  basic_istream<char, Traits>&      operator>>( basic_istream<char, Traits>& st, signed char& ch );    template< class Traits >  basic_istream<char, Traits>&     operator>>( basic_istream<char, Traits>& st, unsigned char& ch ); | (1) |  |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| template< class CharT, class Traits>  basic_istream<CharT, Traits>&      operator>>( basic_istream<CharT, Traits>& st, CharT\* s );    template< class Traits >  basic_istream<char, Traits>&      operator>>( basic_istream<char, Traits>& st, signed char\* s );    template< class Traits >  basic_istream<char, Traits>&     operator>>( basic_istream<char, Traits>& st, unsigned char\* s ); |  | (until C++20) |
| template< class CharT, class Traits, std::size_t N >  basic_istream<CharT, Traits>&      operator>>( basic_istream<CharT, Traits>& st, CharT (&s)[N] );    template< class Traits, std::size_t N >  basic_istream<char, Traits>&      operator>>( basic_istream<char, Traits>& st, signed char (&s)[N] );    template< class Traits, std::size_t N >  basic_istream<char, Traits>&     operator>>( basic_istream<char, Traits>& st, unsigned char (&s)[N] ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
| template< class Istream, class T >  Istream&&     operator>>( Istream&& st, T&& value ); | (3) | (since C++11) |
|  |  |  |

1,2) Performs character input operations.1) Behaves as a FormattedInputFunction. After constructing and checking the sentry object, which may skip leading whitespace, extracts a character and stores it to `ch`. If no character is available, sets failbit (in addition to eofbit that is set as required of a FormattedInputFunction).2) Behaves as a FormattedInputFunction. After constructing and checking the sentry object, which may skip leading whitespace, extracts successive characters and stores them at successive locations of a character array whose first element is pointed to by(until C++20) `s`. The extraction stops if any of the following conditions is met:

- A whitespace character (as determined by the ctype<CharT> facet) is found. The whitespace character is not extracted.

|  |  |
| --- | --- |
| - If st.width() is greater than zero, st.width() - 1 characters are stored. | (until C++20) |
| - n - 1 characters are stored, where n is defined as follows:   - If st.width() is greater than zero, std::min(std::size_t(st.width()), N); - otherwise, n is N. | (since C++20) |

- End of file occurs in the input sequence (this also sets eofbit).

In either case, an additional null character value CharT() is stored at the end of the output. If no characters were extracted, sets failbit (the null character is still written, to the first position in the output). Finally, calls st.width(0) to cancel the effects of std::setw, if any.3) Calls the appropriate extraction operator, given an rvalue reference to an input stream object (equivalent to st >> std::forward<T>(value)). This overload participates in overload resolution only if st >> std::forward<T>(value) is well-formed and `Istream` is a class type publicly and unambiguously derived from std::ios_base.

### Notes

Extracting a single character that is the last character of the stream does not set `eofbit`: this is different from other formatted input functions, such as extracting the last integer with operator>>, but this behavior matches the behavior of std::scanf with "%c" format specifier.

### Parameters

|  |  |  |
| --- | --- | --- |
| st | - | input stream to extract the data from |
| ch | - | reference to a character to store the extracted character to |
| s | - | pointer to(until C++20) a character array to store the extracted characters to |

### Return value

1,2) st3) std::move(st)

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <sstream>
 
int main()
{
    std::string input = "n greetings";
    std::istringstream stream(input);
 
    char c;
    const int MAX = 6;
    char cstr[MAX];
 
    stream >> c >> std::setw(MAX) >> cstr;
    std::cout << "c = " << c << '\n'
              << "cstr = " << cstr << '\n';
 
    double f;
    std::istringstream("1.23") >> f; // rvalue stream extraction
    std::cout << "f = " << f << '\n';
}

```

Output:

```
c = n
cstr = greet
f = 1.23

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 13 | C++98 | the definition of n mentioned a non-existing name eos | replaced with CharT() |
| LWG 68 | C++98 | no null characters were stored at the end of the output for overload (2) | stores a null character |
| LWG 1203 | C++98 | overload for rvalue stream returned lvalue reference to the base class | returns rvalue reference to the derived class |
| LWG 2328 | C++98 | overload for rvalue stream required another argument to be lvalue | made to accept rvalue |
| LWG 2534 | C++98 | overload for rvalue stream was not constrained | constrained |

### See also

|  |  |
| --- | --- |
| operator>> | extracts formatted data   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_istream/operator_gtgt2&oldid=158522>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 September 2023, at 04:56.