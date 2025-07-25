# Other operators

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

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | Constant expressions | | | | | | Primary expressions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lambda expressions (C++11) | | | | | | Requires expressions (C++20) | | | | | | Pack indexing expression (C++26) | | | | | | Potentially-evaluated expressions | | | | | |
| Literals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integer literals | | | | | | Floating-point literals | | | | | | Boolean literals | | | | | | Character literals | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Escape sequences | | | | | | String literals | | | | | | Null pointer literal (C++11) | | | | | | User-defined literal (C++11) | | | | | |
| Operators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | ****Other operators**** | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

| Operator name | Syntax | Over​load​able | Prototype examples (for class T) | |
| --- | --- | --- | --- | --- |
| Inside class definition | Outside class definition |
| function call | `a(a1, a2)` | Yes | R T::operator()(Arg1 &a1, Arg2 &a2, ...); | N/A |
| comma | `a, b` | Yes | T2& T::operator,(T2 &b); | T2& operator,(const T &a, T2 &b); |
| conditional operator | `a ? b : c` | No | N/A | N/A |

The **function call** operator provides function semantics for any object.

The **conditional operator** (colloquially referred to as **ternary conditional** ﻿) checks the boolean value of the first expression and, depending on the resulting value, evaluates and returns either the second or the third expression.

### Built-in function call operator

Function call expressions have the following form:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| function ﻿`(`arg1`,` arg2`,` arg3`,`...`)` |  |  |
|  | | | | | | | | | |

|  |  |  |
| --- | --- | --- |
| function | - | an expression function type or function pointer type |
| arg1`,` arg2`,` arg3`,`... | - | a possibly empty list of arbitrary expressions or brace-enclosed initializer lists(since C++11), except the comma operator is not allowed at the top level to avoid ambiguity |

For a call to a non-member function or to a static member function, function can be an lvalue that refers to a function (in which case the function-to-pointer conversion is suppressed), or a prvalue of function pointer type.

The function (or member) name specified by function can be overloaded, overload resolution rules used to decide which overload is to be called.

If function specifies a member function, it may be virtual, in which case the final overrider of that function will be called, using dynamic dispatch at runtime.

To call the function,

|  |  |
| --- | --- |
| The expression function as well as all expressions arg1, arg2, arg3, etc, provided as arguments are evaluated in arbitrary order, unsequenced with respect to each other. | (until C++17) |
| function is sequenced before each of arg1, arg2, arg3 as well as default arguments, if any. The argument expressions are evaluated in arbitrary order, indeterminately sequenced with respect to each other. | (since C++17) |

Each function parameter is initialized with its corresponding argument after implicit conversion if necessary.

- If there is no corresponding argument, the corresponding default argument is used, and if there is none, the program is ill-formed.
- If the call is made to a member function, then the this pointer to current object is converted as if by explicit cast to the this pointer expected by the function.
- The initialization and destruction of each parameter occurs in the context of the full-expression where the function call appears, which means, for example, that if a constructor or destructor of a parameter throws an exception, the function try blocks of the called function are not considered.

If the function is a variadic function, default argument promotions are applied to all arguments matched by the ellipsis parameter.

It is implementation-defined whether a parameter is destroyed when the function in which it is defined exits or at the end of the enclosing full-expression. Parameters are always destroyed in the reverse order of their construction.

The return type of a function call expression is the return type of the chosen function, decided using static binding (ignoring the virtual keyword), even if the overriding function that is actually called returns a different type. This allows the overriding functions to return pointers or references to classes that are derived from the return type returned by the base function, i.e. C++ supports covariant return types. If function specifies a destructor, the return type is void.

