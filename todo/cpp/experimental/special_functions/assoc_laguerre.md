# std::assoc_laguerre, std::assoc_laguerref, std::assoc_laguerrel

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****assoc_laguerreassoc_laguerrefassoc_laguerrel**** | | | | | | assoc_legendreassoc_legendrefassoc_legendrel | | | | | | betabetafbetal | | | | | | comp_ellint_1comp_ellint_1fcomp_ellint_1l | | | | | | comp_ellint_2comp_ellint_2fcomp_ellint_2l | | | | | | comp_ellint_3comp_ellint_3fcomp_ellint_3l | | | | | | cyl_bessel_icyl_bessel_ifcyl_bessel_il") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cyl_bessel_jcyl_bessel_jfcyl_bessel_jl") | | | | | | cyl_bessel_kcyl_bessel_kfcyl_bessel_kl") | | | | | | cyl_neumanncyl_neumannfcyl_neumannl") | | | | | | ellint_1ellint_1fellint_1l") | | | | | | ellint_2ellint_2fellint_2l") | | | | | | ellint_3ellint_3fellint_3l") | | | | | | expintexpintfexpintl | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hermitehermitefhermitel | | | | | | laguerrelaguerreflaguerrel | | | | | | legendrelegendreflegendrel | | | | | | riemann_zetariemann_zetafriemann_zetal | | | | | | sph_besselsph_besselfsph_bessell") | | | | | | sph_legendresph_legendrefsph_legendrel") | | | | | | sph_neumannsph_neumannfsph_neumannl") | | | | | |

|  |  |  |
| --- | --- | --- |
| double      assoc_laguerre ( unsigned int n, unsigned int m, double x );  double      assoc_laguerre ( unsigned int n, unsigned int m, float x );  double      assoc_laguerre ( unsigned int n, unsigned int m, long double x );  float       assoc_laguerref( unsigned int n, unsigned int m, float x ); long double assoc_laguerrel( unsigned int n, unsigned int m, long double x ); | (1) |  |
| double      assoc_laguerre ( unsigned int n, unsigned int m, IntegralType x ); | (2) |  |
|  |  |  |

1) Computes the associated Laguerre polynomials of the degree n, order m, and argument x.2) A set of overloads or a function template accepting an argument of any integral type. Equivalent to (1) after casting the argument to double.

As all special functions, `assoc_laguerre` is only guaranteed to be available in `<cmath>` if `__STDCPP_MATH_SPEC_FUNCS__` is defined by the implementation to a value at least 201003L and if the user defines `__STDCPP_WANT_MATH_SPEC_FUNCS__` before including any standard library headers.

### Parameters

|  |  |  |
| --- | --- | --- |
| n | - | the degree of the polynomial, a value of unsigned integer type |
| m | - | the order of the polynomial, a value of unsigned integer type |
| x | - | the argument, a value of a floating-point or integral type |

### Return value

If no errors occur, value of the associated Laguerre polynomial of x, that is (-1)m  

|  |
| --- |
| dm |
| dxm |

Ln + m(x), is returned (where Ln + m(x) is the unassociated Laguerre polynomial, std::laguerre(n + m, x)).

### Error handling

Errors may be reported as specified in math_errhandling.

- If the argument is NaN, NaN is returned and domain error is not reported.
- If x is negative, a domain error may occur.
- If n or m is greater or equal to 128, the behavior is implementation-defined.

### Notes

Implementations that do not support TR 29124 but support TR 19768, provide this function in the header `tr1/cmath` and namespace `std::tr1`.

An implementation of this function is also available in boost.math.

The associated Laguerre polynomials are the polynomial solutions of the equation xy,,  
 + (m + 1 - x)y,  
 + ny = 0.

The first few are:

- `assoc_laguerre(0, m, x)` = 1.
- `assoc_laguerre(1, m, x)` = -x + m + 1.
- `assoc_laguerre(2, m, x)` = 

  |  |
  | --- |
  | 1 |
  | 2 |

  [x2  
   - 2(m + 2)x + (m + 1)(m + 2)].
- `assoc_laguerre(3, m, x)` = 

  |  |
  | --- |
  | 1 |
  | 6 |

  [-x3  
   - 3(m + 3)x2  
   - 3(m + 2)(m + 3)x + (m + 1)(m + 2)(m + 3)].

### Example

Run this code

```
#define __STDCPP_WANT_MATH_SPEC_FUNCS__ 1
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
| laguerrelaguerreflaguerrel | Laguerre polynomials   (function) |

### External links

|  |
| --- |
| Weisstein, Eric W. "Associated Laguerre Polynomial." From MathWorld — A Wolfram Web Resource. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/special_functions/assoc_laguerre&oldid=169735>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 February 2024, at 06:03.