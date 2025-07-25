# Macro Symbol Index

From cppreference.com
< c‎ | symbol index
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

This page tries to list all the macro symbols that are available from the **Standard Library**. The symbols are written as follows:

- Function-like macro names with `()`.
- Type-generic macro names marked with (generic).

## _ A B C D E F H I K L M N O P R S T U V W X

### _ (underscore)

__alignas_is_defined (since C11)  
__alignof_is_defined (since C11)  
__bool_true_false_are_defined (since C99)  
_Complex_I (since C99)  
_Imaginary_I (since C99)  
_IOFBF  
_IOLBF  
_IONBF

### A

acos() (generic) (since C99)  
acosh() (generic) (since C99)  
alignas (keyword macro) (since C11)  
alignof (keyword macro) (since C11)  
and (operator macro) (since C95)  
and_eq (operator macro) (since C95)  
asin() (generic) (since C99)  
asinh() (generic) (since C99)  
assert()  
atan() (generic) (since C99)  
atan2() (generic) (since C99)  
atanh() (generic) (since C99)

| `ATOMIC_TYPE_LOCK_FREE` |
| --- |
| ATOMIC_BOOL_LOCK_FREE (since C11)  ATOMIC_CHAR_LOCK_FREE (since C11)  ATOMIC_CHAR16_T_LOCK_FREE (since C11)  ATOMIC_CHAR32_T_LOCK_FREE (since C11)  ATOMIC_INT_LOCK_FREE (since C11)  ATOMIC_LONG_LOCK_FREE (since C11)  ATOMIC_POINTER_LOCK_FREE (since C11)  ATOMIC_LLONG_LOCK_FREE (since C11)  ATOMIC_SHORT_LOCK_FREE (since C11)  ATOMIC_WCHAR_T_LOCK_FREE (since C11) |

ATOMIC_FLAG_INIT (since C11)  
ATOMIC_VAR_INIT() (since C11)(deprecated in C17)

### B

bitand (operator macro) (since C95)  
bitor (operator macro) (since C95)  
bool (keyword macro) (since C99)  
BOOL_WIDTH (since C23)  
BUFSIZ

### C

carg() (generic) (since C99)  
cbrt() (generic) (since C99)  
ceil() (generic) (since C99)  
CHAR_BIT  
CHAR_MAX  
CHAR_MIN  
CHAR_WIDTH (since C23)  
cimag() (generic) (since C99)  
CLOCKS_PER_SEC  
CMPLX() (since C11)  
CMPLXF() (since C11)  
CMPLXL() (since C11)  
compl (operator macro) (since C95)  
complex (keyword macro) (since C99)  
conj() (generic) (since C99)  
copysign() (generic) (since C99)  
cos() (generic) (since C99)  
cosh() (generic) (since C99)  
cproj() (generic) (since C99)  
creal() (generic) (since C99)

### D

DBL_DECIMAL_DIG (since C11)  
DBL_DIG  
DBL_EPSILON  
DBL_HAS_SUBNORM (since C11)  
DBL_MANT_DIG  
DBL_MAX  
DBL_MAX_10_EXP  
DBL_MAX_EXP  
DBL_MIN  
DBL_MIN_10_EXP  
DBL_MIN_EXP  
DBL_TRUE_MIN (since C11)  
DECIMAL_DIG (since C99)

### E

EDOM  
EILSEQ (since C95)  
EOF  
ERANGE  
erf() (generic) (since C99)  
erfc() (generic) (since C99)  
errno (macro variable)  
EXIT_FAILURE  
EXIT_SUCCESS  
exp() (generic) (since C99)  
exp2() (generic) (since C99)  
expm1() (generic) (since C99)

### F

