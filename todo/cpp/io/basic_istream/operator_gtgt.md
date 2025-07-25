# std::basic_istream<CharT,Traits>::operator>>

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
| ****basic_istream::operator>>**** | | | | |
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
| operator>>(std::basic_istream) | | | | |

|  |  |  |
| --- | --- | --- |
| basic_istream& operator>>( unsigned short& value ); | (1) |  |
| basic_istream& operator>>( unsigned int& value ); | (2) |  |
| basic_istream& operator>>( long& value ); | (3) |  |
| basic_istream& operator>>( unsigned long& value ); | (4) |  |
| basic_istream& operator>>( long long& value ); | (5) | (since C++11) |
| basic_istream& operator>>( unsigned long long& value ); | (6) | (since C++11) |
| basic_istream& operator>>( float& value ); | (7) |  |
| basic_istream& operator>>( double& value ); | (8) |  |
| basic_istream& operator>>( long double& value ); | (9) |  |
| basic_istream& operator>>( bool& value ); | (10) |  |
| basic_istream& operator>>( void\*& value ); | (11) |  |
| basic_istream& operator>>( short& value ); | (12) |  |
| basic_istream& operator>>( int& value ); | (13) |  |
| basic_istream& operator>>( /\* extended-floating-point-type \*/& value ); | (14) | (since C++23) |
| basic_istream& operator>>( std::ios_base& (\*func)(std::ios_base&) ); | (15) |  |
| basic_istream& operator>>( std::basic_ios<CharT, Traits>&                                  (\*func)(std::basic_ios<CharT, Traits>&) ); | (16) |  |
| basic_istream& operator>>( basic_istream& (\*func)(basic_istream&) ); | (17) |  |
| basic_istream& operator>>( std::basic_streambuf<CharT, Traits>\* sb ); | (18) |  |
|  |  |  |

Extracts values from an input stream.

1-11) Extracts a value potentially skipping preceding whitespace. The value is stored to a given reference value. This function behaves as a FormattedInputFunction. After constructing and checking the sentry object, which may skip leading whitespace, extracts a value by calling std::num_get::get().12) Extracts a short value potentially skipping preceding whitespace. The value is stored to a given reference value. This function behaves as a FormattedInputFunction. After constructing and checking the sentry object, which may skip leading whitespace, extracts a long value lval by calling std::num_get::get(). After that:

- If lval < std::numeric_limits<short>::min(), sets `failbit` and stores std::numeric_limits<short>::min() to val.
- Otherwise, if std::numeric_limits<short>::max() < lval, sets `failbit` and stores std::numeric_limits<short>::max() to val.
- Otherwise, stores static_cast<short>(lval) to val.
13) Extracts an int value potentially skipping preceding whitespace. The value is stored to a given reference value. This function behaves as a FormattedInputFunction. After constructing and checking the sentry object, which may skip leading whitespace, extracts a long value lval by calling std::num_get::get(). After that:

- If lval < std::numeric_limits<int>::min(), sets `failbit` and stores std::numeric_limits<int>::min() to val.
- Otherwise, if std::numeric_limits<int>::max() < lval, sets `failbit` and stores std::numeric_limits<int>::max() to val.
- Otherwise, stores static_cast<int>(lval) to val.
14) Extracts an extended floating-point value potentially skipping preceding whitespace. The value is stored to a given reference value. The library provides overloads for all cv-unqualified extended floating-point types as the referenced type of the parameter value. Determines the standard floating-point type `FP` as follows:

- If the floating-point conversion rank of /\* extended-floating-point-type \*/ is less than or equal to that of float, then `FP` is float.
- Otherwise, if the floating-point conversion rank of /\* extended-floating-point-type \*/ is less than or equal to that of double, then `FP` is double.
- Otherwise, `FP` is long double.
 This function behaves as a FormattedInputFunction. After constructing and checking the sentry object, which may skip leading whitespace, extracts an `FP` value fval by calling std::num_get::get(). After that:

