# assert

From cppreference.com
< c‎ | error
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

 Error handling

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Error codes | | | | |
| Error codes | | | | |
| errno | | | | |
| Assertions | | | | |
| ****assert**** | | | | |
| static_assert(C11)(removed in C23) | | | | |
| Bounds checking | | | | |
| set_constraint_handler_s(C11) | | | | |
| abort_handler_s(C11) | | | | |
| ignore_handler_s(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<assert.h>` |  |  |
|  |  |  |
| --- | --- | --- |
| #ifdef NDEBUG  #define assert(condition) ((void)0)  #else  #define assert(condition) /\*implementation defined\*/ #endif |  | (until C23) |
| #ifdef NDEBUG  #define assert(...) ((void)0)  #else  #define assert(...) /\*implementation defined\*/ #endif |  | (since C23) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

The definition of the macro `assert` depends on another macro, NDEBUG, which is not defined by the standard library.

If NDEBUG is defined as a macro name at the point in the source code where <assert.h> is included, then `assert` does nothing.

If NDEBUG is not defined, then `assert` checks if its argument(until C23)the expression synthesized from __VA_ARGS__(since C23) (which must have scalar type, otherwise, the behavior is undefined) compares equal to zero. If it does, `assert` outputs implementation-specific diagnostic information on the standard error output and calls abort(). The diagnostic information is required to include the text of `expression`, as well as the values of  the predefined variable __func__ and of(since C99) the predefined macros __FILE__ and __LINE__.

### Parameters

|  |  |  |
| --- | --- | --- |
| condition | - | expression of scalar type |

### Return value

(none)

### Notes

There is no standardized interface to add an additional message to `assert` errors. A portable way to include one is to use a comma operator, or use && with a string literal:

```
assert(("There are five lights", 2 + 2 == 5));
assert(2 + 2 == 5 && "There are five lights");

```

The implementation of `assert` in Microsoft CRT does not conform to C99 and later revisions, because its underlying function (`_wassert`) takes neither __func__ nor an equivalent replacement.

Even though the change of `assert` in C23 (N2829) is not a formal defect report, the C committee recommends implementations to backport the change to old modes.

### Example

Run this code

```
#include <stdio.h>
// uncomment to disable assert()
// #define NDEBUG
#include <assert.h>
#include <math.h>
 
#define TEST(...) __VA_ARGS__
 
int main(void)
{
    double x = -1.0;
    assert(x >= 0.0);
    printf("sqrt(x) = %f\n", sqrt(x));
 
    assert(TEST(x >= 0.0));
 
    return 0;
}

```

Possible output:

```
--- Output with NDEBUG not defined: ---
a.out: main.cpp:10: main: Assertion `x >= 0.0' failed.
 
--- Output with NDEBUG defined: ---
sqrt(x) = -nan

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.2.2.1 The assert macro (p: 196)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.2.1.1 The assert macro (p: 135)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.2.1.1 The assert macro (p: 186-187)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.2.1.1 The assert macro (p: 169)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.2.1.1 The assert macro

### See also

|  |  |
| --- | --- |
| abort | causes abnormal program termination (without cleaning up)   (function) |
| C++ documentation for assert | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/error/assert&oldid=173989>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 31 July 2024, at 16:21.