# std::ranges::views::iota, std::ranges::iota_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty_viewviews::empty | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | single_viewviews::single | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | basic_istream_viewviews::istream | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****iota_viewviews::iota**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | repeat_viewviews::repeat(C++23)(C++23) | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

****std::ranges::iota_view****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| iota_view::iota_view | | | | |
| iota_view::begin | | | | |
| iota_view::end | | | | |
| iota_view::empty | | | | |
| iota_view::size | | | | |
| Deduction guides | | | | |
| Nested classes | | | | |
| **Iterator** | | | | |
| Helper concepts | | | | |
| **decrementable** | | | | |
| **advanceable** | | | | |
| Member types | | | | |
| Member functions | | | | |
| iota_view::**iterator**::**iterator** | | | | |
| iota_view::**iterator**::operator\* | | | | |
| [iota_view::**iterator**::operator[]](iota_view/iterator.html#Member_functions "cpp/ranges/iota view/iterator") | | | | |
| iota_view::**iterator**::operator++ iota_view::**iterator**::operator++(int) | | | | |
| iota_view::**iterator**::operator-- iota_view::**iterator**::operator--(int) | | | | |
| iota_view::**iterator**::operator+= | | | | |
| iota_view::**iterator**::operator-= | | | | |
| Non-member functions | | | | |
| operator==(iota_view::**iterator**) operator<(iota_view::**iterator**) operator>(iota_view::**iterator**) operator<=(iota_view::**iterator**) operator>=(iota_view::**iterator**) operator<=>(iota_view::**iterator**) | | | | |
| operator+(iota_view::**iterator**) | | | | |
| operator-(iota_view::**iterator**) | | | | |
| **Sentinel** | | | | |
| Member functions | | | | |
| iota_view::**sentinel**::**sentinel** | | | | |
| Non-member functions | | | | |
| operator==(iota_view::**iterator**,iota_view::**sentinel**) | | | | |
| operator-(iota_view::**iterator**,iota_view::**sentinel**) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< std::weakly_incrementable W,  std::semiregular Bound = std::unreachable_sentinel_t >      requires /\*weakly-equality-comparable-with\*/<W, Bound> && std::copyable<W>  class iota_view : public ranges::view_interface<iota_view<W, Bound>> | (1) | (since C++20) |
| namespace views {  inline constexpr /\* unspecified \*/ iota = /\* unspecified \*/; } | (2) | (since C++20) |
| Call signature |  |  |
| template< class W >      requires /\* see below \*/ constexpr /\* see below \*/ iota( W&& value ); |  | (since C++20) |
| template< class W, class Bound >      requires /\* see below \*/ constexpr /\* see below \*/ iota( W&& value, Bound&& bound ); |  | (since C++20) |
|  |  |  |

1) A range factory that generates a sequence of elements by repeatedly incrementing an initial value. Can be either bounded or unbounded (infinite).2) views::iota(e) and views::iota(e, f) are expression-equivalent to iota_view<std::decay_t<decltype((e))>>(e) and iota_view(e, f) respectively for any suitable subexpressions e and f.

### Customization point objects

The name `views::iota` denotes a **customization point object**, which is a const function object of a literal `semiregular` class type. For exposition purposes, the cv-unqualified version of its type is denoted as `__iota_fn`.

All instances of `__iota_fn` are equal. The effects of invoking different instances of type `__iota_fn` on the same arguments are equivalent, regardless of whether the expression denoting the instance is an lvalue or rvalue, and is const-qualified or not (however, a volatile-qualified instance is not required to be invocable). Thus, `views::iota` can be copied freely and its copies can be used interchangeably.

Given a set of types `Args...`, if std::declval<Args>()... meet the requirements for arguments to `views::iota` above, `__iota_fn` models

- std::invocable<__iota_fn, Args...>,
- std::invocable<const __iota_fn, Args...>,
- std::invocable<__iota_fn&, Args...>, and
- std::invocable<const __iota_fn&, Args...>.

Otherwise, no function call operator of `__iota_fn` participates in overload resolution.

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| `W` `value_` | the beginning value (exposition-only member object\*) |
| `Bound` `bound_` | the sentinel value, may be unreachable (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | creates an `iota_view`   (public member function) |
| begin | obtains the beginning iterator of an `iota_view`   (public member function) |
| end | obtains the sentinel denoting the end of an `iota_view`   (public member function) |
| empty | tests whether the `iota_view` is empty (i.e. the iterator and the sentinel compare equal)   (public member function) |
| size(optional) | obtains the size of an `iota_view` (only provided if it is bounded)   (public member function) |
| Inherited from std::ranges::view_interface | |
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
| **iterator** | the iterator type (exposition-only member class\*) |
| **sentinel** | the sentinel type used when the `iota_view` is bounded and `Bound` and `W` are not the same type (exposition-only member class\*) |

### Helper templates

|  |  |  |
| --- | --- | --- |
| template< std::weakly_incrementable W, std::semiregular Bound >  constexpr bool ranges::enable_borrowed_range<ranges::iota_view<W, Bound>> = true; |  | (since C++20) |
|  |  |  |

This specialization of ranges::enable_borrowed_range makes `iota_view` satisfy `borrowed_range`.

### Example

Run this code

```
#include <algorithm>
#include <iostream>
#include <ranges>
 
struct Bound
{
    int bound;
    bool operator==(int x) const { return x == bound; }
};
 
int main()
{
    for (int i : std::ranges::iota_view{1, 10})
        std::cout << i << ' ';
    std::cout << '\n';
 
    for (int i : std::views::iota(1, 10))
        std::cout << i << ' ';
    std::cout << '\n';
 
    for (int i : std::views::iota(1, Bound{10}))
        std::cout << i << ' ';
    std::cout << '\n';
 
    for (int i : std::views::iota(1) | std::views::take(9))
        std::cout << i << ' ';
    std::cout << '\n';
 
    std::ranges::for_each(std::views::iota(1, 10),
                          [](int i){ std::cout << i << ' '; });
    std::cout << '\n';
}

```

Output:

```
1 2 3 4 5 6 7 8 9
1 2 3 4 5 6 7 8 9
1 2 3 4 5 6 7 8 9
1 2 3 4 5 6 7 8 9
1 2 3 4 5 6 7 8 9

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 4096 | C++20 | `views::iota` could copy an `iota_view` as-is | forbidden |
| P2325R3 | C++20 | `iota_view` required that `W` is `semiregular` as `view` required `default_initializable` | only requires that `W` is `copyable` |

### See also

|  |  |
| --- | --- |
| iota(C++11) | fills a range with successive increments of the starting value   (function template) |
| ranges::iota(C++23) | fills a range with successive increments of the starting value (algorithm function object) |
| ranges::repeat_viewviews::repeat(C++23) | a `view` consisting of a generated sequence by repeatedly producing the same value (class template) (customization point object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/iota_view&oldid=176915>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 October 2024, at 19:02.