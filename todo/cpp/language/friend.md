# Friend declaration

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | Constructors | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Access specifiers | | | | | | ****`friend` specifier**** | | | | | |  | | | | | |
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
| Constructors and member initializer lists | | | | |
| Default member initializer (C++11) | | | | |
| ****`friend` specifier**** | | | | |
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

The friend declaration appears in a class body and grants a function or another class access to private and protected members of the class where the friend declaration appears.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `friend` function-declaration | (1) |  |
|  | | | | | | | | | |
| `friend` function-definition | (2) |  |
|  | | | | | | | | | |
| `friend` elaborated-type-specifier `;` | (3) | (until C++26) |
|  | | | | | | | | | |
| `friend` simple-type-specifier `;` `friend` typename-specifier `;` | (4) | (since C++11) (until C++26) |
|  | | | | | | | | | |
| `friend` friend-type-specifier-list `;` | (5) | (since C++26) |
|  | | | | | | | | | |

1,2) A function friend declaration.3-5) A class friend declaration.

|  |  |  |
| --- | --- | --- |
| function-declaration | - | a function declaration |
| function-definition | - | a function definition |
| elaborated-type-specifier | - | an elaborated type specifier |
| simple-type-specifier | - | a simple type specifier |
| typename-specifier | - | the keyword typename followed by a qualified identifier or qualified simple template identifier |
| friend-type-specifier-list | - | a non-empty comma-separated list of simple-type-specifier, elaborated-type-specifier, and typename-specifier ﻿s, each specifier can be followed by an ellipsis (`...`) |

### Description

1) Designates a function or several functions as friends of this class:

```
class Y
{
    int data; // private member
 
    // the non-member function operator<< will have access to Y's private members
    friend std::ostream& operator<<(std::ostream& out, const Y& o);
    friend char* X::foo(int); // members of other classes can be friends too
    friend X::X(char), X::~X(); // constructors and destructors can be friends
};
 
// friend declaration does not declare a member function
// this operator<< still needs to be defined, as a non-member
std::ostream& operator<<(std::ostream& out, const Y& y)
{
    return out << y.data; // can access private member Y::data
}

```

2) (only allowed in non-local class definitions) Defines a non-member function, and makes it a friend of this class at the same time. Such non-member function is always inline, unless it is attached to a named module(since C++20).

```
class X
{
    int a;
 
    friend void friend_set(X& p, int i)
    {
        p.a = i; // this is a non-member function
    }
public:
    void member_set(int i)
    {
        a = i; // this is a member function
    }
};

```

3,4) Designates a class as a friend of this class. This means that the friend's member declarations and definitions can access private and protected members of this class and also that the friend can inherit from private and protected members of this class.3) The class is named by elaborated-type-specifier. The name of the class that is used in this friend declaration does not need to be previously declared.4) The class is named by simple-type-specifier or typename-specifier. If the named type is not a class type, this friend declaration is ignored. This declaration will not forward declare a new type.5) Designates all classes in friend-type-specifier-list as a friend of this class. This means that the friends' member declarations and definitions can access private and protected members of this class and also that the friends can inherit from private and protected members of this class. If a named type is not a class type, it is ignored in this friend declaration. Each specifier in friend-type-specifier-list names a class if the specifier is not followed by an ellipsis, otherwise pack expansion applies.

```
class Y {};
 
class A
{
    int data; // private data member
 
    class B {}; // private nested type
 
    enum { a = 100 }; // private enumerator
 
    friend class X; // friend class forward declaration (elaborated class specifier)
    friend Y; // friend class declaration (simple type specifier) (since C++11)
 
    // the two friend declarations above can be merged since C++26:
    // friend class X, Y;
};
 
class X : A::B // OK: A::B accessible to friend
{
    A::B mx; // OK: A::B accessible to member of friend
 
    class Y
    {
        A::B my; // OK: A::B accessible to nested member of friend
    };
 
    int v[A::a]; // OK: A::a accessible to member of friend
};

```

### Template friends

Both function template and class template declarations may appear with the `friend` specifier in any non-local class or class template (although only function templates may be defined within the class or class template that is granting friendship). In this case, every specialization of the template becomes a friend, whether it is implicitly instantiated, partially specialized, or explicitly specialized.

```
class A
{
    template<typename T>
    friend class B; // every B<T> is a friend of A
 
    template<typename T>
    friend void f(T) {} // every f<T> is a friend of A
};

```

Friend declarations cannot refer to partial specializations, but can refer to full specializations:

```
template<class T>
class A {};      // primary
 
template<class T>
class A<T*> {};  // partial
 
template<>
class A<int> {}; // full
 
class X
{
    template<class T>
    friend class A<T*>;  // Error
 
    friend class A<int>; // OK
};

```

