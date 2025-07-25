# Declarations

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

****Declarations****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Overview | | | | | | ****Declaration syntax**** | | | | | | **decl-specifier-seq** | | | | | | Declarator | | | | | | Conflicting declarations | | | | | | Specifiers | | | | | | typedef | | | | | | inline | | | | | | virtual function specifier | | | | | | explicit function specifier | | | | | | friend | | | | | | constexpr(C++11) | | | | | | consteval(C++20) | | | | | | constinit(C++20) | | | | | | Storage class specifiers | | | | | | Translation-unit-local (C++20) | | | | | | class/struct | | | | | | union | | | | | | enum | | | | | | decltype(C++11) | | | | | | auto(C++11) | | | | | | alignas(C++11) | | | | | | constvolatile | | | | | | Pack indexing specifier (C++26) | | | | | | Elaborated type specifier | | | | | | Attributes (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Declarators | | | | | | Reference | | | | | | Pointer | | | | | | Array | | | | | | Block declarations | | | | | | ****Simple-declaration**** | | | | | | →Structured binding declaration (C++17) | | | | | | Alias declaration (C++11) | | | | | | Namespace alias definition | | | | | | using declaration | | | | | | `using` directive | | | | | | static_assert declaration (C++11) | | | | | | asm declaration | | | | | | Opaque enum declaration (C++11) | | | | | | Other declarations | | | | | | Namespace definition | | | | | | Function declaration | | | | | | Class template declaration | | | | | | Function template declaration | | | | | | Explicit template instantiation (C++11) | | | | | | Explicit template specialization | | | | | | Linkage specification | | | | | | ****Attribute declaration**** (C++11) | | | | | | ****Empty declaration**** | | | | | |  | | | | | |

**Declarations** are how names are introduced (or re-introduced) into the C++ program. Not all declarations actually declare anything, and each kind of entity is declared differently. Definitions are declarations that are sufficient to use the entity identified by the name.

A declaration is one of the following:

- Function definition
- Template declaration (including Partial template specialization)
- Explicit template instantiation
- Explicit template specialization
- Namespace definition
- Linkage specification

|  |  |
| --- | --- |
| - Attribute declaration (attr `;`) | (since C++11) |

- Empty declaration (`;`)
- A function declaration without a decl-specifier-seq ﻿:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr ﻿(optional) declarator `;` |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| attr | - | (since C++11) sequence of any number of attributes |
| declarator | - | a function declarator |

:   This declaration must declare a constructor, destructor, or user-defined type conversion function. It can only be used as part of a template declaration, explicit specialization, or explicit instantiation.

- block-declaration (a declaration that can appear inside a block), which, in turn, can be one of the following:

:   - asm declaration

|  |  |
| --- | --- |
| - type alias declaration | (since C++11) |

:   - namespace alias definition
    - using-declaration
    - using directive

|  |  |
| --- | --- |
| - using-enum-declaration | (since C++20) |
| - `static_assert` declaration - opaque enum declaration | (since C++11) |

:   - simple declaration

### Simple declaration

A simple declaration is a statement that introduces, creates, and optionally initializes one or several identifiers, typically variables.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| decl-specifier-seq init-declarator-list ﻿(optional) `;` | (1) |  |
|  | | | | | | | | | |
| attr decl-specifier-seq init-declarator-list`;` | (2) |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| attr | - | (since C++11) sequence of any number of attributes |
| decl-specifier-seq | - | sequence of **specifiers** (see below) |
| init-declarator-list | - | comma-separated list of **declarators** with optional initializers. init-declarator-list is optional when declaring a named class/struct/union or a named enumeration |

A structured binding declaration is also a simple declaration.(since C++17)

### Specifiers

****Declaration specifiers**** (decl-specifier-seq) is a sequence of the following whitespace-separated specifiers, in any order:

- the `typedef` specifier. If present, the entire declaration is a typedef declaration and each declarator introduces a new type name, not an object or a function.
- function specifiers (`inline`, `virtual`, `explicit`), only allowed in function declarations.

|  |  |
| --- | --- |
| - the `inline` specifier is also allowed on variable declarations. | (since C++17) |

- the `friend` specifier, allowed in class and function declarations.

|  |  |
| --- | --- |
| - the `constexpr` specifier, only allowed in variable definitions, function and function template declarations, and the declaration of static data members of literal type. | (since C++11) |
| - the `consteval` specifier, only allowed in function and function template declarations. - the `constinit` specifier, only allowed in declaration of a variable with static or thread storage duration. At most one of the constexpr, consteval, and constinit specifiers is allowed to appear in a decl-specifier-seq. | (since C++20) |

- storage class specifier (register, (until C++17) static, thread_local, (since C++11) extern, mutable). Only one storage class specifier is allowed, except that thread_local may appear together with extern or static(since C++11).
- ****Type specifiers**** (type-specifier-seq), a sequence of specifiers that names a type. The type of every entity introduced by the declaration is this type, optionally modified by the declarator (see below). This sequence of specifiers is also used by type-id. Only the following specifiers are part of type-specifier-seq, in any order:

:   - class specifier
    - enum specifier
    - simple type specifier

    :   - char, char8_t, (since C++20) char16_t, char32_t, (since C++11) wchar_t, bool, short, int, long, signed, unsigned, float, double, void

|  |  |
| --- | --- |
| - `auto` - decltype specifier | (since C++11) |
| - pack indexing specifier | (since C++26) |

:   :   - previously declared class name (optionally qualified)
        - previously declared enum name (optionally qualified)
        - previously declared typedef-name or type alias(since C++11) (optionally qualified)
        - template name with template arguments (optionally qualified, optionally using template disambiguator)

|  |  |
| --- | --- |
| - template name without template arguments (optionally qualified): see class template argument deduction | (since C++17) |

:   - elaborated type specifier

    :   - the keyword class, struct, or union, followed by the identifier (optionally qualified), previously defined as the name of a class.
        - the keyword class, struct, or union, followed by template name with template arguments (optionally qualified, optionally using template disambiguator), previously defined as the name of a class template.
        - the keyword enum followed by the identifier (optionally qualified), previously declared as the name of an enumeration.

    - typename specifier
    - cv qualifier
:   only one type specifier is allowed in a decl-specifier-seq, with the following exceptions:

    - const can be combined with any type specifier except itself.
    - volatile can be combined with any type specifier except itself.
    - signed or unsigned can be combined with char, long, short, or int.
    - short or long can be combined with int.
    - long can be combined with double.

|  |  |
| --- | --- |
| - long can be combined with long. | (since C++11) |

Attributes may appear in decl-specifier-seq, in which case they apply to the type determined by the preceding specifiers.

Repetitions of any specifier in a decl-specifier-seq, such as const static const, or virtual inline virtual are errors, except that long is allowed to appear twice(since C++11).

### Declarators

init-declarator-list is a comma-separated sequence of one or more init-declarators, which have the following syntax:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| declarator initializer ﻿(optional) | (1) |  |
|  | | | | | | | | | |
| declarator requires-clause | (2) | (since C++20) |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| declarator | - | the declarator |
| initializer | - | optional initializer (except where required, such as when initializing references or const objects). See Initialization for details. |
| requires-clause | - | a requires-clause, which adds a constraint to a function declaration |

Each init-declarator in an init-declarator sequence S D1, D2, D3; is processed as if it were a standalone declaration with the same specifiers: S D1; S D2; S D3;.

Each declarator introduces exactly one object, reference, function, or (for typedef declarations) type alias, whose type is provided by decl-specifier-seq and optionally modified by operators such as & (reference to) or [] (array of) or () (function returning) in the declarator. These operators can be applied recursively, as shown below.

A declarator is one of the following:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| unqualified-id attr ﻿(optional) | (1) |  |
|  | | | | | | | | | |
| qualified-id attr ﻿(optional) | (2) |  |
|  | | | | | | | | | |
| `...` identifier attr ﻿(optional) | (3) | (since C++11) |
|  | | | | | | | | | |
| `*` attr ﻿(optional) cv ﻿(optional) declarator | (4) |  |
|  | | | | | | | | | |
| nested-name-specifier `*` attr ﻿(optional) cv ﻿(optional) declarator | (5) |  |
|  | | | | | | | | | |
| `&` attr ﻿(optional) declarator | (6) |  |
|  | | | | | | | | | |
| `&&` attr ﻿(optional) declarator | (7) | (since C++11) |
|  | | | | | | | | | |
| noptr-declarator `[` constexpr ﻿(optional) `]` attr ﻿(optional) | (8) |  |
|  | | | | | | | | | |
| noptr-declarator `(` parameter-list `)` cv ﻿(optional) ref ﻿ ﻿(optional) except ﻿(optional) attr ﻿(optional) | (9) |  |
|  | | | | | | | | | |

1) The name that is declared.2) A declarator that uses a qualified identifier (qualified-id) defines or redeclares a previously declared namespace member or class member.3) Parameter pack, only appears in parameter declarations.4) Pointer declarator: the declaration S \* D; declares `D` as a pointer to the type determined by decl-specifier-seq `S`.5) Pointer to member declaration: the declaration S C::\* D; declares `D` as a pointer to member of `C` of type determined by decl-specifier-seq `S`. nested-name-specifier is a sequence of names and scope resolution operators `::`6) Lvalue reference declarator: the declaration S & D; declares `D` as an lvalue reference to the type determined by decl-specifier-seq `S`.7) Rvalue reference declarator: the declaration S && D; declares `D` as an rvalue reference to the type determined by decl-specifier-seq `S`.8) Array declarator. noptr-declarator any valid declarator, but if it begins with \*, &, or &&, it has to be surrounded by parentheses.9) Function declarator. noptr-declarator any valid declarator, but if it begins with \*, &, or &&, it has to be surrounded by parentheses. It may end with the optional trailing return type.(since C++11)

