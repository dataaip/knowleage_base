# std::iter_value_t, std::iter_reference_t, std::iter_const_reference_t, std::iter_difference_t, std::iter_rvalue_reference_t, std::iter_common_reference_t

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tagcontiguous_iterator_tag(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****iter_value_titer_difference_titer_reference_titer_const_reference_titer_rvalue_reference_titer_common_reference_t****(C++20)(C++20)(C++20)(C++23)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator(deprecated in C++17) | | | | | | iterator_traits | | | | | | incrementable_traits(C++20) | | | | | | indirectly_readable_traits(C++20) | | | | | |  | | | | | |  | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator operations | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | prev(C++11) | | | | | | next(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::advance(C++20) | | | | | | ranges::distance(C++20) | | | | | | ranges::prev(C++20) | | | | | | ranges::next(C++20) | | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begincbegin(C++11)(C++14) | | | | | | rbegincrbegin(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend(C++11)(C++14) | | | | | | rendcrend(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sizessize(C++17)(C++20) | | | | | | empty(C++17) | | | | | | data(C++17) | | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<iterator>` |  |  |
| template< class T >  using iter_value_t = /\* see below \*/; | (1) | (since C++20) |
| template< /\*dereferenceable\*/ T >  using iter_reference_t = decltype(\*std::declval<T&>()); | (2) | (since C++20) |
| template< std::indirectly_readable T >  using iter_const_reference_t =      std::common_reference_t<const std::iter_value_t<T>&&,                             std::iter_reference_t<T>>; | (3) | (since C++23) |
| template< class T >  using iter_difference_t = /\* see below \*/; | (4) | (since C++20) |
| template< /\*dereferenceable\*/ T>      requires /\* see below \*/  using iter_rvalue_reference_t =     decltype(ranges::iter_move(std::declval<T&>())); | (5) | (since C++20) |
| template< std::indirectly_readable T >  using iter_common_reference_t =      std::common_reference_t<std::iter_reference_t<T>, /\*indirect-value-t\*/<T>>; | (6) | (since C++20) |
| Helper templates |  |  |
| template< class T >  concept /\*dereferenceable\*/ = /\* see below \*/; | (7) | (exposition only\*) |
| template< std::indirectly_readable T >  using /\*indirect-value-t\*/ = /\* see below \*/; | (8) | (exposition only\*) |
|  |  |  |

Compute the associated types of an iterator.

1) Computes the value type of `T`.

- If std::iterator_traits<std::remove_cvref_t<T>> is not specialized, then std::iter_value_t<T> is std::indirectly_readable_traits<std::remove_cvref_t<T>>::value_type.
- Otherwise, it is std::iterator_traits<std::remove_cvref_t<T>>::value_type.
2) Computes the **reference type** of `T`.3) Computes the **const reference type** of `T`.4) Computes the difference type of `T`.

- If std::iterator_traits<std::remove_cvref_t<T>> is not specialized, then std::iter_difference_t<T> is std::incrementable_traits<std::remove_cvref_t<T>>::difference_type.
- Otherwise, it is std::iterator_traits<std::remove_cvref_t<T>>::difference_type.
5) Computes the **rvalue reference type** of `T`. The constraint on this alias template is satisfied if and only if the expression ranges::iter_move(std::declval<T&>()) is valid and has a referenceable type.6) Computes the **common reference type** of `T`. This is the common reference type between its reference type and an lvalue reference to its value type.7) The exposition-only concept `dereferenceable` is satisfied if and only if the expression \*std::declval<T&>() is valid and has a referenceable type.8) The exposition-only alias template `indirect-value-t` denotes the following:

- std::invoke_result_t<Proj&, /\*indirect-value-t\*/<I>> if `T` is the same as std::projected<I, Proj> for some types `I` and `Proj`.
- Otherwise, std::iter_value_t<T>&.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| P2609R3 | C++20 | `std::iter_common_reference_t` was defined in terms of std::iter_value_t<T>& which incorrectly handled std::projected types that project into rvalue reference types | defined in terms of /\*indirect-value-t\*/<T> to handle such cases |

### See also

|  |  |
| --- | --- |
| indirectly_readable(C++20) | specifies that a type is indirectly readable by applying operator `*`   (concept) |
| weakly_incrementable(C++20) | specifies that a `semiregular` type can be incremented with pre- and post-increment operators   (concept) |
| indirectly_readable_traits(C++20) | computes the value type of an `indirectly_readable` type   (class template) |
| incrementable_traits(C++20) | computes the difference type of a `weakly_incrementable` type   (class template) |
| iterator_traits | provides uniform interface to the properties of an iterator   (class template) |
| ranges::iterator_tranges::const_iterator_tranges::sentinel_tranges::const_sentinel_t(C++20)(C++23)(C++20)(C++23) | obtains iterator and sentinel types of a range (alias template) |
| ranges::range_reference_tranges::range_const_reference_tranges::range_rvalue_reference_tranges::range_common_reference_t(C++20)(C++23)(C++20)(C++20) | obtains reference types of a range (alias template) |
| ranges::range_difference_tranges::range_size_tranges::range_value_t(C++20)(C++20)(C++20) | obtains size, difference, and value types of a range (alias template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/iter_t&oldid=175692>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 September 2024, at 22:50.