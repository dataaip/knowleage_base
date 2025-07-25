# std::experimental::promise (library fundamentals TS)

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
| packaged_task | | | | |
| ****promise**** | | | | |

**This page is about the modified version of std::promise with type-erased allocator support provided by the Library Fundamentals TSes. For the version of `promise` provided by the concurrency TS supporting the `std::future` improvements made by that TS, see std::experimental::concurrency_v1::promise.**

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/future>` |  |  |
| template< class R > class promise; | (1) | (library fundamentals TS) |
| template< class R > class promise<R&>; | (2) | (library fundamentals TS) |
| template<>          class promise<void>; | (3) | (library fundamentals TS) |
|  |  |  |

`std::experimental::fundamentals_v1::promise` (and `std::experimental::fundamentals_v2::promise`) is a modified version of std::promise provided by the library fundamentals TS with support for type-erased allocators.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `allocator_type` | std::experimental::erased_type |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the promise object   (public member function) |
| get_memory_resource | retrieves a pointer to the memory resource used by this object to allocate memory   (public member function) |

### Non-member function

|  |  |
| --- | --- |
| std::experimental::swap(std::experimental::promise) | specializes the `swap` algorithm   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::uses_allocator<std::experimental::promise> | specializes the std::uses_allocator type trait   (class template specialization) |

## Members identical to std::promise

### Member functions

|  |  |
| --- | --- |
| (destructor) | destructs the promise object   (public member function of `std::promise<R>`) |
| operator= | assigns the shared state   (public member function of `std::promise<R>`) |
| swap | swaps two promise objects   (public member function of `std::promise<R>`) |
| Getting the result | |
| get_future | returns a future associated with the promised result   (public member function of `std::promise<R>`) |
| Setting the result | |
| set_value | sets the result to specific value   (public member function of `std::promise<R>`) |
| set_value_at_thread_exit | sets the result to specific value while delivering the notification only at thread exit   (public member function of `std::promise<R>`) |
| set_exception | sets the result to indicate an exception   (public member function of `std::promise<R>`) |
| set_exception_at_thread_exit | sets the result to indicate an exception while delivering the notification only at thread exit   (public member function of `std::promise<R>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/lib_extensions/promise&oldid=98608>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 January 2018, at 17:49.