|  |  |
| --- | --- |
| In all cases, attr is an optional sequence of attributes. When appearing immediately after the identifier, it applies to the object being declared. | (since C++11) |

cv is a sequence of const and volatile qualifiers, where either qualifier may appear at most once in the sequence.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: explain declaration name hiding rules; how a variable/function declaration hides a class (but not a typedef) with the same name |

### Notes

When a block-declaration appears inside a block, and an identifier introduced by a declaration was previously declared in an outer block, the outer declaration is hidden for the remainder of the block.

If a declaration introduces a variable with automatic storage duration, it is initialized when its declaration statement is executed. All automatic variables declared in a block are destroyed on exit from the block (regardless how the block is exited: via exception, goto, or by reaching its end), in order opposite to their order of initialization.

### Example

Note: this example demonstrates how some complex declarations are parsed in terms of the language grammar. Other popular mnemonics are: the spiral rule, reading inside-out, and declaration mirrors use. There is also an automated parser at <https://cdecl.org>.

Run this code

```
#include <type_traits>
 
struct S
{
    int member;
    // decl-specifier-seq is "int"
    // declarator is "member"
} obj, *pObj(&obj);
// decl-specifier-seq is "struct S { int member; }"
// declarator "obj" declares an object of type S
// declarator "*pObj" declares a pointer to S,
//     and initializer "(&obj)" initializes it
 
int i = 1, *p = nullptr, f(), (*pf)(double);
// decl-specifier-seq is "int"
// declarator "i" declares a variable of type int,
//     and initializer "= 1" initializes it
// declarator "*p" declares a variable of type int*,
//     and initializer "= nullptr" initializes it
// declarator "f()" declares (but doesn't define)
//     a function taking no arguments and returning int
// declarator "(*pf)(double)" declares a pointer to function
//     taking double and returning int
 
int (*(*var1)(double))[3] = nullptr;
// decl-specifier-seq is "int"
// declarator is "(*(*var1)(double))[3]"
// initializer is "= nullptr"
 
// 1. declarator "(*(*var1)(double))[3]" is an array declarator:
//    Type declared is: "(*(*var1)(double))" array of 3 elements
// 2. declarator "(*(*var1)(double))" is a pointer declarator:
//    Type declared is: "(*var1)(double)" pointer to array of 3 elements
// 3. declarator "(*var1)(double)" is a function declarator:
//    Type declared is: "(*var1)" function taking "(double)",
//    returning pointer to array of 3 elements.
// 4. declarator "(*var1)" is a pointer declarator:
//    Type declared is: "var1" pointer to function taking "(double)",
//    returning pointer to array of 3 elements.
// 5. declarator "var1" is an identifier.
// This declaration declares the object var1 of type "pointer to function
// taking double and returning pointer to array of 3 elements of type int"
// The initializer "= nullptr" provides the initial value of this pointer.
 
// C++11 alternative syntax:
auto (*var2)(double) -> int (*)[3] = nullptr;
// decl-specifier-seq is "auto"
// declarator is "(*var2)(double) -> int (*)[3]"
// initializer is "= nullptr"
 
// 1. declarator "(*var2)(double) -> int (*)[3]" is a function declarator:
//    Type declared is: "(*var2)" function taking "(double)", returning "int (*)[3]"
// ...
 
int main()
{
    static_assert(std::is_same_v<decltype(var1), decltype(var2)>);
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 482 | C++98 | the declarators of redeclarations could not be qualified | qualified declarators allowed |
| CWG 569 | C++98 | a single standalone semicolon was not a valid declaration | it is an empty declaration, which has no effect |
| CWG 1830 | C++98 | repetition of a function specifier in a decl-specifier-seq was allowed | repetition is forbidden |

### See also

|  |  |
| --- | --- |
| C documentation for Declarations | |

|  |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/declarations&oldid=169173>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 January 2024, at 23:10.