When a friend declaration refers to a full specialization of a function template, the keyword inline, constexpr(since C++11), consteval(since C++20) and default arguments cannot be used:

```
template<class T>
void f(int);
 
template<>
void f<int>(int);
 
class X
{
    friend void f<int>(int x = 1); // error: default args not allowed
};

```

A template friend declaration can name a member of a class template A, which can be either a member function or a member type (the type must use elaborated-type-specifier). Such declaration is only well-formed if the last component in its nested-name-specifier (the name to the left of the last `::`) is a simple-template-id (template name followed by argument list in angle brackets) that names the class template. The template parameters of such template friend declaration must be deducible from the simple-template-id.

In this case, the member of any specialization of either A or partial specializations of A becomes a friend. This does not involve instantiating the primary template A or partial specializations of A: the only requirements are that the deduction of the template parameters of A from that specialization succeeds, and that substitution of the deduced template arguments into the friend declaration produces a declaration that would be a valid redeclaration of the member of the specialization:

```
// primary template
template<class T>
struct A
{ 
    struct B {};
 
    void f();
 
    struct D { void g(); };
 
    T h();
 
    template<T U>
    T i();
};
 
// full specialization
template<>
struct A<int>
{
    struct B {};
 
    int f();
 
    struct D { void g(); };
 
    template<int U>
    int i();
};
 
// another full specialization
template<>
struct A<float*>
{
    int *h();
};
 
// the non-template class granting friendship to members of class template A
class X
{
    template<class T>
    friend struct A<T>::B; // all A<T>::B are friends, including A<int>::B
 
    template<class T>
    friend void A<T>::f(); // A<int>::f() is not a friend because its signature
                           // does not match, but e.g. A<char>::f() is a friend
 
//  template<class T>
//  friend void A<T>::D::g(); // ill-formed, the last part of the nested-name-specifier,
//                            // D in A<T>::D::, is not simple-template-id
 
    template<class T>
    friend int* A<T*>::h(); // all A<T*>::h are friends:
                            // A<float*>::h(), A<int*>::h(), etc
 
    template<class T> 
    template<T U>       // all instantiations of A<T>::i() and A<int>::i() are friends, 
    friend T A<T>::i(); // and thereby all specializations of those function templates
};

```

|  |  |
| --- | --- |
| Default template arguments are only allowed on template friend declarations if the declaration is a definition and no other declarations of this function template appear in this translation unit. | (since C++11) |

### Template friend operators

A common use case for template friends is declaration of a non-member operator overload that acts on a class template, e.g. operator<<(std::ostream&, const Foo<T>&) for some user-defined Foo<T>.

Such operator can be defined in the class body, which has the effect of generating a separate non-template operator<< for each `T` and makes that non-template operator<< a friend of its Foo<T>:

Run this code

```
#include <iostream>
 
template<typename T>
class Foo
{
public:
    Foo(const T& val) : data(val) {}
private:
    T data;
 
    // generates a non-template operator<< for this T
    friend std::ostream& operator<<(std::ostream& os, const Foo& obj)
    {
        return os << obj.data;
    }
};
 
int main()
{
    Foo<double> obj(1.23);
    std::cout << obj << '\n';
}

```

Output:

```
1.23

```

or the function template has to be declared as a template before the class body, in which case the friend declaration within Foo<T> can refer to the full specialization of operator<< for its `T`:

Run this code

```
#include <iostream>
 
template<typename T>
class Foo; // forward declare to make function declaration possible
 
template<typename T> // declaration
std::ostream& operator<<(std::ostream&, const Foo<T>&);
 
template<typename T>
class Foo
{
public:
    Foo(const T& val) : data(val) {}
private:
    T data;
 
    // refers to a full specialization for this particular T 
    friend std::ostream& operator<< <> (std::ostream&, const Foo&);
 
    // note: this relies on template argument deduction in declarations
    // can also specify the template argument with operator<< <T>"
};
 
// definition
template<typename T>
std::ostream& operator<<(std::ostream& os, const Foo<T>& obj)
{
    return os << obj.data;
}
 
int main()
{
    Foo<double> obj(1.23);
    std::cout << obj << '\n';
}

```

### Linkage

Storage class specifiers are not allowed in friend declarations.

|  |  |
| --- | --- |
| If a function or function template is first declared and defined in a friend declaration, and the enclosing class is defined within an exporting declarations, its name has the same linkage as the name of the enclosing class. | (since C++20) |