- If fval < -std::numeric_limits</\* extended-floating-point-type \*/>::max(), sets `failbit` and stores -std::numeric_limits</\* extended-floating-point-type \*/>::max() to val.
- Otherwise, if std::numeric_limits</\* extended-floating-point-type \*/>::max() < fval, sets `failbit` and stores std::numeric_limits</\* extended-floating-point-type \*/>::max() to val.
- Otherwise, stores static_cast</\* extended-floating-point-type \*/>(fval) to val.
15-17) Calls func(\*this), where func is an I/O manipulator.18) Behaves as an UnformattedInputFunction. After constructing and checking the sentry object, extracts all data from \*this and stores it to sb. The extraction stops if one of the following conditions are met:

:   - end-of-file occurs on the input sequence;
    - inserting in the output sequence fails (in which case the character to be inserted is not extracted);
    - an exception occurs (in which case the exception is caught, and only rethrown if it inserted no characters and `failbit` is enabled in `exceptions()`).

In either case, stores the number of characters extracted in the member variable accessed by subsequent calls to gcount(). If sb is a null pointer or if no characters were inserted into sb, calls setstate(failbit) (which may throw std::ios_base::failure if enabled).

If extraction fails (e.g. if a letter was entered where a digit is expected), zero is written to value and `failbit` is set. For signed integers, if extraction results in the value too large or too small to fit in value, std::numeric_limits<T>::max() or std::numeric_limits<T>::min() (respectively) is written and `failbit` flag is set. For unsigned integers, if extraction results in the value too large or too small to fit in value, std::numeric_limits<T>::max() is written and `failbit` flag is set.

### Parameters

|  |  |  |
| --- | --- | --- |
| value | - | reference to an integer or floating-point value to store the extracted value to |
| func | - | pointer to I/O manipulator function |
| sb | - | pointer to the stream buffer to write all the data to |

### Return value

1-16,18) \*this17) func(\*this)

### Notes

For overload (14), when the extended floating-point type has a floating-point conversion rank that is not equal to the rank of any standard floating-point type, then double rounding during the conversion can result in inaccurate results. std::from_chars() can be used in situations where maximum accuracy is important.

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <sstream>
 
int main()
{
    std::string input = "41 3.14 false hello world";
    std::istringstream stream(input);
 
    int n;
    double f;
    bool b;
 
    stream >> n >> f >> std::boolalpha >> b;
    std::cout << "n = " << n << '\n'
              << "f = " << f << '\n'
              << "b = " << std::boolalpha << b << '\n';
 
    // extract the rest using the streambuf overload
    stream >> std::cout.rdbuf();
    std::cout << '\n';
}

```

Output:

```
n = 41
f = 3.14
b = false
hello world

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 64 | C++98 | it was unclear whether overload (18) can only rethrow the std::ios_base::failure thrown by calling setstate(failbit) | all exceptions caught can be rethrown |
| LWG 118 | C++98 | overload (12,13) delegated the extraction to num_get::get, but it does not have overloads for short and int | a long value is extracted instead of short or int |
| LWG 413 | C++98 | overload (18) only rethrew exceptions thrown while extracting characters from sb, but characters are extracted from \*this | corrected sb to \*this |
| LWG 567 | C++98 | overload (18) behaved as a FormattedInputFunction because of the resolution of LWG issue 60 | it behaves as an UnformattedInputFunction |
| LWG 661 | C++98 | overloads (12,13) did not store the extracted number to value due to the resolution of LWG issue 118 | stores the number if no overflow occurs |
| LWG 696 | C++98 | value was unchanged on extraction failure | set to zero or minimum/ maximum values |

### See also

|  |  |
| --- | --- |
| operator>>(std::basic_istream) | extracts characters and character arrays   (function template) |
| operator<<operator>> | performs stream input and output on strings   (function template) |
| operator<<operator>> | performs stream input and output of bitsets   (function template) |
| operator<<operator>> | serializes and deserializes a complex number   (function template) |
| operator<<operator>>(C++11) | performs stream input and output on pseudo-random number engine   (function template) |
| operator<<operator>>(C++11) | performs stream input and output on pseudo-random number distribution   (function template) |
| read | extracts blocks of characters   (public member function) |
| readsome | extracts already available blocks of characters   (public member function) |
| get | extracts characters   (public member function) |
| getline | extracts characters until the given character is found   (public member function) |
| from_chars(C++17) | converts a character sequence to an integer or floating-point value   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_istream/operator_gtgt&oldid=148931>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 March 2023, at 22:45.