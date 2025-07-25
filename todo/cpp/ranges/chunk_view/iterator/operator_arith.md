# std::ranges::chunk_view<V>::**iterator**<Const>::operator++,--,+=,-=

From cppreference.com
< cpp‎ | ranges‎ | chunk view‎ | iterator
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

std::ranges::chunk_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| chunk_view::chunk_view | | | | |
| chunk_view::base | | | | |
| chunk_view::begin | | | | |
| chunk_view::end | | | | |
| chunk_view::size | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Classes for `input_range`s | | | | | | Deduction guides | | | | | | **outer-iterator** | | | | | | chunk_view::**outer-iterator**::**outer-iterator** | | | | | | chunk_view::**outer-iterator**::operator= | | | | | | chunk_view::**outer-iterator**::operator\* | | | | | | chunk_view::**outer-iterator**::operator++ chunk_view::**outer-iterator**::operator++(int) | | | | | | operator==(chunk_view::**outer-iterator**) | | | | | | operator-(chunk_view::**outer-iterator**) | | | | | | **outer-iterator**::value_type | | | | | | chunk_view::**outer-iterator**::value_type::value_type | | | | | | chunk_view::**outer-iterator**::value_type::begin | | | | | | chunk_view::**outer-iterator**::value_type::end | | | | | | chunk_view::**outer-iterator**::value_type::size | | | | | | **inner-iterator** | | | | | | chunk_view::**inner-iterator**::**inner-iterator** | | | | | | chunk_view::**inner-iterator**::operator= | | | | | | chunk_view::**inner-iterator**::base | | | | | | chunk_view::**inner-iterator**::operator\* | | | | | | chunk_view::**inner-iterator**::operator++ chunk_view::**inner-iterator**::operator++(int) | | | | | | operator==(chunk_view::**inner-iterator**) | | | | | | operator-(chunk_view::**inner-iterator**) | | | | | | iter_move(chunk_view::**inner-iterator**) | | | | | | iter_swap(chunk_view::**inner-iterator**) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template for `forward_range`s | | | | | | **iterator** | | | | | | chunk_view::**iterator**::**iterator** | | | | | | chunk_view::**iterator**::base | | | | | | chunk_view::**iterator**::operator\* | | | | | | [chunk_view::**iterator**::operator[]](operator_at.html "cpp/ranges/chunk view/iterator/operator at") | | | | | | ****chunk_view::**iterator**::operator++ chunk_view::**iterator**::operator++(int) chunk_view::**iterator**::operator-- chunk_view::**iterator**::operator--(int) chunk_view::**iterator**::operator+= chunk_view::**iterator**::operator-=**** | | | | | | operator==(chunk_view::**iterator**) operator<(chunk_view::**iterator**) operator>(chunk_view::**iterator**) operator<=(chunk_view::**iterator**) operator>=(chunk_view::**iterator**) operator<=>(chunk_view::**iterator**) | | | | | | operator+(chunk_view::**iterator**) operator-(chunk_view::**iterator**) | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator++(); | (1) | (since C++23) |
| constexpr /\*iterator\*/ operator++( int ); | (2) | (since C++23) |
| constexpr /\*iterator\*/& operator--()      requires ranges::bidirectional_range<Base>; | (3) | (since C++23) |
| constexpr /\*iterator\*/ operator--( int )      requires ranges::bidirectional_range<Base>; | (4) | (since C++23) |
| constexpr /\*iterator\*/& operator+=( difference_type x )      requires ranges::random_access_range<Base>; | (5) | (since C++23) |
| constexpr /\*iterator\*/& operator-=( difference_type x )      requires ranges::random_access_range<Base>; | (6) | (since C++23) |
|  |  |  |

Advances or decrements the iterator.

Let `current_`, `end_`, and `n_` be the underlying data members of `chunk_view::iterator`.

1) Equivalent to:

```
missing_ = ranges::advance(current_, n_, end_);
return *this;

```

Before the invocation the expression current_ != end_ must be true, otherwise the behavior is undefined.2) Equivalent to: auto tmp = \*this; ++\*this; return tmp;.3) Equivalent to:

```
ranges::advance(current_, missing_ - n_);
missing_ = 0;
return *this;

```

4) Equivalent to: auto tmp = \*this; --\*this; return tmp;.5) Equivalent to:

```
if (x > 0)
{
    ranges::advance(current_, n_ * (x - 1));
    missing_ = ranges::advance(current_, n_, end_);
}
else if (x < 0)
{
    ranges::advance(current_, n_ * x + missing_);
    missing_ = 0;
}
return *this;

```

If x is positive, then before the invocation the expression ranges::distance(current_, end_) > n_ \* (x - 1) must be true (i.e., informally, the requested chunk should be "inside" the underlying sequence). If x is negative, this precondition is always met.6) Equivalent to: return \*this += -x;.

### Parameters

|  |  |  |
| --- | --- | --- |
| x | - | a position relative to current location |

### Return value

1,3,5,6) \*this2,4) a copy of \*this that was made before the change

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| operator+operator-(C++23) | performs iterator arithmetic   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/chunk_view/iterator/operator_arith&oldid=151621>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 May 2023, at 10:37.