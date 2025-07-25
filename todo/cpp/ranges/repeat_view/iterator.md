# std::ranges::repeat_view<W, Bound>::**iterator**

From cppreference.com
< cpp‎ | ranges‎ | repeat view
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

std::ranges::repeat_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| repeat_view::repeat_view | | | | |
| repeat_view::begin | | | | |
| repeat_view::end | | | | |
| repeat_view::size | | | | |
| Deduction guides | | | | |
| ****Iterator**** | | | | |
| Member functions | | | | |
| repeat_view::**iterator**::**iterator** | | | | |
| repeat_view::**iterator**::operator\* | | | | |
| [repeat_view::**iterator**::operator[]](iterator.html#Member_functions "cpp/ranges/repeat view/iterator") | | | | |
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
| struct /\*iterator\*/; |  | (exposition only\*) |
|  |  |  |

ranges::repeat_view<W, Bound>::`iterator` is the type of the iterators returned by `begin()` and `end()` of ranges::repeat_view<W, Bound>.

### Nested types

|  |  |
| --- | --- |
| Exposition-only types | |
| Type | Definition |
| `index-type` | std::conditional_t<std::same_as<Bound, std::unreachable_sentinel_t>, std::ptrdiff_t, Bound> (exposition-only member type\*) |
| Iterator property types | |
| Type | Definition |
| `iterator_concept` | std::random_access_iterator_tag |
| `iterator_category` | std::random_access_iterator_tag |
| `value_type` | `W` |
| `difference_type` | std::conditional_t<**is-signed-integer-like** ﻿<`index-type` ﻿>, `index-type` ﻿,**iota-diff-t** ﻿<`index-type` ﻿>> |

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| const W\* `value_` | a pointer to the value to repeat (exposition-only member object\*) |
| `index-type` `current_` | the current position (exposition-only member object\*) |

### Member functions

## std::ranges::repeat_view::**iterator**::**iterator**

|  |  |  |
| --- | --- | --- |
| /\*iterator\*/() = default; | (1) | (since C++23) |
| constexpr explicit /\*iterator\*/      ( const W\* value, /\*index-type\*/ b = /\*index-type\*/() ); | (2) | (since C++23)  (exposition only\*) |
|  |  |  |

Constructs an iterator. Overload (2) is called by `begin()` and `end()` of `ranges::repeat_view`.

1) Initializes `value_` with nullptr and value-initializes `current_` ﻿.2) Initializes `value_` with value and `current_` with b. If `Bound` is not std::unreachable_sentinel_t and b is negative, the behavior is undefined.

## std::ranges::repeat_view::**iterator**::operator\*

|  |  |  |
| --- | --- | --- |
| constexpr const W& operator\*() const noexcept; |  | (since C++23) |
|  |  |  |

Returns \*`value_`.

## std::ranges::repeat_view::**iterator**::operator[]

|  |  |  |
| --- | --- | --- |
| constexpr const W& operator[]( difference_type n ) const noexcept; |  | (since C++23) |
|  |  |  |

Returns \*(\*this + n).

## std::ranges::repeat_view::**iterator**::operator++

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator++(); | (1) | (since C++23) |
| constexpr void operator++(int); | (2) | (since C++23) |
|  |  |  |

1) Equivalent to ++`current_` ﻿; return \*this;.2) Equivalent to auto tmp = \*this; ++\*this; return tmp;.

## std::ranges::repeat_view::**iterator**::operator--

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator--(); | (1) | (since C++23) |
| constexpr /\*iterator\*/ operator--(int); | (2) | (since C++23) |
|  |  |  |

1) Equivalent to --`current_` ﻿; return \*this;. If `Bound` is not std::unreachable_sentinel_t and `current_` is non-positive, the behavior is undefined.2) Equivalent to auto tmp = \*this; --\*this; return tmp;.

## std::ranges::repeat_view::**iterator**::operator+=

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator+=( difference_type n ); |  | (since C++23) |
|  |  |  |

Equivalent to `current_`+= n; return \*this;.

If `Bound` is not std::unreachable_sentinel_t and `current_`+ n is negative, the behavior is undefined.

## std::ranges::repeat_view::**iterator**::operator-=

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator-=( difference_type n ); |  | (since C++23) |
|  |  |  |

Equivalent to `current_`-= n; return \*this;.

If `Bound` is not std::unreachable_sentinel_t and `current_`- n is negative, the behavior is undefined.

### Non-member functions

## operator==, <=>(std::ranges::repeat_view::**iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr bool operator==      ( const /\*iterator\*/& x, const /\*iterator\*/& y ); | (1) | (since C++23) |
| friend constexpr auto operator<=>      ( const /\*iterator\*/& x, const /\*iterator\*/& y ); | (2) | (since C++23) |
|  |  |  |

1) Returns x.`current_`== y.`current_`.2) Returns x.`current_`<=> y.`current_`.

The `!=` operator is synthesized from `operator==`.

These functions are not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `iterator` is an associated class of the arguments.

## operator+(std::ranges::repeat_view::**iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr /\*iterator\*/ operator+      ( /\*iterator\*/ i, difference_type n ); | (1) | (since C++23) |
| friend constexpr /\*iterator\*/ operator+      ( difference_type n, /\*iterator\*/ i ); | (2) | (since C++23) |
|  |  |  |

Equivalent to i += n; return i;.

These functions are not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `iterator` is an associated class of the arguments.

## operator-(std::ranges::repeat_view::**iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr /\*iterator\*/ operator-      ( /\*iterator\*/ i, difference_type n ); | (1) | (since C++23) |
| friend constexpr difference_type operator-      ( const /\*iterator\*/& x, const /\*iterator\*/& y ); | (2) | (since C++23) |
|  |  |  |

1) Equivalent to i -= n; return i;.2) Returns static_cast<`difference_type`>(x.`current_` ﻿) -  
static_cast<`difference_type`>(y.`current_` ﻿).

These functions are not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `iterator` is an associated class of the arguments.

### Notes

`iterator` is always `random_access_iterator`.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/repeat_view/iterator&oldid=176949>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 October 2024, at 18:15.