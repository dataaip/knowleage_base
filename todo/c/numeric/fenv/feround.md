# fegetround, fesetround

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
| fetestexcept(C99) | | | | |
| feraiseexcept(C99) | | | | |
| fegetexceptflagfesetexceptflag(C99)(C99) | | | | |
| ****fegetroundfesetround****(C99)(C99) | | | | |
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
| int fesetround( int round ); | (1) | (since C99) |
| int fegetround(); | (2) | (since C99) |
|  |  |  |

1) Attempts to establish the floating-point rounding direction equal to the argument round, which is expected to be one of the floating-point rounding macros.

2) Returns the value of the floating-point rounding macro that corresponds to the current rounding direction.

### Parameters

|  |  |  |
| --- | --- | --- |
| round | - | rounding direction, one of floating-point rounding macros |

### Return value

1) ​0​ on success, non-zero otherwise.

2) the floating-point rounding macro describing the current rounding direction or a negative value if the direction cannot be determined.

### Notes

The current rounding mode, reflecting the effects of the most recent `fesetround`, can also be queried with FLT_ROUNDS.

### Example

Run this code

```
#include <fenv.h>
#include <math.h>
#include <stdio.h>
 
// #pragma STDC FENV_ACCESS ON
 
void show_fe_current_rounding_direction(void)
{
    printf("current rounding direction:  ");
    switch (fegetround())
    {
           case FE_TONEAREST:  printf ("FE_TONEAREST");  break;
           case FE_DOWNWARD:   printf ("FE_DOWNWARD");   break;
           case FE_UPWARD:     printf ("FE_UPWARD");     break;
           case FE_TOWARDZERO: printf ("FE_TOWARDZERO"); break;
           default:            printf ("unknown");
    };
    printf("\n");
}
 
int main(void)
{
    /* Default rounding direction */
    show_fe_current_rounding_direction();
    printf("+11.5 -> %+4.1f\n", rint(+11.5)); /* midway between two integers */
    printf("+12.5 -> %+4.1f\n", rint(+12.5)); /* midway between two integers */
 
    /* Save current rounding direction. */
    int curr_direction = fegetround();
 
    /* Temporarily change current rounding direction. */
    fesetround(FE_DOWNWARD);
    show_fe_current_rounding_direction();
    printf("+11.5 -> %+4.1f\n", rint(+11.5));
    printf("+12.5 -> %+4.1f\n", rint(+12.5));
 
    /* Restore default rounding direction. */
    fesetround(curr_direction);
    show_fe_current_rounding_direction();
 
    return 0;
}

```

Possible output:

```
current rounding direction:  FE_TONEAREST
+11.5 -> +12.0
+12.5 -> +12.0
current rounding direction:  FE_DOWNWARD
+11.5 -> +11.0
+12.5 -> +12.0
current rounding direction:  FE_TONEAREST

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.6.3.1 The fegetround function (p: TBD)

:   - 7.6.3.2 The fesetround function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.6.3.1 The fegetround function (p: TBD)

:   - 7.6.3.2 The fesetround function (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.6.3.1 The fegetround function (p: 212)

:   - 7.6.3.2 The fesetround function (p: 212-213)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.6.3.1 The fegetround function (p: 193)

:   - 7.6.3.2 The fesetround function (p: 193-194)

### See also

|  |  |
| --- | --- |
| nearbyintnearbyintfnearbyintl(C99)(C99)(C99) | rounds to an integer using current rounding mode   (function) |
| rintrintfrintllrintlrintflrintlllrintllrintfllrintl(C99)(C99)(C99)(C99)(C99)(C99)(C99)(C99)(C99) | rounds to an integer using current rounding mode with   exception if the result differs   (function) |
| C++ documentation for fegetround, fesetround | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/fenv/feround&oldid=169737>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 February 2024, at 06:21.