# Copy elision

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

 Initialization

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Initializer | | | | |
| Default initialization | | | | |
| Value initialization | | | | |
| Direct initialization | | | | |
| Copy-initialization | | | | |
| List initialization (C++11) | | | | |
| Aggregate initialization | | | | |
| Reference initialization | | | | |
| ****Copy elision**** | | | | |
| Static initialization | | | | |
| Zero initialization | | | | |
| Constant initialization | | | | |
| Dynamic non-local initialization | | | | |
| Ordered dynamic initialization | | | | |
| Unordered dynamic initialization | | | | |
| Class member initialization | | | | |
| Member initializer list | | | | |
| Default member initializer (C++11) | | | | |

When certain criteria are met, the creation of a class object from a source object of the same type (ignoring cv-qualification) can be omitted, even if the selected constructor and/or the destructor for the object have side effects. This elision of object creation is called **copy elision** ﻿.

### Explanation

Copy elision is permitted in the following circumstances (which may be combined to eliminate multiple copies):

- In a return statement in a function with a class return type, when the operand is the name of a non-volatile object obj with automatic storage duration (other than a function parameter or a handler parameter), the copy-initialization of the result object can be omitted by constructing obj directly into the function call’s result object. This variant of copy elision is known as **named return value optimization** (NRVO).

|  |  |
| --- | --- |
| - When a class object target is copy-initialized with a temporary class object obj that has not been bound to a reference, the copy-initialization can be omitted by constructing obj directly into target. This variant of copy elision is known as **unnamed return value optimization** (URVO). Since C++17, URVO is mandatory and no longer considered a form of copy elision; see below. | (until C++17) |
| - In a throw expression, when the operand is the name of a non-volatile object obj with automatic storage duration (other than a function parameter or a handler parameter) that belongs to a scope that does not contain the innermost enclosing try block (if exists), the copy-initialization of the exception object can be omitted by constructing obj directly into the exception object. - In a handler, the copy-initialization of the handler argument can be omitted by treating the handler parameter as an alias for the exception object if the meaning of the program will be unchanged except for the execution of constructors and destructors for the handler argument. | (since C++11) |
| - In coroutines, a copy of a coroutine parameter can be omitted. In this case, references to that copy are replaced with references to the corresponding parameter if the meaning of the program will be unchanged except for the execution of a constructor and destructor for the parameter copy object. | (since C++20) |

When copy elision occurs, the implementation treats the source and target of the omitted initialization as simply two different ways of referring to the same object.

|  |  |
| --- | --- |
| The destruction occurs at the later of the times when the two objects would have been destroyed without the optimization. | (until C++11) |
| If the first parameter of the selected constructor is an rvalue reference to the object’s type, the destruction of that object occurs when the target would have been destroyed. Otherwise, the destruction occurs at the later of the times when the two objects would have been destroyed without the optimization. | (since C++11) |

|  |  |
| --- | --- |
| Prvalue semantics ("guaranteed copy elision") Since C++17, a prvalue is not materialized until needed, and then it is constructed directly into the storage of its final destination. This sometimes means that even when the language syntax visually suggests a copy/move (e.g. copy initialization), no copy/move is performed — which means the type need not have an accessible copy/move constructor at all. Examples include:   - Initializing the returned object in a return statement, when the operand is a prvalue of the same class type (ignoring cv-qualification) as the function return type:  ```text T f() {     return U(); // constructs a temporary of type U,                 // then initializes the returned T from the temporary } T g() {     return T(); // constructs the returned T directly; no move } ```   The destructor of the type returned must be accessible at the point of the return statement and non-deleted, even though no T object is destroyed.   - In the initialization of an object, when the initializer expression is a prvalue of the same class type (ignoring cv-qualification) as the variable type:  ```text T x = T(T(f())); // x is initialized by the result of f() directly; no move ```   This can only apply when the object being initialized is known not to be a potentially-overlapping subobject:   ```text struct C { /* ... */ }; C f();   struct D; D g();   struct D : C {     D() : C(f()) {}    // no elision when initializing a base class subobject     D(int) : D(g()) {} // no elision because the D object being initialized might                        // be a base-class subobject of some other class }; ```   Note: This rule does not specify an optimization, and the Standard does not formally describe it as "copy elision" (because nothing is being elided). Instead, the C++17 core language specification of prvalues and temporaries is fundamentally different from that of earlier C++ revisions: there is no longer a temporary to copy/move from. Another way to describe C++17 mechanics is "unmaterialized value passing" or "deferred temporary materialization": prvalues are returned and used without ever materializing a temporary. | (since C++17) |

