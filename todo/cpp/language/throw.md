# Throwing exceptions

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****`throw`-expression**** | | | | | | `try` block | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | `catch` handler | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | ****`throw`-expression**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

 Exceptions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| try block | | | | |
| ****Throwing exceptions**** | | | | |
| Handling exceptions | | | | |
| Exception specification | | | | |
| noexcept specification (C++11) | | | | |
| dynamic specification (until C++17\*) | | | | |
| noexcept operator (C++11) | | | | |

Throwing an exception transfers control to a handler.

An exception can be thrown from throw expressions, the following contexts may also throw exceptions:

- allocation functions
- `dynamic_cast`
- `typeid`
- new expressions
- standard library functions

### Exception object

Throwing an exception initializes an object with dynamic storage duration, called the **exception object**.

If the type of the exception object would be one of the following types, the program is ill-formed:

- an incomplete type
- an abstract class type
- a pointer to an incomplete type other than (possibly cv-qualified) void

#### Constructing and destructing exception objects

Given the type of the exception object as `T`:

- Let obj be an lvalue of type const T, the copy-initialization of an object of type `T` from obj must be well-formed.
- If `T` is a class type:

:   - The selected constructor is odr-used.
    - The destructor of `T` is potentially invoked.

The memory for the exception object is allocated in an unspecified way. The only guarantee is that the storage will never be allocated by global allocation functions.

If a handler exits by rethrowing, control is passed to another handler for the same exception object. The exception object is not destructed in this case.

|  |  |
| --- | --- |
| When the last remaining active handler for the exception exits by any means other than rethrowing, the exception object is destroyed and the implementation may deallocate the memory for the temporary object in an unspecified way.  The destruction occurs immediately after the destruction of the object declared in the “parameter list” in the handler. | (until C++11) |
| The points of potential destruction for the exception object are:   - When an active handler for the exception exits by any means other than rethrowing, immediately after the destruction of the object (if any) declared in the “parameter list” in the handler. - When an object of type std::exception_ptr that refers to the exception object is destroyed, before the destructor of std::exception_ptr returns.   Among all points of potential destruction for the exception object, there is an unspecified last one where the exception object is destroyed. All other points happen before that last one. The implementation may then deallocate the memory for the exception object in an unspecified way. | (since C++11) |

### throw expressions

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `throw` expression | (1) |  |
|  | | | | | | | | | |
| `throw` | (2) |  |
|  | | | | | | | | | |

1) Throws a new exception.2) Rethrows the exception currently being handled.

|  |  |  |
| --- | --- | --- |
| expression | - | the expression used to construct the exception object |

When a new exception is thrown, its exception object is determined as follows:

1. The array-to-pointer and function-to-pointer standard conversions are performed on expression ﻿.
2. Let ex be the conversion result:

:   :   - The type of the exception object is determined by removing any top-level cv-qualifiers from the type of ex.
        - The exception object is copy-initialized from ex.

If a program attempts to rethrow an exception when no exception is presently being handled, std::terminate will be invoked. Otherwise, the exception is reactivated with the existing exception object (no new exception object is created), and the exception is no longer
considered to be caught.

```
try
{
    // throwing a new exception 123
    throw 123;
}
catch (...) // catch all exceptions
{
    // respond (partially) to exception 123
    throw; // pass the exception to some other handler
}

```

### Stack unwinding

Once the exception object is constructed, the control flow works backwards (up the call stack) until it reaches the start of a try block, at which point the parameters of all associated handlers are compared, in order of appearance, with the type of the exception object to find a match. If no match is found, the control flow continues to unwind the stack until the next try block, and so on. If a match is found, the control flow jumps to the matching handler.

As the control flow moves up the call stack, destructors are invoked for all objects with automatic storage duration that are constructed, but not yet destroyed, since the corresponding try block was entered, in reverse order of completion of their constructors. If an exception is thrown from a destructor of a local variable or of a temporary used in a return statement, the destructor for the object returned from the function is also invoked.

