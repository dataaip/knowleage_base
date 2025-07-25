# std::num_put<CharT,OutputIt>::put, std::num_put<CharT,OutputIt>::do_put

From cppreference.com
< cpp‎ | locale‎ | num put
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Locales and facets | | | | | | Locales | | | | | | has_facet | | | | | | use_facet | | | | | | locale | | | | | | Facet category base classes | | | | | | ctype_base | | | | | | codecvt_base | | | | | | messages_base | | | | | | time_base | | | | | | money_base | | | | | | ctype facets | | | | | | ctype | | | | | | ctype<char> | | | | | | ctype_byname | | | | | | codecvt | | | | | | codecvt_byname | | | | | | numeric facets | | | | | | num_get | | | | | | num_put | | | | | | numpunct | | | | | | numpunct_byname | | | | | | collate facets | | | | | | collate | | | | | | collate_byname | | | | | | time facets | | | | | | time_get | | | | | | time_put | | | | | | time_get_byname | | | | | | time_put_byname | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | monetary facets | | | | | | money_get | | | | | | money_put | | | | | | moneypunct | | | | | | moneypunct_byname | | | | | | messages facets | | | | | | messages | | | | | | messages_byname | | | | | | Character classification and conversion | | | | | | Character classification | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isspace | | | | | | iscntrl | | | | | | isupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | islower | | | | | | isalpha | | | | | | ispunct | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isdigit | | | | | | isxdigit | | | | | | isalnum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isblank(C++11) | | | | | | isprint | | | | | | isgraph | | | | | | | | Character conversions | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | toupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tolower | | | | | | | | String and stream conversions | | | | | | wstring_convert(C++11/17/26\*) | | | | | | wbuffer_convert(C++11/17/26\*) | | | | | | Unicode conversion facets | | | | | | codecvt_utf8(C++11/17/26\*) | | | | | | codecvt_utf16(C++11/17/26\*) | | | | | | codecvt_utf8_utf16(C++11/17/26\*) | | | | | | codecvt_mode(C++11/17/26\*) | | | | | | C library locales | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | LC_ALLLC_COLLATELC_CTYPELC_MONETARYLC_NUMERICLC_TIME | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setlocale | | | | | | localeconv | | | | | | lconv | | | | | |  | | | | | |  | | | | | |  | | | | | | | |

std::num_put

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| num_put::num_put | | | | |
| num_put::~num_put | | | | |
| ****num_put::putnum_put::do_put**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<locale>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| public:  iter_type put( iter_type out, std::ios_base& str,                char_type fill, bool val ) const; |  |  |
| iter_type put( iter_type out, std::ios_base& str,                 char_type fill, long val ) const; |  |  |
| iter_type put( iter_type out, std::ios_base& str,                 char_type fill, long long val ) const; |  | (since C++11) |
| iter_type put( iter_type out, std::ios_base& str,                 char_type fill, unsigned long val ) const; |  |  |
| iter_type put( iter_type out, std::ios_base& str,                 char_type fill, unsigned long long val ) const; |  | (since C++11) |
| iter_type put( iter_type out, std::ios_base& str,                 char_type fill, double val ) const; |  |  |
| iter_type put( iter_type out, std::ios_base& str,                 char_type fill, long double val ) const; |  |  |
| iter_type put( iter_type out, std::ios_base& str,                 char_type fill, const void\* val ) const; |  |  |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| protected:  virtual iter_type do_put( iter_type out, std::ios_base& str,                           char_type fill, bool val ) const; |  |  |
| virtual iter_type do_put( iter_type out, std::ios_base& str,                            char_type fill, long val ) const; |  |  |
| virtual iter_type do_put( iter_type out, std::ios_base& str,                            char_type fill, long long val ) const; |  | (since C++11) |
| virtual iter_type do_put( iter_type out, std::ios_base& str,                            char_type fill, unsigned long val ) const; |  |  |
| virtual iter_type do_put( iter_type out, std::ios_base& str,                            char_type fill, unsigned long long val ) const; |  | (since C++11) |
| virtual iter_type do_put( iter_type out, std::ios_base& str,                            char_type fill, double val ) const; |  |  |
| virtual iter_type do_put( iter_type out, std::ios_base& str,                            char_type fill, long double val ) const; |  |  |
| virtual iter_type do_put( iter_type out, std::ios_base& str,                            char_type fill, const void\* val ) const; |  |  |
|  |  |  |
| --- | --- | --- |
|  |  |  |