If(until C++20)Otherwise, if(since C++20) a function or function template is declared in a friend declaration, and a corresponding non-friend declaration is reachable, the name has the linkage determined from that prior declaration.

Otherwise, the linkage of the name introduced by a friend declaration is determined as usual.

### Notes

Friendship is not transitive (a friend of your friend is not your friend).

Friendship is not inherited (your friend's children are not your friends, and your friends are not your children's friends).

Access specifiers have no effect on the meaning of friend declarations (they can appear in private: or in public: sections, with no difference).

A friend class declaration cannot define a new class (friend class X {}; is an error).

When a local class declares an unqualified function or class as a friend, only functions and classes in the innermost non-class scope are looked up, not the global functions:

```
class F {};
 
int f();
 
int main()
{
    extern int g();
 
    class Local // Local class in the main() function
    {
        friend int f(); // Error, no such function declared in main()
        friend int g(); // OK, there is a declaration for g in main()
        friend class F; // friends a local F (defined later)
        friend class ::F; // friends the global F
    };
 
    class F {}; // local F
}

```

A name first declared in a friend declaration within a class or class template `X` becomes a member of the innermost enclosing namespace of `X`, but is not visible for lookup (except argument-dependent lookup that considers `X`) unless a matching declaration at namespace scope is provided - see namespaces for details.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_variadic_friend` | `202403L` | (C++26) | Variadic friend declarations |

### Keywords

friend

### Example

Stream insertion and extraction operators are often declared as non-member friends:

Run this code

```
#include <iostream>
#include <sstream>
 
class MyClass
{
    int i;                   // friends have access to non-public, non-static
    static inline int id{6}; // and static (possibly inline) members
 
    friend std::ostream& operator<<(std::ostream& out, const MyClass&);
    friend std::istream& operator>>(std::istream& in, MyClass&);
    friend void change_id(int);
public:
    MyClass(int i = 0) : i(i) {}
};
 
std::ostream& operator<<(std::ostream& out, const MyClass& mc)
{
    return out << "MyClass::id = " << MyClass::id << "; i = " << mc.i;
}
 
std::istream& operator>>(std::istream& in, MyClass& mc)
{
    return in >> mc.i;
}
 
void change_id(int id) { MyClass::id = id; }
 
int main()
{
    MyClass mc(7);
    std::cout << mc << '\n';
//  mc.i = 333*2;  // error: i is a private member
    std::istringstream("100") >> mc;
    std::cout << mc << '\n';
//  MyClass::id = 222*3;  // error: id is a private member
    change_id(9);
    std::cout << mc << '\n';
}

```

Output:

```
MyClass::id = 6; i = 7
MyClass::id = 6; i = 100
MyClass::id = 9; i = 100

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 45 | C++98 | members of a class nested in a friend class of `T` have no special access to `T` | a nested class has the same access as the enclosing class |
| CWG 500 | C++98 | friend class of `T` cannot inherit from private or protected members of `T`, but its nested class can | both can inherit from such members |
| CWG 1439 | C++98 | the rule targeting friend declarations in non-local classes did not cover template declarations | covered |
| CWG 1477 | C++98 | a name first declared in a friend declaration within a class or class template was not visible for lookup if the matching declaration is provided in another namespace scope | it is visible for lookup in this case |
| CWG 1804 | C++98 | when a member of a class template is friended, the corresponding member of specializations of partial specializations of the class template was not a friend of the class granting friendship | such members are also friends |
| CWG 2379 | C++11 | friend declarations referring to full specializations of function templates could be declared constexpr | prohibited |
| CWG 2588 | C++98 | the linkages of names introduced by friend declarations were unclear | made clear |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 11.8.4 Friends [class.friend]

:   - 13.7.5 Friends [temp.friend]

- C++20 standard (ISO/IEC 14882:2020):

:   - 11.9.3 Friends [class.friend]

:   - 13.7.4 Friends [temp.friend]

- C++17 standard (ISO/IEC 14882:2017):

:   - 14.3 Friends [class.friend]

:   - 17.5.4 Friends [temp.friend]

- C++14 standard (ISO/IEC 14882:2014):

:   - 11.3 Friends [class.friend]

:   - 14.5.4 Friends [temp.friend]

- C++11 standard (ISO/IEC 14882:2011):

:   - 11.3 Friends [class.friend]

:   - 14.5.4 Friends [temp.friend]

- C++98 standard (ISO/IEC 14882:1998):

:   - 11.3 Friends [class.friend]

:   - 14.5.3 Friends [temp.friend]

### See also

|  |  |
| --- | --- |
| Class types | defines types holding several data members |
| Access specifiers | defines visibility of class members |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/friend&oldid=174568>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 August 2024, at 22:41.