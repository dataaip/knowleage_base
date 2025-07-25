# std::ranges::adjacent_transform_view<V,F,N>::**iterator**

From cppreference.com
< cpp‎ | ranges‎ | adjacent transform view
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

std::ranges::adjacent_transform_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| adjacent_transform_view::adjacent_transform_view | | | | |
| adjacent_transform_view::begin | | | | |
| adjacent_transform_view::end | | | | |
| adjacent_transform_view::size | | | | |
| ****Iterator**** | | | | |
| Member functions | | | | |
| adjacent_transform_view::**iterator**::**iterator** | | | | |
| adjacent_transform_view::**iterator**::operator\* | | | | |
| [adjacent_transform_view::**iterator**::operator[]](iterator/operator_at.html "cpp/ranges/adjacent transform view/iterator/operator at") | | | | |
| adjacent_transform_view::**iterator**::operator++ adjacent_transform_view::**iterator**::operator++(int) adjacent_transform_view::**iterator**::operator-- adjacent_transform_view::**iterator**::operator--(int) adjacent_transform_view::**iterator**::operator+= adjacent_transform_view::**iterator**::operator-= | | | | |
| Non-member functions | | | | |
| operator==(adjacent_transform_view::**iterator**) operator<(adjacent_transform_view::**iterator**) operator>(adjacent_transform_view::**iterator**) operator<=(adjacent_transform_view::**iterator**) operator>=(adjacent_transform_view::**iterator**) operator<=>(adjacent_transform_view::**iterator**) | | | | |
| operator+(adjacent_transform_view::**iterator**) operator-(adjacent_transform_view::**iterator**) | | | | |
| Sentinel | | | | |
| Member functions | | | | |
| adjacent_transform_view::**sentinel**::**sentinel** | | | | |
| Non-member functions | | | | |
| operator==(adjacent_transform_view::**iterator**,adjacent_transform_view::**sentinel**) | | | | |
| operator-(adjacent_transform_view::**iterator**,adjacent_transform_view::**sentinel**) | | | | |

|  |  |  |
| --- | --- | --- |
| template< bool Const >  class /\*iterator\*/ |  | (since C++23)  (exposition only\*) |
|  |  |  |

The return type of `adjacent_transform_view::begin`, and of `adjacent_transform_view::end` when the underlying view `V` is a `common_range`.

The type /\*iterator\*/<true> is returned by the const-qualified overloads. The type /\*iterator\*/<false> is returned by the non-const-qualified overloads.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `Parent` (private) | const ranges::adjacent_transform_view, if `Const` is true. Otherwise, ranges::adjacent_transform_view. (exposition-only member type\*) |
| `Base` (private) | const V, if `Const` is true. Otherwise, V. (exposition-only member type\*) |
| `iterator_category` | - std::input_iterator_tag, if   std::invoke_result_t</\*maybe-const\*/<Const, F>&,                      /\*REPEAT\*/(ranges::range_reference_t<Base>, N)...>  is not a reference. Otherwise,   - let `C` denote the type std::iterator_traits<iterator_t<Base>>::iterator_category.   - std::random_access_iterator_tag, if  std::derived_from<C, std::random_access_iterator_tag> is true. Otherwise,   - std::bidirectional_iterator_tag, if  std::derived_from<C, std::bidirectional_iterator_tag> is true. Otherwise,   - std::forward_iterator_tag, if  std::derived_from<C, std::forward_iterator_tag> is true. Otherwise,   - std::input_iterator_tag. |
| `iterator_concept` | typename /\*inner-iterator\*/<Const>::iterator_concept;. |
| `value_type` | std::remove_cvref_t<std::invoke_result_t</\*maybe-const\*/<Const, F>&,                     /\*REPEAT\*/(ranges::range_reference_t<Base>, N)...>>; |
| `difference_type` | ranges::range_difference_t<Base> |

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| `parent_` (private) | A pointer of type `Parent*`. (exposition-only member object\*) |
| `inner_` (private) | An iterator of type `inner_iterator`. (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs an iterator   (public member function) |
| operator\* | accesses the element   (public member function) |
| [operator[]](iterator/operator_at.html "cpp/ranges/adjacent transform view/iterator/operator at") | accesses an element by index   (public member function) |
| operator++operator++(int)operator--operator--(int)operator+=operator-= | advances or decrements the underlying iterators   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator<operator>operator<=operator>=operator<=>(C++23) | compares the underlying iterators   (function) |
| operator+operator-(C++23) | performs iterator arithmetic   (function) |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 26.7.27.3 Class template adjacent_transform_view::**iterator** [range.adjacent_transform.iterator]

### See also

|  |
| --- |
|  |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/adjacent_transform_view/iterator&oldid=172651>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 June 2024, at 20:46.