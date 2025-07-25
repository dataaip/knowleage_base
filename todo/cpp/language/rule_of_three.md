# The rule of three/five/zero

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

### Rule of three

If a class requires a user-defined destructor, a user-defined copy constructor, or a user-defined copy assignment operator, it almost certainly requires all three.

Because C++ copies and copy-assigns objects of user-defined types in various situations (passing/returning by value, manipulating a container, etc), these special member functions will be called, if accessible, and if they are not user-defined, they are implicitly-defined by the compiler.

The implicitly-defined special member functions should not be used if the class manages a resource whose handle does not destroy the resource themselves (raw pointer, POSIX file descriptor, etc), whose destructor does nothing and copy constructor/assignment operator only copies the value of the handle, without duplicating the underlying resource.

Run this code

```
#include <cstddef>
#include <cstring>
#include <iostream>
#include <utility>
 
class rule_of_three
{
    char* cstring; // raw pointer used as a handle to a
                   // dynamically-allocated memory block
 
public:
    rule_of_three(const char* s, std::size_t n)
        : cstring(new char[n + 1]) // allocate
    {
        std::memcpy(cstring, s, n); // populate
        cstring[n] = '\0';          // tail 0
    }
 
    explicit rule_of_three(const char* s = "")
        : rule_of_three(s, std::strlen(s))
    {
    }
 
    ~rule_of_three() // I. destructor
    {
        delete[] cstring; // deallocate
    }
 
    rule_of_three(const rule_of_three& other) // II. copy constructor
        : rule_of_three(other.cstring)
    {
    }
 
    rule_of_three& operator=(const rule_of_three& other) // III. copy assignment
    {
        if (this == &other)
            return *this;
 
        rule_of_three temp(other); // use the copy constructor
        std::swap(cstring, temp.cstring); // exchange the underlying resource
 
        return *this;
    }
 
    const char* c_str() const // accessor
    {
        return cstring;
    }
};
 
int main()
{
    rule_of_three o1{"abc"};
    std::cout << o1.c_str() << ' ';
    auto o2{o1}; // II. uses copy constructor
    std::cout << o2.c_str() << ' ';
    rule_of_three o3{"def"};
    std::cout << o3.c_str() << ' ';
    o3 = o2; // III. uses copy assignment
    std::cout << o3.c_str() << '\n';
}   // I. all destructors are called here

```

Output:

```
abc abc def abc

```

Classes that manage non-copyable resources through copyable handles may have to declare copy assignment and copy constructor private and not provide their definitions(until C++11)define copy assignment and copy constructor as = delete(since C++11). This is another application of the rule of three: deleting one and leaving the other to be implicitly-defined typically incorrect.

### Rule of five

Because the presence of a user-defined (include = default or = delete declared) destructor, copy-constructor, or copy-assignment operator prevents implicit definition of the move constructor and the move assignment operator, any class for which move semantics are desirable, has to declare all five special member functions:

```
#include <cstddef>
#include <cstring>
#include <utility>
 
class rule_of_five
{
    char* cstring; // raw pointer used as a handle to a
                   // dynamically-allocated memory block
 
public:
    rule_of_five(const char* s, std::size_t n)
        : cstring(new char[n + 1]) // allocate
    {
        std::memcpy(cstring, s, n); // populate
        cstring[n] = '\0';          // tail 0
    }
 
    explicit rule_of_five(const char* s)
        : rule_of_five(s, std::strlen(s))
    {
    }
 
    ~rule_of_five() // I. destructor
    {
        delete[] cstring; // deallocate
    }
 
    rule_of_five(const rule_of_five& other) // II. copy constructor
        : rule_of_five(other.cstring)
    {
    }
 
    rule_of_five& operator=(const rule_of_five& other) // III. copy assignment
    {
        if (this == &other)
            return *this;
 
        rule_of_five temp(other); // use the copy constructor
        std::swap(cstring, temp.cstring); // exchange the underlying resource
 
        return *this;
    }
 
    rule_of_five(rule_of_five&& other) noexcept // IV. move constructor
        : cstring(std::exchange(other.cstring, nullptr))
    {
    }
 
    rule_of_five& operator=(rule_of_five&& other) noexcept // V. move assignment
    {
        rule_of_five temp(std::move(other));
        std::swap(cstring, temp.cstring);
        return *this;
    }
};

```

Unlike Rule of Three, failing to provide move constructor and move assignment is usually not an error, but it will result in a loss of performance.

### Rule of zero

Classes that have custom destructors, copy/move constructors or copy/move assignment operators should deal exclusively with ownership (which follows from the Single Responsibility Principle). Other classes should not have custom destructors, copy/move constructors or copy/move assignment operators[[1]](rule_of_three.html#cite_note-1).

This rule also appears in the C++ Core Guidelines as C.20: If you can avoid defining default operations, do.

```
class rule_of_zero
{
    std::string cppstring;
public:
    // redundant, implicitly defined is better
    // rule_of_zero(const std::string& arg) : cppstring(arg) {}
};

```

When a base class is intended for polymorphic use, its destructor may have to be declared public and virtual. This blocks implicit moves (and deprecates implicit copies), and so the special member functions have to be defined as = default[[2]](rule_of_three.html#cite_note-2).

```
class base_of_five_defaults
{
public:
    base_of_five_defaults(const base_of_five_defaults&) = default;
    base_of_five_defaults(base_of_five_defaults&&) = default;
    base_of_five_defaults& operator=(const base_of_five_defaults&) = default;
    base_of_five_defaults& operator=(base_of_five_defaults&&) = default;
    virtual ~base_of_five_defaults() = default;
};

```

However, this makes the class prone to slicing, which is why polymorphic classes often define copy as = delete (see C.67: A polymorphic class should suppress public copy/move in C++ Core Guidelines), which leads to the following generic wording for the Rule of Five:

:   C.21: If you define or =delete any copy, move, or destructor function, define or =delete them all.

### External links

|  |
| --- |
| 1. ↑ "Rule of Zero", R. Martinho Fernandes 08/15/2012 2. ↑ "A Concern about the Rule of Zero", Scott Meyers, 3/13/2014. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/rule_of_three&oldid=176493>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 September 2024, at 15:24.