# std::valarray<T>::operator+=,-=,\*=,/=,%=,&=,|=,<<=,>>=

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::valarray | | | | | | valarray::~valarray | | | | | | valarray::operator= | | | | | | [valarray::operator[]](operator_at.html "cpp/numeric/valarray/operator at") | | | | | | valarray::swap | | | | | | valarray::size | | | | | | valarray::resize | | | | | | valarray::sum | | | | | | valarray::min | | | | | | valarray::max | | | | | | valarray::shift | | | | | | valarray::cshift | | | | | | valarray::apply | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | valarray::operator+valarray::operator-valarray::operator~valarray::operator! | | | | | | ****valarray::operator+=valarray::operator-=valarray::operator\*=valarray::operator/=valarray::operator%=valarray::operator&=valarray::operator|=valarray::operator^=valarray::operator<<=valarray::operator>>=**** | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::valarray)(C++11) | | | | | | begin(std::valarray)(C++11) | | | | | | end(std::valarray)(C++11) | | | | | | abs | | | | | | exp | | | | | | log | | | | | | log10 | | | | | | pow | | | | | | sqrt | | | | | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator\*operator/operator%operator+operator-operator^operator&operator|operator<<operator>>operator&&operator|| | | | | | | operator==operator!=operator<operator>operator<=operator>= | | | | | |  | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice_array | | | | | | gslice_array | | | | | | indirect_array | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | slice | | | | | | gslice | | | | | | mask_array | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| valarray<T>& operator+=( const valarray<T>& v );  valarray<T>& operator-=( const valarray<T>& v );  valarray<T>& operator\*=( const valarray<T>& v );  valarray<T>& operator/=( const valarray<T>& v );  valarray<T>& operator%=( const valarray<T>& v );  valarray<T>& operator&=( const valarray<T>& v );  valarray<T>& operator|=( const valarray<T>& v );  valarray<T>& operator^=( const valarray<T>& v );  valarray<T>& operator<<=( const valarray<T>& v ); valarray<T>& operator>>=( const valarray<T>& v ); | (1) |  |
| valarray<T>& operator+=( const T& val );  valarray<T>& operator-=( const T& val );  valarray<T>& operator\*=( const T& val );  valarray<T>& operator/=( const T& val );  valarray<T>& operator%=( const T& val );  valarray<T>& operator&=( const T& val );  valarray<T>& operator|=( const T& val );  valarray<T>& operator^=( const T& val );  valarray<T>& operator<<=( const T& val ); valarray<T>& operator>>=( const T& val ); | (2) |  |
|  |  |  |

Applies compound assignment operators to each element in the numeric array.

1) Each element is assigned value obtained by applying the corresponding operator to the previous value of the element and corresponding element from v. The behavior is undefined if size() != v.size(). The behavior is undefined if any of the values in v is computed during the assignment and depends on any of the values in \*this, that is, the expression on the right side of the assignment refers to a variable in the left side of the assignment.2) Each element is assigned value obtained by applying the corresponding operator to the previous value of the element and the value of val.

### Parameters

|  |  |  |
| --- | --- | --- |
| v | - | another numeric array |
| val | - | a value |

### Return value

\*this

### Exceptions

May throw implementation-defined exceptions.

### Notes

Each of the operators can only be instantiated if the following requirements are met:

- The indicated operator can be applied to type `T`.
- The result value can be unambiguously converted to `T`.

### Example

Run this code

```
#include <iostream>
#include <string_view>
#include <type_traits>
#include <valarray>
 
void o(std::string_view rem, auto const& v, bool nl = false)
{
    if constexpr (std::is_scalar_v<std::decay_t<decltype(v)>>)
        std::cout << rem << " : " << v;
    else
    {
        for (std::cout << rem << " : { "; auto const e : v)
            std::cout << e << ' ';
        std::cout << '}';
    }
    std::cout << (nl ? "\n" : ";  ");
}
 
int main()
{
    std::valarray<int> x, y;
 
    o("x", x = {1, 2, 3, 4}), o("y", y = {4, 3, 2, 1}), o("x += y", x += y, 1);
    o("x", x = {4, 3, 2, 1}), o("y", y = {3, 2, 1, 0}), o("x -= y", x -= y, 1);
    o("x", x = {1, 2, 3, 4}), o("y", y = {5, 4, 3, 2}), o("x *= y", x *= y, 1);
    o("x", x = {1, 3, 4, 7}), o("y", y = {1, 1, 3, 5}), o("x &= y", x &= y, 1);
    o("x", x = {0, 1, 2, 4}), o("y", y = {4, 3, 2, 1}), o("x <<=y", x <<=y, 1);
 
    std::cout << '\n';
 
    o("x", x = {1, 2, 3, 4}), o("x += 5", x += 5, 1);
    o("x", x = {1, 2, 3, 4}), o("x *= 2", x *= 2, 1);
    o("x", x = {8, 6, 4, 2}), o("x /= 2", x /= 2, 1);
    o("x", x = {8, 4, 2, 1}), o("x >>=1", x >>=1, 1);
}

```

Output:

```
x : { 1 2 3 4 };  y : { 4 3 2 1 };  x += y : { 5 5 5 5 }
x : { 4 3 2 1 };  y : { 3 2 1 0 };  x -= y : { 1 1 1 1 }
x : { 1 2 3 4 };  y : { 5 4 3 2 };  x *= y : { 5 8 9 8 }
x : { 1 3 4 7 };  y : { 1 1 3 5 };  x &= y : { 1 1 0 5 }
x : { 0 1 2 4 };  y : { 4 3 2 1 };  x <<=y : { 0 8 8 8 }
 
x : { 1 2 3 4 };  x += 5 : { 6 7 8 9 }
x : { 1 2 3 4 };  x *= 2 : { 2 4 6 8 }
x : { 8 6 4 2 };  x /= 2 : { 4 3 2 1 }
x : { 8 4 2 1 };  x >>=1 : { 4 2 1 0 }

```

### See also

|  |  |
| --- | --- |
| operator+operator-operator~operator! | applies a unary arithmetic operator to each element of the valarray   (public member function) |
| operator+operator-operator\*operator/operator%operator&operator|operator^operator<<operator>>operator&&operator|| | applies binary operators to each element of two valarrays, or a valarray and a value   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/valarray/operator_arith2&oldid=160852>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 October 2023, at 13:54.