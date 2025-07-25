# std::ranges::views::filter, std::ranges::filter_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | ****filter_viewviews::filter**** | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

****std::ranges::filter_view****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| filter_view::filter_view | | | | |
| filter_view::base | | | | |
| filter_view::pred | | | | |
| filter_view::begin | | | | |
| filter_view::end | | | | |
| Deduction guides | | | | |
| Iterator | | | | |
| filter_view::**iterator**::**iterator** | | | | |
| filter_view::**iterator**::base | | | | |
| filter_view::**iterator**::operator\*filter_view::**iterator**::operator-> | | | | |
| filter_view::**iterator**::operator++ filter_view::**iterator**::operator++(int) | | | | |
| filter_view::**iterator**::operator-- filter_view::**iterator**::operator--(int) | | | | |
| operator==(filter_view::**iterator**) | | | | |
| iter_move(filter_view::**iterator**) | | | | |
| iter_swap(filter_view::**iterator**) | | | | |
| Sentinel | | | | |
| filter_view::**sentinel**::**sentinel** | | | | |
| filter_view::**sentinel**::base | | | | |
| operator==(filter_view::**iterator**, filter_view::**sentinel**) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< ranges::input_range V,  std::indirect_unary_predicate<ranges::iterator_t<V>> Pred >      requires ranges::view<V> && std::is_object_v<Pred>  class filter_view : public ranges::view_interface<filter_view<V, Pred>> | (1) | (since C++20) |
| namespace views {  inline constexpr /\* unspecified \*/ filter = /\* unspecified \*/; } | (2) | (since C++20) |
| Call signature |  |  |
| template< ranges::viewable_range R, class Pred >      requires /\* see below \*/ constexpr ranges::view auto filter( R&& r, Pred&& pred ); |  | (since C++20) |
| template< class Pred >  constexpr /\* range adaptor closure \*/ filter( Pred&& pred ); |  | (since C++20) |
|  |  |  |

1) A range adaptor that represents `view` of an underlying sequence without the elements that fail to satisfy a predicate.2) RangeAdaptorObject. The expression views::filter(e, p) is expression-equivalent to filter_view(e, p) for any suitable subexpressions e and p.

`filter_view` models the concepts `bidirectional_range`, `forward_range`, `input_range`, and `common_range` when the underlying `view` `V` models respective concepts.

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| `base_` (private) | The underlying `view` of type `V`. (exposition-only member object\*) |
| `pred_` (private) | Wraps the predicate used to filter out elements of `base_` of type `copyable-box``<Pred>`(until C++23)`movable-box``<Pred>`(since C++23) augmenting `Pred` with assignability when needed and hence always satisfies `copyable`or `movable`(since C++23). (exposition-only member object\*) |
| `begin_` (private)  (conditionally present) | An object of optional-like type that caches an iterator to the first element of `base_` that satisfies the `pred_`. Present only if `filter_view` models `forward_range`. (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `filter_view`   (public member function) |
| base | returns the underlying view `V`   (public member function) |
| pred | returns a reference to the predicate stored within `filter_view`   (public member function) |
| begin | returns the beginning iterator of the `filter_view`   (public member function) |
| end | returns the sentinel of the `filter_view`   (public member function) |
| Inherited from std::ranges::view_interface | |
| empty | returns whether the derived view is empty. Provided if it satisfies `sized_range` or `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |
| operator bool | returns whether the derived view is not empty. Provided if ranges::empty is applicable to it.   (public member function of `std::ranges::view_interface<D>`) |
| front | returns the first element in the derived view. Provided if it satisfies `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| back | returns the last element in the derived view. Provided if it satisfies `bidirectional_range` and `common_range`.   (public member function of `std::ranges::view_interface<D>`) |

## std::ranges::filter_view::filter_view

|  |  |  |
| --- | --- | --- |
| filter_view() requires std::default_initializable<V> &&                         std::default_initializable<Pred> = default; | (1) | (since C++20) |
| constexpr explicit filter_view( V base, Pred pred ); | (2) | (since C++20) |
|  |  |  |

1) Value-initializes `base_` via its default member initializer (= V()) and default-initializes `pred_` (which value-initializes the contained `Pred`).2) Initializes `base_` with std::move(base) and initializes `pred_` with std::move(pred).

### Parameters

|  |  |  |
| --- | --- | --- |
| base | - | range to filter |
| pred | - | predicate to filter out elements |

## std::ranges::filter_view::base

|  |  |  |
| --- | --- | --- |
| constexpr V base() const& requires std::copy_constructible<V>; | (1) | (since C++20) |
| constexpr V base() &&; | (2) | (since C++20) |
|  |  |  |

1) Equivalent to return base_;.2) Equivalent to return std::move(base_);.

## std::ranges::filter_view::pred

|  |  |  |
| --- | --- | --- |
| constexpr const Pred& pred() const; |  | (since C++20) |
|  |  |  |

Returns a reference to the contained `Pred` object. The behavior is undefined if `pred_` does not contain a value.

## std::ranges::filter_view::begin

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/ begin(); |  | (exposition only\*) |
|  |  |  |

In order to provide the amortized constant time complexity required by the `range` concept, this function caches the result within the `filter_view` object for use on subsequent calls. Equivalent to

```
if constexpr (!ranges::forward_range<V>)
    return /*iterator*/{*this, ranges::find_if(base_, std::ref(*pred_))};
else
{
    if (!begin_.has_value())
        begin_ = ranges::find_if(base_, std::ref(*pred_)); // caching
    return /*iterator*/{*this, begin_.value())};
}

```

The behavior is undefined if `pred_` does not contain a value.

## std::ranges::filter_view::end

|  |  |  |
| --- | --- | --- |
| constexpr auto end(); |  | (since C++20) |
|  |  |  |

Returns an iterator to the end. Equivalent to

```
if constexpr (ranges::common_range<V>)
    return /*iterator*/{*this, ranges::end(base_)};
else
    return /*sentinel*/{*this};

```

### Deduction guides

|  |  |  |
| --- | --- | --- |
| template< class R, class Pred >  filter_view( R&&, Pred ) -> filter_view<views::all_t<R>, Pred>; |  | (since C++20) |
|  |  |  |

### Nested classes

|  |  |
| --- | --- |
| **iterator** | the iterator type of `filter_view` (exposition-only member class\*) |
| **sentinel** | the sentinel type of `filter_view` when the underlying view is not a `common_range` (exposition-only member class\*) |

### Example

Run this code

```
#include <iostream>
#include <ranges>
 
int main()
{
    auto even = [](int i) { return 0 == i % 2; };
    auto square = [](int i) { return i * i; };
 
    for (int i : std::views::iota(0, 6)
               | std::views::filter(even)
               | std::views::transform(square))
        std::cout << i << ' ';
    std::cout << '\n';
}

```

Output:

```
0 4 16

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3714 (P2711R1) | C++20 | the multi-parameter constructor was not explicit | made explicit |
| P2325R3 | C++20 | if `Pred` is not `default_initializable`, the default constructor constructs a `filter_view` which does not contain a `Pred` | the `filter_view` is also not `default_initializable` |

### See also

|  |  |
| --- | --- |
| ranges::take_while_viewviews::take_while(C++20) | a `view` consisting of the initial elements of another `view`, until the first element on which a predicate returns false (class template) (range adaptor object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/filter_view&oldid=173744>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 July 2024, at 05:34.