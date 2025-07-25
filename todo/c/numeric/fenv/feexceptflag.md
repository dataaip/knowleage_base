# fegetexceptflag, fesetexceptflag

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
| ****fegetexceptflagfesetexceptflag****(C99)(C99) | | | | |
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
| int fegetexceptflag( fexcept_t\* flagp, int excepts ); | (1) | (since C99) |
| int fesetexceptflag( const fexcept_t\* flagp, int excepts ); | (2) | (since C99) |
|  |  |  |

1) Attempts to obtain the full contents of the floating-point exception flags that are listed in the bitmask argument `excepts`, which is a bitwise OR of the floating-point exception macros.

2) Attempts to copy the full contents of the floating-point exception flags that are listed in `excepts` from `flagp` into the floating-point environment. Does not raise any exceptions, only modifies the flags.

The full contents of a floating-point exception flag is not necessarily a boolean value indicating whether the exception is raised or cleared. For example, it may be a struct which includes the boolean status and the address of the code that triggered the exception. These functions obtain all such content and obtain/store it in `flagp` in implementation-defined format.

### Parameters

|  |  |  |
| --- | --- | --- |
| flagp | - | pointer to an fexcept_t object where the flags will be stored or read from |
| excepts | - | bitmask listing the exception flags to get/set |

### Return value

​0​ on success, non-zero otherwise.

### Example

Run this code

```
#include <stdio.h>
#include <fenv.h>
 
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
    fexcept_t excepts;
 
    /* Setup a "current" set of exception flags. */
    feraiseexcept(FE_INVALID);
    show_fe_exceptions();
 
    /* Save current exception flags. */
    fegetexceptflag(&excepts,FE_ALL_EXCEPT);
 
    /* Temporarily raise two other exceptions. */
    feclearexcept(FE_ALL_EXCEPT);
    feraiseexcept(FE_OVERFLOW | FE_INEXACT);
    show_fe_exceptions();
 
    /* Restore previous exception flags. */
    fesetexceptflag(&excepts,FE_ALL_EXCEPT);
    show_fe_exceptions();
 
    return 0;
}

```

Output:

```
current exceptions raised: FE_INVALID
current exceptions raised: FE_INEXACT FE_OVERFLOW
current exceptions raised: FE_INVALID

```

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 7.6.2.2 The fegetexceptflag function (p: 210)

:   - 7.6.2.4 The fesetexceptflag function (p: 211)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.6.2.2 The fegetexceptflag function (p: 191)

:   - 7.6.2.4 The fesetexceptflag function (p: 192)

### See also

|  |  |
| --- | --- |
| C++ documentation for fegetexceptflag, fesetexceptflag | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/fenv/feexceptflag&oldid=133796>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 September 2021, at 02:01.