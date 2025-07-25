# std::ranges::concat_view<Views...>::**iterator**

From cppreference.com
< cpp‎ | ranges‎ | concat view
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

std::ranges::concat_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| concat_view::concat_view | | | | |
| concat_view::begin | | | | |
| concat_view::end | | | | |
| concat_view::size | | | | |
| Deduction guides | | | | |
| ****Iterator**** | | | | |
| Member functions | | | | |
| concat_view::**iterator**::**iterator** | | | | |
| concat_view::**iterator**::operator\* | | | | |
| [concat_view::**iterator**::operator[]](iterator/operator_at.html "cpp/ranges/concat view/iterator/operator at") | | | | |
| concat_view::**iterator**::operator++ concat_view::**iterator**::operator++(int) concat_view::**iterator**::operator-- concat_view::**iterator**::operator--(int) concat_view::**iterator**::operator+= concat_view::**iterator**::operator-= | | | | |
| concat_view::**iterator**::**satisfy** concat_view::**iterator**::**prev** concat_view::**iterator**::**advance-fwd** concat_view::**iterator**::**advance-bwd** | | | | |
| Non-member functions | | | | |
| operator==(concat_view::**iterator**) operator<(concat_view::**iterator**) operator>(concat_view::**iterator**) operator<=(concat_view::**iterator**) operator>=(concat_view::**iterator**) operator<=>(concat_view::**iterator**) | | | | |
| operator+(concat_view::**iterator**) operator-(concat_view::**iterator**) | | | | |
| iter_move(concat_view::**iterator**) | | | | |
| iter_swap(concat_view::**iterator**) | | | | |

|  |  |  |
| --- | --- | --- |
| template< bool Const >  class /\*iterator\*/ | (1) | (exposition only\*) |
| Helper concepts |  |  |
| template< bool Const, class... Rs >  concept /\*concat-is-random-access\*/ = /\* see description \*/; | (2) | (exposition only\*) |
| template< bool Const, class... Rs >  concept /\*concat-is-bidirectional\*/ = /\* see description \*/; | (3) | (exposition only\*) |
|  |  |  |

1) ranges::concat_view<Views...>::`iterator` is the type of the iterators returned by `begin()` and `end()` of ranges::concat_view<Views...>.2) Let `Fs` be the pack that consists of all elements of `Rs` except the last element. Equivalent to 

template<bool Const, class... Rs>  
concept`concat-is-random-access`= // exposition only  
`all-random-access` ﻿<Const, Rs...> &&  
(ranges::common_range<`maybe-const` ﻿<Const, Fs>> && ...);

.3) Let `Fs` be the pack that consists of all elements of `Rs` except the last element. Equivalent to 

template<bool Const, class... Rs>  
concept`concat-is-bidirectional`= // exposition only  
`all-bidirectional` ﻿<Const, Rs...> &&  
(ranges::common_range<`maybe-const` ﻿<Const, Fs>> && ...);

.

### Template parameters

|  |  |  |
| --- | --- | --- |
| Const | - | whether the iterator is a constant iterator |

### Nested types

|  |  |
| --- | --- |
| Exposition-only types | |
| Type | Definition |
| `base-iter` | std::variant<ranges::iterator_t<`maybe-const` ﻿<Const, Views>>...> (exposition-only member type\*) |
| Iterator property types | |
| Type | Definition |
| `iterator_concept` | an iterator tag, see below |
| `iterator_category` (conditionally present) | an iterator tag, see below |
| `value_type` | `concat-value-t` ﻿<`maybe-const` ﻿<Const, Views>...> |
| `difference_type` | std::common_type_t<ranges::range_difference_t<`maybe-const` ﻿<Const, Views>>...> |

#### Determining the iterator concept

`iterator_concept` is defined as follows:

- If `concat-is-random-access` ﻿<Const, Views...> is modeled, `iterator_concept` denotes std::random_access_iterator_tag.
- Otherwise, if `concat-is-bidirectional` ﻿<Const, Views...> is modeled, `iterator_concept` denotes std::bidirectional_iterator_tag.
- Otherwise, if `all-forward` ﻿<Const, Views...> is modeled, `iterator_concept` denotes std::forward_iterator_tag.
- Otherwise, `iterator_concept` denotes std::input_iterator_tag.

#### Determining the iterator category

`iterator_category` is defined if and only if `all-forward` ﻿<Const, Views...> is modeled. In this case, it is defined as follows:

- If std::is_reference_v<`concat-reference-t` ﻿<`maybe-const` ﻿<Const, Views>...>> is false, `iterator_category` denotes std::input_iterator_tag.
- Otherwise, let `Cs` denote the pack of types std::iterator_traits<ranges::iterator_t<`maybe-const` ﻿<Const, Views>>>::iterator_category...:
  - If (std::derived_from<Cs, std::random_access_iterator_tag> && ...) &&  
    `concat-is-random-access` ﻿<Const, Views...> is true, `iterator_category` denotes std::random_access_iterator_tag.
  - Otherwise, if (std::derived_from<Cs, std::bidirectional_iterator_tag> && ...) &&  
    `concat-is-bidirectional` ﻿<Const, Views...> is true, `iterator_category` denotes std::bidirectional_iterator_tag.
  - Otherwise, if (std::derived_from<Cs, std::forward_iterator_tag> && ...) is true, `iterator_category` denotes std::forward_iterator_tag.
  - Otherwise, `iterator_category` denotes std::input_iterator_tag.

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| `maybe-const` ﻿<Const, ranges::concat_view>\* `parent_` | a pointer to the parent `concat_view` (exposition-only member object\*) |
| `base-iter` `it_` | an iterator into the current view (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs an iterator   (public member function) |
| operator\* | accesses the element   (public member function) |
| [operator[]](iterator/operator_at.html "cpp/ranges/concat view/iterator/operator at") | accesses an element by index   (public member function) |
| operator++operator++(int)operator--operator--(int)operator+=operator-= | advances or decrements the underlying iterator   (public member function) |
| Exposition-only function templates | |
| ****satisfy**** | replaces `it_` with the beginning of the next view, if `it_` is the end of current view (exposition-only member function\*) |
| ****prev**** | decrements `it_` such that it points to the previous position (exposition-only member function\*) |
| ****advance-fwd**** | advances the current position on given offset (exposition-only member function\*) |
| ****advance-bwd**** | decrements the current position on given value (exposition-only member function\*) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator<operator>operator<=operator>=operator<=>(C++26) | compares the underlying iterators   (function) |
| operator+operator-(C++26) | performs iterator arithmetic   (function) |
| iter_move(C++26) | casts the result of dereferencing the underlying iterator to its associated rvalue reference type   (function) |
| iter_swap(C++26) | swaps the objects pointed to by two underlying iterators   (function) |

### Example

The preliminary version can be checked out on Compiler Explorer.

Run this code

```
#include <iostream>
#include <iterator>
#include <ranges>
 
int main()
{
    namespace views = std::views;
    static constexpr int p[]{1, 2, 3};
    static constexpr auto e = {4, 5};
    auto t = views::iota(6, 9);
    auto cat = views::concat(p, e, t);
    auto dog = views::concat(cat, cat);
    for (auto i{dog.begin()}; i != std::default_sentinel; ++i)
        std::cout << *i << ' ';
    std::cout << '\n';
}

```

Output:

```
1 2 3 4 5 6 7 8 1 2 3 4 5 6 7 8

```

### References

- C++26 standard (ISO/IEC 14882:2026):

:   - 26.7.18.3 Class template `concat_view::iterator` [range.concat.iterator]

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/concat_view/iterator&oldid=176905>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 October 2024, at 17:32.