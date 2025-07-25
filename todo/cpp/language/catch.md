# Handling exceptions

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `throw`-expression | | | | | | `try` block | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | ****`catch` handler**** | | | | | |
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

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | Constant expressions | | | | | | Primary expressions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lambda expressions (C++11) | | | | | | Requires expressions (C++20) | | | | | | Pack indexing expression (C++26) | | | | | | Potentially-evaluated expressions | | | | | |
| Literals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integer literals | | | | | | Floating-point literals | | | | | | Boolean literals | | | | | | Character literals | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Escape sequences | | | | | | String literals | | | | | | Null pointer literal (C++11) | | | | | | User-defined literal (C++11) | | | | | |
| Operators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

 Exceptions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| try block | | | | |
| Throwing exceptions | | | | |
| ****Handling exceptions**** | | | | |
| Exception specification | | | | |
| noexcept specification (C++11) | | | | |
| dynamic specification (until C++17\*) | | | | |
| noexcept operator (C++11) | | | | |

An exception can be handled by a handler.

### Handler

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `catch` `(` attr ﻿(optional) type-specifier-seq declarator `)` compound-statement | (1) |  |
|  | | | | | | | | | |
| `catch` `(` attr ﻿(optional) type-specifier-seq abstract-declarator ﻿(optional) `)` compound-statement | (2) |  |
|  | | | | | | | | | |
| `catch` `(` `...` `)` compound-statement | (3) |  |
|  | | | | | | | | | |

1) A handler with a named parameter.2) A handler with an unnamed parameter.3) A handler matching all kinds of exceptions.

|  |  |  |
| --- | --- | --- |
| attr | - | (since C++11) any number of attributes, applies to the parameter |
| type-specifier-seq | - | part of a formal parameter declaration, same as in a function parameter list |
| declarator | - | part of a parameter declaration, same as in a function parameter list |
| abstract-declarator | - | part of an unnamed parameter declaration, same as in function parameter list |
| compound-statement | - | a compound statement |

The parameter declaration in a handler describes the type(s) of exceptions that can cause that handler to be entered.

If the parameter is declared to have one of the following types, the program is ill-formed:

- an incomplete type
- an abstract class type

|  |  |
| --- | --- |
| - an rvalue reference type | (since C++11) |

- a pointer to an incomplete type other than (possibly cv-qualified) void
- an lvalue reference to an incomplete type

If the parameter is declared to have type “array of `T`” or function type `T`, the type is adjusted to “pointer to `T`”.

A handler with parameter type `T` can be abbreviated as “a handler of type `T`”.

### Matching exceptions

Each try block associates with a number of handlers, these handlers form a handler sequence. When an exception is thrown from a try block, the handlers in the sequence are tried in order of appearance to match the exception.

A handler is a match for an exception object of type `E` if any of the following conditions is satisfied:

- The handler is of type “possibly cv-qualified `T`” or “lvalue reference to possibly cv-qualified `T`”, and any of the following conditions is satisfied:

:   - `E` and `T` are the same type (ignoring the top-level cv-qualifiers).
    - `T` is an unambiguous public base class of `E`.

- The handler is of type “possibly cv-qualified `T`” or const T& where `T` is a pointer or pointer-to-member type, and any of the following conditions is satisfied:

:   - `E` is a pointer or pointer-to-member type that can be converted to `T` by at least one of the following conversions:

    :   - A standard pointer conversion not involving conversions to pointers to private or protected or ambiguous classes.

|  |  |
| --- | --- |
| - A function pointer conversion. | (since C++17) |

:   :   - A qualification conversion.

|  |  |
| --- | --- |
| - `E` is std::nullptr_t. | (since C++11) |

The catch (...) handler matches exceptions of any type. If present, it can only be the last handler in a handler sequence. This handler may be used to ensure that no uncaught exceptions can possibly escape from a function that offers nothrow exception guarantee.

```
try
{
    f();
}
catch (const std::overflow_error& e)
{} // this executes if f() throws std::overflow_error (same type rule)
catch (const std::runtime_error& e)
{} // this executes if f() throws std::underflow_error (base class rule)
catch (const std::exception& e)
{} // this executes if f() throws std::logic_error (base class rule)
catch (...)
{} // this executes if f() throws std::string or int or any other unrelated type

```

If no match is found among the handlers for a try block, the search for a matching handler continues in a dynamically surrounding try block of the same thread(since C++11).

If no matching handler is found, std::terminate is invoked; whether or not the stack is unwound before this invocation of std::terminate is implementation-defined.

### Handling exceptions

When an exception is thrown, control is transferred to the nearest handler with a matching type; “nearest” means the handler for which the compound statement or the member initializer list (if present) following the try keyword was most recently entered by the thread of control and not yet exited.

#### Initializing the handler parameter

The parameter declared in the parameter list (if any), of type “possibly cv-qualified `T`” or “lvalue reference to possibly cv-qualified `T`”, is initialized from the exception object, of type `E`, as follows:

