# Conflicting declarations

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

Declarations

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Overview | | | | | | Declaration syntax | | | | | | **decl-specifier-seq** | | | | | | Declarator | | | | | | ****Conflicting declarations**** | | | | | | Specifiers | | | | | | typedef | | | | | | inline | | | | | | virtual function specifier | | | | | | explicit function specifier | | | | | | friend | | | | | | constexpr(C++11) | | | | | | consteval(C++20) | | | | | | constinit(C++20) | | | | | | Storage class specifiers | | | | | | Translation-unit-local (C++20) | | | | | | class/struct | | | | | | union | | | | | | enum | | | | | | decltype(C++11) | | | | | | auto(C++11) | | | | | | alignas(C++11) | | | | | | constvolatile | | | | | | Pack indexing specifier (C++26) | | | | | | Elaborated type specifier | | | | | | Attributes (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Declarators | | | | | | Reference | | | | | | Pointer | | | | | | Array | | | | | | Block declarations | | | | | | Simple-declaration | | | | | | →Structured binding declaration (C++17) | | | | | | Alias declaration (C++11) | | | | | | Namespace alias definition | | | | | | using declaration | | | | | | `using` directive | | | | | | static_assert declaration (C++11) | | | | | | asm declaration | | | | | | Opaque enum declaration (C++11) | | | | | | Other declarations | | | | | | Namespace definition | | | | | | Function declaration | | | | | | Class template declaration | | | | | | Function template declaration | | | | | | Explicit template instantiation (C++11) | | | | | | Explicit template specialization | | | | | | Linkage specification | | | | | | Attribute declaration (C++11) | | | | | | Empty declaration | | | | | |  | | | | | |

Unless otherwise specified, two declarations cannot (re)introduce the same entity. The program is ill-formed if such declarations exist.

### Corresponding declarations

Two declarations **correspond** if they (re)introduce the same name, both declare constructors, or both declare destructors, unless

- either is a using declaration,
- one declares a type (not a typedef name) and the other declares a variable, non-static data member other than of an anonymous union, enumerator, function, or function template, or
- each declares a function or function template and they do not declare corresponding overloads.

#### Corresponding function overloads

Two function declarations declare **corresponding overloads** if both declare functions satisfying all following conditions:

- They have the same parameter-type-list, omitting the types of explicit object parameters(since C++23).

|  |  |
| --- | --- |
| - They have equivalent trailing requires clauses (if any, except friend declarations). | (since C++20) |

- If both of them are non-static member functions, they need to additionally satisfy one of the following requirements:

|  |  |
| --- | --- |
| - Exactly one of them is an implicit object member function without ref-qualifier and the types of their object parameters, after removing top-level references, are the same. | (since C++23) |

:   - Their object parameters have the same type.

#### Corresponding function template overloads

Two function template declarations declare **corresponding overloads** if both declare function templates satisfying all following conditions:

- Their template parameter lists have the same length.
- Their corresponding template parameters are equivalent.
- They have equivalent parameter-type-lists, omitting the types of explicit object parameters(since C++23).
- They have equivalent return types.

|  |  |
| --- | --- |
| - Their corresponding template parameters are either both declared without constraint, or both declared with equivalent constraints. - They have equivalent trailing requires clauses (if any). | (since C++20) |

- If both are non-static members function templates, they need to additionally satisfy one of the following requirements:

|  |  |
| --- | --- |
| - Exactly one of them is an implicit object member function template without ref-qualifier and the types of their object parameters, after removing all references, are equivalent. | (since C++23) |

:   - Their object parameters have equivalent types.

```
struct A
{
    friend void c();   // #1
};
 
struct B
{
    friend void c() {} // corresponds to, and defines, #1
};
 
typedef int Int;
 
enum E : int { a };
 
void f(int);   // #2
void f(Int) {} // defines #2
void f(E) {}   // OK, another overload
 
struct X
{
    static void f();
    void f() const;   // error: redeclaration
 
    void g();
    void g() const;   // OK
    void g() &;       // error: redeclaration
 
    void h(this X&, int);
    void h(int) &&;   // OK, another overload
 
    void j(this const X&);
    void j() const &; // error: redeclaration
 
    void k();
    void k(this X&);  // error: redeclaration
};

```

### Multiple declarations of the same entity

|  |  |
| --- | --- |
| A declaration is **name-independent** if its name is _ and it declares   - a variable with automatic storage duration, - a structured binding with no storage class specifier and not inhabiting a namespace scope, - the variable introduced by a lambda capture with an initializer, or - a non-static data member of other than an anonymous union. | (since C++26) |

Unless otherwise specified, two declarations of entities **declare the same entity** if all following conditions are satisfied, considering declarations of unnamed types to introduce their typedef names and enumeration names for linkage purposes (if any exists):

- They correspond.
- They have the same target scope, which is not a function parameter scope or a template parameter scope.

|  |  |
| --- | --- |
| - Neither is a name-independent declaration. | (since C++26) |

- One of the following conditions is satisfied:

:   - They appear in the same translation unit.

|  |  |
| --- | --- |
| - They both declare names with module linkage and are attached to the same module. | (since C++20) |

:   - They both declare names with external linkage.

A declaration of an entity or typedef name `X` is a **redeclaration** of `X` if another declaration of `X` is reachable from it.

#### Restrictions

If any two declarations of an entity `E` violate the corresponding restriction below, the program is ill-formed:

- If one declares `E` to be a variable, the other must also declare `E` as a variable of the same type.
- If one declares `E` to be a function, the other must also declare `E` as a function of the same type.
- If one declares `E` to be an enumerator, the other must also declare `E` as an enumerator.
- If one declares `E` to be a namespace, the other must also declare `E` as a namespace.
- If one declares `E` to be a class type, the other must also declare `E` as a class type.
- If one declares `E` to be an enumeration type, the other must also declare `E` as an enumeration type.
- If one declares `E` to be a class template, the other must also declare `E` as a class template with an equivalent template parameter list (see function template overloading).
- If one declares `E` to be a function template, the other must also declare `E` as a function template with an equivalent template parameter list and type.

|  |  |
| --- | --- |
| - If one declares `E` to be an alias template, the other must also declare `E` as an alias template with an equivalent template parameter list and type-id. | (since C++11) |
| - If one declares `E` to be a (partial specialization of a) variable template, the other must also declare `E` as a (partial specialization of a) variable template with an equivalent template parameter list and type. | (since C++14) |
| - If one declares `E` to be a concept, the other must also declare `E` as a concept. | (since C++20) |

Types are compared after all adjustments of types (during which typedefs are replaced by their definitions). Declarations for an array object can specify array types that differ by the presence or absence of a major array bound. No diagnostic is required if neither declaration is reachable from the other.

```
void g();      // #1
void g(int);   // OK, different entity from #1 (they do not correspond)
int g();       // Error: same entity as #1 with different type
 
void h();      // #2
namespace h {} // Error: same entity as #2, but not a function

```

If a declaration `H` that declares a name with internal linkage precedes a declaration `D` in another translation unit `U` and would declare the same entity as `D` if it appeared in `U`, the program is ill-formed.

### Potentially-conflicting declarations

Two declarations **potentially conflict** if they correspond but declare different entities.

If, in any scope, a name is bound to two declarations `A` and `B` that potentially conflict, `B` is not name-independent(since C++26), and `A` precedes `B`, the program is ill-formed:

```
void f()
{
    int x, y;
    void x(); // Error: different entity for x
    int y;    // Error: redefinition
}
 
enum { f };   // Error: different entity for ::f
 
namespace A {}
namespace B = A;
namespace B = A; // OK, no effect
namespace B = B; // OK, no effect
namespace A = B; // OK, no effect
namespace B {}   // Error: different entity for B
 
void g()
{
    int _;
    _ = 0; // OK
    int _; // OK since C++26, name-independent declaration
    _ = 0; // Error: two non-function declarations in the lookup set
}
 
void h ()
{
    int _;        // #1
    _ ++;         // OK
    static int _; // Error: conflicts with #1 because
                  // static variables are not name-independent
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 279 (P1787R6) | C++98 | it was unclear whether an unnamed class or enumeration can be redeclared if it has a typedef name for linkage purposes | it can be redeclared |
| CWG 338 (P1787R6) | C++98 | it was unclear whether an unnamed enumeration can be redeclared if it has an enumerator as a name for linkage purposes | it can be redeclared |
| CWG 1884 (P1787R6) | C++98 | the restrictions applied to multiple declarations of the same entity were unclear | made clear |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/conflicting_declarations&oldid=174029>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 August 2024, at 00:02.