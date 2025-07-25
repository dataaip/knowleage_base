# std::asin(std::complex)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator+operator- | | | | | | operator+operator-operator\*operator/ | | | | | | operator==operator!=(until C++20) | | | | | | operator<<operator>> | | | | | | get(std::complex)(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | real | | | | | | imag | | | | | | abs | | | | | | arg | | | | | | norm | | | | | | conj | | | | | | proj(C++11) | | | | | | polar | | | | | | operator""ioperator""ifoperator""il(C++14)(C++14)(C++14) | | | | | |
| Exponential functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log10 | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | |
| Power functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pow | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | |
| Trigonometric functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****asin****(C++11) | | | | | | acos(C++11) | | | | | | atan(C++11) | | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asinh(C++11) | | | | | | acosh(C++11) | | | | | | atanh(C++11) | | | | | | |
| Helper types | | | | |
| tuple_size<std::complex>(C++26) | | | | |
| tuple_element<std::complex>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex>` |  |  |
| template< class T >  std::complex<T> asin( const std::complex<T>& z ); |  | (since C++11) |
|  |  |  |

Computes complex arc sine of a complex value z. Branch cut exists outside the interval [−1, +1] along the real axis.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex value |

### Return value

If no errors occur, complex arc sine of z is returned, in the range of a strip unbounded along the imaginary axis and in the interval [−π/2, +π/2] along the real axis.

Errors and special cases are handled as if the operation is implemented by `-i * std::asinh(i * z)`, where `i` is the imaginary unit.

### Notes

Inverse sine (or arc sine) is a multivalued function and requires a branch cut on the complex plane. The branch cut is conventionally placed at the line segments (-∞,-1) and (1,∞) of the real axis.

The mathematical definition of the principal value of arc sine is \(\small \arcsin z = -{\rm i}\ln({\rm i}z+\sqrt{1-z^2})\)arcsin z = -**i**ln(**i**z + √1-z2  
).

For any z, \(\small{ \arcsin(z) = \arccos(-z) - \frac{\pi}{2} }\)asin(z) = acos(-z) - 

|  |
| --- |
| π |
| 2 |

.

### Example

Run this code

```
#include <cmath>
#include <complex>
#include <iostream>
 
int main()
{
    std::cout << std::fixed;
    std::complex<double> z1(-2.0, 0.0);
    std::cout << "asin" << z1 << " = " << std::asin(z1) << '\n';
 
    std::complex<double> z2(-2.0, -0.0);
    std::cout << "asin" << z2 << " (the other side of the cut) = "
              << std::asin(z2) << '\n';
 
    // for any z, asin(z) = acos(−z) − pi / 2
    const double pi = std::acos(-1);
    std::complex<double> z3 = std::acos(z2) - pi / 2;
    std::cout << "sin(acos" << z2 << " - pi / 2) = " << std::sin(z3) << '\n';
}

```

Output:

```
asin(-2.000000,0.000000) = (-1.570796,1.316958)
asin(-2.000000,-0.000000) (the other side of the cut) = (-1.570796,-1.316958)
sin(acos(-2.000000,-0.000000) - pi / 2) = (2.000000,0.000000)

```

### See also

|  |  |
| --- | --- |
| acos(std::complex)(C++11) | computes arc cosine of a complex number (\({\small\arccos{z}}\)arccos(z))   (function template) |
| atan(std::complex)(C++11) | computes arc tangent of a complex number (\({\small\arctan{z}}\)arctan(z))   (function template) |
| sin(std::complex) | computes sine of a complex number (\({\small\sin{z}}\)sin(z))   (function template) |
| asinasinfasinl(C++11)(C++11) | computes arc sine (\({\small\arcsin{x}}\)arcsin(x))   (function) |
| asin(std::valarray) | applies the function std::asin to each element of valarray   (function template) |
| C documentation for casin | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/asin&oldid=150826>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 April 2023, at 08:54.