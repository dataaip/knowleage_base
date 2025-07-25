# std::ranges::views::repeat, std::ranges::repeat_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty_viewviews::empty | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | single_viewviews::single | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | basic_istream_viewviews::istream | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota_viewviews::iota | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****repeat_viewviews::repeat****(C++23)(C++23) | | | | | |

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

****std::ranges::repeat_view****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| repeat_view::repeat_view | | | | |
| repeat_view::begin | | | | |
| repeat_view::end | | | | |
| repeat_view::size | | | | |
| Deduction guides | | | | |
| Iterator | | | | |
| Member functions | | | | |
| repeat_view::**iterator**::**iterator** | | | | |
| repeat_view::**iterator**::operator\* | | | | |
| [repeat_view::**iterator**::operator[]](repeat_view/iterator.html#Member_functions "cpp/ranges/repeat view/iterator") | | | | |
| repeat_view::**iterator**::operator++ repeat_view::**iterator**::operator++(int) | | | | |
| repeat_view::**iterator**::operator-- repeat_view::**iterator**::operator--(int) | | | | |
| repeat_view::**iterator**::operator+= | | | | |
| repeat_view::**iterator**::operator-= | | | | |
| Non-member functions | | | | |
| operator==(repeat_view::**iterator**) operator<=>(repeat_view::**iterator**) | | | | |
| operator+(repeat_view::**iterator**) | | | | |
| operator-(repeat_view::**iterator**) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template< std::move_constructible W,  std::semiregular Bound = std::unreachable_sentinel_t >      requires (std::is_object_v<W> && std::same_as<W, std::remove_cv_t<W>> &&               (/\*integer-like-with-usable-difference-type\*/<Bound> ||                std::same_as<Bound, std::unreachable_sentinel_t>)) class repeat_view : public ranges::view_interface<repeat_view<W, Bound>> | (1) | (since C++23) |
| namespace views {  inline constexpr /\* unspecified \*/ repeat = /\* unspecified \*/; } | (2) | (since C++23) |
| Call signature |  |  |
| template< class W >      requires /\* see below \*/ constexpr /\* see below \*/ repeat( W&& value ); |  | (since C++23) |
| template< class W, class Bound >      requires /\* see below \*/ constexpr /\* see below \*/ repeat( W&& value, Bound&& bound ); |  | (since C++23) |
| Helper concepts |  |  |
| concept /\*integer-like-with-usable-difference-type\*/ =  /\*is-signed-integer-like\*/<T> || (/\*is-integer-like\*/ <T> && std::weakly_incrementable<T>) | (3) | (exposition only\*) |
|  |  |  |

1) A range factory that generates a sequence of elements by repeatedly producing the same value. Can be either bounded or unbounded (infinite).2) views::repeat(e) and views::repeat(e, f) are expression-equivalent to repeat_view<std::decay_t<decltype((E))>>(e) and repeat_view(e, f) respectively for any suitable subexpressions e and f.3) Determines whether a type is integer-like and has a usable difference type.

`repeat_view` models `random_access_range`. If `Bound` is not std::unreachable_sentinel_t, `repeat_view` also models `sized_range` and `common_range`.

### Customization point objects

The name `views::repeat` denotes a **customization point object**, which is a const function object of a literal `semiregular` class type. For exposition purposes, the cv-unqualified version of its type is denoted as `__repeat_fn`.

All instances of `__repeat_fn` are equal. The effects of invoking different instances of type `__repeat_fn` on the same arguments are equivalent, regardless of whether the expression denoting the instance is an lvalue or rvalue, and is const-qualified or not (however, a volatile-qualified instance is not required to be invocable). Thus, `views::repeat` can be copied freely and its copies can be used interchangeably.

Given a set of types `Args...`, if std::declval<Args>()... meet the requirements for arguments to `views::repeat` above, `__repeat_fn` models

- std::invocable<__repeat_fn, Args...>,
- std::invocable<const __repeat_fn, Args...>,
- std::invocable<__repeat_fn&, Args...>, and
- std::invocable<const __repeat_fn&, Args...>.

