# Constructors and member initializer lists

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | ****Constructors**** | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Access specifiers | | | | | | `friend` specifier | | | | | |  | | | | | |
| Class-specific function properties | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Virtual function | | | | | | `override` specifier (C++11) | | | | | | `final` specifier (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | explicit (C++11) | | | | | | static | | | | | |  | | | | | |
| Special member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default constructor | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | Destructor | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 Classes

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| Overview | | | | |
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
| ****Constructors and member initializer lists**** | | | | |
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

**Constructors** are non-static member functions declared with a special declarator syntax, they are used to initialize objects of their class types.

|  |  |
| --- | --- |
| A constructor cannot be a coroutine. | (since C++20) |

|  |  |
| --- | --- |
| A constructor cannot have an explicit object parameter. | (since C++23) |

### Syntax

Constructors are declared using member function declarators of the following form:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| class-name `(` parameter-list ﻿(optional) `)` except ﻿(optional) attr ﻿(optional) |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| class-name | - | an identifier expression, possibly followed by a list of attributes, and(since C++11) possibly enclosed by a pair parentheses |
| parameter-list | - | parameter list |
| except | - | |  |  | | --- | --- | | dynamic exception specification | (until C++11) | | either dynamic exception specification or noexcept specification | (since C++11) (until C++17) | | noexcept specification | (since C++17) | |
| attr | - | (since C++11) a list of attributes |

The only specifiers allowed in the declaration specifiers of a constructor declaration are `friend`, `inline`, `constexpr`(since C++11), `consteval`(since C++20), and `explicit` (in particular, no return type is allowed). Note that cv- and ref-qualifiers are not allowed either: const and volatile semantics of an object under construction only kick in after the most-derived constructor completes.

The identifier expression of class-name must have one of the following forms:

- In a friend declaration, the identifier expression is a qualified identifier that names a constructor.
- Otherwise, in a member declaration that belongs to the member specification of a class or class template:

:   - For classes, the identifier expression is the injected-class-name of the immediately-enclosing class.
    - For class templates, the identifier expression is a class name that names the current instantiation(until C++20)the injected-class-name(since C++20) of the immediately-enclosing class template.

- Otherwise, the identifier expression is a qualified identifier whose terminal unqualified identifier is the injected-class-name of its lookup context.

### Member initializer list

The body of a function definition of any constructor, before the opening brace of the compound statement, may include the **member initializer list**, whose syntax is the colon character `:`, followed by the comma-separated list of one or more member-initializers, each of which has the following syntax:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| class-or-identifier `(` expression-list ﻿(optional) `)` | (1) |  |
|  | | | | | | | | | |
| class-or-identifier braced-init-list | (2) | (since C++11) |
|  | | | | | | | | | |
| parameter-pack `...` | (3) | (since C++11) |
|  | | | | | | | | | |

1) Initializes the base or member named by class-or-identifier using direct-initialization or, if expression-list is empty, value-initialization2) Initializes the base or member named by class-or-identifier using list-initialization (which becomes value-initialization if the list is empty and aggregate-initialization when initializing an aggregate)3) Initializes multiple bases using a pack expansion

|  |  |  |
| --- | --- | --- |
| class-or-identifier | - | any identifier that names a non-static data member or any type name which names either the class itself (for delegating constructors) or a direct or virtual base. |
| expression-list | - | possibly empty, comma-separated list of the arguments to pass to the constructor of the base or member |
| braced-init-list | - | brace-enclosed initializer list |
| parameter-pack | - | name of a variadic template parameter pack |

Run this code

```
struct S
{
    int n;
 
    S(int);       // constructor declaration
 
    S() : n(7) {} // constructor definition:
                  // ": n(7)" is the initializer list
                  // ": n(7) {}" is the function body
};
 
S::S(int x) : n{x} {} // constructor definition: ": n{x}" is the initializer list
 
int main()
{
    S s;      // calls S::S()
    S s2(10); // calls S::S(int)
}

```

### Explanation

Constructors have no names and cannot be called directly. They are invoked when initialization takes place, and they are selected according to the rules of initialization. The constructors without explicit specifier are converting constructors. The constructors with a constexpr specifier make their type a LiteralType. Constructors that may be called without any argument are default constructors. Constructors that take another object of the same type as the argument are copy constructors and move constructors.

Before the compound statement that forms the function body of the constructor begins executing, initialization of all direct bases, virtual bases, and non-static data members is finished. The member initializer list is the place where non-default initialization of these subobjects can be specified. For bases that cannot be default-initialized and for non-static data members that cannot be initialized by default-initialization or by their default member initializer, if any(since C++11), such as members of reference and const-qualified types, member initializers must be specified. (Note that default member initializers for non-static data members of class template instantiations may be invalid if the member type or initializer is dependent.)(since C++11) No initialization is performed for anonymous unions or variant members that do not have a member initializer or default member initializer(since C++11).

The initializers where class-or-identifier names a virtual base class are ignored during construction of any class that is not the most derived class of the object that's being constructed.

Names that appear in expression-list or braced-init-list are evaluated in scope of the constructor:

```
class X
{
    int a, b, i, j;
public:
    const int& r;
    X(int i)
      : r(a) // initializes X::r to refer to X::a
      , b{i} // initializes X::b to the value of the parameter i
      , i(i) // initializes X::i to the value of the parameter i
      , j(this->i) // initializes X::j to the value of X::i
    {}
};

```

Exceptions that are thrown from member initializers may be handled by a function try block.

Member functions (including virtual member functions) can be called from member initializers, but the behavior is undefined if not all direct bases are initialized at that point.

