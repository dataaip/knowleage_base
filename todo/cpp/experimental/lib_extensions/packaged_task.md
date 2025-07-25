# std::experimental::packaged_task (library fundamentals TS)

From cppreference.com
< cpp‎ | experimental‎ | lib extensions
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

Library fundamentals

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::optional | | | | |
| experimental::any | | | | |
| experimental::basic_string_view | | | | |
| experimental::sample | | | | |
| experimental::shared_ptr | | | | |
| experimental::weak_ptr | | | | |
| experimental::apply | | | | |
| experimental::invocation_typeexperimental::raw_invocation_type | | | | |
| experimental::search | | | | |
| experimental::default_searcherexperimental::make_default_searcher | | | | |
| experimental::boyer_moore_searcherexperimental::make_boyer_moore_searcher | | | | |
| experimental::boyer_moore_horspool_searcherexperimental::make_boyer_moore_horspool_searcher | | | | |
| Type-erased and polymorphic allocators | | | | |
| Variable templates for type traits | | | | |

Polymorphic allocator library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| polymorphic_allocator | | | | |
| Convenience aliases for containers using `polymorphic_allocator` | | | | |
| Memory resource classes | | | | |
| memory_resource | | | | |
| synchronized_pool_resource | | | | |
| unsynchronized_pool_resource | | | | |
| monotonic_buffer_resource | | | | |
| resource_adaptor | | | | |
| Global memory resources | | | | |
| new_delete_resource | | | | |
| null_memory_resource | | | | |
| get_default_resource | | | | |
| set_default_resource | | | | |
| Type-erased allocator support for existing classes | | | | |
| function | | | | |
| ****packaged_task**** | | | | |
| promise | | | | |

**This page is about the modified version of std::packaged_task with type-erased allocator support provided by the Library Fundamentals TSes. For the version of `packaged_task` provided by the concurrency TS supporting the `std::future` improvements made by that TS, see std::experimental::concurrency_v1::packaged_task.**

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/future>` |  |  |
| template< class > class packaged_task; //not defined | (1) | (library fundamentals TS) |
| template< class R, class ...Args >   class packaged_task<R(Args...)>; | (2) | (library fundamentals TS) |
|  |  |  |

`std::experimental::fundamentals_v1::packaged_task` (and `std::experimental::fundamentals_v2::packaged_task`) is a modified version of std::packaged_task provided by the library fundamentals TS with support for type-erased allocators.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `allocator_type` | std::experimental::erased_type |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the task object   (public member function) |
| get_memory_resource | retrieves a pointer to the memory resource used by this object to allocate memory   (public member function) |

### Non-member function

|  |  |
| --- | --- |
| std::experimental::swap(std::experimental::packaged_task) | specializes the `swap` algorithm   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::uses_allocator<std::experimental::packaged_task> | specializes the std::uses_allocator type trait   (class template specialization) |

## Members identical to std::packaged_task

### Member functions

|  |  |
| --- | --- |
| (destructor) | destructs the task object   (public member function of `std::packaged_task<R(Args...)>`) |
| operator= | moves the task object   (public member function of `std::packaged_task<R(Args...)>`) |
| valid | checks if the task object has a valid function   (public member function of `std::packaged_task<R(Args...)>`) |
| swap | swaps two task objects   (public member function of `std::packaged_task<R(Args...)>`) |
| Getting the result | |
| get_future | returns a std::future associated with the promised result   (public member function of `std::packaged_task<R(Args...)>`) |
| Execution | |
| operator()") | executes the function   (public member function of `std::packaged_task<R(Args...)>`) |
| make_ready_at_thread_exit | executes the function ensuring that the result is ready only once the current thread exits   (public member function of `std::packaged_task<R(Args...)>`) |
| reset | resets the state abandoning any stored results of previous executions   (public member function of `std::packaged_task<R(Args...)>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/lib_extensions/packaged_task&oldid=98618>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 January 2018, at 21:03.