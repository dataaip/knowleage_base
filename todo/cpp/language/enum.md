# Enumeration declaration

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Fundamental types | | | | | | ****Enumeration types**** | | | | | | Function types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class/struct types | | | | | | Union types | | | | | |  | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Overview | | | | | | Declaration syntax | | | | | | **decl-specifier-seq** | | | | | | Declarator | | | | | | Conflicting declarations | | | | | | Specifiers | | | | | | typedef | | | | | | inline | | | | | | virtual function specifier | | | | | | explicit function specifier | | | | | | friend | | | | | | constexpr(C++11) | | | | | | consteval(C++20) | | | | | | constinit(C++20) | | | | | | Storage class specifiers | | | | | | Translation-unit-local (C++20) | | | | | | class/struct | | | | | | union | | | | | | ****enum**** | | | | | | decltype(C++11) | | | | | | auto(C++11) | | | | | | alignas(C++11) | | | | | | constvolatile | | | | | | Pack indexing specifier (C++26) | | | | | | Elaborated type specifier | | | | | | Attributes (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Declarators | | | | | | Reference | | | | | | Pointer | | | | | | Array | | | | | | Block declarations | | | | | | Simple-declaration | | | | | | →Structured binding declaration (C++17) | | | | | | Alias declaration (C++11) | | | | | | Namespace alias definition | | | | | | using declaration | | | | | | `using` directive | | | | | | static_assert declaration (C++11) | | | | | | asm declaration | | | | | | ****Opaque enum declaration**** (C++11) | | | | | | Other declarations | | | | | | Namespace definition | | | | | | Function declaration | | | | | | Class template declaration | | | | | | Function template declaration | | | | | | Explicit template instantiation (C++11) | | | | | | Explicit template specialization | | | | | | Linkage specification | | | | | | Attribute declaration (C++11) | | | | | | Empty declaration | | | | | |  | | | | | |

An **enumeration** is a distinct type whose value is restricted to a range of values (see below for details), which may include several explicitly named constants ("**enumerators**").

The values of the constants are values of an integral type known as the **underlying type** of the enumeration. An enumeration has the same size, value representation, and alignment requirements as its underlying type. Furthermore, each value of an enumeration has the same representation as the corresponding value of the underlying type.

An enumeration is (re)declared using the following syntax:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| enum-key attr ﻿(optional) enum-head-name ﻿(optional) enum-base ﻿(optional) `{` enumerator-list ﻿(optional) `}` | (1) |  |
|  | | | | | | | | | |
| enum-key attr ﻿(optional) enum-head-name ﻿(optional) enum-base ﻿(optional) `{` enumerator-list `, }` | (2) |  |
|  | | | | | | | | | |
| enum-key attr ﻿(optional) enum-head-name enum-base ﻿(optional) `;` | (3) | (since C++11) |
|  | | | | | | | | | |

1) enum-specifier, which appears in decl-specifier-seq of the declaration syntax: defines the enumeration type and its enumerators.2) A trailing comma can follow the enumerator-list.3) Opaque enum declaration: defines the enumeration type but not its enumerators: after this declaration, the type is a complete type and its size is known.

|  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| enum-key | - | |  |  | | --- | --- | | `enum` | (until C++11) | | one of `enum`, `enum class`, or `enum struct` | (since C++11) | |
| attr | - | (since C++11) optional sequence of any number of attributes |
| enum-head-name | - | |  |  | | --- | --- | | the name of the enumeration that's being declared, it can be omitted. | (until C++11) | | the name of the enumeration that's being declared, optionally preceded by a nested-name-specifier: sequence of names and scope-resolution operators `::`, ending with scope-resolution operator. It can only be omitted in unscoped non-opaque enumeration declarations.  nested-name-specifier may only appear if the enumeration name is present and this declaration is a redeclaration. For opaque enumeration declarations, nested-name-specifier can only appear before the name of the enumeration in explicit specialization declarations.  If nested-name-specifier is present, the **enum-specifier** cannot refer to an enumeration merely inherited or introduced by a using declaration, and the **enum-specifier** can only appear in a namespace enclosing the previous declaration. In such cases, nested-name-specifier cannot begin with a decltype specifier. | (since C++11) | |
| enum-base | - | (since C++11) colon (`:`), followed by a type-specifier-seq that names an integral type (if it is cv-qualified, qualifications are ignored) that will serve as the fixed underlying type for this enumeration type |
| enumerator-list | - | comma-separated list of enumerator definitions, each of which is either simply a unique identifier, which becomes the name of the enumerator, or a unique identifier with a constant expression: identifier `=` constant-expression. In either case, the identifier can be directly followed by an optional attribute specifier sequence.(since C++17) |

