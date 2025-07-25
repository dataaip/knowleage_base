# Pointer declaration

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Overview | | | | | | Declaration syntax | | | | | | **decl-specifier-seq** | | | | | | Declarator | | | | | | Conflicting declarations | | | | | | Specifiers | | | | | | typedef | | | | | | inline | | | | | | virtual function specifier | | | | | | explicit function specifier | | | | | | friend | | | | | | constexpr(C++11) | | | | | | consteval(C++20) | | | | | | constinit(C++20) | | | | | | Storage class specifiers | | | | | | Translation-unit-local (C++20) | | | | | | class/struct | | | | | | union | | | | | | enum | | | | | | decltype(C++11) | | | | | | auto(C++11) | | | | | | alignas(C++11) | | | | | | constvolatile | | | | | | Pack indexing specifier (C++26) | | | | | | Elaborated type specifier | | | | | | Attributes (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Declarators | | | | | | Reference | | | | | | ****Pointer**** | | | | | | Array | | | | | | Block declarations | | | | | | Simple-declaration | | | | | | →Structured binding declaration (C++17) | | | | | | Alias declaration (C++11) | | | | | | Namespace alias definition | | | | | | using declaration | | | | | | `using` directive | | | | | | static_assert declaration (C++11) | | | | | | asm declaration | | | | | | Opaque enum declaration (C++11) | | | | | | Other declarations | | | | | | Namespace definition | | | | | | Function declaration | | | | | | Class template declaration | | | | | | Function template declaration | | | | | | Explicit template instantiation (C++11) | | | | | | Explicit template specialization | | | | | | Linkage specification | | | | | | Attribute declaration (C++11) | | | | | | Empty declaration | | | | | |  | | | | | |

Declares a variable of a pointer or pointer-to-member type.

### Syntax

A pointer declaration is any simple declaration whose declarator has the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `*` attr ﻿(optional) cv ﻿(optional) declarator | (1) |  |
|  | | | | | | | | | |
| nested-name-specifier `*` attr ﻿(optional) cv ﻿(optional) declarator | (2) |  |
|  | | | | | | | | | |

1) ****Pointer declarator****: the declaration S\* D; declares D as a pointer to the type determined by the declaration specifier sequence `S`.2) ****Pointer to member declarator****: the declaration S C::\* D; declares D as a pointer to non-static member of `C` of type determined by the declaration specifier sequence `S`.

|  |  |  |
| --- | --- | --- |
| nested-name-specifier | - | a sequence of names and scope resolution operators `::` |
| attr | - | (since C++11) a list of attributes |
| cv | - | const/volatile qualification which apply to the pointer that is being declared (not to the pointed-to type, whose qualifications are part of declaration specifier sequence) |
| declarator | - | any declarator other than a reference declarator (there are no pointers to references). It can be another pointer declarator (pointer to pointers are allowed) |

There are no pointers to references and there are no pointers to bit-fields.
Typically, mentions of "pointers" without elaboration do not include pointers to (non-static) members.

### Pointers

Every value of pointer type is one of the following:

- a **pointer to an object or function** (in which case the pointer is said to **point to** the object or function), or
- a **pointer past the end of an object**, or
- the **null pointer value** for that type, or
- an **invalid pointer value**.

A pointer that points to an object **represents the address** of the first byte in memory occupied by the object. A pointer past the end of an object **represents the address** of the first byte in memory after the end of the storage occupied by the object.

Note that two pointers that represent the same address may nonetheless have different values.

```
struct C
{
    int x, y;
} c;
 
int* px = &c.x;   // value of px is "pointer to c.x"
int* pxe= px + 1; // value of pxe is "pointer past the end of c.x"
int* py = &c.y;   // value of py is "pointer to c.y"
 
assert(pxe == py); // == tests if two pointers represent the same address
                   // may or may not fire
 
*pxe = 1; // undefined behavior even if the assertion does not fire

```

