# std::experimental::pmr::monotonic_buffer_resource::monotonic_buffer_resource

From cppreference.com
< cpp‎ | experimental‎ | monotonic buffer resource
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

std::experimental::pmr::monotonic_buffer_resource

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****monotonic_buffer_resource::monotonic_buffer_resource**** | | | | |
| monotonic_buffer_resource::~monotonic_buffer_resource | | | | |
| Public member functions | | | | |
| monotonic_buffer_resource::release | | | | |
| monotonic_buffer_resource::upstream_resource | | | | |
| Protected member functions | | | | |
| monotonic_buffer_resource::do_allocate | | | | |
| monotonic_buffer_resource::do_deallocate | | | | |
| monotonic_buffer_resource::do_is_equal | | | | |

|  |  |  |
| --- | --- | --- |
| monotonic_buffer_resource(); | (1) | (library fundamentals TS) |
| explicit monotonic_buffer_resource( memory_resource\* upstream ); | (2) | (library fundamentals TS) |
| explicit monotonic_buffer_resource( std::size_t initial_size ); | (3) | (library fundamentals TS) |
| monotonic_buffer_resource( std::size_t initial_size,                             memory_resource\* upstream ); | (4) | (library fundamentals TS) |
| monotonic_buffer_resource( void\* buffer, std::size_t buffer_size ); | (5) | (library fundamentals TS) |
| monotonic_buffer_resource( void\* buffer, std::size_t buffer_size,                             memory_resource\* upstream ); | (6) | (library fundamentals TS) |
| monotonic_buffer_resource( const monotonic_buffer_resource& ) = delete; | (7) | (library fundamentals TS) |
|  |  |  |

Constructs a `monotonic_buffer_resource`. The constructors not taking an upstream memory resource pointer uses the return value of std::experimental::pmr::get_default_resource() as the upstream memory resource.

1,2) Sets the **current buffer** to null and the **next buffer size** to an implementation-defined size.3,4) Sets the **current buffer** to null and the **next buffer size** to a size no smaller than initial_size.5,6) Sets the **current buffer** to buffer and the **next buffer size** to buffer_size (but not less than 1). Then increase the **next buffer size** by an implementation-defined growth factor (which does not have to be integral).7) Copy constructor is deleted.

### Parameters

|  |  |  |
| --- | --- | --- |
| upstream | - | the upstream memory resource to use; must point to a valid memory resource |
| initial_size | - | the minimum size of the first buffer to allocate; must be greater than zero |
| buffer | - | the initial buffer to use |
| buffer_size | - | the size of the initial buffer; cannot be greater than the number of bytes in buffer |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/monotonic_buffer_resource/monotonic_buffer_resource&oldid=157740>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 September 2023, at 22:37.