# FE_DFL_ENV

From cppreference.com
< cpp‎ | numeric‎ | fenv
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

Floating-point environment

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| feclearexcept(C++11) | | | | |
| fetestexcept(C++11) | | | | |
| feraiseexcept(C++11) | | | | |
| fegetexceptflagfesetexceptflag(C++11)(C++11) | | | | |
| fegetroundfesetround(C++11)(C++11) | | | | |
| fegetenvfesetenv(C++11)(C++11) | | | | |
| feholdexcept(C++11) | | | | |
| feupdateenv(C++11) | | | | |
| Macro constants | | | | |
| FE_ALL_EXCEPTFE_DIVBYZEROFE_INEXACTFE_INVALIDFE_OVERFLOWFE_UNDERFLOW(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | | | | |
| FE_DOWNWARDFE_TONEARESTFE_TOWARDZEROFE_UPWARD(C++11)(C++11)(C++11)(C++11) | | | | |
| ****FE_DFL_ENV****(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cfenv>` |  |  |
| #define FE_DFL_ENV /\*implementation defined\*/ |  | (since C++11) |
|  |  |  |

The macro constant `FE_DFL_ENV` expands to an expression of type const std::fenv_t\*, which points to a full copy of the default floating-point environment, that is, the environment as loaded at program startup.

Additional macros that begin with `FE_` followed by uppercase letters, and have the type const std::fenv_t\*, may be supported by an implementation.

### Example

Run this code

```
#include <cfenv>
#include <iostream>
// #pragma STDC FENV_ACCESS ON
 
void show_env()
{
    const int e = std::fetestexcept(FE_ALL_EXCEPT);
    if (e & FE_DIVBYZERO)
        std::cout << "division by zero is raised\n";
    if (e & FE_INEXACT)
        std::cout << "inexact is raised\n";
    if (e & FE_INVALID)
        std::cout << "invalid is raised\n";
    if (e & FE_UNDERFLOW)
        std::cout << "underflow is raised\n";
    if (e & FE_OVERFLOW)
        std::cout << "overflow is raised\n";
 
    switch (std::fegetround())
    {  
        case FE_DOWNWARD:
            std::cout << "rounding down\n";
            break;
        case FE_TONEAREST:
            std::cout << "rounding to nearest\n";
            break;
        case FE_TOWARDZERO:
            std::cout << "rounding to zero\n";
            break;
        case FE_UPWARD:
            std::cout << "rounding up\n";
            break;
    }
}
 
int main()
{
    std::cout << "On startup:\n";
    show_env();
 
    std::feraiseexcept(FE_UNDERFLOW | FE_OVERFLOW);
    std::fesetround(FE_UPWARD);
 
    std::cout << "\nBefore restoration:\n";
    show_env();
 
    std::fesetenv(FE_DFL_ENV);
 
    std::cout << "\nAfter reset to default:\n";
    show_env();
}

```

Output:

```
On startup: 
rounding to nearest
 
Before restoration: 
underflow is raised
overflow is raised
rounding up
 
After reset to default: 
rounding to nearest

```

### See also

|  |  |
| --- | --- |
| fegetenvfesetenv(C++11) | saves or restores the current floating-point environment   (function) |
| feupdateenv(C++11) | restores the floating-point environment and raises the previously raised exceptions   (function) |
| C documentation for FE_DFL_ENV | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/fenv/FE_DFL_ENV&oldid=160714>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 October 2023, at 23:18.