Indirection through an invalid pointer value and passing an invalid pointer value to a deallocation function have undefined behavior. Any other use of an invalid pointer value has implementation-defined behavior. Some implementations might define that copying an invalid pointer value causes a system-generated runtime fault.

#### Pointers to objects

A pointer to object can be initialized with the return value of the address-of operator applied to any expression of object type, including another pointer type:

```
int n;
int* np = &n;          // pointer to int
int* const* npp = &np; // non-const pointer to const pointer to non-const int
 
int a[2];
int (*ap)[2] = &a;     // pointer to array of int
 
struct S { int n; };
 
S s = {1};
int* sp = &s.n;        // pointer to the int that is a member of s

```

Pointers may appear as operands to the built-in indirection operator (unary operator\*), which returns the lvalue expression identifying the pointed-to object:

```
int n;
int* p = &n;     // pointer to n
int& r = *p;     // reference is bound to the lvalue expression that identifies n
r = 7;           // stores the int 7 in n
std::cout << *p; // lvalue-to-rvalue implicit conversion reads the value from n

```

Pointers to class objects may also appear as the left-hand operands of the member access operators `operator->` and `operator->*`.

Because of the array-to-pointer implicit conversion, pointer to the first element of an array can be initialized with an expression of array type:

```
int a[2];
int* p1 = a; // pointer to the first element a[0] (an int) of the array a
 
int b[6][3][8];
int (*p2)[3][8] = b; // pointer to the first element b[0] of the array b,
                     // which is an array of 3 arrays of 8 ints

```

Because of the derived-to-base implicit conversion for pointers, pointer to a base class can be initialized with the address of a derived class:

```
struct Base {};
struct Derived : Base {};
 
Derived d;
Base* p = &d;

```

If `Derived` is polymorphic, such a pointer may be used to make virtual function calls.

Certain addition, subtraction, increment, and decrement operators are defined for pointers to elements of arrays: such pointers satisfy the LegacyRandomAccessIterator requirements and allow the C++ library algorithms to work with raw arrays.

Comparison operators are defined for pointers to objects in some situations: two pointers that represent the same address compare equal, two null pointer values compare equal, pointers to elements of the same array compare the same as the array indices of those elements, and pointers to non-static data members with the same member access compare in order of declaration of those members.

Many implementations also provide strict total ordering of pointers of random origin, e.g. if they are implemented as addresses within continuous virtual address space. Those implementations that do not (e.g. where not all bits of the pointer are part of a memory address and have to be ignored for comparison, or an additional calculation is required or otherwise pointer and integer is not a 1 to 1 relationship), provide a specialization of std::less for pointers that has that guarantee. This makes it possible to use all pointers of random origin as keys in standard associative containers such as std::set or std::map.

#### Pointers to void

Pointer to object of any type can be implicitly converted to pointer to (possibly cv-qualified) void; the pointer value is unchanged. The reverse conversion, which requires `static_cast` or explicit cast, yields the original pointer value:

```
int n = 1;
int* p1 = &n;
void* pv = p1;
int* p2 = static_cast<int*>(pv);
std::cout << *p2 << '\n'; // prints 1

```

If the original pointer is pointing to a base class subobject within an object of some polymorphic type, `dynamic_cast` may be used to obtain a void\* that is pointing at the complete object of the most derived type.

Pointers to void have the same size, representation and alignment as pointers to char.

Pointers to void are used to pass objects of unknown type, which is common in C interfaces: std::malloc returns void\*, std::qsort expects a user-provided callback that accepts two const void\* arguments. `pthread_create` expects a user-provided callback that accepts and returns void\*. In all cases, it is the caller's responsibility to cast the pointer to the correct type before use.

#### Pointers to functions

A pointer to function can be initialized with an address of a non-member function or a static member function. Because of the function-to-pointer implicit conversion, the address-of operator is optional:

```
void f(int);
void (*p1)(int) = &f;
void (*p2)(int) = f; // same as &f

```

