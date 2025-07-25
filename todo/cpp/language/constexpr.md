# `constexpr` specifier (since C++11)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const`/`volatile` | | | | | | decltype (C++11) | | | | | | auto (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****constexpr**** (C++11) | | | | | | consteval (C++20) | | | | | | constinit (C++20) | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Overview | | | | | | Declaration syntax | | | | | | **decl-specifier-seq** | | | | | | Declarator | | | | | | Conflicting declarations | | | | | | Specifiers | | | | | | typedef | | | | | | inline | | | | | | virtual function specifier | | | | | | explicit function specifier | | | | | | friend | | | | | | ****constexpr****(C++11) | | | | | | consteval(C++20) | | | | | | constinit(C++20) | | | | | | Storage class specifiers | | | | | | Translation-unit-local (C++20) | | | | | | class/struct | | | | | | union | | | | | | enum | | | | | | decltype(C++11) | | | | | | auto(C++11) | | | | | | alignas(C++11) | | | | | | constvolatile | | | | | | Pack indexing specifier (C++26) | | | | | | Elaborated type specifier | | | | | | Attributes (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Declarators | | | | | | Reference | | | | | | Pointer | | | | | | Array | | | | | | Block declarations | | | | | | Simple-declaration | | | | | | →Structured binding declaration (C++17) | | | | | | Alias declaration (C++11) | | | | | | Namespace alias definition | | | | | | using declaration | | | | | | `using` directive | | | | | | static_assert declaration (C++11) | | | | | | asm declaration | | | | | | Opaque enum declaration (C++11) | | | | | | Other declarations | | | | | | Namespace definition | | | | | | Function declaration | | | | | | Class template declaration | | | | | | Function template declaration | | | | | | Explicit template instantiation (C++11) | | | | | | Explicit template specialization | | | | | | Linkage specification | | | | | | Attribute declaration (C++11) | | | | | | Empty declaration | | | | | |  | | | | | |

:   - `constexpr` - specifies that the value of a variable, structured binding(since C++26) or function can appear in constant expressions

### Explanation

The constexpr specifier declares that it is possible to evaluate the value of the entities at compile time. Such entities can then be used where only compile time constant expressions are allowed (provided that appropriate function arguments are given).

A constexpr specifier used in an object declaration or non-static member function(until C++14) implies const.

A constexpr specifier used in the first declaration of a function or static data member(since C++17) implies inline. If any declaration of a function or function template has a constexpr specifier, then every declaration must contain that specifier.

### constexpr variable

A variable or variable template(since C++14) can be declared constexpr if all following conditions are satisfied:

- The declaration is a definition.
- It is of a literal type.
- It is initialized (by the declaration).

|  |  |
| --- | --- |
| - The full-expression of its initialization is a constant expression. | (until C++26) |
| - It is constant-initializable. | (since C++26) |

|  |  |
| --- | --- |
| - It has constant destruction, which means one of the following conditions needs to be satisfied:   - It is not of class type nor (possibly multi-dimensional) array thereof. - It is of a class type with a constexpr destructor or (possibly multi-dimensional) array thereof, and for a hypothetical expression e whose only effect is to destroy the object, e would be a core constant expression if the lifetime of the object and its non-mutable subobjects (but not its mutable subobjects) were considered to start within e.  If a constexpr variable is not translation-unit-local, it should not be initialized to refer to a translation-unit-local entity that is usable in constant expressions, nor have a subobject that refers to such an entity. Such initialization is disallowed in a module interface unit (outside its private module fragment, if any) or a module partition, and is deprecated in any other context. | (since C++20) |

### constexpr function

A function or function template can be declared constexpr.

A function is **constexpr-suitable** if all following conditions are satisfied:

|  |  |
| --- | --- |
| - It is not a virtual function. | (until C++20) |
| - Its return type (if exists) is a literal type. - Each of its parameter types is a literal type. | (until C++23) |
| - It is not a coroutine. | (since C++20) |

- If it is a constructor or destructor(since C++20), its class does not have any virtual base class.

|  |  |
| --- | --- |
| - Its function body is = default, = delete, or a compound statement enclosing only the following:   - null statements - `static_assert` declarations - `typedef` declarations and alias declarations that do not define classes or enumerations - using declarations - using directives - exactly one `return` statement if the function is not a constructor | (until C++14) |
| - Its function body is = default, = delete, or a compound statement that(until C++20) does ****not**** enclose the following:   - goto statements - statements with labels other than case and default   |  |  | | --- | --- | | - try blocks - inline assembly declarations - definitions of variables for which no initialization is performed | (until C++20) |   - definitions of variables of non-literal types - definitions of variables of static or thread storage duration | (since C++14) (until C++23) |

Except for instantiated constexpr functions, non-templated constexpr functions must be constexpr-suitable.

