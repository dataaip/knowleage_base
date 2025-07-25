# Numeric limits

From cppreference.com
< c‎ | types
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

 Type support

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| size_t | | | | |
| ptrdiff_t | | | | |
| nullptr_t(C23) | | | | |
| NULL | | | | |
| max_align_t(C11) | | | | |
| offsetof | | | | |
| ****Numeric limits**** | | | | |
| Fixed width integer types (C99) | | | | |

 ****Numeric limits****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| FLT_ROUNDS | | | | |
| FLT_EVAL_METHOD(C99) | | | | |

### Limits of integer types

|  |  |
| --- | --- |
| Limits of core language integer types | |
| Defined in header `<limits.h>` | |
| BOOL_WIDTH(C23) | bit width of _Bool   (macro constant) |
| CHAR_BIT | bit width of byte   (macro constant) |
| MB_LEN_MAX | maximum number of bytes in a multibyte character   (macro constant) |
| CHAR_WIDTH(C23) | bit width of char, same as `CHAR_BIT`   (macro constant) |
| CHAR_MIN | minimum value of char   (macro constant) |
| CHAR_MAX | maximum value of char   (macro constant) |
| SCHAR_WIDTHSHRT_WIDTHINT_WIDTHLONG_WIDTHLLONG_WIDTH(C23)(C23)(C23)(C23)(C23) | bit width of signed char, short, int, long, and long long respectively   (macro constant) |
| SCHAR_MINSHRT_MININT_MINLONG_MINLLONG_MIN(C99) | minimum value of signed char, short, int, long and long long respectively   (macro constant) |
| SCHAR_MAXSHRT_MAXINT_MAXLONG_MAXLLONG_MAX(C99) | maximum value of signed char, short, int, long and long long respectively   (macro constant) |
| UCHAR_WIDTHUSHRT_WIDTHUINT_WIDTHULONG_WIDTHULLONG_WIDTH(C23)(C23)(C23)(C23)(C23) | bit width of unsigned char, unsigned short, unsigned int, unsigned long, and unsigned long long respectively   (macro constant) |
| UCHAR_MAXUSHRT_MAXUINT_MAXULONG_MAXULLONG_MAX(C99) | maximum value of unsigned char, unsigned short, unsigned int, unsigned long and unsigned long long respectively   (macro constant) |
| BITINT_MAXWIDTH(C23) | maximum width N supported by the declaration of a bit-precise integer in the type specifier _BitInt(N), greater than or equal to `ULLONG_WIDTH`   (macro constant) |
| Limits of library type aliases | |
| Defined in header `<stdint.h>` | |
| PTRDIFF_WIDTH(C23) | bit width of object of ptrdiff_t type   (macro constant) |
| PTRDIFF_MIN(C99) | minimum value of ptrdiff_t   (macro constant) |
| PTRDIFF_MAX(C99) | maximum value of ptrdiff_t   (macro constant) |
| SIZE_WIDTH(C23) | bit width of object of size_t type   (macro constant) |
| SIZE_MAX(C99) | maximum value of size_t   (macro constant) |
| SIG_ATOMIC_WIDTH(C23) | bit width of object of sig_atomic_t type   (macro constant) |
| SIG_ATOMIC_MIN(C99) | minimum value of sig_atomic_t   (macro constant) |
| SIG_ATOMIC_MAX(C99) | maximum value of sig_atomic_t   (macro constant) |
| WINT_WIDTH(C23) | bit width of object of wint_t type   (macro constant) |
| WINT_MIN(C99) | minimum value of `wint_t`   (macro constant) |
| WINT_MAX(C99) | maximum value of `wint_t`   (macro constant) |
| Defined in header `<wchar.h>` | |
| Defined in header `<stdint.h>` | |
| WCHAR_WIDTH(C23) | bit width of object of wchar_t type   (macro constant) |
| WCHAR_MIN(C99) | minimum value of wchar_t   (macro constant) |
| WCHAR_MAX(C99) | maximum value of wchar_t   (macro constant) |

#### Notes

The types of these constants, other than `CHAR_BIT` and `MB_LEN_MAX`, are required to match the results of the integral promotions as applied to objects of the types they describe: `CHAR_MAX` may have type int or unsigned int, but never char. Similarly `USHRT_MAX` may not be of an unsigned type: its type may be int.

A freestanding implementation may lack sig_atomic_t and/or wint_t typedef names, in which case the `SIG_ATOMIC_*` and/or `WINT_*` macros are correspondingly absent.

#### Example

Run this code

