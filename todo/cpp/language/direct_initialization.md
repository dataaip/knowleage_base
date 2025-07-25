# Direct-initialization

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default-initialization | | | | | | Value-initialization | | | | | | Zero-initialization | | | | | | Copy-initialization | | | | | | ****Direct-initialization**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Aggregate initialization | | | | | | List-initialization (C++11) | | | | | | Constant initialization | | | | | | Reference initialization | | | | | |  | | | | | |

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
| ****Direct initialization**** | | | | |
| Copy-initialization | | | | |
| List initialization (C++11) | | | | |
| Aggregate initialization | | | | |
| Reference initialization | | | | |
| Copy elision | | | | |
| Static initialization | | | | |
| Zero initialization | | | | |
| Constant initialization | | | | |
| Dynamic non-local initialization | | | | |
| Ordered dynamic initialization | | | | |
| Unordered dynamic initialization | | | | |
| Class member initialization | | | | |
| Member initializer list | | | | |
| Default member initializer (C++11) | | | | |

Initializes an object from explicit set of constructor arguments.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| T object `(` arg `);` T object `(` arg1, arg2, ... `);` | (1) |  |
|  | | | | | | | | | |
| T object `{` arg `};` | (2) | (since C++11) |
|  | | | | | | | | | |
| T `(` other `)` T `(` arg1, arg2, ... `)` | (3) |  |
|  | | | | | | | | | |
| `static_cast<` T `>(` other `)` | (4) |  |
|  | | | | | | | | | |
| `new` T`(` args, ... `)` | (5) |  |
|  | | | | | | | | | |
| Class`::`Class`()` `:` member`(` args, ... `)` `{` ... `}` | (6) |  |
|  | | | | | | | | | |
| `[`arg`]() {` ... `}` | (7) | (since C++11) |
|  | | | | | | | | | |

### Explanation

Direct-initialization is performed in the following situations:

1) Initialization with a nonempty parenthesized list of expressions or braced-init-lists(since C++11).2) Initialization of an object of non-class type with a single brace-enclosed initializer (note: for class types and other uses of braced-init-list, see list-initialization)(since C++11).3) Initialization of a prvalue temporary(until C++17)the result object of a prvalue(since C++17) by function-style cast or with a parenthesized expression list.4) Initialization of a prvalue temporary(until C++17)the result object of a prvalue(since C++17) by a static_cast expression.5) Initialization of an object with dynamic storage duration by a new-expression with an initializer.6) Initialization of a base or a non-static member by constructor initializer list.7) Initialization of closure object members from the variables caught by copy in a lambda-expression.

The effects of direct-initialization are:

- If `T` is an array type,

|  |  |
| --- | --- |
| - the program is ill-formed. | (until C++20) |
| - the array is initialized as in aggregate initialization, except that narrowing conversions are allowed and any elements without an initializer are value-initialized.   ```text struct A {     explicit A(int i = 0) {} };   A a2); // OK: initializes a[0] with A(1) and a[1] with A() A b[2]{A(1)}; // error: implicit copy-list-initialization of b[1]               //        from {} selected explicit constructor ``` | (since C++20) |

- If `T` is a class type,

|  |  |
| --- | --- |
| - if the initializer is a prvalue expression whose type is the same class as `T` (ignoring cv-qualification), the initializer expression itself, rather than a temporary materialized from it, is used to initialize the destination object. (Before C++17, the compiler may elide the construction from the prvalue temporary in this case, but the appropriate constructor must still be accessible: see copy elision) | (since C++17) |

:   - the constructors of `T` are examined and the best match is selected by overload resolution. The constructor is then called to initialize the object.

|  |  |
| --- | --- |
| - otherwise, if the destination type is a (possibly cv-qualified) aggregate class, it is initialized as described in aggregate initialization except that narrowing conversions are permitted, designated initializers are not allowed, a temporary bound to a reference does not have its lifetime extended, there is no brace elision, and any elements without an initializer are value-initialized.   ```text struct B {     int a;     int&& r; };   int f(); int n = 10;   B b1{1, f()};            // OK, lifetime is extended B b2(1, f());            // well-formed, but dangling reference B b3{1.0, 1};            // error: narrowing conversion B b4(1.0, 1);            // well-formed, but dangling reference B b5(1.0, std::move(n)); // OK ``` | (since C++20) |

- Otherwise, if `T` is a non-class type but the source type is a class type, the conversion functions of the source type and its base classes, if any, are examined and the best match is selected by overload resolution. The selected user-defined conversion is then used to convert the initializer expression into the object being initialized.
- Otherwise, if `T` is bool and the source type is std::nullptr_t, the value of the initialized object is false.
- Otherwise, standard conversions are used, if necessary, to convert the value of other to the cv-unqualified version of `T`, and the initial value of the object being initialized is the (possibly converted) value.

### Notes

Direct-initialization is more permissive than copy-initialization: copy-initialization only considers non-explicit constructors and non-explicit user-defined conversion functions, while direct-initialization considers all constructors and all user-defined conversion functions.

In case of ambiguity between a variable declaration using the direct-initialization syntax (1) (with round parentheses) and a function declaration, the compiler always chooses function declaration. This disambiguation rule is sometimes counter-intuitive and has been called the most vexing parse.

Run this code

```
#include <fstream>
#include <iterator>
#include <string>
 
int main()
{
    std::ifstream file("data.txt");
 
    // The following is a function declaration:
    std::string foo1(std::istreambuf_iterator<char>(file),
                     std::istreambuf_iterator<char>());
    // It declares a function called foo1, whose return type is std::string,
    // first parameter has type std::istreambuf_iterator<char> and the name "file",
    // second parameter has no name and has type std::istreambuf_iterator<char>(),
    // which is rewritten to function pointer type std::istreambuf_iterator<char>(*)()
 
    // Pre-C++11 fix (to declare a variable) - add extra parentheses around one
    // of the arguments:
    std::string str1((std::istreambuf_iterator<char>(file)),
                      std::istreambuf_iterator<char>());
 
    // Post-C++11 fix (to declare a variable) - use list-initialization for any
    // of the arguments:
    std::string str2(std::istreambuf_iterator<char>{file}, {});
}

```

### Example

Run this code

```
#include <iostream>
#include <memory>
#include <string>
 
struct Foo
{
    int mem;
    explicit Foo(int n) : mem(n) {}
};
 
int main()
{
    std::string s1("test"); // constructor from const char*
    std::string s2(10, 'a');
 
    std::unique_ptr<int> p(new int(1));  // OK: explicit constructors allowed
//  std::unique_ptr<int> p = new int(1); // error: constructor is explicit
 
    Foo f(2); // f is direct-initialized:
              // constructor parameter n is copy-initialized from the rvalue 2
              // f.mem is direct-initialized from the parameter n
//  Foo f2 = 2; // error: constructor is explicit
 
    std::cout << s1 << ' ' << s2 << ' ' << *p << ' ' << f.mem  << '\n';
}

```

Output:

```
test aaaaaaaaaa 1 2

```

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
  - initializer list
  - list initialization
  - reference initialization
  - value initialization
  - zero initialization
- move assignment
- move constructor
- `new`
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/direct_initialization&oldid=157684>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 September 2023, at 05:05.