There are two distinct kinds of enumerations: **unscoped enumeration** (declared with the enum-key `enum`) and **scoped enumeration** (declared with the enum-key `enum class` or `enum struct`).

### Unscoped enumerations

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `enum` name ﻿(optional) `{` enumerator `=` constant-expression `,` enumerator `=` constant-expression `,` ... `}` | (1) |  |
|  | | | | | | | | | |
| `enum` name ﻿(optional) `:` type `{` enumerator `=` constant-expression `,` enumerator `=` constant-expression `,` ... `}` | (2) | (since C++11) |
|  | | | | | | | | | |
| `enum` name `:` type `;` | (3) | (since C++11) |
|  | | | | | | | | | |

1) Declares an unscoped enumeration type whose underlying type is not fixed (in this case, the underlying type is an implementation-defined integral type that can represent all enumerator values; this type is not larger than int unless the value of an enumerator cannot fit in an int or unsigned int. If the enumerator-list is empty, the underlying type is as if the enumeration had a single enumerator with value ​0​. If no integral type can represent all the enumerator values, the enumeration is ill-formed).2) Declares an unscoped enumeration type whose underlying type is fixed.3) Opaque enum declaration for an unscoped enumeration must specify the name and the underlying type.

Each enumerator becomes a named constant of the enumeration's type (that is, name), visible in the enclosing scope, and can be used whenever constants are required.

```
enum Color { red, green, blue };
Color r = red;
 
switch(r)
{
    case red  : std::cout << "red\n";   break;
    case green: std::cout << "green\n"; break;
    case blue : std::cout << "blue\n";  break;
}

```

Each enumerator is associated with a value of the underlying type. When `=` are provided in an enumerator-list, the values of enumerators are defined by those associated constant-expressions. If the first enumerator does not have `=`, the associated value is zero. For any other enumerator whose definition does not have an `=`, the associated value is the value of the previous enumerator plus one.

```
enum Foo { a, b, c = 10, d, e = 1, f, g = f + c };
//a = 0, b = 1, c = 10, d = 11, e = 1, f = 2, g = 12

```

The name of an unscoped enumeration may be omitted: such declaration only introduces the enumerators into the enclosing scope:

```
enum { a, b, c = 0, d = a + 2 }; // defines a = 0, b = 1, c = 0, d = 2

```

When an unscoped enumeration is a class member, its enumerators may be accessed using class member access operators `.` and `->`:

```
struct X
{
    enum direction { left = 'l', right = 'r' };
};
X x;
X* p = &x;
 
int a = X::direction::left; // allowed only in C++11 and later
int b = X::left;
int c = x.left;
int d = p->left;

```

|  |  |
| --- | --- |
| In the declaration specifiers of a member declaration, the sequence  `enum` enum-head-name `:`  is always parsed as a part of enumeration declaration:   ```text struct S {     enum E1 : int {};     enum E1 : int {}; // error: redeclaration of enumeration,                       // NOT parsed as a zero-length bit-field of type enum E1 };   enum E2 { e1 };   void f() {     false ? new enum E2 : int(); // OK: 'int' is NOT parsed as the underlying type } ``` | (since C++11) |

#### Enumeration name for linkage purposes

An unnamed enumeration that does not have a typedef name for linkage purposes and that has an enumerator is denoted, for linkage purposes, by its underlying type and its first enumerator; such an enumeration is said to have an enumerator as a **name for linkage purposes**.

### Scoped enumerations

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | |  | | | | | | | | | | | `enum struct|class` name `{` enumerator `=` constant-expression `,` enumerator `=` constant-expression `,` ... `}` | (1) |  | |  | | | | | | | | | | | `enum struct|class` name `:` type `{` enumerator `=` constant-expression `,` enumerator `=` constant-expression `,` ... `}` | (2) |  | |  | | | | | | | | | | | `enum struct|class` name `;` | (3) |  | |  | | | | | | | | | | | `enum struct|class` name `:` type `;` | (4) |  | |  | | | | | | | | | |  1) declares a scoped enumeration type whose underlying type is int (the keywords class and struct are exactly equivalent)2) declares a scoped enumeration type whose underlying type is type3) opaque enum declaration for a scoped enumeration whose underlying type is int4) opaque enum declaration for a scoped enumeration whose underlying type is type Each enumerator becomes a named constant of the enumeration's type (that is, name), which is contained within the scope of the enumeration, and can be accessed using scope resolution operator. There are no implicit conversions from the values of a scoped enumerator to integral types, although `static_cast` may be used to obtain the numeric value of the enumerator. Run this code  ```text #include <iostream>   int main() {     enum class Color { red, green = 20, blue };     Color r = Color::blue;       switch(r)     {         case Color::red  : std::cout << "red\n";   break;         case Color::green: std::cout << "green\n"; break;         case Color::blue : std::cout << "blue\n";  break;     }       // int n = r; // error: no implicit conversion from scoped enum to int     int n = static_cast<int>(r); // OK, n = 21     std::cout << n << '\n'; // prints 21 } ``` | (since C++11) |

