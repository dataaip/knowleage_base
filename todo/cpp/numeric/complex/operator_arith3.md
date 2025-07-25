# operator+,-,\*,/ (std::complex)

From cppreference.com
< cpp‎ | numeric‎ | complex
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

std::complex

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex::complex | | | | | | complex::operator= | | | | | | complex::real | | | | | | complex::imag | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | complex::operator+=complex::operator-=complex::operator\*=complex::operator/= | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator- | | | | | | ****operator+operator-operator\*operator/**** | | | | | | operator==operator!=(until C++20) | | | | | | operator<<operator>> | | | | | | get(std::complex)(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | real | | | | | | imag | | | | | | abs | | | | | | arg | | | | | | norm | | | | | | conj | | | | | | proj(C++11) | | | | | | polar | | | | | | operator""ioperator""ifoperator""il(C++14)(C++14)(C++14) | | | | | |
| Exponential functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log10 | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | |
| Power functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pow | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asin(C++11) | | | | | | acos(C++11) | | | | | | atan(C++11) | | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asinh(C++11) | | | | | | acosh(C++11) | | | | | | atanh(C++11) | | | | | | |
| Helper types | | | | |
| tuple_size<std::complex>(C++26) | | | | |
| tuple_element<std::complex>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class T >  std::complex<T> operator+( const std::complex<T>& lhs, const std::complex<T>& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator+( const std::complex<T>& lhs, const std::complex<T>& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| template< class T >  std::complex<T> operator+( const std::complex<T>& lhs, const T& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator+( const std::complex<T>& lhs, const T& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| template< class T >  std::complex<T> operator+( const T& lhs, const std::complex<T>& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator+( const T& lhs, const std::complex<T>& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| template< class T >  std::complex<T> operator-( const std::complex<T>& lhs, const std::complex<T>& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator-( const std::complex<T>& lhs, const std::complex<T>& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (5) |  |
| template< class T >  std::complex<T> operator-( const std::complex<T>& lhs, const T& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator-( const std::complex<T>& lhs, const T& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (6) |  |
| template< class T >  std::complex<T> operator-( const T& lhs, const std::complex<T>& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator-( const T& lhs, const std::complex<T>& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (7) |  |
| template< class T >  std::complex<T> operator\*( const std::complex<T>& lhs, const std::complex<T>& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator\*( const std::complex<T>& lhs, const std::complex<T>& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (8) |  |
| template< class T >  std::complex<T> operator\*( const std::complex<T>& lhs, const T& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator\*( const std::complex<T>& lhs, const T& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (9) |  |
| template< class T >  std::complex<T> operator\*( const T& lhs, const std::complex<T>& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator\*( const T& lhs, const std::complex<T>& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (10) |  |
| template< class T >  std::complex<T> operator/( const std::complex<T>& lhs, const std::complex<T>& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator/( const std::complex<T>& lhs, const std::complex<T>& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (11) |  |
| template< class T >  std::complex<T> operator/( const std::complex<T>& lhs, const T& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator/( const std::complex<T>& lhs, const T& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  | (12) |  |
| template< class T >  std::complex<T> operator/( const T& lhs, const std::complex<T>& rhs ); |  | (until C++20) |
| template< class T >  constexpr std::complex<T> operator/( const T& lhs, const std::complex<T>& rhs ); |  | (since C++20) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Implements the binary operators for complex arithmetic and for mixed complex/scalar arithmetic. Scalar arguments are treated as complex numbers with the real part equal to the argument and the imaginary part set to zero.

1-3) Returns the sum of its arguments.4-6) Returns the result of subtracting rhs from lhs.7-9) Multiplies its arguments.10-12) Divides lhs by rhs.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | the arguments: either both complex numbers or one complex and one scalar of matching type (float, double, long double) |

### Return value

1-3) std::complex<T>(lhs) += rhs4-6) std::complex<T>(lhs) -= rhs7-9) std::complex<T>(lhs) \*= rhs10-12) std::complex<T>(lhs) /= rhs

### Notes

Because template argument deduction does not consider implicit conversions, these operators cannot be used for mixed integer/complex arithmetic. In all cases, the scalar must have the same type as the underlying type of the complex number.

The GCC flag "-fcx-limited-range" (included by "-ffast-math") changes the behavior of complex multiply/division by removing checks for floating point edge cases. This impacts loop vectorization.

### Example

Run this code

```
#include <complex>
#include <iostream>
 
int main()
{
    std::complex<double> c2(2.0, 0.0);
    std::complex<double> ci(0.0, 1.0);
 
    std::cout << ci << " + " << c2 << " = " << ci + c2 << '\n'
              << ci << " * " << ci << " = " << ci * ci << '\n'
              << ci << " + " << c2 << " / " << ci << " = " << ci + c2 / ci << '\n'
              << 1  << " / " << ci << " = " << 1.0 / ci << '\n';
 
//    std::cout << 1.0f / ci; // compile error
//    std::cout << 1 / ci; // compile error
}

```

Output:

```
(0,1) + (2,0) = (2,1)
(0,1) * (0,1) = (-1,0)
(0,1) + (2,0) / (0,1) = (0,-1)
1 / (0,1) = (0,-1)

```

### See also

|  |  |
| --- | --- |
| operator+=operator-=operator\*=operator/= | compound assignment of two complex numbers or a complex and a scalar   (public member function) |
| operator+operator- | applies unary operators to complex numbers   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/operator_arith3&oldid=154493>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 July 2023, at 12:51.