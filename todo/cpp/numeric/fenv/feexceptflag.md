# std::fegetexceptflag, std::fesetexceptflag

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
| ****fegetexceptflagfesetexceptflag****(C++11)(C++11) | | | | |
| fegetroundfesetround(C++11)(C++11) | | | | |
| fegetenvfesetenv(C++11)(C++11) | | | | |
| feholdexcept(C++11) | | | | |
| feupdateenv(C++11) | | | | |
| Macro constants | | | | |
| FE_ALL_EXCEPTFE_DIVBYZEROFE_INEXACTFE_INVALIDFE_OVERFLOWFE_UNDERFLOW(C++11)(C++11)(C++11)(C++11)(C++11)(C++11) | | | | |
| FE_DOWNWARDFE_TONEARESTFE_TOWARDZEROFE_UPWARD(C++11)(C++11)(C++11)(C++11) | | | | |
| FE_DFL_ENV(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cfenv>` |  |  |
| int fegetexceptflag( std::fexcept_t\* flagp, int excepts ); | (1) | (since C++11) |
| int fesetexceptflag( const std::fexcept_t\* flagp, int excepts ); | (2) | (since C++11) |
|  |  |  |

1) Attempts to obtain the full contents of the floating-point exception flags that are listed in the bitmask argument `excepts`, which is a bitwise OR of the floating point exception macros.

2) Attempts to copy the full contents of the floating-point exception flags that are listed in `excepts` from `flagp` into the floating-point environment. Does not raise any exceptions, only modifies the flags.

The full contents of a floating-point exception flag is not necessarily a boolean value indicating whether the exception is raised or cleared. For example, it may be a struct which includes the boolean status and the address of the code that triggered the exception. These functions obtain all such content and obtain/store it in `flagp` in implementation-defined format.

### Parameters

|  |  |  |
| --- | --- | --- |
| flagp | - | pointer to an std::fexcept_t object where the flags will be stored or read from |
| excepts | - | bitmask listing the exception flags to get/set |

### Return value

​0​ on success, non-zero otherwise.

### See also

|  |  |
| --- | --- |
| C documentation for fegetexceptflag, fesetexceptflag | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/fenv/feexceptflag&oldid=125163>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 December 2020, at 10:24.