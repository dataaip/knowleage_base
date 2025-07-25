# std::indirectly_readable_traits

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | input_iterator_tagoutput_iterator_tagforward_iterator_tagbidirectional_iterator_tagrandom_access_iterator_tagcontiguous_iterator_tag(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iter_value_titer_difference_titer_reference_titer_const_reference_titer_rvalue_reference_titer_common_reference_t(C++20)(C++20)(C++20)(C++23)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iterator(deprecated in C++17) | | | | | | iterator_traits | | | | | | incrementable_traits(C++20) | | | | | | ****indirectly_readable_traits****(C++20) | | | | | |  | | | | | |  | | | | | |
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
| template< class I >  struct indirectly_readable_traits {}; | (1) | (since C++20) |
| template< class T >  struct indirectly_readable_traits<T\*> : /\* cond-value-type \*/<T> {}; | (2) | (since C++20) |
| template< class I >      requires std::is_array_v<I>  struct indirectly_readable_traits<I>; { using value_type = std::remove_cv_t<std::remove_extent_t<I>>; } | (3) | (since C++20) |
| template< class T >  struct indirectly_readable_traits<const T> :     indirectly_readable_traits<T> {}; | (4) | (since C++20) |
| template< /\* has-member-value-type \*/ T >  struct indirectly_readable_traits<T> : /\* cond-value-type \*/<typename T::value_type> {}; | (5) | (since C++20) |
| template< /\* has-member-element-type \*/ T >  struct indirectly_readable_traits<T> : /\* cond-value-type \*/<typename T::element_type> {}; | (6) | (since C++20) |
| template< /\* has-member-value-type \*/ T >      requires /\* has-member-element-type \*/<T> struct indirectly_readable_traits<T> {}; | (7) | (since C++20) |
| template< /\* has-member-value-type \*/ T >      requires /\* has-member-element-type \*/<T> &&               std::same_as<std::remove_cv_t<typename T::element_type>,                            std::remove_cv_t<typename T::value_type>>  struct indirectly_readable_traits<T> : /\* cond-value-type \*/<typename T::value_type> {}; | (8) | (since C++20) |
| Helper classes and concepts |  |  |
| template< class >  struct /\* cond-value-type \*/ {}; | (1) | (exposition only\*) |
| template< class T >      requires std::is_object_v<T>  struct /\* cond-value-type \*/ <T> { using value_type = std::remove_cv_t<T>; }; | (2) | (exposition only\*) |
| template< class T >  concept /\* has-member-value-type \*/ =     requires { typename T::value_type; }; | (3) | (exposition only\*) |
| template< class T >  concept /\* has-member-element-type \*/ =     requires { typename T::element_type; }; | (4) | (exposition only\*) |
|  |  |  |

Computes the associated value type of the template argument. If the associated value type exists, it is represented by the nested type `value_type`, otherwise `value_type` is not defined. A program may specialize `indirectly_readable_traits` for a program-defined type.

### Explanation

The specializations above can be informally described as below.

Given a type `T`, its associated value type `V` is determined as follows:

- If `T` is const-qualified, `V` is the associated value type of const-unqualified `T`.
- Otherwise, if `T` is an array type, `V` is the cv-unqualified array element type.
- Otherwise, a conditional value type `C` is determined first:

:   - If `T` is a pointer type, `C` is the pointed-to type.
    - Otherwise, if `T` has nested types `value_type` and `element_type`:

    :   - If these types are the same (not considering cv-qualification), `C` is `typename T::value_type`.
        - Otherwise, `C` is undefined.

    - Otherwise, if `T` has the nested type `value_type` but not `element_type`, `C` is `typename T::value_type`.
    - Otherwise, if `T` has the nested type `element_type` but not `value_type`, `C` is `typename T::element_type`.
    - Otherwise, `C` is undefined.
:   Then `V` is determined from `C` as follows:

    - If `C` is undefined, or `C` is not an object type, `V` is undefined.
    - Otherwise, `V` is cv-unqualified `C`.

### Notes

`value_type` is intended for use with `indirectly_readable` types such as iterators. It is not intended for use with ranges.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3446 | C++20 | specializations (5,6) were ambiguous for types having both `value_type` and `element_type` nested types | added specialization (8) |
| LWG 3541 | C++20 | LWG 3446 introduced hard error for ambiguous cases that `value_type` and `element_type` are different | added specialization (7) |

### See also

|  |  |
| --- | --- |
| indirectly_readable(C++20) | specifies that a type is indirectly readable by applying operator `*`   (concept) |
| iter_value_titer_reference_titer_const_reference_titer_difference_titer_rvalue_reference_titer_common_reference_t(C++20)(C++20)(C++23)(C++20)(C++20)(C++20) | computes the associated types of an iterator (alias template) |
| iterator_traits | provides uniform interface to the properties of an iterator   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/indirectly_readable_traits&oldid=170152>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 March 2024, at 01:13.