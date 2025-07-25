# Undefined behavior

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

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ASCII | | | | |
| Punctuation | | | | |
| Names and identifiers | | | | |
| Types | | | | |
| Fundamental types | | | | |
| Objects | | | | |
| Scope | | | | |
| Object lifetime | | | | |
| Storage duration and linkage | | | | |
| Definitions and ODR | | | | |
| Name lookup | | | | |
| Qualified name lookup | | | | |
| Unqualified name lookup | | | | |
| The as-if rule | | | | |
| ****Undefined behavior**** | | | | |
| Memory model | | | | |
| Multi-threaded executions and data races (C++11) | | | | |
| Character sets and encodings | | | | |
| Phases of translation | | | | |
| The `main` function | | | | |
| Modules (C++20) | | | | |

Renders the entire program meaningless if certain rules of the language are violated.

### Explanation

The C++ standard precisely defines the observable behavior of every C++ program that does not fall into one of the following classes:

- **ill-formed** - The program has syntax errors or diagnosable semantic errors.

:   - A conforming C++ compiler is required to issue a diagnostic, even if it defines a language extension that assigns meaning to such code (such as with variable-length arrays).
    - The text of the standard uses **shall**, **shall not**, and **ill-formed** to indicate these requirements.

- **ill-formed, no diagnostic required** - The program has semantic errors which may not be diagnosable in general case (e.g. violations of the ODR or other errors that are only detectable at link time).

:   - The behavior is undefined if such program is executed.

- **implementation-defined behavior** - The behavior of the program varies between implementations, and the conforming implementation must document the effects of each behavior.

:   - For example, the type of std::size_t or the number of bits in a byte, or the text of std::bad_alloc::what.
    - A subset of implementation-defined behavior is **locale-specific behavior**, which depends on the implementation-supplied locale.

- **unspecified behavior** - The behavior of the program varies between implementations, and the conforming implementation is not required to document the effects of each behavior.

:   - For example, order of evaluation, whether identical string literals are distinct, the amount of array allocation overhead, etc.
    - Each unspecified behavior results in one of a set of valid results.

|  |  |  |  |
| --- | --- | --- | --- |
| - **erroneous behavior** - The (incorrect) behavior that the implementation is recommended to diagnose.   - Erroneous behavior is always the consequence of incorrect program code. - The evaluation of a constant expression never results in an erroneous behavior. - If the execution contains an operation specified as having erroneous behavior, the implementation is permitted and recommended to issue a diagnostic, and is permitted to terminate the execution at an unspecified time after that operation. - An implementation can issue a diagnostic if it can determine that erroneous behavior is reachable under an implementation-specific set of assumptions about the program behavior, which can result in false positives.   | Examples of erroneous behavior | | --- | | ```text #include <cassert> #include <cstring>   void f() {        int d1, d2;       // d1, d2 have erroneous values     int e1 = d1;      // erroneous behavior     int e2 = d1;      // erroneous behavior     assert(e1 == e2); // holds     assert(e1 == d1); // holds, erroneous behavior     assert(e2 == d1); // holds, erroneous behavior       std::memcpy(&d2, &d1, sizeof(int)); // no erroneous behavior, but                                         // d2 has an erroneous value       assert(e1 == d2); // holds, erroneous behavior     assert(e2 == d2); // holds, erroneous behavior }   unsigned char g(bool b) {     unsigned char c;     // c has erroneous value     unsigned char d = c; // no erroneous behavior, but d has an erroneous value     assert(c == d);      // holds, both integral promotions have erroneous behavior     int e = d;           // erroneous behavior     return b ? d : 0;    // erroneous behavior if b is true } ``` | | (since C++26) |

- **undefined behavior** - There are no restrictions on the behavior of the program.

:   - Some examples of undefined behavior are data races, memory accesses outside of array bounds, signed integer overflow, null pointer dereference, more than one modifications of the same scalar in an expression without any intermediate sequence point(until C++11)that is unsequenced(since C++11), access to an object through a pointer of a different type, etc.
    - Implementations are not required to diagnose undefined behavior (although many simple situations are diagnosed), and the compiled program is not required to do anything meaningful.

