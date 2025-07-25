# std::get_money

From cppreference.com
< cpp‎ | io‎ | manip
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

Input/output library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| I/O manipulators | | | | |
| Print functions (C++23) | | | | |
| C-style I/O | | | | |
| Buffers | | | | |
| basic_streambuf | | | | |
| basic_filebuf | | | | |
| basic_stringbuf | | | | |
| basic_spanbuf(C++23) | | | | |
| strstreambuf(C++98/26\*) | | | | |
| basic_syncbuf(C++20) | | | | |
| Streams | | | | |
| Abstractions | | | | |
| ios_base | | | | |
| basic_ios | | | | |
| basic_istream | | | | |
| basic_ostream | | | | |
| basic_iostream | | | | |
| File I/O | | | | |
| basic_ifstream | | | | |
| basic_ofstream | | | | |
| basic_fstream | | | | |
| String I/O | | | | |
| basic_istringstream | | | | |
| basic_ostringstream | | | | |
| basic_stringstream | | | | |
| Array I/O | | | | |
| basic_ispanstream(C++23) | | | | |
| basic_ospanstream(C++23) | | | | |
| basic_spanstream(C++23) | | | | |
| istrstream(C++98/26\*) | | | | |
| ostrstream(C++98/26\*) | | | | |
| strstream(C++98/26\*) | | | | |
| Synchronized Output | | | | |
| basic_osyncstream(C++20) | | | | |
| Types | | | | |
| streamoff | | | | |
| streamsize | | | | |
| fpos | | | | |
| Error category interface | | | | |
| iostream_category(C++11) | | | | |
| io_errc(C++11) | | | | |

Input/output manipulators

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Floating-point formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showpointnoshowpoint | | | | | | setprecision | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fixedscientifichexfloatdefaultfloat(C++11)(C++11) | | | | | |
| Integer formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbase | | | | | | showbasenoshowbase | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | dechexoct | | | | | |
| Boolean formatting | | | | |
| boolalphanoboolalpha | | | | |
| Field width and fill control | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | setfill | | | | | | setw | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | internalleftright | | | | | |
| Other formatting | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | showposnoshowpos | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uppercasenouppercase | | | | | |
| Whitespace processing | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ws | | | | | | ends | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | skipwsnoskipws | | | | | |
| Output flushing | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | flush | | | | | | endl | | | | | | flush_emit(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | unitbufnounitbuf | | | | | | emit_on_flushnoemit_on_flush(C++20)(C++20) | | | | | |
| Status flags manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | resetiosflags | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setiosflags | | | | | |
| Time and money I/O | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****get_money****(C++11) | | | | | | get_time(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | put_money(C++11) | | | | | | put_time(C++11) | | | | | |
| Quoted manipulator | | | | |
| quoted(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<iomanip>` |  |  |
| template< class MoneyT >  /\*unspecified\*/ get_money( MoneyT& mon, bool intl = false ); |  | (since C++11) |
|  |  |  |

When used in an expression in >> get_money(mon, intl), parses the character input as a monetary value, as specified by the std::money_get facet of the locale currently imbued in in, and stores the value in mon.

The extraction operation in in >> get_money(mon, intl) behaves as a FormattedInputFunction.

### Parameters

|  |  |  |
| --- | --- | --- |
| mon | - | variable where monetary value will be written. Can be either long double or std::basic_string |
| intl | - | expects to find required international currency strings if true, expects optional currency symbols otherwise |

### Return value

An object of unspecified type such that

- if in is an object of type std::basic_istream<CharT, Traits>, the expression in >> get_money(mon, intl)
  - has type std::basic_istream<CharT, Traits>&
  - has value in
  - behaves as if it called f(in, mon, intl)

where the function f is defined as:

```
template<class CharT, class Traits, class MoneyT>
void f(std::basic_ios<CharT, Traits>& str, MoneyT& mon, bool intl)
{
    using Iter = std::istreambuf_iterator<CharT, Traits>;
    using MoneyGet = std::money_get<CharT, Iter>;
 
    std::ios_base::iostate err = std::ios_base::goodbit;
    const MoneyGet& mg = std::use_facet<MoneyGet>(str.getloc());
 
    mg.get(Iter(str.rdbuf()), Iter(), intl, str, err, mon);
 
    if (err != std::ios_base::goodbit)
        str.setstate(err);
}

```

### Example

Run this code

```
#include <iomanip>
#include <iostream>
#include <locale>
#include <sstream>
 
int main()
{
    std::istringstream in("$1,234.56 2.22 USD  3.33");
    long double v1, v2;
    std::string v3;
 
    in.imbue(std::locale("en_US.UTF-8"));
    in >> std::get_money(v1) >> std::get_money(v2) >> std::get_money(v3, true);
 
    if (in)
        std::cout << std::quoted(in.str()) << " parsed as: "
                  << v1 << ", " << v2 << ", " << v3 << '\n';
    else
        std::cout << "Parse failed";
}

```

Output:

```
"$1,234.56 2.22 USD  3.33" parsed as: 123456, 222, 333

```

### See also

|  |  |
| --- | --- |
| money_get | parses and constructs a monetary value from an input character sequence   (class template) |
| put_money(C++11) | formats and outputs a monetary value   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/io/manip/get_money&oldid=159175>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 September 2023, at 22:29.