# std::ranges::views::chunk_by, std::ranges::chunk_by_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | ****chunk_by_viewviews::chunk_by****(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

****std::ranges::chunk_by_view****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| chunk_by_view::chunk_by_view | | | | |
| chunk_by_view::base | | | | |
| chunk_by_view::pred | | | | |
| chunk_by_view::begin | | | | |
| chunk_by_view::end | | | | |
| chunk_by_view::**find_next** | | | | |
| chunk_by_view::**find_prev** | | | | |
| Deduction guides | | | | |
| Iterator | | | | |
| chunk_by_view::**iterator**::**iterator** | | | | |
| chunk_by_view::**iterator**::operator\* | | | | |
| chunk_by_view::**iterator**::operator++ chunk_by_view::**iterator**::operator++(int) chunk_by_view::**iterator**::operator-- chunk_by_view::**iterator**::operator--(int) | | | | |
| operator==(chunk_by_view::**iterator**) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< ranges::forward_range V, std::indirect_binary_predicate<iterator_t<V>,  ranges::iterator_t<V>> Pred >      requires ranges::view<V> && std::is_object_v<Pred>  class chunk_by_view : public ranges::view_interface<chunk_by_view<V, Pred>> | (1) | (since C++23) |
| namespace views {  inline constexpr /\* unspecified \*/ chunk_by = /\* unspecified \*/ ; } | (2) | (since C++23) |
| Call signature |  |  |
| template< ranges::viewable_range R, class Pred >      requires /\* see below \*/ constexpr ranges::view auto chunk_by( R&& r, Pred&& pred ); |  | (since C++23) |
| template< class Pred >  constexpr /\*range adaptor closure\*/ chunk_by( Pred&& pred ); |  | (since C++23) |
|  |  |  |

1) `chunk_by_view` is a range adaptor that takes a `view` and an invocable object pred (the binary predicate), and produces a `view` of subranges (chunks), by splitting the underlying view between each pair of adjacent elements for which pred returns false. The first element of each such pair belongs to the previous chunk, and the second element belongs to the next chunk.2) The name views::chunk_by denotes a RangeAdaptorObject. Given a subexpression e and f, the expression views::chunk_by(e, f) is expression-equivalent to chunk_by_view(e, f).

`chunk_by_view` always models `forward_range`, and models `bidirectional_range` and/or `common_range`, if adapted `view` type models the corresponding concepts.
`chunk_by_view` never models `borrowed_range` or `sized_range`.

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| `V` `base_` | the underlying `view` (exposition-only member object\*) |
| **movable-box**`<Pred>` `pred_` | an object that wraps the predicate used to split the elements of `base_` (exposition-only member object\*) |
| `non-propagating-cache``<iterator>` `begin_` | an object that caches the iterator to the first element (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `chunk_by_view`   (public member function) |
| base | returns a copy of the underlying (adapted) view   (public member function) |
| pred | returns a reference to the stored predicate   (public member function) |
| begin | returns an iterator to the beginning   (public member function) |
| end | returns an iterator or a sentinel to the end   (public member function) |
| ****find_next**** | returns an iterator to the begin of the next subrange (exposition-only member function\*) |
| ****find_prev**** | returns an iterator to the begin of the previous subrange (exposition-only member function\*) |
| Inherited from std::ranges::view_interface | |
| empty | returns whether the derived view is empty. Provided if it satisfies `sized_range` or `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |
| operator bool | returns whether the derived view is not empty. Provided if ranges::empty is applicable to it.   (public member function of `std::ranges::view_interface<D>`) |
| front | returns the first element in the derived view. Provided if it satisfies `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| back | returns the last element in the derived view. Provided if it satisfies `bidirectional_range` and `common_range`.   (public member function of `std::ranges::view_interface<D>`) |

### Deduction guides

### Nested classes

|  |  |
| --- | --- |
| **iterator** | the iterator type (exposition-only member class template\*) |

### Notes

In order to provide the amortized constant time complexity required by the `range` concept, the result of `begin()` is cached within the `chunk_by_view` object. If the underlying range is modified after the first call to `begin()`, subsequent uses of the `chunk_by_view` object might have unintuitive behavior.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_ranges_chunk_by` | `202202L` | (C++23) | `std::ranges::chunk_by_view` |

### Example

Run this code

```
#include <functional>
#include <iostream>
#include <ranges>
#include <string_view>
 
void print_chunks(auto view, std::string_view separator = ", ")
{
    for (auto const subrange : view)
    {
        std::cout << '[';
        for (std::string_view prefix; auto const& elem : subrange)
            std::cout << prefix << elem, prefix = separator;
        std::cout << "] ";
    }
    std::cout << '\n';
}
 
int main()
{
    std::initializer_list v1 = {1, 2, 3, 1, 2, 3, 3, 3, 1, 2, 3};
    auto fn1 = std::ranges::less{};
    auto view1 = v1 | std::views::chunk_by(fn1);
    print_chunks(view1);
 
    std::initializer_list v2 = {1, 2, 3, 4, 4, 0, 2, 3, 3, 3, 2, 1};
    auto fn2 = std::ranges::not_equal_to{};
    auto view2 = v2 | std::views::chunk_by(fn2);
    print_chunks(view2);
 
    std::string_view v3 = "__cpp_lib_ranges_chunk_by";
    auto fn3 = [](auto x, auto y) { return not(x == '_' or y == '_'); };
    auto view3 = v3 | std::views::chunk_by(fn3);
    print_chunks(view3, "");
 
    std::string_view v4 = "\u007a\u00df\u6c34\u{1f34c}"; // "zß水🍌"
    auto fn4 = [](auto, auto ß) { return 128 == ((128 + 64) & ß); };
    auto view4 = v4 | std::views::chunk_by(fn4);
    print_chunks(view4, "");
}

```

Output:

```
[1, 2, 3] [1, 2, 3] [3] [3] [1, 2, 3] 
[1, 2, 3, 4] [4, 0, 2, 3] [3] [3, 2, 1] 
[_] [_] [cpp] [_] [lib] [_] [ranges] [_] [chunk] [_] [by]
[z] [ß] [水] [🍌]

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 26.7.30 Chunk by view [range.chunk.by]

### See also

|  |  |
| --- | --- |
| ranges::chunk_viewviews::chunk(C++23) | a range of `view`s that are `N`-sized non-overlapping successive chunks of the elements of another `view` (class template) (range adaptor object) |
| ranges::slide_viewviews::slide(C++23) | a `view` whose Mth element is a `view` over the Mth through (M + N - 1)th elements of another `view` (class template) (range adaptor object) |
| ranges::stride_viewviews::stride(C++23) | a `view` consisting of elements of another `view`, advancing over N elements at a time (class template) (range adaptor object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/chunk_by_view&oldid=176938>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 October 2024, at 13:03.