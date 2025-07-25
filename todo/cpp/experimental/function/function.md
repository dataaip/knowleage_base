# std::experimental::function<R(Args...)>::function

From cppreference.com
< cpp‎ | experimental‎ | function
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
| function() noexcept; | (1) | (library fundamentals TS) |
| function( std::nullptr_t ) noexcept; | (2) | (library fundamentals TS) |
| function( const function& other ); | (3) | (library fundamentals TS) |
| function( function&& other ); | (4) | (library fundamentals TS) |
| template< class F >   function( F f ); | (5) | (library fundamentals TS) |
|  |  |  |
| --- | --- | --- |
|  | (6) |  |
| template< class Alloc >  function( std::allocator_arg_t, const Alloc& alloc ) noexcept; |  | (library fundamentals TS) |
| function( std::allocator_arg_t,            const allocator_type& alloc ) noexcept; |  | (library fundamentals TS v3) |
|  |  |  |
| --- | --- | --- |
|  | (7) |  |
| template< class Alloc >  function( std::allocator_arg_t, const Alloc& alloc, std::nullptr_t ) noexcept; |  | (library fundamentals TS) |
| function( std::allocator_arg_t, const allocator_type& alloc,             std::nullptr_t ) noexcept; |  | (library fundamentals TS v3) |
|  |  |  |
| --- | --- | --- |
|  | (8) |  |
| template< class Alloc >  function( std::allocator_arg_t, const Alloc& alloc, const function& other ); |  | (library fundamentals TS) |
| function( std::allocator_arg_t, const allocator_type& alloc,             const function& other ); |  | (library fundamentals TS v3) |
|  |  |  |
| --- | --- | --- |
|  | (9) |  |
| template< class Alloc >  function( std::allocator_arg_t, const Alloc& alloc,           function&& other ); |  | (library fundamentals TS) |
| function( std::allocator_arg_t, const allocator_type& alloc,             function&& other ); |  | (library fundamentals TS v3) |
|  |  |  |
| --- | --- | --- |
|  | (10) |  |
| template< class F, class Alloc >   function( std::allocator_arg_t, const Alloc& alloc, F f ); |  | (library fundamentals TS) |
| function( std::allocator_arg_t, const allocator_type& alloc, F f ); |  | (library fundamentals TS v3) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Constructs a `std::experimental::function` from a variety of sources.

1,2) Creates an **empty** function.3) Copies the **target** of other to the **target** of \*this. If other is **empty**, \*this will be **empty** after the call too.4) Moves the **target** of other to the **target** of \*this. If other is **empty**, \*this will be **empty** after the call too. After construction, \*this stores a copy of other.get_allocator().(library fundamentals TS v3)5) Initializes the **target** with a copy of f. If f is a null pointer to function or null pointer to member, \*this will be **empty** after the call. This constructor does not participate in overload resolution unless f is Callable for argument types `Args...` and return type `R`.6-10) Same as (1-5) except that alloc is used to allocate memory for any internal data structures that the `function` might use. These constructors treat alloc as a type-erased allocator (see below).(until library fundamentals TS v3)

|  |  |
| --- | --- |
| After construction via (1-5), this->get_memory_resource() returns the same value as std::experimental::pmr::get_default_resource() during construction. | (library fundamentals TS) (until library fundamentals TS v3) |
| After construction via (1-3) and (5), \*this stores a default constructed std::pmr::polymorphic_allocator<>. | (library fundamentals TS v3) |

When the **target** is a function pointer or a std::reference_wrapper, small object optimization is guaranteed, that is, these targets are always directly stored inside the std::experimental::function object, no dynamic allocation takes place. Other large objects may be constructed in dynamic allocated storage and accessed by the std::experimental::function object through a pointer.

If a constructor moves or copies a function object, including an instance of `std::experimental::function`, then that move or copy is performed by **using-allocator construction** with allocator this->get_memory_resource()(until library fundamentals TS v3)this->get_allocator()(library fundamentals TS v3).

### Type-erased allocator

The constructors of `function` taking an allocator argument `alloc` treats that argument as a type-erased allocator. The memory resource pointer used by `function` to allocate memory is determined using the allocator argument (if specified) as follows:

|  |  |
| --- | --- |
| Type of `alloc` | Value of the memory resource pointer |
| Non-existent (no allocator specified at time of construction) | The value of std::experimental::pmr::get_default_resource() at time of construction. |
| std::nullptr_t | The value of std::experimental::pmr::get_default_resource() at time of construction. |
| A pointer type convertible to std::experimental::pmr::memory_resource\* | static_cast<std::experimental::pmr::memory_resource\*>(alloc) |
| A specialization of std::experimental::pmr::polymorphic_allocator | alloc.resource() |
| Any other type meeting the Allocator requirements | A pointer to a value of type std::experimental::pmr::resource_adaptor<A>(alloc), where `A` is the type of `alloc`. The pointer remains valid only for the lifetime of the `function` object. |
| None of the above | The program is ill-formed. |

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | the function object used to initialize \*this |
| f | - | a callable used to initialize \*this |
| alloc | - | an allocator used for internal memory allocation |
| Type requirements | | |
| -`F` must meet the requirements of Callable and CopyConstructible. | | |

### Exceptions

3,8) Does not throw if other's **target** is a function pointer or a std::reference_wrapper, otherwise may throw std::bad_alloc or any exception thrown by the copy constructor of the stored callable object.4) (none)5,10) Does not throw if f is a function pointer or a std::reference_wrapper, otherwise may throw std::bad_alloc or any exception thrown by the copy constructor of the stored callable object.9) (none)

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/function/function&oldid=157724>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 September 2023, at 23:56.