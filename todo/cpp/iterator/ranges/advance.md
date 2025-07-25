# std::ranges::advance

From cppreference.com
< cpp‎ | iterator
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

Iterator library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Iterator concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_readable(C++20) | | | | | | indirectly_writable(C++20) | | | | | | weakly_incrementable(C++20) | | | | | | incrementable(C++20) | | | | | | **is-integer-like** **is-signed-integer-like**(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sentinel_for(C++20) | | | | | | sized_sentinel_for(C++20) | | | | | | input_iterator(C++20) | | | | | | output_iterator(C++20) | | | | | | input_or_output_iterator(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_iterator(C++20) | | | | | | bidirectional_iterator(C++20) | | | | | | random_access_iterator(C++20) | | | | | | contiguous_iterator(C++20) | | | | | |  | | | | | |  | | | | | |
| Iterator primitives | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tagcontiguous_iterator_tag(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iter_value_titer_difference_titer_reference_titer_const_reference_titer_rvalue_reference_titer_common_reference_t(C++20)(C++20)(C++20)(C++23)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator(deprecated in C++17) | | | | | | iterator_traits | | | | | | incrementable_traits(C++20) | | | | | | indirectly_readable_traits(C++20) | | | | | |  | | | | | |  | | | | | |
| Algorithm concepts and utilities | | | | |
| Indirect callable concepts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_unary_invocableindirectly_regular_unary_invocable(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_unary_predicate(C++20) | | | | | | indirect_binary_predicate(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_equivalence_relation(C++20) | | | | | | indirect_strict_weak_order(C++20) | | | | | |
| Common algorithm requirements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_movable(C++20) | | | | | | indirectly_movable_storable(C++20) | | | | | | indirectly_copyable(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_copyable_storable(C++20) | | | | | | indirectly_swappable(C++20) | | | | | | indirectly_comparable(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | permutable(C++20) | | | | | | mergeable(C++20) | | | | | | sortable(C++20) | | | | | |
| Utilities | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirect_result_t(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | projected_value_t(C++26) | | | | | |
| Iterator adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | reverse_iterator | | | | | | make_reverse_iterator(C++14) | | | | | | move_iterator(C++11) | | | | | | make_move_iterator(C++11) | | | | | | default_sentinel_tdefault_sentinel(C++20)(C++20) | | | | | | unreachable_sentinel_tunreachable_sentinel(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | front_insert_iterator | | | | | | back_insert_iterator | | | | | | inserter | | | | | | insert_iterator | | | | | | front_inserter | | | | | | back_inserter | | | | | | move_sentinel(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | common_iterator(C++20) | | | | | | counted_iterator(C++20) | | | | | | basic_const_iterator(C++23) | | | | | | const_iterator(C++23) | | | | | | const_sentinel(C++23) | | | | | | make_const_iterator(C++23) | | | | | | make_const_sentinel(C++23) | | | | | |  | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Stream iterators | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istream_iterator | | | | | | ostream_iterator | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | istreambuf_iterator | | | | | | ostreambuf_iterator | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator customization points | | | | | | ranges::iter_move(C++20) | | | | | | ranges::iter_swap(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator operations | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | prev(C++11) | | | | | | next(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****ranges::advance****(C++20) | | | | | | ranges::distance(C++20) | | | | | | ranges::prev(C++20) | | | | | | ranges::next(C++20) | | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begincbegin(C++11)(C++14) | | | | | | rbegincrbegin(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend(C++11)(C++14) | | | | | | rendcrend(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sizessize(C++17)(C++20) | | | | | | empty(C++17) | | | | | | data(C++17) | | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<iterator>` |  |  |
| Call signature |  |  |
| template< std::input_or_output_iterator I >  constexpr void advance( I& i, std::iter_difference_t<I> n ); | (1) | (since C++20) |
| template< std::input_or_output_iterator I, std::sentinel_for<I> S >  constexpr void advance( I& i, S bound ); | (2) | (since C++20) |
| template< std::input_or_output_iterator I, std::sentinel_for<I> S >  constexpr std::iter_difference_t<I> advance( I& i, std::iter_difference_t<I> n, S bound ); | (3) | (since C++20) |
|  |  |  |

1) Increments given iterator i for n times.2) Increments given iterator i until i == bound.3) Increments given iterator i for n times, or until i == bound, whichever comes first.

If n is negative, the iterator is decremented. In this case, `I` must model std::bidirectional_iterator, and `S` must be the same type as `I` if bound is provided, otherwise the behavior is undefined.

The function-like entities described on this page are **algorithm function objects** (informally known as **niebloids**), that is:

- Explicit template argument lists cannot be specified when calling any of them.
- None of them are visible to argument-dependent lookup.
- When any of them are found by normal unqualified lookup as the name to the left of the function-call operator, argument-dependent lookup is inhibited.

### Parameters

|  |  |  |
| --- | --- | --- |
| i | - | iterator to be advanced |
| bound | - | sentinel denoting the end of the range i is an iterator to |
| n | - | number of maximal increments of i |

### Return value

3) The difference between n and the actual distance i traversed.

### Complexity

Linear.

However, if `I` additionally models std::random_access_iterator, or `S` models std::sized_sentinel_for<I>, or `I` and `S` model std::assignable_from<I&, S>, complexity is constant.

### Notes

The behavior is undefined if the specified sequence of increments or decrements would require that a non-incrementable iterator (such as the past-the-end iterator) is incremented, or that a non-decrementable iterator (such as the front iterator or the singular iterator) is decremented.

### Possible implementation

|  |
| --- |
| ```text struct advance_fn {     template<std::input_or_output_iterator I>     constexpr void operator()(I& i, std::iter_difference_t<I> n) const     {         if constexpr (std::random_access_iterator<I>)             i += n;         else         {             while (n > 0)             {                 --n;                 ++i;             }               if constexpr (std::bidirectional_iterator<I>)             {                 while (n < 0)                 {                     ++n;                     --i;                 }             }         }     }       template<std::input_or_output_iterator I, std::sentinel_for<I> S>     constexpr void operator()(I& i, S bound) const     {         if constexpr (std::assignable_from<I&, S>)             i = std::move(bound);         else if constexpr (std::sized_sentinel_for<S, I>)             (*this)(i, bound - i);         else             while (i != bound)                 ++i;     }       template<std::input_or_output_iterator I, std::sentinel_for<I> S>     constexpr std::iter_difference_t<I>     operator()(I& i, std::iter_difference_t<I> n, S bound) const     {         if constexpr (std::sized_sentinel_for<S, I>)         {             // std::abs is not constexpr until C++23             auto abs = [](const std::iter_difference_t<I> x) { return x < 0 ? -x : x; };               if (const auto dist = abs(n) - abs(bound - i); dist < 0)             {                 (*this)(i, bound);                 return -dist;             }               (*this)(i, n);             return 0;         }         else         {             while (n > 0 && i != bound)             {                 --n;                 ++i;             }               if constexpr (std::bidirectional_iterator<I>)             {                 while (n < 0 && i != bound)                 {                     ++n;                     --i;                 }             }               return n;         }     } };   inline constexpr auto advance = advance_fn(); ``` |

### Example

Run this code

```
#include <iostream>
#include <iterator>
#include <vector>
 
int main()
{
    std::vector<int> v {3, 1, 4};
 
    auto vi = v.begin();
 
    std::ranges::advance(vi, 2);
    std::cout << "1) value: " << *vi << '\n' << std::boolalpha;
 
    std::ranges::advance(vi, v.end());
    std::cout << "2) vi == v.end(): " << (vi == v.end()) << '\n';
 
    std::ranges::advance(vi, -3);
    std::cout << "3) value: " << *vi << '\n';
 
    std::cout << "4) diff: " << std::ranges::advance(vi, 2, v.end())
              << ", value: " << *vi << '\n';
 
    std::cout << "5) diff: " << std::ranges::advance(vi, 4, v.end())
              << ", vi == v.end(): " << (vi == v.end()) << '\n';
}

```

Output:

```
1) value: 4
2) vi == v.end(): true
3) value: 3
4) diff: 0, value: 4
5) diff: 3, vi == v.end(): true

```

### See also

|  |  |
| --- | --- |
| ranges::next(C++20) | increment an iterator by a given distance or to a bound (algorithm function object) |
| ranges::prev(C++20) | decrement an iterator by a given distance or to a bound (algorithm function object) |
| ranges::distance(C++20) | returns the distance between an iterator and a sentinel, or between the beginning and end of a range (algorithm function object) |
| advance | advances an iterator by given distance   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/ranges/advance&oldid=168436>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 January 2024, at 00:01.