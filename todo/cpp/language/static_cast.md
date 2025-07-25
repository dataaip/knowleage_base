# `static_cast` conversion

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | ****static_cast**** | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Explicit conversions | | | | | | dynamic_cast | | | | | | reinterpret_cast | | | | | |
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | ****`static_cast`**** | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

Converts between types using a combination of implicit and user-defined conversions.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `static_cast<`target-type ﻿`>(`expression ﻿`)` |  |  |
|  | | | | | | | | | |

Returns a value of type target-type.

### Explanation

Only the following conversions can be done with static_cast, except when such conversions would cast away constness (or volatility).

1) If expression is an lvalue of type “**cv1** `Base`” and target-type is “reference to **cv2** `Derived`”, the result refers to the object of type `Derived` enclosing expression if all following conditions are satisfied:

- `Derived` is a complete class type.
- `Base` is a base class of `Derived`.
- **cv1** is not a greater cv-qualification than **cv2**.
 If any of the following conditions is satisfied, the program is ill-formed:

- `Base` is a virtual base class of `Derived`.
- `Base` is a base class of a virtual base class of `Derived`.
- No valid standard conversion from “pointer to `Derived`” to “pointer to `Base`” exists.
 If expression is actually not a base class subobject of an object of type `Derived`, the behavior is undefined.

```
struct B {};
struct D : B { B b; };
 
D d;
B& br1 = d;
B& br2 = d.b;
 
static_cast<D&>(br1); // OK, lvalue denoting the original “d” object
static_cast<D&>(br2); // UB: the “b” subobject is not a base class subobject

```

|  |  |
| --- | --- |
| 2) If target-type is “rvalue reference to `Derived`” and expression is an xvalue of type “(possibly cv-qualified) `Base`” such that `Base` is a base class of `Derived`, the result and constraints of such a conversion are the same as those of the “`Base` lvalue to `Derived` reference” conversion.3) If target-type is an rvalue reference type and the referenced type is reference-compatible with the type of expression, static_cast converts the value of glvalue, class prvalue, or array prvalue(until C++17)any lvalue(since C++17) expression to xvalue referring to the same object as the expression, or to its base class subobject (depending on target-type).[[1]](static_cast.html#cite_note-1) If target-type is an inaccessible or ambiguous base of the type of expression, the program is ill-formed. If expression is a bit-field lvalue, it is first converted to prvalue of the underlying type. | (since C++11) |

4) If target-type is the (possibly cv-qualified) void, the conversion has no result. In this case, expression is a discarded-value expression.5) Otherwise, expression can be explicitly converted to target-type if

|  |  |
| --- | --- |
| the declaration target-type temp(expression ﻿); is well-formed for some invented temporary variable temp.  The effect of such an explicit conversion is the same as performing the declaration and initialization and then using temp as the result of the conversion. The expression ﻿ is used as an lvalue(until C++11)a glvalue(since C++11) if and only if the initialization uses it as an lvalue(until C++11)a glvalue(since C++11). | (until C++17) |
| any of the following conditions is satisfied:   - There is an implicit conversion sequence from expression to target-type. - The overload resolution for a direct-initialization of an object or reference of type target-type from expression would find at least one viable function.  |  |  | | --- | --- | | - target-type is an aggregate type having a first element x and there is an implicit conversion sequence from expression to the type of x. | (since C++20) |   The explicit conversion is defined as follows:   - If target-type is a reference type, the effect is the same as performing the declaration and initialization target-type temp(expression ﻿); for some invented temporary variable temp and then using temp as the result of the conversion. - Otherwise, the result object is direct-initialized from expression ﻿. | (since C++17) |

6) Otherwise, if the conversion from expression to target-type is an inverse of a standard conversion sequence, and the conversion sequence does not contain any of the following conversions, the conversion can be performed by static_cast:

- lvalue-to-rvalue conversion
- array-to-pointer conversion
- function-to-pointer conversion
- null pointer conversion
- null member pointer conversion
- boolean conversion