|  |  |
| --- | --- |
| An enumeration can be initialized from an integer without a cast, using list initialization, if all of the following are true:   - The initialization is direct-list-initialization. - The initializer list has only a single element. - The enumeration is either scoped or unscoped with underlying type fixed. - The conversion is non-narrowing.   This makes it possible to introduce new integer types (e.g. `SafeInt`) that enjoy the same existing calling conventions as their underlying integer types, even on ABIs that penalize passing/returning structures by value.   ```text enum byte : unsigned char {}; // byte is a new integer type; see also std::byte (C++17) byte b{42};        // OK as of C++17 (direct-list-initialization) byte c = {42};     // error byte d = byte{42}; // OK as of C++17; same value as b byte e{-1};        // error   struct A { byte b; }; A a1 = {{42}};     // error (copy-list-initialization of a constructor parameter) A a2 = {byte{42}}; // OK as of C++17   void f(byte); f({42}); // error (copy-list-initialization of a function parameter)   enum class Handle : std::uint32_t { Invalid = 0 }; Handle h{42}; // OK as of C++17 ``` | (since C++17) |

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| using enum declaration  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | |  | | | | | | | | | | | `using enum` using-enum-declarator `;` |  | (since C++20) | |  | | | | | | | | | |  |  |  |  | | --- | --- | --- | | declarator | - | a (possibly qualified) identifier or simple template identifiers |   declarator must name a non-dependent enumeration type. The enumeration declarations are found by type-only ordinary qualified or unqualified lookup, depending on whether declarator is qualified.   ```text enum E { x };   void f() {     int E;     using enum E; // OK }   using F = E; using enum F; // OK   template<class T> using EE = T;   void g() {     using enum EE<E>; // OK } ```   A using enum declaration introduces the enumerator names of the named enumeration as if by a using declaration for each enumerator. When in class scope, a using enum declaration adds the enumerators of the named enumeration as members to the scope, making them accessible for member lookup.   ```text enum class fruit { orange, apple };   struct S {     using enum fruit; // OK: introduces orange and apple into S };   void f() {     S s;     s.orange;  // OK: names fruit::orange     S::orange; // OK: names fruit::orange } ```   Two using enum declarations that introduce two enumerators of the same name conflict.   ```text enum class fruit { orange, apple }; enum class color { red, orange };   void f() {     using enum fruit;    // OK     // using enum color; // error: color::orange and fruit::orange conflict } ``` | (since C++20) |

### Notes

Values of unscoped enumeration type can be promoted or converted to integral types:

```
enum color { red, yellow, green = 20, blue };
color col = red;
int n = blue; // n == 21

```

Values of integer, floating-point, and enumeration types can be converted to any enumeration type by using `static_cast`. Note that the value after such conversion may not necessarily equal any of the named enumerators defined for the enumeration:

```
enum access_t { read = 1, write = 2, exec = 4 }; // enumerators: 1, 2, 4 range: 0..7
access_t rwe = static_cast<access_t>(7);
assert((rwe & read) && (rwe & write) && (rwe & exec));
 
access_t x = static_cast<access_t>(8.0); // undefined behavior since CWG 1766
access_t y = static_cast<access_t>(8);   // undefined behavior since CWG 1766
 
enum foo { a = 0, b = UINT_MAX }; // range: [0, UINT_MAX]
foo x = foo(-1); // undefined behavior since CWG 1766,
                 // even if foo's underlying type is unsigned int

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_enumerator_attributes` | `201411L` | (C++17) | Attributes for enumerators |
| `__cpp_using_enum` | `201907L` | (C++20) | `using enum` |

### Keywords

enum,
struct,
class,
using

### Example

Run this code

