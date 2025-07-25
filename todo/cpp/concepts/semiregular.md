# std::semiregular

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Core language concepts | | | | | | same_as(C++20) | | | | | | derived_from(C++20) | | | | | | convertible_to(C++20) | | | | | | common_reference_with(C++20) | | | | | | common_with(C++20) | | | | | | integral(C++20) | | | | | | signed_integral(C++20) | | | | | | unsigned_integral(C++20) | | | | | | floating_point(C++20) | | | | | | swappableswappable_with(C++20)(C++20) | | | | | | destructible(C++20) | | | | | | constructible_from(C++20) | | | | | | default_initializable(C++20) | | | | | | move_constructible(C++20) | | | | | | copy_constructible(C++20) | | | | | | assignable_from(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Comparison concepts | | | | | | equality_comparableequality_comparable_with(C++20)(C++20) | | | | | | totally_orderedtotally_ordered_with(C++20)(C++20) | | | | | | Object concepts | | | | | | movable(C++20) | | | | | | copyable(C++20) | | | | | | ****semiregular****(C++20) | | | | | | regular(C++20) | | | | | | Callable concepts | | | | | | invocableregular_invocable(C++20)(C++20) | | | | | | predicate(C++20) | | | | | | relation(C++20) | | | | | | equivalence_relation(C++20) | | | | | | strict_weak_order(C++20) | | | | | |

|  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Exposition-only concepts | | | | | | **boolean-testable** ﻿(C++20) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<concepts>` |  |  |
| template< class T >  concept semiregular = std::copyable<T> && std::default_initializable<T>; |  | (since C++20) |
|  |  |  |

The `semiregular` concept specifies that a type is both copyable and default constructible. It is satisfied by types that behave similarly to built-in types like int, except that they need not support comparison with `==`.

### Example

Run this code

```
#include <concepts>
#include <iostream>
 
template<std::semiregular T>
// Credit Alexander Stepanov
// concepts are requirements on T
// Requirement on T: T is semiregular
// T a(b); or T a = b; => copy constructor
// T a; => default constructor
// a = b; => assignment
struct Single
{
    T value;
    // Aggregation initialization for Single behaves like following constructor:
    // explicit Single(const T& x) : value(x) {}
 
    // Implicitly declared special member functions behave like following definitions,
    // except that they may have additional properties:
    // Single(const Single& x) : value(x.value) {}
    // Single() {}
    // ~Single() {}
    // Single& operator=(const Single& x) { value = x.value; return *this; }
    // comparison operator is not defined; it is not required by `semiregular` concept
    // bool operator==(Single const& other) const = delete;
};
 
void print(std::semiregular auto x)
{
    std::cout << x.value << '\n';
}
 
int main()
{
    Single<int> myInt1{4};      // aggregate initialization: myInt1.value = 4
    Single<int> myInt2(myInt1); // copy constructor
    Single<int> myInt3;         // default constructor
    myInt3 = myInt2;            // copy assignment operator
//  myInt1 == myInt2;           // Error: operator== is not defined
 
    print(myInt1); // ok: Single<int> is a `semiregular` type
    print(myInt2);
    print(myInt3);
 
}   // Single<int> variables are destroyed here

```

Output:

```
4
4
4

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 18.6 Object concepts [concepts.object]

- C++20 standard (ISO/IEC 14882:2020):

:   - 18.6 Object concepts [concepts.object]

### See also

|  |  |
| --- | --- |
| regular(C++20) | specifies that a type is regular, that is, it is both ****`semiregular`**** and `equality_comparable`   (concept) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/concepts/semiregular&oldid=177904>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 November 2024, at 13:37.