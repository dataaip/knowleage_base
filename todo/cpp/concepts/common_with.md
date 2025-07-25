# std::common_with

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Core language concepts | | | | | | same_as(C++20) | | | | | | derived_from(C++20) | | | | | | convertible_to(C++20) | | | | | | common_reference_with(C++20) | | | | | | ****common_with****(C++20) | | | | | | integral(C++20) | | | | | | signed_integral(C++20) | | | | | | unsigned_integral(C++20) | | | | | | floating_point(C++20) | | | | | | swappableswappable_with(C++20)(C++20) | | | | | | destructible(C++20) | | | | | | constructible_from(C++20) | | | | | | default_initializable(C++20) | | | | | | move_constructible(C++20) | | | | | | copy_constructible(C++20) | | | | | | assignable_from(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Comparison concepts | | | | | | equality_comparableequality_comparable_with(C++20)(C++20) | | | | | | totally_orderedtotally_ordered_with(C++20)(C++20) | | | | | | Object concepts | | | | | | movable(C++20) | | | | | | copyable(C++20) | | | | | | semiregular(C++20) | | | | | | regular(C++20) | | | | | | Callable concepts | | | | | | invocableregular_invocable(C++20)(C++20) | | | | | | predicate(C++20) | | | | | | relation(C++20) | | | | | | equivalence_relation(C++20) | | | | | | strict_weak_order(C++20) | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exposition-only concepts | | | | | | **boolean-testable** ﻿(C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<concepts>` |  |  |
| template< class T, class U >  concept common_with =      std::same_as<std::common_type_t<T, U>, std::common_type_t<U, T>> &&      requires {          static_cast<std::common_type_t<T, U>>(std::declval<T>());          static_cast<std::common_type_t<T, U>>(std::declval<U>());      } &&      std::common_reference_with<          std::add_lvalue_reference_t<const T>,          std::add_lvalue_reference_t<const U>> &&      std::common_reference_with<          std::add_lvalue_reference_t<std::common_type_t<T, U>>,          std::common_reference_t<              std::add_lvalue_reference_t<const T>, std::add_lvalue_reference_t<const U>>>; |  | (since C++20) |
|  |  |  |

The concept `common_with<T, U>` specifies that two types `T` and `U` share a **common type** (as computed by std::common_type_t) to which both can be converted.

### Semantic requirements

T and U model std::common_with<T, U> only if, given equality-preserving expressions `t1`, `t2`, `u1` and `u2` such that decltype((t1)) and decltype((t2)) are both `T` and decltype((u1)) and decltype((u2)) are both `U`,

- std::common_type_t<T, U>(t1) equals std::common_type_t<T, U>(t2) if and only if `t1` equals `t2`; and
- std::common_type_t<T, U>(u1) equals std::common_type_t<T, U>(u2) if and only if `u1` equals `u2`.

In other words, the conversion to the common type must preserve equality.

### Equality preservation

Expressions declared in requires expressions of the standard library concepts are required to be equality-preserving (except where stated otherwise).

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 18.4.6 Concept `common_with` [concept.common]

- C++20 standard (ISO/IEC 14882:2020):

:   - 18.4.6 Concept `common_with` [concept.common]

### See also

|  |  |
| --- | --- |
| common_type(C++11) | determines the common type of a group of types   (class template) |
| common_referencebasic_common_reference(C++20) | determines the common reference type of a group of types   (class template) |
| common_reference_with(C++20) | specifies that two types share a common reference type   (concept) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/concepts/common_with&oldid=177882>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 November 2024, at 13:30.