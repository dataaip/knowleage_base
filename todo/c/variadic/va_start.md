# va_start

From cppreference.com
< c‎ | variadic
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

 Variadic functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****va_start**** | | | | |
| va_arg | | | | |
| va_copy(C99) | | | | |
| va_end | | | | |
| va_list | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdarg.h>` |  |  |
|  |  |  |
| --- | --- | --- |
| void va_start( va_list ap, parmN ); |  | (until C23) |
| void va_start( va_list ap, ... ); |  | (since C23) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

The `va_start` macro enables access to the variable arguments following the named argument `parmN`(until C23).

`va_start` shall be invoked with an instance to a valid va_list object `ap` before any calls to va_arg.

|  |  |
| --- | --- |
| If `parmN` is declared with `register` storage class specifier, with an array type, with a function type, or with a type not compatible with the type that results from default argument promotions, the behavior is undefined. | (until C23) |
| Only the first argument passed to `va_start` is evaluated. Any additional arguments are neither expanded nor used in any way. | (since C23) |

### Parameters

|  |  |  |
| --- | --- | --- |
| ap | - | an instance of the va_list type |
| parmN | - | the named parameter preceding the first variable parameter |

### Expanded value

(none)

### Example

Run this code

```
#include <stdio.h>
#include <stdarg.h>
 
int add_nums_C99(int count, ...)
{
    int result = 0;
    va_list args;
    va_start(args, count); // count can be omitted since C23
 
    for (int i = 0; i < count; ++i) {
        result += va_arg(args, int);
    }
 
    va_end(args);
    return result;
}
 
#if __STDC_VERSION__ > 201710L
// Same as above, valid since C23
int add_nums_C23(...)
{
    int result = 0;
    va_list args;
    va_start(args);
 
    int count = va_arg(args, int);
    for (int i = 0; i < count; ++i) {
        result += va_arg(args, int);
    }
 
    va_end(args);
    return result;
}
#endif
 
int main(void)
{
    printf("%d\n", add_nums_C99(4, 25, 25, 50, 50));
#if __STDC_VERSION__ > 201710L
    printf("%d\n", add_nums_C23(4, 25, 25, 50, 50));
#endif
}

```

Possible output:

```
150
150

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.16.1.4 The va_start macro (p: 198-199)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.16.1.4 The va_start macro (p: 271-272)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.15.1.4 The va_start macro (p: 251-252)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.8.1.1 The va_start macro

### See also

|  |  |
| --- | --- |
| va_arg | accesses the next variadic function argument   (function macro) |
| va_copy(C99) | makes a copy of the variadic function arguments   (function macro) |
| va_end | ends traversal of the variadic function arguments   (function macro) |
| va_list | holds the information needed by va_start, va_arg, va_end, and va_copy   (typedef) |
| C++ documentation for va_start | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/variadic/va_start&oldid=142169>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 August 2022, at 16:15.