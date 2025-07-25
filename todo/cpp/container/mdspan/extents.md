# std::extents, std::dextents, std::dims

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | mdspan::mdspan | | | | | | mdspan::operator= | | | | | | Element access | | | | | | [mdspan::operator[]](operator_at.html "cpp/container/mdspan/operator at") | | | | | | Observers | | | | | | mdspan::rank | | | | | | mdspan::rank_dynamic | | | | | | mdspan::static_extent | | | | | | mdspan::extent | | | | | | mdspan::size | | | | | | mdspan::empty | | | | | | mdspan::stride | | | | | | mdspan::extents | | | | | | mdspan::data_handle | | | | | | mdspan::mapping | | | | | | mdspan::accessor | | | | | | mdspan::is_uniquemdspan::is_exhaustivemdspan::is_stridedmdspan::is_always_uniquemdspan::is_always_exhaustivemdspan::is_always_strided | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-member functions | | | | | | swap(std::mdspan) | | | | | | Subviews | | | | | | submdspan")(C++26) | | | | | | submdspan_extents")(C++26) | | | | | | Helper types and templates | | | | | | ****extentsdextents**** | | | | | | ****dims****(C++26) | | | | | | default_accessor | | | | | | aligned_accessor")(C++26) | | | | | | Layout mapping policies | | | | | | layout_left | | | | | | layout_right | | | | | | layout_stride | | | | | | layout_left_padded(C++26) | | | | | | layout_right_padded(C++26) | | | | | | Subviews helpers | | | | | | full_extent(C++26) | | | | | | strided_slice(C++26) | | | | | | submdspan_mapping_result(C++26) | | | | | | Deduction guides | | | | | |

****std::extents****

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
| extents::**index-cast** | | | | |
| extents::**dynamic-index** | | | | |
| extents::**dynamic-index-inv** | | | | |
| Non-member functions | | | | |
| extents::operator== | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<mdspan>` |  |  |
| template< class IndexType, std::size_t... Extents >  class extents; | (1) | (since C++23) |
| template< class IndexType, std::size_t Rank >  using dextents = /\* see below \*/ | (2) | (since C++23) |
| template< std::size_t Rank, class IndexType = std::size_t >  using dims = std::dextents<IndexType, Rank>; | (3) | (since C++26) |
|  |  |  |

1) Represents a multidimensional index space of rank equal to sizeof...(Extents).2) A convenient alias template for an all-dynamic `extents`. Let `d` denote std::dynamic_extent, each specialization of it dextents<IndexType, Rank> is equivalent to extents<IndexType /\*, d, d, ..., d\*/> (i.e. `d` is repeated a total of `Rank` times).3) A convenient alias template for an all-dynamic `extents` with std::size_t as the default index type.

Each specialization of `extents` models `regular` and is TriviallyCopyable.

### Template parameters

|  |  |  |
| --- | --- | --- |
| IndexType | - | the type of each non-dynamic `Extents`. Shall be a signed or unsigned integer type. Otherwise, the program is ill-formed |
| Extents | - | represents extent (size of an integer interval) for each rank index. Each element of it is either equal to std::dynamic_extent (in this case, it represents a **dynamic extent** and the extent size will be determined dynamically), or is representable as a value of type `IndexType` (then it represents a **static extent** and the extent size is just the value of it), or else the program is ill-formed |
| Rank | - | denotes the rank of an all-dynamic `extents` |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `index_type` | `IndexType` |
| `size_type` | std::make_unsigned_t<index_type> |
| `rank_type` | std::size_t |

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| std::array<index_type, rank_dynamic()> `dynamic-extents` (private) | An array which stores the size of each dynamic extents. (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs an `extents`   (public member function) |
| Observers | |
| rank[static] | returns the static rank of an `extents`   (public static member function) |
| rank_dynamic[static] | returns the dynamic rank of an `extents`   (public static member function) |
| static_extent[static] | returns static extent size of an `extents` at a certain rank index   (public static member function) |
| extent | returns dynamic extent size of an `extents` at a certain rank index   (public member function) |
| Helpers | |
| **fwd-prod-of-extents** | returns the product of extent size in range ``​0​`,`i`)` (exposition-only member function\*) |
| [**rev-prod-of-extents** | returns the product of extents size in range ``i + 1`,`rank()`)` (exposition-only member function\*) |
| [**index-cast** | casts the input into an integer type (exposition-only member function\*) |
| **dynamic-index**(private) | returns the number of dynamic extents below a certain rank index (exposition-only member function\*) |
| **dynamic-index-inv**(private) | returns the number `r` such that in range ``​0​`,`r + 1`)` there is exactly `i + 1` dynamic extents for a certain argument `i` (exposition-only member function\*) |

### Non-member functions

|  |  |
| --- | --- |
| [operator==(C++23) | compare underlying extents in each dimension of two `extents`   (function) |

### Deduction guides(C++23)

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| rank(C++11) | obtains the number of dimensions of an array type   (class template) |
| extent(C++11) | obtains the size of an array type along a specified dimension   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/mdspan/extents&oldid=177399>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 October 2024, at 20:48.