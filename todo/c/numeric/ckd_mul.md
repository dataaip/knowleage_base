# ckd_mul

From cppreference.com
< c‎ | numeric
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

Checked integer arithmetic

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| ckd_add(C23) | | | | |
| ckd_sub(C23) | | | | |
| ****ckd_mul****(C23) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdckdint.h>` |  |  |
| #define ckd_mul( result, a, b ) /\* implementation-defined \*/  // exposed interface: bool ckd_mul( type1\* result, type2 a, type3 b ); |  | (since C23) |
|  |  |  |

Computes the multiplication x × y and stores the result into \*result. The multiplication is performed as if both operands were represented in a signed integer type with infinite range, and the result was then converted from this integer type to type1. If the value assigned to \*result correctly represents the mathematical result of the operation, it returns false. Otherwise, it returns true. In this case, the value assigned to \*result is the mathematical result of the operation wrapped around to the width of \*result.

### Parameters

|  |  |  |
| --- | --- | --- |
| a, b | - | integer values |
| result | - | address of where result should be stored |

### Return value

false if the value assigned to \*result correctly represents the mathematical result of the multiplication, true otherwise.

### Note

Both type2 and type3 shall be any integer type other than "plain" char, bool, a bit-precise integer type, or an enumerated type, and they can be the same. \*result shall be a modifiable lvalue of any integer type other than "plain" char, bool, a bit-precise integer type, or an enumerated type.

It is recommended to produce a diagnostic message if type2 or type3 are not suitable integer types, or if \*result is not a modifiable lvalue of a suitable integer type.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.20.1 The ckd_ checked integer operation macros (p: 311)

### See also

|  |  |
| --- | --- |
| ckd_add(C23) | checked addition operation on two integers (type-generic function macro) |
| ckd_sub(C23) | checked subtraction operation on two integers (type-generic function macro) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/ckd_mul&oldid=178631>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 December 2024, at 22:37.