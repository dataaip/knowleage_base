# std::ranges::views::stride, std::ranges::stride_view

From cppreference.com
< cpp‎ | ranges
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

Ranges library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begin | | | | | | cbegin | | | | | | end | | | | | | cend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rbegin | | | | | | crbegin | | | | | | rend | | | | | | crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | size | | | | | | ssize | | | | | | data | | | | | | cdata | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty | | | | | |  | | | | | |  | | | | | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range conversions | | | | | | std::from_range_t std::from_range(C++23)(C++23) | | | | | | to(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Dangling iterator handling | | | | | | dangling | | | | | | borrowed_iterator_t | | | | | | borrowed_subrange_t | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range primitives | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | range_size_trange_difference_trange_value_t | | | | | | elements_of(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator_tconst_iterator_tsentinel_tconst_sentinel_t(C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | range_reference_trange_const_reference_trange_rvalue_reference_trange_common_reference_t(C++23) | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | range | | | | | | borrowed_range | | | | | | sized_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_range | | | | | | view | | | | | | viewable_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_range | | | | | | output_range | | | | | | forward_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bidirectional_range | | | | | | random_access_range | | | | | | contiguous_range | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | constant_range(C++23) | | | | | |  | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Views | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | view_interface | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | subrange | | | | | |  | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range factories | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty_viewviews::empty | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | single_viewviews::single | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | basic_istream_viewviews::istream | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota_viewviews::iota | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | repeat_viewviews::repeat(C++23)(C++23) | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | ****stride_viewviews::stride****(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

****std::ranges::stride_view****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| stride_view::stride_view | | | | |
| stride_view::base | | | | |
| stride_view::stride | | | | |
| stride_view::begin | | | | |
| stride_view::end | | | | |
| stride_view::size | | | | |
| Deduction guides | | | | |
| Iterator | | | | |
| Member functions | | | | |
| stride_view::**iterator**::**iterator** | | | | |
| stride_view::**iterator**::base | | | | |
| stride_view::**iterator**::operator\* | | | | |
| [stride_view::**iterator**::operator[]](stride_view/iterator/operator_at.html "cpp/ranges/stride view/iterator/operator at") | | | | |
| stride_view::**iterator**::operator++ stride_view::**iterator**::operator++(int) stride_view::**iterator**::operator-- stride_view::**iterator**::operator--(int) stride_view::**iterator**::operator+= stride_view::**iterator**::operator-= | | | | |
| Non-member functions | | | | |
| operator==(std::default_sentinel_t) operator==(stride_view::**iterator**) operator<(stride_view::**iterator**) operator>(stride_view::**iterator**) operator<=(stride_view::**iterator**) operator>=(stride_view::**iterator**) operator<=>(stride_view::**iterator**) | | | | |
| operator+(stride_view::**iterator**) operator-(stride_view::**iterator**) | | | | |
| iter_move(stride_view::**iterator**) | | | | |
| iter_swap(stride_view::**iterator**) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< ranges::input_range V >      requires ranges::view<V>  class stride_view : public ranges::view_interface<stride_view<V>> | (1) | (since C++23) |
| namespace views {  inline constexpr /\* unspecified \*/ stride = /\* unspecified \*/; } | (2) | (since C++23) |
| Call signature |  |  |
| template< ranges::viewable_range R >  constexpr ranges::view auto stride( R&& r, ranges::range_difference_t<R> n ); |  | (since C++23) |
| template< class DifferenceType >  constexpr /\*range adaptor closure\*/ stride( DifferenceType&& n ); |  | (since C++23) |
| Helper templates |  |  |
|  |  |  |

1) `stride_view` is a range adaptor that takes a `view` and a number `n` and produces a view, that consists of elements of the original view by advancing over **n** elements at a time. This means that each `m`**th** element of the produced view is `(n * i)`th element of the original view, for some non-negative index `i`.
The elements of the original view, whose "index" is not a multiple of `n`, are not present in the produced view. Let `S` be the size of the original view. Then the size of produced view is:

- (S / n) + (S % n ? 1 : 0), if S >= n; otherwise,
- 1, if S > 0; otherwise,
- ​0​, and the resulting view is empty.
2) The name views::stride denotes a RangeAdaptorObject. Given subexpressions e and n, the expression views::stride(e, n) is expression-equivalent to stride_view(e, n). The `n` must be greater than ​0​, otherwise the behavior is undefined.

`stride_view` always models `input_range`, and models `forward_range`, `bidirectional_range`, `random_access_range`, and/or `sized_range`, if adapted `view` type V models the corresponding concept.
stride_view<V> models `common_range` whenever the underlying view V does.

### Data members

|  |  |
| --- | --- |
| Member object | Definition |
| `base_` (private) | The underlying `view` of type `V`. (exposition-only member object\*) |
| `stride_` (private) | The size object (the "stride") of type ranges::range_difference_t<V>. (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `stride_view`   (public member function) |
| stride(C++23) | returns the stored stride value   (public member function) |
| base | returns a copy of the underlying (adapted) view   (public member function) |
| begin | returns an iterator to the beginning   (public member function) |
| end | returns an iterator or a sentinel to the end   (public member function) |
| size | returns the number of elements. Provided only if the underlying (adapted) range satisfies `sized_range`.   (public member function) |
| Inherited from std::ranges::view_interface | |
| empty | returns whether the derived view is empty. Provided if it satisfies `sized_range` or `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |
| operator bool | returns whether the derived view is not empty. Provided if ranges::empty is applicable to it.   (public member function of `std::ranges::view_interface<D>`) |
| front | returns the first element in the derived view. Provided if it satisfies `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| back | returns the last element in the derived view. Provided if it satisfies `bidirectional_range` and `common_range`.   (public member function of `std::ranges::view_interface<D>`) |
| [operator[]](view_interface/operator_at.html "cpp/ranges/view interface/operator at") | returns the `n`th element in the derived view. Provided if it satisfies `random_access_range`.   (public member function of `std::ranges::view_interface<D>`) |

### Deduction guides

### Nested classes

|  |  |
| --- | --- |
| **iterator**(C++23) | the iterator type (exposition-only member class template\*) |

### Helper templates

|  |  |  |
| --- | --- | --- |
| template< class V >  constexpr bool ranges::enable_borrowed_range<stride_view<V>> = ranges::enable_borrowed_range<V>; |  | (since C++23) |
|  |  |  |

This specialization of ranges::enable_borrowed_range makes `stride_view` satisfy `borrowed_range` when the underlying view satisfies it.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_ranges_stride` | `202207L` | (C++23) | `std::ranges::stride_view` |

### Example

Run this code

```
#include <algorithm>
#include <iostream>
#include <ranges>
#include <string_view>
using namespace std::literals;
 
void print(std::ranges::viewable_range auto&& v, std::string_view separator = " ")
{
    for (auto const& x : v)
        std::cout << x << separator;
    std::cout << '\n';
}
 
int main()
{
    print(std::views::iota(1, 13) | std::views::stride(3));
    print(std::views::iota(1, 13) | std::views::stride(3) | std::views::reverse);
    print(std::views::iota(1, 13) | std::views::reverse | std::views::stride(3));
 
    print("0x0!133713337*x//42/A$@"sv | std::views::stride(0B11) |
          std::views::transform([](char O) -> char { return 0100 | O; }),
          "");
}

```

Output:

```
1 4 7 10
10 7 4 1
12 9 6 3
password

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 26.7.31 Stride view [range.stride]

### See also

|  |  |
| --- | --- |
| ranges::slide_viewviews::slide(C++23) | a `view` whose Mth element is a `view` over the Mth through (M + N - 1)th elements of another `view` (class template) (range adaptor object) |
| ranges::chunk_viewviews::chunk(C++23) | a range of `view`s that are `N`-sized non-overlapping successive chunks of the elements of another `view` (class template) (range adaptor object) |
| ranges::adjacent_viewviews::adjacent(C++23) | a `view` consisting of tuples of references to adjacent elements of the adapted view (class template) (range adaptor object) |
| ranges::filter_viewviews::filter(C++20) | a `view` that consists of the elements of a `range` that satisfies a predicate (class template) (range adaptor object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/stride_view&oldid=172436>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 June 2024, at 18:57.