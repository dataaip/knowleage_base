# std::ranges::iota_view<W, Bound>::**iterator**

From cppreference.com
< cpp‎ | ranges‎ | iota view
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

std::ranges::iota_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| iota_view::iota_view | | | | |
| iota_view::begin | | | | |
| iota_view::end | | | | |
| iota_view::empty | | | | |
| iota_view::size | | | | |
| Deduction guides | | | | |
| Nested classes | | | | |
| ******Iterator****** | | | | |
| ****Helper concepts**** | | | | |
| **decrementable** | | | | |
| **advanceable** | | | | |
| Member types | | | | |
| Member functions | | | | |
| iota_view::**iterator**::**iterator** | | | | |
| iota_view::**iterator**::operator\* | | | | |
| [iota_view::**iterator**::operator[]](iterator.html#Member_functions "cpp/ranges/iota view/iterator") | | | | |
| iota_view::**iterator**::operator++ iota_view::**iterator**::operator++(int) | | | | |
| iota_view::**iterator**::operator-- iota_view::**iterator**::operator--(int) | | | | |
| iota_view::**iterator**::operator+= | | | | |
| iota_view::**iterator**::operator-= | | | | |
| Non-member functions | | | | |
| operator==(iota_view::**iterator**) operator<(iota_view::**iterator**) operator>(iota_view::**iterator**) operator<=(iota_view::**iterator**) operator>=(iota_view::**iterator**) operator<=>(iota_view::**iterator**) | | | | |
| operator+(iota_view::**iterator**) | | | | |
| operator-(iota_view::**iterator**) | | | | |
| **Sentinel** | | | | |
| Member functions | | | | |
| iota_view::**sentinel**::**sentinel** | | | | |
| Non-member functions | | | | |
| operator==(iota_view::**iterator**,iota_view::**sentinel**) | | | | |
| operator-(iota_view::**iterator**,iota_view::**sentinel**) | | | | |

|  |  |  |
| --- | --- | --- |
| struct /\*iterator\*/; | (1) | (exposition only\*) |
| Helper alias templates |  |  |
| template< class I >  using /\*iota-diff-t\*/ = /\* see below \*/; | (2) | (exposition only\*) |
| Helper concepts |  |  |
| template< class I >  concept /\*decrementable\*/ =      std::incrementable<I> && requires(I i) {          { --i } -> std::same_as<I&>;          { i-- } -> std::same_as<I>; }; | (3) | (exposition only\*) |
| template< class I >  concept /\*advanceable\*/ =      /\*decrementable\*/<I> && std::totally_ordered<I> &&      requires(I i, const I j, const /\*iota-diff-t\*/<I> n) {          { i += n } -> std::same_as<I&>;          { i -= n } -> std::same_as<I&>;          I(j + n);          I(n + j);          I(j - n);          { j - j } -> std::convertible_to</\*iota-diff-t\*/<I>>; }; | (4) | (exposition only\*) |
|  |  |  |

1) ranges::iota_view<W, Bound>::`iterator` is the type of the iterators returned by `begin()` and `end()` of ranges::iota_view<W, Bound>.2) Calculates the difference type for both iterator types and integer-like types.

- If `I` is not an integral type, or if it is an integral type and sizeof(std::iter_difference_t<I>) is greater than sizeof(I), then /\*iota-diff-t\*/<I> is std::iter_difference_t<I>.
- Otherwise, /\*iota-diff-t\*/<I> is a signed integer type of width greater than the width of `I` if such a type exists.
- Otherwise, `I` is one of the widest integral types, and /\*iota-diff-t\*/<I> is an unspecified signed-integer-like type of width not less than the width of `I`. It is unspecified whether /\*iota-diff-t\*/<I> models `weakly_incrementable` in this case.
3) Specifies that a type is `incrementable`, and pre- and post- operator-- for the type have common meaning.4) Specifies that a type is both `decrementable` and `totally_ordered`, and operator+=, operator-=, operator+, and operator- among the type and its different type have common meaning.

/\*iterator\*/ models

- `random_access_iterator` if W models `advanceable` (4),
- `bidirectional_iterator` if W models `decrementable` (3),
- `forward_iterator` if W models `incrementable`, and
- `input_iterator` otherwise.

However, it only satisfies LegacyInputIterator if `W` models `incrementable`, and does not satisfy LegacyInputIterator otherwise.

### Semantic requirements

3) Type `I` models `decrementable` only if `I` satisfies `decrementable` and all concepts it subsumes are modeled, and given equal objects a and b of type `I`:

- If a and b are in the domain of both pre- and post- operator-- (i.e. they are decrementable), then the following are all true:
  - std::addressof(--a) == std::addressof(a),
  - bool(a-- == b),
  - bool(((void)a--, a) == --b),
  - bool(++(--a) == b).
