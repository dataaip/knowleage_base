# std::experimental::scope_fail<EF>::~scope_fail

From cppreference.com
< cpp‎ | experimental‎ | scope fail
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

std::experimental::scope_fail

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| scope_fail::scope_fail | | | | |
| ****scope_fail::~scope_fail**** | | | | |
| Modifiers | | | | |
| scope_fail::release | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| ~scope_fail() noexcept; |  | (library fundamentals TS v3) |
|  |  |  |

Calls the exit function if the result of std::uncaught_exceptions() is greater than the counter of uncaught exceptions (typically on stack unwinding) and the `scope_fail` is active, then destroys the stored `EF` (if it is a function object) and any other non-static data members.

### Notes

Whether the destructor is called on stack unwinding can be detected by the comparison of the result of std::uncaught_exceptions() and the counter of uncaught exceptions in the `scope_fail`.

### See also

|  |  |
| --- | --- |
| release | makes the `scope_fail` inactive   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/scope_fail/%7Escope_fail&oldid=115119>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 January 2020, at 19:18.