|  |  |
| --- | --- |
| - function pointer conversion | (since C++17) |

 If a program uses static_cast to perform the inverse of an ill-formed standard conversion sequence, it is ill-formed.7) Otherwise, lvalue-to-rvalue, array-to-pointer, and function-to-pointer conversions are applied to expression. After these conversions, only the following conversions can be performed by static_cast:

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| a) A value of scoped enumeration type can be converted to an integer or floating-point type.  |  |  | | --- | --- | | - If target-type is (possibly cv-qualified) bool, the result is false if the original value of expression is zero and true for all other values. - If target-type is an integral type other than (possibly cv-qualified) bool, the value is unchanged if the original value of expression can be represented by target-type. Otherwise, the resulting value is unspecified. | (until C++20) | | - If target-type is an integral type, the result is the same as that of converting to the enumeration’s underlying type and then to target-type. | (since C++20) |  - If target-type is a floating-point type, the result is the same as that of converting from the original value to target-type. | (since C++11) |

b) A value of integer or enumeration type can be converted to any complete enumeration type.

- If target-type has a fixed underlying type, expression is first converted to that type by integral promotion or integral conversion, if necessary, and then to target-type.
- If target-type does not have a fixed underlying type, the value of expression is unchanged if the original value is within the range of the enumeration values, otherwise the behavior is undefined.
c) A value of a floating-point type can also be converted to any complete enumeration type. The result is the same as converting the original value of expression first to the underlying type of target-type, and then to target-type itself.

|  |  |
| --- | --- |
| d) A prvalue of floating-point type can be explicitly converted to any other floating-point type.  - If the source value of expression can be represented exactly in target-type, it does not change. - Otherwise, if the source value of expression is between two representable values of target-type, the result of the conversion is an implementation-defined choice of either of those values.[[2]](static_cast.html#cite_note-2) - Otherwise, the behavior is undefined. | (since C++23) |

e) An rvalue(until C++11)A prvalue(since C++11) of type “pointer to **cv1** `Base`” can be explicitly converted to the type “pointer to **cv2** `Derived`” if all following conditions are satisfied:

- `Derived` is a complete class type.
- `Base` is a base class of `Derived`.
- **cv1** is not a greater cv-qualification than **cv2**.
 If expression is a null pointer value, the result is a null pointer value of type target-type. Otherwise, the result is a pointer to the object of type `Derived` enclosing the object of type `Base` pointed to by expression. If any of the following conditions is satisfied, the program is ill-formed:

- `Base` is a virtual base class of `Derived`.
- `Base` is a base class of a virtual base class of `Derived`.
- No valid standard conversion from “pointer to `Derived`” to “pointer to `Base`” exists.
 If expression is not a null pointer value and does not actually point to a base class subobject of an object of type `Derived`, the behavior is undefined.f) An rvalue(until C++11)A prvalue(since C++11) of type “pointer to member of `Derived` of type **cv1** `T`” can be explicitly converted to the type “pointer to member of `Base` of type **cv2** `T`” if all following conditions are satisfied:

- `Derived` is a complete class type.
- `Base` is a base class of `Derived`.
- **cv1** is not a greater cv-qualification than **cv2**.
 If expression is a null member pointer value, the result is a null member pointer value of type target-type. Otherwise, the result is a pointer to the original (possibly indirect) member of class `Base`. If no valid standard conversion from “pointer to member of `Base` of type `T`” to “pointer to member of `Derived` of type `T`” exists, the program is ill-formed. If expression is not a null member pointer value and the member it denotes is not a (possibly indirect) member of class `Base`, the behavior is undefined.g) An rvalue(until C++11)A prvalue(since C++11) of type “pointer to **cv1** void” can be explicitly converted to the type “pointer to **cv2** `T`” if `T` is an object type and **cv1** is not a greater cv-qualification than **cv2**.

