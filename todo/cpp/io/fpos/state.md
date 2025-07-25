# std::fpos<State>::state

From cppreference.com
< cpp‎ | io‎ | fpos
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

std::fpos

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****fpos::state**** | | | | |

|  |  |  |
| --- | --- | --- |
| State state() const; | (1) |  |
| void state( State st ); | (2) |  |
|  |  |  |

Manages the file position state.

1) Returns the value of the file position state.2) Replaces the file position state with the value of st.

For the specializations of std::fpos that are used in the standard library, `State` is always std::mbstate_t.

### Parameters

|  |  |  |
| --- | --- | --- |
| st | - | new value for the state |

### Return value

1) The current value of the `fpos` state.2) (none)

### Example

Run this code

```
#include <cwchar>
#include <iostream>
#include <sstream>
 
int main()
{
    std::istringstream s("test");
    std::mbstate_t st = s.tellg().state();
 
    if (std::mbsinit(&st))
        std::cout << "The stream is in the initial shift state\n";
}

```

Output:

```
The stream is in the initial shift state

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 441 | C++98 | overload (1) was not declared const (it is const in the synopsis) | added const |

### See also

|  |  |
| --- | --- |
| mbstate_t | conversion state information necessary to iterate multibyte character strings   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/fpos/state&oldid=159105>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 September 2023, at 10:46.