# std::ranges::ref_view

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ****ref_view**** | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

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
| template< ranges::range R >      requires std::is_object_v<R>  class ref_view : public ranges::view_interface<ref_view<R>> |  | (since C++20) |
|  |  |  |

`ref_view` is a `view` of the elements of some other `range`. It wraps a reference to that `range`.

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| `r_` (private) | A pointer of type `R*` to the underlying range. (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a `ref_view` that references to the given range   (public member function) |
| base | returns the references to the referenced range   (public member function) |
| begin | returns the beginning iterator of the referenced range   (public member function) |
| end | returns the sentinel of the referenced range   (public member function) |
| empty | checks whether the referenced range is empty   (public member function) |
| size | returns the size of the referenced `sized_range`   (public member function) |
| data | returns the pointer to the beginning of the referenced `contiguous_range`   (public member function) |
| Inherited from std::ranges::view_interface | |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |
| operator bool | returns whether the derived view is not empty. Provided if ranges::empty is applicable to it.   (public member function of `std::ranges::view_interface<D>`) |
| front | returns the first element in the derived view. Provided if it satisfies `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| back | returns the last element in the derived view. Provided if it satisfies `bidirectional_range` and `common_range`.   (public member function of `std::ranges::view_interface<D>`) |
| [operator[]](view_interface/operator_at.html "cpp/ranges/view interface/operator at") | returns the `n`th element in the derived view. Provided if it satisfies `random_access_range`.   (public member function of `std::ranges::view_interface<D>`) |

## std::ranges::ref_view::ref_view

|  |  |  |
| --- | --- | --- |
| template< /\*different-from\*/<ref_view> T >      requires std::convertible_to<T, R&> && requires { _FUN(std::declval<T>()); } constexpr ref_view( T&& t ); |  | (since C++20) |
|  |  |  |

Initializes `r_` with std::addressof(static_cast<R&>(std::forward<T>(t))).

/\*different-from\*/<T, U> is satisfied if and only if std::remove_cvref_t<T> and std::remove_cvref_t<U> are not the same type, and overloads of `_FUN` are declared as void _FUN(R&); void _FUN(R&&) = delete;.

### Parameters

|  |  |  |
| --- | --- | --- |
| t | - | range to reference |

## std::ranges::ref_view::base

|  |  |  |
| --- | --- | --- |
| constexpr R& base() const; |  | (since C++20) |
|  |  |  |

Equivalent to return \*r_;.

## std::ranges::ref_view::begin

|  |  |  |
| --- | --- | --- |
| constexpr ranges::iterator_t<R> begin() const; |  | (since C++20) |
|  |  |  |

Equivalent to return ranges::begin(\*r_);.

## std::ranges::ref_view::end

|  |  |  |
| --- | --- | --- |
| constexpr ranges::sentinel_t<R> end() const; |  | (since C++20) |
|  |  |  |

Equivalent to return ranges::end(\*r_);.

## std::ranges::ref_view::empty

|  |  |  |
| --- | --- | --- |
| constexpr bool empty() const      requires requires { ranges::empty(\*r_); }; |  | (since C++20) |
|  |  |  |

Equivalent to return ranges::empty(\*r_);.

## std::ranges::ref_view::size

|  |  |  |
| --- | --- | --- |
| constexpr auto size() const      requires ranges::sized_range<R>; |  | (since C++20) |
|  |  |  |

Equivalent to return ranges::size(\*r_);.

## std::ranges::ref_view::data

|  |  |  |
| --- | --- | --- |
| constexpr auto data() const      requires ranges::contiguous_range<R>; |  | (since C++20) |
|  |  |  |

Equivalent to return ranges::data(\*r_);.

### Deduction guides

|  |  |  |
| --- | --- | --- |
| template< class R >  ref_view( R& ) -> ref_view<R>; |  | (since C++20) |
|  |  |  |

### Helper templates

|  |  |  |
| --- | --- | --- |
| template< class T >  constexpr bool enable_borrowed_range<ranges::ref_view<T>> = true; |  | (since C++20) |
|  |  |  |

This specialization of `std::ranges::enable_borrowed_range` makes `ref_view` satisfy `borrowed_range`.

### Example

Run this code

```
#include <iostream>
#include <ranges>
 
int main()
{
    const std::string s{"cosmos"};
 
    const std::ranges::take_view tv{s, 3};
    const std::ranges::ref_view rv{tv};
 
    std::cout
        << std::boolalpha
        << "call empty() : " << rv.empty() << '\n'
        << "call size()  : " << rv.size() << '\n'
        << "call begin() : " << *rv.begin() << '\n'
        << "call end()   : " << *(rv.end() - 1) << '\n'
        << "call data()  : " << rv.data() << '\n'
        << "call base()  : " << rv.base().size() << '\n' // ~> tv.size()
        << "range-for    : ";
 
    for (const auto c : rv)
        std::cout << c;
    std::cout << '\n';
}

```

Output:

```
call empty() : false
call size()  : 3
call begin() : c
call end()   : s
call data()  : cosmos
call base()  : 3
range-for    : cos

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P2325R3 | C++20 | default constructor was provided as `view` must be `default_initializable` | removed along with the requirement |

### See also

|  |  |
| --- | --- |
| reference_wrapper(C++11) | CopyConstructible and CopyAssignable reference wrapper   (class template) |
| ranges::owning_view(C++20) | a `view` with unique ownership of some `range`   (class template) |
| views::all_tviews::all(C++20) | a `view` that includes all elements of a `range` (alias template) (range adaptor object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/ref_view&oldid=172702>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 June 2024, at 22:57.