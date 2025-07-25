# Bit manipulation (since C23)

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

Bit manipulation

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| stdc_leading_zeros(C23) | | | | |
| stdc_leading_ones")(C23) | | | | |
| stdc_trailing_zeros")(C23) | | | | |
| stdc_trailing_ones")(C23) | | | | |
| stdc_first_leading_zero")(C23) | | | | |
| stdc_first_leading_one")(C23) | | | | |
| stdc_first_trailing_zero")(C23) | | | | |
| stdc_first_trailing_one")(C23) | | | | |
| stdc_count_zeros")(C23) | | | | |
| stdc_count_ones")(C23) | | | | |
| stdc_has_single_bit")(C23) | | | | |
| stdc_bit_width")(C23) | | | | |
| stdc_bit_floor")(C23) | | | | |
| stdc_bit_ceil")(C23) | | | | |
| Macro constants | | | | |
| __STDC_ENDIAN_LITTLE__ __STDC_ENDIAN_BIG__ __STDC_ENDIAN_NATIVE__(C23)(C23)(C23) | | | | |

|  |  |
| --- | --- |
| Functions | |
| Defined in header `<stdbit.h>` | |
| stdc_leading_zeros(C23) | counts the number of consecutive ​0​ bits, starting from the most significant bit (type-generic function macro) |
| stdc_leading_ones")(C23) | counts the number of consecutive 1 bits, starting from the most significant bit (type-generic function macro) |
| stdc_trailing_zeros")(C23) | counts the number of consecutive ​0​ bits, starting from the least significant bit (type-generic function macro) |
| stdc_trailing_ones")(C23) | counts the number of consecutive 1 bits, starting from the least significant bit (type-generic function macro) |
| stdc_first_leading_zero")(C23) | finds the first position of ​0​ bit, starting from the most significant bit (type-generic function macro) |
| stdc_first_leading_one")(C23) | finds the first position of 1 bit, starting from the most significant bit (type-generic function macro) |
| stdc_first_trailing_zero")(C23) | finds the first position of ​0​ bit, starting from the least significant bit (type-generic function macro) |
| stdc_first_trailing_one")(C23) | finds the first position of 1 bit, starting from the least significant bit (type-generic function macro) |
| stdc_count_zeros")(C23) | counts the number of ​0​ bits in an unsigned integer (type-generic function macro) |
| stdc_count_ones")(C23) | counts the number of 1 bits in an unsigned integer (type-generic function macro) |
| stdc_has_single_bit")(C23) | checks if a number is an integral power of 2 (type-generic function macro) |
| stdc_bit_width")(C23) | finds the smallest number of bits needed to represent the given value (type-generic function macro) |
| stdc_bit_floor")(C23) | finds the largest integral power of 2 not greater than the given value (type-generic function macro) |
| stdc_bit_ceil")(C23) | finds the smallest integral power of 2 not less than the given value (type-generic function macro) |
| Macro constants | |
| Defined in header `<stdbit.h>` | |
| __STDC_ENDIAN_LITTLE____STDC_ENDIAN_BIG__ __STDC_ENDIAN_NATIVE__(C23) | indicates the endianness of scalar types   (macro constant) |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.18 Bit and byte utilities <stdbit.h>

### See also

|  |  |
| --- | --- |
| C++ documentation for Bit manipulation | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/bit_manip&oldid=180023>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 February 2025, at 08:22.