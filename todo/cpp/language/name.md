# Identifiers

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

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ASCII | | | | |
| Punctuation | | | | |
| ****Names and identifiers**** | | | | |
| Types | | | | |
| Fundamental types | | | | |
| Objects | | | | |
| Scope | | | | |
| Object lifetime | | | | |
| Storage duration and linkage | | | | |
| Definitions and ODR | | | | |
| Name lookup | | | | |
| Qualified name lookup | | | | |
| Unqualified name lookup | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model | | | | |
| Multi-threaded executions and data races (C++11) | | | | |
| Character sets and encodings | | | | |
| Phases of translation | | | | |
| The `main` function | | | | |
| Modules (C++20) | | | | |

An **identifier** is an arbitrarily long sequence of digits, underscores, lowercase and uppercase Latin letters, and most Unicode characters.

The first character of a valid identifier must be one of the following:

- uppercase Latin letters A-Z
- lowercase Latin letters a-z
- underscore
- any Unicode character with the Unicode property XID_Start

Any other character of a valid identifier must be one of the following:

- digits 0-9
- uppercase Latin letters A-Z
- lowercase Latin letters a-z
- underscore
- any Unicode character with the Unicode property XID_Continue

The lists of characters with properties XID_Start and XID_Continue can be found in DerivedCoreProperties.txt.

Identifiers are case-sensitive (lowercase and uppercase letters are distinct), and every character is significant. Every identifier must conform to Normalization Form C.

Note: Support of Unicode identifiers is limited in most implementations, e.g. gcc (until 10).

### In declarations

An identifier can be used to name objects, references, functions, enumerators, types, class members, namespaces, templates, template specializations, parameter packs(since C++11), goto labels, and other entities, with the following exceptions:

- The identifiers that are keywords cannot be used for other purposes.

|  |  |
| --- | --- |
| - The only place they can be used as non-keywords is in an attribute-token (e.g. [[private]] is a valid attribute). | (since C++11) |

- The identifiers that are alternative representations for certain operators and punctuators cannot be used for other purposes.

|  |  |
| --- | --- |
| - The identifiers with special meaning (final, import, module(since C++20) and override) are used explicitly in a certain context rather than being regular identifiers.   - Unless otherwise specified, any ambiguity as to whether a given identifier has a special meaning is resolved to interpret the token as a regular identifier. | (since C++11) |

- Identifiers that appear as a token or preprocessing token (i.e., not in user-defined-string-literal like operator ""id)(since C++11) of one of the following forms are reserved:
  - in the global namespace, identifiers that begin with an underscore
  - identifiers that contain a double underscore or begin with an underscore followed by an uppercase letter, except the following identifiers:

:   :   - predefined macros (including language feature test macros)(since C++20)

|  |  |
| --- | --- |
| - std::_Exit - __func__ | (since C++11) |

:   :   - the following macros defined in the standard library:

        :   - the C-style I/O library macros _IOFBF, _IOLBF and _IONBF

|  |  |
| --- | --- |
| - the C compatibility macros __alignas_is_defined and __alignof_is_defined (defined in <stdalign.h>) - the C compatibility macro __bool_true_false_are_defined (defined in <stdbool.h>) | (since C++11) |
| - library feature test macros | (since C++20) |

“Reserved” here means that the standard library headers #define or declare such identifiers for their internal needs, the compiler may predefine non-standard identifiers of that kind, and that name mangling algorithm may assume that some of these identifiers are not in use. If the programmer uses such identifiers, the program is ill-formed, no diagnostic required.

In addition, it is undefined behavior to #define or #undef certain names in a translation unit, see reserved macro names for more details.

#### Zombie identifiers

As of C++14, some identifiers are removed from the C++ standard library. They are listed in the list of zombie names.

However, these identifiers are still reserved for previous standardization in a certain context. Removed member function names may not be used as a name for function-like macros, and other removed member names may not be used as a name for object-like macros in portable code.

### In expressions

An identifier that names a variable, a function, specialization of a concept,(since C++20) or an enumerator can be used as an expression. The result of an expression consisting of just the identifier is the entity named by the identifier. The value category of the expression is **lvalue** if the identifier names a function, a variable, a template parameter object(since C++20), or a data member, and **rvalue**(until C++11)**prvalue**(since C++11) otherwise (e.g. an enumerator is an rvalue(until C++11)a prvalue(since C++11) expression, a specialization of a concept is a bool prvalue(since C++20)).

#### Type

The type of an identifier expression is the same as the type of the entity it names.