fabs() (generic) (since C99)  
false (since C99)  
fdim() (generic) (since C99)  
FE_ALL_EXCEPT (since C99)  
FE_DFL_ENV (since C99)  
FE_DIVBYZERO (since C99)  
FE_DOWNWARD (since C99)  
FE_INEXACT (since C99)  
FE_INVALID (since C99)  
FE_OVERFLOW (since C99)  
FE_TONEAREST (since C99)  
FE_TOWARDZERO (since C99)  
FE_UNDERFLOW (since C99)  
FE_UPWARD (since C99)  
FILENAME_MAX  
floor() (generic) (since C99)  
FLT_DECIMAL_DIG (since C11)  
FLT_DIG  
FLT_EPSILON  
FLT_EVAL_METHOD (since C99)  
FLT_HAS_SUBNORM (since C11)  
FLT_MANT_DIG  
FLT_MAX  
FLT_MAX_10_EXP  
FLT_MAX_EXP  
FLT_MIN  
FLT_MIN_10_EXP  
FLT_MIN_EXP  
FLT_RADIX  
FLT_ROUNDS  
FLT_TRUE_MIN (since C11)  
fma() (generic) (since C99)  
fmax() (generic) (since C99)  
fmin() (generic) (since C99)  
fmod() (generic) (since C99)  
FOPEN_MAX  
FP_FAST_FMA (since C99)  
FP_FAST_FMAF (since C99)  
FP_FAST_FMAL (since C99)  
FP_ILOGB0 (since C99)  
FP_ILOGBNAN (since C99)  
FP_INFINITE (since C99)  
FP_NAN (since C99)  
FP_NORMAL (since C99)  
FP_SUBNORMAL (since C99)  
FP_ZERO (since C99)  
fpclassify() (since C99)  
frexp() (generic) (since C99)

### H

HUGE_VAL  
HUGE_VALF (since C99)  
HUGE_VALL (since C99)  
hypot() (generic) (since C99)

### I

I (since C99)  
ilogb() (generic) (since C99)  
imaginary (keyword macro) (since C99)  
INFINITY (since C99)

| `INTWIDTH_MAX` |
| --- |
| INT_FAST16_MAX (since C99)  INT_FAST32_MAX (since C99)  INT_FAST64_MAX (since C99)  INT_FAST8_MAX (since C99)  INT_LEAST16_MAX (since C99)  INT_LEAST32_MAX (since C99)  INT_LEAST64_MAX (since C99)  INT_LEAST8_MAX (since C99)  INT16_MAX (since C99)  INT32_MAX (since C99)  INT64_MAX (since C99)  INT8_MAX (since C99)  INTMAX_MAX (since C99)  INTPTR_MAX (since C99) |

| `INTWIDTH_MIN` |
| --- |
| INT_FAST16_MIN (since C99)  INT_FAST32_MIN (since C99)  INT_FAST64_MIN (since C99)  INT_FAST8_MIN (since C99)  INT_LEAST16_MIN (since C99)  INT_LEAST32_MIN (since C99)  INT_LEAST64_MIN (since C99)  INT_LEAST8_MIN (since C99)  INT16_MIN (since C99)  INT32_MIN (since C99)  INT64_MIN (since C99)  INT8_MIN (since C99)  INTMAX_MIN (since C99)  INTPTR_MIN (since C99) |

| `INTWIDTH_WIDTH` |
| --- |
| INT_FAST16_WIDTH (since C23)  INT_FAST32_WIDTH (since C23)  INT_FAST64_WIDTH (since C23)  INT_FAST8_WIDTH (since C23)  INT_LEAST16_WIDTH (since C23)  INT_LEAST32_WIDTH (since C23)  INT_LEAST64_WIDTH (since C23)  INT_LEAST8_WIDTH (since C23)  INT16_WIDTH (since C23)  INT32_WIDTH (since C23)  INT64_WIDTH (since C23)  INT8_WIDTH (since C23)  INTMAX_WIDTH (since C23)  INTPTR_WIDTH (since C23) |

INT_MAX  
INT_MIN  
INT_WIDTH (since C23)  
INT16_C() (since C99)  
INT32_C() (since C99)  
INT64_C() (since C99)  
INT8_C() (since C99)  
INTMAX_C() (since C99)  
isfinite() (since C99)  
isgreater() (since C99)  
isgreaterequal() (since C99)  
isinf() (since C99)  
isless() (since C99)  
islessequal() (since C99)  
islessgreater() (since C99)  
isnan() (since C99)  
isnormal() (since C99)  
isunordered() (since C99)

