# __STDC_ENDIAN_LITTLE__, __STDC_ENDIAN_BIG__, __STDC_ENDIAN_NATIVE__

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
| ****__STDC_ENDIAN_LITTLE__ __STDC_ENDIAN_BIG__ __STDC_ENDIAN_NATIVE__****(C23)(C23)(C23) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdbit.h>` |  |  |
| #define __STDC_ENDIAN_LITTLE__ /\* implementation-defined \*/ | (1) | (since C23) |
| #define __STDC_ENDIAN_BIG__    /\* implementation-defined \*/ | (2) | (since C23) |
| #define __STDC_ENDIAN_NATIVE__ /\* implementation-defined \*/ | (3) | (since C23) |
|  |  |  |

Indicates the endianness of all scalar types:

- If all scalar types are little-endian, __STDC_ENDIAN_NATIVE__ equals __STDC_ENDIAN_LITTLE__.
- If all scalar types are big-endian, __STDC_ENDIAN_NATIVE__ equals __STDC_ENDIAN_BIG__.
- If the platform uses neither little-endian nor big-endian, __STDC_ENDIAN_NATIVE__ equals neither __STDC_ENDIAN_BIG__ nor __STDC_ENDIAN_LITTLE__.
- The values of the integer constant expressions for __STDC_ENDIAN_BIG__ and __STDC_ENDIAN_LITTLE__ are not equal.

### Example

Run this code

```
#include <stdbit.h>
#include <stdio.h>
 
int main()
{
    switch(__STDC_ENDIAN_NATIVE__)
    {
        case __STDC_ENDIAN_LITTLE__:
            printf("__STDC_ENDIAN_LITTLE__\n");
            break;
        case __STDC_ENDIAN_BIG__:
            printf("__STDC_ENDIAN_BIG__\n");
            break;
        default:
            printf("mixed-endian\n");
    }
    return __STDC_ENDIAN_NATIVE__;
}

```

Possible output:

```
mixed-endian

```

### See also

|  |  |
| --- | --- |
| C++ documentation for endian | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/numeric/bit/endian&oldid=178957>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 January 2025, at 11:35.