- If a and b are in the domain of both pre- and post- operator++ (i.e. they are incrementable), then bool(--(++a) == b) is true.
4) Let `D` denote /\*iota-diff-t\*/<I>. Type `I` models `advanceable` only if `I` satisfies `advanceable` and all concepts it subsumes are modeled, and given

- objects a and b of type `I` and
- value n of type `D`,

such that b is reachable from a after n applications of ++a, all following conditions are satisfied:

- (a += n) is equal to b.
- std::addressof(a += n) is equal to std::addressof(a).
- I(a + n) is equal to (a += n).
- For any two positive values x and y of type `D`, if I(a + D(x + y)) is well-defined, then I(a + D(x + y)) is equal to I(I(a + x) + y).
- I(a + D(0)) is equal to a.
- If I(a + D(n - 1)) is well-defined, then I(a + n) is equal to [](I c) { return ++c; }(I(a + D(n - 1))).
- (b += -n) is equal to a.
- (b -= n) is equal to a.
- std::addressof(b -= n) is equal to std::addressof(b).
- I(b - n) is equal to (b -= n).
- D(b - a) is equal to n.
- D(a - b) is equal to D(-n).
- bool(a <= b) is true.

### Nested types

|  |  |
| --- | --- |
| Type | Definition |
| `iterator_concept` | an iterator tag, see below |
| `iterator_category` (only present if `W` models `incrementable` and /\*iota-diff-t\*/<W> is an integral type) | std::input_iterator_tag |
| `value_type` | `W` |
| `difference_type` | /\*iota-diff-t\*/<W> |

#### Determining the iterator concept

`iterator_concept` is defined as follows:

- If `W` models `advanceable`, `iterator_concept` denotes std::random_access_iterator_tag.
- Otherwise, if `W` models `decrementable`, `iterator_concept` denotes std::bidirectional_iterator_tag.
- Otherwise, if `W` models `incrementable`, `iterator_concept` denotes std::forward_iterator_tag.
- Otherwise, `iterator_concept` denotes std::input_iterator_tag.

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| `W` `value_` | the current value (exposition-only member object\*) |

### Member functions

## std::ranges::iota_view::**iterator**::**iterator**

|  |  |  |
| --- | --- | --- |
| /\*iterator\*/() requires std::default_initializable<W> = default; | (1) | (since C++20) |
| constexpr explicit /\*iterator\*/( W value ); | (2) | (since C++20) |
|  |  |  |

1) Value initializes `value_`.2) Initializes `value_` with value.

## std::ranges::iota_view::**iterator**::operator\*

|  |  |  |
| --- | --- | --- |
| constexpr W operator\*() const      noexcept(std::is_nothrow_copy_constructible_v<W>); |  | (since C++20) |
|  |  |  |

Returns `value_`.

### Example

Run this code

```
#include <cassert>
#include <ranges>
 
int main()
{
    auto it{std::views::iota(6, 9).begin()};
    const int& r = *it; // binds with temporary
    assert(*it == 6 and r == 6);
    ++it;
    assert(*it == 7 and r == 6);
}

```

## std::ranges::iota_view::**iterator**::operator++

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator++(); | (1) | (since C++20) |
| constexpr void operator++(int); | (2) | (since C++20) |
| constexpr /\*iterator\*/ operator++(int) requires std::incrementable<W>; | (3) | (since C++20) |
|  |  |  |

1) Equivalent to ++`value_` ﻿; return \*this;.2) Equivalent to ++`value_` ﻿;.3) Equivalent to auto tmp = \*this; ++`value_` ﻿; return tmp;.

### Example

Run this code

```
#include <cassert>
#include <ranges>
 
int main()
{
    auto it{std::views::iota(8).begin()};
    assert(*it == 8);
    assert(*++it == 9);
    assert(*it++ == 9);
    assert(*it == 10);
}

```

## std::ranges::iota_view::**iterator**::operator--

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator--() requires /\*decrementable\*/<W>; | (1) | (since C++20) |
| constexpr /\*iterator\*/operator--(int) requires /\*decrementable\*/<W>; | (2) | (since C++20) |
|  |  |  |

1) Equivalent to --`value_` ﻿; return \*this;.2) Equivalent to auto tmp = \*this; --`value_` ﻿; return tmp;.

### Example

Run this code

```
#include <cassert>
#include <ranges>
 
int main()
{
    auto it{std::views::iota(8).begin()};
    assert(*it == 8);
    assert(*--it == 7);
    assert(*it-- == 7);
    assert(*it == 6);
}

```

## std::ranges::iota_view::**iterator**::operator+=

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator+=( difference_type n )      requires /\*advanceable\*/<W>; |  | (since C++20) |
|  |  |  |

Updates `value_` and returns \*this:

- If `W` is an unsigned-integer-like type:
  - If n is non-negative, performs `value_`+= static_cast<W>(n).
  - Otherwise, performs `value_`-= static_cast<W>(-n).