### K

kill_dependency() (since C11)

### L

L_tmpnam  
L_tmpnam_s (since C11)  
LC_ALL  
LC_COLLATE  
LC_CTYPE  
LC_MONETARY  
LC_NUMERIC  
LC_TIME  
LDBL_DECIMAL_DIG (since C11)  
LDBL_DIG  
LDBL_EPSILON  
LDBL_HAS_SUBNORM (since C11)  
LDBL_MANT_DIG  
LDBL_MAX  
LDBL_MAX_10_EXP  
LDBL_MAX_EXP  
LDBL_MIN  
LDBL_MIN_10_EXP  
LDBL_MIN_EXP  
LDBL_TRUE_MIN (since C11)  
ldexp() (generic) (since C99)  
lgamma() (generic) (since C99)  
LLONG_MAX (since C99)  
LLONG_MIN (since C99)  
LLONG_WIDTH (since C23)  
llrint() (generic) (since C99)  
llround() (generic) (since C99)  
log() (generic) (since C99)  
log10() (generic) (since C99)  
log1p() (generic) (since C99)  
log2() (generic) (since C99)  
logb() (generic) (since C99)  
LONG_MAX  
LONG_MIN  
LONG_WIDTH (since C23)  
lrint() (generic) (since C99)  
lround() (generic) (since C99)

### M

MATH_ERREXCEPT (since C99)  
math_errhandling (since C99)  
MATH_ERRNO (since C99)  
MB_CUR_MAX (macro variable)  
MB_LEN_MAX

### N

NAN (since C99)  
nearbyint() (generic) (since C99)  
nextafter() (generic) (since C99)  
nexttoward() (generic) (since C99)  
noreturn (keyword macro) (since C11)  
not (operator macro) (since C95)  
not_eq (operator macro) (since C95)  
NULL

### O

offsetof()  
ONCE_FLAG_INIT (since C11)  
or (operator macro) (since C95)  
or_eq (operator macro) (since C95)

### P

pow() (generic) (since C99)

| `PRI{d i o u x X}WIDTH`  (macro string) |
| --- |
| PRId16 (since C99)  PRId32 (since C99)  PRId64 (since C99)  PRId8 (since C99)  PRIdFAST16 (since C99)  PRIdFAST32 (since C99)  PRIdFAST64 (since C99)  PRIdFAST8 (since C99)  PRIdLEAST16 (since C99)  PRIdLEAST32 (since C99)  PRIdLEAST64 (since C99)  PRIdLEAST8 (since C99)  PRIdMAX (since C99)  PRIdPTR (since C99)  PRIi16 (since C99)  PRIi32 (since C99)  PRIi64 (since C99)  PRIi8 (since C99)  PRIiFAST16 (since C99)  PRIiFAST32 (since C99)  PRIiFAST64 (since C99)  PRIiFAST8 (since C99)  PRIiLEAST16 (since C99)  PRIiLEAST32 (since C99)  PRIiLEAST64 (since C99)  PRIiLEAST8 (since C99)  PRIiMAX (since C99)  PRIiPTR (since C99)  PRIo16 (since C99)  PRIo32 (since C99)  PRIo64 (since C99)  PRIo8 (since C99)  PRIoFAST16 (since C99)  PRIoFAST32 (since C99)  PRIoFAST64 (since C99)  PRIoFAST8 (since C99)  PRIoLEAST16 (since C99)  PRIoLEAST32 (since C99)  PRIoLEAST64 (since C99)  PRIoLEAST8 (since C99)  PRIoMAX (since C99)  PRIoPTR (since C99)  PRIu16 (since C99)  PRIu32 (since C99)  PRIu64 (since C99)  PRIu8 (since C99)  PRIuFAST16 (since C99)  PRIuFAST32 (since C99)  PRIuFAST64 (since C99)  PRIuFAST8 (since C99)  PRIuLEAST16 (since C99)  PRIuLEAST32 (since C99)  PRIuLEAST64 (since C99)  PRIuLEAST8 (since C99)  PRIuMAX (since C99)  PRIuPTR (since C99)  PRIx16 (since C99)  PRIX16 (since C99)  PRIx32 (since C99)  PRIX32 (since C99)  PRIx64 (since C99)  PRIX64 (since C99)  PRIx8 (since C99)  PRIX8 (since C99)  PRIxFAST16 (since C99)  PRIXFAST16 (since C99)  PRIxFAST32 (since C99)  PRIXFAST32 (since C99)  PRIxFAST64 (since C99)  PRIXFAST64 (since C99)  PRIxFAST8 (since C99)  PRIXFAST8 (since C99)  PRIxLEAST16 (since C99)  PRIXLEAST16 (since C99)  PRIxLEAST32 (since C99)  PRIXLEAST32 (since C99)  PRIxLEAST64 (since C99)  PRIXLEAST64 (since C99)  PRIxLEAST8 (since C99)  PRIXLEAST8 (since C99)  PRIxMAX (since C99)  PRIXMAX (since C99)  PRIxPTR (since C99)  PRIXPTR (since C99) |

