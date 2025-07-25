# Localization library

From cppreference.com
< cpp
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
| ****Localization library**** | | | | |
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

****Localization library****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Locales and facets | | | | | | Locales | | | | | | has_facet | | | | | | use_facet | | | | | | locale | | | | | | Facet category base classes | | | | | | ctype_base | | | | | | codecvt_base | | | | | | messages_base | | | | | | time_base | | | | | | money_base | | | | | | ctype facets | | | | | | ctype | | | | | | ctype<char> | | | | | | ctype_byname | | | | | | codecvt | | | | | | codecvt_byname | | | | | | numeric facets | | | | | | num_get | | | | | | num_put | | | | | | numpunct | | | | | | numpunct_byname | | | | | | collate facets | | | | | | collate | | | | | | collate_byname | | | | | | time facets | | | | | | time_get | | | | | | time_put | | | | | | time_get_byname | | | | | | time_put_byname | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | monetary facets | | | | | | money_get | | | | | | money_put | | | | | | moneypunct | | | | | | moneypunct_byname | | | | | | messages facets | | | | | | messages | | | | | | messages_byname | | | | | | Character classification and conversion | | | | | | Character classification | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isspace | | | | | | iscntrl | | | | | | isupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | islower | | | | | | isalpha | | | | | | ispunct | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isdigit | | | | | | isxdigit | | | | | | isalnum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | isblank(C++11) | | | | | | isprint | | | | | | isgraph | | | | | | | | Character conversions | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | toupper | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tolower | | | | | | | | String and stream conversions | | | | | | wstring_convert(C++11/17/26\*) | | | | | | wbuffer_convert(C++11/17/26\*) | | | | | | Unicode conversion facets | | | | | | codecvt_utf8(C++11/17/26\*) | | | | | | codecvt_utf16(C++11/17/26\*) | | | | | | codecvt_utf8_utf16(C++11/17/26\*) | | | | | | codecvt_mode(C++11/17/26\*) | | | | | | C library locales | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | LC_ALLLC_COLLATELC_CTYPELC_MONETARYLC_NUMERICLC_TIME | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setlocale | | | | | | localeconv | | | | | | lconv | | | | | |  | | | | | |  | | | | | |  | | | | | | | |

The locale facility includes internationalization support for character classification and string collation, numeric, monetary, and date/time formatting and parsing, and message retrieval. Locale settings control the behavior of stream I/O, regular expression library, and other components of the C++ standard library.

### Locales and facets

|  |  |
| --- | --- |
| Defined in header `<locale>` | |
| Locales | |
| locale | set of polymorphic facets that encapsulate cultural differences   (class) |
| use_facet | obtains a facet from a locale   (function template) |
| has_facet | checks if a locale implements a specific facet   (function template) |
| Facet category base classes | |
| ctype_base | defines character classification categories   (class) |
| codecvt_base | defines character conversion errors   (class) |
| messages_base | defines messages catalog type   (class) |
| time_base | defines date format constants   (class) |
| money_base | defines monetary formatting patterns   (class) |
| ctype facets | |
| ctype | defines character classification tables   (class template) |
| ctype_byname | represents the system-supplied std::ctype for the named locale   (class template) |
| ctype<char> | specialization of std::ctype for type char   (class template specialization) |
| codecvt | converts between character encodings, including UTF-8, UTF-16, UTF-32   (class template) |
| codecvt_byname | represents the system-supplied std::codecvt for the named locale   (class template) |
| numeric facets | |
| num_get | parses numeric values from an input character sequence   (class template) |
| num_put | formats numeric values for output as character sequence   (class template) |
| numpunct | defines numeric punctuation rules   (class template) |
| numpunct_byname | represents the system-supplied std::numpunct for the named locale   (class template) |
| collate facets | |
| collate | defines lexicographical comparison and hashing of strings   (class template) |
| collate_byname | represents the system-supplied std::collate for the named locale   (class template) |
| time facets | |
| time_get | parses time/date values from an input character sequence into std::tm   (class template) |
| time_get_byname | represents the system-supplied std::time_get for the named locale   (class template) |
| time_put | formats contents of std::tm for output as character sequence   (class template) |
| time_put_byname | represents the system-supplied std::time_put for the named locale   (class template) |
| monetary facets | |
| money_get | parses and constructs a monetary value from an input character sequence   (class template) |
| money_put | formats a monetary value for output as a character sequence   (class template) |
| moneypunct | defines monetary formatting parameters used by std::money_get and std::money_put   (class template) |
| moneypunct_byname | represents the system-supplied std::moneypunct for the named locale   (class template) |
| messages facets | |
| messages | implements retrieval of strings from message catalogs   (class template) |
| messages_byname | represents the system-supplied std::messages for the named locale   (class template) |

