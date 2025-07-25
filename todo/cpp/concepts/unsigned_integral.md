# std::unsigned_integral

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Core language concepts | | | | | | same_as(C++20) | | | | | | derived_from(C++20) | | | | | | convertible_to(C++20) | | | | | | common_reference_with(C++20) | | | | | | common_with(C++20) | | | | | | integral(C++20) | | | | | | signed_integral(C++20) | | | | | | ****unsigned_integral****(C++20) | | | | | | floating_point(C++20) | | | | | | swappableswappable_with(C++20)(C++20) | | | | | | destructible(C++20) | | | | | | constructible_from(C++20) | | | | | | default_initializable(C++20) | | | | | | move_constructible(C++20) | | | | | | copy_constructible(C++20) | | | | | | assignable_from(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Comparison concepts | | | | | | equality_comparableequality_comparable_with(C++20)(C++20) | | | | | | totally_orderedtotally_ordered_with(C++20)(C++20) | | | | | | Object concepts | | | | | | movable(C++20) | | | | | | copyable(C++20) | | | | | | semiregular(C++20) | | | | | | regular(C++20) | | | | | | Callable concepts | | | | | | invocableregular_invocable(C++20)(C++20) | | | | | | predicate(C++20) | | | | | | relation(C++20) | | | | | | equivalence_relation(C++20) | | | | | | strict_weak_order(C++20) | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exposition-only concepts | | | | | | **boolean-testable** ﻿(C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<concepts>` |  |  |
| template< class T >  concept unsigned_integral = std::integral<T> && !std::signed_integral<T>; |  | (since C++20) |
|  |  |  |

The concept `unsigned_integral<T>` is satisfied if and only if `T` is an integral type and std::is_signed_v<T> is false.

### Notes

`unsigned_integral<T>` may be satisfied by a type that is not an unsigned integer type, for example, bool.

### Example

Run this code

```
#include <concepts>
#include <iostream>
#include <string_view>
 
void test(std::signed_integral auto x, std::string_view text = "")
{
    std::cout << text << " (" + (text == "") << x << ") is a signed integral\n";
}
 
void test(std::unsigned_integral auto x, std::string_view text = "")
{
    std::cout << text << " (" + (text == "") << x << ") is an unsigned integral\n";
}
 
void test(auto x, std::string_view text = "")
{
    std::cout << text << " (" + (text == "") << x << ") is non-integral\n";
}
 
int main()
{
    test(42);               // signed
    test(0xFULL, "0xFULL"); // unsigned
    test('A');              // platform-dependent
    test(true, "true");     // unsigned
    test(4e-2, "4e-2");     // non-integral (hex-float)
    test("∫∫");             // non-integral
}

```

Possible output:

```
(42) is a signed integral
0xFULL (15) is an unsigned integral
(A) is a signed integral
true (1) is an unsigned integral
4e-2 (0.04) is non-integral
(∫∫) is non-integral

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
| is_signed(C++11) | checks if a type is a signed arithmetic type   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/concepts/unsigned_integral&oldid=177885>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 November 2024, at 13:33.