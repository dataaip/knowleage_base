# std::experimental::unique_resource<R, D>::get_deleter

From cppreference.com
< cpp‎ | experimental‎ | unique resource
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

std::experimental::unique_resource

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| unique_resource::unique_resource | | | | |
| unique_resource::~unique_resource | | | | |
| unique_resource::operator= | | | | |
| Modifiers | | | | |
| unique_resource::release | | | | |
| unique_resource::reset | | | | |
| Observers | | | | |
| unique_resource::get | | | | |
| ****unique_resource::get_deleter**** | | | | |
| unique_resource::operator\*unique_resource::operator-> | | | | |
| Non-member functions | | | | |
| make_unique_resource_checked | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| const D& get_deleter() const noexcept; |  | (library fundamentals TS v3) |
|  |  |  |

Accesses the deleter object which would be used for disposing the managed resource.

### Parameters

(none)

### Return value

The stored deleter.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| get_deleter | returns the deleter that is used for destruction of the managed object   (public member function of `std::unique_ptr<T,Deleter>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/unique_resource/get_deleter&oldid=115191>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 January 2020, at 02:14.