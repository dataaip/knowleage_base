# localeconv

From cppreference.com
< c‎ | locale
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

 Localization support

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| setlocale | | | | |
| ****localeconv**** | | | | |
| lconv | | | | |
| Locale categories | | | | |
| LC_ALLLC_COLLATELC_CTYPELC_MONETARYLC_NUMERICLC_TIME | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<locale.h>` |  |  |
| struct lconv\* localeconv(void); |  |  |
|  |  |  |

The `localeconv` function obtains a pointer to a static object of type lconv, which represents numeric and monetary formatting rules of the current C locale.

### Parameters

(none)

### Return value

pointer to the current lconv object.

### Notes

Modifying the object references through the returned pointer is undefined behavior.

`localeconv` modifies a static object, calling it from different threads without synchronization is undefined behavior.

### Example

Run this code

```
#include <locale.h>
#include <stdio.h>
 
int main(void)
{
    setlocale(LC_MONETARY, "en_IN.utf8");
    struct lconv* lc = localeconv();
    printf("Local Currency Symbol        : %s\n", lc->currency_symbol);
    printf("International Currency Symbol: %s\n", lc->int_curr_symbol);
}

```

Output:

```
Local Currency Symbol        : ₹
International Currency Symbol: INR

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.11.2.1 The localeconv function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.11.2.1 The localeconv function (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.11.2.1 The localeconv function (p: 225-230)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.11.2.1 The localeconv function (p: 206-211)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.4.2.1 The localeconv function

### See also

|  |  |
| --- | --- |
| setlocale | gets and sets the current C locale   (function) |
| lconv | formatting details, returned by ****localeconv**** (struct) |
| C++ documentation for localeconv | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/locale/localeconv&oldid=180071>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 February 2025, at 20:39.