# clock_t

From cppreference.com
< c‎ | chrono
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

 Date and time utilities

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Time manipulation | | | | |
| difftime | | | | |
| time | | | | |
| clock | | | | |
| timespec_get(C11) | | | | |
| timespec_getres(C23) | | | | |
| Format conversions | | | | |
| asctimeasctime_s(deprecated in C23)(C11) | | | | |
| ctimectime_s(deprecated in C23)(C11) | | | | |
| strftime | | | | |
| wcsftime(C95) | | | | |
| gmtimegmtime_rgmtime_s(C23)(C11) | | | | |
| localtimelocaltime_rlocaltime_s(C23)(C11) | | | | |
| mktime | | | | |
| Constants | | | | |
| CLOCKS_PER_SEC | | | | |
| Types | | | | |
| tm | | | | |
| time_t | | | | |
| ****clock_t**** | | | | |
| timespec(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<time.h>` |  |  |
| typedef /\* unspecified \*/ clock_t; |  |  |
|  |  |  |

Arithmetic(until C11)Real(since C11) type capable of representing the processor time used by a process. It has implementation-defined range and precision.

### Example

Run this code

```
#include <stdio.h>
#include <time.h>
#include <math.h>
 
volatile double sink;
int main (void)
{
  clock_t start = clock();
 
  for(size_t i=0; i<3141592; ++i)
      sink+=sin(i);
 
  clock_t end = clock();
  double cpu_time_used = ((double) (end - start)) / CLOCKS_PER_SEC;
 
  printf("for loop took %f seconds to execute \n", cpu_time_used);
}

```

Possible output:

```
for loop took 0.271828 seconds to execute

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 7.27.1/3 Components of time (p: 284)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.27.1/3 Components of time (p: 388)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.23.1/3 Components of time (p: 338)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.12.1 Components of time

### See also

|  |  |
| --- | --- |
| clock | returns raw processor clock time since the program is started   (function) |
| CLOCKS_PER_SEC | number of processor clock ticks per second   (macro constant) |
| C++ documentation for clock_t | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/chrono/clock_t&oldid=135526>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 November 2021, at 18:56.