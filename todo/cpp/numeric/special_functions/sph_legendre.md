# std::sph_legendre, std::sph_legendref, std::sph_legendrel

From cppreference.com
< cpp‎ | numeric‎ | special functions
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

Mathematical special functions

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | assoc_laguerreassoc_laguerrefassoc_laguerrel | | | | | | assoc_legendreassoc_legendrefassoc_legendrel | | | | | | betabetafbetal | | | | | | comp_ellint_1comp_ellint_1fcomp_ellint_1l | | | | | | comp_ellint_2comp_ellint_2fcomp_ellint_2l | | | | | | comp_ellint_3comp_ellint_3fcomp_ellint_3l | | | | | | cyl_bessel_icyl_bessel_ifcyl_bessel_il | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cyl_bessel_jcyl_bessel_jfcyl_bessel_jl | | | | | | cyl_bessel_kcyl_bessel_kfcyl_bessel_kl | | | | | | cyl_neumanncyl_neumannfcyl_neumannl | | | | | | ellint_1ellint_1fellint_1l | | | | | | ellint_2ellint_2fellint_2l | | | | | | ellint_3ellint_3fellint_3l | | | | | | expintexpintfexpintl | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hermitehermitefhermitel | | | | | | laguerrelaguerreflaguerrel | | | | | | legendrelegendreflegendrel | | | | | | riemann_zetariemann_zetafriemann_zetal | | | | | | sph_besselsph_besselfsph_bessell | | | | | | ****sph_legendresph_legendrefsph_legendrel**** | | | | | | sph_neumannsph_neumannfsph_neumannl | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cmath>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| float       sph_legendre ( unsigned l, unsigned m, float theta );  double      sph_legendre ( unsigned l, unsigned m, double theta ); long double sph_legendre ( unsigned l, unsigned m, long double theta ); |  | (since C++17)  (until C++23) |
| /\* floating-point-type \*/ sph_legendre( unsigned l, unsigned m,                                          /\* floating-point-type \*/ theta ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       sph_legendref( unsigned l, unsigned m, float theta ); | (2) | (since C++17) |
| long double sph_legendrel( unsigned l, unsigned m, long double theta ); | (3) | (since C++17) |
| Additional overloads |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Integer >  double      sph_legendre ( unsigned l, unsigned m, Integer theta ); | (A) | (since C++17) |
|  |  |  |

1-3) Computes the spherical associated Legendre function of degree l, order m, and polar angle theta. The library provides overloads of `std::sph_legendre` for all cv-unqualified floating-point types as the type of the parameter theta.(since C++23)A) Additional overloads are provided for all integer types, which are treated as double.

### Parameters

|  |  |  |
| --- | --- | --- |
| l | - | degree |
| m | - | order |
| theta | - | polar angle, measured in radians |

### Return value

If no errors occur, returns the value of the spherical associated Legendre function (that is, spherical harmonic with ϕ = 0) of l, m, and theta, where the spherical harmonic function is defined as Ym  
l(theta,ϕ) = (-1)m  
[

|  |
| --- |
| (2l+1)(l-m)! |
| 4π(l+m)! |

]1/2  
Pm  
l(cos(theta))eimϕ  
 where Pm  
l(x) is std::assoc_legendre(l, m, x)) and |m|≤l.

Note that the Condon-Shortley phase term  (-1)m  
 is included in this definition because it is omitted from the definition of Pm  
l in std::assoc_legendre.

### Error handling

Errors may be reported as specified in math_errhandling.

- If the argument is NaN, NaN is returned and domain error is not reported.
- If l≥128, the behavior is implementation-defined.

### Notes

Implementations that do not support C++17, but support ISO 29124:2010, provide this function if `__STDCPP_MATH_SPEC_FUNCS__` is defined by the implementation to a value at least 201003L and if the user defines `__STDCPP_WANT_MATH_SPEC_FUNCS__` before including any standard library headers.

Implementations that do not support ISO 29124:2010 but support TR 19768:2007 (TR1), provide this function in the header `tr1/cmath` and namespace `std::tr1`.

An implementation of the spherical harmonic function is available in boost.math, and it reduces to this function when called with the parameter phi set to zero.

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their argument num of integer type, std::sph_legendre(int_num1, int_num2, num) has the same effect as std::sph_legendre(int_num1, int_num2, static_cast<double>(num)).

### Example

Run this code

```
#include <cmath>
#include <iostream>
#include <numbers>
 
int main()
{
    // spot check for l=3, m=0
    double x = 1.2345;
    std::cout << "Y_3^0(" << x << ") = " << std::sph_legendre(3, 0, x) << '\n';
 
    // exact solution
    std::cout << "exact solution = "
              << 0.25 * std::sqrt(7 / std::numbers::pi)
                  * (5 * std::pow(std::cos(x), 3) - 3 * std::cos(x))
              << '\n';
}

```

Output:

```
Y_3^0(1.2345) = -0.302387
exact solution = -0.302387

```

### See also

|  |  |
| --- | --- |
| assoc_legendreassoc_legendrefassoc_legendrel(C++17)(C++17)(C++17) | associated Legendre polynomials   (function) |

### External links

|  |
| --- |
| Weisstein, Eric W. "Spherical Harmonic." From MathWorld — A Wolfram Web Resource. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/special_functions/sph_legendre&oldid=149663>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 March 2023, at 10:00.