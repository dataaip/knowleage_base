# std::experimental::atomic_weak_ptr<T>::store

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
| ****atomic_weak_ptr::store**** | | | | |
| atomic_weak_ptr::load | | | | |
| atomic_weak_ptr::operator weak_ptr<T> | | | | |
| atomic_weak_ptr::exchange | | | | |
| atomic_weak_ptr::compare_exchange_weakatomic_weak_ptr::compare_exchange_strong | | | | |

|  |  |  |
| --- | --- | --- |
| void store( weak_ptr<T> desired, std::memory_order order = std::memory_order_seq_cst ) noexcept; |  |  |
|  |  |  |

Atomically replaces the current value with `desired`. Memory is affected according to the value of `order`.

`order` must be one of std::memory_order_relaxed, std::memory_order_release or std::memory_order_seq_cst. Otherwise the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| desired | - | the `weak_ptr` to store into the atomic variable |
| order | - | memory order constraints to enforce |

### Return value

(none)

### Remarks

All changes to the `atomic_weak_ptr` object itself, and all associated use_count increments, are guaranteed to be performed atomically. Associated `use_count` decrements take place after the atomic operation, but are not required to be part of it. Any associated destruction or deallocation operations take place after the atomic operation and are not part of it.

### See also

|  |  |
| --- | --- |
| operator= | stores a value into an `atomic_weak_ptr` object   (public member function) |
| std::atomic_is_lock_free(std::shared_ptr)std::atomic_load(std::shared_ptr)std::atomic_load_explicit(std::shared_ptr)std::atomic_store(std::shared_ptr)std::atomic_store_explicit(std::shared_ptr)std::atomic_exchange(std::shared_ptr)std::atomic_exchange_explicit(std::shared_ptr)std::atomic_compare_exchange_weak(std::shared_ptr)std::atomic_compare_exchange_strong(std::shared_ptr)std::atomic_compare_exchange_weak_explicit(std::shared_ptr)std::atomic_compare_exchange_strong_explicit(std::shared_ptr)(deprecated in C++20)(removed in C++26) | specializes atomic operations for `std::shared_ptr`   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/atomic_weak_ptr/store&oldid=93169>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 May 2017, at 12:34.