```
#include <limits.h>
#include <stdint.h>
#include <stdio.h>
 
int main(void)
{
    printf("CHAR_BIT       = %d\n", CHAR_BIT);
    printf("MB_LEN_MAX     = %d\n\n", MB_LEN_MAX);
 
    printf("CHAR_MIN       = %+d\n", CHAR_MIN);
    printf("CHAR_MAX       = %+d\n", CHAR_MAX);
    printf("SCHAR_MIN      = %+d\n", SCHAR_MIN);
    printf("SCHAR_MAX      = %+d\n", SCHAR_MAX);
    printf("UCHAR_MAX      = %u\n\n", UCHAR_MAX);
 
    printf("SHRT_MIN       = %+d\n", SHRT_MIN);
    printf("SHRT_MAX       = %+d\n", SHRT_MAX);
    printf("USHRT_MAX      = %u\n\n", USHRT_MAX);
 
    printf("INT_MIN        = %+d\n", INT_MIN);
    printf("INT_MAX        = %+d\n", INT_MAX);
    printf("UINT_MAX       = %u\n\n", UINT_MAX);
 
    printf("LONG_MIN       = %+ld\n", LONG_MIN);
    printf("LONG_MAX       = %+ld\n", LONG_MAX);
    printf("ULONG_MAX      = %lu\n\n", ULONG_MAX);
 
    printf("LLONG_MIN      = %+lld\n", LLONG_MIN);
    printf("LLONG_MAX      = %+lld\n", LLONG_MAX);
    printf("ULLONG_MAX     = %llu\n\n", ULLONG_MAX);
 
    printf("PTRDIFF_MIN    = %td\n", PTRDIFF_MIN);
    printf("PTRDIFF_MAX    = %+td\n", PTRDIFF_MAX);
    printf("SIZE_MAX       = %zu\n", SIZE_MAX);
    printf("SIG_ATOMIC_MIN = %+jd\n",(intmax_t)SIG_ATOMIC_MIN);
    printf("SIG_ATOMIC_MAX = %+jd\n",(intmax_t)SIG_ATOMIC_MAX);
    printf("WCHAR_MIN      = %+jd\n",(intmax_t)WCHAR_MIN);
    printf("WCHAR_MAX      = %+jd\n",(intmax_t)WCHAR_MAX);
    printf("WINT_MIN       = %jd\n", (intmax_t)WINT_MIN);
    printf("WINT_MAX       = %jd\n", (intmax_t)WINT_MAX);
}

```

Possible output:

```
CHAR_BIT       = 8
MB_LEN_MAX     = 16
 
CHAR_MIN       = -128
CHAR_MAX       = +127
SCHAR_MIN      = -128
SCHAR_MAX      = +127
UCHAR_MAX      = 255
 
SHRT_MIN       = -32768
SHRT_MAX       = +32767
USHRT_MAX      = 65535
 
INT_MIN        = -2147483648
INT_MAX        = +2147483647
UINT_MAX       = 4294967295
 
LONG_MIN       = -9223372036854775808
LONG_MAX       = +9223372036854775807
ULONG_MAX      = 18446744073709551615
 
LLONG_MIN      = -9223372036854775808
LLONG_MAX      = +9223372036854775807
ULLONG_MAX     = 18446744073709551615
 
PTRDIFF_MIN    = -9223372036854775808
PTRDIFF_MAX    = +9223372036854775807
SIZE_MAX       = 18446744073709551615
SIG_ATOMIC_MIN = -2147483648
SIG_ATOMIC_MAX = +2147483647
WCHAR_MIN      = -2147483648
WCHAR_MAX      = +2147483647
WINT_MIN       = 0
WINT_MAX       = 4294967295

```

### Limits of floating-point types

