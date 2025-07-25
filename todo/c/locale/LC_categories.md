# LC_ALL, LC_COLLATE, LC_CTYPE, LC_MONETARY, LC_NUMERIC, LC_TIME

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
| localeconv | | | | |
| lconv | | | | |
| Locale categories | | | | |
| ****LC_ALLLC_COLLATELC_CTYPELC_MONETARYLC_NUMERICLC_TIME**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<locale.h>` |  |  |
| #define LC_ALL      /\* implementation-defined \*/ |  |  |
| #define LC_COLLATE  /\* implementation-defined \*/ |  |  |
| #define LC_CTYPE    /\* implementation-defined \*/ |  |  |
| #define LC_MONETARY /\* implementation-defined \*/ |  |  |
| #define LC_NUMERIC  /\* implementation-defined \*/ |  |  |
| #define LC_TIME     /\* implementation-defined \*/ |  |  |
|  |  |  |

Each of the above macro constants expand to integer constant expressions with distinct values that are suitable for use as the first argument of setlocale.

|  |  |
| --- | --- |
| Constant | Explanation |
| `LC_ALL` | selects the entire C locale |
| `LC_COLLATE` | selects the collation category of the C locale |
| `LC_CTYPE` | selects the character classification category of the C locale |
| `LC_MONETARY` | selects the monetary formatting category of the C locale |
| `LC_NUMERIC` | selects the numeric formatting category of the C locale |
| `LC_TIME` | selects the time formatting category of the C locale |

Additional macro constants, with names that begin with `LC_` followed by at least one uppercase letter, may be defined in `locale.h`. For example, the POSIX specification requires `LC_MESSAGES` (which controls, among other things, perror and strerror), ISO/IEC 30112:2014 (2014 draft) additionally defines `LC_IDENTIFICATION`, `LC_XLITERATE`, `LC_NAME`, `LC_ADDRESS`, `LC_TELEPHONE`, `LC_PAPER`, `LC_MEASUREMENT`, and `LC_KEYBOARD`, which are supported by the GNU C library (except for `LC_XLITERATE`).

### Example

Run this code

```
#include <locale.h>
#include <stdio.h>
#include <time.h>
#include <wchar.h>
 
int main(void)
{
    setlocale(LC_ALL, "en_US.UTF-8"); // the C locale will be the UTF-8 enabled English
    setlocale(LC_NUMERIC, "de_DE.utf8"); // decimal dot will be German
    setlocale(LC_TIME, "ja_JP.utf8");    // date/time formatting will be Japanese
    wchar_t str[100];
    time_t t = time(NULL);
    wcsftime(str, 100, L"%A %c", localtime(&t));
    wprintf(L"Number: %.2f\nDate: %Ls\n", 3.14, str);
}

```

Possible output:

```
Number: 3,14
Date: 金曜日 2023年09月15日 20時04分14秒

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.11/3 Localization <locale.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.11/3 Localization <locale.h> (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.11/3 Localization <locale.h> (p: 224)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.11/3 Localization <locale.h> (p: 205)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.4 LOCALIZATION <locale.h>

### See also

|  |  |
| --- | --- |
| setlocale | gets and sets the current C locale   (function) |
| C++ documentation for locale categories | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/locale/LC_categories&oldid=180072>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 February 2025, at 20:42.