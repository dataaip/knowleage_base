# std::basic_ostream<CharT,Traits>::operator<<

From cppreference.com
< cpp‎ | io‎ | basic ostream
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

std::basic_ostream

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Global objects | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | coutwcout | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cerrwcerr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clogwclog | | | | | |
| Member functions | | | | |
| basic_ostream::basic_ostream | | | | |
| basic_ostream::~basic_ostream | | | | |
| basic_ostream::operator=(C++11) | | | | |
| Formatted output | | | | |
| ****basic_ostream::operator<<**** | | | | |
| Unformatted output | | | | |
| basic_ostream::put | | | | |
| basic_ostream::write | | | | |
| Positioning | | | | |
| basic_ostream::tellp | | | | |
| basic_ostream::seekp | | | | |
| Miscellaneous | | | | |
| basic_ostream::flush | | | | |
| basic_ostream::swap(C++11) | | | | |
| Member classes | | | | |
| basic_ostream::sentry | | | | |
| Non-member functions | | | | |
| operator<<(std::basic_ostream) | | | | |
| print(std::ostream)(C++23) | | | | |
| println(std::ostream)(C++23) | | | | |
| vprint_unicode(std::ostream)(C++23) | | | | |
| vprint_nonunicode(std::ostream)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_ostream& operator<<( bool value ); | (1) |  |
| basic_ostream& operator<<( long value ); | (2) |  |
| basic_ostream& operator<<( unsigned long value ); | (3) |  |
| basic_ostream& operator<<( long long value ); | (4) | (since C++11) |
| basic_ostream& operator<<( unsigned long long value ); | (5) | (since C++11) |
| basic_ostream& operator<<( double value ); | (6) |  |
| basic_ostream& operator<<( long double value ); | (7) |  |
| basic_ostream& operator<<( const void\* value ); | (8) |  |
| basic_ostream& operator<<( const volatile void\* value ); | (9) | (since C++23) |
| basic_ostream& operator<<( std::nullptr_t ); | (10) | (since C++17) |
| basic_ostream& operator<<( short value ); | (11) |  |
| basic_ostream& operator<<( int value ); | (12) |  |
| basic_ostream& operator<<( unsigned short value ); | (13) |  |
| basic_ostream& operator<<( unsigned int value ); | (14) |  |
| basic_ostream& operator<<( float value ); | (15) |  |
| basic_ostream& operator<<( /\* extended-floating-point-type \*/ value ); | (16) | (since C++23) |
| basic_ostream& operator<<( std::basic_streambuf<CharT, Traits>\* sb ); | (17) |  |
| basic_ostream& operator<<(      std::ios_base& (\*func)(std::ios_base&) ); | (18) |  |
| basic_ostream& operator<<(      std::basic_ios<CharT, Traits>& (\*func)(std::basic_ios<CharT, Traits>&) ); | (19) |  |
| basic_ostream& operator<<(  std::basic_ostream<CharT, Traits>& (\*func) (std::basic_ostream<CharT, Traits>&) ); | (20) |  |
|  |  |  |

Inserts data into the stream.

1-8) Inserts value. This function behaves as a FormattedOutputFunction. After constructing and checking the sentry object, inserts a value by calling std::num_put::put(). If the end of file condition was encountered during output (put().failed() == true), sets `badbit`.9) Equivalent to return operator<<(const_cast<const void\*>(p));.10) Equivalent to return \*this << s;, where s is an implementation-defined null-terminated character type string.11) Inserts a value from short value. This function behaves as a FormattedOutputFunction. After constructing and checking the sentry object, inserts a long value lval as in (2), where lval is

- static_cast<long>(static_cast<unsigned short>(value)), if flags() & std::ios_base::basefield is std::ios_base::oct or std::ios_base::hex, or
- static_cast<long>(value) otherwise.
12) Inserts a value from int value. This function behaves as a FormattedOutputFunction. After constructing and checking the sentry object, inserts a long value lval as in (2), where lval is

- static_cast<long>(static_cast<unsigned int>(value)), if flags() & std::ios_base::basefield is std::ios_base::oct or std::ios_base::hex, or
- static_cast<long>(value) otherwise.
13,14) Inserts a value from unsigned short or unsigned int value. This function behaves as a FormattedOutputFunction. After constructing and checking the sentry object, inserts static_cast<unsigned long>(value) as in (3).15) Inserts a value from float value. This function behaves as a FormattedOutputFunction. After constructing and checking the sentry object, inserts static_cast<double>(value) as in (6).16) Inserts a value from value. The library provides overloads for all cv-unqualified extended floating-point types as the type of the parameter value. This function behaves as a FormattedOutputFunction. After constructing and checking the sentry object, checks the floating-point conversion rank of /\* extended-floating-point-type \*/:

