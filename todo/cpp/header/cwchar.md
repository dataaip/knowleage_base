# Standard library header <cwchar>

From cppreference.com
< cpp‎ | header
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

Standard library headers

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | ****<cwchar>**** | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header was originally in the C standard library as <wchar.h>.

This header is part of the null-terminated wide and multibyte strings libraries.
It also provides some C-style I/O functions and conversion from C-style Date.

### Macros

|  |  |
| --- | --- |
| NULL | implementation-defined null pointer constant   (macro constant) |
| WEOF | a non-character value of type `std::wint_t` used to indicate errors   (macro constant) |
| WCHAR_MIN | the smallest valid value of wchar_t   (macro constant) |
| WCHAR_MAX | the largest valid value of wchar_t   (macro constant) |

### Types

|  |  |
| --- | --- |
| mbstate_t | conversion state information necessary to iterate multibyte character strings   (class) |
| size_t | unsigned integer type returned by the sizeof operator   (typedef) |
| `wint_t` | integer type that can hold any valid wide character and at least one more value |
| tm | calendar time type   (class) |

### Functions

|  |  |
| --- | --- |
| String manipulation | |
| wcscpy | copies one wide string to another   (function) |
| wcsncpy | copies a certain amount of wide characters from one string to another   (function) |
| wcscat | appends a copy of one wide string to another   (function) |
| wcsncat | appends a certain amount of wide characters from one wide string to another   (function) |
| wcsxfrm | transform a wide string so that `wcscmp` would produce the same result as `wcscoll`   (function) |
| String examination | |
| wcslen | returns the length of a wide string   (function) |
| wcscmp | compares two wide strings   (function) |
| wcsncmp | compares a certain amount of characters from two wide strings   (function) |
| wcscoll | compares two wide strings in accordance to the current locale   (function) |
| wcschr | finds the first occurrence of a wide character in a wide string   (function) |
| wcsrchr | finds the last occurrence of a wide character in a wide string   (function) |
| wcsspn | returns the length of the maximum initial segment that consists of only the wide characters found in another wide string   (function) |
| wcscspn | returns the length of the maximum initial segment that consists of only the wide **not** found in another wide string   (function) |
| wcspbrk | finds the first location of any wide character in one wide string, in another wide string   (function) |
| wcsstr | finds the first occurrence of a wide string within another wide string   (function) |
| wcstok | finds the next token in a wide string   (function) |
| Wide character array manipulation | |
| wmemcpy | copies a certain amount of wide characters between two non-overlapping arrays   (function) |
| wmemmove | copies a certain amount of wide characters between two, possibly overlapping, arrays   (function) |
| wmemcmp | compares a certain amount of wide characters from two arrays   (function) |
| wmemchr | finds the first occurrence of a wide character in a wide character array   (function) |
| wmemset | copies the given wide character to every position in a wide character array   (function) |
| Multibyte/wide character conversion | |
| mbsinit | checks if the std::mbstate_t object represents initial shift state   (function) |
| btowc | widens a single-byte narrow character to wide character, if possible   (function) |
| wctob | narrows a wide character to a single-byte narrow character, if possible   (function) |
| mbrlen | returns the number of bytes in the next multibyte character, given state   (function) |
| mbrtowc | converts the next multibyte character to wide character, given state   (function) |
| wcrtomb | converts a wide character to its multibyte representation, given state   (function) |
| mbsrtowcs | converts a narrow multibyte character string to wide string, given state   (function) |
| wcsrtombs | converts a wide string to narrow multibyte character string, given state   (function) |
| Input/Output | |
| fgetwcgetwc | gets a wide character from a file stream   (function) |
| fgetws | gets a wide string from a file stream   (function) |
| fputwcputwc | writes a wide character to a file stream   (function) |
| fputws | writes a wide string to a file stream   (function) |
| getwchar | reads a wide character from stdin   (function) |
| putwchar | writes a wide character to stdout   (function) |
| ungetwc | puts a wide character back into a file stream   (function) |
| fwide | switches a file stream between wide character I/O and narrow character I/O   (function) |
| wscanffwscanfswscanf | reads formatted wide character input from stdin, a file stream or a buffer   (function) |
| vwscanfvfwscanfvswscanf(C++11)(C++11)(C++11) | reads formatted wide character input from stdin, a file stream or a buffer using variable argument list   (function) |
| wprintffwprintfswprintf | prints formatted wide character output to stdout, a file stream or a buffer   (function) |
| vwprintfvfwprintfvswprintf | prints formatted wide character output to stdout, a file stream or a buffer using variable argument list   (function) |
| String conversions | |
| wcsftime | converts a std::tm object to custom wide string textual representation   (function) |
| wcstolwcstoll | converts a wide string to an integer value   (function) |
| wcstoulwcstoull | converts a wide string to an unsigned integer value   (function) |
| wcstofwcstodwcstold | converts a wide string to a floating-point value   (function) |

### Notes

- NULL is also defined in the following headers:
  - <cstddef>
  - <cstring>
  - <ctime>
  - <clocale>
  - <cstdio>
- std::size_t is also defined in the following headers:
  - <cstddef>
  - <ctime>
  - <cstdio>
- `std::wint_t` is also defined in the following headers:
  - <cwctype>
- std::tm is also defined in the following headers:
  - <ctime>

### Synopsis

