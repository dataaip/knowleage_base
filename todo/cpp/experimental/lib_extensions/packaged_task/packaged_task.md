# std::experimental::packaged_task<R(Args...)>::packaged_task (library fundamentals TS)

From cppreference.com
< cpp‎ | experimental‎ | lib extensions‎ | packaged task
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
| promise | | | | |

|  |  |  |
| --- | --- | --- |
| packaged_task() noexcept; | (1) | (library fundamentals TS) |
| template< class F >  explicit packaged_task( F&& f ); | (2) | (library fundamentals TS) |
| template< class F, class Allocator >  explicit packaged_task( std::allocator_arg_t, const Allocator& alloc, F&& f ); | (3) | (library fundamentals TS) |
| packaged_task( const packaged_task& ) = delete; | (4) | (library fundamentals TS) |
| packaged_task( packaged_task&& rhs ) noexcept; | (5) | (library fundamentals TS) |
|  |  |  |

Constructs a new `std::experimental::packaged_task` object.

1) Constructs a `std::experimental::packaged_task` object with no task and no shared state.2) Constructs a `std::experimental::packaged_task` object with a shared state and a copy of the task, initialized with std::forward<F>(f). This constructor does not participate in overload resolution if std::decay<F>::type is the same type as std::packaged_task<R(ArgTypes...)>.3) Constructs a `std::experimental::packaged_task` object with a shared state and a copy of the task, initialized with std::forward<F>(f). Uses the provided allocator to allocate memory necessary to store the task, which is treated as a type-erased allocator (see below). This constructor does not participate in overload resolution if std::decay<F>::type is the same type as std::packaged_task<R(ArgTypes...)>.4) The copy constructor is deleted, `std::experimental::packaged_task` is move-only.5) Constructs a `std::experimental::packaged_task` with the shared state and task formerly owned by rhs, leaving rhs with no shared state and a moved-from task.

### Type-erased allocator

The constructors of `packaged_task` taking an allocator argument `alloc` treats that argument as a type-erased allocator. The memory resource pointer used by `packaged_task` to allocate memory is determined using the allocator argument (if specified) as follows:

|  |  |
| --- | --- |
| Type of `alloc` | Value of the memory resource pointer |
| Non-existent (no allocator specified at time of construction) | The value of std::experimental::pmr::get_default_resource() at time of construction. |
| std::nullptr_t | The value of std::experimental::pmr::get_default_resource() at time of construction. |
| A pointer type convertible to std::experimental::pmr::memory_resource\* | static_cast<std::experimental::pmr::memory_resource\*>(alloc) |
| A specialization of std::experimental::pmr::polymorphic_allocator | alloc.resource() |
| Any other type meeting the Allocator requirements | A pointer to a value of type std::experimental::pmr::resource_adaptor<A>(alloc), where `A` is the type of `alloc`. The pointer remains valid only for the lifetime of the `packaged_task` object. |
| None of the above | The program is ill-formed. |

### Parameters

|  |  |  |
| --- | --- | --- |
| f | - | the callable target (function, member function, lambda-expression, functor) to execute |
| alloc | - | the allocator to use when storing the task |
| rhs | - | the `std::experimental::packaged_task` to move from |

### Exceptions

2,3) Any exceptions thrown by copy/move constructor of f and possiblly std::bad_alloc if the allocation fails.4) (none)
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/lib_extensions/packaged_task/packaged_task&oldid=157738>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 September 2023, at 22:29.