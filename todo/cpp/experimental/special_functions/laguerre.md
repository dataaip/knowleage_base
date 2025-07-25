# std::laguerre, std::laguerref, std::laguerrel

From cppreference.com
< cpp‎ | experimental‎ | special functions
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Mathematical special functions

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | assoc_laguerreassoc_laguerrefassoc_laguerrel | | | | | | assoc_legendreassoc_legendrefassoc_legendrel | | | | | | betabetafbetal | | | | | | comp_ellint_1comp_ellint_1fcomp_ellint_1l | | | | | | comp_ellint_2comp_ellint_2fcomp_ellint_2l | | | | | | comp_ellint_3comp_ellint_3fcomp_ellint_3l | | | | | | cyl_bessel_icyl_bessel_ifcyl_bessel_il") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cyl_bessel_jcyl_bessel_jfcyl_bessel_jl") | | | | | | cyl_bessel_kcyl_bessel_kfcyl_bessel_kl") | | | | | | cyl_neumanncyl_neumannfcyl_neumannl") | | | | | | ellint_1ellint_1fellint_1l") | | | | | | ellint_2ellint_2fellint_2l") | | | | | | ellint_3ellint_3fellint_3l") | | | | | | expintexpintfexpintl | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hermitehermitefhermitel | | | | | | ****laguerrelaguerreflaguerrel**** | | | | | | legendrelegendreflegendrel | | | | | | riemann_zetariemann_zetafriemann_zetal | | | | | | sph_besselsph_besselfsph_bessell") | | | | | | sph_legendresph_legendrefsph_legendrel") | | | | | | sph_neumannsph_neumannfsph_neumannl") | | | | | |

|  |  |  |
| --- | --- | --- |
| double      laguerre( unsigned int n, double x );  double      laguerre( unsigned int n, float x );  double      laguerre( unsigned int n, long double x );  float       laguerref( unsigned int n, float x ); long double laguerrel( unsigned int n, long double x ); | (1) |  |
| double      laguerre( unsigned int n, IntegralType x ); | (2) |  |
|  |  |  |

1) Computes the non-associated Laguerre polynomials of the degree n and argument x.2) A set of overloads or a function template accepting an argument of any integral type. Equivalent to (1) after casting the argument to double.

As all special functions, `laguerre` is only guaranteed to be available in `<cmath>` if `__STDCPP_MATH_SPEC_FUNCS__` is defined by the implementation to a value at least 201003L and if the user defines `__STDCPP_WANT_MATH_SPEC_FUNCS__` before including any standard library headers.

### Parameters

|  |  |  |
| --- | --- | --- |
| n | - | the degree of the polynomial, a value of unsigned integer type |
| x | - | the argument, a value of a floating-point or integral type |

### Return value

If no errors occur, value of the nonassociated Laguerre polynomial of `x`, that is 

|  |
| --- |
| **e**x |
| n! |

|  |
| --- |
| dn |
| dxn |

(xn  
**e**-x), is returned.

### Error handling

Errors may be reported as specified in math_errhandling.

- If the argument is NaN, NaN is returned and domain error is not reported.
- If x is negative, a domain error may occur.
- If n is greater or equal than 128, the behavior is implementation-defined.

### Notes

Implementations that do not support TR 29124 but support TR 19768, provide this function in the header `tr1/cmath` and namespace `std::tr1`.

An implementation of this function is also available in boost.math.

The Laguerre polynomials are the polynomial solutions of the equation xy,,  
 + (1 - x)y,  
 + ny = 0.

The first few are:

- laguerre(0, x) = 1.
- laguerre(1, x) = -x + 1.
- laguerre(2, x) = 

  |  |
  | --- |
  | 1 |
  | 2 |

  [x2  
   - 4x + 2].
- laguerre(3, x) = 

  |  |
  | --- |
  | 1 |
  | 6 |

  [-x3  
   - 9x2  
   - 18x + 6].

### Example

(works as shown with gcc 6.0)

Run this code

```
#define __STDCPP_WANT_MATH_SPEC_FUNCS__ 1
#include <cmath>
#include <iostream>
 
double L1(double x)
{
    return -x + 1;
}
 
double L2(double x)
{
    return 0.5 * (x * x - 4 * x + 2);
}
 
int main()
{
    // spot-checks
    std::cout << std::laguerre(1, 0.5) << '=' << L1(0.5) << '\n'
              << std::laguerre(2, 0.5) << '=' << L2(0.5) << '\n';
}

```

Output:

```
0.5=0.5
0.125=0.125

```

### See also

|  |  |
| --- | --- |
| assoc_laguerreassoc_laguerrefassoc_laguerrel | associated Laguerre polynomials   (function) |

### External links

Weisstein, Eric W. "Laguerre Polynomial." From MathWorld--A Wolfram Web Resource.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/special_functions/laguerre&oldid=158800>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 September 2023, at 10:42.