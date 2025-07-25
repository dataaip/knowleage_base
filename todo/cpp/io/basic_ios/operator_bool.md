# std::basic_ios<CharT,Traits>::operator bool

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
| basic_ios::good | | | | |
| basic_ios::eof | | | | |
| basic_ios::fail | | | | |
| basic_ios::bad | | | | |
| basic_ios::operator! | | | | |
| ****basic_ios::operator bool**** | | | | |
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
| operator /\* unspecified-boolean-type \*/() const; | (1) | (until C++11) |
| explicit operator bool() const; | (2) | (since C++11) |
|  |  |  |

Checks whether the stream has no errors.

1) Returns a value that evaluates to false in a boolean context if fail() returns true, otherwise returns a value that evaluates to true in a boolean context.2) Returns true if the stream has no errors and is ready for I/O operations. Specifically, returns !fail().

This operator makes it possible to use streams and functions that return references to streams as loop conditions, resulting in the idiomatic C++ input loops such as while (stream >> value) {...} or while (std::getline(stream, string)) {...}. Such loops execute the loop's body only if the input operation succeeded.

### Parameters

(none)

### Return value

1) A value that evaluates to true in a boolean context if the stream has no errors, a value that evaluates to false in a boolean context otherwise.2) true if the stream has no errors, false otherwise.

### Notes

This conversion can be used in contexts where a bool is expected (e.g. an if condition). However, implicit conversions (e.g. to int) that can occur with bool are not allowed.

In C++98, operator bool could not be provided directly due to the safe bool problem. The initial solution in C++98 is to provide operator void\*, which returns a null pointer if fail() returns true or a non-null pointer otherwise. It is replaced by the resolution of LWG issue 468, which allows Safe Bool idiom to be applied.

Since C++11, conversion functions can be explicit. The resolution of LWG issue 1094 introduced the explicit operator bool and the boolean conversion is now safe.

### Example

Run this code

```
#include <iostream>
#include <sstream>
 
int main()
{
    std::istringstream s("1 2 3 error");
    int n;
 
    std::cout << std::boolalpha << "s is " << static_cast<bool>(s) << '\n';
    while (s >> n)
        std::cout << n << '\n';
    std::cout << "s is " << static_cast<bool>(s) << '\n';
}

```

Output:

```
s is true
1
2
3
s is false

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 468 | C++98 | operator void\* was provided | a conversion function to an unspecified boolean type is provided instead |

### See also

The following table shows the value of basic_ios accessors (good(), fail(), etc.) for all possible combinations of ios_base::iostate flags:

|  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ios_base::iostate flags | | | `basic_ios` accessors | | | | | |
| `eofbit` | `failbit` | `badbit` | good() | fail() | bad() | eof() | ****operator bool**** | operator! |
| false | false | false | true | false | false | false | true | false |
| false | false | true | false | true | true | false | false | true |
| false | true | false | false | true | false | false | false | true |
| false | true | true | false | true | true | false | false | true |
| true | false | false | false | false | false | true | true | false |
| true | false | true | false | true | true | true | false | true |
| true | true | false | false | true | false | true | false | true |
| true | true | true | false | true | true | true | false | true |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/basic_ios/operator_bool&oldid=148329>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 February 2023, at 23:48.