# Extensions for concurrency

From cppreference.com
< cpp‎ | experimental
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
| ****Extensions for concurrency**** (concurrency TS) | | | | |
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

****Extensions for concurrency****

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

The C++ Extensions for Concurrency, ISO/IEC TS 19571:2016, defines the following new components for the C++ standard library:

### Continuations and other extensions for std::future

|  |  |
| --- | --- |
| Defined in header `<experimental/future>` | |
| future(concurrency TS) | a version of std::future enhanced with continuations and other features   (class template) |
| shared_future(concurrency TS) | a version of std::shared_future enhanced with continuations and other features   (class template) |
| promise(concurrency TS) | a modified version of std::promise that uses std::experimental::future   (class template) |
| packaged_task(concurrency TS) | a modified version of std::packaged_task that uses std::experimental::future   (class template) |
| when_all(concurrency TS) | produces a future that becomes ready when all given futures or `shared_futures` are ready   (function template) |
| when_any(concurrency TS) | produces a future that becomes ready when at least one of the given futures or shared_futures is ready   (function template) |
| make_ready_future(concurrency TS) | produces a future that is ready immediately and holds the given value   (function template) |
| make_exceptional_future(concurrency TS) | produces a future that is ready immediately and holds the given exception   (function template) |

### Feature test macros

|  |  |
| --- | --- |
| Defined in header `<experimental/future>` | |
| __cpp_lib_experimental_future_continuations | a value of at least 201505 indicates that future::then and other extensions are supported   (macro constant) |
| Defined in header `<experimental/latch>` | |
| __cpp_lib_experimental_latch | a value of at least 201505 indicates that the latch type is supported   (macro constant) |
| Defined in header `<experimental/barrier>` | |
| __cpp_lib_experimental_barrier | a value of at least 201505 indicates that barrier type is supported   (macro constant) |
| Defined in header `<experimental/atomic>` | |
| __cpp_lib_experimental_atomic_smart_pointers | a value of at least 201505 indicates that the atomic smart pointers are supported   (macro constant) |

## Merged into C++20

The following components of the Concurrency TS have been adopted into the C++20 standard.

### Latches and barriers

|  |  |
| --- | --- |
| Defined in header `<experimental/latch>` | |
| latch(concurrency TS) | single-use thread barrier   (class) |
| Defined in header `<experimental/barrier>` | |
| barrier(concurrency TS) | reusable thread barrier   (class) |
| flex_barrier(concurrency TS) | reusable thread barrier with customizable behavior on completion   (class) |

### Atomic smart pointers

These class templates replace the shared_ptr atomic function overloads

|  |  |
| --- | --- |
| Defined in header `<experimental/atomic>` | |
| atomic_shared_ptr(concurrency TS) | atomic version of std::shared_ptr   (class template) |
| atomic_weak_ptr(concurrency TS) | atomic version of std::weak_ptr   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/concurrency&oldid=163704>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 November 2023, at 10:45.