# std::ranges::concat_view<Views...>::**iterator**<Const>::**satisfy**, **prev**, **advance-fwd**, **advance-bwd**

From cppreference.com
< cpp‎ | ranges‎ | concat view‎ | iterator
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

std::ranges::concat_view

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| concat_view::concat_view | | | | |
| concat_view::begin | | | | |
| concat_view::end | | | | |
| concat_view::size | | | | |
| Deduction guides | | | | |
| Iterator | | | | |
| Member functions | | | | |
| concat_view::**iterator**::**iterator** | | | | |
| concat_view::**iterator**::operator\* | | | | |
| [concat_view::**iterator**::operator[]](operator_at.html "cpp/ranges/concat view/iterator/operator at") | | | | |
| concat_view::**iterator**::operator++ concat_view::**iterator**::operator++(int) concat_view::**iterator**::operator-- concat_view::**iterator**::operator--(int) concat_view::**iterator**::operator+= concat_view::**iterator**::operator-= | | | | |
| ****concat_view::**iterator**::**satisfy** concat_view::**iterator**::**prev** concat_view::**iterator**::**advance-fwd** concat_view::**iterator**::**advance-bwd****** | | | | |
| Non-member functions | | | | |
| operator==(concat_view::**iterator**) operator<(concat_view::**iterator**) operator>(concat_view::**iterator**) operator<=(concat_view::**iterator**) operator>=(concat_view::**iterator**) operator<=>(concat_view::**iterator**) | | | | |
| operator+(concat_view::**iterator**) operator-(concat_view::**iterator**) | | | | |
| iter_move(concat_view::**iterator**) | | | | |
| iter_swap(concat_view::**iterator**) | | | | |

The following exposition-only member function templates simplify the description.

Each helper function template has a non-type template parameter of type std::size_t.

- If the name of the template parameter is N, the template argument is always `it_` ﻿.index().
- If the name of the template parameter is I, the template argument can be any std::size_t value in ``​0​`,`sizeof...(Views)`)`.

However, the template argument might not be a compile-time constant, therefore the actual effect of `helper` ﻿<non_const>(/\* arguments \*/) is similar to 
if (non_const == 0)  
`helper` ﻿<0>(/\* arguments \*/);  
else if (non_const == 1)  
`helper` ﻿<1>(/\* arguments \*/);  
/\* other indices \*/  
else if (non_const == (sizeof...(Views) - 1))  
`helper` ﻿<sizeof...(Views) - 1>(/\* arguments \*/);  
.

### Helper templates

## Mini helper templates

|  |  |  |
| --- | --- | --- |
| template< [std::size_t N >  constexpr auto /\*get-iter\*/(); | (1) | (exposition only\*) |
| template< std::size_t I >  constexpr auto /\*get-view\*/(); | (2) | (exposition only\*) |
| template< std::size_t I >  constexpr auto /\*get-begin\*/(); | (3) | (exposition only\*) |
| template< std::size_t I >  constexpr auto /\*get-end\*/(); | (4) | (exposition only\*) |
| template< std::size_t N >  constexpr auto /\*to-underlying-diff-type\*/( difference_type value ); | (5) | (exposition only\*) |
|  |  |  |

The mini helper templates simplify the description of the main helper templates and member functions. They are not included in the C++ standard documents.

1) Obtains the underlying iterator contained in `it_` ﻿. Returns std::get<N>(`it_` ﻿).2) Obtains the Ith view in the parent `concat_view`. Returns std::get<I>(`parent_` ﻿->`views_` ﻿).3) Obtains an iterator to the beginning of the Ith view in the parent `concat_view`. Returns ranges::begin(`get-view` ﻿<I>()).4) Obtains a past-the-end iterator or a sentinel of the Ith view in the parent `concat_view`. Returns ranges::end(`get-view` ﻿<I>()).5) Converts value to the underlying difference type of the underlying iterator contained in `it_` ﻿. Returns static_cast<std::iter_difference_t<std::variant_alternative_t<N,`base-iter` ﻿>>>(value).

## std::ranges::concat_view::**iterator**::**satisfy**<N>

|  |  |  |
| --- | --- | --- |
| template< std::size_t N >  constexpr void /\*satisfy\*/(); |  | (exposition only\*) |
|  |  |  |

Adjusts the current (global) position of `it_` ﻿.

- If N is sizeof...(Views) - 1, does nothing.
- Otherwise, equivalent to if (`get-iter` ﻿<N>() ==`get-end` ﻿<N>())  
  {  
  `it_` ﻿.template emplace<N + 1>(`get-begin` ﻿<N + 1>());  
  `satisfy` ﻿<N + 1>();  
  }.

## std::ranges::concat_view::**iterator**::**prev**<N>

|  |  |  |
| --- | --- | --- |
| template< size_t N >  constexpr void /\*prev\*/(); |  | (exposition only\*) |
|  |  |  |

Moves `it_` to the previous (global) position.

- If N is ​0​, equivalent to --`get-iter` ﻿<0>();.
- Otherwise, equivalent to if (`get-iter` ﻿<N>() ==`get-begin` ﻿<N>())  
  {  
  `it_` ﻿.template emplace<N - 1>(`get-end` ﻿<N - 1>());  
  `prev` ﻿<N - 1>();  
  }  
  else  
  --`get-iter` ﻿<0>();.

## std::ranges::concat_view::**iterator**::**advance-fwd**<N>

|  |  |  |
| --- | --- | --- |
| template< size_t N >  constexpr void /\*advance-fwd\*/( difference_type offset,                                 difference_type steps ); |  | (exposition only\*) |
|  |  |  |

Advances the current (global) position step steps forward.

- If N is sizeof...(Views) - 1, equivalent to `get-iter` ﻿<N>() +=`to-underlying-diff-type` ﻿(steps);.
- Otherwise, equivalent to auto n_size = ranges::distance(`get-view` ﻿<N>()));  
  if (offset + steps < n_size)  
  `get-iter` ﻿<N>() +=`to-underlying-diff-type` ﻿(steps);  
  else  
  {  
  `it_` ﻿.template emplace<N + 1>(`get-begin` ﻿<N + 1>());  
  `advance-fwd` ﻿<N + 1>(0, offset + steps - n_size);  
  }.

### Parameters

|  |  |  |
| --- | --- | --- |
| offset | - | the offset of the current (global) position from the beginning of range `it_` currently refers into |
| steps | - | the number of steps to advance forward |

## std::ranges::concat_view::**iterator**::**advance-bwd**<N>

|  |  |  |
| --- | --- | --- |
| template< size_t N >  constexpr void /\*advance-bwd\*/( difference_type offset,                                 difference_type steps ); |  | (exposition only\*) |
|  |  |  |

Advances the current (global) position steps steps backward.

- If N is ​0​, equivalent to `get-iter` ﻿<N>() -=`to-underlying-diff-type` ﻿(steps);.
- Otherwise, equivalent to if (offset >= steps)  
  `get-iter` ﻿<N>() -=`to-underlying-diff-type` ﻿(steps);  
  else  
  {  
  auto prev_size = ranges::distance(`get-view` ﻿<N - 1>());  
  `it_` ﻿.template emplace<N - 1>(`get-end` ﻿<N - 1>());  
  `advance-bwd` ﻿<N - 1>(prev_size, steps - offset);  
  }.

### Parameters

|  |  |  |
| --- | --- | --- |
| offset | - | the offset of the current (global) position from the beginning of range `it_` currently refers into |
| steps | - | the number of steps to advance backward |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/ranges/concat_view/iterator/helpers&oldid=176986>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 October 2024, at 17:21.