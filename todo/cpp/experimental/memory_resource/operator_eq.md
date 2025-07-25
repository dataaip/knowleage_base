# operator==, operator!= (std::experimental::pmr::memory_resource)

From cppreference.com
< cpp‎ | experimental‎ | memory resource
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

std::experimental::pmr::memory_resource

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| memory_resource::memory_resource | | | | |
| Public member functions | | | | |
| memory_resource::allocate | | | | |
| memory_resource::deallocate | | | | |
| memory_resource::is_equal | | | | |
| Protected member functions | | | | |
| memory_resource::do_allocate | | | | |
| memory_resource::do_deallocate | | | | |
| memory_resource::do_is_equal | | | | |
| Non-member functions | | | | |
| ****operator==operator!=**** | | | | |

|  |  |  |
| --- | --- | --- |
| bool operator==( const memory_resource& a, const memory_resource& b ) noexcept; | (1) | (library fundamentals TS) |
| bool operator!=( const memory_resource& a, const memory_resource& b ) noexcept; | (2) | (library fundamentals TS) |
|  |  |  |

Compares the `memory_resource`s a and b for equality. Two `memory_resource`s compare equal if and only if memory allocated from one `memory_resource` can be deallocated from the other and vice versa.

### Return value

1) &a == &b || a.is_equal(b)2) !(a == b)

### See also

|  |  |
| --- | --- |
| is_equal | compare for equality with another `memory_resource`   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/memory_resource/operator_eq&oldid=154999>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 July 2023, at 06:19.