For virtual calls (if the direct bases are initialized at that point), the same rules apply as the rules for the virtual calls from constructors and destructors: virtual member functions behave as if the dynamic type of \*this is the static type of the class that's being constructed (dynamic dispatch does not propagate down the inheritance hierarchy) and virtual calls (but not static calls) to pure virtual member functions are undefined behavior.

|  |  |
| --- | --- |
| If a non-static data member has a default member initializer and also appears in a member initializer list, then the member initializer is used and the default member initializer is ignored:   ```text struct S {     int n = 42;   // default member initializer     S() : n(7) {} // will set n to 7, not 42 }; ``` | (since C++11) |

Reference members cannot be bound to temporaries in a member initializer list:

```
struct A
{
    A() : v(42) {} // Error
    const int& v;
};

```

Note: same applies to default member initializer.

|  |  |
| --- | --- |
| Delegating constructor If the name of the class itself appears as class-or-identifier in the member initializer list, then the list must consist of that one member initializer only; such a constructor is known as the **delegating constructor**, and the constructor selected by the only member of the initializer list is the **target constructor**.  In this case, the target constructor is selected by overload resolution and executed first, then the control returns to the delegating constructor and its body is executed.  Delegating constructors cannot be recursive.   ```text class Foo { public:      Foo(char x, int y) {}     Foo(int y) : Foo('a', y) {} // Foo(int) delegates to Foo(char, int) }; ```  Inheriting constructors See using declaration. | (since C++11) |

#### Initialization order

The order of member initializers in the list is irrelevant: the actual order of initialization is as follows:

1) If the constructor is for the most-derived class, virtual bases are initialized in the order in which they appear in depth-first left-to-right traversal of the base class declarations (left-to-right refers to the appearance in base-specifier lists).2) Then, direct bases are initialized in left-to-right order as they appear in this class's base-specifier list.3) Then, non-static data member are initialized in order of declaration in the class definition.4) Finally, the body of the constructor is executed.

(Note: if initialization order was controlled by the appearance in the member initializer lists of different constructors, then the destructor wouldn't be able to ensure that the order of destruction is the reverse of the order of construction.)

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_delegating_constructors` | `200604L` | (C++11) | Delegating constructors |

### Example

Run this code

```
#include <fstream>
#include <string>
#include <mutex>
 
struct Base
{
    int n;
};   
 
struct Class : public Base
{
    unsigned char x;
    unsigned char y;
    std::mutex m;
    std::lock_guard<std::mutex> lg;
    std::fstream f;
    std::string s;
 
    Class(int x) : Base{123}, // initialize base class
        x(x),     // x (member) is initialized with x (parameter)
        y{0},     // y initialized to 0
        f{"test.cc", std::ios::app}, // this takes place after m and lg are initialized
        s(__func__), // __func__ is available because init-list is a part of constructor
        lg(m),    // lg uses m, which is already initialized
        m{}       // m is initialized before lg even though it appears last here
    {}            // empty compound statement
 
    Class(double a) : y(a + 1),
        x(y), // x will be initialized before y, its value here is indeterminate
        lg(m)
    {} // base class initializer does not appear in the list, it is
       // default-initialized (not the same as if Base() were used, which is value-init)
 
    Class()
    try // function try block begins before the function body, which includes init list
      : Class(0.0) // delegate constructor
    {
        // ...
    }
    catch (...)
    {
        // exception occurred on initialization
    }
};
 
int main()
{
    Class c;
    Class c1(1);
    Class c2(0.1);
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 194 | C++98 | the declarator syntax of constructor only allowed at most one function specifier (e.g. a constructor cannot be declared inline explicit) | multiple function specifiers allowed |
| CWG 257 | C++98 | it was unspecified whether an abstract class should provide member initializers for its virtual base classes | specified as not required and such member initializers are ignored during execution |
| CWG 263 | C++98 | the declarator syntax of constructor prohibited constructors from being friends | allowed constructors to be friends |
| CWG 1345 | C++98 | anonymous union members without default member initializers were default-initialized | they are not initialized |
| CWG 1435 | C++98 | the meaning of “class name” in the declarator syntax of constructor was unclear | changed the syntax to a specialized function declarator syntax |
| CWG 1696 | C++98 | reference members could be initialized to temporaries (whose lifetime would end at the end of constructor) | such initialization is ill-formed |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 11.4.5 Constructors [class.ctor]

:   - 11.9.3 Initializing bases and members [class.base.init]

- C++20 standard (ISO/IEC 14882:2020):

:   - 11.4.4 Constructors [class.ctor]

:   - 11.10.2 Initializing bases and members [class.base.init]

- C++17 standard (ISO/IEC 14882:2017):

:   - 15.1 Constructors [class.ctor]

:   - 15.6.2 Initializing bases and members [class.base.init]

- C++14 standard (ISO/IEC 14882:2014):

:   - 12.1 Constructors [class.ctor]

:   - 12.6.2 Initializing bases and members [class.base.init]

- C++11 standard (ISO/IEC 14882:2011):

:   - 12.1 Constructors [class.ctor]

:   - 12.6.2 Initializing bases and members [class.base.init]

- C++98 standard (ISO/IEC 14882:1998):

:   - 12.1 Constructors [class.ctor]

:   - 12.6.2 Initializing bases and members [class.base.init]

### See also

- copy elision
- converting constructor
- copy assignment
- copy constructor
- default constructor
- destructor
- `explicit`
- initialization
  - aggregate initialization
  - constant initialization
  - copy initialization
  - default initialization
  - direct initialization
  - list initialization
  - reference initialization
  - value initialization
  - zero initialization
- move assignment
- move constructor
- `new`
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/constructor&oldid=172281>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 June 2024, at 22:34.