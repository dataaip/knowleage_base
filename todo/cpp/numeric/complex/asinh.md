# std::asinh(std::complex)

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asin(C++11) | | | | | | acos(C++11) | | | | | | atan(C++11) | | | | | | |
| Hyperbolic functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****asinh****(C++11) | | | | | | acosh(C++11) | | | | | | atanh(C++11) | | | | | | |
| Helper types | | | | |
| tuple_size<std::complex>(C++26) | | | | |
| tuple_element<std::complex>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex>` |  |  |
| template< class T >   complex<T> asinh( const complex<T>& z ); |  | (since C++11) |
|  |  |  |

Computes complex arc hyperbolic sine of a complex value z with branch cuts outside the interval [−i; +i] along the imaginary axis.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex value |

### Return value

If no errors occur, the complex arc hyperbolic sine of z is returned, in the range of a strip mathematically unbounded along the real axis and in the interval [−iπ/2; +iπ/2] along the imaginary axis.

### Error handling and special values

Errors are reported consistent with math_errhandling.

If the implementation supports IEEE floating-point arithmetic,

- std::asinh(std::conj(z)) == std::conj(std::asinh(z))
- std::asinh(-z) == -std::asinh(z)
- If z is `(+0,+0)`, the result is `(+0,+0)`
- If z is `(x,+∞)` (for any positive finite x), the result is `(+∞,π/2)`
- If z is `(x,NaN)` (for any finite x), the result is `(NaN,NaN)` and FE_INVALID may be raised
- If z is `(+∞,y)` (for any positive finite y), the result is `(+∞,+0)`
- If z is `(+∞,+∞)`, the result is `(+∞,π/4)`
- If z is `(+∞,NaN)`, the result is `(+∞,NaN)`
- If z is `(NaN,+0)`, the result is `(NaN,+0)`
- If z is `(NaN,y)` (for any finite nonzero y), the result is `(NaN,NaN)` and FE_INVALID may be raised
- If z is `(NaN,+∞)`, the result is `(±∞,NaN)` (the sign of the real part is unspecified)
- If z is `(NaN,NaN)`, the result is `(NaN,NaN)`

### Notes

Although the C++ standard names this function "complex arc hyperbolic sine", the inverse functions of the hyperbolic functions are the area functions. Their argument is the area of a hyperbolic sector, not an arc. The correct name is "complex inverse hyperbolic sine", and, less common, "complex area hyperbolic sine".

Inverse hyperbolic sine is a multivalued function and requires a branch cut on the complex plane. The branch cut is conventionally placed at the line segments (-**i**∞,-**i**) and (**i**,**i**∞) of the imaginary axis.

The mathematical definition of the principal value of the inverse hyperbolic sine is asinh z = ln(z + √1+z2  
).

For any z, asinh(z) = 

|  |
| --- |
| asin(iz) |
| i |

.

### Example

Run this code

```
#include <complex>
#include <iostream>
 
int main()
{
    std::cout << std::fixed;
    std::complex<double> z1(0.0, -2.0);
    std::cout << "asinh" << z1 << " = " << std::asinh(z1) << '\n';
 
    std::complex<double> z2(-0.0, -2);
    std::cout << "asinh" << z2 << " (the other side of the cut) = "
              << std::asinh(z2) << '\n';
 
    // for any z, asinh(z) = asin(iz) / i
    std::complex<double> z3(1.0, 2.0);
    std::complex<double> i(0.0, 1.0);
    std::cout << "asinh" << z3 << " = " << std::asinh(z3) << '\n'
              << "asin" << z3 * i << " / i = " << std::asin(z3 * i) / i << '\n';
}

```

Output:

```
asinh(0.000000,-2.000000) = (1.316958,-1.570796)
asinh(-0.000000,-2.000000) (the other side of the cut) = (-1.316958,-1.570796)
asinh(1.000000,2.000000) = (1.469352,1.063440)
asin(-2.000000,1.000000) / i = (1.469352,1.063440)

```

### See also

|  |  |
| --- | --- |
| acosh(std::complex)(C++11) | computes area hyperbolic cosine of a complex number (\({\small\operatorname{arcosh}{z}}\)arcosh(z))   (function template) |
| atanh(std::complex)(C++11) | computes area hyperbolic tangent of a complex number (\({\small\operatorname{artanh}{z}}\)artanh(z))   (function template) |
| sinh(std::complex) | computes hyperbolic sine of a complex number (\({\small\sinh{z}}\)sinh(z))   (function template) |
| asinhasinhfasinhl(C++11)(C++11)(C++11) | computes the inverse hyperbolic sine (\({\small\operatorname{arsinh}{x}}\)arsinh(x))   (function) |
| C documentation for casinh | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/asinh&oldid=150827>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 April 2023, at 09:03.