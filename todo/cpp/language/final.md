# `final` specifier (since C++11)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Virtual function | | | | | | `override` specifier (C++11) | | | | | | ****`final` specifier**** (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | explicit (C++11) | | | | | | static | | | | | |  | | | | | |
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
| ****`final` specifier**** (C++11) | | | | |

Specifies that a virtual function cannot be overridden in a derived class, or that a class cannot be derived from.

### Syntax

When applied to a member function, the identifier `final` appears immediately after the declarator in the syntax of a member function declaration or a member function definition inside a class definition.

When applied to a class (including struct and union), the identifier `final` appears at the beginning of the class definition, immediately after the name of the class, and cannot appear in a class declaration.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| declarator virt-specifier-seq ﻿(optional) pure-specifier ﻿(optional) | (1) |  |
|  | | | | | | | | | |
| declarator virt-specifier-seq ﻿(optional) function-body | (2) |  |
|  | | | | | | | | | |
| class-key attr ﻿(optional) class-head-name class-virt-specifier ﻿(optional) base-clause ﻿(optional) | (3) |  |
|  | | | | | | | | | |

1) In a member function declaration, `final` may appear in virt-specifier-seq immediately after the declarator, and before the pure-specifier, if used.2) In a member function definition inside a class definition, `final` may appear in virt-specifier-seq immediately after the declarator and just before function-body.3) In a class definition, `final` may appear as class-virt-specifier immediately after the name of the class, just before the colon that begins the base-clause, if used.

In the cases (1,2), virt-specifier-seq, if used, is either `override` or `final`, or `final override` or `override final`. In the case (3), the only allowed value of class-virt-specifier, if used, is `final`.

### Explanation

When used in a virtual function declaration or definition, final specifier ensures that the function is virtual and specifies that it may not be overridden by derived classes. The program is ill-formed (a compile-time error is generated) otherwise.

When used in a class definition, final specifies that this class may not appear in the base-specifier-list of another class definition (in other words, cannot be derived from). The program is ill-formed otherwise (a compile-time error is generated). final can also be used with a union definition, in which case it has no effect (other than on the outcome of std::is_final)(since C++14), since unions cannot be derived from.

final is an identifier with a special meaning when used in a member function declaration or class head. In other contexts, it is not reserved and may be used to name objects and functions.

### Note

In a sequence of the following tokens:

1. one of class, struct and union
2. a possibly qualified identifier
3. final
4. one of : and {

the third token final in the sequence is always considered as a specifier instead of an identifier.

Run this code

```
struct A;
struct A final {}; // OK, definition of struct A,
                   // not value-initialization of variable final
 
struct X
{
    struct C { constexpr operator int() { return 5; } };
    struct B final : C{}; // OK, definition of nested class B,
                          // not declaration of a bit-field member final
};
 
// Abnormal final usage.
 
struct final final // OK, definition of a struct named `final` from which
{                  // you cannot inherit
};
 
// struct final final {}; // Error: redefinition of `struct final`, NOT a
                          // definition of a variable `final` using an elaborated
                          // type specifier `struct final` followed by an
                          // aggregate initialization
 
// struct override : final {}; // Error: cannot derive from final base type;
                               // `override` in given context is a normal name
void foo()
{
    [[maybe_unused]]
    final final; // OK, declaration of a variable named `final` of type
                 // `struct final` 
}
 
struct final final; // OK, declaration of a variable named `final` of type
                    // `struct final` using an elaborated type specifier
int main()
{
}

```

### Keywords

final

### Example

Run this code

```
struct Base
{
    virtual void foo();
};
 
struct A : Base
{
    void foo() final; // Base::foo is overridden and A::foo is the final override
    void bar() final; // Error: bar cannot be final as it is non-virtual
};
 
struct B final : A // struct B is final
{
    void foo() override; // Error: foo cannot be overridden as it is final in A
};
 
struct C : B {}; // Error: B is final

```

Possible output:

```
main.cpp:9:10: error: 'void A::bar()' marked 'final', but is not virtual
    9 |     void bar() final; // Error: bar cannot be final as it is non-virtual
      |          ^~~
main.cpp:14:10: error: virtual function 'virtual void B::foo()' overriding final function
   14 |     void foo() override; // Error: foo cannot be overridden as it is final in A
      |          ^~~
main.cpp:8:10: note: overridden function is 'virtual void A::foo()'
    8 |     void foo() final; // Base::foo is overridden and A::foo is the final override
      |          ^~~
main.cpp:17:8: error: cannot derive from 'final' base 'B' in derived type 'C'
   17 | struct C : B // Error: B is final
      |

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 11 Classes [class]

:   - 11.7.3 Virtual functions [class.virtual]

- C++20 standard (ISO/IEC 14882:2020):

:   - 11 Classes [class]

:   - 11.7.2 Virtual functions [class.virtual]

- C++17 standard (ISO/IEC 14882:2017):

:   - 12 Classes [class]

:   - 13.3 Virtual functions [class.virtual]

- C++14 standard (ISO/IEC 14882:2014):

:   - 9 Classes [class]

:   - 10.3 Virtual functions [class.virtual]

- C++11 standard (ISO/IEC 14882:2011):

:   - 9 Classes [class]

:   - 10.3 Virtual functions [class.virtual]

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1318 | C++11 | a class definition which has final after the class name and an empty member specification list might make final an identifier | final is always a specifier in this case |

### See also

|  |  |
| --- | --- |
| `override` specifier(C++11) | explicitly declares that a method overrides another method |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/final&oldid=176072>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 September 2024, at 11:08.