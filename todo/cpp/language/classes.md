# Classes

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
| ****Classes**** | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | Constructors | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Access specifiers | | | | | | `friend` specifier | | | | | |  | | | | | |
| Class-specific function properties | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Virtual function | | | | | | `override` specifier (C++11) | | | | | | `final` specifier (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | explicit (C++11) | | | | | | static | | | | | |  | | | | | |
| Special member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default constructor | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | Destructor | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 ****Classes****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| ****Overview**** | | | | |
| `class`/`struct` types | | | | |
| `union` types | | | | |
| Injected-class-name | | | | |
| Members | | | | |
| Data members | | | | |
| Static members | | | | |
| The `this` pointer | | | | |
| Nested classes | | | | |
| Member templates | | | | |
| Bit-fields | | | | |
| `using`-declarations | | | | |
| Member functions | | | | |
| Member access specifiers | | | | |
| Constructors and member initializer lists | | | | |
| Default member initializer (C++11) | | | | |
| `friend` specifier | | | | |
| `explicit` specifier | | | | |
| Converting constructor | | | | |
| Special member functions | | | | |
| Default constructor | | | | |
| Copy constructor | | | | |
| Move constructor (C++11) | | | | |
| Copy assignment operator | | | | |
| Move assignment operator (C++11) | | | | |
| Destructor | | | | |
| Inheritance | | | | |
| Base and derived classes | | | | |
| Empty base optimization (EBO) | | | | |
| Virtual member functions | | | | |
| Pure virtual functions and abstract classes | | | | |
| `override` specifier (C++11) | | | | |
| `final` specifier (C++11) | | | | |

A class is a user-defined type.

A class type is defined by class-specifier, which appears in decl-specifier-seq of the declaration syntax. See class declaration for the syntax of the class specifier.

A class can have the following kinds of members:

1) data members:a) non-static data members, including bit-fields.b) static data members2) member functions:a) non-static member functionsb) static member functions3) nested types:a) nested classes and enumerations defined within the class definitionb) aliases of existing types, defined with `typedef` or type alias (since C++11)declarationsc) the name of the class within its own definition acts as a public member type alias of itself for the purpose of lookup (except when used to name a constructor): this is known as **injected-class-name**4) enumerators from all unscoped enumerations defined within the class, or introduced by using-declarations or using-enum-declarations(since C++20)5) member templates (variable templates, (since C++14)class templates or function templates) may appear in the body of any non-local class/struct/union.

All members are defined at once in the class definition, they cannot be added to an already-defined class (unlike the members of namespaces)

A member of a class `T` cannot use `T` as its name if the member is

- a static data member,
- a member function,
- a member type,
- a member template,
- an enumerator of an enumeration (unless the enumeration is scoped)(since C++11), or
- a member of a member anonymous union.

However, a non-static data member may use the name `T` as long as there are no user-declared constructors.

A class with at least one declared or inherited virtual member function is **polymorphic**. Objects of this type are polymorphic objects and have runtime type information stored as part of the object representation, which may be queried with `dynamic_cast` and `typeid`. Virtual member functions participate in dynamic binding.

A class with at least one declared or inherited pure virtual member function is an abstract class. Objects of this type cannot be created.

|  |  |
| --- | --- |
| A class with a constexpr constructor is a LiteralType: objects of this type can be manipulated by constexpr functions at compile time. | (since C++11) |

### Properties of classes

|  |  |  |  |
| --- | --- | --- | --- |
| Trivially copyable class A **trivially copyable class** is a class that   - has at least one eligible copy constructor, move constructor, copy assignment operator, or move assignment operator, - each eligible copy constructor is trivial - each eligible move constructor is trivial - each eligible copy assignment operator is trivial - each eligible move assignment operator is trivial, and - has a non-deleted trivial destructor.  |  |  | | --- | --- | | Trivial class A **trivial class** is a class that   - is trivially copyable, and - has one or more eligible default constructors such that each is trivial. | (deprecated in C++26) |  Standard-layout class A **standard-layout class** is a class that   - has no non-static data members of type non-standard-layout class (or array of such types) or reference, - has no virtual functions and no virtual base classes, - has the same access control for all non-static data members, - has no non-standard-layout base classes, - only one class in the hierarchy has non-static data members, and - Informally, none of the base classes has the same type as the first non-static data member. Or, formally: given the class as S, has no element of the set M(S) of types as a base class, where M(X) for a type X is defined as:   - If X is a non-union class type with no (possibly inherited) non-static data members, the set M(X) is empty. - If X is a non-union class type whose first non-static data member has type X0 (where said member may be an anonymous union), the set M(X) consists of X0 and the elements of M(X0). - If X is a union type, the set M(X) is the union of all M(Ui) and the set containing all Ui, where each Ui is the type of the ith non-static data member of X. - If X is an array type with element type Xe, the set M(X) consists of Xe and the elements of M(Xe). - If X is a non-class, non-array type, the set M(X) is empty.  A **standard-layout struct** is a standard-layout class defined with the class keyword struct or the class keyword class. A **standard-layout union** is a standard-layout class defined with the class keyword union. | (since C++11) |

#### Implicit-lifetime class

An **implicit-lifetime class** is a class that

- is an aggregate whose destructor is not user-declared(until C++11)user-provided(since C++11), or
- has at least one trivial eligible constructor and a trivial, non-deleted destructor.

Notes: the implicit-lifetime property is clarified by defect report P0593R6.

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| POD class A **POD class** is a class that   |  |  | | --- | --- | | - is an aggregate, - has no user-declared copy assignment operator, - has no user-declared destructor, and - has no non-static data members of type non-POD class (or array of such types) or reference. | (until C++11) | | - is a trivial class, - is a standard-layout class, and - has no non-static data members of type non-POD class (or array of such types). | (since C++11) |   A **POD struct** is a non-union POD class. A **POD union** is a union that is a POD class. | (deprecated in C++20) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 148 | C++98 | POD classes could not contain pointers to member, which are themselves POD (scalar) types | restriction removed |
| CWG 383 | C++98 | copy assignment operators or destructors could be user-declared in POD classes if they are not defined | not allowed |
| CWG 1363 | C++11 | a class that has both trivial default constructors and non-trivial  default constructors at the same time could be trivial | it is non-trivial |
| CWG 1496 | C++11 | a class that only has constructors that are all defined as deleted could be trivial | it is non-trivial |
| CWG 1672 | C++11 | a class could be a standard-layout class if it has multiple empty base classes | it is not a standard-layout class |
| CWG 1734 | C++11 | a trivially copyable class could not have non-trivial deleted copy/move constructors/assignment operators | can be trivial if deleted |
| CWG 1813 | C++11 | a class was never a standard-layout class if it has a base class that inherits a non-static data member | it can be a standard-layout class |
| CWG 1881 | C++11 | for a standard-layout class and its base classes, unnamed bit-fields might be declared in a different class declaring the data members | all non-static data members and bit-fields need to be first declared in the same class |
| CWG 1909 | C++98 | a member template could have the same name as its class | prohibited |
| CWG 2120 | C++11 | the definition of M(X) in determining a standard- layout class did not consider the case of a class whose first member is an array | addressed this case in the definition of M(X) |
| CWG 2605 | C++98 | an implicit-lifetime class could have a user-provided destructor | prohibited |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/classes&oldid=178050>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 November 2024, at 21:58.