|  |  |
| --- | --- |
| When an object of class type `X` is passed to or returned from a function, if each copy constructor, move constructor, and destructor of `X` is either trivial or deleted, and `X` has at least one non-deleted copy or move constructor, implementations are permitted to create a temporary object to hold the function parameter or result object.  The temporary object is constructed from the function argument or return value, respectively, and the function's parameter or return object is initialized as if by using the non-deleted trivial constructor to copy the temporary (even if that constructor is inaccessible or would not be selected by overload resolution to perform a copy or move of the object).  This allows objects of small class types, such as std::complex or std::span, to be passed to or returned from functions in registers. | (since C++17) |

The value category of a function call expression is lvalue if the function returns an lvalue reference or an rvalue reference to function, is an xvalue if the function returns an rvalue reference to object, and is a prvalue otherwise. If the function call expression is a prvalue of object type, it must have complete type except when used as the operand of `decltype` (or as the right operand of a built-in comma operator that is the operand of decltype)(since C++11).

Function call expression is similar in syntax to value initialization T(), to function-style cast expression T(A1), and to direct initialization of a temporary T(A1, A2, A3, ...), where `T` is the name of a type.

Run this code

```
#include <cstdio>
 
struct S
{
    int f1(double d)
    {
        return printf("%f \n", d); // variable argument function call
    }
 
    int f2()
    {
        return f1(7); // member function call, same as this->f1()
                      // integer argument converted to double
    }
};
 
void f()
{
    puts("function called"); // function call
}
 
int main()
{
    f();    // function call
    S s;
    s.f2(); // member function call
}

```

Output:

```
function called
7.000000

```

### Built-in comma operator

Comma expressions have the following form:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| E1 `,` E2 |  |  |
|  | | | | | | | | | |

