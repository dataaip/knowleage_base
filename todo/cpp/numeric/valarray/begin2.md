# std::begin(std::valarray)

From cppreference.com
< cpp‎ | numeric‎ | valarray
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

Numerics library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Common mathematical functions | | | | |
| Mathematical special functions (C++17) | | | | |
| Mathematical constants (C++20) | | | | |
| Basic linear algebra algorithms (C++26) | | | | |
| Data-parallel types (SIMD) (C++26) | | | | |
| Floating-point environment (C++11) | | | | |
| Complex numbers | | | | |
| Numeric array (`valarray`) | | | | |
| Pseudo-random number generation | | | | |
| Bit manipulation (C++20) | | | | |
| Factor operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | gcd(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lcm(C++17) | | | | | |
| Interpolations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | midpoint(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lerp(C++20) | | | | | |
| Saturation arithmetic | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | add_sat(C++26) | | | | | | sub_sat(C++26) | | | | | | saturate_cast(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mul_sat(C++26) | | | | | | div_sat(C++26) | | | | | |  | | | | | |
| Generic numeric operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | adjacent_difference | | | | | | partial_sum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

std::valarray

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::valarray | | | | | | valarray::~valarray | | | | | | valarray::operator= | | | | | | [valarray::operator[]](operator_at.html "cpp/numeric/valarray/operator at") | | | | | | valarray::swap | | | | | | valarray::size | | | | | | valarray::resize | | | | | | valarray::sum | | | | | | valarray::min | | | | | | valarray::max | | | | | | valarray::shift | | | | | | valarray::cshift | | | | | | valarray::apply | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::operator+valarray::operator-valarray::operator~valarray::operator! | | | | | | valarray::operator+=valarray::operator-=valarray::operator\*=valarray::operator/=valarray::operator%=valarray::operator&=valarray::operator|=valarray::operator^=valarray::operator<<=valarray::operator>>= | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | ****begin(std::valarray)****(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| template< class T >   /\* see below \*/ begin( valarray<T>& v ); | (1) | (since C++11) |
| template< class T >   /\* see below \*/ begin( const valarray<T>& v ); | (2) | (since C++11) |
|  |  |  |

The overload of std::begin for `valarray` returns an iterator of unspecified type referring to the first element in the numeric array.

1) The return type must

- meet the requirements of mutable LegacyRandomAccessIterator,

|  |  |
| --- | --- |
| - model `contiguous_iterator`, | (since C++20) |

- have a member type `value_type`, which is `T`, and
- have a member type `reference`, which is `T&`.
2) The return type must

- meet the requirements of constant LegacyRandomAccessIterator,

|  |  |
| --- | --- |
| - model `contiguous_iterator`, | (since C++20) |

- have a member type `value_type`, which is `T`, and
- have a member type `reference`, which is `const T&`.

The iterator returned from this function is invalidated when the member function `resize()` is called on v or when the lifetime of v ends, whichever comes first.

### Parameters

|  |  |  |
| --- | --- | --- |
| v | - | a numeric array |

### Return value

Iterator to the first value in the numeric array.

### Exceptions

May throw implementation-defined exceptions.

### Notes

Unlike other functions that take `std::valarray` arguments, `begin()` cannot accept the replacement types (such as the types produced by expression templates) that may be returned from expressions involving valarrays: std::begin(v1 + v2) is not portable, std::begin(std::valarray<T>(v1 + v2)) has to be used instead.

The intent of this function is to allow range for loops to work with valarrays, not to provide container semantics.

### Example

Run this code

```
#include <algorithm>
#include <iostream>
#include <valarray>
 
void show(const std::valarray<int>& v)
{
    std::for_each(std::begin(v), std::end(v), [](int c)
    {
        std::cout << c << ' ';
    });
    std::cout << '\n';
};
 
int main()
{
    const std::valarray<int> x{47, 70, 37, 52, 90, 23, 17, 33, 22, 16, 21, 4};
    const std::valarray<int> y{25, 31, 71, 56, 21, 21, 15, 34, 21, 27, 12, 6};
 
    show(x); 
    show(y); 
 
    const std::valarray<int> z{x + y};
 
    for (char c : z)
        std::cout << c;
}

```

Output:

```
47 70 37 52 90 23 17 33 22 16 21 4 
25 31 71 56 21 21 15 34 21 27 12 6 
Hello, C++!

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2058 | C++11 | 1. `begin()` was required to support replacement types 2. it was unspecified when the returned iterators will be invalidated | 1. not required 2. specified |

### See also

|  |  |
| --- | --- |
| std::end(std::valarray)(C++11) | specializes std::end   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/begin2&oldid=157134>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 August 2023, at 13:55.