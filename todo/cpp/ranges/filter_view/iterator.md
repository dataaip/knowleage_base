# std::ranges::filter_view<V,Pred>::**iterator**

From cppreference.com
< cpp‎ | ranges‎ | filter view
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

std::ranges::filter_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| filter_view::filter_view | | | | |
| filter_view::base | | | | |
| filter_view::pred | | | | |
| filter_view::begin | | | | |
| filter_view::end | | | | |
| Deduction guides | | | | |
| ****Iterator**** | | | | |
| filter_view::**iterator**::**iterator** | | | | |
| filter_view::**iterator**::base | | | | |
| filter_view::**iterator**::operator\*filter_view::**iterator**::operator-> | | | | |
| filter_view::**iterator**::operator++ filter_view::**iterator**::operator++(int) | | | | |
| filter_view::**iterator**::operator-- filter_view::**iterator**::operator--(int) | | | | |
| operator==(filter_view::**iterator**) | | | | |
| iter_move(filter_view::**iterator**) | | | | |
| iter_swap(filter_view::**iterator**) | | | | |
| Sentinel | | | | |
| filter_view::**sentinel**::**sentinel** | | | | |
| filter_view::**sentinel**::base | | | | |
| operator==(filter_view::**iterator**, filter_view::**sentinel**) | | | | |

|  |  |  |
| --- | --- | --- |
| class /\*iterator\*/; |  | (since C++20)  (exposition only\*) |
|  |  |  |

The return type of filter_view::begin.

This is a `bidirectional_iterator` if V models `bidirectional_range`, a `forward_iterator` if V models `forward_range`, and `input_iterator` otherwise.

Modification of the element denoted by this iterator is permitted, but results in undefined behavior if the resulting value does not satisfy the filter's predicate.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `iterator_concept` | - std::bidirectional_iterator_tag, if V models `bidirectional_range`, - std::forward_iterator_tag, if V models `forward_iterator`, - std::input_iterator_tag otherwise. |
| `iterator_category` (conditionally present) | Defined if and only if V models `forward_range`. Let C be the type std::iterator_traits<ranges::iterator_t<V>>::iterator_category.   - std::bidirectional_iterator_tag, if C models std::derived_from<std::bidirectional_iterator_tag>, - std::forward_iterator_tag, if C models std::derived_from<std::forward_iterator_tag>, - C otherwise. |
| `value_type` | ranges::range_value_t<V> |
| `difference_type` | ranges::range_difference_t<V> |

### Data members

|  |  |
| --- | --- |
| Member name | Definition |
| `current_` (private) | An iterator of type ranges::iterator_t<V> into the underlying `view`. (exposition-only member object\*) |
| `parent_` (private) | A pointer of type ranges::filter_view<V, Pred>\* to the parent `filter_view` object. (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs an iterator   (public member function) |
| base | returns the underlying iterator   (public member function) |
| operator\*operator-> | forwards to the underlying iterator   (public member function) |
| operator++operator++(int) | advances the iterator   (public member function) |
| operator--operator--(int) | decrements the iterator   (public member function) |

## std::ranges::filter_view::**iterator**::**iterator**

|  |  |  |
| --- | --- | --- |
| /\*iterator\*/()      requires std::default_initializable<ranges::iterator_t<V>> = default; | (1) | (since C++20) |
| constexpr /\*iterator\*/( filter_view& parent,                          ranges::iterator_t<V> current ); | (2) | (since C++20) |
|  |  |  |

1) Initializes `current_` and `parent_` with their default member initializers, which are = ranges::iterator_t<V>() and = nullptr respectively.2) Initializes `current_` with std::move(current) and `parent_` with std::addressof(parent).

## std::ranges::filter_view::**iterator**::base

|  |  |  |
| --- | --- | --- |
| constexpr const ranges::iterator_t<V>& base() const & noexcept; | (1) | (since C++20) |
| constexpr ranges::iterator_t<V> base() &&; | (2) | (since C++20) |
|  |  |  |

