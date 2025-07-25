# std::experimental::pmr::monotonic_buffer_resource::do_allocate

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
| monotonic_buffer_resource::monotonic_buffer_resource | | | | |
| monotonic_buffer_resource::~monotonic_buffer_resource | | | | |
| Public member functions | | | | |
| monotonic_buffer_resource::release | | | | |
| monotonic_buffer_resource::upstream_resource | | | | |
| Protected member functions | | | | |
| ****monotonic_buffer_resource::do_allocate**** | | | | |
| monotonic_buffer_resource::do_deallocate | | | | |
| monotonic_buffer_resource::do_is_equal | | | | |

|  |  |  |
| --- | --- | --- |
| virtual void\* do_allocate( std::size_t bytes, std::size_t alignment ); |  | (library fundamentals TS) |
|  |  |  |

Allocates storage.

If the **current buffer** has sufficient unused space to fit a block with the specified size and alignment, allocates the return block from the current buffer.

Otherwise, this function allocates a new buffer by calling `upstream_resource()->allocate(n, m)`, where `n` is not less than the greater of bytes and the **next buffer size** and `m` is not less than alignment. It sets the new buffer as the **current buffer**, increases the **next buffer size** by an implementation-defined growth factor (which is not necessarily integral), and then allocates the return block from the newly allocated buffer.

### Return value

A pointer to allocated storage of at least bytes bytes in size, aligned to the specified alignment if such alignment is supported, and to alignof(std::max_align_t) otherwise.

### Exceptions

Throws nothing unless calling `allocate()` on the upstream memory resource throws.

### See also

|  |  |
| --- | --- |
| allocate | allocates memory   (public member function of `std::experimental::pmr::memory_resource`) |
| do_allocate[virtual] | allocates memory   (virtual protected member function of `std::experimental::pmr::memory_resource`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/monotonic_buffer_resource/do_allocate&oldid=155000>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 July 2023, at 06:24.