PTRDIFF_MAX (since C99)  
PTRDIFF_MIN (since C99)  
PTRDIFF_WIDTH (since C23)

### R

RAND_MAX  
remainder() (generic) (since C99)  
remquo() (generic) (since C99)  
rint() (generic) (since C99)  
round() (generic) (since C99)  
RSIZE_MAX (macro variable) (since C11)

### S

scalbln() (generic) (since C99)  
scalbn() (generic) (since C99)  
SCHAR_MAX  
SCHAR_MIN  
SCHAR_WIDTH (since C23)

| `SCN{d i o u x}WIDTH`  (macro string) |
| --- |
| SCNd16 (since C99)  SCNd32 (since C99)  SCNd64 (since C99)  SCNd8 (since C99)  SCNdFAST16 (since C99)  SCNdFAST32 (since C99)  SCNdFAST64 (since C99)  SCNdFAST8 (since C99)  SCNdLEAST16 (since C99)  SCNdLEAST32 (since C99)  SCNdLEAST64 (since C99)  SCNdLEAST8 (since C99)  SCNdMAX (since C99)  SCNdPTR (since C99)  SCNi16 (since C99)  SCNi32 (since C99)  SCNi64 (since C99)  SCNi8 (since C99)  SCNiFAST16 (since C99)  SCNiFAST32 (since C99)  SCNiFAST64 (since C99)  SCNiFAST8 (since C99)  SCNiLEAST16 (since C99)  SCNiLEAST32 (since C99)  SCNiLEAST64 (since C99)  SCNiLEAST8 (since C99)  SCNiMAX (since C99)  SCNiPTR (since C99)  SCNo16 (since C99)  SCNo32 (since C99)  SCNo64 (since C99)  SCNo8 (since C99)  SCNoFAST16 (since C99)  SCNoFAST32 (since C99)  SCNoFAST64 (since C99)  SCNoFAST8 (since C99)  SCNoLEAST16 (since C99)  SCNoLEAST32 (since C99)  SCNoLEAST64 (since C99)  SCNoLEAST8 (since C99)  SCNoMAX (since C99)  SCNoPTR (since C99)  SCNu16 (since C99)  SCNu32 (since C99)  SCNu64 (since C99)  SCNu8 (since C99)  SCNuFAST16 (since C99)  SCNuFAST32 (since C99)  SCNuFAST64 (since C99)  SCNuFAST8 (since C99)  SCNuLEAST16 (since C99)  SCNuLEAST32 (since C99)  SCNuLEAST64 (since C99)  SCNuLEAST8 (since C99)  SCNuMAX (since C99)  SCNuPTR (since C99)  SCNx16 (since C99)  SCNx32 (since C99)  SCNx64 (since C99)  SCNx8 (since C99)  SCNxFAST16 (since C99)  SCNxFAST32 (since C99)  SCNxFAST64 (since C99)  SCNxFAST8 (since C99)  SCNxLEAST16 (since C99)  SCNxLEAST32 (since C99)  SCNxLEAST64 (since C99)  SCNxLEAST8 (since C99)  SCNxMAX (since C99)  SCNxPTR (since C99) |

