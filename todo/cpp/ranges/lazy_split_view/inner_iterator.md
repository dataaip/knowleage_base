# std::ranges::lazy_split_view<V, Pattern>::**inner_iterator**

From cppreference.com
< cpp‎ | ranges‎ | lazy split view
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

std::ranges::lazy_split_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| lazy_split_view::lazy_split_view | | | | |
| lazy_split_view::base | | | | |
| lazy_split_view::begin | | | | |
| lazy_split_view::end | | | | |
| Nested classes | | | | |
| lazy_split_view::**outer_iterator** | | | | |
| lazy_split_view::**outer_iterator**::value_type | | | | |
| ****lazy_split_view::**inner_iterator****** | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| template< bool Const >  struct /\*inner_iterator\*/; |  | (since C++20)  (exposition only\*) |
|  |  |  |

The return type of `lazy_split_view::``outer_iterator`::value_type::begin().

`Const` matches the template argument of `outer_iterator`.

### Member types

|  |  |
| --- | --- |
| Member | Definition |
| `Base` | `maybe-const` ﻿<Const, V> (exposition-only member type\*) |
| `iterator_concept` | - `outer_iterator`<Const>::iterator_concept, that is std::forward_iterator_tag, if `Base` models `forward_range`. - std::input_iterator_tag, otherwise. |
| `iterator_category` (conditionally present) | Present only if `Base` models `forward_range`.   - std::forward_iterator_tag if std::iterator_traits<ranges::iterator_t<Base>>::iterator_category models std::derived_from<std::forward_iterator_tag>. - std::iterator_traits<ranges::iterator_t<Base>>::iterator_category otherwise. |
| `value_type` | ranges::range_value_t<Base> |
| `difference_type` | ranges::range_difference_t<Base> |

### Data members

|  |  |
| --- | --- |
| Member | Description |
| `outer_iterator`<Const> `i_` (private) | an iterator into the underlying `view` of the parent object `lazy_split_view` (exposition-only member object\*) |
| bool `incremented_` (private) | a flag that indicates whether the operator++ was invoked on this object at least once (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor)(C++20) | constructs an iterator   (public member function) |
| base(C++20) | returns the underlying iterator   (public member function) |
| operator\*(C++20) | returns the current element   (public member function) |
| operator++operator++(int)(C++20) | advances the iterator   (public member function) |

### Member functions

## std::ranges::lazy_split_view::**inner_iterator**::**inner_iterator**

|  |  |  |
| --- | --- | --- |
| /\*inner_iterator\*/() = default; | (1) | (since C++20) |
| constexpr explicit /\*inner_iterator\*/( /\*outer_iterator\*/<Const> i ); | (2) | (since C++20) |
|  |  |  |

1) Value initializes data member `i_` via its default member initializer (= /\*outer_iterator\*/<Const>()).2) Initializes `i_` with std::move(i).

The data member `incremented_` is initialized with its default member initializer to false.

## std::ranges::lazy_split_view::**inner_iterator**::**base**

|  |  |  |
| --- | --- | --- |
| constexpr const ranges::iterator_t<Base>& base() const & noexcept; | (1) | (since C++20) |
| constexpr ranges::iterator_t<Base> base() &&      requires ranges::forward_range<V>; | (2) | (since C++20) |
|  |  |  |

Returns a copy of the underlying iterator.

1) Copy constructs the result from the underlying iterator. Equivalent to return i_./\*cur\*/();.2) Move constructs the result from the underlying iterator. Equivalent to return std::move(i_./\*cur\*/());.

## std::ranges::lazy_split_view::**inner_iterator**::operator\*

|  |  |  |
| --- | --- | --- |
| constexpr decltype(auto) operator\*() const; |  | (since C++20) |
|  |  |  |

Returns the element the underlying iterator points to.

Equivalent to return \*i_./\*cur\*/();.

## std::ranges::lazy_split_view::**inner_iterator**::operator++

|  |  |  |
| --- | --- | --- |
| constexpr /\*inner_iterator\*/& operator++(); | (1) | (since C++20) |
| constexpr decltype(auto) operator++(int); | (2) | (since C++20) |
|  |  |  |

1) The function body is equivalent to  
incremented_ = true;  

if constexpr (!ranges::forward_range<Base>)  
{  
    if constexpr (Pattern::size() == 0)  
        return \*this;  
}  
++i_./\*cur\*/();

return \*this;2) Equivalent to  
if constexpr (ranges::forward_range<Base>)  

{  
    auto tmp = \*this;  
    ++\*this;  
    return tmp;  
}  
else  
    ++\*this; // no return statement

### Non-member functions

|  |  |
| --- | --- |
| operator==(C++20) | compares the iterators or the iterator and std::default_sentinel   (function) |
| iter_move(C++20) | casts the result of dereferencing the underlying iterator to its associated rvalue reference type   (function) |
| iter_swap(C++20) | swaps the objects pointed to by two underlying iterators   (function) |

## operator==(std::ranges::split_view::**inner_iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr bool operator==( const /\*inner_iterator\*/& x,  const /\*inner_iterator\*/& y )       requires forward_range<Base>; | (1) | (since C++20) |
| friend constexpr bool operator==( const /\*inner_iterator\*/& x,                                    std::default_sentinel_t ); | (2) | (since C++20) |
|  |  |  |

1) Equivalent to return x.i_./\*cur\*/() == y.i_./\*cur\*/();.2) The function body is equivalent to

```
auto [pcur, pend] = ranges::subrange{x.i_.parent_->pattern_};
auto end = ranges::end(x.i_.parent_->base_);
if constexpr (/*tiny_range*/<Pattern>)
{
    const auto& cur = x.i_./*cur*/();
    if (cur == end)
        return true;
    if (pcur == pend)
        return x.incremented_;
    return *cur == *pcur;
}
else
{
    auto cur = x.i_./*cur*/();
    if (cur == end)
        return true;
    if (pcur == pend)
        return x.incremented_;
    do
    {
        if (*cur != *pcur)
            return false;
        if (++pcur == pend)
            return true;
    }
    while (++cur != end);
    return false;
}

```

The `!=` operator is synthesized from `operator==`.

These functions are not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `std::ranges::split_view::inner_iterator` is an associated class of the arguments.

## iter_move(std::ranges::split_view::**inner_iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr decltype(auto) iter_move( const /\*inner_iterator\*/& i )      noexcept(noexcept(ranges::iter_move(i.i_./\*cur\*/()))); |  | (since C++20) |
|  |  |  |

Equivalent to return ranges::iter_move(i.i_./\*cur\*/());.

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `std::ranges::split_view::inner_iterator` is an associated class of the arguments.

## iter_swap(std::ranges::split_view::**inner_iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr void iter_swap( const /\*inner_iterator\*/& x,  const /\*inner_iterator\*/& y )      noexcept(noexcept(ranges::iter_swap(x.i_.current, y.i_.current)))     requires std::indirectly_swappable<ranges::iterator_t<Base>>; |  | (since C++20) |
|  |  |  |

Equivalent to ranges::iter_swap(x.i_./\*cur\*/(), y.i_./\*cur\*/()).

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `std::ranges::split_view::inner_iterator` is an associated class of the arguments.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3591 | C++20 | the && overload of `base` might invalidate outer iterators | constraints added |
| LWG 3593 | C++20 | the const& overload of `base` returns a reference but might not be noexcept | made noexcept |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/lazy_split_view/inner_iterator&oldid=179927>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 January 2025, at 15:34.