If an exception is thrown from a constructor or (rare) from a destructor of an object (regardless of the object's storage duration), destructors are called for all fully-constructed non-static non-variant members and base classes, in reverse order of completion of their constructors. Variant members of union-like classes are only destroyed in the case of unwinding from constructor, and if the active member changed between initialization and destruction, the behavior is undefined.

|  |  |
| --- | --- |
| If a delegating constructor exits with an exception after the non-delegating constructor successfully completed, the destructor for this object is called. | (since C++11) |

If the exception is thrown from a constructor that is invoked by a new-expression, the matching deallocation function is called, if available.

This process is called **stack unwinding**.

If any function that is called directly by the stack unwinding mechanism, after initialization of the exception object and before the start of the exception handler, exits with an exception, std::terminate is called. Such functions include destructors of objects with automatic storage duration whose scopes are exited, and the copy constructor of the exception object that is called (if not elided) to initialize catch-by-value arguments.

If an exception is thrown and not caught, including exceptions that escape the initial function of std::thread, the main function, and the constructor or destructor of any static or thread-local objects, then std::terminate is called. It is implementation-defined whether any stack unwinding takes place for uncaught exceptions.

### Notes

When rethrowing exceptions, the second form must be used to avoid object slicing in the (typical) case where exception objects use inheritance:

```
try
{
    std::string("abc").substr(10); // throws std::out_of_range
}
catch (const std::exception& e)
{
    std::cout << e.what() << '\n';
//  throw e; // copy-initializes a new exception object of type std::exception
    throw;   // rethrows the exception object of type std::out_of_range
}

```

The throw-expression is classified as prvalue expression of type void. Like any other expression, it may be a sub-expression in another expression, most commonly in the conditional operator:

```
double f(double d)
{
    return d > 1e7 ? throw std::overflow_error("too big") : d;
}
 
int main()
{
    try
    {
        std::cout << f(1e10) << '\n';
    }
    catch (const std::overflow_error& e)
    {
        std::cout << e.what() << '\n';
    }
}

```

### Keywords

throw

### Example

Run this code

```
#include <iostream>
#include <stdexcept>
 
struct A
{
    int n;
 
    A(int n = 0): n(n) { std::cout << "A(" << n << ") constructed successfully\n"; }
    ~A() { std::cout << "A(" << n << ") destroyed\n"; }
};
 
int foo()
{
    throw std::runtime_error("error");
}
 
struct B
{
    A a1, a2, a3;
 
    B() try : a1(1), a2(foo()), a3(3)
    {
        std::cout << "B constructed successfully\n";
    }
    catch(...)
    {
        std::cout << "B::B() exiting with exception\n";
    }
 
    ~B() { std::cout << "B destroyed\n"; }
};
 
struct C : A, B
{
    C() try
    {
        std::cout << "C::C() completed successfully\n";
    }
    catch(...)
    {
        std::cout << "C::C() exiting with exception\n";
    }
 
    ~C() { std::cout << "C destroyed\n"; }
};
 
int main () try
{
    // creates the A base subobject
    // creates the a1 member of B
    // fails to create the a2 member of B
    // unwinding destroys the a1 member of B
    // unwinding destroys the A base subobject
    C c;
}
catch (const std::exception& e)
{
    std::cout << "main() failed to create C with: " << e.what();
}

```

Output:

```
A(0) constructed successfully
A(1) constructed successfully
A(1) destroyed
B::B() exiting with exception
A(0) destroyed
C::C() exiting with exception
main() failed to create C with: error

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 499 | C++98 | an array with unknown bound could not be thrown because its type is incomplete, but an exception object can be created from the decayed pointer without any problem | apply the type completion requirement to the exception object instead |
| CWG 668 | C++98 | std::terminate was not called if an exception is thrown from the destructor of a local non-automatic object | call std::terminate in this case |
| CWG 1863 | C++11 | copy constructor was not required for move-only exception objects when thrown, but copying allowed later | copy constructor required |
| CWG 1866 | C++98 | variant members were leaked on stack unwinding from constructor | variant members destroyed |
| CWG 2176 | C++98 | throw from a local variable destructor could skip return value destructor | function return value added to unwinding |
| CWG 2699 | C++98 | throw "EX" would actually throw char\* rather than const char\* | corrected |
| CWG 2711 | C++98 | the source of the copy-initialization of the exception object was not specified | copy-initialized from expression |
| CWG 2775 | C++98 | the exception object copy-initialization requirement was unclear | made clear |
| CWG 2854 | C++98 | the storage duration of exception objects was unclear | made clear |
| P1825R0 | C++11 | implicit move from parameters was forbidden in `throw` | allowed |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 7.6.18 Throwing an exception [expr.throw]

:   - 14.2 Throwing an exception [except.throw]

- C++20 standard (ISO/IEC 14882:2020):

:   - 7.6.18 Throwing an exception [expr.throw]

:   - 14.2 Throwing an exception [except.throw]

- C++17 standard (ISO/IEC 14882:2017):

:   - 8.17 Throwing an exception [expr.throw]

:   - 18.1 Throwing an exception [except.throw]

- C++14 standard (ISO/IEC 14882:2014):

:   - 15.1 Throwing an exception [except.throw]

- C++11 standard (ISO/IEC 14882:2011):

:   - 15.1 Throwing an exception [except.throw]

- C++03 standard (ISO/IEC 14882:2003):

:   - 15.1 Throwing an exception [except.throw]

- C++98 standard (ISO/IEC 14882:1998):

:   - 15.1 Throwing an exception [except.throw]

### See also

- copy elision
- try block
- handler
- noexcept specifier
- Exception handling

|  |  |
| --- | --- |
| - dynamic exception specifications | (until C++17) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/throw&oldid=176676>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 October 2024, at 07:16.