|  |  |
| --- | --- |
| - If expression is a null pointer value, the result is a null pointer value of type target-type. - If the expression represents the address `A` of a byte in memory and `A` satisfies the alignment requirement of `T`, then the resulting pointer value also represents `A`. - The result of any other such pointer conversion is unspecified. - If expression the result of a prior conversion from an object of type “pointer to **cv3** `T`”, the result has the original value. | (until C++17) |
| - If expression represents the address `A` of a byte in memory but `A` does not satisfy the alignment requirement of `T`, then the resulting pointer value is unspecified. - Otherwise, if expression points to an object a, and there is an object b of type `T` (ignoring cv-qualification) that is pointer-interconvertible (see below) with a, the result is a pointer to b. - Otherwise, the pointer value is unchanged by the conversion. | (since C++17) |

As with all cast expressions, the result is:

- an lvalue if target-type is an lvalue reference type or an rvalue reference to function type(since C++11);

|  |  |
| --- | --- |
| - an xvalue if target-type is an rvalue reference to object type; | (since C++11) |

- a prvalue otherwise.

1. ↑ This type of static_cast is used to implement move semantics in std::move.
2. ↑ If IEEE arithmetic is supported, rounding defaults to nearest.

### Pointer-interconvertible objects

Two objects a and b are **pointer-interconvertible** if:

- they are the same object, or
- one is a union object and the other is a non-static data member of that object, or
- one is a standard-layout class object and the other is the first non-static data member of that object or any base class subobject of that object, or
- there exists an object c such that a and c are pointer-interconvertible, and c and b are pointer-interconvertible.

```
union U { int a; double b; } u;
void* x = &u;                        // x's value is “pointer to u”
double* y = static_cast<double*>(x); // y's value is “pointer to u.b”
char* z = static_cast<char*>(x);     // z's value is “pointer to u”

```

### Notes

Base-to-derived conversions (**downcasts**) using static_cast make no runtime checks to ensure that the dynamic type of the pointed/referred object is `Derived`, and may only be used safely if this precondition is guaranteed by other means, such as when implementing static polymorphism. Safe downcast may be done with `dynamic_cast`.

static_cast may also be used to disambiguate function overloads by performing a function-to-pointer conversion to specific type, as in

```
std::for_each(files.begin(), files.end(),
              static_cast<std::ostream&(*)(std::ostream&)>(std::flush));

```

### Keywords

static_cast

### Example

Run this code

```
#include <iostream>
#include <vector>
 
struct B
{
    int m = 42;
    const char* hello() const
    {
        return "Hello world, this is B!\n";
    }
};
 
struct D : B
{
    const char* hello() const
    {
        return "Hello world, this is D!\n";
    }
};
 
enum class E { ONE = 1, TWO, THREE };
enum EU { ONE = 1, TWO, THREE };
 
int main()
{
    // 1. static downcast
    D d;
    B& br = d; // upcast via implicit conversion
    std::cout << "1) " << br.hello();
    D& another_d = static_cast<D&>(br); // downcast
    std::cout << "1) " << another_d.hello();
 
    // 3. lvalue to xvalue
    std::vector<int> v0{1, 2, 3};
    std::vector<int> v2 = static_cast<std::vector<int>&&>(v0);
    std::cout << "3) after move, v0.size() = " << v0.size() << '\n';
 
    // 4. discarded-value expression
    static_cast<void>(v2.size());
 
    // 5. initializing conversion
    int n = static_cast<int>(3.14);
    std::cout << "5) n = " << n << '\n';
    std::vector<int> v = static_cast<std::vector<int>>(10);
    std::cout << "5) v.size() = " << v.size() << '\n';
 
    // 6. inverse of implicit conversion
    void* nv = &n;
    int* ni = static_cast<int*>(nv);
    std::cout << "6) *ni = " << *ni << '\n';
 
    // 7a. scoped enum to int
    E e = E::TWO;
    int two = static_cast<int>(e);
    std::cout << "7a) " << two << '\n';
 
    // 7b. int to enum, enum to another enum
    E e2 = static_cast<E>(two);
    [[maybe_unused]]
    EU eu = static_cast<EU>(e2);
 
    // 7f. pointer to member upcast
    int D::*pm = &D::m;
    std::cout << "7f) " << br.*static_cast<int B::*>(pm) << '\n';
 
    // 7g. void* to any object pointer
    void* voidp = &e;
    [[maybe_unused]]
    std::vector<int>* p = static_cast<std::vector<int>*>(voidp);
}

```

