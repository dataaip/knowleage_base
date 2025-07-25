# std::experimental::scope_success<EF>::release

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
| scope_success::~scope_success | | | | |
| Modifiers | | | | |
| ****scope_success::release**** | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| void release() noexcept; |  | (library fundamentals TS v3) |
|  |  |  |

Makes the `scope_success` inactive.

Once a `scope_success` is inactive, it cannot become active again, and will not call its exit function on destruction.

### Parameters

(none)

### Return value

(none)

### Notes

`release` may be either manually called or automatically called by `scope_success`'s move constructor.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a new `scope_success`   (public member function) |
| (destructor) | calls the exit function when the scope is exited normally if the `scope_success` is active, then destroys the `scope_success`   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/scope_success/release&oldid=115102>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 January 2020, at 17:56.