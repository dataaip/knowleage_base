# std::layout_right

From cppreference.com
< cpp‎ | container‎ | mdspan
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

Containers library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Sequence | | | | |
| array(C++11) | | | | |
| vector | | | | |
| vector<bool> | | | | |
| inplace_vector(C++26) | | | | |
| deque | | | | |
| forward_list(C++11) | | | | |
| list | | | | |
| Associative | | | | |
| set | | | | |
| multiset | | | | |
| map | | | | |
| multimap | | | | |
| Unordered associative | | | | |
| unordered_set(C++11) | | | | |
| unordered_multiset(C++11) | | | | |
| unordered_map(C++11) | | | | |
| unordered_multimap(C++11) | | | | |
| Adaptors | | | | |
| stack | | | | |
| queue | | | | |
| priority_queue | | | | |
| flat_set(C++23) | | | | |
| flat_multiset(C++23) | | | | |
| flat_map(C++23) | | | | |
| flat_multimap(C++23) | | | | |
| Views | | | | |
| span(C++20) | | | | |
| mdspan(C++23) | | | | |
| Tables | | | | |
| Iterator invalidation | | | | |
| Member function table | | | | |
| Non-member function table | | | | |

std::mdspan

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | mdspan::mdspan | | | | | | mdspan::operator= | | | | | | Element access | | | | | | [mdspan::operator[]](operator_at.html "cpp/container/mdspan/operator at") | | | | | | Observers | | | | | | mdspan::rank | | | | | | mdspan::rank_dynamic | | | | | | mdspan::static_extent | | | | | | mdspan::extent | | | | | | mdspan::size | | | | | | mdspan::empty | | | | | | mdspan::stride | | | | | | mdspan::extents | | | | | | mdspan::data_handle | | | | | | mdspan::mapping | | | | | | mdspan::accessor | | | | | | mdspan::is_uniquemdspan::is_exhaustivemdspan::is_stridedmdspan::is_always_uniquemdspan::is_always_exhaustivemdspan::is_always_strided | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-member functions | | | | | | swap(std::mdspan) | | | | | | Subviews | | | | | | submdspan")(C++26) | | | | | | submdspan_extents")(C++26) | | | | | | Helper types and templates | | | | | | extentsdextents | | | | | | dims(C++26) | | | | | | default_accessor | | | | | | aligned_accessor")(C++26) | | | | | | Layout mapping policies | | | | | | layout_left | | | | | | ****layout_right**** | | | | | | layout_stride | | | | | | layout_left_padded(C++26) | | | | | | layout_right_padded(C++26) | | | | | | Subviews helpers | | | | | | full_extent(C++26) | | | | | | strided_slice(C++26) | | | | | | submdspan_mapping_result(C++26) | | | | | | Deduction guides | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<mdspan>` |  |  |
| struct layout_right; |  | (since C++23) |
|  |  |  |

`layout_right` is a LayoutMappingPolicy which provides a layout mapping where the rightmost extent has stride 1, and strides increase right-to-left as the product of extents.

|  |  |
| --- | --- |
| `layout_right` is a TrivialType. | (until C++26) |
| `layout_right` is TriviallyCopyable, and std::is_trivially_default_constructible_v<layout_right> is true. | (since C++26) |

It is the default layout mapping policy used by std::mdspan if no user-specified layout is provided.

### Nested class templates

|  |  |
| --- | --- |
| mapping | a layout mapping of layout_right (public member class template) |

### See also

|  |  |
| --- | --- |
| layout_right_padded(C++26) | row-major layout mapping policy with padding stride that can be greater than or equal to the rightmost extent   (class template) |
| layout_left(C++23) | column-major multidimensional array layout mapping policy; leftmost extent has stride `1`   (class) |
| layout_stride(C++23) | a layout mapping policy with user-defined strides   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/mdspan/layout_right&oldid=178060>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 November 2024, at 01:28.