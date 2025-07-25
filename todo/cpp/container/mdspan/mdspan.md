# std::mdspan<T,Extents,LayoutPolicy,AccessorPolicy>::mdspan

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | ****mdspan::mdspan**** | | | | | | mdspan::operator= | | | | | | Element access | | | | | | [mdspan::operator[]](operator_at.html "cpp/container/mdspan/operator at") | | | | | | Observers | | | | | | mdspan::rank | | | | | | mdspan::rank_dynamic | | | | | | mdspan::static_extent | | | | | | mdspan::extent | | | | | | mdspan::size | | | | | | mdspan::empty | | | | | | mdspan::stride | | | | | | mdspan::extents | | | | | | mdspan::data_handle | | | | | | mdspan::mapping | | | | | | mdspan::accessor | | | | | | mdspan::is_uniquemdspan::is_exhaustivemdspan::is_stridedmdspan::is_always_uniquemdspan::is_always_exhaustivemdspan::is_always_strided | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Non-member functions | | | | | | swap(std::mdspan) | | | | | | Subviews | | | | | | submdspan")(C++26) | | | | | | submdspan_extents")(C++26) | | | | | | Helper types and templates | | | | | | extentsdextents | | | | | | dims(C++26) | | | | | | default_accessor | | | | | | aligned_accessor")(C++26) | | | | | | Layout mapping policies | | | | | | layout_left | | | | | | layout_right | | | | | | layout_stride | | | | | | layout_left_padded(C++26) | | | | | | layout_right_padded(C++26) | | | | | | Subviews helpers | | | | | | full_extent(C++26) | | | | | | strided_slice(C++26) | | | | | | submdspan_mapping_result(C++26) | | | | | | Deduction guides | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr mdspan(); | (1) | (since C++23) |
| template< class... OtherIndexTypes >      constexpr explicit mdspan( data_handle_type p, OtherIndexTypes... exts ); | (2) | (since C++23) |
| template< class OtherIndexType, std::size_t N >  constexpr explicit(N != rank_dynamic())         mdspan( data_handle_type p, std::span<OtherIndexType, N> exts ); | (3) | (since C++23) |
| template< class OtherIndexType, std::size_t N >  constexpr explicit(N != rank_dynamic())         mdspan( data_handle_type p, const std::array<OtherIndexType, N>& exts ); | (4) | (since C++23) |
| constexpr mdspan( data_handle_type p, const extents_type& ext ); | (5) | (since C++23) |
| constexpr mdspan( data_handle_type p, const mapping_type& m ); | (6) | (since C++23) |
| constexpr mdspan( data_handle_type p, const mapping_type& m,                    const accessor_type& a ); | (7) | (since C++23) |
| template< class OtherElementType, class OtherExtents,  class OtherLayoutPolicy, class OtherAccessor >      constexpr explicit(/\* see below \*/)          mdspan( const mdspan<OtherElementType, OtherExtents,                              OtherLayoutPolicy, OtherAccessor>& other ); | (8) | (since C++23) |
| constexpr mdspan( const mdspan& rhs ) = default; | (9) | (since C++23) |
| constexpr mdspan( mdspan&& rhs ) = default; | (10) | (since C++23) |
|  |  |  |

Constructs an `mdspan`, optionally using user-supplied data handle p, layout mapping m, and accessor a. If extents exts or ext are supplied, they are converted to extents_type and used to initialize the layout mapping.

1) Constructs an empty mdspan. Value-initializes `ptr_`, `map_`, and `acc_`.

- The behavior is undefined if ``​0​`,`map_.required_span_size()`)` is not an accessible range of [`ptr_` and `acc_` for the values of `map_` and `acc_` after the invocation of this constructor.
- This overload participates in overload resolution only if

:   - rank_dynamic() > 0 is true,
    - std::is_default_constructible_v<data_handle_type> is true,
    - std::is_default_constructible_v<mapping_type> is true, and
    - std::is_default_constructible_v<accessor_type> is true.

2) Constructs an mdspan over the underlying data referred by p with extents represented by `exts...`. Value-initializes `acc_`, direct-non-list-initializes `ptr_` with std::move(p) and `map_` with extents_type(static_cast<index_type>(std::move(exts))...).

