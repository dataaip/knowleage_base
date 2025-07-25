# std::derived_from

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Core language concepts | | | | | | same_as(C++20) | | | | | | ****derived_from****(C++20) | | | | | | convertible_to(C++20) | | | | | | common_reference_with(C++20) | | | | | | common_with(C++20) | | | | | | integral(C++20) | | | | | | signed_integral(C++20) | | | | | | unsigned_integral(C++20) | | | | | | floating_point(C++20) | | | | | | swappableswappable_with(C++20)(C++20) | | | | | | destructible(C++20) | | | | | | constructible_from(C++20) | | | | | | default_initializable(C++20) | | | | | | move_constructible(C++20) | | | | | | copy_constructible(C++20) | | | | | | assignable_from(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Comparison concepts | | | | | | equality_comparableequality_comparable_with(C++20)(C++20) | | | | | | totally_orderedtotally_ordered_with(C++20)(C++20) | | | | | | Object concepts | | | | | | movable(C++20) | | | | | | copyable(C++20) | | | | | | semiregular(C++20) | | | | | | regular(C++20) | | | | | | Callable concepts | | | | | | invocableregular_invocable(C++20)(C++20) | | | | | | predicate(C++20) | | | | | | relation(C++20) | | | | | | equivalence_relation(C++20) | | | | | | strict_weak_order(C++20) | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exposition-only concepts | | | | | | **boolean-testable** ﻿(C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<concepts>` |  |  |
| template< class Derived, class Base >  concept derived_from =      std::is_base_of_v<Base, Derived> && std::is_convertible_v<const volatile Derived\*, const volatile Base\*>; |  | (since C++20) |
|  |  |  |

The concept derived_from<Derived, Base> is satisfied if and only if `Base` is a class type that is either `Derived` or a public and unambiguous base of `Derived`, ignoring cv-qualifiers.

Note that this behavior is different to `std::is_base_of` when `Base` is a private or protected base of `Derived`.

### Example

Run this code

```
#include <concepts>
 
class A {};
 
class B : public A {};
 
class C : private A {};
 
// std::derived_from == true only for public inheritance or exact same class
static_assert(std::derived_from<B, B> == true);      // same class: true
static_assert(std::derived_from<int, int> == false); // same primitive type: false
static_assert(std::derived_from<B, A> == true);      // public inheritance: true
static_assert(std::derived_from<C, A> == false);     // private inheritance: false
 
// std::is_base_of == true also for private inheritance
static_assert(std::is_base_of_v<B, B> == true);      // same class: true
static_assert(std::is_base_of_v<int, int> == false); // same primitive type: false
static_assert(std::is_base_of_v<A, B> == true);      // public inheritance: true
static_assert(std::is_base_of_v<A, C> == true);      // private inheritance: true
 
int main() {}

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 18.4.3 Concept `derived_from` [concept.derived]

- C++20 standard (ISO/IEC 14882:2020):

:   - 18.4.3 Concept `derived_from` [concept.derived]

### See also

|  |  |
| --- | --- |
| is_base_of(C++11) | checks if a type is a base of the other type   (class template) |
| is_convertibleis_nothrow_convertible(C++11)(C++20) | checks if a type can be converted to the other type   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/concepts/derived_from&oldid=177879>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 November 2024, at 13:28.