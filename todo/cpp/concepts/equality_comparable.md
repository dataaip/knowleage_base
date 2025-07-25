# std::equality_comparable, std::equality_comparable_with

From cppreference.com
< cpp‎ | concepts
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

Concepts library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Core language concepts | | | | | | same_as(C++20) | | | | | | derived_from(C++20) | | | | | | convertible_to(C++20) | | | | | | common_reference_with(C++20) | | | | | | common_with(C++20) | | | | | | integral(C++20) | | | | | | signed_integral(C++20) | | | | | | unsigned_integral(C++20) | | | | | | floating_point(C++20) | | | | | | swappableswappable_with(C++20)(C++20) | | | | | | destructible(C++20) | | | | | | constructible_from(C++20) | | | | | | default_initializable(C++20) | | | | | | move_constructible(C++20) | | | | | | copy_constructible(C++20) | | | | | | assignable_from(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Comparison concepts | | | | | | ****equality_comparableequality_comparable_with****(C++20)(C++20) | | | | | | totally_orderedtotally_ordered_with(C++20)(C++20) | | | | | | Object concepts | | | | | | movable(C++20) | | | | | | copyable(C++20) | | | | | | semiregular(C++20) | | | | | | regular(C++20) | | | | | | Callable concepts | | | | | | invocableregular_invocable(C++20)(C++20) | | | | | | predicate(C++20) | | | | | | relation(C++20) | | | | | | equivalence_relation(C++20) | | | | | | strict_weak_order(C++20) | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exposition-only concepts | | | | | | **boolean-testable** ﻿(C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<concepts>` |  |  |
| template< class T >  concept equality_comparable = __WeaklyEqualityComparableWith<T, T>; | (1) | (since C++20) |
| template< class T, class U >  concept equality_comparable_with =      std::equality_comparable<T> &&      std::equality_comparable<U> &&      __ComparisonCommonTypeWith<T, U> &&      std::equality_comparable<          std::common_reference_t<              const std::remove_reference_t<T>&,              const std::remove_reference_t<U>&>> &&     __WeaklyEqualityComparableWith<T, U>; | (2) | (since C++20) |
| Helper concepts |  |  |
| template< class T, class U >  concept __WeaklyEqualityComparableWith =      requires(const std::remove_reference_t<T>& t,               const std::remove_reference_t<U>& u) {          { t == u } -> boolean-testable;          { t != u } -> boolean-testable;          { u == t } -> boolean-testable;          { u != t } -> boolean-testable; }; | (3) | (exposition only\*) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| template< class T, class U >  concept __ComparisonCommonTypeWith =      std::common_reference_with<          const std::remove_reference_t<T>&, const std::remove_reference_t<U>&>; |  | (until C++23)  (exposition only\*) |
| template< class T, class U, class C = std::common_reference_t<const T&, const U&> >  concept _ComparisonCommonTypeWithImpl =      std::same_as<std::common_reference_t<const T&, const U&>,                   std::common_reference_t<const U&, const T&>> &&      requires {          requires std::convertible_to<const T&, const C&> ||              std::convertible_to<T, const C&>;          requires std::convertible_to<const U&, const C&> ||              std::convertible_to<U, const C&>;      };  template< class T, class U >  concept __ComparisonCommonTypeWith =     _ComparisonCommonTypeWithImpl<std::remove_cvref_t<T>, std::remove_cvref_t<U>>; |  | (since C++23)  (exposition only\*) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

1) The concept `std::equality_comparable` specifies that the comparison operators `==` and `!=` on `T` reflects equality: `==` yields true if and only if the operands are equal.2) The concept `std::equality_comparable_with` specifies that the comparison operators `==` and `!=` on (possibly mixed) `T` and `U` operands yield results consistent with equality. Comparing mixed operands yields results equivalent to comparing the operands converted to their common type.3) The exposition-only concept `__WeaklyEqualityComparableWith` specifies that an object of type `T` and an object of type `U` can be compared for equality with each other (in either order) using both `==` and `!=`, and the results of the comparisons are consistent.4) The exposition-only concept `__ComparisonCommonTypeWith` specifies that two types share a common type, and a const lvalue or a non-const rvalue(since C++23) of either type is convertible to that common type.

### Semantic requirements

These concepts are modeled only if they are satisfied and all concepts they subsume are modeled.

In the following paragraphs, given an expression `E` and a type `C`, CONVERT_TO<C>(E) is defined as:

|  |  |
| --- | --- |
| - static_cast<C>(std::as_const(E)). | (until C++23) |
| - static_cast<const C&>(std::as_const(E)) if that is a valid expression, - static_cast<const C&>(std::move(E)) otherwise. | (since C++23) |

1) std::equality_comparable<T> is modeled only if, given objects `a` and `b` of type `T`, bool(a == b) is true if and only if `a` and `b` are equal. Together with the requirement that a == b is equality-preserving, this implies that `==` is symmetric and transitive, and further that `==` is reflexive for all objects `a` that are equal to at least one other object.2) std::equality_comparable_with<T, U> is modeled only if, let

- `t` and `t2` be lvalues denoting distinct equal objects of types const std::remove_reference_t<T> and std::remove_cvref_t<T> respectively,
- `u` and `u2` be lvalues denoting distinct equal objects of types const std::remove_reference_t<U> and std::remove_cvref_t<U> respectively,
- `C` be std::common_reference_t<const std::remove_reference_t<T>&, const std::remove_reference_t<U>&>,

the following expression is true:

- bool(t == u) == bool(CONVERT_TO<C>(t2) == CONVERT_TO<C>(u2)).
3) __WeaklyEqualityComparableWith<T, U> is modeled only if given

- `t`, an lvalue of type const std::remove_reference_t<T> and
- `u`, an lvalue of type const std::remove_reference_t<U>,

the following are true:

- t == u, u == t, t != u, u != t have the same domain;
- bool(u == t) == bool(t == u);
- bool(t != u) == !bool(t == u); and
- bool(u != t) == bool(t != u).
4) __WeaklyEqualityComparableWith<T, U> is modeled only if:

|  |  |
| --- | --- |
| The corresponding `common_reference_with` concept is modeled. | (until C++23) |
| Let   - `C` be std::common_reference_t<const T&, const U&>, - `t1` and `t2` be equality-preserving expressions that are lvalues of type std::remove_cvref_t<T>, - `u1` and `u2` be equality-preserving expressions that are lvalues of type std::remove_cvref_t<U>,   the following conditions hold:   - CONVERT_TO<C>(t1) equals CONVERT_TO<C>(t2) if and only if `t1` equals `t2`; and - CONVERT_TO<C>(u1) equals CONVERT_TO<C>(u2) if and only if `u1` equals `u2`. | (since C++23) |

### Equality preservation

Expressions declared in requires expressions of the standard library concepts are required to be equality-preserving (except where stated otherwise).

### Implicit expression variations

A requires expression that uses an expression that is non-modifying for some constant lvalue operand also requires implicit expression variations.

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 18.5.4 Concept `equality_comparable` [concept.equalitycomparable]

- C++20 standard (ISO/IEC 14882:2020):

:   - 18.5.3 Concept `equality_comparable` [concept.equalitycomparable]

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/concepts/equality_comparable&oldid=177894>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 November 2024, at 13:36.