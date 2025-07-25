# std::experimental::unique_resource<R, D>::reset

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
| ****unique_resource::reset**** | | | | |
| Observers | | | | |
| unique_resource::get | | | | |
| unique_resource::get_deleter | | | | |
| unique_resource::operator\*unique_resource::operator-> | | | | |
| Non-member functions | | | | |
| make_unique_resource_checked | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| void reset() noexcept; | (1) | (library fundamentals TS v3) |
| template< class RR >  void reset( RR&& r ); | (2) | (library fundamentals TS v3) |
|  |  |  |

1) Disposes the resource by calling the deleter with the underlying resource handle if the `unique_resource` owns it. The `unique_resource` does not own the resource after the call.2) Replaces the resource by calling (1) and then assigns the stored resource handle with std::forward<RR>(r) if std::is_nothrow_assignable_v<RS, RR> is true, otherwise std::as_const(r), where `RS` is the type of stored resource handle. The `unique_resource` owns the resource after the call. If copy-assignment of the store resource handle throws an exception, calls del_(r), where `del` is the deleter object. This overload participates in overload resolution only if the selected assignment expression assigning the stored resource handle is well-formed. The program is ill-formed if del_(r) is ill-formed. The behavior is undefined if del_(r) results in undefined behavior or throws an exception.

### Parameters

|  |  |  |
| --- | --- | --- |
| r | - | resource handle for a new resource to manage |

### Return value

(none)

### Exceptions

2) Any exception thrown in assigning the stored resource handle.

### Notes

The mechanism ensures no leaking of resources.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| reset | replaces the managed object   (public member function of `std::unique_ptr<T,Deleter>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/unique_resource/reset&oldid=156351>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 August 2023, at 22:52.