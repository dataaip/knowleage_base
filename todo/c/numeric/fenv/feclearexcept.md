# feclearexcept

From cppreference.com
< c‎ | numeric‎ | fenv
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 Numerics

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Common mathematical functions | | | | |
| Floating-point environment (C99) | | | | |
| Pseudo-random number generation | | | | |
| Complex number arithmetic (C99) | | | | |
| Type-generic math (C99) | | | | |
| Bit manipulation (C23) | | | | |
| Checked integer arithmetic (C23) | | | | |

 Floating-point environment

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| ****feclearexcept****(C99) | | | | |
| fetestexcept(C99) | | | | |
| feraiseexcept(C99) | | | | |
| fegetexceptflagfesetexceptflag(C99)(C99) | | | | |
| fegetroundfesetround(C99)(C99) | | | | |
| fegetenvfesetenv(C99) | | | | |
| feholdexcept(C99) | | | | |
| feupdateenv(C99) | | | | |
| Macro constants | | | | |
| FE_ALL_EXCEPTFE_DIVBYZEROFE_INEXACTFE_INVALIDFE_OVERFLOWFE_UNDERFLOW(C99) | | | | |
| FE_DOWNWARDFE_TONEARESTFE_TOWARDZEROFE_UPWARD(C99) | | | | |
| FE_DFL_ENV(C99) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<fenv.h>` |  |  |
| int feclearexcept( int excepts ); |  | (since C99) |
|  |  |  |

Attempts to clear the floating-point exceptions that are listed in the bitmask argument `excepts`, which is a bitwise OR of the floating-point exception macros.

### Parameters

|  |  |  |
| --- | --- | --- |
| excepts | - | bitmask listing the exception flags to clear |

### Return value

​0​ if all indicated exceptions were successfully cleared or if `excepts` is zero. Returns a non-zero value on error.

### Example

Run this code

```
#include <fenv.h>
#include <stdio.h>
#include <math.h>
#include <float.h>
 
/*
 * A possible implementation of hypot which makes use of many advanced
 * floating-point features.
 */
double hypot_demo(double a, double b) {
  const int range_problem = FE_OVERFLOW | FE_UNDERFLOW;
  feclearexcept(range_problem);
  // try a fast algorithm
  double result = sqrt(a * a + b * b);
  if (!fetestexcept(range_problem))  // no overflow or underflow
    return result;                   // return the fast result
  // do a more complicated calculation to avoid overflow or underflow
  int a_exponent,b_exponent;
  frexp(a, &a_exponent);
  frexp(b, &b_exponent);
 
  if (a_exponent - b_exponent > DBL_MAX_EXP)
    return fabs(a) + fabs(b);        // we can ignore the smaller value
  // scale so that fabs(a) is near 1
  double a_scaled = scalbn(a, -a_exponent);
  double b_scaled = scalbn(b, -a_exponent);
  // overflow and underflow is now impossible 
  result = sqrt(a_scaled * a_scaled + b_scaled * b_scaled);
  // undo scaling
  return scalbn(result, a_exponent);
}
 
int main(void)
{
  // Normal case takes the fast route
  printf("hypot(%f, %f) = %f\n", 3.0, 4.0, hypot_demo(3.0, 4.0));
  // Extreme case takes the slow but more accurate route
  printf("hypot(%e, %e) = %e\n", DBL_MAX / 2.0, 
                                DBL_MAX / 2.0, 
                                hypot_demo(DBL_MAX / 2.0, DBL_MAX / 2.0));
 
  return 0;
}

```

Output:

```
hypot(3.000000, 4.000000) = 5.000000
hypot(8.988466e+307, 8.988466e+307) = 1.271161e+308

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.6.2.1 The feclearexcept function (p: 209)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.6.2.1 The feclearexcept function (p: 190)

### See also

|  |  |
| --- | --- |
| fetestexcept(C99) | determines which of the specified floating-point status flags are set   (function) |
| C++ documentation for feclearexcept | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/fenv/feclearexcept&oldid=133793>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 September 2021, at 01:58.