# std::extents<IndexType,Extents...>::**index-cast**

From cppreference.com
< cpp‎ | container‎ | mdspan‎ | extents
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | mdspan::mdspan | | | | | | mdspan::operator= | | | | | | Element access | | | | | | [mdspan::operator[]](../operator_at.html "cpp/container/mdspan/operator at") | | | | | | Observers | | | | | | mdspan::rank | | | | | | mdspan::rank_dynamic | | | | | | mdspan::static_extent | | | | | | mdspan::extent | | | | | | mdspan::size | | | | | | mdspan::empty | | | | | | mdspan::stride | | | | | | mdspan::extents | | | | | | mdspan::data_handle | | | | | | mdspan::mapping | | | | | | mdspan::accessor | | | | | | mdspan::is_uniquemdspan::is_exhaustivemdspan::is_stridedmdspan::is_always_uniquemdspan::is_always_exhaustivemdspan::is_always_strided | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-member functions | | | | | | swap(std::mdspan) | | | | | | Subviews | | | | | | submdspan")(C++26) | | | | | | submdspan_extents")(C++26) | | | | | | Helper types and templates | | | | | | extentsdextents | | | | | | dims(C++26) | | | | | | default_accessor | | | | | | aligned_accessor")(C++26) | | | | | | Layout mapping policies | | | | | | layout_left | | | | | | layout_right | | | | | | layout_stride | | | | | | layout_left_padded(C++26) | | | | | | layout_right_padded(C++26) | | | | | | Subviews helpers | | | | | | full_extent(C++26) | | | | | | strided_slice(C++26) | | | | | | submdspan_mapping_result(C++26) | | | | | | Deduction guides | | | | | |

std::extents

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| extents::extents | | | | |
| Observers | | | | |
| extents::rank | | | | |
| extents::rank_dynamic | | | | |
| extents::static_extent | | | | |
| extents::extent | | | | |
| Helpers | | | | |
| extents::**fwd-prod-of-extents** | | | | |
| extents::**rev-prod-of-extents** | | | | |
| ****extents::**index-cast****** | | | | |
| extents::**dynamic-index** | | | | |
| extents::**dynamic-index-inv** | | | | |
| Non-member functions | | | | |
| extents::operator== | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| template< class OtherIndexType >  static constexpr auto /\*index-cast\*/( OtherIndexType&& i ) noexcept; |  | (since C++23)  (exposition only\*) |
|  |  |  |

Casts the index i of type `OtherIndexType` into a certain integral type.

It is equivalent to:

- return i;, if `OtherIndexType` is an integral type other than bool and
- return static_cast<index_type>(i); otherwise.

### Parameters

|  |  |  |
| --- | --- | --- |
| i | - | the index to be cast |

### Return value

Cast index.

### Notes

A call to this function will always return an integral type other than bool. Integer-class types can use the static_cast branch without loss of precision because this function's call sites are already constrained on the convertibility of `OtherIndexType` to `index_type`.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/mdspan/extents/index-cast&oldid=178730>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 December 2024, at 17:29.