SEEK_CUR  
SEEK_END  
SEEK_SET  
setjmp()  
SHRT_MAX  
SHRT_MIN  
SHRT_WIDTH (since C23)  
SIG_ATOMIC_MAX (since C99)  
SIG_ATOMIC_MIN (since C99)  
SIG_ATOMIC_WIDTH (since C23)  
SIG_DFL  
SIG_ERR  
SIG_IGN  
SIGABRT  
SIGFPE  
SIGILL  
SIGINT  
signbit() (since C99)  
SIGSEGV  
SIGTERM  
sin() (generic) (since C99)  
sinh() (generic) (since C99)  
SIZE_MAX (since C99)  
SIZE_WIDTH (since C23)  
sqrt() (generic) (since C99)  
static_assert (keyword macro) (since C11)  
stderr  
stdin  
stdout

### T

tan() (generic) (since C99)  
tanh() (generic) (since C99)  
tgamma() (generic) (since C99)  
thread_local (keyword macro) (since C11)  
TIME_UTC (since C11)  
TMP_MAX  
TMP_MAX_S (since C11)  
true (since C99)  
trunc() (generic) (since C99)  
TSS_DTOR_ITERATIONS (since C11)

### U

UCHAR_MAX  
UCHAR_WIDTH (since C23)

| `UINTWIDTH_MAX` |
| --- |
| UINT_FAST16_MAX (since C99)  UINT_FAST32_MAX (since C99)  UINT_FAST64_MAX (since C99)  UINT_FAST8_MAX (since C99)  UINT_LEAST16_MAX (since C99)  UINT_LEAST32_MAX (since C99)  UINT_LEAST64_MAX (since C99)  UINT_LEAST8_MAX (since C99)  UINT16_MAX (since C99)  UINT32_MAX (since C99)  UINT64_MAX (since C99)  UINT8_MAX (since C99)  UINTMAX_MAX (since C99)  UINTPTR_MAX (since C99) |

| `UINTWIDTH_WIDTH` |
| --- |
| UINT_FAST16_WIDTH (since C23)  UINT_FAST32_WIDTH (since C23)  UINT_FAST64_WIDTH (since C23)  UINT_FAST8_WIDTH (since C23)  UINT_LEAST16_WIDTH (since C23)  UINT_LEAST32_WIDTH (since C23)  UINT_LEAST64_WIDTH (since C23)  UINT_LEAST8_WIDTH (since C23)  UINT16_WIDTH (since C23)  UINT32_WIDTH (since C23)  UINT64_WIDTH (since C23)  UINT8_WIDTH (since C23)  UINTMAX_WIDTH (since C23)  UINTPTR_WIDTH (since C23) |

UINT_MAX  
UINT_WIDTH (since C23)  
UINT16_C() (since C99)  
UINT32_C() (since C99)  
UINT64_C() (since C99)  
UINT8_C() (since C99)  
UINTMAX_C() (since C99)  
ULLONG_MAX (since C99)  
ULLONG_WIDTH (since C23)  
ULONG_MAX  
ULONG_WIDTH (since C23)  
USHRT_MAX  
USHRT_WIDTH (since C23)

### V

va_arg()  
va_copy() (since C99)  
va_end()  
va_list  
va_start()

### W

WCHAR_MAX (since C99)  
WCHAR_MIN (since C99)  
WCHAR_WIDTH (since C23)  
WEOF (since C95)  
WINT_MAX (since C99)  
WINT_MIN (since C99)  
WINT_WIDTH (since C23)

### X

xor (operator macro) (since C95)  
xor_eq (operator macro) (since C95)

### See also

|  |  |
| --- | --- |
| C++ documentation for Macro Symbol Index | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/symbol_index/macro&oldid=130989>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 June 2021, at 10:19.