```
namespace std {
  using size_t =    /* see description */; // freestanding
  using mbstate_t = /* see description */; // freestanding
  using wint_t =    /* see description */; // freestanding
 
  struct tm;
 
  int fwprintf(FILE* stream, const wchar_t* format, ...);
  int fwscanf(FILE* stream, const wchar_t* format, ...);
  int swprintf(wchar_t* s, size_t n, const wchar_t* format, ...);
  int swscanf(const wchar_t* s, const wchar_t* format, ...);
  int vfwprintf(FILE* stream, const wchar_t* format, va_list arg);
  int vfwscanf(FILE* stream, const wchar_t* format, va_list arg);
  int vswprintf(wchar_t* s, size_t n, const wchar_t* format, va_list arg);
  int vswscanf(const wchar_t* s, const wchar_t* format, va_list arg);
  int vwprintf(const wchar_t* format, va_list arg);
  int vwscanf(const wchar_t* format, va_list arg);
  int wprintf(const wchar_t* format, ...);
  int wscanf(const wchar_t* format, ...);
  wint_t fgetwc(FILE* stream);
  wchar_t* fgetws(wchar_t* s, int n, FILE* stream);
  wint_t fputwc(wchar_t c, FILE* stream);
  int fputws(const wchar_t* s, FILE* stream);
  int fwide(FILE* stream, int mode);
  wint_t getwc(FILE* stream);
  wint_t getwchar();
  wint_t putwc(wchar_t c, FILE* stream);
  wint_t putwchar(wchar_t c);
  wint_t ungetwc(wint_t c, FILE* stream);
  double wcstod(const wchar_t* nptr, wchar_t** endptr);
  float wcstof(const wchar_t* nptr, wchar_t** endptr);
  long double wcstold(const wchar_t* nptr, wchar_t** endptr);
  long int wcstol(const wchar_t* nptr, wchar_t** endptr, int base);
  long long int wcstoll(const wchar_t* nptr, wchar_t** endptr, int base);
  unsigned long int wcstoul(const wchar_t* nptr, wchar_t** endptr, int base);
  unsigned long long int wcstoull(const wchar_t* nptr, wchar_t** endptr, int base);
  wchar_t* wcscpy(wchar_t* s1, const wchar_t* s2);                // freestanding
  wchar_t* wcsncpy(wchar_t* s1, const wchar_t* s2, size_t n);     // freestanding
  wchar_t* wmemcpy(wchar_t* s1, const wchar_t* s2, size_t n);     // freestanding
  wchar_t* wmemmove(wchar_t* s1, const wchar_t* s2, size_t n);    // freestanding
  wchar_t* wcscat(wchar_t* s1, const wchar_t* s2);                // freestanding
  wchar_t* wcsncat(wchar_t* s1, const wchar_t* s2, size_t n);     // freestanding
  int wcscmp(const wchar_t* s1, const wchar_t* s2);               // freestanding
  int wcscoll(const wchar_t* s1, const wchar_t* s2);
  int wcsncmp(const wchar_t* s1, const wchar_t* s2, size_t n);    // freestanding
  size_t wcsxfrm(wchar_t* s1, const wchar_t* s2, size_t n);
  int wmemcmp(const wchar_t* s1, const wchar_t* s2, size_t n);    // freestanding
  const wchar_t* wcschr(const wchar_t* s, wchar_t c);             // freestanding
  wchar_t* wcschr(wchar_t* s, wchar_t c);                         // freestanding
  size_t wcscspn(const wchar_t* s1, const wchar_t* s2);           // freestanding
  const wchar_t* wcspbrk(const wchar_t* s1, const wchar_t* s2);   // freestanding
  wchar_t* wcspbrk(wchar_t* s1, const wchar_t* s2);               // freestanding
  const wchar_t* wcsrchr(const wchar_t* s, wchar_t c);            // freestanding
  wchar_t* wcsrchr(wchar_t* s, wchar_t c);                        // freestanding
  size_t wcsspn(const wchar_t* s1, const wchar_t* s2);            // freestanding
  const wchar_t* wcsstr(const wchar_t* s1, const wchar_t* s2);    // freestanding
  wchar_t* wcsstr(wchar_t* s1, const wchar_t* s2);                // freestanding
  wchar_t* wcstok(wchar_t* s1, const wchar_t* s2, wchar_t** ptr); // freestanding
  const wchar_t* wmemchr(const wchar_t* s, wchar_t c, size_t n);  // freestanding
  wchar_t* wmemchr(wchar_t* s, wchar_t c, size_t n);              // freestanding
  size_t wcslen(const wchar_t* s);                                // freestanding
  wchar_t* wmemset(wchar_t* s, wchar_t c, size_t n);              // freestanding
  size_t wcsftime(wchar_t* s, size_t maxsize, const wchar_t* format, const tm* timeptr);
  wint_t btowc(int c);
  int wctob(wint_t c);
 
  // multibyte / wide string and character conversion functions
  int mbsinit(const mbstate_t* ps);
  size_t mbrlen(const char* s, size_t n, mbstate_t* ps);
  size_t mbrtowc(wchar_t* pwc, const char* s, size_t n, mbstate_t* ps);
  size_t wcrtomb(char* s, wchar_t wc, mbstate_t* ps);
  size_t mbsrtowcs(wchar_t* dst, const char** src, size_t len, mbstate_t* ps);
  size_t wcsrtombs(char* dst, const wchar_t** src, size_t len, mbstate_t* ps);
}
 
#define NULL      /* see description */ // freestanding
#define WCHAR_MAX /* see description */ // freestanding
#define WCHAR_MIN /* see description */ // freestanding
#define WEOF      /* see description */ // freestanding

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 345 | C++98 | std::tm was not provided in `<cwchar>` | provided |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/cwchar&oldid=158967>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 September 2023, at 02:10.