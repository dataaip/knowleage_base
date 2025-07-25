# Address of an overloaded function

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

 Functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Declarations | | | | |
| Function declaration | | | | |
| Function parameter list | | | | |
| Function definition | | | | |
| Default arguments | | | | |
| Variadic arguments | | | | |
| `inline` specifier | | | | |
| Lambda expressions (C++11) | | | | |
| Coroutines (C++20) | | | | |
| Function calls | | | | |
| Argument-Dependent Lookup (ADL) | | | | |
| Function-call operator | | | | |
| Function objects | | | | |
| Overloading | | | | |
| Overload resolution | | | | |
| Operator overloading | | | | |
| ****Address of an overload set**** | | | | |

Besides function-call expressions, where overload resolution takes place, the name of an overloaded function may appear in the following 7 contexts:

| Context | Target |
| --- | --- |
| initializer in a declaration of an object or reference | the object or reference being initialized |
| on the right-hand-side of an assignment expression | the left-hand side of the assignment |
| as a function call argument | the function parameter |
| as a user-defined operator argument | the operator parameter |
| the `return` statement | the return value of a function or conversion |
| explicit cast or `static_cast` argument | the corresponding cast |
| non-type template argument | the corresponding template parameter |

In each context, the name of an overloaded function may be preceded by address-of operator `&` and may be enclosed in a redundant set of parentheses.

|  |  |
| --- | --- |
| If the target type contains a placeholder type, placeholder type deduction is performed, and the following description uses the deduced type as target type. | (since C++26) |

### Selecting functions

When the address of an overloaded function is taken, a set `S` of functions is selected from the overload set referred to by the name of the overload function:

- If there is no target, all non-template functions named are selected.
- Otherwise, a non-template function with type `F` is selected for the function type `FT` of the target type if `F` (after possibly applying the function pointer conversion)(since C++17) is identical to `FT`.[[1]](overloaded_address.html#cite_note-1)
- The specialization (if any) generated by template argument deduction for each function template named is also added to `S`.

If the target is of function pointer type or reference to function type, `S` can only include non-member functions, explicit object member functions(since C++23) and static member functions. If the target is of pointer-to-member-function type, `S` can only include implicit object member functions.

1. ↑ In other words, the class of which the function is a member is ignored if the target type is a pointer-to-member-function type.

### Eliminating functions

After forming the set `S`, functions are elimiated in the following order:

|  |  |
| --- | --- |
| - All functions with associated constraints that are not satisfied are eliminated from the `S`. | (since C++20) |

- If more than one function in `S` remains, all function template specializations in `S` are eliminated if `S` also contains a non-template function.

|  |  |
| --- | --- |
| - Any given non-template function func is eliminated if `S` contains a second non-template function that is more partial-ordering-constrained than func. | (since C++20) |

- Any given function template specialization spec is eliminated if `S` contains a second function template specialization whose function template is more specialized than the function template of spec.

After such eliminations (if any), exactly one selected function should remain in `S`. Otherwise, the program is ill-formed.

### Example

Run this code

```
int f(int) { return 1; }
int f(double) { return 2; }
 
void g(int(&f1)(int), int(*f2)(double)) { f1(0); f2(0.0); }
 
template<int(*F)(int)>
struct Templ {};
 
struct Foo
{
    int mf(int) { return 3; }
    int mf(double) { return 4; }
};
 
struct Emp
{
    void operator<<(int (*)(double)) {}
};
 
int main()
{
    // 1. initialization
    int (*pf)(double) = f; // selects int f(double)
    int (&rf)(int) = f; // selects int f(int)
    int (Foo::*mpf)(int) = &Foo::mf; // selects int mf(int)
 
    // 2. assignment
    pf = nullptr;
    pf = &f; // selects int f(double)
 
    // 3. function argument
    g(f, f); // selects int f(int) for the 1st argument
             // and int f(double) for the second
 
    // 4. user-defined operator
    Emp{} << f; //selects int f(double)
 
    // 5. return value
    auto foo = []() -> int (*)(int)
    {
        return f; // selects int f(int)
    };
 
    // 6. cast
    auto p = static_cast<int(*)(int)>(f); // selects int f(int)
 
    // 7. template argument
    Templ<f> t;  // selects int f(int)
 
    // prevent “unused variable” warnings as if by [[maybe_unused]]
    [](...){}(pf, rf, mpf, foo, p, t);
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 202 | C++98 | non-type template argument was not a context of taking the address of an overloaded function | it is |
| CWG 250 | C++98 | function template specializations generated with non-deduced template arguments were not selected from the overload set | also selected |
| CWG 1153 | C++98 | it was unclear whether a given function type matches the target type | made clear |
| CWG 1563 | C++11 | it was unclear whether list-initialization is a context of taking the address of an overloaded function | made clear |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 12.3 Address of overloaded function [over.over]

- C++20 standard (ISO/IEC 14882:2020):

:   - 12.5 Address of overloaded function [over.over]

- C++17 standard (ISO/IEC 14882:2017):

:   - 16.4 Address of overloaded function [over.over]

- C++14 standard (ISO/IEC 14882:2014):

:   - 13.4 Address of overloaded function [over.over]

- C++11 standard (ISO/IEC 14882:2011):

:   - 13.4 Address of overloaded function [over.over]

- C++98 standard (ISO/IEC 14882:1998):

:   - 13.4 Address of overloaded function [over.over]

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/overloaded_address&oldid=179851>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 January 2025, at 00:09.