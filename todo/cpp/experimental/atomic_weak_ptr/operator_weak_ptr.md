# std::experimental::atomic_weak_ptr<T>::operator weak_ptr<T>

From cppreference.com
< cpp‎ | experimental‎ | atomic weak ptr
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

Extensions for concurrency

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| std::future extensions | | | | |
| experimental::future | | | | |
| experimental::shared_future | | | | |
| experimental::when_all | | | | |
| experimental::when_any | | | | |
| experimental::make_ready_future | | | | |
| experimental::make_exceptional_future | | | | |
| Latches and barriers | | | | |
| experimental::latch | | | | |
| experimental::barrier | | | | |
| experimental::flex_barrier | | | | |
| Atomic smart pointers | | | | |
| experimental::atomic_shared_ptr | | | | |
| experimental::atomic_weak_ptr | | | | |

std::experimental::atomic_weak_ptr

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| atomic_weak_ptr::atomic_weak_ptr | | | | |
| atomic_weak_ptr::operator= | | | | |
| atomic_weak_ptr::is_lock_free | | | | |
| atomic_weak_ptr::store | | | | |
| atomic_weak_ptr::load | | | | |
| ****atomic_weak_ptr::operator weak_ptr<T>**** | | | | |
| atomic_weak_ptr::exchange | | | | |
| atomic_weak_ptr::compare_exchange_weakatomic_weak_ptr::compare_exchange_strong | | | | |

|  |  |  |
| --- | --- | --- |
| operator weak_ptr<T>() const noexcept; |  |  |
|  |  |  |

Atomically loads and returns the current value of the `atomic_weak_ptr`. Equivalent to load().

### Parameters

(none)

### Return value

The current value of the `atomic_weak_ptr`.

### Remarks

All associated use_count increments are guaranteed to be performed as part of the atomic operation.

### See also

|  |  |
| --- | --- |
| load | atomically obtains the value of the atomic object   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/atomic_weak_ptr/operator_weak_ptr&oldid=93167>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 May 2017, at 12:34.