1) Public member function, calls the protected virtual member function `do_put` of the most derived class.2) Writes characters to the output sequence out which represent the value of val, formatted as requested by the formatting flags str.flags() and the std::numpunct and std::ctype facets of the locale imbued in the stream str. This function is called by all formatted output stream operators, such as std::cout << n;.

Conversion occurs in four stages:

#### Stage 1: conversion specifier selection

- I/O format flags are obtained, as if by

:   fmtflags basefield = (str.flags() & std::ios_base::basefield);
:   fmtflags uppercase = (str.flags() & std::ios_base::uppercase);
:   fmtflags floatfield = (str.flags() & std::ios_base::floatfield);
:   fmtflags showpos = (str.flags() & std::ios_base::showpos);
:   fmtflags showbase = (str.flags() & std::ios_base::showbase);
:   fmtflags showpoint = (str.flags() & std::ios_base::showpoint);

- If the type of val is bool:
  - If boolalpha == 0, then converts val to type int and performs integer output.
  - If boolalpha != 0, obtains std::use_facet<std::numpunct<CharT>>(str.getloc()).truename() if val == true or std::use_facet<std::numpunct<CharT>>(str.getloc()).falsename() if val == false, and outputs each successive character c of that string to out with \*out++ = c. No further processing is done in this case, the function returns out.
- If the type of val is an integer type, the first applicable choice of the following is selected:
  - If basefield == oct, will use conversion specifier %o
  - If basefield == hex && !uppercase, will use conversion specifier %x
  - If basefield == hex, will use conversion specifier %X
  - If the type of val is signed, will use conversion specifier %d
  - If the type of val is unsigned, will use conversion specifier %u
- For integer types, length modifier is added to the conversion specification if necessary: l for long and unsigned long, ll for long long and unsigned long long(since C++11).
- If the type of val is a floating-point type, the first applicable choice of the following is selected:
  - If floatfield == std::ios_base::fixed, will use conversion specifier %f
  - If floatfield == std::ios_base::scientific && !uppercase, will use conversion specifier %e
  - If floatfield == std::ios_base::scientific, will use conversion specifier %E

|  |  |
| --- | --- |
| - If floatfield == (std::ios_base::fixed | std::ios_base::scientific) && !uppercase, will use conversion specifier %a - If floatfield == (std::ios_base::fixed | std::ios_base::scientific), will use conversion specifier %A | (since C++11) |

:   - If !uppercase, will use conversion specifier %g
    - Otherwise, will use conversion specifier %G
:   Also:

    - If the type of val is long double, the length modifier L is added to the conversion specifier.
    - If the type of val is a floating-point type and floatfield != (ios_base::fixed | ios_base::scientific)(since C++11), the precision modifier is added and set to str.precision(). Otherwise, no precision is specified.

- For both integer and floating-point types, if showpos is set, the modifier + is prepended
- For integer types, if showbase is set, the modifier # is prepended.
- For floating-point types, if showpoint is set, the modifier # is prepended.
- If the type of val is void\*, will use conversion specifier %p
- A narrow character string is created as if by a call to std::printf(spec, val) in the "C" locale, where spec is the chosen conversion specifier.

#### Stage 2: locale-specific conversion

- Every character c obtained in Stage 1, other than the decimal point '.', is converted to CharT by calling std::use_facet<std::ctype<CharT>>(str.getloc()).widen(c).
- For arithmetic types, the thousands separator character, obtained from std::use_facet<std::numpunct<CharT>>(str.getloc()).thousands_sep(), is inserted into the sequence according to the grouping rules provided by std::use_facet<std::numpunct<CharT>>(str.getloc()).grouping()
- Decimal point characters ('.') are replaced by std::use_facet<std::numpunct<CharT>>(str.getloc()).decimal_point()

