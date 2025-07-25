# std::ranges::subrange<I,S,K>::operator PairLike

From cppreference.com
< cpp‎ | ranges‎ | subrange
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest")(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

std::ranges::subrange

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| subrange::subrange | | | | |
| ****subrange::operator PairLike**** | | | | |
| Observers | | | | |
| subrange::begin | | | | |
| subrange::end | | | | |
| subrange::empty | | | | |
| subrange::size | | | | |
| Iterator operations | | | | |
| subrange::advance | | | | |
| subrange::next | | | | |
| subrange::prev | | | | |
| Deduction guides | | | | |
| Non-member functions | | | | |
| get(std::ranges::subrange) | | | | |
| Helper types | | | | |
| subrange_kind | | | | |
| tuple_size<std::ranges::subrange> | | | | |
| tuple_element<std::ranges::subrange> | | | | |

|  |  |  |
| --- | --- | --- |
| template< /\*different-from\*/<subrange> PairLike >      requires /\*pair-like-convertible-from\*/<PairLike, const I&, const S&> constexpr operator PairLike() const; | (1) | (since C++20) |
| Helper concepts |  |  |
| template< class T >  concept /\*pair-like\*/ = /\* see description \*/; | (2) | (exposition only\*) |
| template< class T, class U, class V >  concept /\*pair-like-convertible-from\*/ = /\* see description \*/; | (3) | (exposition only\*) |
|  |  |  |

1) Converts `subrange` to a pair-like type. For the definition of /\*different-from\*/, see `different-from` ﻿.2) Determines whether a type is **pair-like** ﻿.

|  |  |
| --- | --- |
| Equivalent to:   ```text template< class T > concept /*pair-like*/ =     !std::is_reference_v<T> && requires(T t)     {         typename std::tuple_size<T>::type;         requires std::derived_from<std::tuple_size<T>,                                    std::integral_constant<std::size_t, 2>>;         typename std::tuple_element_t<0, std::remove_const_t<T>>;         typename std::tuple_element_t<1, std::remove_const_t<T>>;         { std::get<0>(t) } -> std::convertible_to<                                   const std::tuple_element_t<0, T>&>;         { std::get<1>(t) } -> std::convertible_to<                                   const std::tuple_element_t<1, T>&>;     }; ``` | (until C++23) |
| This concept is equivalent to the library-wide exposition-only concept **pair-like**. | (since C++23) |

3) Determines whether a pair-like type can be constructed from two values of possibly different given types.

|  |  |
| --- | --- |
| Equivalent to:   ```text template< class T, class U, class V > concept /*pair-like-convertible-from*/ =     !ranges::range<T> && /*pair-like*/<T> &&     std::constructible_from<T, U, V> &&     /*convertible-to-non-slicing*/<U, std::tuple_element_t<0, T>> &&     std::convertible_to<V, std::tuple_element_t<1, T>>; ``` | (until C++23) |
| Equivalent to:   ```text template< class T, class U, class V > concept /*pair-like-convertible-from*/ =     !ranges::range<T> && !std::is_reference_v<T> && /*pair-like*/<T> &&     std::constructible_from<T, U, V> &&     /*convertible-to-non-slicing*/<U, std::tuple_element_t<0, T>> &&     std::convertible_to<V, std::tuple_element_t<1, T>>; ``` | (since C++23) |

### Return value

PairLike(`begin_` ﻿,`end_` ﻿)

### Notes

Following types in the standard library are pair-like:

- std::pair<T, U>
- std::tuple<T, U>
- std::array<T, 2>
- std::ranges::subrange<I, S, K>

|  |  |
| --- | --- |
| - std::complex<T> | (since C++26) |

|  |  |
| --- | --- |
| A program-defined type derived from one of these types can be a pair-like type, if   - std::tuple_size and std::tuple_element are correctly specialized for it, and - calls to std::get<0> and std::get<1> for its value are well-formed. | (until C++23) |

Since `subrange` specializations are `range` types, conversion to them are not performed via this conversion function.

std::array specializations cannot be converted from `subrange`, since they are `range` types.

### Example

Run this code

```
#include <iostream>
#include <ranges>
#include <string>
#include <utility>
 
using striter = std::string::const_iterator;
 
using legacy_strview = std::pair<striter, striter>;
 
void legacy_print(legacy_strview p)
{
    for (; p.first != p.second; ++p.first)
        std::cout << *p.first << ' ';
    std::cout << '\n';
}
 
int main()
{
    std::string dat{"ABCDE"};
    for (auto v{std::ranges::subrange{dat}}; v; v = {v.begin(), v.end() - 1})
    {
        /*...*/
        legacy_print(legacy_strview{v});
    }
}

```

Output:

```
A B C D E 
A B C D 
A B C 
A B 
A

```

### See also

|  |  |
| --- | --- |
| **tuple-likepair-like**(C++23) | specifies that a type implemented the **tuple protocol** (std::get, std::tuple_element, std::tuple_size) (exposition-only concept\*) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/subrange/operator_PairLike&oldid=176901>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 October 2024, at 16:53.