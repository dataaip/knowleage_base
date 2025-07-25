# Storage class specifiers

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
| ****Storage duration specifiers**** | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Overview | | | | | | Declaration syntax | | | | | | **decl-specifier-seq** | | | | | | Declarator | | | | | | Conflicting declarations | | | | | | Specifiers | | | | | | typedef | | | | | | inline | | | | | | virtual function specifier | | | | | | explicit function specifier | | | | | | friend | | | | | | constexpr(C++11) | | | | | | consteval(C++20) | | | | | | constinit(C++20) | | | | | | ****Storage class specifiers**** | | | | | | Translation-unit-local (C++20) | | | | | | class/struct | | | | | | union | | | | | | enum | | | | | | decltype(C++11) | | | | | | auto(C++11) | | | | | | alignas(C++11) | | | | | | constvolatile | | | | | | Pack indexing specifier (C++26) | | | | | | Elaborated type specifier | | | | | | Attributes (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Declarators | | | | | | Reference | | | | | | Pointer | | | | | | Array | | | | | | Block declarations | | | | | | Simple-declaration | | | | | | →Structured binding declaration (C++17) | | | | | | Alias declaration (C++11) | | | | | | Namespace alias definition | | | | | | using declaration | | | | | | `using` directive | | | | | | static_assert declaration (C++11) | | | | | | asm declaration | | | | | | Opaque enum declaration (C++11) | | | | | | Other declarations | | | | | | Namespace definition | | | | | | Function declaration | | | | | | Class template declaration | | | | | | Function template declaration | | | | | | Explicit template instantiation (C++11) | | | | | | Explicit template specialization | | | | | | Linkage specification | | | | | | Attribute declaration (C++11) | | | | | | Empty declaration | | | | | |  | | | | | |

The storage class specifiers are a part of the decl-specifier-seq of a name's declaration syntax. Together with the scope of the name, they control two independent properties of the name: its **storage duration** and its **linkage**.

### Storage duration

The **storage duration** is the property of an object that defines the minimum potential lifetime of the storage containing the object. The storage duration is determined by the construct used to create the object and is one of the following:

- static storage duration

|  |  |
| --- | --- |
| - thread storage duration | (since C++11) |

- automatic storage duration
- dynamic storage duration

Static, thread,(since C++11) and automatic storage durations are associated with objects introduced by declarations and with temporary objects. The dynamic storage duration is associated with objects created by a new expression or with implicitly created objects.

The storage duration categories apply to references as well.

The storage duration of subobjects and reference members is that of their complete object.

#### Specifiers

The following keywords are **storage class specifiers** ﻿:

|  |  |
| --- | --- |
| - auto | (until C++11) |
| - register | (until C++17) |

- static

|  |  |
| --- | --- |
| - thread_local | (since C++11) |

- extern
- mutable

In a decl-specifier-seq, there can be at most one storage class specifier, except that thread_local may appear with static or extern(since C++11).

mutable has no effect on storage duration. For its usage, see const/volatile.

Other storage class specifiers can appear in the decl-specifier-seq ﻿s of the following declarations:

| Specifier | Can appear in the decl-specifier-seq ﻿s of | | | | | | | | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Variable declarations | | | | Function declarations | | | Structured binding declarations (since C++17) |
| Non-member | | Member | | Non-member | Member | |
| Non-parameter | Function parameter | Non-static | Static | Non-static | Static |
| auto | Block scope only | Yes | No | No | No | No | No | N/A |
| register | Block scope only | Yes | No | No | No | No | No | N/A |
| static | Yes | No | Declares static | | Namespace scope only | Declares static | | Yes |
| thread_local | Yes | No | No | Yes | No | No | No | Yes |
| extern | Yes | No | No | No | Yes | No | No | No |

Anonymous unions can also be declared with static.

|  |  |
| --- | --- |
| register is a hint that the variable so declared will be heavily used, so that its value can be stored in a CPU register. The hint can be ignored, and in most implementations it will be ignored if the address of the variable is taken. This use is deprecated. | (until C++17) |

#### Static storage duration

A variable satisfying all following conditions has **static storage duration** ﻿:

- It belongs to a namespace scope or are first declared with static or extern.

|  |  |
| --- | --- |
| - It does not have thread storage duration. | (since C++11) |

The storage for these entities lasts for the duration of the program.

|  |  |
| --- | --- |
| Thread storage duration All variables declared with thread_local have **thread storage duration**.  The storage for these entities lasts for the duration of the thread in which they are created. There is a distinct object or reference per thread, and use of the declared name refers to the entity associated with the current thread. | (since C++11) |

#### Automatic storage duration

The following variables have **automatic storage duration** ﻿:

- Variables that belong to a block scope and are not explicitly declared static, thread_local,(since C++11) or extern. The storage for such variables lasts until the block in which they are created exits.
- Variables that belong to a parameter scope (i.e. function parameters). The storage for a function parameter lasts until immediately after its destruction.

#### Dynamic storage duration

Objects created by the following methods during program execution have **dynamic storage duration** ﻿:

- new expressions. The storage for such objects is allocated by allocation functions and deallocated by deallocation functions.
- Implicitly creation by other means. The storage for such objects overlaps with some existing storage.
- Exception objects. The storage for such objects is allocated and deallocated in an unspecified way.

### Linkage

A name can have **external linkage** ﻿, **module linkage**(since C++20), **internal linkage**, or **no linkage**:

- An entity whose name has external linkage can be redeclared in another translation unit, and the redeclaration can be attached to a different module(since C++20).

|  |  |
| --- | --- |
| - An entity whose name has module linkage can be redeclared in another translation unit, as long as the redeclaration is attached to the same module. | (since C++20) |

- An entity whose name has internal linkage can be redeclared in another scope in the same translation unit.
- An entity whose name has no linkage can only be redeclared in the same scope.

The following linkages are recognized:

#### No linkage

Any of the following names declared at block scope have no linkage:

- variables that are not explicitly declared extern (regardless of the static modifier);
- local classes and their member functions;
- other names declared at block scope such as typedefs, enumerations, and enumerators.

Names not specified with external, module,(since C++20) or internal linkage also have no linkage, regardless of which scope they are declared in.

#### Internal linkage

Any of the following names declared at namespace scope have internal linkage:

- variables, variable templates(since C++14), functions, or function templates declared static;
- non-template (since C++14)variables of non-volatile const-qualified type, unless

|  |  |
| --- | --- |
| - they are inline, | (since C++17) |
| - they are declared in the purview of a module interface unit (outside the private module fragment, if any) or module partition, | (since C++20) |

:   - they are explicitly declared extern, or
    - they were previously declared and the prior declaration did not have internal linkage;

- data members of anonymous unions.

|  |  |
| --- | --- |
| In addition, all names declared in unnamed namespaces or a namespace within an unnamed namespace, even ones explicitly declared extern, have internal linkage. | (since C++11) |

#### External linkage

Variables and functions with external linkage also have language linkage, which makes it possible to link translation units written in different programming languages.

Any of the following names declared at namespace scope have external linkage, unless they are declared in an unnamed namespace or their declarations are attached to a named module and are not exported(since C++20):

- variables and functions not listed above (that is, functions not declared static, non-const variables not declared static, and any variables declared extern);
- enumerations;
- names of classes, their member functions, static data members (const or not), nested classes and enumerations, and functions first introduced with friend declarations inside class bodies;
- names of all templates not listed above (that is, not function templates declared static).

Any of the following names first declared at block scope have external linkage:

- names of variables declared extern;
- names of functions.

|  |  |
| --- | --- |
| Module linkage Names declared at namespace scope have module linkage if their declarations are attached to a named module and are not exported, and do not have internal linkage. | (since C++20) |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: add the description of the behavior when an entity is declared with different linkages in the same translation unit (6.6 paragraph 6), note the difference between C++20 (ill-formed) and the current draft (well-formed) |

### Static block variables

Block variables with static or thread(since C++11) storage duration are initialized the first time control passes through their declaration (unless their initialization is zero- or constant-initialization, which can be performed before the block is first entered). On all further calls, the declaration is skipped.

- If the initialization throws an exception, the variable is not considered to be initialized, and initialization will be attempted again the next time control passes through the declaration.
- If the initialization recursively enters the block in which the variable is being initialized, the behavior is undefined.

|  |  |
| --- | --- |
| - If multiple threads attempt to initialize the same static local variable concurrently, the initialization occurs exactly once (similar behavior can be obtained for arbitrary functions with std::call_once).   - Usual implementations of this feature use variants of the double-checked locking pattern, which reduces runtime overhead for already-initialized local statics to a single non-atomic boolean comparison. | (since C++11) |

The destructor for a block variable with static storage duration is called at program exit, but only if the initialization took place successfully.

Variables with static storage duration in all definitions of the same inline function (which may be implicitly inline) all refer to the same object defined in one translation unit, as long as the function has external linkage.

### Translation-unit-local entities

The concept of translation-unit-local entities is standardized in C++20, see this page for more details.

An entity is **translation-unit-local** (or **TU-local** for short) if

- it has a name with internal linkage, or
- it does not have a name with linkage and is introduced within the definition of a TU-local entity, or
- it is a template or template specialization whose template argument or template declaration uses a TU-local entity.

Bad things (usually violation of ODR) can happen if the type of a non-TU-local entity depends on a TU-local entity, or if a declaration of, or a deduction guide for,(since C++17) a non-TU-local entity names a TU-local entity outside its

- function-body for a non-inline function or function template
- initializer for a variable or variable template
- friend declarations in a class definition
- use of value of a variable, if the variable is usable in constant expressions

|  |  |
| --- | --- |
| Such uses are disallowed in a module interface unit (outside its private-module-fragment, if any) or a module partition, and are deprecated in any other context.  A declaration that appears in one translation unit cannot name a TU-local entity declared in another translation unit that is not a header unit. A declaration instantiated for a template appears at the point of instantiation of the specialization. | (since C++20) |

### Notes

Names at the top-level namespace scope (file scope in C) that are const and not extern have external linkage in C, but internal linkage in C++.

Since C++11, auto is no longer a storage class specifier; it is used to indicate type deduction.

|  |  |
| --- | --- |
| In C, the address of a register variable cannot be taken, but in C++, a variable declared register is semantically indistinguishable from a variable declared without any storage class specifiers. | (until C++17) |
| In C++, unlike C, variables cannot be declared register. | (since C++17) |

Names of thread_local variables with internal or external linkage referred from different scopes may refer to the same or to different instances depending on whether the code is executing in the same or in different threads.

The extern keyword can also be used to specify language linkage and explicit template instantiation declarations, but it's not a storage class specifier in those cases (except when a declaration is directly contained in a language linkage specification, in which case the declaration is treated as if it contains the extern specifier).

Storage class specifiers, except for thread_local, are not allowed on explicit specializations and explicit instantiations:

```
template<class T>
struct S
{
    thread_local static int tlm;
};
 
template<>
thread_local int S<float>::tlm = 0; // "static" does not appear here

```

|  |  |
| --- | --- |
| A const (may be implied by constexpr) variable template used to have internal linkage by default, which was inconsistent with other templated entities. Defect report CWG2387 corrected this. | (since C++14) |
| `inline` acts as a workaround for CWG2387 by giving external linkage by default. This is why the inline was added to many variable templates and then removed after having CWG2387 accepted. Standard library implementations also need to use inline as long as a supported compiler has not get CWG2387 implemented. See GCC Bugzilla #109126 and MSVC STL PR #4546. | (since C++17) |

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_threadsafe_static_init` | `200806L` | (C++11) | Dynamic initialization and destruction with concurrency |

### Keywords

auto,
register,
static,
extern,
thread_local,
mutable

### Example

Run this code

```
#include <iostream>
#include <mutex>
#include <string>
#include <thread>
 
thread_local unsigned int rage = 1;
std::mutex cout_mutex;
 
void increase_rage(const std::string& thread_name)
{
    ++rage; // modifying outside a lock is okay; this is a thread-local variable
    std::lock_guard<std::mutex> lock(cout_mutex);
    std::cout << "Rage counter for " << thread_name << ": " << rage << '\n';
}
 
int main()
{
    std::thread a(increase_rage, "a"), b(increase_rage, "b");
 
    {
        std::lock_guard<std::mutex> lock(cout_mutex);
        std::cout << "Rage counter for main: " << rage << '\n';
    }
 
    a.join();
    b.join();
}

```

Possible output:

```
Rage counter for a: 2
Rage counter for main: 1
Rage counter for b: 2

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 216 | C++98 | unnamed class and enumeration in class scope have different linkage from those in namespace scope | they all have external linkage in these scopes |
| CWG 389 | C++98 | a name with no linkage should not be used to declare an entity with linkage | a type without linkage shall not be used as the type of a variable or function with linkage, unless the variable or function has C language linkage |
| CWG 426 | C++98 | an entity could be declared with both internal and external linkage in the same translation unit | the program is ill-formed in this case |
| CWG 527 | C++98 | the type restriction introduced by the resolution of CWG 389 was also applied to variables and functions that cannot be named outside their own translation units | the restriction is lifted for these variables and functions (i.e. with no linkage or internal linkage, or declared within unnamed namespaces) |
| CWG 809 | C++98 | register served very little function | deprecated |
| CWG 1648 | C++11 | static was implied even if thread_local is combined with extern | implied only if no other storage class specifier is present |
| CWG 1686 | C++98 C++11 | the name of a non-static variable declared in namespace scope had internal linkage only if it is explicitly declared const (C++98) or constexpr (C++11) | only required the type to be const-qualified |
| CWG 2019 | C++98 | the storage duration of reference members were unspecified | same as their complete object |
| CWG 2387 | C++14 | unclear whether const-qualified variable template have internal linkage by default | const qualifier does not affect the linkage of variable templates or their instances |
| CWG 2533 | C++98 | the storage duration of implicitly- created objects were unclear | made clear |
| CWG 2850 | C++98 | it was unclear when the storage for function parameters are deallocated | made clear |
| CWG 2872 | C++98 | the meaning of “can be referred to” was unclear | improved wording |
| P2788R0 | C++20 | declaring a const-qualified variable in a namespace gave it internal linkage even in a module unit | internal linkage is not given |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 6.7.5 Storage duration [basic.stc]

- C++20 standard (ISO/IEC 14882:2020):

:   - 6.7.5 Storage duration [basic.stc]

- C++17 standard (ISO/IEC 14882:2017):

:   - 6.7 Storage duration [basic.stc]

- C++14 standard (ISO/IEC 14882:2014):

:   - 3.7 Storage duration [basic.stc]

- C++11 standard (ISO/IEC 14882:2011):

:   - 3.7 Storage duration [basic.stc]

- C++03 standard (ISO/IEC 14882:2003):

:   - 3.7 Storage duration [basic.stc]

- C++98 standard (ISO/IEC 14882:1998):

:   - 3.7 Storage duration [basic.stc]

### See also

|  |  |
| --- | --- |
| C documentation for storage duration | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/storage_duration&oldid=177472>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 November 2024, at 19:44.