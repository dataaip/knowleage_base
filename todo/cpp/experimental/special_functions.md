# Mathematical special functions

From cppreference.com
< cpp‎ | experimental
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
| ****Mathematical special functions**** (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

****Mathematical special functions****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | assoc_laguerreassoc_laguerrefassoc_laguerrel | | | | | | assoc_legendreassoc_legendrefassoc_legendrel | | | | | | betabetafbetal | | | | | | comp_ellint_1comp_ellint_1fcomp_ellint_1l | | | | | | comp_ellint_2comp_ellint_2fcomp_ellint_2l | | | | | | comp_ellint_3comp_ellint_3fcomp_ellint_3l | | | | | | cyl_bessel_icyl_bessel_ifcyl_bessel_il") | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cyl_bessel_jcyl_bessel_jfcyl_bessel_jl") | | | | | | cyl_bessel_kcyl_bessel_kfcyl_bessel_kl") | | | | | | cyl_neumanncyl_neumannfcyl_neumannl") | | | | | | ellint_1ellint_1fellint_1l") | | | | | | ellint_2ellint_2fellint_2l") | | | | | | ellint_3ellint_3fellint_3l") | | | | | | expintexpintfexpintl | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | hermitehermitefhermitel | | | | | | laguerrelaguerreflaguerrel | | | | | | legendrelegendreflegendrel | | | | | | riemann_zetariemann_zetafriemann_zetal | | | | | | sph_besselsph_besselfsph_bessell") | | | | | | sph_legendresph_legendrefsph_legendrel") | | | | | | sph_neumannsph_neumannfsph_neumannl") | | | | | |

The Mathematical Special Functions library, ISO/IEC 29124:2010, specifies extensions to the C++ standard library that include mathematical special functions (originally part of ISO/IEC TR 19768:2007).

This special functions in this library are implemented in boost.math, which is currently available on more compilers and platforms than implementations of this standard. At the time of this writing (1/2016) the only compiler that announced direct support is gcc, for version 6.1.

### Non-member functions

|  |  |
| --- | --- |
| Defined in header `<cmath>` | |
| assoc_laguerreassoc_laguerrefassoc_laguerrel | associated Laguerre polynomials   (function) |
| assoc_legendreassoc_legendrefassoc_legendrel | associated Legendre polynomials   (function) |
| betabetafbetal | beta function   (function) |
| comp_ellint_1comp_ellint_1fcomp_ellint_1l | (complete) elliptic integral of the first kind   (function) |
| comp_ellint_2comp_ellint_2fcomp_ellint_2l | (complete) elliptic integral of the second kind   (function) |
| comp_ellint_3comp_ellint_3fcomp_ellint_3l | (complete) elliptic integral of the third kind   (function) |
| cyl_bessel_icyl_bessel_ifcyl_bessel_il") | regular modified cylindrical Bessel functions   (function) |
| cyl_bessel_jcyl_bessel_jfcyl_bessel_jl") | cylindrical Bessel functions (of the first kind)   (function) |
| cyl_bessel_kcyl_bessel_kfcyl_bessel_kl") | irregular modified cylindrical Bessel functions   (function) |
| cyl_neumanncyl_neumannfcyl_neumannl") | cylindrical Neumann functions   (function) |
| ellint_1ellint_1fellint_1l") | (incomplete) elliptic integral of the first kind   (function) |
| ellint_2ellint_2fellint_2l") | (incomplete) elliptic integral of the second kind   (function) |
| ellint_3ellint_3fellint_3l") | (incomplete) elliptic integral of the third kind   (function) |
| expintexpintfexpintl | exponential integral   (function) |
| hermitehermitefhermitel | Hermite polynomials   (function) |
| legendrelegendreflegendrel | Legendre polynomials   (function) |
| laguerrelaguerreflaguerrel | Laguerre polynomials   (function) |
| riemann_zetariemann_zetafriemann_zetal | Riemann zeta function   (function) |
| sph_besselsph_besselfsph_bessell") | spherical Bessel functions (of the first kind)   (function) |
| sph_legendresph_legendrefsph_legendrel") | spherical associated Legendre functions   (function) |
| sph_neumannsph_neumannfsph_neumannl") | spherical Neumann functions   (function) |

### Macros

|  |  |
| --- | --- |
| __STDCPP_MATH_SPEC_FUNCS__ | a value of at least 201003L indicates that ISO/IEC 29124:2010 is supported   (macro constant) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/special_functions&oldid=158792>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 September 2023, at 10:33.