|  |  |
| --- | --- |
| Defined in header `<float.h>` | |
| FLT_RADIX | the radix (integer base) used by the representation of all three floating-point types   (macro constant) |
| DECIMAL_DIG(C99) | conversion from long double to decimal with at least `DECIMAL_DIG` digits and back to long double is the identity conversion: this is the decimal precision required to serialize/deserialize a long double   (macro constant) |
| FLT_DECIMAL_DIGDBL_DECIMAL_DIGLDBL_DECIMAL_DIG(C11) | conversion from float/double/long double to decimal with at least `FLT_DECIMAL_DIG`/`DBL_DECIMAL_DIG`/`LDBL_DECIMAL_DIG` digits and back is the identity conversion: this is the decimal precision required to serialize/deserialize a floating-point value. Defined to at least 6, 10, and 10 respectively, or 9 for IEEE float and 17 for IEEE double (see also the C++ analog: `max_digits10`)   (macro constant) |
| FLT_MINDBL_MINLDBL_MIN | minimum, normalized, positive value of float, double and long double respectively   (macro constant) |
| FLT_TRUE_MINDBL_TRUE_MINLDBL_TRUE_MIN(C11) | minimum positive value of float, double and long double respectively   (macro constant) |
| FLT_MAXDBL_MAXLDBL_MAX | maximum finite value of float, double and long double respectively   (macro constant) |
| FLT_EPSILONDBL_EPSILONLDBL_EPSILON | absolute value difference between 1.0 and the next representable value for float, double and long double respectively   (macro constant) |
| FLT_DIGDBL_DIGLDBL_DIG | number of decimal digits that are guaranteed to be preserved in text → float/double/long double → text roundtrip without change due to rounding or overflow (see the C++ analog `digits10` for detail)   (macro constant) |
| FLT_MANT_DIGDBL_MANT_DIGLDBL_MANT_DIG | number of base-`FLT_RADIX` digits that are in the floating-point mantissa and that can be represented without losing precision for float, double and long double respectively   (macro constant) |
| FLT_MIN_EXPDBL_MIN_EXPLDBL_MIN_EXP | minimum negative integer such that `FLT_RADIX` raised by power one less than that integer is a normalized float, double and long double respectively   (macro constant) |
| FLT_MIN_10_EXPDBL_MIN_10_EXPLDBL_MIN_10_EXP | minimum negative integer such that 10 raised to that power is a normalized float, double and long double respectively   (macro constant) |
| FLT_MAX_EXPDBL_MAX_EXPLDBL_MAX_EXP | maximum positive integer such that `FLT_RADIX` raised by power one less than that integer is a representable finite float, double and long double respectively   (macro constant) |
| FLT_MAX_10_EXPDBL_MAX_10_EXPLDBL_MAX_10_EXP | maximum positive integer such that 10 raised to that power is a representable finite float, double and long double respectively   (macro constant) |
| FLT_ROUNDS | rounding mode of floating-point arithmetic   (macro constant) |
| FLT_EVAL_METHOD(C99) | specifies in what precision all arithmetic operations are done   (macro constant) |

|  |  |
| --- | --- |
| FLT_HAS_SUBNORMDBL_HAS_SUBNORMLDBL_HAS_SUBNORM(C11)(deprecated in C23) | whether the type supports subnormal (denormal) numbers: -1 – indeterminable, ​0​ – absent, 1 – present   (macro constant) |

#### Example

Run this code

```
#include <float.h>
#include <math.h>
#include <stdio.h>
 
int main(void)
{
    printf("DECIMAL_DIG     = %d\n", DECIMAL_DIG);
    printf("FLT_DECIMAL_DIG = %d\n", FLT_DECIMAL_DIG);
    printf("FLT_RADIX       = %d\n", FLT_RADIX);
    printf("FLT_MIN         = %e\n", FLT_MIN);
    printf("FLT_MAX         = %e\n", FLT_MAX);
    printf("FLT_EPSILON     = %e\n", FLT_EPSILON);
    printf("FLT_DIG         = %d\n", FLT_DIG);
    printf("FLT_MANT_DIG    = %d\n", FLT_MANT_DIG);
    printf("FLT_MIN_EXP     = %d\n", FLT_MIN_EXP);
    printf("FLT_MIN_10_EXP  = %d\n", FLT_MIN_10_EXP);
    printf("FLT_MAX_EXP     = %d\n", FLT_MAX_EXP);
    printf("FLT_MAX_10_EXP  = %d\n", FLT_MAX_10_EXP);
    printf("FLT_ROUNDS      = %d\n", FLT_ROUNDS);
    printf("FLT_EVAL_METHOD = %d\n", FLT_EVAL_METHOD);
    printf("FLT_HAS_SUBNORM = %d\n", FLT_HAS_SUBNORM);
}

```

Possible output:

```
DECIMAL_DIG     = 37
FLT_DECIMAL_DIG = 9
FLT_RADIX       = 2
FLT_MIN         = 1.175494e-38
FLT_MAX         = 3.402823e+38
FLT_EPSILON     = 1.192093e-07
FLT_DIG         = 6
FLT_MANT_DIG    = 24
FLT_MIN_EXP     = -125
FLT_MIN_10_EXP  = -37
FLT_MAX_EXP     = 128
FLT_MAX_10_EXP  = 38
FLT_ROUNDS      = 1
FLT_EVAL_METHOD = 1
FLT_HAS_SUBNORM = 1

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 5.2.4.2 Numerical limits (p: TBD)

:   - 7.22.3 Limits of other integer types (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 5.2.4.2 Numerical limits (p: 20-27)

:   - 7.20.3 Limits of other integer types (p: 215-216)

- C11 standard (ISO/IEC 9899:2011):

:   - 5.2.4.2 Numerical limits (p: 26-34)

:   - 7.20.3 Limits of other integer types (p: 293-294)

- C99 standard (ISO/IEC 9899:1999):

:   - 5.2.4.2 Numerical limits (p: 21-28)

:   - 7.18.3 Limits of other integer types (p: 259-260)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 2.2.4.2 Numerical limits

### See also

|  |  |
| --- | --- |
| C++ documentation for C numeric limits interface | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/types/limits&oldid=180103>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 February 2025, at 16:06.