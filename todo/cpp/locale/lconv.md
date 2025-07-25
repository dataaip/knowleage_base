# std::lconv

From cppreference.com
< cpp‎ | locale
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Freestanding and hosted | | | | |
| Language | | | | |
| Standard library | | | | |
| Standard library headers | | | | |
| Named requirements | | | | |
| Feature test macros (C++20) | | | | |
| Language support library | | | | |
| Concepts library (C++20) | | | | |
| Diagnostics library | | | | |
| Memory management library | | | | |
| Metaprogramming library (C++11) | | | | |
| General utilities library | | | | |
| Containers library | | | | |
| Iterators library | | | | |
| Ranges library (C++20) | | | | |
| Algorithms library | | | | |
| Strings library | | | | |
| Text processing library | | | | |
| Numerics library | | | | |
| Date and time library | | | | |
| Input/output library | | | | |
| Filesystem library (C++17) | | | | |
| Concurrency support library (C++11) | | | | |
| Execution support library (C++26) | | | | |
| Technical specifications | | | | |
| Symbols index | | | | |
| External libraries | | | | |

Text processing library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Localization library | | | | |
| Regular expressions library (C++11) | | | | |
| Formatting library (C++20) | | | | |
| Null-terminated sequence utilities | | | | |
| Byte strings | | | | |
| Multibyte strings | | | | |
| Wide strings | | | | |
| Primitive numeric conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | to_chars(C++17) | | | | | | to_chars_result(C++17) | | | | | | from_chars(C++17) | | | | | | from_chars_result(C++17) | | | | | | chars_format(C++17) | | | | | |
| Text encoding identifications | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | text_encoding(C++26) | | | | | |

