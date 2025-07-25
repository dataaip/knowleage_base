# **is-integer-like** ﻿, **is-signed-integer-like**

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | indirectly_readable(C++20) | | | | | | indirectly_writable(C++20) | | | | | | weakly_incrementable(C++20) | | | | | | incrementable(C++20) | | | | | | ******is-integer-like** **is-signed-integer-like******(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sentinel_for(C++20) | | | | | | sized_sentinel_for(C++20) | | | | | | input_iterator(C++20) | | | | | | output_iterator(C++20) | | | | | | input_or_output_iterator(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward_iterator(C++20) | | | | | | bidirectional_iterator(C++20) | | | | | | random_access_iterator(C++20) | | | | | | contiguous_iterator(C++20) | | | | | |  | | | | | |  | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterator operations | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | advance | | | | | | distance | | | | | | prev(C++11) | | | | | | next(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ranges::advance(C++20) | | | | | | ranges::distance(C++20) | | | | | | ranges::prev(C++20) | | | | | | ranges::next(C++20) | | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Range access | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | begincbegin(C++11)(C++14) | | | | | | rbegincrbegin(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | endcend(C++11)(C++14) | | | | | | rendcrend(C++14)(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sizessize(C++17)(C++20) | | | | | | empty(C++17) | | | | | | data(C++17) | | | | | | | |

|  |  |  |
| --- | --- | --- |
| template< class T >  constexpr bool /\*is-integer-like\*/ = /\* see description \*/; | (1) | (since C++20)  (exposition only\*) |
| template< class T >  constexpr bool /\*is-signed-integer-like\*/ = /\* see description \*/; | (2) | (since C++20)  (exposition only\*) |
|  |  |  |

1) /\*is-integer-like\*/<T> is true if and only if `T` is an integer-like type.2) /\*is-signed-integer-like\*/<T> is true if and only if `T` is a signed-integer-like type.

### Integer-class type

A type `T` is an **integer-class type** if it is in a set of implementation-defined types that behave as integer types do, as defined below. An integer-class type is not necessarily a class type.

An integer-class type can represent \(\scriptsize 2^N \)2N  
 consecutive integers, where N, a positive integer, is called the **width** of the integer-class type.

An integer-class type is either signed or unsigned:

- A **signed integer class type** can represent all integers in `[`\(\scriptsize -2^{N-1} \)-2N-1  
  `,`\(\scriptsize 2^{N-1}-1 \)2N-1  
  -1`]`, where N is greater than the width of every signed integral type.
- An **unsigned integer class type** can represent all integers in `[`\(\scriptsize 0 \)0`,`\(\scriptsize 2^N-1 \)2N  
  -1`]`, where N is greater than the width of every unsigned integral type.

All integer-class types model `regular` and `three_way_comparable`<std::strong_ordering>.

A value-initialized object of integer-class type has value â0â.

An expression E of integer-class type `T` is contextually convertible to bool as if by bool(E != T(0)).

### Integer-like type

A type other than (possibly cv-qualified) bool is **integer-like** if it models `integral` or if it is an integer-class type.

- An integer-like type is **signed-integer-like** if it models `signed_integral` or if it is a signed-integer-class type.
- An integer-like type is **unsigned-integer-like** if it models `unsigned_integral` or if it is an unsigned-integer-class type.

### Required behaviors

Expressions of integer-class type are explicitly convertible to any integer-like type, and implicitly convertible to any integer-class type of equal or greater width and the same signedness. Expressions of integral type are both implicitly and explicitly convertible to any integer-class type. Conversions between integral and integer-class types and between two integer-class types do not exit via an exception. The result of such a conversion is the unique value of the destination type that is congruent to the source modulo \(\scriptsize 2^N \)2N  
, where N is the width of the destination type.

Let `Int<T>` denote the following type:

- If `T` is an integer-class type, `Int<T>` is a unique hypothetical extended integer type of the same signedness with the same width as `T`.
- If `T` is an integral type, let `Int<T>` is the same type as `T`.

Given the following types, values and operators:

|  |  |
| --- | --- |
| Type | Definition |
| `IC` | an integer-class type |
| `IL` | an integer-like type |
| Value | Definition |
| a | an object of type `IC` |
| b | an object of type `IL` |
| c | an lvalue of an integeral type |
| x | an object of type `Int<IC>` that represent the same value as a |
| y | an object of type `Int<IL>` that represent the same value as b |
| Operator | Definition |
| @= | one of +=, -=, \*=, /=, %=, &=, |=, ^=, <<= and >>= |
| @ | one of +, -, \*, /, %, &, |, ^, <<, >>, &&, ||, ==, !=, <, >, <=, >=, <=> and , |

The following expressions must be well-formed and have their specified result and effects if the specified conditions are satisfied:

| Expression | Condition | Result | Effects |
| --- | --- | --- | --- |
| a++ | No condition | a prvalue of type `IC` whose value is equal to that of a prior to the evaluation | modifies the value of a by adding 1 to it |
| a-- | modifies the value of a by subtracting 1 to it |
| ++a | expression-equivalent to a += 1 | | |
| --a | expression-equivalent to a -= 1 | | |
| &a | expression-equivalent to std::addressof(a) | | |
| !a | !x is well-formed | same as !x | |
| +a | +x is well-formed | same as +x, but has type `IC` | same as +x |
| -a | -x is well-formed | same as -x, but has type `IC` | same as -x |
| ~a | ~x is well-formed | same as ~x, but has type `IC` | same as ~x |
| c @= a | c @= x is well-formed | an lvalue referring to c | same as c @= x |
| a @= b | x @= y is well-formed | an lvalue referring to a | same as x @= y, except that the value that would be stored into x is stored into a |
| a @ b | x @ y is well-formed | same as x @ y, but the result type is different:  - If x @ y is of type `Int<IC>`, the result has type `IC`. - If x @ y is of type `Int<IL>`, the result has type `IL`. - If x @ y is of any other type `T`, the result has type `T`. | same as x @ y |
| b @ a | y @ x is well-formed | same as y @ x, but the result type is different:  - If y @ x is of type `Int<IC>`, the result has type `IC`. - If y @ x is of type `Int<IL>`, the result has type `IL`. - If y @ x is of any other type `T`, the result has type `T`. | same as y @ x |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3366 (P2393R1) | C++20 | the conversion between an integer-class type and its corresponding integer type was not guaranteed to produce a representable value | guaranteed |
| LWG 3376 (P2393R1) | C++20 | integer-class types could only be class types | also allowed non-class types |
| LWG 3467 | C++20 | bool was considered as an integer-like type | excluded |
| LWG 3575 (P2393R1) | C++20 | integer-class types were not guaranteed to be three-way-comparable | guaranteed |

### See also

|  |  |
| --- | --- |
| weakly_incrementable(C++20) | specifies that a `semiregular` type can be incremented with pre- and post-increment operators   (concept) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/iterator/is-integer-like&oldid=176026>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 September 2024, at 22:40.