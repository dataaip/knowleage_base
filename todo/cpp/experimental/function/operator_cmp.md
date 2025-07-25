# operator==,!=(std::experimental::function)

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
| Defined in header `<experimental/functional>` |  |  |
| template< class R, class... ArgTypes >  bool operator==( const std::experimental::function<R(ArgTypes...)>& f, std::nullptr_t ) noexcept; | (1) | (library fundamentals TS) |
| template< class R, class... ArgTypes >  bool operator==( std::nullptr_t, const std::experimental::function<R(ArgTypes...)>& f ) noexcept; | (2) | (library fundamentals TS)  (removed in library fundamentals TS v3) |
| template< class R, class... ArgTypes >  bool operator!=( const std::experimental::function<R(ArgTypes...)>& f, std::nullptr_t ) noexcept; | (3) | (library fundamentals TS)  (removed in library fundamentals TS v3) |
| template< class R, class... ArgTypes >  bool operator!=( std::nullptr_t, const std::experimental::function<R(ArgTypes...)>& f ) noexcept; | (4) | (library fundamentals TS)  (removed in library fundamentals TS v3) |
|  |  |  |

Compares a `std::experimental::function` with a null pointer. Empty functions (that is, functions without a callable target) compare equal, non-empty functions compare non-equal.

|  |  |
| --- | --- |
| The `!=` operator is synthesized from `operator==`. | (library fundamentals TS v3) |

### Parameters

|  |  |  |
| --- | --- | --- |
| f | - | `std::experimental::function` to compare |

### Return value

1,2) !f3,4) (bool) f

### See also

|  |  |
| --- | --- |
| operator==operator!=(removed in C++20) | compares a std::function with nullptr   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/function/operator_cmp&oldid=157725>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 September 2023, at 00:01.