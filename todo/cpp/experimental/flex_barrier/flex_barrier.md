# std::experimental::flex_barrier::flex_barrier

From cppreference.com
< cpp‎ | experimental‎ | flex barrier
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

std::experimental::flex_barrier

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****flex_barrier::flex_barrier**** | | | | |
| flex_barrier::~flex_barrier | | | | |
| flex_barrier::arrive_and_wait | | | | |
| flex_barrier::arrive_and_drop | | | | |

|  |  |  |
| --- | --- | --- |
| explicit flex_barrier( std::ptrdiff_t num_threads ); | (1) | (concurrency TS) |
| template< class F >  flex_barrier( std::ptrdiff_t num_threads, F completion ); | (2) | (concurrency TS) |
| flex_barrier( const flex_barrier & ) = delete; | (3) | (concurrency TS) |
|  |  |  |

1) Has the same effect as flex_barrier(num_threads, c), where `c` is a Callable object whose invocation returns -1 and has no side effects.2) Constructs a `flex_barrier` for num_threads participating threads, using completion for the completion phase. The set of participating threads is the first num_threads threads to arrive at the synchronization point.3) Copy constructor is deleted; `flex_barrier` is not copyable.

### Parameters

|  |  |  |
| --- | --- | --- |
| num_threads | - | the number of participating threads for the `flex_barrier`; must be non-negative |
| completion | - | a function object controlling the completion phase; must be Callable with no arguments and return type std::ptrdiff_t, and when invoked, must return a value no less than -1 and must not throw an exception |
| Type requirements | | |
| -`F` must meet the requirements of CopyConstructible. | | |

### Notes

If num_threads is zero, the set of participating threads is empty, and flex_barrier can only be destroyed.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/flex_barrier/flex_barrier&oldid=154817>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 July 2023, at 22:23.