### Notes

Copy elision is the only allowed form of optimization(until C++14) one of the two allowed forms of optimization, alongside allocation elision and extension,(since C++14) that can change observable side-effects. Because some compilers do not perform copy elision in every situation where it is allowed (e.g., in debug mode), programs that rely on the side-effects of copy/move constructors and destructors are not portable.

|  |  |
| --- | --- |
| In a return statement or a throw expression, if the compiler cannot perform copy elision but the conditions for copy elision are met, or would be met except that the source is a function parameter, the compiler will attempt to use the move constructor even if the source operand is designated by an lvalue(until C++23) the source operand will be treated as an rvalue(since C++23); see return statement for details.  In constant expression and constant initialization, copy elision is never performed.   ```text struct A {     void* p;     constexpr A() : p(this) {}     A(const A&); // Disable trivial copyability };   constexpr A a;  // OK: a.p points to a   constexpr A f() {     A x;     return x; } constexpr A b = f(); // error: b.p would be dangling and point to the x inside f   constexpr A c = A(); // (until C++17) error: c.p would be dangling and point to a temporary                      // (since C++17) OK: c.p points to c; no temporary is involved ``` | (since C++11) |

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_guaranteed_copy_elision` | `201606L` | (C++17) | Guaranteed copy elision through simplified value categories |

### Example

Run this code

```
#include <iostream>
 
struct Noisy
{
    Noisy() { std::cout << "constructed at " << this << '\n'; }
    Noisy(const Noisy&) { std::cout << "copy-constructed\n"; }
    Noisy(Noisy&&) { std::cout << "move-constructed\n"; }
    ~Noisy() { std::cout << "destructed at " << this << '\n'; }
};
 
Noisy f()
{
    Noisy v = Noisy(); // (until C++17) copy elision initializing v from a temporary;
                       //               the move constructor may be called
                       // (since C++17) "guaranteed copy elision"
    return v; // copy elision ("NRVO") from v to the result object;
              // the move constructor may be called
}
 
void g(Noisy arg)
{
    std::cout << "&arg = " << &arg << '\n';
}
 
int main()
{
    Noisy v = f(); // (until C++17) copy elision initializing v from the result of f()
                   // (since C++17) "guaranteed copy elision"
 
    std::cout << "&v = " << &v << '\n';
 
    g(f()); // (until C++17) copy elision initializing arg from the result of f()
            // (since C++17) "guaranteed copy elision"
}

```

Possible output:

```
constructed at 0x7fffd635fd4e
&v = 0x7fffd635fd4e
constructed at 0x7fffd635fd4f
&arg = 0x7fffd635fd4f
destructed at 0x7fffd635fd4f
destructed at 0x7fffd635fd4e

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1967 | C++11 | when copy elision is done using a move constructor, the lifetime of the moved-from object was still considered | not considered |
| CWG 2426 | C++17 | destructor was not required when returning a prvalue | destructor is potentially invoked |
| CWG 2930 | C++98 | only copy(/move) operations could be elided, but a non-copy(/move) constructor can be selected by copy-initialization | elides any object construction of related copy-initializations |

### See also

- copy initialization
- copy constructor
- move constructor
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/copy_elision&oldid=180173>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 February 2025, at 01:13.