# std::exp(std::complex)

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log10 | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****exp**** | | | | | | |
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
| Defined in header `<complex>` |  |  |
| template< class T >   std::complex<T> exp( const std::complex<T>& z ); |  |  |
|  |  |  |

Compute base-e exponential of z, that is **e** (Euler's number, `2.7182818`) raised to the z power.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex value |

### Return value

If no errors occur, **e** raised to the power of z, \(\small e^z\)ez  
, is returned.

### Error handling and special values

Errors are reported consistent with math_errhandling.

If the implementation supports IEEE floating-point arithmetic,

- std::exp(std::conj(z)) == std::conj(std::exp(z))
- If z is `(±0,+0)`, the result is `(1,+0)`
- If z is `(x,+∞)` (for any finite x), the result is `(NaN,NaN)` and FE_INVALID is raised.
- If z is `(x,NaN)` (for any finite x), the result is `(NaN,NaN)` and FE_INVALID may be raised.
- If z is `(+∞,+0)`, the result is `(+∞,+0)`
- If z is `(-∞,y)` (for any finite y), the result is `+0cis(y)`
- If z is `(+∞,y)` (for any finite nonzero y), the result is `+∞cis(y)`
- If z is `(-∞,+∞)`, the result is `(±0,±0)` (signs are unspecified)
- If z is `(+∞,+∞)`, the result is `(±∞,NaN)` and FE_INVALID is raised (the sign of the real part is unspecified)
- If z is `(-∞,NaN)`, the result is `(±0,±0)` (signs are unspecified)
- If z is `(+∞,NaN)`, the result is `(±∞,NaN)` (the sign of the real part is unspecified)
- If z is `(NaN,+0)`, the result is `(NaN,+0)`
- If z is `(NaN,y)` (for any nonzero y), the result is `(NaN,NaN)` and FE_INVALID may be raised
- If z is `(NaN,NaN)`, the result is `(NaN,NaN)`

where \(\small{\rm cis}(y)\)cis(y) is \(\small \cos(y)+{\rm i}\sin(y)\)cos(y) + i sin(y).

### Notes

The complex exponential function \(\small e^z\)ez  
 for \(\small z = x + {\rm i}y\)z = x+iy equals \(\small e^x {\rm cis}(y)\)ex  
 cis(y), or, \(\small e^x (\cos(y)+{\rm i}\sin(y))\)ex  
 (cos(y) + i sin(y)).

The exponential function is an **entire function** in the complex plane and has no branch cuts.

The following have equivalent results when the real part is 0:

- std::exp(std::complex<float>(0, theta))
- std::complex<float>(cosf(theta), sinf(theta))
- std::polar(1.f, theta)

In this case `exp` can be about 4.5x slower. One of the other forms should be used instead of calling `exp` with an argument whose real part is literal 0. There is no benefit in trying to avoid `exp` with a runtime check of z.real() == 0 though.

### Example

Run this code

```
#include <cmath>
#include <complex>
#include <iostream>
 
int main()
{
   const double pi = std::acos(-1.0);
   const std::complex<double> i(0.0, 1.0);
 
   std::cout << std::fixed << " exp(i * pi) = " << std::exp(i * pi) << '\n';
}

```

Output:

```
exp(i * pi) = (-1.000000,0.000000)

```

### See also

|  |  |
| --- | --- |
| log(std::complex) | complex natural logarithm with the branch cuts along the negative real axis   (function template) |
| expexpfexpl(C++11)(C++11) | returns e raised to the given power (\({\small e^x}\)ex)   (function) |
| exp(std::valarray) | applies the function std::exp to each element of valarray   (function template) |
| polar | constructs a complex number from magnitude and phase angle   (function template) |
| C documentation for cexp | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/exp&oldid=150848>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 April 2023, at 23:24.