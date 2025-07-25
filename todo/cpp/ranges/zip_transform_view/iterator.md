# std::ranges::zip_transform_view<F,Views...>::**iterator**

From cppreference.com
< cpp‎ | ranges‎ | zip transform view
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

std::ranges::zip_transform_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| zip_transform_view::zip_transform_view | | | | |
| zip_transform_view::begin | | | | |
| zip_transform_view::end | | | | |
| zip_transform_view::size | | | | |
| Deduction guides | | | | |
| ****Iterator**** | | | | |
| Member functions | | | | |
| zip_transform_view::**iterator**::**iterator** | | | | |
| zip_transform_view::**iterator**::operator\* | | | | |
| [zip_transform_view::**iterator**::operator[]](iterator/operator_at.html "cpp/ranges/zip transform view/iterator/operator at") | | | | |
| zip_transform_view::**iterator**::operator++ zip_transform_view::**iterator**::operator++(int) zip_transform_view::**iterator**::operator-- zip_transform_view::**iterator**::operator--(int) zip_transform_view::**iterator**::operator+= zip_transform_view::**iterator**::operator-= | | | | |
| Non-member functions | | | | |
| operator==(zip_transform_view::**iterator**) operator<=>(zip_transform_view::**iterator**) | | | | |
| operator+(zip_transform_view::**iterator**) operator-(zip_transform_view::**iterator**) | | | | |
| Sentinel | | | | |
| Member functions | | | | |
| zip_transform_view::**sentinel**::**sentinel** | | | | |
| Non-member functions | | | | |
| operator==(zip_transform_view::**sentinel**) | | | | |
| operator-(zip_transform_view::**sentinel**) | | | | |

|  |  |  |
| --- | --- | --- |
| template< bool Const >  class /\*iterator\*/; |  | (since C++23)  (exposition only\*) |
|  |  |  |

The iterator type of a possibly const-qualified `zip_transform_view`, returned by `zip_transform_view::begin` and in certain cases by `zip_transform_view::end`.

The type /\*iterator\*/<true> or /\*iterator\*/<false> treats the underlying views as const-qualified or non-const-qualified respectively.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `Parent` (private) | `zip_transform_view` if Const is false, const zip_transform_view otherwise. (exposition-only member type\*) |
| `Base` (private) | `InnerView` if Const is false, const InnerView otherwise. (exposition-only member type\*) |
| `iterator_category` (conditionally present) | Let /\*maybe-const\*/<Const, F>& denote const F& if Const is true, F& otherwise.  Let /\*maybe-const\*/<Const, Views> denote const Views if Const is true, Views otherwise.  Let /\*POT\*/ denote the pack of types std::iterator_traits<std::iterator_t<     /\*maybe-const\*/<Const, Views>>>::iterator_category...  If /\*Base\*/ models `forward_range`, then `iterator_category` denotes:   - std::input_iterator_tag, if std::invoke_result_t</\*maybe-const\*/<Const, F>&,     ranges::range_reference_t</\*maybe-const\*/<Const, Views>>...>   is not a reference.   - Otherwise,   - std::random_access_iterator_tag, if   (std::derived_from</\*POT\*/, std::random_access_iterator_tag> && ...) is true.   - Otherwise, std::bidirectional_iterator_tag, if   (std::derived_from</\*POT\*/, std::bidirectional_iterator_tag> && ...) is true.   - Otherwise, std::forward_iterator_tag, if   (std::derived_from</\*POT\*/, std::forward_iterator_tag> && ...) is true.   - Otherwise, std::input_iterator_tag.  Not present if /\*Base\*/ does not model `forward_range`. |
| `iterator_concept` | /\*ziperator\*/<Const>::iterator_concept |
| `value_type` | Let /\*RREF\*/ be ranges::range_reference_t<Views>...,  and /\*CRREF\*/ be ranges::range_reference_t<const Views>.... Then:   - std::remove_cvref_t<std::invoke_result_t<F&, /\*RREF\*/>> if Const is false, - std::remove_cvref_t<std::invoke_result_t<const F&, /\*CRREF\*/>> otherwise. |
| `difference_type` | range::range_difference_t</\*Base\*/> |

### Data members

|  |  |
| --- | --- |
| Member object | Definition |
| `parent_` (private) | A pointer `Parent*` to the parent object (exposition-only member object\*) |
| `inner_` (private) | An iterator of type `ziperator<Const>`. (exposition-only member type\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs an iterator   (public member function) |
| operator\* | obtains the result of applying the invocable object to the underlying pointed-to elements   (public member function) |
| [operator[]](iterator/operator_at.html "cpp/ranges/zip transform view/iterator/operator at") | obtains the result of applying the invocable object to the underlying elements at given offset   (public member function) |
| operator++operator++(int)operator--operator--(int)operator+=operator-= | advances or decrements the underlying iterator   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator<=>(C++23) | compares the underlying iterators   (function) |
| operator+operator-(C++23) | performs iterator arithmetic on underlying iterators   (function) |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/zip_transform_view/iterator&oldid=173490>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 July 2024, at 01:08.