- If the rank is less than or equal to that of double, inserts static_cast<double>(value) as in (6).
- Otherwise, if the rank is less than or equal to that of long double, inserts static_cast<long double>(value) as in (7).
- Otherwise, an invocation of this overload is conditionally supported with implementation-defined semantics.
17) This function behaves as an UnformattedOutputFunction. After constructing and checking the sentry object, checks if sb is a null pointer. If it is, executes setstate(badbit) and exits. Otherwise, extracts characters from the input sequence controlled by sb and inserts them into \*this until one of the following conditions are met:

:   - end-of-file occurs on the input sequence;
    - inserting in the output sequence fails (in which case the character to be inserted is not extracted);
    - an exception occurs (in which case the exception is caught).

If no characters were inserted, executes setstate(failbit). If an exception was thrown while extracting, sets `failbit` and, if `failbit` is set in exceptions(), rethrows the exception.18-20) Calls func(\*this). These overloads are used to implement output I/O manipulators such as std::endl.

### Parameters

|  |  |  |
| --- | --- | --- |
| value | - | integer, floating-point, boolean, or pointer value to insert |
| func | - | function to call |
| sb | - | pointer to the stream buffer to read the data from |

### Return value

1-19) \*this20) func(\*this)

### Notes

There are no overloads for pointers to non-static members, pointers to volatiles,(until C++23) or function pointers (other than the ones with signatures accepted by the (18-20) overloads).

- Attempting to output such objects invokes implicit conversion to bool, and, for any non-null pointer value, the value 1 is printed (unless `boolalpha` was set, in which case true is printed).

Character and character string arguments (e.g., of type char or const char\*) are handled by the non-member overloads of operator<<.

- Attempting to output a character using the member function call syntax (e.g., std::cout.operator<<('c');) will call one of the overloads in (2-5) or (11-14) and output the numerical value.
- Attempting to output a character string using the member function call syntax will call overload (8) and print the pointer value instead.

Overload (10) was added by the resolution of LWG issue 2221, but it is never implemented in any standard library implementation under C++11/14 modes.

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <sstream>
 
int fun() { return 42; }
 
int main()
{
    std::istringstream input(" \"Some text.\" ");
    double f = 3.14;
    bool b = true;
 
    std::cout
        << fun()          // int overload (12)
        << ' '            // non-member overload
        << std::boolalpha // function overload (18)
        << b              // bool overload (1)
        << " "            // non-member overload
        << std::fixed     // function overload (18) again
        << f              // double overload (6)
        << input.rdbuf()  // streambuf overload
        << fun            // bool overload (1): there's no overload for int(*)()
        << std::endl;     // function overload (18) again
 
    int x = 0;
    int* p1 = &x;
    volatile int* p2 = &x;
    std::cout
        << "p1: " << p1 << '\n'  // `const void*` overload, prints address
        << "p2: " << p2 << '\n'; // before C++23 (P1147): bool overload :), because
            // operator<<(const void*) is not a match, as it discards the `volatile`
            // qualifier. To fix this, C++23 adds `const volatile void*` overload (9),
            // that prints the address as expected.
}

```

Possible output:

```
42 true 3.140000 "Some text." true
p1: 0x7ffcea766600
p2: 0x7ffcea766600

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 117 | C++98 | overloads (1-8,11-15) delegated the insertion to num_put::put, but it does not have overloads for short, unsigned short, int, unsigned int, and float | they are converted before being passed to `num_put::put` |
| LWG 567 | C++98 | overload (17) behaved as a FormattedOutputFunction because of the resolution of LWG issue 60 | it behaves as an UnformattedOutputFunction |

### See also

|  |  |
| --- | --- |
| operator<<(std::basic_ostream) | inserts character data or insert into rvalue stream   (function template) |
| operator<<operator>> | performs stream input and output on strings   (function template) |
| operator<<(C++17) | performs stream output on string views   (function template) |
| operator<<operator>> | performs stream input and output of bitsets   (function template) |
| operator<<operator>> | serializes and deserializes a complex number   (function template) |
| operator<<operator>>(C++11) | performs stream input and output on pseudo-random number engine   (function template) |
| operator<<operator>>(C++11) | performs stream input and output on pseudo-random number distribution   (function template) |
| put | inserts a character   (public member function) |
| write | inserts blocks of characters   (public member function) |
| to_chars(C++17) | converts an integer or floating-point value to a character sequence   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ostream/operator_ltlt&oldid=179588>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 January 2025, at 09:13.