|  |  |  |  |
| --- | --- | --- | --- |
| The following exceptions exist:   - If the entity named by the (unqualified) identifier is a local entity, and would result in an intervening lambda expression capturing it by copy if it were named outside of an unevaluated operand in the declarative region in which the identifier appears, then the type of the expression is the type of a class member access expression naming the non-static data member that would be declared for such a capture in the closure object of the innermost such intervening lambda expression.  ```text void f() {     float x, &r = x;       [=]     {         decltype(x) y1;        // y1 has type float         decltype((x)) y2 = y1; // y2 has type float const& because this lambda                                // is not mutable and x is an lvalue         decltype(r) r1 = y1;   // r1 has type float&         decltype((r)) r2 = y2; // r2 has type float const&     }; } ```  |  |  | | --- | --- | | - If the entity named is a template parameter object for a template parameter of type `T`, the type of the expression is const T. | (since C++20) | | (since C++11) |

#### Unqualified identifiers

Besides suitably declared identifiers, the following can be used in expressions in the same role:

- an overloaded operator name in function notation, such as operator+ or operator new;
- a user-defined conversion function name, such as operator bool;

|  |  |
| --- | --- |
| - a user-defined literal operator name, such as operator "" _km; | (since C++11) |

- a template name followed by its argument list, such as MyTemplate<int>;
- the character ~ followed by a class name, such as ~MyClass;

|  |  |
| --- | --- |
| - the character ~ followed by a decltype specifier, such as ~decltype(str). | (since C++11) |

|  |  |
| --- | --- |
| - the character ~ followed by a pack indexing specifier, such as ~pack...[0]. | (since C++26) |

Together with identifiers they are known as **unqualified identifier expressions**.

#### Qualified identifiers

A **qualified identifier expression** is an unqualified identifier expression prepended by a scope resolution operator ::, and optionally, a sequence of any of the following separated by scope resolution operators:

- a namespace name;
- a class name;

|  |  |
| --- | --- |
| - an enumeration name; - a `decltype` specifier denoting a class or enumeration type. | (since C++11) |

|  |  |
| --- | --- |
| - a pack indexing specifier denoting a class or enumeration type. | (since C++26) |

For example, the expression std::string::npos is an expression that names the static member npos in the class string in namespace std. The expression ::tolower names the function tolower in the global namespace. The expression ::std::cout names the global variable cout in namespace std, which is a top-level namespace. The expression boost::signals2::connection names the type connection declared in namespace signals2, which is declared in namespace boost.

The keyword template may appear in qualified identifiers as necessary to disambiguate dependent template names.

See qualified lookup for the details of the name lookup for qualified identifiers.

### Implicit member access transformation

If an identifier expression E denotes a non-static non-type member of some class `C` and all following conditions are satisfied, E is transformed into the class member access expression this->E:

- E is not the right operand of a member access operator.
- If E is a qualified identifier expression, E is not the un-parenthesized operand of an address-of operator.
- Any of the following conditions is satisfied:

:   - E is potentially evaluated.
    - `C` is the innermost enclosing class at E.
    - `C` is a base class of the innermost enclosing class at E.

This transformation does not apply in the template definition context (see dependent names).

```
struct X
{
    int x;
};
 
struct B
{
    int b;
};
 
struct D : B
{
    X d;
 
    void func()
    {
        d;   // OK, will be transformed into this->d
        b;   // OK, will be transformed into this->b
        x;   // Error: this->x is ill-formed
 
        d.x; // OK, will be transformed into this->d.x
             // instead of d.this->x or this->d.this->x
    }
};

```

### Names

A **name** is the use of one of the following to refer to an entity:

- an identifier
- an overloaded operator name in function notation (operator+, operator new)
- a user-defined conversion function name (operator bool)

|  |  |
| --- | --- |
| - a user-defined literal operator name (operator ""_km) | (since C++11) |

- a template name followed by its argument list (MyTemplate<int>)

Every name is introduced into the program by a declaration. A name used in more than one translation unit may refer to the same or different entities, depending on linkage.

When the compiler encounters an unknown name in a program, it associates it with the declaration that introduced the name by means of name lookup, except for the dependent names in template declarations and definitions (for those names, the compiler determines whether they name a type, a template, or some other entity, which may require explicit disambiguation).

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1440 | C++11 | decltype expressions preceding `::` could denote any type | can only denote class or enumeration types |
| CWG 1963 | C++11 | implementation-defined characters other than digits, non-digits and universal character names could be used in an identifier | prohibited |
| CWG 2521 | C++11 | the identifier in user-defined-string-literal of a literal operator was reserved as usual | the rules are different |
| CWG 2771 | C++98 | &a was not transformed into &this->a in class contexts | it is transformed |
| CWG 2777 | C++20 | the type of an identifier expression was unclear if it names a template parameter object | made clear |
| CWG 2818 | C++98 | predefined macro names are reserved | they are not reserved |

### See also

|  |  |
| --- | --- |
| C documentation for Identifiers | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/identifiers&oldid=178677>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 December 2024, at 09:25.