Localization library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Locales and facets | | | | | | Locales | | | | | | has_facet | | | | | | use_facet | | | | | | locale | | | | | | Facet category base classes | | | | | | ctype_base | | | | | | codecvt_base | | | | | | messages_base | | | | | | time_base | | | | | | money_base | | | | | | ctype facets | | | | | | ctype | | | | | | ctype<char> | | | | | | ctype_byname | | | | | | codecvt | | | | | | codecvt_byname | | | | | | numeric facets | | | | | | num_get | | | | | | num_put | | | | | | numpunct | | | | | | numpunct_byname | | | | | | collate facets | | | | | | collate | | | | | | collate_byname | | | | | | time facets | | | | | | time_get | | | | | | time_put | | | | | | time_get_byname | | | | | | time_put_byname | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | monetary facets | | | | | | money_get | | | | | | money_put | | | | | | moneypunct | | | | | | moneypunct_byname | | | | | | messages facets | | | | | | messages | | | | | | messages_byname | | | | | | Character classification and conversion | | | | | | Character classification | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isspace | | | | | | iscntrl | | | | | | isupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | islower | | | | | | isalpha | | | | | | ispunct | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isdigit | | | | | | isxdigit | | | | | | isalnum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isblank(C++11) | | | | | | isprint | | | | | | isgraph | | | | | | | | Character conversions | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | toupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tolower | | | | | | | | String and stream conversions | | | | | | wstring_convert(C++11/17/26\*) | | | | | | wbuffer_convert(C++11/17/26\*) | | | | | | Unicode conversion facets | | | | | | codecvt_utf8(C++11/17/26\*) | | | | | | codecvt_utf16(C++11/17/26\*) | | | | | | codecvt_utf8_utf16(C++11/17/26\*) | | | | | | codecvt_mode(C++11/17/26\*) | | | | | | C library locales | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | LC_ALLLC_COLLATELC_CTYPELC_MONETARYLC_NUMERICLC_TIME | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setlocale | | | | | | localeconv | | | | | | ****lconv**** | | | | | |  | | | | | |  | | | | | |  | | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<clocale>` |  |  |
| struct lconv; |  |  |
|  |  |  |

The class `std::lconv` contains numeric and monetary formatting rules as defined by a C locale. Objects of this struct may be obtained with std::localeconv. The members of `std::lconv` are values of type char and of type char\*. Each char\* member except `decimal_point` may be pointing at a null character (that is, at an empty C-string). The members of type char are all non-negative numbers, any of which may be CHAR_MAX if the corresponding value is not available in the current C locale.

### Member objects

#### Non-monetary numeric formatting parameters

|  |  |
| --- | --- |
| char\* decimal_point | the character used as the decimal point   (public member object) |
| char\* thousands_sep | the character used to separate groups of digits before the decimal point   (public member object) |
| char\* grouping | a string whose elements indicate the sizes of digit groups   (public member object) |

#### Monetary numeric formatting parameters

|  |  |
| --- | --- |
| char\* mon_decimal_point | the character used as the decimal point   (public member object) |
| char\* mon_thousands_sep | the character used to separate groups of digits before the decimal point   (public member object) |
| char\* mon_grouping | a string whose elements indicate the sizes of digit groups   (public member object) |
| char\* positive_sign | a string used to indicate non-negative monetary quantity   (public member object) |
| char\* negative_sign | a string used to indicate negative monetary quantity   (public member object) |

#### Local monetary numeric formatting parameters

|  |  |
| --- | --- |
| char\* currency_symbol | the symbol used for currency in the current C locale   (public member object) |
| char frac_digits | the number of digits after the decimal point to display in a monetary quantity   (public member object) |
| char p_cs_precedes | 1 if currency_symbol is placed before non-negative value, ​0​ if after   (public member object) |
| char n_cs_precedes | 1 if currency_symbol is placed before negative value, ​0​ if after   (public member object) |
| char p_sep_by_space | indicates the separation of `currency_symbol`, `positive_sign`, and the non-negative monetary value   (public member object) |
| char n_sep_by_space | indicates the separation of `currency_symbol`, `negative_sign`, and the negative monetary value   (public member object) |
| char p_sign_posn | indicates the position of `positive_sign` in a non-negative monetary value   (public member object) |
| char n_sign_posn | indicates the position of `negative_sign` in a negative monetary value   (public member object) |

#### International monetary numeric formatting parameters

|  |  |
| --- | --- |
| char\* int_curr_symbol | the string used as international currency name in the current C locale   (public member object) |
| char int_frac_digits | the number of digits after the decimal point to display in an international monetary quantity   (public member object) |
| char int_p_cs_precedes(C++11) | 1 if int_curr_symbol is placed before non-negative international monetary value, ​0​ if after   (public member object) |
| char int_n_cs_precedes(C++11) | 1 if int_curr_symboll is placed before negative international monetary value, ​0​ if after   (public member object) |
| char int_p_sep_by_space(C++11) | indicates the separation of `int_curr_symbol`, `positive_sign`, and the non-negative international monetary value   (public member object) |
| char int_n_sep_by_space(C++11) | indicates the separation of `int_curr_symbol`, `negative_sign`, and the negative international monetary value   (public member object) |
| char int_p_sign_posn(C++11) | indicates the position of `positive_sign` in a non-negative international monetary value   (public member object) |
| char int_n_sign_posn(C++11) | indicates the position of `negative_sign` in a negative international monetary value   (public member object) |

The characters of the C-strings pointed to by `grouping` and `mon_grouping` are interpreted according to their numeric values. When the terminating '\0' is encountered, the last value seen is assumed to repeat for the remainder of digits. If CHAR_MAX is encountered, no further digits are grouped. the typical grouping of three digits at a time is "\003".

The values of `p_sep_by_space`, `n_sep_by_space`, `int_p_sep_by_space`, `int_n_sep_by_space` are interpreted as follows:

|  |  |
| --- | --- |
| 0 | no space separates the currency symbol and the value |
| 1 | sign sticks to the currency symbol, value is separated by a space |
| 2 | sign sticks to the value. Currency symbol is separated by a space |

The values of `p_sign_posn`, `n_sign_posn`, `int_p_sign_posn`, `int_n_sign_posn` are interpreted as follows:

|  |  |
| --- | --- |
| 0 | parentheses around the value and the currency symbol are used to represent the sign |
| 1 | sign before the value and the currency symbol |
| 2 | sign after the value and the currency symbol |
| 3 | sign before the currency symbol |
| 4 | sign after the currency symbol |

### Example

Run this code

```
#include <clocale>
#include <iostream>
 
int main()
{
    std::setlocale(LC_ALL, "ja_JP.UTF-8");
    std::lconv* lc = std::localeconv();
    std::cout << "Japanese currency symbol: " << lc->currency_symbol
              << '(' << lc->int_curr_symbol << ")\n";
}

```

Output:

```
Japanese currency symbol: ￥(JPY )

```

### See also

|  |  |
| --- | --- |
| localeconv | queries numeric and monetary formatting details of the current locale   (function) |
| numpunct | defines numeric punctuation rules   (class template) |
| moneypunct | defines monetary formatting parameters used by std::money_get and std::money_put   (class template) |
| C documentation for lconv | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/locale/lconv&oldid=96330>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 October 2017, at 00:38.