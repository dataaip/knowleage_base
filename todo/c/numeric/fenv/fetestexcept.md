# fetestexcept

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
| feclearexcept(C99) | | | | |
| ****fetestexcept****(C99) | | | | |
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
| int fetestexcept( int excepts ); |  | (since C99) |
|  |  |  |

Determines which of the specified subset of the floating-point exceptions are currently set. The argument `excepts` is a bitwise OR of the floating-point exception macros.

### Parameters

|  |  |  |
| --- | --- | --- |
| excepts | - | bitmask listing the exception flags to test |

### Return value

Bitwise OR of the floating-point exception macros that are both included in `excepts` and correspond to floating-point exceptions currently set.

### Example

Run this code

```
#include <stdio.h>
#include <math.h>
#include <fenv.h>
#include <float.h>
 
#pragma STDC FENV_ACCESS ON
 
void show_fe_exceptions(void)
{
    printf("current exceptions raised: ");
    if(fetestexcept(FE_DIVBYZERO))     printf(" FE_DIVBYZERO");
    if(fetestexcept(FE_INEXACT))       printf(" FE_INEXACT");
    if(fetestexcept(FE_INVALID))       printf(" FE_INVALID");
    if(fetestexcept(FE_OVERFLOW))      printf(" FE_OVERFLOW");
    if(fetestexcept(FE_UNDERFLOW))     printf(" FE_UNDERFLOW");
    if(fetestexcept(FE_ALL_EXCEPT)==0) printf(" none");
    printf("\n");
}
 
int main(void)
{
    /* Show default set of exception flags. */
    show_fe_exceptions();
 
    /* Perform some computations which raise exceptions. */
    printf("1.0/0.0     = %f\n", 1.0/0.0);        /* FE_DIVBYZERO            */
    printf("1.0/10.0    = %f\n", 1.0/10.0);       /* FE_INEXACT              */
    printf("sqrt(-1)    = %f\n", sqrt(-1));       /* FE_INVALID              */
    printf("DBL_MAX*2.0 = %f\n", DBL_MAX*2.0);    /* FE_INEXACT FE_OVERFLOW  */
    printf("nextafter(DBL_MIN/pow(2.0,52),0.0) = %.1f\n",
           nextafter(DBL_MIN/pow(2.0,52),0.0));   /* FE_INEXACT FE_UNDERFLOW */
    show_fe_exceptions();
 
    return 0;
}

```

Output:

```
current exceptions raised:  none
1.0/0.0     = inf
1.0/10.0    = 0.100000
sqrt(-1)    = -nan
DBL_MAX*2.0 = inf
nextafter(DBL_MIN/pow(2.0,52),0.0) = 0.0
current exceptions raised:  FE_DIVBYZERO FE_INEXACT FE_INVALID FE_OVERFLOW FE_UNDERFLOW

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.6.2.5 The fetestexcept function (p: 211-212)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.6.2.5 The fetestexcept function (p: 192-193)

### See also

|  |  |
| --- | --- |
| feclearexcept(C99) | clears the specified floating-point status flags   (function) |
| C++ documentation for fetestexcept | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/fenv/fetestexcept&oldid=133794>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 September 2021, at 02:00.