- If `T` is a base class of `E`, the parameter is copy-initialized from an lvalue of type `T` designating the corresponding base class subobject of the exception object.
- Otherwise, the parameter is copy-initialized from an lvalue of type `E` designating the exception object.

The lifetime of the parameter ends when the handler exits, after the destruction of any objects with automatic storage duration initialized within the handler.

When the parameter is declared as an object, any changes to that object will not affect the exception object.

When the parameter is declared as a reference to an object, any changes to the referenced object are changes to the exception object and will have effect should that object be rethrown.

#### Activating the handler

A handler is considered **active** when initialization is complete for the parameter (if any) of the handler.

Also, an implicit handler is considered active when std::terminate is entered due to a throw.

A handler is no longer considered active when the handler exits.

The exception with the most recently activated handler that is still active is called the **currently handled exception**. Such an exception can be rethrown.

### Control flow

The compound-statement of a handler is a control-flow-limited statement:

```
void f()
{
    goto label;     // error
    try
    {
        goto label; // error
    }
    catch (...)
    {
        goto label: // OK
        label: ;
    }
}

```

### Notes

Stack unwinding occurs while control is transferring to a handler. When a handler becomes active, stack unwinding is already completed.

The exception thrown by the throw expression throw 0 does not match a handler of pointer or pointer-to-member type.

|  |  |
| --- | --- |
| - throw nullptr can be used instead to throw a null pointer that matches such handlers. | (since C++11) |

Exception objects can never have array or function types, therefore a handler of reference to array or function type is never a match for any exception object.

It is possible to write handlers that can never be executed, for example by placing a handler for a final derived class after a handler for a corresponding unambiguous public base class:

```
try
{
    f();
}
catch (const std::exception& e)
{} // will be executed if f() throws std::runtime_error
catch (const std::runtime_error& e)
{} // dead code!

```

Many implementations overly extend the resolution of CWG issue 388 to handlers of reference to non-const pointer types:

```
int i;
try
{
    try
    {
        throw static_cast<float*>(nullptr);
    }
    catch (void*& pv)
    {
        pv = &i;
        throw;
    }
}
catch (const float* pf)
{
    assert(pf == nullptr); // should pass, but fails on MSVC and Clang
}

```

### Keywords

catch

### Example

The following example demonstrates several usage cases of the handlers:

Run this code

```
#include <iostream>
#include <vector>
 
int main()
{
    try
    {
        std::cout << "Throwing an integer exception...\n";
        throw 42;
    }
    catch (int i)
    {
        std::cout << " the integer exception was caught, with value: " << i << '\n';
    }
 
    try
    {
        std::cout << "Creating a vector of size 5... \n";
        std::vector<int> v(5);
        std::cout << "Accessing the 11th element of the vector...\n";
        std::cout << v.at(10); // vector::at() throws std::out_of_range
    }
    catch (const std::exception& e) // caught by reference to base
    {
        std::cout << " a standard exception was caught, with message: '"
                  << e.what() << "'\n";
    }
}

```

Possible output:

```
Throwing an integer exception...
 the integer exception was caught, with value: 42
Creating a vector of size 5...
Accessing the 11th element of the vector...
 a standard exception was caught, with message: 'out_of_range'

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 98 | C++98 | a switch statement can transfer control into a handler | prohibited |
| CWG 210 | C++98 | throw expressions were matched against the handlers | exception objects are matched against the handlers |
| CWG 388 | C++98 | an exception of pointer or pointer to member type could not be matched by a const reference to a different type | made matchable when convertible |
| CWG 1166 | C++98 | the behavior was unspecified when a handler whose type is a reference to an abstract class type is matched | abstract class types are not allowed for handlers |
| CWG 1769 | C++98 | when the type of the handler is a base of the type of the exception object, a converting constructor might be used for the initialization of the handler parameter | the parameter is copy-initialized from the corresponding base class subobject of the exception object |
| CWG 2093 | C++98 | an exception object of pointer to object type could not match a handler of pointer to object type through qualification conversion | allowed |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 14.4 Handling an exception [except.handle]

- C++20 standard (ISO/IEC 14882:2020):

:   - 14.4 Handling an exception [except.handle]

- C++17 standard (ISO/IEC 14882:2017):

:   - 18.3 Handling an exception [except.handle]

- C++14 standard (ISO/IEC 14882:2014):

:   - 15.3 Handling an exception [except.handle]

- C++11 standard (ISO/IEC 14882:2011):

:   - 15.3 Handling an exception [except.handle]

- C++03 standard (ISO/IEC 14882:2003):

:   - 15.3 Handling an exception [except.handle]

- C++98 standard (ISO/IEC 14882:1998):

:   - 15.3 Handling an exception [except.handle]

### See also

- try block
- Throwing exceptions
- Exception handling
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/catch&oldid=176679>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 October 2024, at 08:50.