# std::layout_stride::mapping

From cppreference.com
< cpp‎ | container‎ | mdspan‎ | layout stride
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

****std::layout_stride::mapping****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| mapping::mapping") | | | | |
| Observers | | | | |
| mapping::extents | | | | |
| mapping::strides | | | | |
| mapping::required_span_size | | | | |
| mapping::operator()") | | | | |
| mapping::is_uniquemapping::is_exhaustivemapping::is_stridedmapping::is_always_uniquemapping::is_always_exhaustivemapping::is_always_strided | | | | |
| mapping::stride | | | | |
| Non-member functions | | | | |
| operator== | | | | |
| submdspan_mapping(std::layout_stride::mapping)")(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<mdspan>` |  |  |
| template< class Extents >  class layout_stride::mapping; |  | (since C++23) |
|  |  |  |

The class template `layout_stride::mapping` controls how multidimensional indices are mapped with user-defined strides to a one-dimensional value representing the offset.

Every specialization of `mapping` is a LayoutMapping and a TriviallyCopyable type which satisfies `regular`.

The program is ill-formed if the size of the multidimensional index space Extents() is not representable as a value of type Extents::index_type when Extents::rank_dynamic() is ​0​.

### Template parameters

|  |  |  |
| --- | --- | --- |
| Extents | - | specifies number of dimensions, their sizes, and which are known at compile time. Must be a specialization of `std::extents`. |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `extents_type` | `Extents` |
| `index_type` | `extents_type::index_type` |
| `size_type` | `extents_type::size_type` |
| `rank_type` | `extents_type::rank_type` |
| `layout_type` | std::layout_stride |

### Member constants

|  |  |
| --- | --- |
| Member | Definition |
| constexpr rank_type `rank_`  (private) [static] | extents_type::rank() (exposition-only static member constant\*) |

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| `extents_type` `extents_` (private) | the extents object (exposition-only member object\*) |
| std::array<index_type, rank_> `strides_` (private) | the array of strides (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor)") | constructs a new mapping   (public member function) |
| operator=(explicitly defaulted) | assigns a mapping   (public member function) |
| Observers | |
| extents | obtains the extents object   (public member function) |
| strides | obtains the array of strides   (public member function) |
| required_span_size | returns the required size of the mapping   (public member function) |
| operator()") | maps a multidimensional index into an offset value   (public member function) |
| is_unique[static] | determines if this mapping is unique (every combination of indices maps to a different underlying element)   (public static member function) |
| is_exhaustive | determines if this mapping is exhaustive (every underlying element can be accessed with some combination of indices)   (public member function) |
| is_strided[static] | determines if this mapping is strided (in each dimension, incrementing an index jumps over the same number of underlying elements every time)   (public static member function) |
| is_always_unique[static] | determines if this layout mapping is always unique   (public static member function) |
| is_always_exhaustive[static] | determines if this layout mapping is always exhaustive   (public static member function) |
| is_always_strided[static] | determines if this layout mapping is always strided   (public static member function) |
| stride | obtains the stride along the specified dimension   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator== | compares this layout mapping of `layout_stride` with other mapping   (function template) |
| submdspan_mapping(std::layout_stride::mapping)")(C++26) | calculates the mapping and data handle offset used for `subdmspan`   (public member function) |

### See also

|  |  |
| --- | --- |
| mapping | a layout mapping of layout_left (public member class template of `std::layout_left`) |
| mapping | a layout mapping of layout_right (public member class template of `std::layout_right`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/mdspan/layout_stride/mapping&oldid=178732>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 December 2024, at 18:24.