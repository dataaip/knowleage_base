# std::assoc_laguerre, std::assoc_laguerref, std::assoc_laguerrel

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****assoc_laguerreassoc_laguerrefassoc_laguerrel**** | | | | | | assoc_legendreassoc_legendrefassoc_legendrel | | | | | | betabetafbetal | | | | | | comp_ellint_1comp_ellint_1fcomp_ellint_1l | | | | | | comp_ellint_2comp_ellint_2fcomp_ellint_2l | | | | | | comp_ellint_3comp_ellint_3fcomp_ellint_3l | | | | | | cyl_bessel_icyl_bessel_ifcyl_bessel_il | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cyl_bessel_jcyl_bessel_jfcyl_bessel_jl | | | | | | cyl_bessel_kcyl_bessel_kfcyl_bessel_kl | | | | | | cyl_neumanncyl_neumannfcyl_neumannl | | | | | | ellint_1ellint_1fellint_1l | | | | | | ellint_2ellint_2fellint_2l | | | | | | ellint_3ellint_3fellint_3l | | | | | | expintexpintfexpintl | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hermitehermitefhermitel | | | | | | laguerrelaguerreflaguerrel | | | | | | legendrelegendreflegendrel | | | | | | riemann_zetariemann_zetafriemann_zetal | | | | | | sph_besselsph_besselfsph_bessell | | | | | | sph_legendresph_legendrefsph_legendrel | | | | | | sph_neumannsph_neumannfsph_neumannl | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cmath>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| float       assoc_laguerre ( unsigned int n, unsigned int m, float x );  double      assoc_laguerre ( unsigned int n, unsigned int m, double x ); long double assoc_laguerre ( unsigned int n, unsigned int m, long double x ); |  | (since C++17)  (until C++23) |
| /\* floating-point-type \*/ assoc_laguerre( unsigned int n, unsigned int m,                                            /\* floating-point-type \*/ x ); |  | (since C++23) |
|  |  |  |
| --- | --- | --- |
| float       assoc_laguerref( unsigned int n, unsigned int m, float x ); | (2) | (since C++17) |
| long double assoc_laguerrel( unsigned int n, unsigned int m, long double x ); | (3) | (since C++17) |
| Additional overloads |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Integer >  double      assoc_laguerre ( unsigned int n, unsigned int m, Integer x ); | (A) | (since C++17) |
|  |  |  |

1-3) Computes the associated Laguerre polynomials of the degree n, order m, and argument x. The library provides overloads of `std::assoc_laguerre` for all cv-unqualified floating-point types as the type of the parameter x.(since C++23)A) Additional overloads are provided for all integer types, which are treated as double.

### Parameters

|  |  |  |
| --- | --- | --- |
| n | - | the degree of the polynomial, an unsigned integer value |
| m | - | the order of the polynomial, an unsigned integer value |
| x | - | the argument, a floating-point or integer value |

### Return value

If no errors occur, value of the associated Laguerre polynomial of x, that is \((-1)^m \: \frac{ \mathsf{d} ^ m}{ \mathsf{d}x ^ m} \, \mathsf{L}_{n+m}(x)\)(-1)m  

|  |
| --- |
| dm |
| dxm |

Ln+m(x), is returned (where \(\mathsf{L}_{n+m}(x)\)Ln+m(x) is the unassociated Laguerre polynomial, std::laguerre(n + m, x)).

### Error handling

Errors may be reported as specified in math_errhandling

- If the argument is NaN, NaN is returned and domain error is not reported
- If x is negative, a domain error may occur
- If n or m is greater or equal to 128, the behavior is implementation-defined

### Notes

Implementations that do not support C++17, but support ISO 29124:2010, provide this function if `__STDCPP_MATH_SPEC_FUNCS__` is defined by the implementation to a value at least 201003L and if the user defines `__STDCPP_WANT_MATH_SPEC_FUNCS__` before including any standard library headers.

Implementations that do not support ISO 29124:2010 but support TR 19768:2007 (TR1), provide this function in the header `tr1/cmath` and namespace `std::tr1`.

An implementation of this function is also available in boost.math.

The associated Laguerre polynomials are the polynomial solutions of the equation \(x\ddot{y} + (m+1-x)\dot{y} + ny = 0\)xy,,  
+(m+1-x)y,  
+ny = 0.

The first few are:

| Function | Polynomial |
| --- | --- |
| assoc_laguerre(0, m, x) | 1 |
| assoc_laguerre(1, m, x) | -x + m + 1 |
| assoc_laguerre(2, m, x) | |  | | --- | | 1 | | 2 |  [x2  - 2(m + 2)x + (m + 1)(m + 2)] |
| assoc_laguerre(3, m, x) | |  | | --- | | 1 | | 6 |  [-x3  - 3(m + 3)x2  - 3(m + 2)(m + 3)x + (m + 1)(m + 2)(m + 3)] |

The additional overloads are not required to be provided exactly as (A). They only need to be sufficient to ensure that for their argument num of integer type, std::assoc_laguerre(int_num1, int_num2, num) has the same effect as std::assoc_laguerre(int_num1, int_num2, static_cast<double>(num)).

### Example

Run this code

```
#include <cmath>
#include <iostream>
 
double L1(unsigned m, double x)
{
    return -x + m + 1;
}
 
double L2(unsigned m, double x)
{
    return 0.5 * (x * x - 2 * (m + 2) * x + (m + 1) * (m + 2));
}
 
int main()
{
    // spot-checks
    std::cout << std::assoc_laguerre(1, 10, 0.5) << '=' << L1(10, 0.5) << '\n'
              << std::assoc_laguerre(2, 10, 0.5) << '=' << L2(10, 0.5) << '\n';
}

```

Output:

```
10.5=10.5
60.125=60.125

```

### See also

|  |  |
| --- | --- |
| laguerrelaguerreflaguerrel(C++17)(C++17)(C++17) | Laguerre polynomials   (function) |

### External links

|  |
| --- |
| Weisstein, Eric W. "Associated Laguerre Polynomial." From MathWorld — A Wolfram Web Resource. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/special_functions/assoc_laguerre&oldid=149661>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 March 2023, at 09:38.