# std::experimental::atomic_shared_ptr<T>::atomic_shared_ptr

From cppreference.com
< cpp‎ | experimental‎ | atomic shared ptr
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

std::experimental::atomic_shared_ptr

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****atomic_shared_ptr::atomic_shared_ptr**** | | | | |
| atomic_shared_ptr::operator= | | | | |
| atomic_shared_ptr::is_lock_free | | | | |
| atomic_shared_ptr::store | | | | |
| atomic_shared_ptr::load | | | | |
| atomic_shared_ptr::operator shared_ptr<T> | | | | |
| atomic_shared_ptr::exchange | | | | |
| atomic_shared_ptr::compare_exchange_weakatomic_shared_ptr::compare_exchange_strong | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr atomic_shared_ptr() noexcept; | (1) |  |
| constexpr atomic_shared_ptr( shared_ptr<T> desired ) noexcept; | (2) |  |
| atomic_shared_ptr( const atomic_shared_ptr& ) = delete; | (3) |  |
|  |  |  |

Constructs a new `atomic_shared_ptr` object.

1) The default constructor initializes the object to an empty state.2) Initializes the underlying `shared_ptr<T>` with `desired`. The initialization is not atomic.3) Atomic variables are not CopyConstructible.

### Parameters

|  |  |  |
| --- | --- | --- |
| desired | - | value to initialize with |

### Exceptions

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/atomic_shared_ptr/atomic_shared_ptr&oldid=103369>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 June 2018, at 14:37.