|  |  |
| --- | --- |
| - **runtime-undefined behavior** - The behavior that is undefined except when it occurs during the evaluation of an expression as a core constant expression. | (since C++11) |

### UB and optimization

Because correct C++ programs are free of undefined behavior, compilers may produce unexpected results when a program that actually has UB is compiled with optimization enabled:

For example,

#### Signed overflow

```
int foo(int x)
{
    return x + 1 > x; // either true or UB due to signed overflow
}

```

may be compiled as (demo)

```
foo(int):
        mov     eax, 1
        ret

```

#### Access out of bounds

```
int table[4] = {};
bool exists_in_table(int v)
{
    // return true in one of the first 4 iterations or UB due to out-of-bounds access
    for (int i = 0; i <= 4; i++)
        if (table[i] == v)
            return true;
    return false;
}

```

May be compiled as (demo)

```
exists_in_table(int):
        mov     eax, 1
        ret

```

#### Uninitialized scalar

```
std::size_t f(int x)
{
    std::size_t a;
    if (x) // either x nonzero or UB
        a = 42;
    return a;
}

```

May be compiled as (demo)

```
f(int):
        mov     eax, 42
        ret

```

The output shown was observed on an older version of gcc

Run this code

```
#include <cstdio>
 
int main()
{
    bool p; // uninitialized local variable
    if (p)  // UB access to uninitialized scalar
        std::puts("p is true");
    if (!p) // UB access to uninitialized scalar
        std::puts("p is false");
}

```

Possible output:

```
p is true
p is false

```

#### Invalid scalar

```
int f()
{
    bool b = true;
    unsigned char* p = reinterpret_cast<unsigned char*>(&b);
    *p = 10;
    // reading from b is now UB
    return b == 0;
}

```

May be compiled as (demo)

```
f():
        mov     eax, 11
        ret

```

#### Null pointer dereference

The examples demonstrate reading from the result of dereferencing a null pointer.

```
int foo(int* p)
{
    int x = *p;
    if (!p)
        return x; // Either UB above or this branch is never taken
    else
        return 0;
}
 
int bar()
{
    int* p = nullptr;
    return *p; // Unconditional UB
}

```

may be compiled as (demo)

```
foo(int*):
        xor     eax, eax
        ret
bar():
        ret

```

#### Access to pointer passed to std::realloc

Choose clang to observe the output shown

Run this code

```
#include <cstdlib>
#include <iostream>
 
int main()
{
    int* p = (int*)std::malloc(sizeof(int));
    int* q = (int*)std::realloc(p, sizeof(int));
    *p = 1; // UB access to a pointer that was passed to realloc
    *q = 2;
    if (p == q) // UB access to a pointer that was passed to realloc
        std::cout << *p << *q << '\n';
}

```

Possible output:

```
12

```

#### Infinite loop without side-effects

Choose clang or the latest gcc to observe the output shown.

Run this code

```
#include <iostream>
 
bool fermat()
{
    const int max_value = 1000;
 
    // Non-trivial infinite loop with no side effects is UB
    for (int a = 1, b = 1, c = 1; true; )
    {
        if (((a * a * a) == ((b * b * b) + (c * c * c))))
            return true; // disproved :()
        a++;
        if (a > max_value)
        {
            a = 1;
            b++;
        }
        if (b > max_value)
        {
            b = 1;
            c++;
        }
        if (c > max_value)
            c = 1;
    }
 
    return false; // not disproved
}
 
int main()
{
    std::cout << "Fermat's Last Theorem ";
    fermat()
        ? std::cout << "has been disproved!\n"
        : std::cout << "has not been disproved.\n";
}

```

Possible output:

```
Fermat's Last Theorem has been disproved!

```

### Ill-formed with diagnostic message

Note that compilers are permitted to extend the language in ways that give meaning to ill-formed programs. The only thing C++ standard requires in such cases is a diagnostic message (compiler warning), unless the program was "ill-formed no diagnostic required".

