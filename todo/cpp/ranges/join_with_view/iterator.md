# std::ranges::join_with_view<V,Pattern>::**iterator**

From cppreference.com
< cpp‎ | ranges‎ | join with view
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

std::ranges::join_with_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| join_with_view::join_with_view | | | | |
| join_with_view::base | | | | |
| join_with_view::begin | | | | |
| join_with_view::end | | | | |
| Deduction guides | | | | |
| ****Iterator**** | | | | |
| Member functions | | | | |
| join_with_view::**iterator**::**iterator** | | | | |
| join_with_view::**iterator**::operator\* | | | | |
| join_with_view::**iterator**::operator++ join_with_view::**iterator**::operator++(int) join_with_view::**iterator**::operator-- join_with_view::**iterator**::operator--(int) | | | | |
| Non-member functions | | | | |
| operator==(join_with_view::**iterator**)(C++23) | | | | |
| iter_move(join_with_view::**iterator**)(C++23) | | | | |
| iter_swap(join_with_view::**iterator**)(C++23) | | | | |
| Sentinel | | | | |
| join_with_view::**sentinel**::**sentinel** | | | | |
| operator==(join_with_view::**sentinel**)(C++23) | | | | |

|  |  |  |
| --- | --- | --- |
| template< bool Const >  class /\*iterator\*/ |  | (exposition only\*) |
|  |  |  |

ranges::join_with_view<V, Pattern>::`iterator` is the type of the iterators returned by `begin()` and `end()` of ranges::join_with_view<V, Pattern>.

The state of an iterator of this class is managed as if there are two nested iterators:

- an **outer iterator** into the parent range \*`parent_`

:   - If `Base` models `forward_range`, it is `outer_it_`.
    - Otherwise, it is `parent_` ﻿->`outer_it_`.

- an **inner iterator** `inner_it_` into the pattern range `parent_` ﻿->`pattern_` or into a child range of the parent range

This iterator class has the invariant that the inner iterator is always dereferenceable unless the outer iterator is not dereferenceable. When an iterator is constructed, incremented or decremented, its outer iterator might be adjusted to hold the invariant.

### Template parameters

|  |  |  |
| --- | --- | --- |
| Const | - | whether the iterator is a constant iterator |

### Nested types

|  |  |
| --- | --- |
| Exposition-only types | |
| Type | Definition |
| `Parent` | `maybe-const` ﻿<Const, ranges::join_with_view<V, Pattern>> (exposition-only member type\*) |
| `Base` | `maybe-const` ﻿<Const, V> (exposition-only member type\*) |
| `InnerBase` | ranges::range_reference_t<`Base` ﻿> (exposition-only member type\*) |
| `PatternBase` | `maybe-const` ﻿<Const, Pattern> (exposition-only member type\*) |
| `OuterIter` | ranges::iterator_t<`Base` ﻿> (exposition-only member type\*) |
| `InnerIter` | ranges::iterator_t<`InnerBase` ﻿> (exposition-only member type\*) |
| `PatternIter` | ranges::iterator_t<`PatternBase` ﻿> (exposition-only member type\*) |
| Iterator property types | |
| Type | Definition |
| `iterator_concept` | an iterator tag, see below |
| `iterator_category` (conditionally present) | an iterator tag, see below |
| `value_type` | std::common_type_t<ranges::range_value_t<`InnerBase` ﻿>,  ranges::range_value_t<`PatternBase` ﻿>> |
| `difference_type` | std::common_type_t<ranges::range_difference_t<`Base` ﻿>,  ranges::range_difference_t<`InnerBase` ﻿>,  ranges::range_difference_t<`PatternBase` ﻿>> |

#### Determining the iterator concept

`iterator_concept` is defined as follows:

- If all following conditions are satisfied, `iterator_concept` denotes std::bidirectional_iterator_tag:
  - std::is_reference_v<`InnerBase` ﻿> is true.
  - `Base` models `bidirectional_range`.
  - `InnerBase` and `PatternBase` each model `common_range`.
- Otherwise, if all following conditions are satisfied, `iterator_concept` denotes std::forward_iterator_tag:
  - std::is_reference_v<`InnerBase` ﻿> is true.
  - `Base` and `InnerBase` each model `forward_range`.
- Otherwise, `iterator_concept` denotes std::input_iterator_tag.

#### Determining the iterator category

Given the following types:

- Let `OuterC` be std::iterator_traits<`OuterIter` ﻿>::iterator_category.
- Let `InnerC` be std::iterator_traits<`InnerIter` ﻿>::iterator_category.
- Let `PatternC` be std::iterator_traits<`PatternIter` ﻿>::iterator_category.

`iterator_category` is defined if and only if std::is_reference_v<`InnerBase` ﻿> is true, and `Base` and `InnerBase` each model `forward_range`. In this case, it is defined as follows:

- If std::is_reference_v<std::common_reference_t<ranges::range_reference_t<`InnerBase` ﻿>,  
  ranges::range_reference_t<`PatternBase` ﻿>> is false, `iterator_category` denotes std::input_iterator_tag.
- Otherwise, if all following conditions are satisfied, `iterator_category` denotes std::bidirectional_iterator_tag:
  - `OuterC`, `InnerC`, and `PatternC` each model std::derived_from<std::bidirectional_iterator_tag>.
  - `InnerBase` and `PatternBase` each model `common_range`.
- Otherwise, if `OuterC`, `InnerC`, and `PatternC` each model std::derived_from<std::forward_iterator_tag>, `iterator_category` denotes std::forward_iterator_tag.
- Otherwise, `iterator_category` denotes std::input_iterator_tag.

### Data members

|  |  |
| --- | --- |
| Member | Description |
| `Parent` ﻿\* `parent_` | the pointer to the parent `join_with_view` (exposition-only member object\*) |
| `OuterIter` `outer_it_`  (present only if `Base` models `forward_range`) | the outer iterator (exposition-only member object\*) |
| std::variant<`PatternIter` ﻿,`InnerIter` ﻿> `inner_it_` | the inner iterator (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs an iterator   (public member function) |
| operator\* | accesses the element   (public member function) |
| operator++operator++(int)operator--operator--(int) | advances or decrements the underlying iterator   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==(C++23) | compares the underlying iterators   (function) |
| iter_move(C++23) | casts the result of dereferencing the underlying iterator to its associated rvalue reference type   (function) |
| iter_swap(C++23) | swaps the objects pointed to by two underlying iterators   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/join_with_view/iterator&oldid=176927>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 October 2024, at 04:47.