Unlike functions or references to functions, pointers to functions are objects and thus can be stored in arrays, copied, assigned, etc.

```
void (a[10])(int);  // Error: array of functions
void (&a[10])(int); // Error: array of references
void (*a[10])(int); // OK: array of pointers to functions

```

Note: declarations involving pointers to functions can often be simplified with type aliases:

```
using F = void(int); // named type alias to simplify declarations
F a[10];  // Error: array of functions
F& a[10]; // Error: array of references
F* a[10]; // OK: array of pointers to functions

```

A pointer to function can be used as the left-hand operand of the function call operator, this invokes the pointed-to function:

```
int f(int n)
{
    std::cout << n << '\n';
    return n * n;
}
 
int main()
{
    int (*p)(int) = f;
    int x = p(7);
}

```

Dereferencing a function pointer yields the lvalue identifying the pointed-to function:

```
int f();
int (*p)() = f;  // pointer p is pointing to f
int (&r)() = *p; // the lvalue that identifies f is bound to a reference
r();             // function f invoked through lvalue reference
(*p)();          // function f invoked through the function lvalue
p();             // function f invoked directly through the pointer

```

A pointer to function may be initialized from an overload set which may include functions, function template specializations, and function templates, if only one overload matches the type of the pointer (see address of an overloaded function for more detail):

```
template<typename T>
T f(T n) { return n; }
 
double f(double n) { return n; }
 
int main()
{
    int (*p)(int) = f; // instantiates and selects f<int>
}

```

Equality comparison operators are defined for pointers to functions (they compare equal if pointing to the same function).

### Pointers to members

#### Pointers to data members

A pointer to non-static member object `m` which is a member of class `C` can be initialized with the expression &C::m exactly. Expressions such as &(C::m) or &m inside `C`'s member function do not form pointers to members.

Such a pointer may be used as the right-hand operand of the pointer-to-member access operators operator.\* and operator->\*:

```
struct C { int m; };
 
int main()
{
    int C::* p = &C::m;          // pointer to data member m of class C
    C c = {7};
    std::cout << c.*p << '\n';   // prints 7
    C* cp = &c;
    cp->m = 10;
    std::cout << cp->*p << '\n'; // prints 10
}

```

Pointer to data member of an accessible unambiguous non-virtual base class can be implicitly converted to pointer to the same data member of a derived class:

```
struct Base { int m; };
struct Derived : Base {};
 
int main()
{
    int Base::* bp = &Base::m;
    int Derived::* dp = bp;
    Derived d;
    d.m = 1;
    std::cout << d.*dp << ' ' << d.*bp << '\n'; // prints 1 1
}

```

Conversion in the opposite direction, from a pointer to data member of a derived class to a pointer to data member of an unambiguous non-virtual base class, is allowed with `static_cast` and explicit cast, even if the base class does not have that member (but the most-derived class does, when the pointer is used for access):

```
struct Base {};
struct Derived : Base { int m; };
 
int main()
{
    int Derived::* dp = &Derived::m;
    int Base::* bp = static_cast<int Base::*>(dp);
 
    Derived d;
    d.m = 7;
    std::cout << d.*bp << '\n'; // okay: prints 7
 
    Base b;
    std::cout << b.*bp << '\n'; // undefined behavior
}

```

The pointed-to type of a pointer-to-member may be a pointer-to-member itself: pointers to members can be multilevel, and can be cv-qualified differently at every level. Mixed multi-level combinations of pointers and pointers-to-members are also allowed:

```
struct A
{
    int m;
    // const pointer to non-const member
    int A::* const p;
};
 
int main()
{
    // non-const pointer to data member which is a const pointer to non-const member
    int A::* const A::* p1 = &A::p;
 
    const A a = {1, &A::m};
    std::cout << a.*(a.*p1) << '\n'; // prints 1
 
    // regular non-const pointer to a const pointer-to-member
    int A::* const* p2 = &a.p;
    std::cout << a.**p2 << '\n'; // prints 1
}

```

