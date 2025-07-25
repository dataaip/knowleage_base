# std::ranges::views::reverse, std::ranges::reverse_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****reverse_viewviews::reverse**** | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< ranges::view V >      requires ranges::bidirectional_range<V>  class reverse_view : public ranges::view_interface<reverse_view<V>> | (1) | (since C++20) |
| namespace views {  inline constexpr /\* unspecified \*/ reverse = /\* unspecified \*/; } | (2) | (since C++20) |
| Call signature |  |  |
| template< ranges::viewable_range R >      requires /\* see below \*/ constexpr ranges::view auto reverse( R&& r ); |  | (since C++20) |
|  |  |  |

1) A range adaptor that represents a view of underlying `view` with reversed order.2) RangeAdaptorObject. The expression views::reverse(e) is expression-equivalent to one of the following expressions, except that e is evaluated only once:

- e.base(), if the type of `e` is a (possibly cv-qualified) specialization of `reverse_view`;
- otherwise, if the type of e is (possibly cv-qualified) ranges::subrange<std::reverse_iterator<I>, std::reverse_iterator<I>, K> for some iterator type `I` and value `K` of type `ranges::subrange_kind`:

:   - ranges::subrange<I, I, K>(e.end().base(), e.begin().base(), e.size()), if `K` is `ranges::subrange_kind::sized`;
    - otherwise ranges::subrange<I, I, K>(e.end().base(), e.begin().base());

- otherwise ranges::reverse_view{e}.

In other words, `views::reverse` unwraps reversed views if possible.

A `reverse_view` always models `bidirectional_range` and `common_range`, and it models `borrowed_range`, `sized_range`, or `random_access_range` if the underlying view type `V` models the corresponding concept.

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| `base_` (private) | The underlying view of type `V`. (exposition-only member object\*) |
| `cached_end_` (private) | An optional-like cache object that holds either no value or the end iterator/position of the underlying view, which exists only if the underlying view type `V` does not model `common_range`. (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `reverse_view`   (public member function) |
| base | returns the underlying view `V`   (public member function) |
| begin | returns the beginning iterator of the `reverse_view`   (public member function) |
| end | returns the end iterator of the `reverse_view`   (public member function) |
| size | returns the size of the view if it is bounded   (public member function) |
| Inherited from std::ranges::view_interface | |
| empty | returns whether the derived view is empty. Provided if it satisfies `sized_range` or `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |
| operator bool | returns whether the derived view is not empty. Provided if ranges::empty is applicable to it.   (public member function of `std::ranges::view_interface<D>`) |
| front | returns the first element in the derived view. Provided if it satisfies `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| back | returns the last element in the derived view. Provided if it satisfies `bidirectional_range` and `common_range`.   (public member function of `std::ranges::view_interface<D>`) |
| [operator[]](view_interface/operator_at.html "cpp/ranges/view interface/operator at") | returns the `n`th element in the derived view. Provided if it satisfies `random_access_range`.   (public member function of `std::ranges::view_interface<D>`) |

## std::ranges::reverse_view::reverse_view

|  |  |  |
| --- | --- | --- |
| reverse_view() requires std::default_initializable<V> = default; | (1) | (since C++20) |
| constexpr reverse_view( V r ); | (2) | (since C++20) |
|  |  |  |

1) Value-initializes `base_` via its default member initializer (= V()).2) Initializes `base_` with std::move(r).

### Parameters

|  |  |  |
| --- | --- | --- |
| r | - | range to reverse |

## std::ranges::reverse_view::base

|  |  |  |
| --- | --- | --- |
| constexpr V base() const& requires std::copy_constructible<V>; | (1) | (since C++20) |
| constexpr V base() &&; | (2) | (since C++20) |
|  |  |  |

Returns the underlying view.

1) Copy-constructs the result from the underlying view. Equivalent to return base_;.2) Move-constructs the result from the underlying view. Equivalent to return std::move(base_);.

## std::ranges::reverse_view::begin

|  |  |  |
| --- | --- | --- |
| constexpr std::reverse_iterator<ranges::iterator_t<V>> begin(); | (1) | (since C++20) |
| constexpr std::reverse_iterator<ranges::iterator_t<V>> begin()      requires ranges::common_range<V>; | (2) | (since C++20) |
| constexpr auto begin() const requires ranges::common_range<const V>; | (3) | (since C++20) |
|  |  |  |

1) Returns std::make_reverse_iterator(ranges::next(ranges::begin(base_), ranges::end(base_))). In order to provide the amortized constant time complexity required by the `range` concept, this function caches the result within the cache object for use on subsequent calls.2,3) Equivalent to return std::make_reverse_iterator(ranges::end(base_));.

## std::ranges::reverse_view::end

|  |  |  |
| --- | --- | --- |
| constexpr std::reverse_iterator<ranges::iterator_t<V>> end(); | (1) | (since C++20) |
| constexpr auto end() const requires ranges::common_range<const V>; | (2) | (since C++20) |
|  |  |  |

Equivalent to return std::make_reverse_iterator(ranges::begin(base_));.

## std::ranges::reverse_view::size

|  |  |  |
| --- | --- | --- |
| constexpr auto size() requires ranges::sized_range<V>; | (1) | (since C++20) |
| constexpr auto size() const requires ranges::sized_range<const V>; | (2) | (since C++20) |
|  |  |  |

Returns the size of the view if the view is bounded.

1,2) Equivalent to return ranges::size(base_);.

### Deduction guides

|  |  |  |
| --- | --- | --- |
| template< class R >  reverse_view( R&& ) -> reverse_view<views::all_t<R>>; |  | (since C++20) |
|  |  |  |

### Helper templates

|  |  |  |
| --- | --- | --- |
| template< class T >  constexpr bool enable_borrowed_range<std::ranges::reverse_view<T>> = ranges::enable_borrowed_range<T>; |  | (since C++20) |
|  |  |  |

This specialization of std::ranges::enable_borrowed_range makes `reverse_view` satisfy `borrowed_range` when the underlying view satisfies it.

### Example

Run this code

```
#include <iostream>
#include <ranges>
 
int main()
{
    static constexpr auto il = {3, 1, 4, 1, 5, 9};
 
    std::ranges::reverse_view rv{il};
    for (int i : rv)
        std::cout << i << ' ';
    std::cout << '\n';
 
    for (int i : il | std::views::reverse)
        std::cout << i << ' ';
    std::cout << '\n';
 
    // operator[] is inherited from std::view_interface
    for (auto i{0U}; i != rv.size(); ++i)
        std::cout << rv[i] << ' ';
    std::cout << '\n';
}

```

Output:

```
9 5 1 4 1 3
9 5 1 4 1 3
9 5 1 4 1 3

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3494 | C++20 | `reverse_view` was never a `borrowed_range` | it is a `borrowed_range` if its underlying view is |

### See also

|  |  |
| --- | --- |
| reverse_iterator | iterator adaptor for reverse-order traversal   (class template) |
| ranges::reverse(C++20) | reverses the order of elements in a range (algorithm function object) |
| ranges::reverse_copy(C++20) | creates a copy of a range that is reversed (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/reverse_view&oldid=172685>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 June 2024, at 21:50.