Output:

```
1) Hello world, this is B!
1) Hello world, this is D!
3) after move, v0.size() = 0
5) n = 3
5) v.size() = 10
6) *ni = 3
7a) 2
7f) 42

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 137 | C++98 | the constness and volatility of pointers to void could be casted away | cv-qualifications cannot be casted away in such cases |
| CWG 427 | C++98 | downcast might be ambiguous with direct-initialization | selects downcast in this case |
| CWG 439 | C++98 | when converting a “pointer to object” to “pointer to void” then back to itself, it could only preserve its value if the result type has the same cv-qualification | cv-qualification may be different |
| CWG 1094 | C++98 | the conversion from floating-point values to enumeration values was unspecified | specified |
| CWG 1320 | C++11 | the conversion from scoped enumeration values to bool was unspecified | specified |
| CWG 1412 | C++98 | the result of the conversion from “pointer to void” to “pointer to object” was unclear | made clear |
| CWG 1447 | C++11 | the conversion from bit-fields to rvalue references was unspecified (cannot bind references to bit-fields) | specified |
| CWG 1766 | C++98 | the conversion from integral or enumeration values to enumeration values yielded unspecified result if expression is out of range | the behavior is undefined in this case |
| CWG 1832 | C++98 | the conversion from integral or enumeration values to enumeration values allowed target-type to be incomplete | not allowed |
| CWG 2224 | C++98 | the conversion from a member of base class type to its complete object of derived class type was valid | the behavior is undefined in this case |
| CWG 2254 | C++11 | a standard-layout class object with no data members was pointer-interconvertible to its first base class | it is pointer-interconvertible to any of its base classes |
| CWG 2284 | C++11 | a non-standard-layout union object and a non-static data member of that object were not pointer-interconvertible | they are |
| CWG 2310 | C++98 | for base-to-derived pointer conversions and derived-to-base pointer-to-member conversions, the derived class type could be incomplete | must be complete |
| CWG 2338 | C++11 | the conversion to enumeration types with fixed underlying type resulted in undefined behavior if expression is out of range | convert to the underlying type first (no undefined behavior) |
| CWG 2499 | C++11 | a standard-layout class might have a non-pointer-interconvertible base class, even though all base subobjects have the same address | it does not have |
| CWG 2718 | C++98 | for base-to-derived reference conversions, the derived class type could be incomplete | must be complete |
| CWG 2882 | C++98 | it was unclear whether static_cast<void>(expr) attempts to form an implicit conversion sequence from expr to void | no attempt in this case |

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 7.6.1.9 Static cast [expr.static.cast]

- C++20 standard (ISO/IEC 14882:2020):

:   - 7.6.1.8 Static cast [expr.static.cast]

- C++17 standard (ISO/IEC 14882:2017):

:   - 8.2.9 Static cast [expr.static.cast]

- C++14 standard (ISO/IEC 14882:2014):

:   - 5.2.9 Static cast [expr.static.cast]

- C++11 standard (ISO/IEC 14882:2011):

:   - 5.2.9 Static cast [expr.static.cast]

- C++98 standard (ISO/IEC 14882:1998):

:   - 5.2.9 Static cast [expr.static.cast]

- C++03 standard (ISO/IEC 14882:2003):

:   - 5.2.9 Static cast [expr.static.cast]

### See also

- `const_cast`
- `dynamic_cast`
- `reinterpret_cast`
- explicit cast
- implicit conversions
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/static_cast&oldid=175308>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 August 2024, at 22:38.