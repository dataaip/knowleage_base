# Variadic functions

From cppreference.com
< c
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| ****Variadic function support**** | | | | |
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

 ****Variadic functions****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| va_start | | | | |
| va_arg | | | | |
| va_copy(C99) | | | | |
| va_end | | | | |
| va_list | | | | |

Variadic functions are functions (e.g. printf) which take a variable number of arguments.

The declaration of a variadic function uses an ellipsis as the last parameter, e.g. int printf(const char\* format, ...);. See variadic arguments for additional detail on the syntax and automatic argument conversions.

Accessing the variadic arguments from the function body uses the following library facilities:

|  |  |
| --- | --- |
| Types | |
| va_list | holds the information needed by va_start, va_arg, va_end, and va_copy   (typedef) |
| Macros | |
| Defined in header `<stdarg.h>` | |
| va_start | enables access to variadic function arguments   (function macro) |
| va_arg | accesses the next variadic function argument   (function macro) |
| va_copy(C99) | makes a copy of the variadic function arguments   (function macro) |
| va_end | ends traversal of the variadic function arguments   (function macro) |

### Example

Print values of different types.

Run this code

```
#include <stdarg.h>
#include <stdio.h>
 
void simple_printf(const char* fmt, ...)
{
    va_list args;
 
    for (va_start(args, fmt); *fmt != '\0'; ++fmt)
    {
        switch(*fmt)
        {
            case 'd':
            {
                int i = va_arg(args, int);
                printf("%d\n", i);
                break;
            }
            case 'c':
            {
                // A 'char' variable will be promoted to 'int'
                // A character literal in C is already 'int' by itself
                int c = va_arg(args, int);
                printf("%c\n", c);
                break;
            }
            case 'f':
            {
                double d = va_arg(args, double);
                printf("%f\n", d);
                break;
            }
            default:
                puts("Unknown formatter!");
                goto END;
        }
    }
END:
    va_end(args);
}
 
int main(void)
{
    simple_printf("dcff", 3, 'a', 1.969, 42.5);
}

```

Output:

```
3
a
1.969000
42.50000

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.16 Variable arguments <stdarg.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.16 Variable arguments <stdarg.h> (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.16 Variable arguments <stdarg.h> (p: 269-272)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.15 Variable arguments <stdarg.h> (p: 249-252)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.8 VARIABLE ARGUMENTS <stdarg.h>

### See also

|  |  |
| --- | --- |
| C++ documentation for Variadic functions | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/variadic&oldid=180120>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 February 2025, at 01:22.