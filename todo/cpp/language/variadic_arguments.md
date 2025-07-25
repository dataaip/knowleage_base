# Variadic arguments

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 Functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Declarations | | | | |
| Function declaration | | | | |
| Function parameter list | | | | |
| Function definition | | | | |
| Default arguments | | | | |
| ****Variadic arguments**** | | | | |
| `inline` specifier | | | | |
| Lambda expressions (C++11) | | | | |
| Coroutines (C++20) | | | | |
| Function calls | | | | |
| Argument-Dependent Lookup (ADL) | | | | |
| Function-call operator | | | | |
| Function objects | | | | |
| Overloading | | | | |
| Overload resolution | | | | |
| Operator overloading | | | | |
| Address of an overload set | | | | |

Allows a function to accept any number of extra arguments.

A function is a variadic if the last parameter of its parameter list is an ellipsis (...).

|  |  |
| --- | --- |
| The comma preceding the ellipsis can be omitted. | (deprecated in C++26) |

```
// the function declared as follows
int printx(const char* fmt, ...);
int printx(const char* fmt...); // same as above, but deprecated since C++26
 
// may be called with one or more arguments:
printx("hello world");
printx("a=%d b=%d", a, b);
 
int printy(..., const char* fmt); // error: ... can only be the last parameter
int printz(...); // valid, but the arguments cannot be accessed portably

```

|  |  |
| --- | --- |
| This is different from a function parameter pack expansion, which is indicated by an ellipsis that is a part of a parameter declarator, rather than an ellipsis being a parameter alone. Both parameter pack expansion and the “variadic” ellipsis may appear in the declaration of a function template, as in the case of std::is_function. | (since C++11) |

### Default argument promotions

When a variadic function is called, after lvalue-to-rvalue, array-to-pointer, and function-to-pointer conversions, each argument that is a part of the variable argument list undergoes additional conversions known as **default argument promotions**:

|  |  |
| --- | --- |
| - std::nullptr_t is converted to void\*. | (since C++11) |

- float arguments are converted to double as in floating-point promotion.
- bool, char, short, and unscoped enumerations are converted to int or wider integer types as in integral promotion.

Non-POD class types(until C++11)Scoped enumerations and class types with an eligible non-trivial copy constructor, an eligible non-trivial move constructor, or a non-trivial destructor(since C++11) are conditionally-supported in potentially-evaluated calls with implementation-defined semantics (these types are always supported in unevaluated calls).

Because variadic parameters have the lowest rank for the purpose of overload resolution, they are commonly used as the catch-all fallbacks in SFINAE.

Within the body of a function that uses variadic arguments, the values of these arguments may be accessed using the `<cstdarg>` library facilities:

|  |  |
| --- | --- |
| Defined in header `<cstdarg>` | |
| va_start | enables access to variadic function arguments   (function macro) |
| va_arg | accesses the next variadic function argument   (function macro) |
| va_copy(C++11) | makes a copy of the variadic function arguments   (function macro) |
| va_end | ends traversal of the variadic function arguments   (function macro) |
| va_list | holds the information needed by va_start, va_arg, va_end, and va_copy   (typedef) |

The behavior of the va_start macro is undefined if the last parameter before the ellipsis has reference type, or has type that is not compatible with the type that results from default argument promotions.

|  |  |
| --- | --- |
| If the a pack expansion or an entity resulting from a lambda capture is used as the last parameter in va_start, the program is ill-formed, no diagnostic required. | (since C++11) |

### Alternatives

|  |  |
| --- | --- |
| - Variadic templates can also be used to create functions that take variable number of arguments. They are often the better choice because they do not impose restrictions on the types of the arguments, do not perform integral and floating-point promotions, and are type safe. - If all variable arguments share a common type, a std::initializer_list provides a convenient mechanism (albeit with a different syntax) for accessing variable arguments. In this case however the arguments cannot be modified since std::initializer_list can only provide a const pointer to its elements. | (since C++11) |

### Notes

In the C programming language until C23, at least one named parameter must appear before the ellipsis parameter, so R printz(...); is not valid until C23. In C++, this form is allowed even though the arguments passed to such function are not accessible, and is commonly used as the fallback overload in SFINAE, exploiting the lowest priority of the ellipsis conversion in overload resolution.

This syntax for variadic arguments was introduced in 1983 C++ without the comma before the ellipsis. When C89 adopted function prototypes from C++, it replaced the syntax with one requiring the comma. For compatibility, C++98 accepts both C++-style f(int n...) and C-style f(int n, ...). The original C++-style grammar is deprecated since C++26.

|  |  |
| --- | --- |
| The comma can be used in abbreviated function templates to make the ellipsis signify a variadic function instead of a variadic template:  void f1(auto...);   // same as template<class... Ts> void f3(Ts...) void f2(auto, ...); // same as template<class T> void f3(T, ...) | (since C++20) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 506 | C++98 | passing non-POD class arguments to an ellipsis resulted in undefined behavior | passing such arguments is conditionally-supported with implementation-defined semantics |
| CWG 634 | C++98 | conditionally-supported class types made some SFINAE idioms not work | always supported if unevaluated |
| CWG 2247 | C++11 | no restriction on passing parameter pack or lambda capture to `va_start` | made ill-formed, no diagnostic required |
| CWG 2347 | C++11 | it was unclear whether scoped enumerations passed to an ellipsis are subject to default argument promotions | passing scoped enumerations is conditionally-supported with implementation-defined semantics |

### See also

|  |  |
| --- | --- |
| C documentation for Variadic arguments | |
| C documentation for Implicit conversions | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/variadic_arguments&oldid=179642>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 January 2025, at 04:00.