#### Pointers to member functions

A pointer to non-static member function f which is a member of class `C` can be initialized with the expression &C::f exactly. Expressions such as &(C::f) or &f inside `C`'s member function do not form pointers to member functions.

Such a pointer may be used as the right-hand operand of the pointer-to-member access operators operator.\* and operator->\*. The resulting expression can be used only as the left-hand operand of a function-call operator:

```
struct C
{
    void f(int n) { std::cout << n << '\n'; }
};
 
int main()
{
    void (C::* p)(int) = &C::f; // pointer to member function f of class C
    C c;
    (c.*p)(1);                  // prints 1
    C* cp = &c;
    (cp->*p)(2);                // prints 2
}

```

Pointer to member function of a base class can be implicitly converted to pointer to the same member function of a derived class:

```
struct Base
{
    void f(int n) { std::cout << n << '\n'; }
};
struct Derived : Base {};
 
int main()
{
    void (Base::* bp)(int) = &Base::f;
    void (Derived::* dp)(int) = bp;
    Derived d;
    (d.*dp)(1);
    (d.*bp)(2);
}

```

Conversion in the opposite direction, from a pointer to member function of a derived class to a pointer to member function of an unambiguous non-virtual base class, is allowed with `static_cast` and explicit cast, even if the base class does not have that member function (but the most-derived class does, when the pointer is used for access):

```
struct Base {};
struct Derived : Base
{
    void f(int n) { std::cout << n << '\n'; }
};
 
int main()
{
    void (Derived::* dp)(int) = &Derived::f;
    void (Base::* bp)(int) = static_cast<void (Base::*)(int)>(dp);
 
    Derived d;
    (d.*bp)(1); // okay: prints 1
 
    Base b;
    (b.*bp)(2); // undefined behavior
}

```

Pointers to member functions may be used as callbacks or as function objects, often after applying std::mem_fn or std::bind:

Run this code

```
#include <algorithm>
#include <cstddef>
#include <functional>
#include <iostream>
#include <string>
 
int main()
{
    std::vector<std::string> v = {"a", "ab", "abc"};
    std::vector<std::size_t> l;
    transform(v.begin(), v.end(), std::back_inserter(l),
              std::mem_fn(&std::string::size));
    for (std::size_t n : l)
        std::cout << n << ' ';
    std::cout << '\n';
}

```

Output:

```
1 2 3

```

### Null pointers

Pointers of every type have a special value known as **null pointer value** of that type. A pointer whose value is null does not point to an object or a function (the behavior of dereferencing a null pointer is undefined), and compares equal to all pointers of the same type whose value is also **null**.

A **null pointer constant** can be used to initialize a pointer to null or to assign the null value to an existing pointer, it is one of the following values:

- An integer literal with value zero.

|  |  |
| --- | --- |
| - A prvalue of type std::nullptr_t (usually nullptr). | (since C++11) |

The macro NULL can also be used, it expands to an implementation-defined null pointer constant.

Zero-initialization and value-initialization also initialize pointers to their null values.

Null pointers can be used to indicate the absence of an object (e.g. std::function::target()), or as other error condition indicators (e.g. dynamic_cast). In general, a function that receives a pointer argument almost always needs to check if the value is null and handle that case differently (for example, the delete expression does nothing when a null pointer is passed).

### Invalid pointers

A pointer value p is **valid in the context of** an evaluation e if one of the following condition is satisfied:

- p is a null pointer value.
- p is a pointer to function.
- p it is a pointer to or past the end of an object o, and e is in the duration of the region of storage for o.

If a pointer value p is used in an evaluation e, and p is not valid in the context of e, then:

- If e is an indirection or an invocation of a deallocation function, the behavior is undefined.
- Otherwise, the behavior is implementation-defined.

