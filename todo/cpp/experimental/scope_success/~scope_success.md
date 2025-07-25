# std::experimental::scope_success<EF>::~scope_success

From cppreference.com
< cpp‎ | experimental‎ | scope success
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Library fundamentals v3

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::scope_exit | | | | |
| experimental::scope_fail | | | | |
| experimental::scope_success | | | | |
| experimental::unique_resource | | | | |

std::experimental::scope_success

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| scope_success::scope_success | | | | |
| ****scope_success::~scope_success**** | | | | |
| Modifiers | | | | |
| scope_success::release | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| ~scope_success() noexcept(noexcept(std::declval<EF&>()())); |  | (library fundamentals TS v3) |
|  |  |  |

Calls the exit function if the result of std::uncaught_exceptions() is less than or equal to the counter of uncaught exceptions (typically on normal exit) and the `scope_success` is active, then destroys the stored `EF` (if it is a function object) and any other non-static data members.

### Exceptions

Throws any exception thrown by calling the exit function.

### Notes

Whether the destructor is called on stack unwinding can be detected by the comparison of the result of std::uncaught_exceptions() and the counter of uncaught exceptions in the `scope_success`.

Unlike other classes or class template specializations in the C++ standard library and other C++ TR/TS's, `scope_success`'s destructor is permitted to throw an exception.

### See also

|  |  |
| --- | --- |
| release | makes the `scope_success` inactive   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/scope_success/%7Escope_success&oldid=115121>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 January 2020, at 19:22.