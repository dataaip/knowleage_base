# std::ranges::transform_view<V,F>::**iterator**

From cppreference.com
< cpp‎ | ranges‎ | transform view
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

std::ranges::transform_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| transform_view::transform_view | | | | |
| transform_view::base | | | | |
| transform_view::begin | | | | |
| transform_view::end | | | | |
| transform_view::size | | | | |
| Deduction guides | | | | |
| ****Iterator**** | | | | |
| transform_view::**iterator**::**iterator** | | | | |
| transform_view::**iterator**::base | | | | |
| transform_view::**iterator**::operator\* | | | | |
| [transform_view::**iterator**::operator[]](iterator/operator_at.html "cpp/ranges/transform view/iterator/operator at") | | | | |
| transform_view::**iterator**::operator++ transform_view::**iterator**::operator++(int) transform_view::**iterator**::operator-- transform_view::**iterator**::operator--(int) transform_view::**iterator**::operator+= transform_view::**iterator**::operator-= | | | | |
| operator==(transform_view::**iterator**) operator<(transform_view::**iterator**) operator>(transform_view::**iterator**) operator<=(transform_view::**iterator**) operator>=(transform_view::**iterator**) operator<=>(transform_view::**iterator**) | | | | |
| operator+(transform_view::**iterator**) operator-(transform_view::**iterator**) | | | | |
| iter_move(transform_view::**iterator**) | | | | |
| Sentinel | | | | |
| transform_view::**sentinel**::**sentinel** | | | | |
| transform_view::**sentinel**::base | | | | |
| operator==(transform_view::**iterator**,transform_view::**sentinel**) | | | | |
| operator-(transform_view::**iterator**,transform_view::**sentinel**) | | | | |

|  |  |  |
| --- | --- | --- |
| template< bool Const >  class /\*iterator\*/ |  | (since C++20)  (exposition only\*) |
|  |  |  |

The return type of `transform_view::begin`, and of `transform_view::end` when the underlying view is a `common_range`.

The type /\*iterator\*/<true> is returned by the const-qualified overloads. The type /\*iterator\*/<false> is returned by the non-const-qualified overloads.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `Parent` (private) | `maybe-const` ﻿<Const, ranges::transform_view<V, F>> (exposition-only member type\*) |
| `Base` (private) | `maybe-const` ﻿<Const, V> (exposition-only member type\*) |
| `iterator_concept` | - std::random_access_iterator_tag, if `Base` models `random_access_range`, - std::bidirectional_iterator_tag, if `Base` models `bidirectional_range`, - std::forward_iterator_tag, if `Base` models `forward_range`, - std::input_iterator_tag otherwise. |
| `iterator_category` (present only if `Base` models `forward_range`) | Let `MCF` be `maybe-const` ﻿<Const, F>.  - std::input_iterator_tag, if std::invoke_result_t<MCF&, ranges::range_reference_t<Base>> is not a reference.   Otherwise, let `C` be std::iterator_traits<ranges::iterator_t<Base>>::iterator_category.   - std::random_access_iterator_tag, if `C` is std::contiguous_iterator_tag; - `C`, otherwise. |
| `value_type` | std::remove_cvref_t<std::invoke_result_t<MCF&, ranges::range_reference_t<Base>>>, where `MCF` denotes `maybe-const` ﻿<Const, F> |
| `difference_type` | ranges::range_difference_t<Base> |

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| `current_` (private) | An iterator into (possibly const-qualified) `V`. (exposition-only member object\*) |
| `parent_` (private) | A pointer to parent `transform_view`. (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs an iterator   (public member function) |
| base | returns the underlying iterator   (public member function) |
| operator\* | accesses the transformed element   (public member function) |
| [operator[]](iterator/operator_at.html "cpp/ranges/transform view/iterator/operator at") | accesses an element by index   (public member function) |
| operator++operator++(int)operator--operator--(int)operator+=operator-= | advances or decrements the underlying iterator   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator<operator>operator<=operator>=operator<=>(C++20) | compares the underlying iterators   (function) |
| operator+operator-(C++20) | performs iterator arithmetic   (function) |
| iter_move(C++20) | obtains an rvalue reference to the transformed element   (function) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P2259R1 | C++20 | member `iterator_category` is always defined | defined only if `Base` models `forward_range` |
| LWG 3555 | C++20 | the definition of `iterator_concept` ignores const | made to consider |
| LWG 3798 | C++20 | `iterator_category` is input-only if transformation result is rvalue reference | may have a stronger category |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/transform_view/iterator&oldid=175926>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 September 2024, at 17:53.