```
int* f()
{
    int obj;
    int* local_ptr = new (&obj) int;
 
    *local_ptr = 1; // OK, the evaluation “*local_ptr” is
                    // in the storage duration of “obj”
 
    return local_ptr;
}
 
int* ptr = f();  // the storage duration of “obj” is expired,
                 // therefore “ptr” is an invalid pointer in the following contexts
 
int* copy = ptr; // implementation-defined behavior
*ptr = 2;        // undefined behavior: indirection of an invalid pointer
delete ptr;      // undefined behavior: deallocating storage from an invalid pointer

```

### Constness

- If cv appears before `*` in the pointer declaration, it is part of the declaration specifier sequence and applies to the pointed-to object.
- If cv appears after `*` in the pointer declaration, it is part of the declarator and applies to the pointer that's being declared.

| Syntax | meaning |
| --- | --- |
| const T\* | pointer to constant object |
| T const\* | pointer to constant object |
| T\* const | constant pointer to object |
| const T\* const | constant pointer to constant object |
| T const\* const | constant pointer to constant object |

```
// pc is a non-const pointer to const int
// cpc is a const pointer to const int
// ppc is a non-const pointer to non-const pointer to const int
const int ci = 10, *pc = &ci, *const cpc = pc, **ppc;
// p is a non-const pointer to non-const int
// cp is a const pointer to non-const int
int i, *p, *const cp = &i;
 
i = ci;    // okay: value of const int copied into non-const int
*cp = ci;  // okay: non-const int (pointed-to by const pointer) can be changed
pc++;      // okay: non-const pointer (to const int) can be changed
pc = cpc;  // okay: non-const pointer (to const int) can be changed
pc = p;    // okay: non-const pointer (to const int) can be changed
ppc = &pc; // okay: address of pointer to const int is pointer to pointer to const int
 
ci = 1;    // error: const int cannot be changed
ci++;      // error: const int cannot be changed
*pc = 2;   // error: pointed-to const int cannot be changed
cp = &ci;  // error: const pointer (to non-const int) cannot be changed
cpc++;     // error: const pointer (to const int) cannot be changed
p = pc;    // error: pointer to non-const int cannot point to const int
ppc = &p;  // error: pointer to pointer to const int cannot point to
           // pointer to non-const int

```

In general, implicit conversion from one multi-level pointer to another follows the rules described in qualification conversions.

### Composite pointer type

When an operand of a comparison operator or any of the second and third operands of a conditional operator is a pointer or pointer-to-member, a composite pointer type is determined to be the common type of these operands.

Given two operands p1 and p2 having types `T1` and `T2`, respectively, p1 and p2 can only have a composite pointer type if any of the following conditions are satisfied:

|  |  |  |  |
| --- | --- | --- | --- |
| - p1 and p2 are both pointers. - One of p1 and p2 is a pointer and the other operand is a null pointer constant.  |  |  | | --- | --- | | - p1 and p2 are both null pointer constants, and at least one of `T1` and `T2` is a non-integral type. | (since C++11) | | (until C++14) |
| - At least one of `T1` and `T2` is a pointer type, pointer-to-member type or std::nullptr_t. | (since C++14) |

The **composite pointer type** `C` of p1 and p2 is determined as follows:

|  |  |
| --- | --- |
| - If p1 is a null pointer constant, `C` is `T2`. - Otherwise, if p2 is a null pointer constant, `C` is `T1`. | (until C++11) |
| - If p1 and p2 are both null pointer constants, `C` is std::nullptr_t. - Otherwise, if p1 is a null pointer constant, `C` is `T2`. - Otherwise, if p2 is a null pointer constant, `C` is `T1`. | (since C++11) |

- Otherwise, if all following conditions are satisfied:

:   - `T1` or `T2` is “pointer to **cv1** void”.
    - The other type is “pointer to **cv2** `T`”, where `T` is an object type or void.
:   `C` is “pointer to **cv12** void”, where **cv12** is the union of **cv1** and **cv2**.

