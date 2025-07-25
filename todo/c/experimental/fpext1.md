# Floating-point extensions part 1: binary floating-point arithmetic

From cppreference.com
< c‎ | experimental
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

 Technical Specifications

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Extensions for embedded processors") | | | | |
| Dynamic memory extensions | | | | |
| ****Floating-point extensions part 1: Binary floating-point**** | | | | |
| Floating-point extensions part 4: Supplementary functions | | | | |

 ****Floating-point extensions part 1: Binary floating-point****Template:c/experimental/fpext1/navbar content")

Floating-point extensions for C - Part 1: Binary floating-point arithmetic, ISO/IEC TS 18661-1:2014, defines the following new components for the C standard library, as recommended by ISO/IEC/IEEE 60559:2011 (the current revision of IEEE-754)

|  |  |
| --- | --- |
| __STDC_IEC_60559_BFP__ | integer constant of type long and value 201ymmL, replaces __STDC_IEC_559__   (macro constant) |
| __STDC_IEC_60559_COMPLEX__ | integer constant of type long and value 201ymmL, replaces __STDC_IEC_559_COMPLEX__   (macro constant) |
| Defined in header `<limits.h>` | |
| CHAR_WIDTH SCHAR_WIDTH UCHAR_WIDTHSHRT_WIDTH USHRT_WIDTHINT_WIDTH UINT_WIDTHLONG_WIDTH ULONG_WIDTHLLONG_WIDTH ULLONG_WIDTH(FP Ext 1 TS) | width, in bits, of the corresponding type   (macro constant) |
| Defined in header `<float.h>` | |
| CR_DECIMAL_DIG")(FP Ext 1 TS) | conversions between all supported binary floating-point types and character sequences with at most CR_DECIMAL_DIG significant decimal digits are correctly rounded (this is at least DECIMAL_DIG + 3)   (macro constant) |
| Defined in header `<fenv.h>` | |
| femode_t(FP Ext 1 TS) | collection of dynamic floating-point control modes supported by the implementation, including the dynamic rounding direction mode   (typedef) |
| FE_DFL_MODE(FP Ext 1 TS) | pointer to the default femode_t   (macro constant) |
| FE_SNANS_ALWAYS_SIGNAL(FP Ext 1 TS) | defined (as integer constant 1) if sNaN arguments cause the functions that suppress qNaNs, like hypot or fmax, to raise FE_INVALID and return a qNaN   (macro constant) |
| fesetexcept")(FP Ext 1 TS) | sets the specified floating-point exception flags without causing any side-effects that raising them would   (function) |
| fetestexceptflag")(FP Ext 1 TS) | tests if given flags are in a saved representation of the floating-point exception flags   (function) |
| fegetmodefesetmode")(FP Ext 1 TS) | gets and sets all the implementation’s dynamic floating-point control modes collectively   (function) |
| Defined in header `<stdint.h>` | |
| INTn_WIDTH UINTn_WIDTHINT_LEASTn_WIDTH UINT_LEASTn_WIDTHINT_FASTn_WIDTH UINT_FASTn_WIDTHINTPTR_WIDTH UINTPTR_WIDTHINTMAX_WIDTH UINTMAX_WIDTHPTRDIFF_WIDTHSIG_ATOMIC_WIDTHSIZE_WIDTHWCHAR_WIDTH WINT_WIDTH(FP Ext 1 TS) | width, in bits, of the corresponding type   (macro constant) |
| Defined in header `<stdlib.h>` | |
| strfromdstrfromfstrfroml")(FP Ext 1 TS) | convert a single foating-point number to string using the specified snprintf format   (function) |
| Defined in header `<math.h>` | |
| FP_INT_UPWARDFP_INT_DOWNWARDFP_INT_TOWARDZERO FP_INT_TONEARESTFROMZEROFP_INT_TONEAREST(FP Ext 1 TS) | rounding direction for the functions ceil, floor, trunc, round, and roundeven, suitable for use with fromfp family of functions   (macro constant) |
| FP_LLOGB0(FP Ext 1 TS) | value returned by llogb if the argument is zero   (macro constant) |
| FP_LLOGBNAN(FP Ext 1 TS) | value returned by llogb if the argument is NaN   (macro constant) |
| SNANFSNANSNANL")(FP Ext 1 TS) | represents a signalling NaN for float, double, long double respectively   (macro constant) |
| FP_FAST_FADD FP_FAST_FADDL FP_FAST_DADDLFP_FAST_FSUB FP_FAST_FSUBL FP_FAST_DSUBLFP_FAST_FMUL FP_FAST_FMULL FP_FAST_DMULLFP_FAST_FDIV FP_FAST_FDIVL FP_FAST_DDIVLFP_FAST_FFMA FP_FAST_FFMAL FP_FAST_DFMALFP_FAST_FSQRT FP_FAST_FSQRTL FP_FAST_DSQRTL(FP Ext 1 TS) | if defined, indicates that the corresponding function executes faster than the equivalent function in a larger type followed by a cast to target type   (macro constant) |
| iseqsig(FP Ext 1 TS) | (function macro) |
| iscanonical(FP Ext 1 TS) | tests if the floating-point value is canonical   (function macro) |
| issignaling(FP Ext 1 TS) | tests if the floating-point value is a signalling NaN   (function macro) |
| issubnormal(FP Ext 1 TS) | tests if the floating-point value is subnormal   (function macro) |
| iszero(FP Ext 1 TS) | tests if the floating-point value is a zero (positive, negative, unsigned)   (function macro) |
| fromfpfromfpffromfpl")(FP Ext 1 TS) | round to signed integer using the specified rounding direction   (function) |
| ufromfpufromfpfufromfpl")(FP Ext 1 TS) | round to unsigned integer using the specified rounding direction   (function) |
| fromfpxfromfpxffromfpxl")(FP Ext 1 TS) | round to signed integer using the specified rounding direction, reporting inexactness   (function) |
| ufromfpxufromfpxfufromfpxl")(FP Ext 1 TS) | round to unsigned integer using the specified rounding direction, reporting inexactness   (function) |
| roundevenroundevenfroundevenl")(FP Ext 1 TS) | rounds to nearest, halfway cases to even   (function) |
| llogbllogbfllogbl")(FP Ext 1 TS) | equivalent to logb except the return type is long   (function) |
| fmaxmagfmaxmagffmaxmagl")(FP Ext 1 TS) | returns the value of their argument of maximum magnitude   (function) |
| fminmagfminmagffminmagl")(FP Ext 1 TS) | returns the value of their argument of minimum magnitude   (function) |
| nextupnextupfnextupl(FP Ext 1 TS) | returns the next greater representable floating-point value   (function) |
| nextdownnextdownfnextdown l")(FP Ext 1 TS) | returns the next smaller representable floating-point value   (function) |
| faddfaddldaddl")(FP Ext 1 TS) | calculates x+y as if in infinite precision and rounded once to target type   (function) |
| fsubfsubldsubl")(FP Ext 1 TS) | calculates x-y as if in infinite precision and rounded once to target type   (function) |
| fmulfmulldmull")(FP Ext 1 TS) | calculates x\*y as if in infinite precision and rounded once to target type   (function) |
| fdivfdivlddivl")(FP Ext 1 TS) | calculates x/y as if in infinite precision and rounded once to target type   (function) |
| ffmaffmaldfmal")(FP Ext 1 TS) | calculates the same as fma as if in infinite precision and rounded once to target type   (function) |
| fsqrtfsqrtldsqrtl")(FP Ext 1 TS) | calculates the same as sqrt as if in infinite precision and rounded once to target type   (function) |
| totalordertotalorderftotalorderl")(FP Ext 1 TS) | orders two floating-point values using the ISO 60559 total order relation   (function) |
| totalordermagtotalordermagftotalordermagl")(FP Ext 1 TS) | orders the magnitudes of two floating-point values using the ISO 60559 total order relation   (function) |
| canonicalizecanonicalizefcanonicalizel")(FP Ext 1 TS) | obtains the ISO 60559 canonical binary encoding of the given floating-point value   (function) |
| getpayloadgetpayloadfgetpayloadl")(FP Ext 1 TS) | extracts the payload from the given NaN value   (function) |
| setpayloadsetpayloadfsetpayloadl")(FP Ext 1 TS) | creates a quiet NaN with the specified payload   (function) |
| setpayloadsigsetpayloadsigfsetpayloadsigl")(FP Ext 1 TS) | creates a signalling NaN with the specified payload   (function) |
| Defined in header `<tgmath.h>` | |
| roundeven(FP Ext 1 TS) | generic overload of roundeven   (function) |
| llogb(FP Ext 1 TS) | generic overload of llogb   (function) |
| fmaxmag(FP Ext 1 TS) | generic overload of fmaxmag   (function) |
| fminmag(FP Ext 1 TS) | generic overload of fminmag   (function) |
| nextup(FP Ext 1 TS) | generic overload of nextup   (function) |
| nextdown(FP Ext 1 TS) | generic overload of nextdown   (function) |
| fromfp(FP Ext 1 TS) | generic overload of fromfp   (function) |
| ufromfp(FP Ext 1 TS) | generic overload of ufromfp   (function) |
| fromfpx(FP Ext 1 TS) | generic overload of fromfpx   (function) |
| ufromfpx(FP Ext 1 TS) | generic overload of ufromfpx   (function) |
| nextdown(FP Ext 1 TS) | generic overload of nextdown   (function) |
| totalorder(FP Ext 1 TS) | generic overload of totalorder   (function) |
| totalordermag(FP Ext 1 TS) | generic overload of totalordermag   (function) |
| fadd(FP Ext 1 TS) | generic overload of fadd   (function) |
| dadd(FP Ext 1 TS) | generic overload of dadd   (function) |
| fsub(FP Ext 1 TS) | generic overload of fsub   (function) |
| dsub(FP Ext 1 TS) | generic overload of dsub   (function) |
| fmul(FP Ext 1 TS) | generic overload of fmul   (function) |
| dmul(FP Ext 1 TS) | generic overload of dmul   (function) |
| fdiv(FP Ext 1 TS) | generic overload of fdiv   (function) |
| ddiv(FP Ext 1 TS) | generic overload of ddiv   (function) |
| ffma(FP Ext 1 TS) | generic overload of ffma   (function) |
| dfma(FP Ext 1 TS) | generic overload of dfma   (function) |
| fsqrt(FP Ext 1 TS) | generic overload of fsqrt   (function) |
| dsqrt(FP Ext 1 TS) | generic overload of dsqrt   (function) |

### Notes

The standard C macros __STDC_IEC_559__ and __STDC_IEC_559_COMPLEX__ are made obsolete by this technical specification.

All functions and macros added to the C library by this extension are only declared if a macro __STDC_WANT_IEC_60559_BFP_EXT__ is defined before the corresponding header is included.

Besides additions to the standard library, ISO/IEC TS 18661-1:2014 makes a number of changes to the core language, notably splitting floating-point control between static (controlled by the new #pragma STDC FENV_ROUND), and dynamic (controlled by fesetround). Most math.h functions respect the static rounding mode, if set, over the dynamic rounding mode.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: add to the pragma page or describe the pragma in full here? |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/experimental/fpext1&oldid=124001>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 November 2020, at 11:53.