#### Stage 3: padding

- The adjustment flag is obtained as if by std::fmtflags adjustfield = (flags & (std::ios_base::adjustfield)) and examined to identify padding location, as follows:
  - If adjustfield == std::ios_base::left, will pad after
  - If adjustfield == std::ios_base::right, will pad before
  - If adjustfield == std::ios_base::internal and a sign character occurs in the representation, will pad after the sign
  - If adjustfield == std::ios_base::internal and Stage 1 representation began with 0x or 0X, will pad after the x or X
  - Otherwise, will pad before
- If str.width() is non-zero (e.g. std::setw was just used) and the number of CharT's after Stage 2 is less than str.width(), then copies of the fill character are inserted at the position indicated by padding to bring the length of the sequence to str.width().

In any case, str.width(0) is called to cancel the effects of std::setw.

#### Stage 4: output

Every successive character c from the sequence of CharT's from Stage 3 is output as if by \*out++ = c.

### Parameters

|  |  |  |
| --- | --- | --- |
| out | - | iterator pointing to the first character to be overwritten |
| str | - | stream to retrieve the formatting information from |
| fill | - | padding character used when the results needs to be padded to the field width |
| val | - | value to convert to string and output |

### Return value

out

### Notes

The leading zero generated by the conversion specification #o (resulting from the combination of std::showbase and std::oct for example) is not counted as a padding character.

|  |  |
| --- | --- |
| When formatting a floating point value as hexfloat (i.e., when floatfield == (std::ios_base::fixed | std::ios_base::scientific)), the stream's precision is not used; instead, the number is always printed with enough precision to exactly represent the value. | (since C++11) |

### Example

Output a number using the facet directly, and demonstrate user-defined facet:

Run this code

```
#include <iostream>
#include <locale>
 
// this custom num_put outputs squares of all integers (except long long)
struct squaring_num_put : std::num_put<char>
{
    iter_type do_put(iter_type out, std::ios_base& str,
                     char_type fill, long val) const
    {
        return std::num_put<char>::do_put(out, str, fill, val * val);
    }
 
    iter_type do_put(iter_type out, std::ios_base& str,
                     char_type fill, unsigned long val) const
    {
        return std::num_put<char>::do_put(out, str, fill, val * val);
    }
};
 
int main()
{
    auto& facet = std::use_facet<std::num_put<char>>(std::locale());
    facet.put(std::cout, std::cout, '0', 2.71);
    std::cout << '\n';
 
    std::cout.imbue(std::locale(std::cout.getloc(), new squaring_num_put));
    std::cout << 6 << ' ' << -12 << '\n';
}

```

Output:

```
2.71
36 144

```

An implementation of operator<< for a user-defined type.

Run this code

```
#include <iostream>
#include <iterator>
#include <locale>
 
struct base { long x = 10; };
 
template<class CharT, class Traits>
std::basic_ostream<CharT, Traits>&
    operator<<(std::basic_ostream<CharT, Traits>& os, base const& b)
{
    try
    {
        typename std::basic_ostream<CharT, Traits>::sentry s(os);
 
        if (s)
        {
            std::ostreambuf_iterator<CharT, Traits> it(os);
            std::use_facet<std::num_put<CharT>>(os.getloc())
                .put(it, os, os.fill(), b.x);
        }
    }
    catch (...)
    {
        // set badbit on os and rethrow if required
    }
 
    return os;
}
 
int main()
{
    base b;
    std::cout << b;
}

```

Output:

```
10

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 34 | C++98 | the bool overload used non-existing members truename and falsename of std::ctype | use these members of std::numpunct |
| LWG 231 | C++98 | the precision modifier was only added if (flags & fixed) != 0 or str.precision() > 0 | removed these conditions |
| LWG 282 | C++98 | the thousand separators were only inserted for integral types in stage 2 | also inserted for floating-point types |

### See also

|  |  |
| --- | --- |
| operator<< | inserts formatted data   (public member function of `std::basic_ostream<CharT,Traits>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/locale/num_put/put&oldid=160189>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 October 2023, at 07:56.