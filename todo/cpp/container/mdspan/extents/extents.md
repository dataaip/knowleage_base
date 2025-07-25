# std::extents<IndexType,Extents...>::extents

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
| ****extents::extents**** | | | | |
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
| constexpr extents() = default; | (1) | (since C++23) |
| template< class OtherIndexType, std::size_t... OtherExtents >  constexpr explicit(/\*see below\*/)     extents( const std::extents<OtherIndexType, OtherExtents...>& other ) noexcept; | (2) | (since C++23) |
| template< class... OtherIndexTypes >  constexpr explicit extents( OtherIndexTypes... exts ) noexcept; | (3) | (since C++23) |
| template< class OtherIndexType, std::size_t N >  constexpr explicit(N != rank_dynamic())     extents( std::span<OtherIndexType, N> exts ) noexcept; | (4) | (since C++23) |
| template< class OtherIndexType, std::size_t N >  constexpr explicit(N != rank_dynamic())     extents( const std::array<OtherIndexType, N>& exts ) noexcept; | (5) | (since C++23) |
|  |  |  |

Construct an `extents`. One can construct `extents` from just dynamic extents, which are all the values getting stored, or from all the extents with a precondition.

1) Default constructor. Initializes all dynamic extents to zero.2) Conversion from another `extents` object. After construction, \*this == other is true.

- The behavior is undefined if

:   - other.extent(r) != static_extent(r) for any r for which static_extent(r) represents a static extent, or
    - other.extent(r) is not representable as a value of type IndexType for any rank value r in other.

- This overload participates in overload resolution only if

:   - sizeof...(OtherExtents) == rank() is true, and
    - ((OtherExtents == std::dynamic_extent || Extents == std::dynamic_extent ||  
        OtherExtents == Extents) && ...) is true.

- This constructor is explicit if

:   - ((Extents != std::dynamic_extent && OtherExtents == std::dynamic_extent) || ...) is true, or
    - std::numeric_limits<IndexType>::max() < std::numeric_limits<OtherIndexType>::max() is true.

3) Let N be sizeof...(exts) and exts_arr be std::array<IndexType, N>{static_cast<IndexType>(std::move(exts))...}, equivalent to extents(exts_arr).

- This overload participates in overload resolution only if

:   - (std::is_convertible_v<OtherIndexTypes, IndexType> && ...) is true,
    - (std::is_nothrow_constructible_v<IndexType, OtherIndexTypes> && ...) is true, and
    - N == rank_dynamic() || N == rank() is true.

- The behavior is undefined if

:   - N != rank_dynamic() and exts_arr[r] is not equal to static_extent(r) for any r for which static_extent(r) represents a static extent, or
    - an element in exts is negative or not representable as a value of type IndexType.

4,5) If N equals rank_dynamic(), for all d in ``​0​`,`rank_dynamic()`)`, [direct-non-list-initializes `dynamic-extents`[d] with std::as_const(exts[d]). Otherwise, for all d in `[`​0​`,`rank_dynamic()`)`, direct-non-list-initializes `dynamic-extents`[d] with std::as_const(exts[`dynamic-index-inv`(d)]).

- This overload participates in overload resolution only if

:   - std::is_convertible_v<const OtherIndexType&, IndexType> is true,
    - std::is_nothrow_constructible_v<IndexType, const OtherIndexType&> is true, and
    - N == rank_dynamic() || N == rank() is true.

- The behavior is undefined if

:   - N != rank_dynamic() and exts[r] is not equal to static_extent(r) for any r for which static_extent(r) represents a static extent, or
    - exts[r] is negative or not representable as a value of type IndexType for any rank index r.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `extents` to convert from |
| exts | - | represents the extents |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |  |  |
| --- | --- | --- | --- |
| |  |  | | --- | --- | |  | This section is incomplete | | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/mdspan/extents/extents&oldid=172200>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 June 2024, at 19:48.