- The behavior is undefined if ``​0​`,`map_.required_span_size()`)` is not an accessible range of [`ptr_` and `acc_` for the values of `map_` and `acc_` after the invocation of this constructor.
- Let N be sizeof...(OtherIndexTypes). This overload participates in overload resolution only if

:   - (std::is_convertible_v<OtherIndexTypes, index_type> && ...) is true,
    - (std::is_nothrow_constructible<index_type, OtherIndexTypes> && ...) is true,
    - N == rank() || N == rank_dynamic() is true,
    - std::is_constructible_v<mapping_type, extents_type> is true, and
    - std::is_default_constructible_v<accessor_type> is true.

3,4) Constructs an mdspan over the underlying data referred by p with extents represented by pack exts. Value-initializes `acc_`, direct-non-list-initializes `ptr_` with std::move(p) and `map_` with extents_type(exts).

- The behavior is undefined if ``​0​`,`map_.required_span_size()`)` is not an accessible range of [`ptr_` and `acc_` for the values of `map_` and `acc_` after the invocation of this constructor.
- This overload participates in overload resolution only if

:   - std::is_convertible_v<const OtherIndexTypes&, index_type> is true,
    - std::is_nothrow_constructible<index_type, const OtherIndexTypes&> is true,
    - N == rank() || N == rank_dynamic() is true,
    - std::is_constructible_v<mapping_type, extents_type> is true, and
    - std::is_default_constructible_v<accessor_type> is true.

5) Constructs an mdspan over the underlying data referred by p with extents represented by ext. Value-initializes `acc_`, direct-non-list-initializes `ptr_` with std::move(p) and `map_` with exts.

- The behavior is undefined if ``​0​`,`map_.required_span_size()`)` is not an accessible range of p and [`acc_` for the values of `map_` and `acc_` after the invocation of this constructor.
- This overload participates in overload resolution only if

:   - std::is_constructible_v<mapping_type, const mapping_type&> is true, and
    - std::is_default_constructible_v<accessor_type> is true.

6) Constructs an mdspan over the underlying data referred by p with layout mapping m. Value-initializes `acc_`, direct-non-list-initializes `ptr_` with std::move(p) and `map_` with m.

- The behavior is undefined if ``​0​`,`m.required_span_size()`)` is not an accessible range of p and [`acc_` for the values of `acc_` after the invocation of this constructor.
- This overload participates in overload resolution only if std::is_default_constructible_v<accessor_type> is true.
7) Constructs an mdspan over the underlying data referred by p with layout mapping m and accessor a. Direct-non-list-initializes `ptr_` with std::move(p), `map_` with m and `acc_` with a.

- The behavior is undefined if ``​0​`,`m.required_span_size()`)` is not an accessible range of p and a after the invocation of this constructor.
8) Converting constructor from another mdspan. [Direct-non-list-initializes `ptr_` with other.ptr_, `map_` with other.map_ and `acc_` with other.acc_.

- The behavior is undefined if :

:   - ``​0​`,`map_.required_span_size()`)` is not an accessible range of [`ptr_` and `acc_` for the values of `map_` and `acc_` after the invocation of this constructor, or
    - for each rank index `r` of extents_type,    extents_type::static_extent(r) == std::dynamic_extent  
      || extents_type::static_extent(r) == other.extent(r) is false.

- This overload participates in overload resolution only if

:   - std::is_constructible_v<mapping_type, const OtherLayoutPolicy​::  
          ​template mapping<OtherExtents>&> is true, and
    - std::is_constructible_v<accessor_type, const OtherAccessor&> is true.

- The program is ill-formed if:

:   - std::is_constructible_v<data_handle_type,  
          const OtherAccessor​::​data_handle_type&> is false, or
    - std::is_constructible_v<extents_type, OtherExtents> is false.

- The expression inside explicit is equivalent to:    !std::is_convertible_v<const OtherLayoutPolicy::  
         template mapping<OtherExtents>&, mapping_type>  
  || !std::is_convertible_v<const OtherAccessor&, accessor_type>
9) Defaulted copy constructor.10) Defaulted move constructor.

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | a handle to the underlying data |
| m | - | a layout mapping |
| a | - | an accessor |
| ext | - | a `std::extents` object |
| exts | - | represents a multi-dimensional extents |
| other | - | another mdspan to convert from |
| rhs | - | another mdspan to copy or move from |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 24.7.3.6.2 Constructors [mdspan.mdspan.cons]

### See also

|  |  |
| --- | --- |
|  | This section is incomplete |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/mdspan/mdspan&oldid=172295>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 June 2024, at 11:12.