For example, unless language extensions are disabled via `--pedantic-errors`, GCC will compile the following example with only a warning even though it appears in the C++ standard as an example of an "error" (see also GCC Bugzilla #55783)

Run this code

```
#include <iostream>
 
// Example tweak, do not use constant
double a{1.0};
 
// C++23 standard, §9.4.5 List-initialization [dcl.init.list], Example #6:
struct S
{
    // no initializer-list constructors
    S(int, double, double); // #1
    S();                    // #2
    // ...
};
 
S s1 = {1, 2, 3.0}; // OK, invoke #1
S s2{a, 2, 3}; // error: narrowing
S s3{}; // OK, invoke #2
// — end example]
 
S::S(int, double, double) {}
S::S() {}
 
int main()
{
    std::cout << "All checks have passed.\n";
}

```

Possible output:

```
main.cpp:17:6: error: type 'double' cannot be narrowed to 'int' in initializer ⮠
list [-Wc++11-narrowing]
S s2{a, 2, 3}; // error: narrowing
     ^
main.cpp:17:6: note: insert an explicit cast to silence this issue
S s2{a, 2, 3}; // error: narrowing
     ^
     static_cast<int>( )
1 error generated.

```

### References

| Extended content |
| --- |
| - C++23 standard (ISO/IEC 14882:2024):   - 3.25 ill-formed program [defns.ill.formed]  - 3.26 implementation-defined behavior [defns.impl.defined]  - 3.66 unspecified behavior [defns.unspecified]  - 3.68 well-formed program [defns.well.formed]   - C++20 standard (ISO/IEC 14882:2020):   - TBD ill-formed program [defns.ill.formed]  - TBD implementation-defined behavior [defns.impl.defined]  - TBD unspecified behavior [defns.unspecified]  - TBD well-formed program [defns.well.formed]   - C++17 standard (ISO/IEC 14882:2017):   - TBD ill-formed program [defns.ill.formed]  - TBD implementation-defined behavior [defns.impl.defined]  - TBD unspecified behavior [defns.unspecified]  - TBD well-formed program [defns.well.formed]   - C++14 standard (ISO/IEC 14882:2014):   - TBD ill-formed program [defns.ill.formed]  - TBD implementation-defined behavior [defns.impl.defined]  - TBD unspecified behavior [defns.unspecified]  - TBD well-formed program [defns.well.formed]   - C++11 standard (ISO/IEC 14882:2011):   - TBD ill-formed program [defns.ill.formed]  - TBD implementation-defined behavior [defns.impl.defined]  - TBD unspecified behavior [defns.unspecified]  - TBD well-formed program [defns.well.formed]   - C++98 standard (ISO/IEC 14882:1998):   - TBD ill-formed program [defns.ill.formed]  - TBD implementation-defined behavior [defns.impl.defined]  - TBD unspecified behavior [defns.unspecified]  - TBD well-formed program [defns.well.formed] |

### See also

|  |  |
| --- | --- |
| `[[assume(expression)]]`(C++23) | specifies that the **expression** will always evaluate to true at a given point (attribute specifier) |
| `[[indeterminate]]`(C++26) | specifies that an object has an indeterminate value if it is not initialized (attribute specifier) |
| unreachable(C++23) | marks unreachable point of execution   (function) |
| C documentation for Undefined behavior | |

### External links

|  |  |
| --- | --- |
| 1. | The LLVM Project Blog: What Every C Programmer Should Know About Undefined Behavior #1/3 |
| 2. | The LLVM Project Blog: What Every C Programmer Should Know About Undefined Behavior #2/3 |
| 3. | The LLVM Project Blog: What Every C Programmer Should Know About Undefined Behavior #3/3 |
| 4. | Undefined behavior can result in time travel (among other things, but time travel is the funkiest) |
| 5. | Understanding Integer Overflow in C/C++ |
| 6. | Fun with NULL pointers, part 1 (local exploit in Linux 2.6.30 caused by UB due to null pointer dereference) |
| 7. | Undefined Behavior and Fermat’s Last Theorem |
| 8. | C++ programmer's guide to undefined behavior |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/ub&oldid=179857>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 January 2025, at 23:24.