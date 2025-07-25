# Standard library header <mdspan> (C++23)

From cppreference.com
< cpp‎ | header
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

Standard library headers

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | ****<mdspan>**** (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the containers library.

|  |  |
| --- | --- |
| Classes | |
| mdspan(C++23) | a multi-dimensional non-owning array view   (class template) |
| extents(C++23) | a descriptor of a multidimensional index space of some rank   (class template) |
| layout_left(C++23) | column-major multidimensional array layout mapping policy; leftmost extent has stride `1`   (class) |
| layout_right(C++23) | row-major multidimensional array layout mapping policy; rightmost extent has stride `1`   (class) |
| layout_stride(C++23) | a layout mapping policy with user-defined strides   (class) |
| layout_left_padded(C++26) | column-major layout mapping policy with padding stride that can be greater than or equal to the leftmost extent   (class template) |
| layout_right_padded(C++26) | row-major layout mapping policy with padding stride that can be greater than or equal to the rightmost extent   (class template) |
| default_accessor(C++23) | a type for indexed access to elements of `mdspan`   (class template) |
| strided_slice(C++26) | a slice specifier representing a set of regularly spaced indices as indicated by an offset, an extent, and a stride   (class template) |
| submdspan_mapping_result(C++26) | a return type of the overloads of `submdspan_mapping`   (class template) |
| Alias templates | |
| dextentsdims(C++23)(C++26) | convenience alias template for an all-dynamic std::extents (alias template) |
| Functions | |
| submdspan_extents")(C++26) | creates new extents from the existing extents and slice specifiers   (function template) |
| submdspan")(C++26) | returns a view of a subset of an existing `mdspan`   (function template) |
| Tags | |
| full_extentfull_extent_t(C++26) | a slice specifier tag describing full range of indices in the specified extent. (tag) |

### Synopsis

```
// all freestanding
namespace std {
  // class template extents
  template<class IndexType, size_t... Extents>
  class extents;
 
  // alias template dextents
  template<class IndexType, size_t Rank>
  using dextents = /* see description */;
 
  // alias template dims
  template<size_t Rank, class IndexType = size_t>
  using dims = /* see description */;
 
  // layout mapping
  struct layout_left;
  struct layout_right;
  struct layout_stride;
  template<size_t PaddingValue = dynamic_extent>
  struct layout_left_padded;
  template<size_t PaddingValue = dynamic_extent>
  struct layout_right_padded;
 
  // class template default_accessor
  template<class ElementType>
  class default_accessor;
 
  // class template mdspan
  template<class ElementType,
           class Extents,
           class LayoutPolicy   = layout_right,
           class AccessorPolicy = default_accessor<ElementType>>
  class mdspan;
 
  // submdspan creation
  template<class OffsetType, class LengthType, class StrideType>
  struct strided_slice;
 
  template<class LayoutMapping>
  struct submdspan_mapping_result;
 
  struct full_extent_t
  {
    explicit full_extent_t() = default;
  };
  inline constexpr full_extent_t full_extent{};
 
  template<class IndexType, class... Extents, class... SliceSpecifiers>
  constexpr auto submdspan_extents(const extents<IndexType, Extents...>&,
                                   SliceSpecifiers...);
 
  // submdspan function template
  template<class ElementType,
           class Extents,
           class LayoutPolicy,
           class AccessorPolicy,
           class... SliceSpecifiers>
  constexpr auto submdspan(
    const mdspan<ElementType, Extents, LayoutPolicy, AccessorPolicy>& src,
    SliceSpecifiers... slices) -> /* see description */;
 
  template<class T, class IndexType>
  concept /*index-pair-like*/ = // exposition only
    /*pair-like*/<T> && convertible_to<tuple_element_t<0, T>, IndexType> &&
    convertible_to<tuple_element_t<1, T>, IndexType>;
}

```

#### Class template std::mdspan

```
namespace std {
  template<class ElementType,
           class Extents,
           class LayoutPolicy   = layout_right,
           class AccessorPolicy = default_accessor<ElementType>>
  class mdspan
  {
  public:
    using extents_type     = Extents;
    using layout_type      = LayoutPolicy;
    using accessor_type    = AccessorPolicy;
    using mapping_type     = typename layout_type::template mapping<extents_type>;
    using element_type     = ElementType;
    using value_type       = remove_cv_t<element_type>;
    using index_type       = typename extents_type::index_type;
    using size_type        = typename extents_type::size_type;
    using rank_type        = typename extents_type::rank_type;
    using data_handle_type = typename accessor_type::data_handle_type;
    using reference        = typename accessor_type::reference;
 
    static constexpr rank_type rank() noexcept { return extents_type::rank(); }
    static constexpr rank_type rank_dynamic() noexcept
    {
      return extents_type::rank_dynamic();
    }
    static constexpr size_t static_extent(rank_type r) noexcept
    {
      return extents_type::static_extent(r);
    }
    constexpr index_type extent(rank_type r) const noexcept
    {
      return extents().extent(r);
    }
 
    // constructors
    constexpr mdspan();
    constexpr mdspan(const mdspan& rhs) = default;
    constexpr mdspan(mdspan&& rhs)      = default;
 
    template<class... OtherIndexTypes>
    constexpr explicit mdspan(data_handle_type ptr, OtherIndexTypes... exts);
    template<class OtherIndexType, size_t N>
    constexpr explicit(N != rank_dynamic())
      mdspan(data_handle_type p, span<OtherIndexType, N> exts);
    template<class OtherIndexType, size_t N>
    constexpr explicit(N != rank_dynamic())
      mdspan(data_handle_type p, const array<OtherIndexType, N>& exts);
    constexpr mdspan(data_handle_type p, const extents_type& ext);
    constexpr mdspan(data_handle_type p, const mapping_type& m);
    constexpr mdspan(data_handle_type p, const mapping_type& m, const accessor_type& a);
 
    template<class OtherElementType,
             class OtherExtents,
             class OtherLayoutPolicy,
             class OtherAccessorPolicy>
    constexpr explicit(/* see description */)
      mdspan(const mdspan<OtherElementType,
                          OtherExtents,
                          OtherLayoutPolicy,
                          OtherAccessorPolicy>& other);
 
    constexpr mdspan& operator=(const mdspan& rhs) = default;
    constexpr mdspan& operator=(mdspan&& rhs)      = default;
 
    // members
    template<class... OtherIndexTypes>
    constexpr reference operator[](OtherIndexTypes... indices) const;
    template<class OtherIndexType>
    constexpr reference operator[](span<OtherIndexType, rank()> indices) const;
    template<class OtherIndexType>
    constexpr reference operator[](const array<OtherIndexType, rank()>& indices) const;
 
    constexpr size_type size() const noexcept;
    constexpr bool empty() const noexcept;
 
    friend constexpr void swap(mdspan& x, mdspan& y) noexcept;
 
    constexpr const extents_type& extents() const noexcept { return /*map_*/.extents(); }
    constexpr const data_handle_type& data_handle() const noexcept { return /*ptr_*/; }
    constexpr const mapping_type& mapping() const noexcept { return /*map_*/; }
    constexpr const accessor_type& accessor() const noexcept { return /*acc_*/; }
 
    static constexpr bool is_always_unique() { return mapping_type::is_always_unique(); }
    static constexpr bool is_always_exhaustive()
    {
      return mapping_type::is_always_exhaustive();
    }
    static constexpr bool is_always_strided()
    {
      return mapping_type::is_always_strided();
    }
 
    constexpr bool is_unique() const { return /*map_*/.is_unique(); }
    constexpr bool is_exhaustive() const { return /*map_*/.is_exhaustive(); }
    constexpr bool is_strided() const { return /*map_*/.is_strided(); }
    constexpr index_type stride(rank_type r) const { return /*map_*/.stride(r); }
 
  private:
    accessor_type /*acc_*/;    // exposition only
    mapping_type /*map_*/;     // exposition only
    data_handle_type /*ptr_*/; // exposition only
  };
 
  template<class CArray>
    requires(is_array_v<CArray> && rank_v<CArray> == 1)
  mdspan(CArray&)
    -> mdspan<remove_all_extents_t<CArray>, extents<size_t, extent_v<CArray, 0>>>;
 
  template<class Pointer>
    requires(is_pointer_v<remove_reference_t<Pointer>>)
  mdspan(Pointer&&)
    -> mdspan<remove_pointer_t<remove_reference_t<Pointer>>, extents<size_t>>;
 
  template<class ElementType, class... Integrals>
    requires((is_convertible_v<Integrals, size_t> && ...) && sizeof...(Integrals) > 0)
  explicit mdspan(ElementType*, Integrals...)
    -> mdspan<ElementType, extents<size_t, /*maybe-static-ext*/<Integrals>...>>;
 
  template<class ElementType, class OtherIndexType, size_t N>
  mdspan(ElementType*, span<OtherIndexType, N>)
    -> mdspan<ElementType, dextents<size_t, N>>;
 
  template<class ElementType, class OtherIndexType, size_t N>
  mdspan(ElementType*, const array<OtherIndexType, N>&)
    -> mdspan<ElementType, dextents<size_t, N>>;
 
  template<class ElementType, class IndexType, size_t... ExtentsPack>
  mdspan(ElementType*, const extents<IndexType, ExtentsPack...>&)
    -> mdspan<ElementType, extents<IndexType, ExtentsPack...>>;
 
  template<class ElementType, class MappingType>
  mdspan(ElementType*, const MappingType&) -> mdspan<ElementType,
                                                     typename MappingType::extents_type,
                                                     typename MappingType::layout_type>;
 
  template<class MappingType, class AccessorType>
  mdspan(const typename AccessorType::data_handle_type&,
         const MappingType&,
         const AccessorType&) -> mdspan<typename AccessorType::element_type,
                                        typename MappingType::extents_type,
                                        typename MappingType::layout_type,
                                        AccessorType>;
}

```

#### Class template std::extents

```
namespace std {
  template<class IndexType, size_t... Extents>
  class extents
  {
  public:
    using index_type = IndexType;
    using size_type  = make_unsigned_t<index_type>;
    using rank_type  = size_t;
 
    // observers of the multidimensional index space
    static constexpr rank_type rank() noexcept { return sizeof...(Extents); }
    static constexpr rank_type rank_dynamic() noexcept
    {
      return /*dynamic-index*/(rank());
    }
    static constexpr size_t static_extent(rank_type) noexcept;
    constexpr index_type extent(rank_type) const noexcept;
 
    // constructors
    constexpr extents() noexcept = default;
 
    template<class OtherIndexType, size_t... OtherExtents>
    constexpr explicit(/* see description */)
      extents(const extents<OtherIndexType, OtherExtents...>&) noexcept;
    template<class... OtherIndexTypes>
    constexpr explicit extents(OtherIndexTypes...) noexcept;
    template<class OtherIndexType, size_t N>
    constexpr explicit(N != rank_dynamic()) extents(span<OtherIndexType, N>) noexcept;
    template<class OtherIndexType, size_t N>
    constexpr explicit(N != rank_dynamic())
      extents(const array<OtherIndexType, N>&) noexcept;
 
    // comparison operators
    template<class OtherIndexType, size_t... OtherExtents>
    friend constexpr bool operator==(
      const extents&,
      const extents<OtherIndexType, OtherExtents...>&) noexcept;
 
    // exposition only helpers
    constexpr size_t /*fwd-prod-of-extents*/(rank_type) const noexcept; // exposition only
    constexpr size_t /*rev-prod-of-extents*/(rank_type) const noexcept; // exposition only
    template<class OtherIndexType>
    static constexpr auto /*index-cast*/(OtherIndexType&&) noexcept; // exposition only
 
  private:
    static constexpr rank_type /*dynamic-index*/(rank_type) noexcept; // exposition only
    static constexpr rank_type /*dynamic-index-inv*/(
      rank_type) noexcept;                                   // exposition only
    array<index_type, rank_dynamic()> /*dynamic-extents*/{}; // exposition only
  };
 
  template<class... Integrals>
  explicit extents(Integrals...)->/* see description */;
}

```

#### Layout mapping policies

```
namespace std {
  struct layout_left
  {
    template<class Extents>
    class mapping;
  };
  struct layout_right
  {
    template<class Extents>
    class mapping;
  };
  struct layout_stride
  {
    template<class Extents>
    class mapping;
  };
 
  template<size_t PaddingValue>
  struct layout_left_padded
  {
    template<class Extents>
    class mapping;
  };
  template<size_t PaddingValue>
  struct layout_right_padded
  {
    template<class Extents>
    class mapping;
  };
}

```

#### Class template std::layout_left::mapping

```
namespace std {
  template<class Extents>
  class layout_left::mapping
  {
  public:
    using extents_type = Extents;
    using index_type   = typename extents_type::index_type;
    using size_type    = typename extents_type::size_type;
    using rank_type    = typename extents_type::rank_type;
    using layout_type  = layout_left;
 
    // constructors
    constexpr mapping() noexcept               = default;
    constexpr mapping(const mapping&) noexcept = default;
    constexpr mapping(const extents_type&) noexcept;
    template<class OtherExtents>
    constexpr explicit(!is_convertible_v<OtherExtents, extents_type>)
      mapping(const mapping<OtherExtents>&) noexcept;
    template<class OtherExtents>
    constexpr explicit(!is_convertible_v<OtherExtents, extents_type>)
      mapping(const layout_right::mapping<OtherExtents>&) noexcept;
    template<class LayoutLeftPaddedMapping>
    constexpr explicit(
      !is_convertible_v<typename LayoutLeftPaddedMapping::extents_type, extents_type>)
      mapping(const LayoutLeftPaddedMapping&) noexcept;
    template<class OtherExtents>
    constexpr explicit(extents_type::rank() > 0)
      mapping(const layout_stride::mapping<OtherExtents>&);
 
    constexpr mapping& operator=(const mapping&) noexcept = default;
 
    // observers
    constexpr const extents_type& extents() const noexcept { return /*extents_*/; }
 
    constexpr index_type required_span_size() const noexcept;
 
    template<class... Indices>
    constexpr index_type operator()(Indices...) const noexcept;
 
    static constexpr bool is_always_unique() noexcept { return true; }
    static constexpr bool is_always_exhaustive() noexcept { return true; }
    static constexpr bool is_always_strided() noexcept { return true; }
 
    static constexpr bool is_unique() noexcept { return true; }
    static constexpr bool is_exhaustive() noexcept { return true; }
    static constexpr bool is_strided() noexcept { return true; }
 
    constexpr index_type stride(rank_type) const noexcept;
 
    template<class OtherExtents>
    friend constexpr bool operator==(const mapping&,
                                     const mapping<OtherExtents>&) noexcept;
 
  private:
    extents_type /*extents_*/{}; // exposition only
 
    // submdspan mapping specialization
    template<class... SliceSpecifiers>
    constexpr auto /*submdspan-mapping-impl*/(SliceSpecifiers...) const // exposition only
      -> /* see description */;
 
    template<class... SliceSpecifiers>
    friend constexpr auto submdspan_mapping(const mapping& src, SliceSpecifiers... slices)
    {
      return src./*submdspan-mapping-impl*/(slices...);
    }
  };
}

```

#### Class template std::layout_right::mapping

```
namespace std {
  template<class Extents>
  class layout_right::mapping
  {
  public:
    using extents_type = Extents;
    using index_type   = typename extents_type::index_type;
    using size_type    = typename extents_type::size_type;
    using rank_type    = typename extents_type::rank_type;
    using layout_type  = layout_right;
 
    // constructors
    constexpr mapping() noexcept               = default;
    constexpr mapping(const mapping&) noexcept = default;
    constexpr mapping(const extents_type&) noexcept;
    template<class OtherExtents>
    constexpr explicit(!is_convertible_v<OtherExtents, extents_type>)
      mapping(const mapping<OtherExtents>&) noexcept;
    template<class OtherExtents>
    constexpr explicit(!is_convertible_v<OtherExtents, extents_type>)
      mapping(const layout_left::mapping<OtherExtents>&) noexcept;
    template<class LayoutRightPaddedMapping>
    constexpr explicit(
      !is_convertible_v<typename LayoutRightPaddedMapping::extents_type, extents_type>)
      mapping(const LayoutRightPaddedMapping&) noexcept;
    template<class OtherExtents>
    constexpr explicit(extents_type::rank() > 0)
      mapping(const layout_stride::mapping<OtherExtents>&) noexcept;
 
    constexpr mapping& operator=(const mapping&) noexcept = default;
 
    // observers
    constexpr const extents_type& extents() const noexcept { return /*extents_*/; }
 
    constexpr index_type required_span_size() const noexcept;
 
    template<class... Indices>
    constexpr index_type operator()(Indices...) const noexcept;
 
    static constexpr bool is_always_unique() noexcept { return true; }
    static constexpr bool is_always_exhaustive() noexcept { return true; }
    static constexpr bool is_always_strided() noexcept { return true; }
 
    static constexpr bool is_unique() noexcept { return true; }
    static constexpr bool is_exhaustive() noexcept { return true; }
    static constexpr bool is_strided() noexcept { return true; }
 
    constexpr index_type stride(rank_type) const noexcept;
 
    template<class OtherExtents>
    friend constexpr bool operator==(const mapping&,
                                     const mapping<OtherExtents>&) noexcept;
 
  private:
    extents_type /*extents_*/{}; // exposition only
 
    // submdspan mapping specialization
    template<class... SliceSpecifiers>
    constexpr auto /*submdspan-mapping-impl*/(SliceSpecifiers...) const // exposition only
      -> /* see description */;
 
    template<class... SliceSpecifiers>
    friend constexpr auto submdspan_mapping(const mapping& src, SliceSpecifiers... slices)
    {
      return src./*submdspan-mapping-impl*/(slices...);
    }
  };
}

```

#### Class template std::layout_stride::mapping

```
namespace std {
  template<class Extents>
  class layout_stride::mapping
  {
  public:
    using extents_type = Extents;
    using index_type   = typename extents_type::index_type;
    using size_type    = typename extents_type::size_type;
    using rank_type    = typename extents_type::rank_type;
    using layout_type  = layout_stride;
 
  private:
    static constexpr rank_type /*rank_*/ = extents_type::rank(); // exposition only
 
  public:
    // constructors
    constexpr mapping() noexcept;
    constexpr mapping(const mapping&) noexcept = default;
    template<class OtherIndexType>
    constexpr mapping(const extents_type&, span<OtherIndexType, /*rank_*/>) noexcept;
    template<class OtherIndexType>
    constexpr mapping(const extents_type&,
                      const array<OtherIndexType, /*rank_*/>&) noexcept;
 
    template<class StridedLayoutMapping>
    constexpr explicit(/* see description */)
      mapping(const StridedLayoutMapping&) noexcept;
 
    constexpr mapping& operator=(const mapping&) noexcept = default;
 
    // observers
    constexpr const extents_type& extents() const noexcept { return /*extents_*/; }
    constexpr array<index_type, /*rank_*/> strides() const noexcept
    {
      return /*strides_*/;
    }
 
    constexpr index_type required_span_size() const noexcept;
 
    template<class... Indices>
    constexpr index_type operator()(Indices...) const noexcept;
 
    static constexpr bool is_always_unique() noexcept { return true; }
    static constexpr bool is_always_exhaustive() noexcept { return false; }
    static constexpr bool is_always_strided() noexcept { return true; }
 
    static constexpr bool is_unique() noexcept { return true; }
    constexpr bool is_exhaustive() const noexcept;
    static constexpr bool is_strided() noexcept { return true; }
 
    constexpr index_type stride(rank_type i) const noexcept { return /*strides_*/[i]; }
 
    template<class OtherMapping>
    friend constexpr bool operator==(const mapping&, const OtherMapping&) noexcept;
 
  private:
    extents_type /*extents_*/{};                 // exposition only
    array<index_type, /*rank_*/> /*strides_*/{}; // exposition only
 
    // submdspan mapping specialization
    template<class... SliceSpecifiers>
    constexpr auto /*submdspan-mapping-impl*/(SliceSpecifiers...) const // exposition only
      -> /* see description */;
 
    template<class... SliceSpecifiers>
    friend constexpr auto submdspan_mapping(const mapping& src, SliceSpecifiers... slices)
    {
      return src./*submdspan-mapping-impl*/(slices...);
    }
  };
}

```

#### Class template std::layout_left_padded::mapping

```
namespace std {
  template<size_t PaddingValue>
  template<class Extents>
  class layout_left_padded<PaddingValue>::mapping
  {
  public:
    static constexpr size_t padding_value = PaddingValue;
 
    using extents_type                    = Extents;
    using index_type                      = typename extents_type::index_type;
    using size_type                       = typename extents_type::size_type;
    using rank_type                       = typename extents_type::rank_type;
    using layout_type                     = layout_left_padded<PaddingValue>;
 
  private:
    static constexpr size_t /*rank_*/ = extents_type::rank(); // exposition only
    static constexpr size_t /*first-static-extent*/ =         // exposition only
      extents_type::static_extent(0);
 
    // exposition only members
    static constexpr size_t /*static-padding-stride*/ =
      /* see description */; // exposition only
 
  public:
    // constructors
    constexpr mapping() noexcept
      : mapping(extents_type{})
    {
    }
    constexpr mapping(const mapping&) noexcept = default;
    constexpr mapping(const extents_type&);
    template<class OtherIndexType>
    constexpr mapping(const extents_type&, OtherIndexType);
    template<class OtherExtents>
    constexpr explicit(!is_convertible_v<OtherExtents, extents_type>)
      mapping(const layout_left::mapping<OtherExtents>&);
    template<class OtherExtents>
    constexpr explicit(extents_type::rank() > 0)
      mapping(const layout_stride::mapping<OtherExtents>&);
    template<class LayoutLeftPaddedMapping>
    constexpr explicit(/* see description */) mapping(const LayoutLeftPaddedMapping&);
    template<class LayoutRightPaddedMapping>
    constexpr explicit(/* see description */)
      mapping(const LayoutRightPaddedMapping&) noexcept;
 
    constexpr mapping& operator=(const mapping&) noexcept = default;
 
    // observers
    constexpr const extents_type& extents() const noexcept { return /*extents_*/; }
    constexpr array<index_type, rank_> strides() const noexcept;
 
    constexpr index_type required_span_size() const noexcept;
    template<class... Indices>
    constexpr index_type operator()(Indices...) const noexcept;
 
    static constexpr bool is_always_unique() noexcept { return true; }
    static constexpr bool is_always_exhaustive() noexcept;
    static constexpr bool is_always_strided() noexcept { return true; }
 
    static constexpr bool is_unique() noexcept { return true; }
    constexpr bool is_exhaustive() const noexcept;
    static constexpr bool is_strided() noexcept { return true; }
 
    constexpr index_type stride(rank_type) const noexcept;
 
    template<class LayoutLeftPaddedMapping>
    friend constexpr bool operator==(const mapping&,
                                     const LayoutLeftPaddedMapping&) noexcept;
 
  private:
    // exposition only members
    index_type /*stride-1*/ = /*static-padding-stride*/; // exposition only
    extents_type /*extents_*/{};                         // exposition only
    // submdspan mapping specialization
    template<class... SliceSpecifiers>
    constexpr auto /*submdspan-mapping-impl*/(SliceSpecifiers...) const // exposition only
      -> /* see description */;
 
    template<class... SliceSpecifiers>
    friend constexpr auto submdspan_mapping(const mapping& src, SliceSpecifiers... slices)
    {
      return src./*submdspan-mapping-impl*/(slices...);
    }
  };
}

```

#### Class template std::layout_right_padded::mapping

```
namespace std {
  template<size_t PaddingValue>
  template<class Extents>
  class layout_right_padded<PaddingValue>::mapping
  {
  public:
    static constexpr size_t padding_value = PaddingValue;
 
    using extents_type                    = Extents;
    using index_type                      = typename extents_type::index_type;
    using size_type                       = typename extents_type::size_type;
    using rank_type                       = typename extents_type::rank_type;
    using layout_type                     = layout_right_padded<PaddingValue>;
 
  private:
    static constexpr size_t /*rank_*/ = extents_type::rank(); // exposition only
    static constexpr size_t /*last-static-extent*/ =          // exposition only
      extents_type::static_extent(/*rank_*/ - 1);
 
    // exposition only members
    static constexpr size_t /*static-padding-stride*/ =
      /* see description */; // exposition only
 
  public:
    // constructors
    constexpr mapping() noexcept
      : mapping(extents_type{})
    {
    }
    constexpr mapping(const mapping&) noexcept = default;
    constexpr mapping(const extents_type&);
    template<class OtherIndexType>
    constexpr mapping(const extents_type&, OtherIndexType);
 
    template<class OtherExtents>
    constexpr explicit(!is_convertible_v<OtherExtents, extents_type>)
      mapping(const layout_right::mapping<OtherExtents>&);
    template<class OtherExtents>
    constexpr explicit(rank_ > 0) mapping(const layout_stride::mapping<OtherExtents>&);
    template<class LayoutRightPaddedMapping>
    constexpr explicit(/* see description */) mapping(const LayoutRightPaddedMapping&);
    template<class LayoutLeftPaddedMapping>
    constexpr explicit(/* see description */)
      mapping(const LayoutLeftPaddedMapping&) noexcept;
 
    constexpr mapping& operator=(const mapping&) noexcept = default;
 
    // observers
    constexpr const extents_type& extents() const noexcept { return extents_; }
    constexpr array<index_type, rank_> strides() const noexcept;
 
    constexpr index_type required_span_size() const noexcept;
 
    template<class... Indices>
    constexpr index_type operator()(Indices...) const noexcept;
 
    static constexpr bool is_always_unique() noexcept { return true; }
    static constexpr bool is_always_exhaustive() noexcept;
    static constexpr bool is_always_strided() noexcept { return true; }
 
    static constexpr bool is_unique() noexcept { return true; }
    constexpr bool is_exhaustive() const noexcept;
    static constexpr bool is_strided() noexcept { return true; }
 
    constexpr index_type stride(rank_type) const noexcept;
 
    template<class LayoutRightPaddedMapping>
    friend constexpr bool operator==(const mapping&,
                                     const LayoutRightPaddedMapping&) noexcept;
 
  private:
    // exposition only members
    index_type /*stride-rm2*/ = /*static-padding-stride*/; // exposition only
    extents_type /*extents_*/{};                           // exposition only
 
    // submdspan mapping specialization
    template<class... SliceSpecifiers>
    constexpr auto /*submdspan-mapping-impl*/(SliceSpecifiers...) const // exposition only
      -> /* see description */;
 
    template<class... SliceSpecifiers>
    friend constexpr auto submdspan_mapping(const mapping& src, SliceSpecifiers... slices)
    {
      return src./*submdspan-mapping-impl*/(slices...);
    }
  };
}

```

#### Exposition-only helpers

```
template<class T>
constexpr bool /*is-extents*/ = false; // exposition only
template<class IndexType, size_t... Args>
constexpr bool /*is-extents*/<extents<IndexType, Args...>> = true; // exposition only;
 
template<class M>
concept /*layout-mapping-alike*/ = requires { // exposition only
  requires /*is-extents*/<typename M::extents_type>;
  {
    M::is_always_strided()
  } -> same_as<bool>;
  {
    M::is_always_exhaustive()
  } -> same_as<bool>;
  {
    M::is_always_unique()
  } -> same_as<bool>;
  bool_constant<M::is_always_strided()>::value;
  bool_constant<M::is_always_exhaustive()>::value;
  bool_constant<M::is_always_unique()>::value;
};
 
template<class T>
constexpr T
/*de-ice*/(T val)
{
  return val;
}
template</*integral-constant-like*/ T>
constexpr auto
/*de-ice*/(T)
{
  return T::value;
}
 
template<class IndexType, size_t k, class... SliceSpecifiers>
constexpr IndexType
/*first_*/(SliceSpecifiers... slices);
 
template<size_t k, class Extents, class... SliceSpecifiers>
constexpr auto
/*last_*/(const Extents& src, SliceSpecifiers... slices);
 
template<class IndexType, size_t N, class... SliceSpecifiers>
constexpr array<IndexType, sizeof...(SliceSpecifiers)>
/*src-indices*/(const array<IndexType, N>& indices, SliceSpecifiers... slices);

```

#### Class template std::default_accessor

```
namespace std {
  template<class ElementType>
  struct default_accessor
  {
    using offset_policy                   = default_accessor;
    using element_type                    = ElementType;
    using reference                       = ElementType&;
    using data_handle_type                = ElementType*;
 
    constexpr default_accessor() noexcept = default;
    template<class OtherElementType>
    constexpr default_accessor(default_accessor<OtherElementType>) noexcept;
    constexpr reference access(data_handle_type p, size_t i) const noexcept;
    constexpr data_handle_type offset(data_handle_type p, size_t i) const noexcept;
  };
}

```

#### Class template std::strided_slice

```
namespace std {
  template<class OffsetType, class ExtentType, class StrideType>
  struct strided_slice
  {
    using offset_type = OffsetType;
    using extent_type = ExtentType;
    using stride_type = StrideType;
 
    [[no_unique_address]] offset_type offset{};
    [[no_unique_address]] extent_type extent{};
    [[no_unique_address]] stride_type stride{};
  };
}

```

#### Class template std::submdspan_mapping_result

```
namespace std {
  template<class LayoutMapping>
  struct submdspan_mapping_result
  {
    [[no_unique_address]] LayoutMapping mapping = LayoutMapping();
    size_t offset{};
  };
}

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 24.7.4 Header `<mdspan>` synopsis [mdspan.syn]

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/mdspan&oldid=173198>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 July 2024, at 07:00.