In a comma expression E1, E2, the expression E1 is evaluated, its result is discarded (although if it has class type, it won't be destroyed until the end of the containing full expression), and its side effects are completed before evaluation of the expression E2 begins (note that a user-defined `operator,` cannot guarantee sequencing)(until C++17).

The type, value, and value category of the result of the comma expression are exactly the type, value, and value category of the second operand, E2. If E2 is a temporary expression(since C++17), the result of the expression is that temporary expression(since C++17). If E2 is a bit-field, the result is a bit-field.

The comma in various comma-separated lists, such as function argument lists (f(a, b, c)) and initializer lists int a[] = {1, 2, 3}, is not the comma operator. If the comma operator needs to be used in such contexts, it has to be parenthesized: f(a, (n++, n + b), c).

|  |  |
| --- | --- |
| Using an unparenthesized comma expression as second (right) argument of a subscript operator is deprecated.  For example, a[b, c] is deprecated and a[(b, c)] is not. | (since C++20) (until C++23) |
| An unparenthesized comma expression cannot be second (right) argument of a subscript operator. For example, a[b, c] is either ill-formed or equivalent to a.operator[](b, c).  Parentheses are needed when using a comma expression as the subscript, e.g., a[(b, c)]. | (since C++23) |

Run this code

```
#include <iostream>
 
int main()
{
    // comma is often used to execute more than one expression
    // where the language grammar allows only one expression:
 
    // * in the third component of the for loop
    for (int i = 0, j = 10; i <= j; ++i, --j)
    //            ^list separator      ^comma operator
        std::cout << "i = " << i << " j = " << j << '\n';
 
    // * in a return statement
    // return log("an error!"), -1;
 
    // * in an initializer expression
    // MyClass(const Arg& arg)
    // : member{ throws_if_bad(arg), arg }
 
    // etc.
 
    // comma operators can be chained; the result of the last
    // (rightmost) expression is the result of the whole chain:
    int n = 1;
    int m = (++n, std::cout << "n = " << n << '\n', ++n, 2 * n);
 
    // m is now 6
    std::cout << "m = " << (++m, m) << '\n';
}

```

Output:

```
i = 0 j = 10
i = 1 j = 9
i = 2 j = 8
i = 3 j = 7
i = 4 j = 6
i = 5 j = 5
n = 2
m = 7

```

### Conditional operator

The conditional operator expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| E1 `?` E2 `:` E3 |  |  |
|  | | | | | | | | | |

The first operand of the conditional operator is evaluated and contextually converted to bool. After both the value evaluation and all side effects of the first operand are completed, if the result was true, the second operand is evaluated. If the result was false, the third operand is evaluated.

The type and value category of the conditional expression E1 ? E2 : E3 are determined according to the following rules:

- If either E2 or E3 has type void:

:   - If both E2 and E3 are of type void, the result is a prvalue of type void.
    - Otherwise, if the operand of type void is a (possibly parenthesized) throw expression, the result has the type and the value category of the other expression. If the other expression is a bit-field, the result is a bit-field.[[1]](operator_other.html#cite_note-1)
    - Otherwise, the program is ill-formed.

```
2 + 2 == 4 ? throw 123 : throw 456;
 
std::string str = 2 + 2 == 4 ? "OK" : throw std::logic_error("2 + 2 != 4");

```

- Otherwise, if E2 or E3 are lvalue bit-fields(until C++11)glvalue bit-fields of the same value category(since C++11) and of types **cv1** `T` and **cv2** `T`, respectively, the operands are considered to be of type **cv** `T` for the remainder of this section, where cv is the union of **cv1** and **cv2**.

- Otherwise, if E2 and E3 have different types, at least one of which is a (possibly cv-qualified) class type, or both are lvalues(until C++11)glvalues of the same value category(since C++11) and have the same type except for cv-qualification, then an attempt is made to form an implicit conversion sequence.[[2]](operator_other.html#cite_note-2)

:   Attempts are made to form an implicit conversion sequence from an operand expression X of type `TX` to a **target type** related to the type `TY` of the operand expression Y as follows:

    - If Y is an lvalue, the target type is `TY&`, but an implicit conversion sequence can only be formed if the reference would bind directly to an lvalue(until C++11)a glvalue(since C++11).

|  |  |
| --- | --- |
| - If Y is an xvalue, the target type is `TY&&`, but an implicit conversion sequence can only be formed if the reference would bind directly. | (since C++11) |

:   - If Y is an rvalue(until C++11)a prvalue(since C++11) or if none of the conversion sequences above can be formed, and at least one of `TX` and `TY` is a (possibly cv-qualified) class type:

    :   - If `TX` and `TY` are the same class type (ignoring cv-qualification):

        :   - If `TY` is at least as cv-qualified as `TX`, the target type is `TY`.
            - Otherwise, no conversion sequence is formed.

        - Otherwise, if `TY` is a base class of `TX`, the target type is `TY` with the cv-qualifiers of `TX`.
        - Otherwise, the target type is the type of Z, where Z is the value of Y after applying the lvalue-to-rvalue, array-to-pointer, and function-to-pointer standard conversions.

    - Otherwise, no conversion sequence is formed.
:   Using this process, it is determined whether an implicit conversion sequence can be formed from E2 to the target type determined for the E3, and vice versa.

    - If both sequences can be formed, or one can be formed but it is the ambiguous conversion sequence, the program is ill-formed.
    - If no conversion sequence can be formed, the operands are left unchanged.
    - Otherwise, if exactly one conversion sequence can be formed, that conversion is applied to the chosen operand and the converted operand is used in place of the original operand for the remaining process.

```
struct A {};
 
struct B : A {};
 
using T = const B;
 
A a = true ? A() : T(); // Y = A(), TY = A, X = T(), TX = const B, Target = const A

```

|  |  |
| --- | --- |
| - If E2 and E3 are lvalues of the same type, then the result is an lvalue of that type, and is a bit-field if at least one of E2 and E3 is a bit-field. | (until C++11) |
| - If E2 and E3 are glvalues of the same type and the same value category, then the result has the same type and value category, and is a bit-field if at least one of E2 and E3 is a bit-field. | (since C++11) |

- Otherwise, the result is an rvalue(until C++11)a prvalue(since C++11).

:   - If E2 and E3 do not have the same type, and either has (possibly cv-qualified) class type, overload resolution is performed using the built-in candidates to attempt to convert the operands to built-in types.

    :   - If the overload resolution fails, the program is ill-formed.
        - Otherwise, the selected conversions are applied and the converted operands are used in place of the original operands for the remaining process.

    - The array-to-pointer and function-to-pointer conversions are applied to (possibly-converted) E2 and E3. After those conversions, at least one of the following conditions must hold, otherwise the program is ill-formed:

    :   - E2 and E3 have the same type. In this case, the result is of that type and the result is copy-initialized using the selected operand.
        - Both E2 and E3 have arithmetic or enumeration type. In this case, usual arithmetic conversions are applied to bring them to their common type, and the result is of that type.
        - At least one of E2 and E3 is a pointer. In this case, lvalue-to-rvalue, pointer, function pointer(since C++17) and qualification conversions are applied to bring them to their composite pointer type, and the result is of that type.
        - At least one of E2 and E3 is a pointer to members. In this case, lvalue-to-rvalue, pointer-to-member, function pointer(since C++17) and qualification conversions are applied to bring them to their composite pointer type, and the result is of that type.

|  |  |
| --- | --- |
| - Both E2 and E3 are null pointer constants, and at least one of which is of type std::nullptr_t. In this case, the result is of type std::nullptr_t. | (since C++11) |

```
int* intPtr;
 
using Mixed = decltype(true ? nullptr : intPtr);
 
static_assert(std::is_same_v<Mixed, int*>); // nullptr becoming int*
 
struct A
{
    int* m_ptr;
} a;
 
int* A::* memPtr = &A::m_ptr; // memPtr is a pointer to member m_ptr of A
 
// memPtr makes nullptr as type of pointer to member m_ptr of A
static_assert(std::is_same_v<decltype(false ? memPtr : nullptr), int*A::*>);
 
// a.*memPtr is now just pointer to int and nullptr also becomes pointer to int
static_assert(std::is_same_v<decltype(false ? a.*memPtr : nullptr), int*>);

```

1. ↑  Such conditional operator was commonly used in C++11 constexpr programming prior to C++14.
2. ↑ Member access, whether a conversion function is deleted(since C++11) and whether an operand is a bit-field are ignored.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: any chance to make this more readable without losing the fine point? At the very least, a one-line micro-example for each bullet point would help tremendously |

#### Overloads

For every pair of promoted arithmetic types `L` and `R` and for every type `P`, where `P` is a pointer, pointer-to-member, or scoped enumeration type, the following function signatures participate in overload resolution:

|  |  |  |
| --- | --- | --- |
| LR operator?:(bool, L, R); |  |  |
| P operator?:(bool, P, P); |  |  |
|  |  |  |

where LR is the result of usual arithmetic conversions performed on `L` and `R`.

The operator “`?:`” cannot be overloaded, these function signatures only exist for the purpose of overload resolution.

|  |  |
| --- | --- |
| The result type of a conditional operator is also accessible as the binary type trait std::common_type. | (since C++11) |

Run this code

```
#include <iostream>
#include <string>
 
struct Node
{
    Node* next;
    int data;
 
    // deep-copying copy constructor
    Node(const Node& other)
        : next(other.next ? new Node(*other.next) : NULL)
        , data(other.data)
    {}
 
    Node(int d) : next(NULL), data(d) {}
 
    ~Node() { delete next; }
};
 
int main()
{   
    // simple rvalue example
    int n = 1 > 2 ? 10 : 11;  // 1 > 2 is false, so n = 11
 
    // simple lvalue example
    int m = 10; 
    (n == m ? n : m) = 7; // n == m is false, so m = 7
 
    //output the result
    std::cout << "n = " << n << "\nm = " << m;
}

```

Output:

```
n = 11
m = 7

```

### Standard library

Many classes in the standard library overload `operator()` to be used as function objects.

|  |  |
| --- | --- |
| operator() | deletes the object or array   (public member function of `std::default_delete<T>`) |
| operator() | returns the sum of two arguments   (public member function of `std::plus<T>`) |
| operator() | returns the difference between two arguments   (public member function of `std::minus<T>`) |
| operator() | returns the product of two arguments   (public member function of `std::multiplies<T>`) |
| operator() | returns the result of the division of the first argument by the second argument   (public member function of `std::divides<T>`) |
| operator() | returns the remainder from the division of the first argument by the second argument   (public member function of `std::modulus<T>`) |
| operator() | returns the negation of the argument   (public member function of `std::negate<T>`) |
| operator() | checks if the arguments are equal   (public member function of `std::equal_to<T>`) |
| operator() | checks if the arguments are not equal   (public member function of `std::not_equal_to<T>`) |
| operator() | checks if the first argument is greater than the second   (public member function of `std::greater<T>`) |
| operator() | checks if the first argument is less than the second   (public member function of `std::less<T>`) |
| operator() | checks if the first argument is greater than or equal to the second   (public member function of `std::greater_equal<T>`) |
| operator() | checks if the first argument is less than or equal to the second   (public member function of `std::less_equal<T>`) |
| operator() | returns the logical AND of the two arguments   (public member function of `std::logical_and<T>`) |
| operator() | returns the logical OR of the two arguments   (public member function of `std::logical_or<T>`) |
| operator() | returns the logical NOT of the argument   (public member function of `std::logical_not<T>`) |
| operator() | returns the result of bitwise AND of two arguments   (public member function of `std::bit_and<T>`) |
| operator() | returns the result of bitwise OR of two arguments   (public member function of `std::bit_or<T>`) |
| operator() | returns the result of bitwise XOR of two arguments   (public member function of `std::bit_xor<T>`) |
| operator() | returns the logical complement of the result of a call to the stored predicate   (public member function of `std::unary_negate<Predicate>`) |
| operator() | returns the logical complement of the result of a call to the stored predicate   (public member function of `std::binary_negate<Predicate>`) |
| operator()") | calls the stored function   (public member function of `std::reference_wrapper<T>`) |
| operator()") | invokes the target   (public member function of `std::function<R(Args...)>`) |
| operator()") | invokes the target   (public member function of `std::move_only_function`) |
| operator()") | invokes the target   (public member function of `std::copyable_function`) |
| operator()&action=edit&redlink=1 "cpp/coroutine/coroutine handle/operator() (page does not exist)") | resumes execution of the coroutine   (public member function of `std::coroutine_handle<Promise>`) |
| operator()") | lexicographically compares two strings using this locale's collate facet   (public member function of `std::locale`) |
| operator() | compares two values of type `value_type`   (public member function of `std::map<Key,T,Compare,Allocator>::value_compare`) |
| operator() | compares two values of type `value_type`   (public member function of `std::multimap<Key,T,Compare,Allocator>::value_compare`) |
| operator()") | executes the function   (public member function of `std::packaged_task<R(Args...)>`) |
| operator()") | advances the engine's state and returns the generated value   (public member function of `std::linear_congruential_engine<UIntType,a,c,m>`) |
| operator()")(C++11) | generates the next random number in the distribution   (public member function of `std::uniform_int_distribution<IntType>`) |

The comma operator is not overloaded by any class in the standard library. The boost library uses operator, in boost.assign, boost.spirit, and other libraries. The database access library SOCI also overloads operator,.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 446 | C++98 | it was unspecified whether a temporary is created for an lvalue-to-rvalue conversion on the conditional operator | always creates a temporary if the operator returns a class rvalue |
| CWG 462 | C++98 | if the second operand of a comma operator is a temporary, it was unspecified whether its lifetime will be extended when the result of the comma expression is bound to a reference | the result of the comma expression is the temporary in this case (hence its lifetime is extended) |
| CWG 587 | C++98 | when the second and third operands of a conditional operator are lvalues of the same type except for cv-qualification, the result was an lvalue if these operands have class types or an rvalue otherwise | the result is always an lvalue in this case |
| CWG 1029 | C++98 | the type of a destructor call was unspecified | specified as void |
| CWG 1550 | C++98 | parenthesized throw expressions were not allowed in conditional expressions if other operand is non-void | accepted |
| CWG 1560 | C++98 | void operand of conditional operators caused gratuitous lvalue-to-rvalue conversion on the other operand, always resulting in rvalue | a conditional expression with a void can be lvalue |
| CWG 1642 | C++98 | the expression function in a function call expression could be a function pointer lvalue | not allowed |
| CWG 1805 | C++98 | when determining the target type for the implicit conversion sequence, the way to convert Y to Z was unclear | made clear |
| CWG 1895 | C++98 C++11 | unclear if deleted (C++11) or inaccessible (C++98) conversion function prevents conversion in conditional expressions, and conversions from base class to derived class prvalue were not considered | handled like overload resolution |
| CWG 1932 | C++98 | same-type bit-fields were missing in conditional expressions | handled by underlying types |
| CWG 2226 | C++11 | when determining the target type of the other operand of a conditional operator, reference could not bind to an xvalue if that operand is an lvalue | allowed |
| CWG 2283 | C++17 | the type completeness requirement for function call operator was accidently removed by P0135R1 | restored the requirement |
| CWG 2321 | C++98 | when determining the target type of the other operand of a conditional operator, a derived class type could not be converted to a less cv-qualified base class type | allowed to convert to the base class type with the cv-qualification from the derived class operand |
| CWG 2715 | C++98 | the initialization and destruction of each parameter would occur within the context of the calling function, which might not exist[[1]](operator_other.html#cite_note-3) | occurs within the context of the enclosing full-expression |
| CWG 2850 | C++98 | the destruction order of parameters was unclear | made clear |
| CWG 2865 | C++98 | if `TX` and `TY` are the same class type and `TX` is more cv-qualified than `TY`, an implicit conversion sequence could still be formed from a prvalue Y | no conversion sequence will be formed in this case |
| CWG 2906 | C++98 | lvalue-to-rvalue conversions were unconditionally applied in the rvalue result case for the conditional operator | only applied in some cases |

1. ↑ For example, functions can be called in the initializer of a namespace-scope variable, there is no “calling function” in this context.

### See also

Operator precedence  
Operator overloading

| Common operators | | | | | | |
| --- | --- | --- | --- | --- | --- | --- |
| assignment | increment decrement | arithmetic | logical | comparison | member access | ****other**** |
| a = b  a += b  a -= b  a \*= b  a /= b  a %= b  a &= b  a |= b  a ^= b  a <<= b  a >>= b | ++a  --a  a++  a-- | +a  -a  a + b  a - b  a \* b  a / b  a % b  ~a  a & b  a | b  a ^ b  a << b  a >> b | !a  a && b  a || b | a == b  a != b  a < b  a > b  a <= b  a >= b  a <=> b | a[...]  \*a  &a  a->b  a.b  a->\*b  a.\*b | function call  a(...) |
| comma  a, b |
| conditional  a ? b : c |
| Special operators | | | | | | |
| static_cast converts one type to another related type  dynamic_cast converts within inheritance hierarchies  const_cast adds or removes cv-qualifiers  reinterpret_cast converts type to unrelated type  C-style cast converts one type to another by a mix of static_cast, const_cast, and reinterpret_cast  new creates objects with dynamic storage duration  delete destructs objects previously created by the new expression and releases obtained memory area  sizeof queries the size of a type  sizeof... queries the size of a pack (since C++11)  typeid queries the type information of a type  noexcept checks if an expression can throw an exception (since C++11)  alignof queries alignment requirements of a type (since C++11) | | | | | | |

|  |  |
| --- | --- |
| C documentation for Other operators | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/operator_other&oldid=179794>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 January 2025, at 01:22.