Otherwise, no function call operator of `__repeat_fn` participates in overload resolution.

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| `movable-box` ﻿<W> `value_` | the repeating element of the view (exposition-only member object\*) |
| `Bound` `bound_` | the sentinel value (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | creates a `repeat_view`   (public member function) |
| begin | obtains the beginning iterator of a `repeat_view`   (public member function) |
| end | obtains the sentinel denoting the end of a `repeat_view`   (public member function) |
| size | obtains the size of a `repeat_view` if it is sized   (public member function) |
| Inherited from std::ranges::view_interface | |
| empty | returns whether the derived view is empty. Provided if it satisfies `sized_range` or `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |
| operator bool | returns whether the derived view is not empty. Provided if ranges::empty is applicable to it.   (public member function of `std::ranges::view_interface<D>`) |
| front | returns the first element in the derived view. Provided if it satisfies `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| back | returns the last element in the derived view. Provided if it satisfies `bidirectional_range` and `common_range`.   (public member function of `std::ranges::view_interface<D>`) |
| [operator[]](view_interface/operator_at.html "cpp/ranges/view interface/operator at") | returns the `n`th element in the derived view. Provided if it satisfies `random_access_range`.   (public member function of `std::ranges::view_interface<D>`) |

## std::ranges::repeat_view::repeat_view

|  |  |  |
| --- | --- | --- |
| repeat_view() requires std::default_initializable<W> = default; | (1) | (since C++23) |
| constexpr explicit repeat_view( const W& value, Bound bound = Bound() ); | (2) | (since C++23) |
| constexpr explicit repeat_view( W&& value, Bound bound = Bound() ); | (3) | (since C++23) |
| template < class... WArgs, class... BoundArgs >      requires std::constructible_from<W, WArgs...>            && std::constructible_from<Bound, BoundArgs...>  constexpr explicit      repeat( std::piecewise_construct_t, std::tuple<WArgs...> value_args, std::tuple<BoundArgs...> bound_args = std::tuple<>{} ); | (4) | (since C++23) |
|  |  |  |

1) Default-initializes `value_` and value-initializes `bound_` ﻿.2) Initializes `value_` with value and initializes `bound_` with bound. If `Bound` is not std::unreachable_sentinel_t and bool(bound >= 0) is false, the behavior is undefined.3) Initializes `value_` with std::move(value) and initializes `bound_` with bound. If `Bound` is not std::unreachable_sentinel_t and bool(bound >= 0) is false, the behavior is undefined.4) Initializes `value_` with std::make_from_tuple<T>(std::move(value_args)) and `bound_` with std::make_from_tuple<Bound>(std::move(bound_args)). If `Bound` is not std::unreachable_sentinel_t and bool(bound >= 0) is false, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| value | - | the value to be repeatedly produced |
| bound | - | the bound |
| value_args | - | the tuple containing the initializers of `value_` |
| bound_args | - | the tuple containing the initializers of `bound_` |

## std::ranges::repeat_view::begin

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/ begin() const; |  | (since C++23) |
|  |  |  |

Returns `iterator` ﻿(std::addressof(\*`value_` ﻿)).

## std::ranges::repeat_view::end

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/ end() const      requires (!std::same_as<Bound, std::unreachable_sentinel_t>); | (1) | (since C++23) |
| constexpr std::unreachable_sentinel_t end() const; | (2) | (since C++23) |
|  |  |  |

1) Returns `iterator` ﻿(std::addressof(\*`value_` ﻿),`bound_` ﻿).2) Returns std::unreachable_sentinel.

## std::ranges::repeat_view::size

|  |  |  |
| --- | --- | --- |
| constexpr auto size() const      requires (!std::same_as<Bound, std::unreachable_sentinel_t>); |  | (since C++23) |
|  |  |  |

Returns `to-unsigned-like` ﻿(`bound_` ﻿).

### Deduction guides

|  |  |  |
| --- | --- | --- |
| template< class W, class Bound = std::unreachable_sentinel_t >  repeat_view( W, Bound = Bound() ) -> repeat_view<W, Bound>; |  | (since C++23) |
|  |  |  |

### Nested classes

|  |  |
| --- | --- |
| **iterator** | the iterator type (exposition-only member class\*) |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_ranges_repeat` | `202207L` | (C++23) | `std::ranges::repeat_view` |

### Example

Run this code

```
#include <iostream>
#include <ranges>
#include <string_view>
using namespace std::literals;
 
int main()
{
    // bounded overload
    for (auto s : std::views::repeat("C++"sv, 3))
        std::cout << s << ' ';
    std::cout << '\n';
 
    // unbounded overload
    for (auto s : std::views::repeat("I know that you know that"sv)
                | std::views::take(3))
        std::cout << s << ' ';
    std::cout << "...\n";
}

```

Output:

```
C++ C++ C++
I know that you know that I know that you know that I know that you know that ...

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 4053 | C++20 | unary calls to `views::repeat` did not decay the argument | decay the argument |
| LWG 4054 | C++20 | calling `views::repeat` with a `repeat_view` did not create a nested `repeat_view` | creates a nested `repeat_view` |

### See also

|  |  |
| --- | --- |
| ranges::iota_viewviews::iota(C++20) | a `view` consisting of a sequence generated by repeatedly incrementing an initial value (class template) (customization point object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/repeat_view&oldid=176947>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 October 2024, at 17:36.