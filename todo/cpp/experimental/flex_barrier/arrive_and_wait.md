# std::experimental::flex_barrier::arrive_and_wait

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
| flex_barrier::flex_barrier | | | | |
| flex_barrier::~flex_barrier | | | | |
| ****flex_barrier::arrive_and_wait**** | | | | |
| flex_barrier::arrive_and_drop | | | | |

|  |  |  |
| --- | --- | --- |
| void arrive_and_wait(); |  | (concurrency TS) |
|  |  |  |

Blocks and arrives at the `flex_barrier`'s synchronization point.

The behavior is undefined if the calling thread is not in the set of participating threads of this `flex_barrier`.

Calls to `arrive_and_wait` synchronizes with the start of the completion phase of the `flex_barrier`. The completion of the completion phase synchronizes with the return from the call.

Calls to `arrive_and_drop` and `arrive_and_wait` never introduce data races with themselves or each other.

### Notes

It is safe for a thread to call either `arrive_and_wait()` or `arrive_and_drop()` immediately on return from this call (provided that the function object for the completion phase did not return zero). It's not necessary to ensure that all blocked threads have exited `arrive_and_wait()` before a thread calls it again.

The completion phase executes the function object specified when the `flex_barrier` was constructed. If it returns -1, the set of participating threads is unchanged; otherwise, the set of participating threads is a new set with the size equal to the return value `N`, and consists of the next `N` threads to arrive at the synchronization point. If N == 0, the `flex_barrier` can only be destroyed.

The initial set of participating threads for a `flex_barrier` constructed for `num_threads` threads is the first `num_threads` to arrive at its synchronization point.

### Exceptions

Throws nothing.

### See also

|  |  |
| --- | --- |
| arrive_and_drop | arrive at the synchronization point and remove the current thread from the set of participating threads   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/flex_barrier/arrive_and_wait&oldid=98604>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 January 2018, at 17:15.