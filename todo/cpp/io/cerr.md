# std::cerr, std::wcerr

From cppreference.com
< cpp‎ | io
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | coutwcout | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****cerrwcerr**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clogwclog | | | | | |
| Member functions | | | | |
| basic_ostream::basic_ostream | | | | |
| basic_ostream::~basic_ostream | | | | |
| basic_ostream::operator=(C++11) | | | | |
| Formatted output | | | | |
| basic_ostream::operator<< | | | | |
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
| Defined in header `<iostream>` |  |  |
| extern std::ostream cerr; | (1) |  |
| extern std::wostream wcerr; | (2) |  |
|  |  |  |

The global objects `std::cerr` and `std::wcerr` control output to a stream buffer of implementation-defined type (derived from std::streambuf and std::wstreambuf, respectively), associated with the standard C error output stream stderr.

These objects are guaranteed to be initialized during or before the first time an object of type std::ios_base::Init is constructed and are available for use in the constructors and destructors of static objects with ordered initialization (as long as <iostream> is included before the object is defined).

Unless std::ios_base::sync_with_stdio(false) has been issued, it is safe to concurrently access these objects from multiple threads for both formatted and unformatted output.

Once initialized, (std::cerr.flags() & unitbuf) != 0 (same for `std::wcerr`) meaning that any output sent to these stream objects is immediately flushed to the OS (via std::basic_ostream::sentry's destructor).

In addition, std::cerr.tie() returns &std::cout (same for `std::wcerr` and std::wcout), meaning that any output operation on `std::cerr` first executes std::cout.flush() (via std::basic_ostream::sentry's constructor).

### Notes

The 'c' in the name refers to "character" (stroustrup.com FAQ); `cerr` means "character error (stream)" and `wcerr` means "wide character error (stream)".

### Example

Output to stderr via `std::cerr` flushes out the pending output on std::cout, while output to stderr via std::clog does not.

Run this code

```
#include <chrono>
#include <iostream>
#include <thread>
using namespace std::chrono_literals;
 
void f()
{
    std::cout << "Output from thread...";
    std::this_thread::sleep_for(2s);
    std::cout << "...thread calls flush()" << std::endl;
}
 
int main()
{
    std::jthread t1{f};
    std::this_thread::sleep_for(1000ms);
    std::clog << "This output from main is not tie()'d to cout\n";
    std::cerr << "This output is tie()'d to cout\n";
}

```

Possible output:

```
This output from main is not tie()'d to cout
Output from thread...This output is tie()'d to cout
...thread calls flush()

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 455 | C++98 | std::cerr.tie() and std::wcerr.tie() returned null pointers | they return &std::cout and &std::wcout respectively |

### See also

|  |  |
| --- | --- |
| Init | initializes standard stream objects   (public member class of `std::ios_base`) |
| clogwclog | writes to the standard C error stream stderr (global object) |
| coutwcout | writes to the standard C output stream stdout (global object) |
| stdinstdoutstderr | expression of type FILE\* associated with the input stream expression of type FILE\* associated with the output stream expression of type FILE\* associated with the error output stream   (macro constant) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/cerr&oldid=158808>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 September 2023, at 11:29.