```
#include <cstdint>
#include <iostream>
 
// enum that takes 16 bits
enum smallenum: std::int16_t
{
    a,
    b,
    c
};
 
// color may be red (value 0), yellow (value 1), green (value 20), or blue (value 21)
enum color
{
    red,
    yellow,
    green = 20,
    blue
};
 
// altitude may be altitude::high or altitude::low
enum class altitude: char
{
    high = 'h',
    low = 'l', // trailing comma only allowed after CWG 518
}; 
 
// the constant d is 0, the constant e is 1, the constant f is 3
enum
{
    d,
    e,
    f = e + 2
};
 
// enumeration types (both scoped and unscoped) can have overloaded operators
std::ostream& operator<<(std::ostream& os, color c)
{
    switch(c)
    {
        case red   : os << "red";    break;
        case yellow: os << "yellow"; break;
        case green : os << "green";  break;
        case blue  : os << "blue";   break;
        default    : os.setstate(std::ios_base::failbit);
    }
    return os;
}
 
std::ostream& operator<<(std::ostream& os, altitude al)
{
    return os << static_cast<char>(al);
}
 
// The scoped enum (C++11) can be partially emulated in earlier C++ revisions:
 
enum struct E11 { x, y }; // since C++11
 
struct E98 { enum { x, y }; }; // OK in pre-C++11
 
namespace N98 { enum { x, y }; } // OK in pre-C++11
 
struct S98 { static const int x = 0, y = 1; }; // OK in pre-C++11
 
void emu()
{
    std::cout << (static_cast<int>(E11::y) + E98::y + N98::y + S98::y) << '\n'; // 4
}
 
namespace cxx20
{
    enum class long_long_long_name { x, y };
 
    void using_enum_demo()
    {
        std::cout << "C++20 `using enum`: __cpp_using_enum == ";
        switch (auto rnd = []{return long_long_long_name::x;}; rnd())
        {
#if defined(__cpp_using_enum)
            using enum long_long_long_name;
            case x: std::cout << __cpp_using_enum << "; x\n"; break;
            case y: std::cout << __cpp_using_enum << "; y\n"; break;
#else
            case long_long_long_name::x: std::cout << "?; x\n"; break;
            case long_long_long_name::y: std::cout << "?; y\n"; break;
#endif
        }
    }
}
 
int main()
{
    color col = red;
    altitude a;
    a = altitude::low;
 
    std::cout << "col = " << col << '\n'
              << "a = "   << a   << '\n'
              << "f = "   << f   << '\n';
 
    cxx20::using_enum_demo();
}

```

Possible output:

```
col = red
a = l
f = 3
C++20 `using enum`: __cpp_using_enum == 201907; x

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 377 | C++98 | the behavior was unspecified when no integral type can represent all the enumerator values | the enumeration is ill- formed in this case |
| CWG 518 | C++98 | a trailing comma was not allowed after the enumerator list | allowed |
| CWG 1514 | C++11 | a redefinition of enumeration with fixed underlying type could be parsed as a bit-field in a class member declaration | always parsed as a redefinition |
| CWG 1638 | C++11 | grammar of opaque enumeration declaration prohibited use for template specializations | nested-name-specifier permitted |
| CWG 1766 | C++98 | casting an out-of-range value to an enumeration without fixed underlying type had an unspecified result | the behavior is undefined |
| CWG 1966 | C++11 | the resolution of CWG issue 1514 made the `:` of a conditional expression part of enum-base | only apply the resolution to member declaration specifiers |
| CWG 2156 | C++11 | enum definitions could define enumeration types by using-declarations | prohibited |
| CWG 2157 | C++11 | the resolution of CWG issue 1966 did not cover qualified enumeration names | covered |
| CWG 2530 | C++98 | an enumerator list could contain multiple enumerators with the same identifier | prohibited |
| CWG 2590 | C++98 | the size, value representation and alignment requirements of an enumeration did not depend on its underlying type | all of them are identical to those of the underlying type |
| CWG 2621 | C++20 | the enumeration name lookup used in using enum declarations was unclear | made clear |
| CWG 2877 | C++20 | the enumeration name lookup used in using enum declarations was not type-only | made type-only |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 9.7.1 Enumeration declarations [dcl.enum]

- C++20 standard (ISO/IEC 14882:2020):

:   - 9.7.1 Enumeration declarations [dcl.enum]

- C++17 standard (ISO/IEC 14882:2017):

:   - 10.2 Enumeration declarations [dcl.enum]

- C++14 standard (ISO/IEC 14882:2014):

:   - 7.2 Enumeration declarations [dcl.enum]

- C++11 standard (ISO/IEC 14882:2011):

:   - 7.2 Enumeration declarations [dcl.enum]

- C++03 standard (ISO/IEC 14882:2003):

:   - 7.2 Enumeration declarations [dcl.enum]

- C++98 standard (ISO/IEC 14882:1998):

:   - 7.2 Enumeration declarations [dcl.enum]

### See also

|  |  |
| --- | --- |
| is_enum(C++11) | checks if a type is an enumeration type   (class template) |
| is_scoped_enum(C++23) | checks if a type is a scoped enumeration type   (class template) |
| underlying_type(C++11) | obtains the underlying integer type for a given enumeration type   (class template) |
| to_underlying(C++23) | converts an enumeration to its underlying type   (function template) |
| C documentation for Enumerations | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/enum&oldid=175215>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 August 2024, at 17:12.