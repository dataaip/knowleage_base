# std::floating_point

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Core language concepts | | | | | | same_as(C++20) | | | | | | derived_from(C++20) | | | | | | convertible_to(C++20) | | | | | | common_reference_with(C++20) | | | | | | common_with(C++20) | | | | | | integral(C++20) | | | | | | signed_integral(C++20) | | | | | | unsigned_integral(C++20) | | | | | | ****floating_point****(C++20) | | | | | | swappableswappable_with(C++20)(C++20) | | | | | | destructible(C++20) | | | | | | constructible_from(C++20) | | | | | | default_initializable(C++20) | | | | | | move_constructible(C++20) | | | | | | copy_constructible(C++20) | | | | | | assignable_from(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Comparison concepts | | | | | | equality_comparableequality_comparable_with(C++20)(C++20) | | | | | | totally_orderedtotally_ordered_with(C++20)(C++20) | | | | | | Object concepts | | | | | | movable(C++20) | | | | | | copyable(C++20) | | | | | | semiregular(C++20) | | | | | | regular(C++20) | | | | | | Callable concepts | | | | | | invocableregular_invocable(C++20)(C++20) | | | | | | predicate(C++20) | | | | | | relation(C++20) | | | | | | equivalence_relation(C++20) | | | | | | strict_weak_order(C++20) | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exposition-only concepts | | | | | | **boolean-testable** ﻿(C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<concepts>` |  |  |
| template< class T >  concept floating_point = std::is_floating_point_v<T>; |  | (since C++20) |
|  |  |  |

The concept floating_point<T> is satisfied if and only if `T` is a floating-point type.

### Example

Run this code

```
#include <concepts>
#include <iostream>
#include <type_traits>
 
constexpr std::floating_point auto x2(std::floating_point auto x)
{
    return x + x;
}
 
constexpr std::integral auto x2(std::integral auto x)
{
    return x << 1;
}
 
int main()
{
    constexpr auto d = x2(1.1);
    static_assert(std::is_same_v<double const, decltype(d)>);
    std::cout << d << '\n';
 
    constexpr auto f = x2(2.2f);
    static_assert(std::is_same_v<float const, decltype(f)>);
    std::cout << f << '\n';
 
    constexpr auto i = x2(444);
    static_assert(std::is_same_v<int const, decltype(i)>);
    std::cout << i << '\n';
}

```

Output:

```
2.2
4.4
888

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 18.4.7 Arithmetic concepts [concepts.arithmetic]

- C++20 standard (ISO/IEC 14882:2020):

:   - 18.4.7 Arithmetic concepts [concepts.arithmetic]

### See also

|  |  |
| --- | --- |
| is_floating_point(C++11) | checks if a type is a floating-point type   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/concepts/floating_point&oldid=177886>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 November 2024, at 13:33.