|  |  |
| --- | --- |
| For a non-constructor constexpr function that is neither defaulted nor templated, if no argument values exist such that an invocation of the function could be an evaluated subexpression of a core constant expression, the program is ill-formed, no diagnostic required.  For a templated constexpr function, if no specialization of the function/class template would make the templated function constexpr-suitable when considered as a non-templated function, the program is ill-formed, no diagnostic required. | (until C++23) |

An invocation of a constexpr function in a given context produces the same result as an invocation of an equivalent non-constexpr function in the same context in all respects, with the following exceptions:

- An invocation of a constexpr function can appear in a constant expression.
- Copy elision is not performed in a constant expression.

### constexpr constructor

On top of the requirements of constexpr functions, a constructor also needs to satisfy all following conditions to be constexpr-suitable:

|  |  |  |  |
| --- | --- | --- | --- |
| - Its function body is = delete or satisfies the following additional requirements:  |  |  | | --- | --- | | - If the class is a union having variant members, exactly one of them is initialized. - If the class is a union-like class, but is not a union, for each of its anonymous union members having variant members, exactly one of them is initialized. - Every non-variant non-static data member and base class subobject is initialized. | (until C++20) |   - If the constructor is a delegating constructor, the target constructor is a constexpr constructor. - If the constructor is a non-delegating constructor, every constructor selected to initialize non-static data members and base class subobjects is a constexpr constructor. | (until C++23) |

- The class does not have any virtual base class.

|  |  |
| --- | --- |
| For a constexpr constructor that is neither defaulted nor templated, if no argument values exist such that an invocation of the function could be an evaluated subexpression of the initialization full-expression of some object subject to constant expression, the program is ill-formed, no diagnostic required. | (until C++23) |

### constexpr destructor

|  |  |
| --- | --- |
| Destructors cannot be constexpr, but a trivial destructor can be implicitly called in constant expressions. | (until C++20) |
| On top of the requirements of constexpr functions, a destructor also needs to satisfy all following conditions to be constexpr-suitable:   |  |  | | --- | --- | | - For every subobject of class type or (possibly multi-dimensional) array thereof, that class type has a constexpr destructor. | (until C++23) |  - The class does not have any virtual base class. | (since C++20) |

### Notes

|  |  |
| --- | --- |
| Because the `noexcept` operator always returns true for a constant expression, it can be used to check if a particular invocation of a constexpr function takes the constant expression branch:   ```text constexpr int f();  constexpr bool b1 = noexcept(f()); // false, undefined constexpr function constexpr int f() { return 0; } constexpr bool b2 = noexcept(f()); // true, f() is a constant expression ``` | (until C++17) |

|  |  |
| --- | --- |
| It is possible to write a constexpr function whose invocation can never satisfy the requirements of a core constant expression:   ```text void f(int& i) // not a constexpr function {     i = 0; }   constexpr void g(int& i) // well-formed since C++23 {     f(i); // unconditionally calls f, cannot be a constant expression } ``` | (since C++23) |

Constexpr constructors are permitted for classes that are not literal types. For example, the default constructor of std::shared_ptr is constexpr, allowing constant initialization.

Reference variables can be declared constexpr (their initializers have to be reference constant expressions):

```
static constexpr int const& x = 42; // constexpr reference to a const int object
                                    // (the object has static storage duration
                                    //  due to life extension by a static reference)

```

|  |  |
| --- | --- |
| Even though try blocks and inline assembly are allowed in constexpr functions, throwing exceptions that are uncaught(since C++26) or executing the assembly is still disallowed in a constant expression.  If a variable has constant destruction, there is no need to generate machine code in order to call destructor for it, even if its destructor is not trivial.  A non-lambda, non-special-member, and non-templated constexpr function cannot implicitly become an immediate function. Users need to explicitly mark it consteval to make such an intended function definition well-formed. | (since C++20) |

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_constexpr` | `200704L` | (C++11) | constexpr |
| `201304L` | (C++14) | Relaxed constexpr, non-const constexpr methods |
| `201603L` | (C++17) | Constexpr lambda |
| `201907L` | (C++20) | Trivial default initialization and asm-declaration in constexpr functions |
| `202002L` | (C++20) | Changing the active member of a union in constant evaluation |
| `202110L` | (C++23) | Non-literal variables, labels, and goto statements in constexpr functions |
| `202207L` | (C++23) | Relaxing some constexpr restrictions |
| `202211L` | (C++23) | Permitting static constexpr variables in constexpr functions |
| `202306L` | (C++26) | Constexpr cast from void\*: towards constexpr type-erasure |
| `__cpp_constexpr_in_decltype` | `201711L` | (C++11) (DR) | Generation of function and variable definitions when needed for constant evaluation |
| `__cpp_constexpr_dynamic_alloc` | `201907L` | (C++20) | Operations for dynamic storage duration in constexpr functions |

### Keywords

constexpr

### Example

Defines C++11/14 constexpr functions that compute factorials; defines a literal type that extends string literals:

Run this code

```
#include <iostream>
#include <stdexcept>
 
