# std::ranges::subrange

From cppreference.com
< cpp‎ | ranges
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | view_interface | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****subrange**** | | | | | |  | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range factories | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | empty_viewviews::empty | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | single_viewviews::single | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | basic_istream_viewviews::istream | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota_viewviews::iota | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | repeat_viewviews::repeat(C++23)(C++23) | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Range adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | views::all_tviews::all | | | | | | ref_view | | | | | | owning_view | | | | | | as_rvalue_viewviews::as_rvalue(C++23)(C++23) | | | | | | filter_viewviews::filter | | | | | | transform_viewviews::transform | | | | | | take_viewviews::take | | | | | | take_while_viewviews::take_while | | | | | | concat_viewviews::concat(C++26)(C++26) | | | | | | views::counted | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | drop_viewviews::drop | | | | | | drop_while_viewviews::drop_while | | | | | | join_viewviews::join | | | | | | join_with_viewviews::join_with(C++23)(C++23) | | | | | | lazy_split_viewviews::lazy_split | | | | | | split_viewviews::split | | | | | | common_viewviews::common | | | | | | cache_latest_viewviews::cache_latest(C++26)(C++26) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_viewviews::reverse | | | | | | as_const_viewviews::as_const(C++23)(C++23) | | | | | | elements_viewviews::elements | | | | | | keys_viewviews::keys | | | | | | values_viewviews::values | | | | | | enumerate_viewviews::enumerate(C++23)(C++23) | | | | | | zip_viewviews::zip(C++23)(C++23) | | | | | | zip_transform_viewviews::zip_transform(C++23)(C++23) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | adjacent_viewviews::adjacent(C++23)(C++23) | | | | | | views::pairwise(C++23) | | | | | | adjacent_transform_viewviews::adjacent_transform(C++23)(C++23) | | | | | | views::pairwise_transform(C++23) | | | | | | chunk_viewviews::chunk(C++23)(C++23) | | | | | | slide_viewviews::slide(C++23)(C++23) | | | | | | chunk_by_viewviews::chunk_by(C++23)(C++23) | | | | | | stride_viewviews::stride(C++23)(C++23) | | | | | | cartesian_product_viewviews::cartesian_product(C++23)(C++23) | | | | | |  | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range generators | | | | | | std::generator(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor closure objects | | | | | | range_adaptor_closure(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range adaptor objects | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Helper items | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **copyable-box** **movable-box**(until C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | **simple-view** | | | | | | **non-propagating-cache** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | |  | | | | | |

****std::ranges::subrange****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| subrange::subrange | | | | |
| subrange::operator PairLike | | | | |
| Observers | | | | |
| subrange::begin | | | | |
| subrange::end | | | | |
| subrange::empty | | | | |
| subrange::size | | | | |
| Iterator operations | | | | |
| subrange::advance | | | | |
| subrange::next | | | | |
| subrange::prev | | | | |
| Deduction guides | | | | |
| Non-member functions | | | | |
| get(std::ranges::subrange) | | | | |
| Helper types | | | | |
| subrange_kind | | | | |
| tuple_size<std::ranges::subrange> | | | | |
| tuple_element<std::ranges::subrange> | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<ranges>` |  |  |
| template<  std::input_or_output_iterator I,      std::sentinel_for<I> S = I,      ranges::subrange_kind K = std::sized_sentinel_for<S, I> ?                                    ranges::subrange_kind::sized :                                    ranges::subrange_kind::unsized  >      requires (K == ranges::subrange_kind::sized ||                   !std::sized_sentinel_for<S, I>)  class subrange : public ranges::view_interface<subrange<I, S, K>> | (1) | (since C++20) |
| Helper concepts |  |  |
| template<class From, class To>  concept /\*uses-nonqualification-pointer-conversion\*/ = /\* see description \*/; | (2) | (exposition only\*) |
| template<class From, class To>  concept /\*convertible-to-non-slicing\*/ = /\* see description \*/; | (3) | (exposition only\*) |
|  |  |  |

1) The `subrange` class template combines together an iterator and a sentinel into a single `view`. It models `sized_range` whenever the final template parameter is subrange_kind​::​sized (which happens when std::sized_sentinel_for<S, I> is satisfied or when size is passed explicitly as a constructor argument).2) Determines whether `From` is convertible to `To` without qualification conversions. Equivalent to:

```
template<class From, class To>
concept /*uses-nonqualification-pointer-conversion*/ =
    std::is_pointer_v<From> && std::is_pointer_v<To> &&
        !std::convertible_to<std::remove_pointer_t<From>(*)[],
                             std::remove_pointer_t<To>(*)[]>;

```

3) Determines whether `From` is convertible to `To` without derived-to-base conversion:

```
template<class From, class To>
concept /*convertible-to-non-slicing*/ =
    std::convertible_to<From, To> &&
        !/*uses-nonqualification-pointer-conversion*/
            <std::decay_t<From>, std::decay_t<To>>;

```

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| constexpr bool `StoreSize`  [static] | K == ranges::subrange_kind::sized && !std::sized_sentinel_for<S, I> (exposition-only static member constant\*) |
| `I` `begin_` | an iterator to the beginning of the subrange (exposition-only member object\*) |
| `S` `end_` | a sentinel denoting the end of the subrange (exposition-only member object\*) |
| `make-unsigned-like-t` ﻿<std::iter_difference_t<I>> `size_`  (present only if `StoreSize` is true) | the size of the subrange (exposition-only member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | creates a new `subrange`   (public member function) |
| operator PairLike | converts the `subrange` to a **pair-like** type   (public member function) |
| Observers | |
| begin | obtains the iterator   (public member function) |
| end | obtains the sentinel   (public member function) |
| empty | checks whether the `subrange` is empty   (public member function) |
| size | obtains the size of the `subrange`   (public member function) |
| Iterator operations | |
| advance | advances the iterator by given distance   (public member function) |
| prev | obtains a copy of the `subrange` with its iterator decremented by a given distance   (public member function) |
| next | obtains a copy of the `subrange` with its iterator advanced by a given distance   (public member function) |
| Inherited from std::ranges::view_interface | |
| cbegin(C++23) | returns a constant iterator to the beginning of the range.   (public member function of `std::ranges::view_interface<D>`) |
| cend(C++23) | returns a sentinel for the constant iterator of the range.   (public member function of `std::ranges::view_interface<D>`) |
| operator bool | returns whether the derived view is not empty. Provided if ranges::empty is applicable to it.   (public member function of `std::ranges::view_interface<D>`) |
| data | gets the address of derived view's data. Provided if its iterator type satisfies `contiguous_iterator`.   (public member function of `std::ranges::view_interface<D>`) |
| front | returns the first element in the derived view. Provided if it satisfies `forward_range`.   (public member function of `std::ranges::view_interface<D>`) |
| back | returns the last element in the derived view. Provided if it satisfies `bidirectional_range` and `common_range`.   (public member function of `std::ranges::view_interface<D>`) |
| [operator[]](view_interface/operator_at.html "cpp/ranges/view interface/operator at") | returns the `n`th element in the derived view. Provided if it satisfies `random_access_range`.   (public member function of `std::ranges::view_interface<D>`) |

### Deduction guides

### Non-member functions

|  |  |
| --- | --- |
| get(std::ranges::subrange)(C++20) | obtains iterator or sentinel from a ****std::ranges::subrange****   (function template) |

### Helper types

|  |  |
| --- | --- |
| ranges::subrange_kind(C++20) | specifies whether a ****std::ranges::subrange**** models std::ranges::sized_range   (enum) |
| std::tuple_size<std::ranges::subrange>(C++20) | obtains the size of a ****std::ranges::subrange****   (class template specialization) |
| std::tuple_element<std::ranges::subrange>(C++20) | obtains the type of the iterator or the sentinel of a ****std::ranges::subrange****   (class template specialization) |

### Helper templates

|  |  |  |
| --- | --- | --- |
| template< class I, class S, ranges::subrange_kind K >  constexpr bool ranges::enable_borrowed_range<ranges::subrange<I, S, K>> = true; |  | (since C++20) |
|  |  |  |

This specialization of ranges::enable_borrowed_range makes `subrange` satisfy `borrowed_range`.

### Example

Run this code

```
#include <map>
#include <print>
#include <ranges>
 
void make_uppercase(char& v)
{
    v += 'A' - 'a';
}
 
void uppercase_transform(std::multimap<int, char>& m, int k)
{
    auto [first, last] = m.equal_range(k);
    for (auto& [_, v] : std::ranges::subrange(first, last))
        make_uppercase(v);
}
 
int main()
{
    std::multimap<int, char> mm{{4, 'a'}, {3, '-'}, {4, 'b'}, {5, '-'}, {4, 'c'}};
    std::println("Before: {}", mm);
    uppercase_transform(mm, 4);
    std::println("After:  {}", mm);
}

```

Output:

```
Before: {3: '-', 4: 'a', 4: 'b', 4: 'c', 5: '-'}
After:  {3: '-', 4: 'A', 4: 'B', 4: 'C', 5: '-'}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3470 | C++20 | `convertible-to-non-slicing` might reject qualification conversions | always accepts them |

### See also

|  |  |
| --- | --- |
| ranges::view_interface(C++20) | helper class template for defining a `view`, using the curiously recurring template pattern   (class template) |

### External links

|  |
| --- |
| Read/write all values of a `std::multimap` with a given key in C++20 — SO |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/subrange&oldid=179863>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 January 2025, at 04:18.