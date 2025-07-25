# Main function

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
| Undefined behavior | | | | |
| Memory model | | | | |
| Multi-threaded executions and data races (C++11) | | | | |
| Character sets and encodings | | | | |
| Phases of translation | | | | |
| ****The `main` function**** | | | | |
| Modules (C++20) | | | | |

A program shall contain a global function named main, which is the designated start of the program in hosted environment. It shall have one of the following forms:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| int `main() {` body `}` | (1) |  |
|  | | | | | | | | | |
| int `main(`int argc`,` char\* argv`[]``) {` body `}` | (2) |  |
|  | | | | | | | | | |
| int `main(`/\* implementation-defined \*/`) {` body `}` | (3) |  |
|  | | | | | | | | | |

1) A `main` function running independently of environment-provided arguments.2) A `main` function accepting environment-provided arguments. The names of argc and argv are arbitrary, as well as the representation of the types of the parameters: int main(int ac, char\*\* av) is equally valid.3) A `main` function of implement-defined type, returning int. The C++ standard recommends implementation-defined `main` functions to place the extra (optional) parameters after argv.

|  |  |  |
| --- | --- | --- |
| argc | - | Non-negative value representing the number of arguments passed to the program from the environment in which the program is run. |
| argv | - | Pointer to the first element of an array of argc + 1 pointers, of which the last one is null and the previous ones, if any, point to null-terminated multibyte strings that represent the arguments passed to the program from the execution environment. If argv[0] is not a null pointer (or, equivalently, if argc > 0), it points to a string that represents the name used to invoke the program, or to an empty string. |
| body | - | The body of the `main` function. |

### Explanation

The `main` function is called at program startup after initialization of the non-local objects with static storage duration. It is the designated entry point to a program that is executed in **hosted** environment (that is, with an operating system). The entry points to **freestanding** programs (boot loaders, OS kernels, etc) are implementation-defined.

The parameters of the two-parameter form of the `main` function allow arbitrary multibyte character strings to be passed from the execution environment (these are typically known as **command line arguments**), the pointers argv[1] .. argv[argc - 1] point at the first characters in each of these strings. argv[0] (if non-null) is the pointer to the initial character of a null-terminated multibyte string that represents the name used to invoke the program itself (or an empty string "" if this is not supported by the execution environment). The strings are modifiable, although these modifications do not propagate back to the execution environment: they can be used, for example, with std::strtok. The size of the array pointed to by argv is at least argc + 1, and the last element, argv[argc], is guaranteed to be a null pointer.

The `main` function has the following several special properties:

1) The body of the `main` function does not need to contain the return statement: if control reaches the end of `main` without encountering a return statement, the effect is that of executing return 0;.2) Execution of the return (or the implicit return upon reaching the end of `main`) is equivalent to first leaving the function normally (which destroys the objects with automatic storage duration) and then calling std::exit with the same argument as the argument of the return (std::exit then destroys static objects and terminates the program).

The `main` function has several restrictions (violation of which renders the program ill-formed):

1) It cannot be named anywhere in the programa) in particular, it cannot be called recursivelyb) its address cannot be takenc) it cannot be used in a `typeid` expression or a `decltype`-specifier(since C++11)2) It cannot be predefined and cannot be overloaded: effectively, the name `main` in the global namespace is reserved for functions (although it can be used to name classes, namespaces, enumerations, and any entity in a non-global namespace, except that an entity named `main` cannot be declared with C language linkage in any namespace.3) It cannot be defined as deleted or(since C++11) declared with any language linkage, `constexpr`(since C++11), `consteval`(since C++20), `inline`, or `static`.

|  |  |
| --- | --- |
| 4) The return type of the `main` function cannot be deduced (auto main() {...} is not allowed). | (since C++14) |

|  |  |
| --- | --- |
| 5) The `main` function cannot be a coroutine. | (since C++20) |

|  |  |
| --- | --- |
| 6) The `main` function cannot attach to a named module. | (since C++20) |

### Notes

If the `main` function is defined with a function try block, the exceptions thrown by the destructors of static objects (which are destroyed by the implied std::exit) are not caught by it.

The manner in which the arguments given at the OS command line are converted into the multibyte character arrays referenced by argv may involve implementation-defined processing:

- Parsing C++ Command-Line Arguments MSDN
- Shell Introduction POSIX

A very common implementation-defined form of main() has a third argument (in addition to `argc` and `argv`), of type char\*\*, pointing at an array of pointers to the execution environment variables.

### Example

Demonstrates how to inform a program about where to find its input and where to write its results.  
A possible invocation: ./convert table_in.dat table_out.dat

Run this code

```
#include <cstdlib>
#include <iomanip>
#include <iostream>
 
int main(int argc, char *argv[])
{
    std::cout << "argc == " << argc << '\n';
 
    for (int ndx{}; ndx != argc; ++ndx)
        std::cout << "argv[" << ndx << "] == " << std::quoted(argv[ndx]) << '\n';
    std::cout << "argv[" << argc << "] == "
              << static_cast<void*>(argv[argc]) << '\n';
 
    /* ... */
 
    return argc == 3 ? EXIT_SUCCESS : EXIT_FAILURE; // optional return value
}

```

Possible output:

```
argc == 3
argv[0] == "./convert"
argv[1] == "table_in.dat"
argv[2] == "table_out.dat"
argv[3] == 0

```

### References

| Extended content |
| --- |
| - C++23 standard (ISO/IEC 14882:2024):   - 6.9.3.1 main function [basic.start.main] |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1003 | C++98 | supported parameter names of `main` were overly restricted | all valid parameter names are supported |
| CWG 1886 | C++98 | the `main` function could be declared with a language linkage | prohibited |
| CWG 2479 | C++20 | the `main` function could be declared consteval | prohibited |
| CWG 2811 | C++98 | whether the `main` function is used after N3214 was unclear | it is considered used when named |

### See also

|  |  |
| --- | --- |
| C documentation for `main` function | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/main_function&oldid=172278>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 6 June 2024, at 22:14.