|  |  |
| --- | --- |
| - Otherwise, if all following conditions are satisfied:   - `T1` or `T2` is “pointer to function type `F1`”. - The other type is “pointer to noexcept function type `F2`”. - `F1` and `F2` are the same except noexcept.  `C` is “pointer to `F1`”. | (since C++17) |

- Otherwise, if all following conditions are satisfied:

:   - `T1` is “pointer to `C1`”.
    - `T2` is “pointer to `C2`”.
    - One of `C1` and `C2` is reference-related to the other.
:   `C` is

    - the qualification-combined type of `T1` and `T2`, if `C1` is reference-related to `C2`, or
    - the qualification-combined type of `T2` and `T1`, if `C2` is reference-related to `C1`.

|  |  |
| --- | --- |
| - Otherwise, if all following conditions are satisfied:   - `T1` or `T2` is “pointer to member of `C1` of function type `F1`”. - The other type is “pointer to member of `C2` of noexcept function type `F2`”. - One of `C1` and `C2` is reference-related to the other. - `F1` and `F2` are the same except noexcept.  `C` is  - “pointer to member of `C2` of type `F1`”, if `C1` is reference-related to `C2`, or - “pointer to member of `C1` of type `F1`”, if `C2` is reference-related to `C1`. | (since C++17) |

- Otherwise, if all following conditions are satisfied:

:   - `T1` is “pointer to member of `C1` of non-function type `M1`”.
    - `T2` is “pointer to member of `C2` of non-function type `M2`”
    - `M1` and `M2` are the same except top-level cv-qualifications.
    - One of `C1` and `C2` is reference-related to the other.
:   `C` is

    - the qualification-combined type of `T2` and `T1`, if `C1` is reference-related to `C2`, or
    - the qualification-combined type of `T1` and `T2`, if `C2` is reference-related to `C1`.

- Otherwise, if `T1` and `T2` are similar types, `C` is the qualification-combined type of `T1` and `T2`.
- Otherwise, p1 and p2 do not have a composite pointer type, a program that necessitates the determination of `C` such a type is ill-formed.

```
using p = void*;
using q = const int*;
// The determination of the composite pointer type of “p” and “q”
// falls into the [“pointer to cv1 void” and “pointer to cv2 T”] case:
// cv1 = empty, cv2 = const, cv12 = const
// substitute “cv12 = const” into “pointer to cv12 void”:
// the composite pointer type is “const void*”
 
using pi = int**;
using pci = const int**;
// The determination of the composite pointer type of “pi” and “pci”
// falls into the [pointers to similar types “C1” and “C2”] case:
// C1 = int*, C2 = const int*
// they are reference-related types (in both direction) because they are similar
// the composite pointer type is the qualification-combined type
// of “p1” and “pc1” (or that of “pci” and “pi”): “const void* const *”

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 73 | C++98 | a pointer to an object never compares equal to a pointer to one past the end of an array | for non-null and non-function pointers, compare the addresses they represent |
| CWG 903 | C++98 | any integral constant expression that evaluates to 0 was a null pointer constant | limited to integer literals with value 0 |
| CWG 1438 | C++98 | the behavior of using an invalid pointer value in any way was undefined | behaviors other than indirection and passing to deallocation functions are implementation-defined |
| CWG 1512 (N3624) | C++98 | the rule of composite pointer type was incomplete, and thus did not allow comparison between int\*\* and const int\*\* | made complete |
| CWG 2206 | C++98 | a pointer to void and a pointer to function had a composite pointer type | they do not have such a type |
| CWG 2381 | C++17 | function pointer conversions were not allowed when determining the composite pointer type | allowed |
| CWG 2822 | C++98 | reaching the end of the duration of a region of storage could invalidate pointer values | pointer validity is based on the evaluation context |
| CWG 2933 | C++98 | pointers to functions were always invalid | they are always valid |

### See also

|  |  |
| --- | --- |
| C documentation for Pointer declaration | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/pointer&oldid=180197>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 February 2025, at 00:34.