### Character classification and conversion

|  |  |
| --- | --- |
| Defined in header `<locale>` | |
| Character classification | |
| isspace(std::locale) | checks if a character is classified as whitespace by a locale   (function template) |
| isblank(std::locale)(C++11) | checks if a character is classified as a blank character by a locale   (function template) |
| iscntrl(std::locale) | checks if a character is classified as a control character by a locale   (function template) |
| isupper(std::locale) | checks if a character is classified as uppercase by a locale   (function template) |
| islower(std::locale) | checks if a character is classified as lowercase by a locale   (function template) |
| isalpha(std::locale) | checks if a character is classified as alphabetic by a locale   (function template) |
| isdigit(std::locale) | checks if a character is classified as a digit by a locale   (function template) |
| ispunct(std::locale) | checks if a character is classified as punctuation by a locale   (function template) |
| isxdigit(std::locale) | checks if a character is classified as a hexadecimal digit by a locale   (function template) |
| isalnum(std::locale) | checks if a character is classified as alphanumeric by a locale   (function template) |
| isprint(std::locale) | checks if a character is classified as printable by a locale   (function template) |
| isgraph(std::locale) | checks if a character is classified as graphical by a locale   (function template) |
| Character conversions | |
| toupper(std::locale) | converts a character to uppercase using the ctype facet of a locale   (function template) |
| tolower(std::locale) | converts a character to lowercase using the `ctype` facet of a locale   (function template) |
| String and stream conversions | |
| wstring_convert(C++11)(deprecated in C++17)(removed in C++26) | performs conversions between a wide string and a byte string   (class template) |
| wbuffer_convert(C++11)(deprecated in C++17)(removed in C++26) | performs conversion between a byte stream buffer and a wide stream buffer   (class template) |

|  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Locale-independent unicode conversion facets  |  |  | | --- | --- | | Defined in header `<codecvt>` | | | codecvt_utf8(C++11)(deprecated in C++17)(removed in C++26) | converts between UTF-8 and UCS-2/UCS-4   (class template) | | codecvt_utf16(C++11)(deprecated in C++17)(removed in C++26) | converts between UTF-16 and UCS-2/UCS-4   (class template) | | codecvt_utf8_utf16(C++11)(deprecated in C++17)(removed in C++26) | converts between UTF-8 and UTF-16   (class template) | | codecvt_mode(C++11)(deprecated in C++17)(removed in C++26) | tags to alter behavior of the standard codecvt facets   (enum) | | (until C++26) |

### C library locales

|  |  |
| --- | --- |
| Defined in header `<clocale>` | |
| setlocale | gets and sets the current C locale   (function) |
| LC_ALLLC_COLLATELC_CTYPELC_MONETARYLC_NUMERICLC_TIME | locale categories for std::setlocale   (macro constant) |
| localeconv | queries numeric and monetary formatting details of the current locale   (function) |
| lconv | formatting details, returned by std::localeconv   (class) |

### See also

|  |  |
| --- | --- |
| C documentation for Localization support | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/locale&oldid=179015>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 January 2025, at 19:48.