// C++11 constexpr functions use recursion rather than iteration
constexpr int factorial(int n)
{
    return n <= 1 ? 1 : (n * factorial(n - 1));
}
 
// C++14 constexpr functions may use local variables and loops
#if __cplusplus >= 201402L
constexpr int factorial_cxx14(int n)
{
    int res = 1;
    while (n > 1)
        res *= n--;
    return res;
}
#endif // C++14
 
// A literal class
class conststr
{
    const char* p;
    std::size_t sz;
public:
    template<std::size_t N>
    constexpr conststr(const char(&a)[N]): p(a), sz(N - 1) {}
 
    // constexpr functions signal errors by throwing exceptions
    // in C++11, they must do so from the conditional operator ?:
    constexpr char operator[](std::size_t n) const
    {
        return n < sz ? p[n] : throw std::out_of_range("");
    }
 
    constexpr std::size_t size() const { return sz; }
};
 
// C++11 constexpr functions had to put everything in a single return statement
// (C++14 does not have that requirement)
constexpr std::size_t countlower(conststr s, std::size_t n = 0,
                                             std::size_t c = 0)
{
    return n == s.size() ? c :
        'a' <= s[n] && s[n] <= 'z' ? countlower(s, n + 1, c + 1)
                                   : countlower(s, n + 1, c);
}
 
// An output function that requires a compile-time constant, for testing
template<int n>
struct constN
{
    constN() { std::cout << n << '\n'; }
};
 
int main()
{
    std::cout << "4! = ";
    constN<factorial(4)> out1; // computed at compile time
 
    volatile int k = 8; // disallow optimization using volatile
    std::cout << k << "! = " << factorial(k) << '\n'; // computed at run time
 
    std::cout << "The number of lowercase letters in \"Hello, world!\" is ";
    constN<countlower("Hello, world!")> out2; // implicitly converted to conststr
 
    constexpr int a[12] = {0, 1, 2, 3, 4, 5, 6, 7, 8};
    constexpr int length_a = sizeof a / sizeof(int); // std::size(a) in C++17,
                                                      // std::ssize(a) in C++20
    std::cout << "Array of length " << length_a << " has elements: ";
    for (int i = 0; i < length_a; ++i)
        std::cout << a[i] << ' ';
    std::cout << '\n';
}

```

Output:

```
4! = 24
8! = 40320
The number of lowercase letters in "Hello, world!" is 9
Array of length 12 has elements: 0 1 2 3 4 5 6 7 8 0 0 0

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1358 | C++11 | templated constexpr functions also needed to have at least one valid argument value | no need |
| CWG 1359 | C++11 | constexpr union constructors must initialize all data members | initializes exactly one data member for non-empty unions |
| CWG 1366 | C++11 | classes with constexpr constructors whose function bodies are = default or = delete could have virtual base classes | such classes can neither have virtual base classes |
| CWG 1595 | C++11 | constexpr delegating constructors required all involved constructors to be constexpr | only requires the target constructor to be constexpr |
| CWG 1712 | C++14 | a constexpr variable template was required to have all its declarations contain the constexpr specifier[[1]](constexpr.html#cite_note-1) | not required anymore |
| CWG 1911 | C++11 | constexpr constructors for non-literal types were not allowed | allowed in constant initialization |
| CWG 2004 | C++11 | copy/move of a union with a mutable member was allowed in a constant expression | mutable variants disqualify implicit copy/move |
| CWG 2022 | C++98 | whether equivalent constexpr and non-constexpr function produce equal result might depend on whether copy elision is performed | assume that copy elision is always performed in constant expressions |
| CWG 2163 | C++14 | labels were allowed in constexpr functions even though goto statements are prohibited | labels also prohibited |
| CWG 2268 | C++11 | copy/move of a union with a mutable member was prohibited by the resolution of CWG issue 2004 | allowed if the object is created within the constant expression |
| CWG 2278 | C++98 | the resolution of CWG issue 2022 was not implementable | assume that copy elision is never performed in constant expressions |
| CWG 2531 | C++11 | a non-inline variable became inline if it is redeclared with constexpr | the variable does not become inline |

1. ↑ It is redundant because there cannot be more than one declaration of a variable template with the constexpr specifier.

### See also

|  |  |
| --- | --- |
| constant expression | defines an expression that can be evaluated at compile time |
| `consteval` specifier(C++20) | specifies that a function is an **immediate function**, that is, every call to the function must be in a constant evaluation |
| `constinit` specifier(C++20) | asserts that a variable has static initialization, i.e. zero initialization and constant initialization |
| C documentation for constexpr | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/constexpr&oldid=179324>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 January 2025, at 01:32.