1) Equivalent to return current_;.2) Equivalent to return std::move(current_);.

## std::ranges::filter_view::**iterator**::operator\*,->

|  |  |  |
| --- | --- | --- |
| constexpr ranges::range_reference_t<V> operator\*() const; | (1) | (since C++20) |
| constexpr ranges::iterator_t<V> operator->() const      requires /\*has-arrow\*/<ranges::iterator_t<V>> && std::copyable<ranges::iterator_t<V>>; | (2) | (since C++20) |
|  |  |  |

1) Equivalent to return \*current_;.2) Equivalent to return current_;.  

For a type `I`, /\*has-arrow\*/<I> is modeled or satisfied, if and only if `I` models or satisfies `input_iterator` respectively, and either `I` is a pointer type or requires(I i){ i.operator->();} is true.

## std::ranges::filter_view::**iterator**::operator++

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator++(); | (1) | (since C++20) |
| constexpr void operator++( int ); | (2) | (since C++20) |
| constexpr /\*iterator\*/ operator++( int )      requires ranges::forward_range<V>; | (3) | (since C++20) |
|  |  |  |

1) Equivalent to  
current_ = ranges::find_if(std::move(++current_), ranges::end(parent_->base_),  
                           std::ref(\*parent_->pred_));  
return \*this;.2) Equivalent to ++\*this;.3) Equivalent to auto tmp = \*this; ++\*this; return tmp;.

## std::ranges::filter_view::**iterator**::operator--

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator--()      requires ranges::bidirectional_range<V>; | (1) | (since C++20) |
| constexpr /\*iterator\*/ operator--( int )      requires ranges::bidirectional_range<V>; | (2) | (since C++20) |
|  |  |  |

1) Equivalent to  
do  
    --current_;  
while (!std::invoke(\*parent_->pred_, \*current_));  
return \*this;.2) Equivalent to auto tmp = \*this; --\*this; return tmp;.

### Non-member functions

|  |  |
| --- | --- |
| operator==(C++20) | compares the underlying iterators   (function) |
| iter_move(C++20) | casts the result of dereferencing the underlying iterator to its associated rvalue reference type   (function) |
| iter_swap(C++20) | swaps the objects pointed to by two underlying iterators   (function) |

## operator==(std::ranges::filter_view::**iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr bool operator==( const /\*iterator\*/& x, const /\*iterator\*/& y )      requires std::equality_comparable<ranges::iterator_t<V>>; |  | (since C++20) |
|  |  |  |

Equivalent to return x.current_ == y.current_;.

The `!=` operator is synthesized from `operator==`.

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `std::ranges::filter_view::iterator` is an associated class of the arguments.

## iter_move(std::ranges::filter_view::**iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr ranges::range_rvalue_reference_t<V>  iter_move( const /\*iterator\*/& i ) noexcept(noexcept(ranges::iter_move(i.current_))); |  | (since C++20) |
|  |  |  |

Equivalent to return ranges::iter_move(i.current_);.

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `std::ranges::filter_view::iterator` is an associated class of the arguments.

## iter_swap(std::ranges::filter_view::**iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr void iter_swap( const /\*iterator\*/& x, const /\*iterator\*/& y )  noexcept(noexcept(ranges::iter_swap(x.current_, y.current_)))         requires std::indirectly_swappable<ranges::iterator_t<V>>; |  | (since C++20) |
|  |  |  |

Equivalent to ranges::iter_swap(x.current_, y.current_).

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `std::ranges::filter_view::iterator` is an associated class of the arguments.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P2259R1 | C++20 | member type `iterator_category` was always defined | defined only if `V` is a `forward_range` |
| LWG 3533 | C++20 | the const& overload of `base` copied the underlying iterator | returns a reference to it |
| LWG 3593 | C++20 | the const& overload of `base` might not be noexcept | made noexcept |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/filter_view/iterator&oldid=173486>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 July 2024, at 01:04.