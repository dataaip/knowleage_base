# `try` block

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `throw`-expression | | | | | | ****`try` block**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | `catch` handler | | | | | |
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
| while | | | | |
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
| ****try block**** | | | | |
| Transactional memory | | | | |
| `synchronized`, `atomic_commit`, etc (TM TS) | | | | |

 Exceptions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****try block**** | | | | |
| Throwing exceptions | | | | |
| Handling exceptions | | | | |
| Exception specification | | | | |
| noexcept specification (C++11) | | | | |
| dynamic specification (until C++17\*) | | | | |
| noexcept operator (C++11) | | | | |

An exception thrown in a try block can possibly be handled by an associated handler.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `try` compound-statement handler-seq | (1) |  |
|  | | | | | | | | | |
| `try` ctor-initializer ﻿(optional) compound-statement handler-seq | (2) |  |
|  | | | | | | | | | |

1) An ordinary try block.2) A function try block. compound-statement must be the compound statement component of a function body.

|  |  |  |
| --- | --- | --- |
| compound-statement | - | a compound statement |
| handler-seq | - | a non-empty sequence of handlers |
| ctor-initializer | - | member initializer list (for constructors only) |

### Ordinary try block

An ordinary try block is a statement.

If an exception is thrown from its compound-statement, the exception will be matched against the handlers in its handler-seq ﻿:

```
void f()
{
    throw 1;     // NOT handled by the handler below
    try
    {
        throw 2; // handled by the associated handler
    }
    catch (...)
    {
        // handles the exception 2
    }
    throw 3;     // NOT handled by the handler above
}

```

### Function try block

A function try block is a special kind of function body.

If an exception is thrown from its compound-statement or ctor-initializer (if any), the exception will be matched against the handlers in its handler-seq ﻿:

```
int f(bool cond)
{
    if (cond)
        throw 1;
    return 0;
}
 
struct X
{
    int mem;
 
    X() try : mem(f(true)) {}
    catch (...)
    {
        // handles the exception 1
    }
 
    X(int) try
    {
        throw 2;
    }
    catch (...)
    {
        // handles the exception 2
    }
};

```

Exceptions thrown in destructors of objects with static storage duration or in constructors of objects associated with non-block variables with static storage duration are not caught by a function try block on the main function.

|  |  |
| --- | --- |
| Exceptions thrown in destructors of objects with thread storage duration or in constructors of objects associated with non-block variables with thread storage duration are not caught by a function try block on the initial function of the thread. | (since C++11) |

Flowing off the end of the compound-statement of a handler of a function try block is equivalent to flowing off the end of the compound-statement of that function try block, unless the function is a constructor or destructor (see below).

#### Constructor and destructor try block

For a class `C`, if the function body of its constuctor or destructor definition is a function try block, and an exception is thrown during the initialization or destruction, respectively, of `C`’s subobjects, the exception will also be matched against the handlers in the handler-seq ﻿ of the function try block:

```
int f(bool cond = true)
{
    if (cond)
        throw 1;
    return 0;
}
 
struct X
{
    int mem = f();
 
    ~X()
    {
        throw 2;
    }
};
 
struct Y
{
    X mem;
 
    Y() try {}
    catch (...)
    {
        // handles the exception 1
    }
 
    ~Y() try {}
    catch (...)
    {
        // handles the exception 2
    }
};

```

Referring to any non-static member or base class of an object in the handler for a function try block of a constructor or destructor for that object results in undefined behavior.

If a return statement appears in a handler of the function try block of a constructor, the program is ill-formed.

The currently handled exception is rethrown if control reaches the end of a handler of the function try block of a constructor or destructor.

### Control flow

The compound-statement of a try block is a control-flow-limited statement:

```
void f()
{
    goto label;     // error
    try
    {
        goto label; // OK
        label: ;
    }
    catch (...)
    {
        goto label; // error
    }
}

```

A jump statement (`goto`, `break`, `return`, `continue`) can be used to transfer control out of a try block (including its handlers). When this happens, each variable declared in the try block will be destroyed in the context that directly contains its declaration:

```
try
{
    T1 t1;
    try
    {
        T2 t2;
        goto label; // destroy t2 first, then t1
    }
    catch(...)
    {
        // executed if an exception is thrown while destroying t2
    }
}
catch(...)
{
    // executed if an exception is thrown while destroying t1
}
label: ;

```

### Keywords

try

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 98 | C++98 | a switch statement can transfer control into the compound-statement of a try block | prohibited |
| CWG 1167 | C++98 | it was unspecified whether a function try block on a destructor will catch exceptions from a base or member destructor | such exceptions are caught |

### See also

- Throwing exceptions
- Handling exceptions
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/try&oldid=176509>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 September 2024, at 01:55.