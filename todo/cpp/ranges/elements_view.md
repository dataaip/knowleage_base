# std::ranges::views::elements, std::ranges::elements_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | ****elements_viewviews::elements**** | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

****std::ranges::elements_view****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| elements_view::elements_view | | | | |
| elements_view::base | | | | |
| elements_view::begin | | | | |
| elements_view::end | | | | |
| elements_view::size | | | | |
| Nested classes | | | | |
| Iterator | | | | |
| elements_view::**iterator**::**iterator** | | | | |
| elements_view::**iterator**::base | | | | |
| elements_view::**iterator**::operator\* | | | | |
| [elements_view::**iterator**::operator[]](elements_view/iterator/operator_at.html "cpp/ranges/elements view/iterator/operator at") | | | | |
| elements_view::**iterator**::operator++ elements_view::**iterator**::operator++(int) elements_view::**iterator**::operator-- elements_view::**iterator**::operator--(int) elements_view::**iterator**::operator+= elements_view::**iterator**::operator-= | | | | |
| operator==(elements_view::**iterator**) operator<(elements_view::**iterator**) operator>(elements_view::**iterator**) operator<=(elements_view::**iterator**) operator>=(elements_view::**iterator**) operator<=>(elements_view::**iterator**) | | | | |
| operator+(elements_view::**iterator**) operator-(elements_view::**iterator**) | | | | |
| Sentinel | | | | |
| elements_view::**sentinel**::**sentinel** | | | | |
| elements_view::**sentinel**::base | | | | |
| operator==(elements_view::**iterator**,elements_view::**sentinel**) | | | | |
| operator-(elements_view::**iterator**,elements_view::**sentinel**) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< ranges::input_range V, std::size_t N >      requires ranges::view<V> &&               /\*has-tuple-element\*/<ranges::range_value_t<V>, N> &&               /\*has-tuple-element\*/<std::remove_reference_t<                                         ranges::range_reference_t<V>>, N> &&               /\*returnable-element\*/<ranges::range_reference_t<V>, N>  class elements_view : public ranges::view_interface<elements_view<V, N>>; | (1) | (since C++20) |
| namespace views {  template< std::size_t N >      constexpr /\* unspecified \*/ elements = /\* unspecified \*/; } | (2) | (since C++20) |
| Call signature |  |  |
| template< ranges::viewable_range R >      requires /\* see below \*/ constexpr ranges::view auto elements<N>( R&& r ); |  | (since C++20) |
| Helper concepts |  |  |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| template< class T, std::size_t N >  concept /\*has-tuple-element\*/ =      requires(T t) {          typename std::tuple_size<T>::type;          requires N < std::tuple_size_v<T>;          typename std::tuple_element_t<N, T>;          { std::get<N>(t) } -> std::convertible_to<                                    const std::tuple_element_t<N, T>&>; }; |  | (until C++23)  (exposition only\*) |
| template< class T, std::size_t N >  concept /\*has-tuple-element\*/ = /\*tuple-like\*/<T> && N < std::tuple_size_v<T> |  | (since C++23)  (exposition only\*) |
|  |  |  |
| --- | --- | --- |
| template< class T, std::size_t N >  concept returnable-element =       std::is_reference_v<T> || std::move_constructible< std::tuple_element_t<N, T>>; | (4) | (exposition only\*) |
|  |  |  |

1) Accepts a `view` of tuple-like values, and issues a view with a value type of the `N`th element of the adapted view's value-type.2) Every specialization of `views::elements` is a RangeAdaptorObject. The expression views::elements<M>(e) is expression-equivalent to elements_view<views::all_t<decltype((e))>, M>{e} for any suitable subexpression e and constant expression M.3) Ensures that the elements of the underlying view are tuple-like values, see **tuple-like**(since C++23).4) Ensures that dangling references cannot be returned.

`elements_view` models the concepts `random_access_range`, `bidirectional_range`, `forward_range`, `input_range`, `common_range`, and `sized_range` when the underlying view `V` models respective concepts.

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| `base_` (private) | the underlying (adapted) view of type `V` (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `elements_view`   (public member function) |
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

### Nested classes

|  |  |
| --- | --- |
| **iterator** | the iterator type (exposition-only member class template\*) |
| **sentinel** | the sentinel type (exposition-only member class template\*) |

### Helper templates

|  |  |  |
| --- | --- | --- |
| template<class T, std::size_t N>  constexpr bool enable_borrowed_range<std::ranges::elements_view<T, N>> = ranges::enable_borrowed_range<T>; |  | (since C++20) |
|  |  |  |

This specialization of ranges::enable_borrowed_range makes `elements_view` satisfy `borrowed_range` when the underlying view satisfies it.

### Example

Run this code

```
#include <iostream>
#include <ranges>
#include <string>
#include <tuple>
#include <vector>
 
int main()
{
    const std::vector<std::tuple<int, char, std::string>> vt
    {
        {1, 'A', "α"},
        {2, 'B', "β"},
        {3, 'C', "γ"},
        {4, 'D', "δ"},
        {5, 'E', "ε"},
    };
 
    for (int const e : std::views::elements<0>(vt))
        std::cout << e << ' ';
    std::cout << '\n';
 
    for (char const e : vt | std::views::elements<1>)
        std::cout << e << ' ';
    std::cout << '\n';
 
    for (std::string const& e : std::views::elements<2>(vt))
        std::cout << e << ' ';
    std::cout << '\n';
}

```

Output:

```
1 2 3 4 5
A B C D E
α β γ δ ε

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3494 | C++20 | `elements_view` was never a `borrowed_range` | it is a `borrowed_range` if its underlying view is |
| LWG 3502 | C++20 | dangling reference could be obtained from `elements_view` | such usage is forbidden |

### See also

|  |  |
| --- | --- |
| ranges::keys_viewviews::keys(C++20) | takes a `view` consisting of pair-like values and produces a `view` of the first elements of each pair (class template) (range adaptor object) |
| ranges::values_viewviews::values(C++20) | takes a `view` consisting of pair-like values and produces a `view` of the second elements of each pair (class template) (range adaptor object) |
| ranges::zip_viewviews::zip(C++23) | a `view` consisting of tuples of references to corresponding elements of the adapted views (class template) (customization point object) |
| ranges::zip_transform_viewviews::zip_transform(C++23) | a `view` consisting of results of application of a transformation function to corresponding elements of the adapted views (class template) (customization point object) |
| slice | BLAS-like slice of a valarray: starting index, length, stride   (class) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/elements_view&oldid=173599>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 July 2024, at 13:34.