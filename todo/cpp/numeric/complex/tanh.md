# std::tanh(std::complex)

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sinh | | | | | | cosh | | | | | | ****tanh**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asinh(C++11) | | | | | | acosh(C++11) | | | | | | atanh(C++11) | | | | | | |
| Helper types | | | | |
| tuple_size<std::complex>(C++26) | | | | |
| tuple_element<std::complex>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex>` |  |  |
| template< class T >   complex<T> tanh( const complex<T>& z ); |  | (since C++11) |
|  |  |  |

Computes complex hyperbolic tangent of a complex value z.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex value |

### Return value

If no errors occur, complex hyperbolic tangent of z is returned.

### Error handling and special values

Errors are reported consistent with math_errhandling.

If the implementation supports IEEE floating-point arithmetic,

- std::tanh(std::conj(z)) == std::conj(std::tanh(z)).
- std::tanh(-z) == -std::tanh(z).
- If z is `(+0,+0)`, the result is `(+0,+0)`.
- If z is `(x,+∞)` (for any[[1]](tanh.html#cite_note-1) finite x), the result is `(NaN,NaN)` and FE_INVALID is raised.
- If z is `(x,NaN)` (for any[[2]](tanh.html#cite_note-2) finite x), the result is `(NaN,NaN)` and FE_INVALID may be raised.
- If z is `(+∞,y)` (for any finite positive y), the result is `(1,+0)`.
- If z is `(+∞,+∞)`, the result is `(1,±0)` (the sign of the imaginary part is unspecified).
- If z is `(+∞,NaN)`, the result is `(1,±0)` (the sign of the imaginary part is unspecified).
- If z is `(NaN,+0)`, the result is `(NaN,+0)`.
- If z is `(NaN,y)` (for any non-zero y), the result is `(NaN,NaN)` and FE_INVALID may be raised.
- If z is `(NaN,NaN)`, the result is `(NaN,NaN)`.

1. ↑ per C11 DR471, this only holds for non-zero x. If `z` is `(0,∞)`, the result should be `(0,NaN)`.
2. ↑ per C11 DR471, this only holds for non-zero x. If `z` is `(0,NaN)`, the result should be `(0,NaN)`.

### Notes

Mathematical definition of hyperbolic tangent is tanh z = 

|  |
| --- |
| ez -e-z |
| ez +e-z |

.

Hyperbolic tangent is an analytical function on the complex plane and has no branch cuts. It is periodic with respect to the imaginary component, with period πi, and has poles of the first order along the imaginary line, at coordinates (0, π(1/2 + n)). However no common floating-point representation is able to represent π/2 exactly, thus there is no value of the argument for which a pole error occurs.

### Example

Run this code

```
#include <cmath>
#include <complex>
#include <iostream>
 
int main()
{
    std::cout << std::fixed;
    std::complex<double> z(1.0, 0.0); // behaves like real tanh along the real line
    std::cout << "tanh" << z << " = " << std::tanh(z)
              << " (tanh(1) = " << std::tanh(1) << ")\n";
 
    std::complex<double> z2(0.0, 1.0); // behaves like tangent along the imaginary line
    std::cout << "tanh" << z2 << " = " << std::tanh(z2)
              << " ( tan(1) = " << std::tan(1) << ")\n";
}

```

Output:

```
tanh(1.000000,0.000000) = (0.761594,0.000000) (tanh(1) = 0.761594)
tanh(0.000000,1.000000) = (0.000000,1.557408) ( tan(1) = 1.557408)

```

### See also

|  |  |
| --- | --- |
| sinh(std::complex) | computes hyperbolic sine of a complex number (\({\small\sinh{z}}\)sinh(z))   (function template) |
| cosh(std::complex) | computes hyperbolic cosine of a complex number (\({\small\cosh{z}}\)cosh(z))   (function template) |
| atanh(std::complex)(C++11) | computes area hyperbolic tangent of a complex number (\({\small\operatorname{artanh}{z}}\)artanh(z))   (function template) |
| tanhtanhftanhl(C++11)(C++11) | computes hyperbolic tangent (\({\small\tanh{x}}\)tanh(x))   (function) |
| tanh(std::valarray) | applies the function std::tanh to each element of valarray   (function template) |
| C documentation for ctanh | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/tanh&oldid=159323>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 September 2023, at 05:05.