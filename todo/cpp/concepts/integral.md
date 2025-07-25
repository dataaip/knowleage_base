# std::integral

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Core language concepts | | | | | | same_as(C++20) | | | | | | derived_from(C++20) | | | | | | convertible_to(C++20) | | | | | | common_reference_with(C++20) | | | | | | common_with(C++20) | | | | | | ****integral****(C++20) | | | | | | signed_integral(C++20) | | | | | | unsigned_integral(C++20) | | | | | | floating_point(C++20) | | | | | | swappableswappable_with(C++20)(C++20) | | | | | | destructible(C++20) | | | | | | constructible_from(C++20) | | | | | | default_initializable(C++20) | | | | | | move_constructible(C++20) | | | | | | copy_constructible(C++20) | | | | | | assignable_from(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Comparison concepts | | | | | | equality_comparableequality_comparable_with(C++20)(C++20) | | | | | | totally_orderedtotally_ordered_with(C++20)(C++20) | | | | | | Object concepts | | | | | | movable(C++20) | | | | | | copyable(C++20) | | | | | | semiregular(C++20) | | | | | | regular(C++20) | | | | | | Callable concepts | | | | | | invocableregular_invocable(C++20)(C++20) | | | | | | predicate(C++20) | | | | | | relation(C++20) | | | | | | equivalence_relation(C++20) | | | | | | strict_weak_order(C++20) | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exposition-only concepts | | | | | | **boolean-testable** ﻿(C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<concepts>` |  |  |
| template< class T >  concept integral = std::is_integral_v<T>; |  | (since C++20) |
|  |  |  |

The concept integral<T> is satisfied if and only if `T` is an integral type.

### Example

Run this code

```
#include <concepts>
#include <iostream>
 
void print(std::integral auto i)
{
    std::cout << "Integral: " << i << '\n';
}
 
void print(auto x)
{
    std::cout << "Non-integral: " << x << '\n';
}
 
int main()
{
    std::cout << std::boolalpha;
 
    static_assert(std::integral<bool>);
    print(true);
 
    static_assert(std::integral<char>);
    print('o');
 
    static_assert(std::integral<int>);
    print(007);
 
    static_assert( ! std::integral<double> );
    print(2e2);
 
    static_assert( ! std::integral<decltype("")> );
    print("∫∫∫");
}

```

Output:

```
Integral: true
Integral: o
Integral: 7
Non-integral: 200
Non-integral: ∫∫∫

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 18.4.7 Arithmetic concepts [concepts.arithmetic]

- C++20 standard (ISO/IEC 14882:2020):

:   - 18.4.7 Arithmetic concepts [concepts.arithmetic]

### See also

|  |  |
| --- | --- |
| is_integral(C++11) | checks if a type is an integral type   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/concepts/integral&oldid=177883>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 November 2024, at 13:30.