- Otherwise, performs `value_`+= n.

### Example

Run this code

```
#include <cassert>
#include <ranges>
 
int main()
{
    auto it{std::views::iota(5).begin()};
    assert(*it == 5);
    assert(*(it += 3) == 8);
}

```

## std::ranges::iota_view::**iterator**::operator-=

|  |  |  |
| --- | --- | --- |
| constexpr /\*iterator\*/& operator-=( difference_type n )      requires /\*advanceable\*/<W>; |  | (since C++20) |
|  |  |  |

Updates `value_` and returns \*this:

- If `W` is an unsigned-integer-like type:
  - If n is non-negative, performs `value_`-= static_cast<W>(n).
  - Otherwise, performs `value_`+= static_cast<W>(-n).
- Otherwise, performs `value_`-= n.

### Example

Run this code

```
#include <cassert>
#include <ranges>
 
int main()
{
    auto it{std::views::iota(6).begin()};
    assert(*it == 6);
    assert(*(it -= -3) == 9);
}

```

## std::ranges::iota_view::**iterator**::operator[]

|  |  |  |
| --- | --- | --- |
| constexpr W operator[]( difference_type n ) const      requires /\*advanceable\*/<W>; |  | (since C++20) |
|  |  |  |

Returns W(`value_`+ n).

### Example

Run this code

```
#include <cassert>
#include <ranges>
 
int main()
{
    auto it{std::views::iota(6).begin()};
    assert(*it == 6);
    assert(*(it + 3) == 9);
}

```

### Non-member functions

## operator==, <, >, <=, >=, <=>(std::ranges::iota_view::**iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr bool operator==  ( const /\*iterator\*/& x, const /\*iterator\*/& y )     requires std::equality_comparable<W>; | (1) | (since C++20) |
| friend constexpr bool operator<  ( const /\*iterator\*/& x, const /\*iterator\*/& y )     requires std::totally_ordered<W>; | (2) | (since C++20) |
| friend constexpr bool operator>  ( const /\*iterator\*/& x, const /\*iterator\*/& y )     requires std::totally_ordered<W>; | (3) | (since C++20) |
| friend constexpr bool operator<=  ( const /\*iterator\*/& x, const /\*iterator\*/& y )     requires std::totally_ordered<W>; | (4) | (since C++20) |
| friend constexpr bool operator>=  ( const /\*iterator\*/& x, const /\*iterator\*/& y )     requires std::totally_ordered<W>; | (5) | (since C++20) |
| friend constexpr bool operator<=>  ( const /\*iterator\*/& x, const /\*iterator\*/& y )     requires std::totally_ordered<W> && std::three_way_comparable<W>; | (6) | (since C++20) |
|  |  |  |

1) Returns x.`value_`== y.`value_`.2) Returns x.`value_`< y.`value_`.3) Returns y < x.4) Returns !(y < x).5) Returns !(x < y).6) Returns x.`value_`<=> y.`value_`.

The `!=` operator is synthesized from `operator==`.

These functions are not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when **iterator** is an associated class of the arguments.

## operator+(std::ranges::iota_view::**iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr /\*iterator\*/ operator+  ( /\*iterator\*/ i, difference_type n )     requires /\*advanceable\*/<W>; | (1) | (since C++20) |
| friend constexpr /\*iterator\*/ operator+  ( difference_type n, /\*iterator\*/ i )     requires /\*advanceable\*/<W>; | (2) | (since C++20) |
|  |  |  |

Equivalent to i += n; return i;.

These functions are not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when **iterator** is an associated class of the arguments.

## operator-(std::ranges::iota_view::**iterator**)

|  |  |  |
| --- | --- | --- |
| friend constexpr /\*iterator\*/ operator-  ( /\*iterator\*/ i, difference_type n )     requires /\*advanceable\*/<W>; | (1) | (since C++20) |
| friend constexpr difference_type operator-  ( const /\*iterator\*/& x, const /\*iterator\*/& y )     requires /\*advanceable\*/<W>; | (2) | (since C++20) |
|  |  |  |

1) Equivalent to i -= n; return i;.2) Let `D` be `difference_type`:

- If `W` is an integer-like type:
  - If `W` is signed-integer-like, returns D(D(x.`value_` ﻿) - D(y.`value_` ﻿)).
  - Otherwise, returns y.`value_`> x.`value_`? D(-D(y.`value_`- x.`value_` ﻿)) : D(x.`value_`- y.`value_` ﻿).
- Otherwise, returns x.`value_`- y.`value_`.

These functions are not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when **iterator** is an associated class of the arguments.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P2259R1 | C++20 | member `iterator_category` is always defined | defined only if `W` satisfies `incrementable` |
| LWG 3580 | C++20 | bodies of operator+ and operator- rule out implicit move | made suitable for implicit move |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/iota_view/iterator&oldid=176931>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 October 2024, at 08:57.