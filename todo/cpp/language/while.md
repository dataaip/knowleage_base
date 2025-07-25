# `while` loop

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | for | | | | | | range-`for` (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****while**** | | | | | | `do-while` | | | | | |
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

 Statements

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Labels | | | | |
| label : statement | | | | |
| Expression statements | | | | |
| expression ; | | | | |
| Compound statements | | | | |
| `{` statement... `}` | | | | |
| Selection statements | | | | |
| if | | | | |
| switch | | | | |
| Iteration statements | | | | |
| ****while**** | | | | |
| do while | | | | |
| for | | | | |
| range for (C++11) | | | | |
| Jump statements | | | | |
| break | | | | |
| continue | | | | |
| return | | | | |
| goto | | | | |
| Declaration statements | | | | |
| declaration ; | | | | |
| Try blocks | | | | |
| try block | | | | |
| Transactional memory | | | | |
| `synchronized`, `atomic_commit`, etc (TM TS) | | | | |

Conditionally executes a statement repeatedly.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr ﻿(optional) `while (` condition `)` statement |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| attr | - | (since C++11) any number of attributes |
| condition | - | a condition |
| statement | - | a statement (typically a compound statement) |

### Condition

A condition can either be an expression or a simple declaration.

|  |  |
| --- | --- |
| - If it can be syntactically resolved as a structured binding declaration, it is interpreted as a structured binding declaration. | (since C++26) |

- If it can be syntactically resolved as an expression, it is treated as an expression. Otherwise, it is treated as a declaration that is not a structured binding declaration(since C++26).

When control reaches condition, the condition will yield a value, which is used to determine whether statement will be executed.

#### Expression

If condition is an expression, the value it yields is the the value of the expression contextually converted to bool. If that conversion is ill-formed, the program is ill-formed.

#### Declaration

If condition is a simple declaration, the value it yields is the value of the decision variable (see below) contextually converted to bool. If that conversion is ill-formed, the program is ill-formed.

##### Non-structured binding declaration

The declaration has the following restrictions:

- Syntactically conforms to the following form:

|  |  |
| --- | --- |
| - type-specifier-seq declarator `=` assignment-expression | (until C++11) |
| - attribute-specifier-seq(optional) decl-specifier-seq declarator brace-or-equal-initializer | (since C++11) |

- The declarator cannot specify a function or an array.
- The type specifier sequence(until C++11)declaration specifier sequence can only contain type specifiers and constexpr, and it(since C++11) cannot define a class or enumeration.

The decision variable of the declaration is the declared variable.

|  |  |
| --- | --- |
| Structured binding declaration The declaration has the following restrictions:   - The expression in its initializer cannot be of an array type. - The declaration specifier sequence can only contain type specifiers and constexpr.   The decision variable of the declaration is the invented variable e introduced by the declaration. | (since C++26) |

### Explanation

A while statement is equivalent to

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| /\* label \*/ `:`  `{`  `if (` condition `)`  `{`  statement  `goto` /\* label \*/ `;`  `}`  `}` |  |  |
|  | | | | | | | | | |

If condition is a declaration, the variable it declares is destroyed and created with each iteration of the loop.

If the loop needs to be terminated within statement, a break statement can be used as terminating statement.

If the current iteration needs to be terminated within statement, a continue statement can be used as shortcut.

### Notes

Regardless of whether statement is a compound statement, it always introduces a block scope. Variables declared in it are only visible in the loop body, in other words,

```
while (--x >= 0)
    int i;
// i goes out of scope

```

is the same as

```
while (--x >= 0)
{
    int i;
} // i goes out of scope

```

As part of the C++ forward progress guarantee, the behavior is undefined if a loop that is not a trivial infinite loop(since C++26) without observable behavior does not terminate. Compilers are permitted to remove such loops.

### Keywords

while

### Example

Run this code

```
#include <iostream>
 
int main()
{
    // while loop with a single statement
    int i = 0;
    while (i < 10)
         i++;
    std::cout << i << '\n';
 
    // while loop with a compound statement
    int j = 2;
    while (j < 9)
    {
        std::cout << j << ' ';
        j += 2;
    }
    std::cout << '\n';
 
    // while loop with a declaration condition
    char cstr[] = "Hello";
    int k = 0;
    while (char c = cstr[k++])
        std::cout << c;
    std::cout << '\n';
}

```

Output:

```
10
2 4 6 8
Hello

```

### See also

|  |  |
| --- | --- |
| C documentation for while | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/while&oldid=173813>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 July 2024, at 00:06.