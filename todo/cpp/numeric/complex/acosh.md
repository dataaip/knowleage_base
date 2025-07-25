# std::acosh(std::complex)

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sinh | | | | | | cosh | | | | | | tanh | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | asinh(C++11) | | | | | | ****acosh****(C++11) | | | | | | atanh(C++11) | | | | | | |
| Helper types | | | | |
| tuple_size<std::complex>(C++26) | | | | |
| tuple_element<std::complex>(C++26) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<complex>` |  |  |
| template< class T >   complex<T> acosh( const complex<T>& z ); |  | (since C++11) |
|  |  |  |

Computes complex arc hyperbolic cosine of a complex value z with branch cut at values less than 1 along the real axis.

### Parameters

|  |  |  |
| --- | --- | --- |
| z | - | complex value |

### Return value

If no errors occur, the complex arc hyperbolic cosine of z is returned, in the range of a half-strip of nonnegative values along the real axis and in the interval [−iπ; +iπ] along the imaginary axis.

### Error handling and special values

Errors are reported consistent with math_errhandling.

If the implementation supports IEEE floating-point arithmetic,

- std::acosh(std::conj(z)) == std::conj(std::acosh(z)).
- If z is `(±0,+0)`, the result is `(+0,π/2)`.
- If z is `(x,+∞)` (for any finite x), the result is `(+∞,π/2)`.
- If z is `(x,NaN)` (for any[[1]](acosh.html#cite_note-1) finite x), the result is `(NaN,NaN)` and FE_INVALID may be raised.
- If z is `(-∞,y)` (for any positive finite y), the result is `(+∞,π)`.
- If z is `(+∞,y)` (for any positive finite y), the result is `(+∞,+0)`.
- If z is `(-∞,+∞)`, the result is `(+∞,3π/4)`.
- If z is `(±∞,NaN)`, the result is `(+∞,NaN)`.
- If z is `(NaN,y)` (for any finite y), the result is `(NaN,NaN)` and FE_INVALID may be raised.
- If z is `(NaN,+∞)`, the result is `(+∞,NaN)`.
- If z is `(NaN,NaN)`, the result is `(NaN,NaN)`.

1. ↑ per C11 DR471, this holds for non-zero x only. If z is `(0,NaN)`, the result should be `(NaN,π/2)`.

### Notes

Although the C++ standard names this function "complex arc hyperbolic cosine", the inverse functions of the hyperbolic functions are the area functions. Their argument is the area of a hyperbolic sector, not an arc. The correct name is "complex inverse hyperbolic cosine", and, less common, "complex area hyperbolic cosine".

Inverse hyperbolic cosine is a multivalued function and requires a branch cut on the complex plane. The branch cut is conventionally placed at the line segment (-∞,+1) of the real axis.

The mathematical definition of the principal value of the inverse hyperbolic cosine is acosh z = ln(z + √z+1 √z-1).

For any z, acosh(z) = 

|  |
| --- |
| √z-1 |
| √1-z |

 acos(z), or simply i acos(z) in the upper half of the complex plane.

### Example

Run this code

```
#include <complex>
#include <iostream>
 
int main()
{
    std::cout << std::fixed;
    std::complex<double> z1(0.5, 0);
    std::cout << "acosh" << z1 << " = " << std::acosh(z1) << '\n';
 
    std::complex<double> z2(0.5, -0.0);
    std::cout << "acosh" << z2 << " (the other side of the cut) = "
              << std::acosh(z2) << '\n';
 
    // in upper half-plane, acosh = i acos 
    std::complex<double> z3(1, 1), i(0, 1);
    std::cout << "acosh" << z3 << " = " << std::acosh(z3) << '\n'
              << "i*acos" << z3 << " = " << i*std::acos(z3) << '\n';
}

```

Output:

```
acosh(0.500000,0.000000) = (0.000000,-1.047198)
acosh(0.500000,-0.000000) (the other side of the cut) = (0.000000,1.047198)
acosh(1.000000,1.000000) = (1.061275,0.904557)
i*acos(1.000000,1.000000) = (1.061275,0.904557)

```

### See also

|  |  |
| --- | --- |
| acos(std::complex)(C++11) | computes arc cosine of a complex number (\({\small\arccos{z}}\)arccos(z))   (function template) |
| asinh(std::complex)(C++11) | computes area hyperbolic sine of a complex number (\({\small\operatorname{arsinh}{z}}\)arsinh(z))   (function template) |
| atanh(std::complex)(C++11) | computes area hyperbolic tangent of a complex number (\({\small\operatorname{artanh}{z}}\)artanh(z))   (function template) |
| cosh(std::complex) | computes hyperbolic cosine of a complex number (\({\small\cosh{z}}\)cosh(z))   (function template) |
| acoshacoshfacoshl(C++11)(C++11)(C++11) | computes the inverse hyperbolic cosine (\({\small\operatorname{arcosh}{x}}\)arcosh(x))   (function) |
| C documentation for cacosh | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/complex/acosh&oldid=159322>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 September 2023, at 04:53.