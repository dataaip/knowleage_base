# std::ranges::views::single, std::ranges::single_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty_viewviews::empty | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****single_viewviews::single**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | basic_istream_viewviews::istream | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota_viewviews::iota | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | repeat_viewviews::repeat(C++23)(C++23) | | | | | |

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

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< std::copy_constructible T >      requires std::is_object_v<T>  class single_view : public ranges::view_interface<single_view<T>> |  | (since C++20)  (until C++23) |
| template< std::move_constructible T >      requires std::is_object_v<T>  class single_view : public ranges::view_interface<single_view<T>> |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| namespace views {  inline constexpr /\* unspecified \*/ single = /\* unspecified \*/; } | (2) | (since C++20) |
| Call signature |  |  |
| template< class T >      requires /\* see below \*/ constexpr /\* see below \*/ single( T&& t ); |  | (since C++20) |
|  |  |  |

1) Produces a `view` that contains exactly one element of a specified value.2) The expression views::single(e) is expression-equivalent to single_view<std::decay_t<decltype((e))>>(e) for any suitable subexpression e.

The lifetime of the element is bound to the parent `single_view`. Copying `single_view` makes a copy of the element.

### Customization point objects

The name `views::single` denotes a **customization point object**, which is a const function object of a literal `semiregular` class type. For exposition purposes, the cv-unqualified version of its type is denoted as `__single_fn`.

All instances of `__single_fn` are equal. The effects of invoking different instances of type `__single_fn` on the same arguments are equivalent, regardless of whether the expression denoting the instance is an lvalue or rvalue, and is const-qualified or not (however, a volatile-qualified instance is not required to be invocable). Thus, `views::single` can be copied freely and its copies can be used interchangeably.

Given a set of types `Args...`, if std::declval<Args>()... meet the requirements for arguments to `views::single` above, `__single_fn` models

- std::invocable<__single_fn, Args...>,
- std::invocable<const __single_fn, Args...>,
- std::invocable<__single_fn&, Args...>, and
- std::invocable<const __single_fn&, Args...>.

