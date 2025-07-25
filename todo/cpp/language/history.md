# History of C++

From cppreference.com
< cpp‎ | language
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

C++ language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General topics | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Preprocessor | | | | | | Comments | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Keywords | | | | | | Escape sequences | | | | | |
| Flow control | | | | |
| Conditional execution statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | switch | | | | | |
| Iteration statements (loops) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | for | | | | | | range-`for` (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | while | | | | | | `do-while` | | | | | |
| Jump statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | continue - break | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | goto - return | | | | | |
| Functions | | | | |
| Function declaration | | | | |
| Lambda function expression | | | | |
| `inline` specifier | | | | |
| Dynamic exception specifications (until C++17\*) | | | | |
| `noexcept` specifier (C++11) | | | | |
| Exceptions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `throw`-expression | | | | | | `try` block | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | `catch` handler | | | | | |
| Namespaces | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace declaration | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace aliases | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Fundamental types | | | | | | Enumeration types | | | | | | Function types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class/struct types | | | | | | Union types | | | | | |  | | | | | |
| Specifiers | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const`/`volatile` | | | | | | decltype (C++11) | | | | | | auto (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | constexpr (C++11) | | | | | | consteval (C++20) | | | | | | constinit (C++20) | | | | | |
| Storage duration specifiers | | | | |
| Initialization | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default-initialization | | | | | | Value-initialization | | | | | | Zero-initialization | | | | | | Copy-initialization | | | | | | Direct-initialization | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Aggregate initialization | | | | | | List-initialization (C++11) | | | | | | Constant initialization | | | | | | Reference initialization | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Expressions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operators | | | | | | Operator precedence | | | | | |
| Alternative representations | | | | |
| Literals | | | | |
| Boolean - Integer - Floating-point | | | | |
| Character - String - nullptr (C++11) | | | | |
| User-defined (C++11) | | | | |
| Utilities | | | | |
| Attributes (C++11) | | | | |
| Types | | | | |
| `typedef` declaration | | | | |
| Type alias declaration (C++11) | | | | |
| Casts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | static_cast | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Explicit conversions | | | | | | dynamic_cast | | | | | | reinterpret_cast | | | | | |
| Memory allocation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `new` expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `delete` expression | | | | | |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | Constructors | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Access specifiers | | | | | | `friend` specifier | | | | | |  | | | | | |
| Class-specific function properties | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Virtual function | | | | | | `override` specifier (C++11) | | | | | | `final` specifier (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | explicit (C++11) | | | | | | static | | | | | |  | | | | | |
| Special member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default constructor | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | Destructor | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****History of C++**** | | | | | |

## Early C++

- 1979: C with Classes first implemented

1. New features: classes, member functions, derived classes, separate compilation, public and private access control, friends, type checking of function arguments, default arguments, inline functions, overloaded assignment operator, constructors, destructors, f() same as f(void), call-function and return-function (synchronization features, not in C++)
2. Libraries: the concurrent task library (not in C++)

- 1982: C with Classes reference manual published
- 1984: C84 implemented, reference manual published
- 1985: Cfront 1.0

1. New features: virtual functions, function and operator overloading, references, new and delete operators, the keyword `const`, scope resolution operator
2. Library additions: complex number, `string` (AT&T version), I/O stream

- 1985: The C++ Programming Language, 1st edition
- 1986: The "whatis?" paper documenting the remaining design goals, including multiple inheritance, exception handling, and templates.
- 1987: C++ support in GCC 1.15.3
- 1989: Cfront 2.0

1. New features: multiple inheritance, pointers to members, protected access, type-safe linkage, abstract classes, static and const-qualified member functions, class-specific new and delete
2. Library additions: I/O manipulators

- 1990: The Annotated C++ Reference Manual

This book described the language as designed, including some features that were not yet implemented. It served as the de-facto standard until the ISO.

1. New features: namespaces, exception handling, nested classes, templates

- 1991: Cfront 3.0
- 1991: The C++ Programming Language, 2nd edition

## Standard C++

- 1990: ANSI C++ Committee founded
- 1991: ISO C++ Committee founded
- 1992: STL implemented in C++

### C++98/03 period

- 1998: ****C++98**** (ISO/IEC 14882:1998)

1. New features: RTTI (`dynamic_cast`, `typeid`), covariant return types, cast operators, `mutable`, `bool`, declarations in conditions, template instantiations, member templates, export
2. Library additions: locales, bitset, valarray, auto_ptr, templatized string, I/O streams, and complex numbers.
3. Based on STL: containers, algorithms, iterators, function objects

- 1998: The C++ Programming Language, 3rd edition
- 1999: Boost founded by the committee members to produce new high-quality candidate libraries for the standard.
- 2003: ****C++03**** (ISO/IEC 14882:2003)

This was a minor revision, intended to be little more than a technical corrigendum. This revision introduces the definition of value initialization.

| Defect Reports fixed in C++03 (92 core, 125 library) |
| --- |
| - CWG#1 - CWG#20 - CWG#21 - CWG#22 - CWG#24 - CWG#25 - CWG#30 - CWG#32 - CWG#33 - CWG#35 - CWG#38 - CWG#40 - CWG#41 - CWG#43 - CWG#48 - CWG#49 - CWG#51 - CWG#52 - CWG#53 - CWG#56 - CWG#59 - CWG#64 - CWG#65 - CWG#67 - CWG#68 - CWG#69 - CWG#73 - CWG#74 - CWG#75 - CWG#76 - CWG#80 - CWG#83 - CWG#84 - CWG#85 - CWG#89 - CWG#90 - CWG#93 - CWG#94 - CWG#98 - CWG#100 - CWG#101 - CWG#103 - CWG#105 - CWG#108 - CWG#116 - CWG#120 - CWG#121 - CWG#123 - CWG#126 - CWG#127 - CWG#128 - CWG#131 - CWG#134 - CWG#135 - CWG#137 - CWG#142 - CWG#145 - CWG#147 - CWG#148 - CWG#149 - CWG#151 - CWG#152 - CWG#153 - CWG#159 - CWG#161 - CWG#163 - CWG#164 - CWG#166 - CWG#171 - CWG#173 - CWG#176 - CWG#178 - CWG#179 - CWG#181 - CWG#183 - CWG#185 - CWG#187 - CWG#188 - CWG#190 - CWG#193 - CWG#194 - CWG#202 - CWG#206 - CWG#210 - CWG#213 - CWG#217 - CWG#227 - CWG#235 - CWG#241 - CWG#249 - CWG#250 - CWG#304  - LWG#1 - LWG#3 - LWG#5 - LWG#7 - LWG#8 - LWG#9 - LWG#11 - LWG#13 - LWG#14 - LWG#15 - LWG#16 - LWG#17 - LWG#18 - LWG#19 - LWG#20 - LWG#21 - LWG#22 - LWG#24 - LWG#25 - LWG#26 - LWG#27 - LWG#28 - LWG#29 - LWG#30 - LWG#31 - LWG#32 - LWG#33 - LWG#34 - LWG#35 - LWG#36 - LWG#37 - LWG#38 - LWG#39 - LWG#40 - LWG#41 - LWG#42 - LWG#46 - LWG#47 - LWG#48 - LWG#50 - LWG#51 - LWG#52 - LWG#53 - LWG#54 - LWG#55 - LWG#56 - LWG#57 - LWG#59 - LWG#60 - LWG#61 - LWG#62 - LWG#63 - LWG#64 - LWG#66 - LWG#68 - LWG#69 - LWG#70 - LWG#71 - LWG#74 - LWG#75 - LWG#78 - LWG#79 - LWG#80 - LWG#83 - LWG#86 - LWG#90 - LWG#106 - LWG#108 - LWG#110 - LWG#112 - LWG#114 - LWG#115 - LWG#119 - LWG#122 - LWG#124 - LWG#125 - LWG#126 - LWG#127 - LWG#129 - LWG#132 - LWG#133 - LWG#134 - LWG#137 - LWG#139 - LWG#141 - LWG#142 - LWG#144 - LWG#146 - LWG#147 - LWG#148 - LWG#150 - LWG#151 - LWG#152 - LWG#154 - LWG#155 - LWG#156 - LWG#158 - LWG#159 - LWG#160 - LWG#161 - LWG#164 - LWG#168 - LWG#169 - LWG#170 - LWG#172 - LWG#173 - LWG#174 - LWG#175 - LWG#176 - LWG#181 - LWG#189 - LWG#193 - LWG#195 - LWG#199 - LWG#208 - LWG#209 - LWG#210 - LWG#211 - LWG#212 - LWG#217 - LWG#220 - LWG#222 - LWG#223 - LWG#224 - LWG#227 |

- 2006: Performance TR (ISO/IEC TR 18015:2006) (ISO Store) (2006 draft)

This TR discussed the costs of various C++ abstractions, provided implementation guidance, discussed use of C++ in embedded systems and introduced `<hardware>` interface to C's ISO/IEC TR 18037:2008 `<iohw.h>`.

- 2007: Library extension TR1 (ISO/IEC TR 19768:2007) (ISO store) (2005 draft).

This TR is a C++ library extension, which adds the following to the C++ standard library:

1. From Boost: reference_wrapper, Smart pointers, Member function, result_of, bind, function, Type Traits, Random, Mathematical Special Functions, tuple, array, Unordered Containers (including hash), and Regular Expressions.
2. From C99: mathematical functions from `<math.h>` that were new in C99, blank character class, Floating-point environment, hexfloat I/O Manipulator, fixed-size integral types, the `long long` type, va_copy, the snprintf() and vfscanf() families of functions, and the C99 conversion specifies for printf() and scanf() families of functions.

All of TR1 except for the special functions was included in C++11, with minor changes.

- 2010: Mathematical special functions (ISO/IEC 29124:2010) (ISO Store) (2010 draft)

This international standard is a C++ standard library extension, which adds the special functions that were part of TR1, but were not included in C++11: elliptic integrals, exponential integral, Laguerre polynomials, Legendre polynomials, Hermite polynomials, Bessel functions, Neumann functions, beta function, and Riemann zeta function. This standard was merged into C++17.

### C++11 period

- 2011: ****C++11**** (ISO/IEC 14882:2011) (ISO Store) (2012 post-publication draft).

Main Article: C++11

A large number of changes were introduced to both standardize existing practices and improve the abstractions available to the C++ programmers

- 2011: Decimal floating-point TR (ISO/IEC TR 24733:2011) (ISO Store) (2009 draft)

This TR implements the decimal floating-point types from IEEE 754-2008 Standard for Floating-Point Arithmetic: `std::decimal::decimal32`, `std::decimal::decimal64`, and `std::decimal::decimal128`.

- 2012: The Standard C++ Foundation founded
- 2013: The C++ Programming Language, 4th edition

### C++14 period

- 2014: ****C++14**** (ISO Store) (ANSI Store)) (2014 final draft)

Main Article: C++14

Minor revision of the C++ standard

- 2015: Filesystem library TS (ISO/IEC TS 18822:2015) (ISO Store) (2014 draft)

This TS is an experimental C++ library extension that specifies a filesystem library based on boost.filesystem V3 (with some modifications and extensions). This TS was merged into C++17.

- 2015: Extensions for Parallelism TS (ISO/IEC TS 19570:2015) (ISO Store) (2015 draft)

This TS standardizes parallel and vector-parallel API for all standard library algorithms, as well as adds new algorithms such as `reduce`, `transform_reduce`, or `exclusive_scan`. This TS was merged into C++17.

- 2015: Extensions for Transactional Memory TS (ISO/IEC TS 19841:2015) (ISO Store) ([2015 draft)

This TS extends the C++ core language with synchronized and atomic blocks, as well as transaction-safe functions, which implement transactional memory semantics.

- 2015: Extensions for Library Fundamentals TS (ISO/IEC TS 19568:2015) (ISO Store) (2015 draft)

This TS adds several new components to the C++ standard library: optional, any, string_view, sample, search, apply, polymorphic allocators, and variable templates for type traits. This TS was merged into C++17.

- 2015: Extensions for Concepts TS (ISO/IEC TS 19217:2015) (ISO Store) (2015 draft)

This TS extends the C++ core language with concepts (named type requirements) and constraints (limits on the types allowed in template, function, and variable declarations), which aids metaprogramming and simplifies template instantiation diagnostics, see concepts. This TS was merged into C++20, with some omissions.

- 2016: Extensions for Concurrency TS (ISO/IEC TS 19571:2016) (ISO Store) (2015 draft)

This TS extends the C++ library to include several extensions to std::future, latches and barriers, and atomic smart pointers.

### C++17 period

- 2017: ****C++17**** (ISO Store) (ANSI Store)) (n4659 2017-03-21 final draft)

Main Article: C++17

The major revision of the C++ standard after C++11

- 2017: Extensions for Ranges TS (ISO/IEC TS 21425:2017) (ISO Store) (2017 draft)

This TS extends the C++ library to include ranges, a new, more powerful, abstraction to replace iterator pairs, along with range views, sentinel ranges, projections for on-the-fly transformations, new iterator adaptors and algorithms. This extension finally makes it possible to sort a vector with sort(v);

- 2017: Extensions for Coroutines TS (ISO/IEC TS 22277:2017) (ISO Store) (2017 draft)

This TS extends the C++ core language and the standard library to include stackless coroutines (resumable functions). This adds the keywords co_await, co_yield, and co_return.

- 2018: Extensions for Networking TS (ISO/IEC TS 19216:2018) (ISO Store) (2017 draft)

This TS extends the C++ library to include TCP/IP networking based on boost.asio.

- 2018: Extensions for modules TS (ISO/IEC TS 21544:2018) (ISO Store) (2018 draft)

This TS extends the C++ core language to include modules. This adds the special identifiers module, import, and reintroduces the keyword export with a new meaning.

- 2018: Extensions for Parallelism version 2 TS (ISO/IEC TS 19570:2018) (ISO Store) (2018 draft)

This TS extends the C++ library to include two new execution policies (unseq and vec), additional parallel algorithms such as reduction_plus or for_loop_strided, task blocks for forking and joining parallel tasks, SIMD types and operations on those types.

### C++20 period

- 2020: ****C++20**** (ISO Store) (final draft n4860 2020-03-31)

Main Article: C++20

The major revision of the C++ standard after C++17

- 2021: Reflection TS (ISO/IEC TS 23619:2021) (ISO store) (2020 draft)

This TS extends C++ with the facilities to inspect program entities such as variables, enumerations, classes and their members, lambdas and their captures, etc.

### Future development

- Experimental technical specifications
- 2026: ****C++**** latest draft n5001 (2024-12-17)

Main Article: C++23

The next major revision of the C++ standard

### See also

|  |  |
| --- | --- |
| C documentation for History of C | |

### External links

|  |  |
| --- | --- |
| 1. | A History of C++: 1979-1991 |
| 2. | Evolving a language in and for the real world: C++ 1991-2006 |
| 3. | Thriving in a crowded and changing world: C++ 2006-2020 |
| 4. | Standard C++ foundation |
| 5. | C++ on Wikipedia |
| 6. | C++ Standards Committee |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/history&oldid=176073>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 September 2024, at 11:08.