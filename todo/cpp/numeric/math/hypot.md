# std::hypot, std::hypotf, std::hypotl

From cppreference.com
< cpp‎ | numeric‎ | math
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

Common mathematical functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Basic operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | abs(int)labsllabsimaxabs(C++11) | | | | | | abs(float)fabs | | | | | | divldivlldivimaxdiv(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fmod | | | | | | remainder(C++11) | | | | | | remquo(C++11) | | | | | | fma(C++11) | | | | | | fmax(C++11) | | | | | | fmin(C++11) | | | | | | fdim(C++11) | | | | | | nannanfnanl(C++11)(C++11)(C++11) | | | | | |
| Exponential functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | exp | | | | | | exp2(C++11) | | | | | | expm1(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | log | | | | | | log10 | | | | | | log1p(C++11) | | | | | | log2(C++11) | | | | | |
| Power functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | sqrt | | | | | | cbrt(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****hypot****(C++11) | | | | | | pow | | | | | |
| Trigonometric and  hyperbolic functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | sin | | | | | | cos | | | | | | tan | | | | | | asin | | | | | | acos | | | | | | atan | | | | | | atan2 | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sinh | | | | | | cosh | | | | | | tanh | | | | | | asinh(C++11) | | | | | | acosh(C++11) | | | | | | atanh(C++11) | | | | | |  | | | | | |
| Error and gamma functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erf(C++11) | | | | | | erfc(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lgamma(C++11) | | | | | | tgamma(C++11) | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Nearest integer floating point operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ceil | | | | | | floor | | | | | | roundlroundllround(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | trunc(C++11) | | | | | | nearbyint(C++11) | | | | | | rintlrintllrint(C++11)(C++11)(C++11) | | | | | |
| Floating point manipulation functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ldexp | | | | | | scalbnscalbln(C++11)(C++11) | | | | | | ilogb(C++11) | | | | | | logb(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | frexp | | | | | | modf | | | | | | nextafternexttoward(C++11)(C++11) | | | | | | copysign(C++11) | | | | | |
| Classification and comparison | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | fpclassify(C++11) | | | | | | isfinite(C++11) | | | | | | isinf(C++11) | | | | | | isnan(C++11) | | | | | | isnormal(C++11) | | | | | | signbit(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isgreater(C++11) | | | | | | isgreaterequal(C++11) | | | | | | isless(C++11) | | | | | | islessequal(C++11) | | | | | | islessgreater(C++11) | | | | | | isunordered(C++11) | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | div_t | | | | | | ldiv_t | | | | | | lldiv_t(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | imaxdiv_t(C++11) | | | | | | float_t(C++11) | | | | | | double_t(C++11) | | | | | |
| Macro constants | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | HUGE_VALFHUGE_VALHUGE_VALL(C++11)(C++11) | | | | | | math_errhandlingMATH_ERRNOMATH_ERREXCEPT(C++11) | | | | | | INFINITY(C++11) | | | | | | NAN(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Classification | | | | | | FP_NORMALFP_SUBNORMALFP_ZEROFP_INFINITEFP_NAN(C++11)(C++11)(C++11)(C++11)(C++11) | | | | | |  | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cmath>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| float       hypot ( float x, float y );  double      hypot ( double x, double y ); long double hypot ( long double x, long double y ); |  | (since C++11)  (until C++23) |
| /\*floating-point-type\*/               hypot ( /\*floating-point-type\*/ x, /\*floating-point-type\*/ y ); |  | (since C++23)  (constexpr since C++26) |
|  |  |  |
| --- | --- | --- |
| float       hypotf( float x, float y ); | (2) | (since C++11)  (constexpr since C++26) |
| long double hypotl( long double x, long double y ); | (3) | (since C++11)  (constexpr since C++26) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| float       hypot ( float x, float y, float z );  double      hypot ( double x, double y, double z ); long double hypot ( long double x, long double y, long double z ); |  | (since C++17)  (until C++23) |
| /\*floating-point-type\*/              hypot ( /\*floating-point-type\*/ x,                      /\*floating-point-type\*/ y, /\*floating-point-type\*/ z ); |  | (since C++23)  (constexpr since C++26) |
|  |  |  |
| --- | --- | --- |
| Additional overloads |  |  |
| Defined in header `<cmath>` |  |  |
| template< class Arithmetic1, Arithmetic2 >  /\*common-floating-point-type\*/             hypot ( Arithmetic1 x, Arithmetic2 y ); | (A) | (since C++11)  (constexpr since C++26) |
| template< class Arithmetic1, Arithmetic2, Arithmetic3 >  /\*common-floating-point-type\*/             hypot ( Arithmetic1 x, Arithmetic2 y, Arithmetic3 z ); | (B) | (since C++17) |
|  |  |  |

1-3) Computes the square root of the sum of the squares of x and y, without undue overflow or underflow at intermediate stages of the computation.The library provides overloads of `std::hypot` for all cv-unqualified floating-point types as the type of the parameters x and y.(since C++23)4) Computes the square root of the sum of the squares of x, y, and z, without undue overflow or underflow at intermediate stages of the computation.The library provides overloads of `std::hypot` for all cv-unqualified floating-point types as the type of the parameters x, y and z.(since C++23)A,B) Additional overloads are provided for all other combinations of arithmetic types.

The value computed by the two-argument version of this function is the length of the hypotenuse of a right-angled triangle with sides of length x and y, or the distance of the point `(x,y)` from the origin `(0,0)`, or the magnitude of a complex number `x+iy`.

The value computed by the three-argument version of this function is the distance of the point `(x,y,z)` from the origin `(0,0,0)`.

### Parameters

|  |  |  |
| --- | --- | --- |
| x, y, z | - | floating-point or integer values |

### Return value

1-3,A) If no errors occur, the hypotenuse of a right-angled triangle, \(\scriptsize{\sqrt{x^2+y^2} }\)√x2  
+y2  
, is returned.4,B) If no errors occur, the distance from origin in 3D space, \(\scriptsize{\sqrt{x^2+y^2+z^2} }\)√x2  
+y2  
+z2  
, is returned.

If a range error due to overflow occurs, +HUGE_VAL, `+HUGE_VALF`, or `+HUGE_VALL` is returned.

If a range error due to underflow occurs, the correct result (after rounding) is returned.

### Error handling

Errors are reported as specified in math_errhandling.

If the implementation supports IEEE floating-point arithmetic (IEC 60559),

- std::hypot(x, y), std::hypot(y, x), and std::hypot(x, -y) are equivalent.
- if one of the arguments is ±0, std::hypot(x, y) is equivalent to std::fabs called with the non-zero argument.
- if one of the arguments is ±∞, std::hypot(x, y) returns +∞ even if the other argument is NaN.
- otherwise, if any of the arguments is NaN, NaN is returned.

### Notes

Implementations usually guarantee precision of less than 1 ulp (Unit in the Last Place — Unit of Least Precision): GNU, BSD.

std::hypot(x, y) is equivalent to std::abs(std::complex<double>(x, y)).

POSIX specifies that underflow may only occur when both arguments are subnormal and the correct result is also subnormal (this forbids naive implementations).

|  |  |
| --- | --- |
| Distance between two points `(x1, y1, z1)` and `(x2, y2, z2)` on 3D space can be calculated using 3-argument overload of `std::hypot` as std::hypot(x2 - x1, y2 - y1, z2 - z1). | (since C++17) |

The additional overloads are not required to be provided exactly as (A,B). They only need to be sufficient to ensure that for their first argument num1, second argument num2 and the optional third argument num3:

|  |  |
| --- | --- |
| - If num1, num2 or num3 has type long double, then   - std::hypot(num1, num2) has the same effect as std::hypot(static_cast<long double>(num1),            static_cast<long double>(num2)), and - std::hypot(num1, num2, num3) has the same effect as std::hypot(static_cast<long double>(num1),            static_cast<long double>(num2),            static_cast<long double>(num3)).   - Otherwise, if num1, num2 and/or num3 has type double or an integer type, then   - std::hypot(num1, num2) has the same effect as std::hypot(static_cast<double>(num1),            static_cast<double>(num2)), and - std::hypot(num1, num2, num3) has the same effect as std::hypot(static_cast<double>(num1),            static_cast<double>(num2),            static_cast<double>(num3)).   - Otherwise, if num1, num2 or num3 has type float, then   - std::hypot(num1, num2) has the same effect as std::hypot(static_cast<float>(num1),            static_cast<float>(num2)), and - std::hypot(num1, num2, num3) has the same effect as std::hypot(static_cast<float>(num1),            static_cast<float>(num2),            static_cast<float>(num3)). | (until C++23) |
| If num1, num2 and num3 have arithmetic types, then   - std::hypot(num1, num2) has the same effect as std::hypot(static_cast</\*common-floating-point-type\*/>(num1),            static_cast</\*common-floating-point-type\*/>(num2)), and - std::hypot(num1, num2, num3) has the same effect as std::hypot(static_cast</\*common-floating-point-type\*/>(num1),            static_cast</\*common-floating-point-type\*/>(num2),            static_cast</\*common-floating-point-type\*/>(num3)),   where /\*common-floating-point-type\*/ is the floating-point type with the greatest floating-point conversion rank and greatest floating-point conversion subrank among the types of num1, num2 and num3, arguments of integer type are considered to have the same floating-point conversion rank as double.  If no such floating-point type with the greatest rank and subrank exists, then overload resolution does not result in a usable candidate from the overloads provided. | (since C++23) |

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_hypot` | `201603L` | (C++17) | 3-argument overload of `std::hypot` (4,B) |

### Example

Run this code

```
#include <cerrno>
#include <cfenv>
#include <cfloat>
#include <cmath>
#include <cstring>
#include <iostream>
 
// #pragma STDC FENV_ACCESS ON
 
struct Point3D { float x, y, z; };
 
int main()
{
    // typical usage
    std::cout << "(1,1) cartesian is (" << std::hypot(1, 1)
              << ',' << std::atan2(1,1) << ") polar\n";
 
    Point3D a{3.14, 2.71, 9.87}, b{1.14, 5.71, 3.87};
    // C++17 has 3-argument hypot overload:
    std::cout << "distance(a,b) = "
              << std::hypot(a.x - b.x, a.y - b.y, a.z - b.z) << '\n';
 
    // special values
    std::cout << "hypot(NAN,INFINITY) = " << std::hypot(NAN, INFINITY) << '\n';
 
    // error handling
    errno = 0;
    std::feclearexcept(FE_ALL_EXCEPT);
    std::cout << "hypot(DBL_MAX,DBL_MAX) = " << std::hypot(DBL_MAX, DBL_MAX) << '\n';
 
    if (errno == ERANGE)
        std::cout << "    errno = ERANGE " << std::strerror(errno) << '\n';
    if (std::fetestexcept(FE_OVERFLOW))
        std::cout << "    FE_OVERFLOW raised\n";
}

```

Output:

```
(1,1) cartesian is (1.41421,0.785398) polar
distance(a,b) = 7
hypot(NAN,INFINITY) = inf
hypot(DBL_MAX,DBL_MAX) = inf
    errno = ERANGE Numerical result out of range
    FE_OVERFLOW raised

```

### See also

|  |  |
| --- | --- |
| powpowfpowl(C++11)(C++11) | raises a number to the given power (\(\small{x^y}\)xy)   (function) |
| sqrtsqrtfsqrtl(C++11)(C++11) | computes square root (\(\small{\sqrt{x}}\)√x)   (function) |
| cbrtcbrtfcbrtl(C++11)(C++11)(C++11) | computes cube root (\(\small{\sqrt[3]{x}}\)3√x)   (function) |
| abs(std::complex) | returns the magnitude of a complex number   (function template) |
| C documentation for hypot | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/math/hypot&oldid=180162>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 February 2025, at 22:23.