Otherwise, no function call operator of `__single_fn` participates in overload resolution.

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| `copyable-box` ﻿`<T>` `value_` (until C++23) | the single element of the view (exposition-only member object\*) |
| `movable-box` ﻿`<T>` `value_` (since C++23) | the single element of the view (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `single_view`   (public member function) |
| begin | returns a pointer to the element   (public member function) |
| end | returns a pointer past the element   (public member function) |
| empty[static] | returns false   (public static member function) |
| size[static] | returns 1   (public static member function) |
| data | returns a pointer to the element   (public member function) |
| Inherited from std::ranges::view_interface | |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |
| operator bool | returns whether the derived view is not empty. Provided if ranges::empty is applicable to it.   (public member function of `std::ranges::view_interface<D>`) |
| front | returns the first element in the derived view. Provided if it satisfies `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| back | returns the last element in the derived view. Provided if it satisfies `bidirectional_range` and `common_range`.   (public member function of `std::ranges::view_interface<D>`) |
| [operator[]](view_interface/operator_at.html "cpp/ranges/view interface/operator at") | returns the `n`th element in the derived view. Provided if it satisfies `random_access_range`.   (public member function of `std::ranges::view_interface<D>`) |

## std::ranges::single_view::single_view

|  |  |  |
| --- | --- | --- |
| single_view() requires std::default_initializable<T> = default; | (1) | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| constexpr explicit single_view( const T& t ); |  | (since C++20)  (until C++23) |
| constexpr explicit single_view( const T& t )      requires std::copy_constructible<T>; |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| constexpr explicit single_view( T&& t ); | (3) | (since C++20) |
| template< class... Args >      requires std::constructible_from<T, Args...> constexpr explicit single_view( std::in_place_t, Args&&... args ); | (4) | (since C++20) |
|  |  |  |

Constructs a `single_view`.

1) Default initializes `value_`, which value-initializes its contained value.2) Initializes `value_` with t.3) Initializes `value_` with std::move(t).4) Initializes `value_` as if by `value_`{std::in_place, std::forward<Args>(args)...}.

## std::ranges::single_view::begin

|  |  |  |
| --- | --- | --- |
| constexpr T\* begin() noexcept;  constexpr const T\* begin() const noexcept; |  | (since C++20) |
|  |  |  |

Equivalent to return data();.

## std::ranges::single_view::end

|  |  |  |
| --- | --- | --- |
| constexpr T\* end() noexcept;  constexpr const T\* end() const noexcept; |  | (since C++20) |
|  |  |  |

Equivalent to return data() + 1;.

## std::ranges::single_view::empty

|  |  |  |
| --- | --- | --- |
| static constexpr bool empty() noexcept; |  | (since C++20) |
|  |  |  |

Equivalent to return false;.

## std::ranges::single_view::size

|  |  |  |
| --- | --- | --- |
| static constexpr std::size_t size() noexcept; |  | (since C++20) |
|  |  |  |

Equivalent to return 1;.

Makes `single_view` model /\*tiny-range\*/ as required by `split_view`.

## std::ranges::single_view::data

|  |  |  |
| --- | --- | --- |
| constexpr T\* data() noexcept;  constexpr const T\* data() const noexcept; |  | (since C++20) |
|  |  |  |

Returns a pointer to the contained value of `value_`. The behavior is undefined if `value_` does not contains a value.

### Deduction guides

|  |  |  |
| --- | --- | --- |
| template< class T >  single_view( T ) -> single_view<T>; |  | (since C++20) |
|  |  |  |

### Notes

For a `single_view`, the inherited `empty` member function always returns false, and the inherited operator bool conversion function always returns true.

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <ranges>
#include <string>
#include <tuple>
 
int main()
{
    constexpr std::ranges::single_view sv1{3.1415}; // uses (const T&) constructor
    static_assert(sv1);
    static_assert(not sv1.empty());
 
    std::cout << "1) *sv1.data(): " << *sv1.data() << '\n'
              << "2) *sv1.begin(): " << *sv1.begin() << '\n'
              << "3)  sv1.size(): " << sv1.size() << '\n'
              << "4)  distance: " << std::distance(sv1.begin(), sv1.end()) << '\n';
 
    std::string str{"C++20"};
    std::cout << "5)  str = " << std::quoted(str) << '\n';
    std::ranges::single_view sv2{std::move(str)}; // uses (T&&) constructor
    std::cout << "6) *sv2.data(): " << std::quoted(*sv2.data()) << '\n'
              << "7)  str = " << std::quoted(str) << '\n';
 
    std::ranges::single_view<std::tuple<int, double, std::string>>
        sv3{std::in_place, 42, 3.14, "😄"}; // uses (std::in_place_t, Args&&... args)
 
    std::cout << "8)  sv3 holds a tuple: { "
              << std::get<0>(sv3[0]) << ", "
              << std::get<1>(sv3[0]) << ", "
              << std::get<2>(sv3[0]) << " }\n";
}

```

Output:

```
1) *sv1.data(): 3.1415
2) *sv1.begin(): 3.1415
3)  sv1.size(): 1
4)  distance: 1
5)  str = "C++20"
6) *sv2.data(): "C++20"
7)  str = ""
8)  sv3 holds a tuple: { 42, 3.14, 😄 }

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3428 | C++20 | `single_view` was convertible from std::in_place_t | the constructor is made explicit |
| LWG 4035 | C++20 | `single_view` did not provide the member function `empty()` | provides `empty()` |
| P2367R0 | C++20 | deduction guides for `single_view` failed to decay the argument; `views::single` copied but not wrapped a `single_view` | a decaying guide provided; made always wrapping |

### See also

|  |  |
| --- | --- |
| optional(C++17) | a wrapper that may or may not hold an object   (class template) |
| ranges::empty_viewviews::empty(C++20) | an empty `view` with no elements (class template) (variable template) |
| ranges::split_viewviews::split(C++20) | a `view` over the subranges obtained from splitting another `view` using a delimiter (class template) (range adaptor object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/single_view&oldid=176146>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 September 2024, at 23:57.