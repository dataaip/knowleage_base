# Other operators

From cppreference.com
< c‎ | language
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 C language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic concepts | | | | |
| Keywords | | | | |
| Preprocessor | | | | |
| Statements | | | | |
| Expressions | | | | |
| Initialization | | | | |
| Declarations | | | | |
| Functions | | | | |
| Miscellaneous | | | | |
| History of C | | | | |
| Technical Specifications | | | | |

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| value category | | | | |
| evaluation order and sequence points | | | | |
| constant expressions | | | | |
| implicit conversions | | | | |
| generic selection (C11) | | | | |
| constants and literals | | | | |
| integer constant | | | | |
| floating constant | | | | |
| character constant | | | | |
| true/false(C23) | | | | |
| nullptr(C23) | | | | |
| string literal | | | | |
| compound literal (C99) | | | | |
| operators | | | | |
| operator precedence | | | | |
| member access and indirection | | | | |
| logical operators | | | | |
| comparison operators | | | | |
| arithmetic operators | | | | |
| assignment operators | | | | |
| increment and decrement | | | | |
| ****function call, comma, conditional operator**** | | | | |
| sizeof | | | | |
| _Alignof(C11\*) | | | | |
| cast operators | | | | |

A collection of operators that do not fit into any of the other major categories.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: consider a more general-purpose ToC for this and other tables that cover multiple topics |

| Operator | Operator name | Example | Description |
| --- | --- | --- | --- |
| (...) | function call | f(...) | call the function ****f****(), with zero or more arguments |
| , | comma operator | a, b | evaluate expression ****a****, disregard its return value and complete any side-effects, then evaluate expression ****b****, returning the type and the result of this evaluation |
| (type) | type cast | (type)a | cast the type of ****a**** to ****type**** |
| ? : | conditional operator | a ? b : c | if ****a**** is logically true (does not evaluate to zero) then evaluate expression ****b****, otherwise evaluate expression ****c**** |
| sizeof | sizeof operator | sizeof a | the size in bytes of ****a**** |
| _Alignof (since C11) | _Alignof operator | _Alignof(type) | the alignment required of ****type**** |
| typeof | typeof operators | typeof(a) | the type of ****a**** |

### Function call

The function call expression has the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| expression `(` argument-list ﻿(optional) `)` |  |  |
|  | | | | | | | | | |

where

|  |  |  |
| --- | --- | --- |
| expression | - | any expression of pointer-to-function type (after lvalue conversions) |
| argument-list | - | comma-separated list of expressions (which cannot be comma operators) of any complete object type. May be omitted when calling functions that take no arguments. |

The behavior of the function call expression depends on whether the prototype of the function being called is in scope at the point of call.

#### Call to a function with a prototype

1) The number of parameters must equal the number of arguments (unless the ellipsis parameter is used).2) The type of each parameter must be a type such that implicit conversion as if by assignment exists that converts the unqualified type of the corresponding argument to the type of the parameter.

|  |  |
| --- | --- |
| Additionally, for every parameter of array type that uses the keyword `static` between `[` and `]`, the argument expression must designate a pointer to the element of an array with at least that many elements as specified in the size expression of the parameter. | (since C99) |

3) The arguments are evaluated in unspecified order and without sequencing.4) Assignment is performed to copy the value of each argument to the corresponding function parameter, ignoring any type qualifiers on the parameter type and its possibly recursive elements or members, if any (note: the function can modify its parameters, and those changes do not affect the arguments; C function calls are only call-by-value).

:   - if there is a trailing ellipsis parameter, Default argument promotions") are performed on the remaining arguments, which are made available to va_list.

5) Function is executed, and the value it returns becomes the value of the function call expression (if the function returns void, the function call expression is a void expression)

```
void f(char* p, int x) {}
int main(void)
{
    f("abc", 3.14); // array to pointer and float to int conversions
}

```

|  |  |
| --- | --- |
| Call to a function without a prototype1) The arguments are evaluated in unspecified order and without sequencing.2) Default argument promotions are performed on every argument expression.3) Assignment is performed to copy the value of each argument to the corresponding function parameter, ignoring any type qualifiers on the parameter type and its possibly recursive elements or members, if any.4) Function is executed, and the value it returns becomes the value of the function call expression (if the function returns void, the function call expression is a void expression)  ```text void f(); // no prototype int main(void) {     f(1, 1.0f); // UB unless f is defined to take an int and a double } void f(int a, double c) {} ```   The behavior of a function call to a function without a prototype is undefined if   - the number of arguments does not match the number of parameters. - the promoted types of the arguments are not compatible with the promoted types of the parameters except that   - signed and unsigned versions of the same integer type are considered compatible if the value of the argument is representable by both types. - pointers to void and pointers to (possibly cvr-qualified) character types are considered compatible | (until C23) |

#### Notes

The evaluations of expression that designates the function to be called and all arguments are unsequenced with respect to each other (but there is a sequence point before the body of the function begins executing)

```
(*pf[f1()]) (f2(), f3() + f4()); // f1, f2, f3, f4 may be called in any order

```

Although function call is only defined for pointers to functions, it works with function designators due to the function-to-pointer implicit conversion.

```
int f(void) { return 1; }
int (*pf)(void) = f;
 
int main(void)
{
    f();    // convert f to pointer, then call
    (&f)(); // create a pointer to function, then call
 
    pf();    // call the function
    (*pf)(); // obtain the function designator, convert to pointer, then calls
 
    (****f)(); // convert to pointer, obtain the function, repeat 4x, then call
    (****pf)(); // also OK
}

```

Functions that ignore unused arguments, such as printf, must be called with a prototype in scope (the prototype of such functions necessarily uses the trailing ellipsis parameter) to avoid invoking undefined behavior.

The current standard wording of the semantics of preparing function parameters is defective, because it specifies that parameters are assigned from arguments while calling, which incorrectly rejects const-qualified parameter or member types, and inappropriately applies the semantics of volatile which is unimplementable for function parameters on many platforms. A post-C11 defect report DR427 proposed change of such semantics from assignment to initialization, but was closed as not-a-defect.

|  |  |
| --- | --- |
| A function call expression where expression consists entirely of an identifier and that identifier is undeclared acts as though the identifier is declared as   ```text extern int identifier(); // returns int and has no prototype ```   So the following complete program is valid C89:   ```text main() {     int n = atoi("123"); // implicitly declares atoi as int atoi() } ``` | (until C99) |

### Comma operator

The comma operator expression has the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs `,` rhs |  |  |
|  | | | | | | | | | |

where

|  |  |  |
| --- | --- | --- |
| lhs | - | any expression |
| rhs | - | any expression other than another comma operator (in other words, comma operator's associativity is left-to-right) |

First, the left operand, lhs, is evaluated and its result value is discarded.

Then, a sequence point takes place, so that all side effects of lhs are complete.

Then, the right operand, rhs, is evaluated and its result is returned by the comma operator as a non-lvalue.

### Notes

The type of the lhs may be void (that is, it may be a call to a function that returns void, or it can be an expression cast to void)

The comma operator may be lvalue in C++, but never in C

The comma operator may return a struct (the only other expressions that return structs are compound literals, function calls, assignments, and the conditional operator)

In the following contexts, the comma operator cannot appear at the top level of an expression because the comma has a different meaning:

- argument list in a function call
- initializer expression or initializer list
- generic selection

If the comma operator has to be used in such context, it must be parenthesized:

```
// int n = 2,3; // error, comma assumed to begin the next declarator
// int a[2] = {1,2,3}; // error: more initializers than elements
int n = (2,3), a[2] = {(1,2),3}; // OK
 
f(a, (t=3, t+2), c); // OK, first, stores 3 in t, then calls f with three arguments

```

Top-level comma operator is also disallowed in array bounds

```
// int a[2,3]; // error
int a[(2,3)]; // OK, VLA array of size 3 (VLA because (2,3) is not a constant expression)

```

Comma operator is not allowed in constant expressions, regardless of whether it's on the top level or not

```
// static int n = (1,2); // Error: constant expression cannot call the comma operator

```

### Cast operator

See cast operator

### Conditional operator

The conditional operator expression has the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| condition `?` expression-true `:` expression-false |  |  |
|  | | | | | | | | | |

where

|  |  |  |
| --- | --- | --- |
| condition | - | an expression of scalar type |
| expression-true | - | the expression that will be evaluated if condition compares unequal to zero |
| expression-false | - | the expression that will be evaluated if condition compares equal to zero |

Only the following expressions are allowed as expression-true and expression-false

- two expressions of any arithmetic type
- two expressions of the same struct or union type
- two expressions of void type
- two expressions of pointer type, pointing to types that are compatible, ignoring cvr-qualifiers

|  |  |
| --- | --- |
| - two expressions of nullptr_t type | (since C23) |

- one expression is a pointer and the other is the null pointer constant (such as NULL)or a nullptr_t value(since C23)
- one expression is a pointer to object and the other is a pointer to void (possibly qualified)

1) First, evaluates condition. There is a sequence point after this evaluation.2) If the result of condition compares unequal to zero, executes expression-true, otherwise executes expression-false3) Performs a conversion from the result of the evaluation to the **common type**, defined as follows:1) if the expressions have arithmetic type, the common type is the type after usual arithmetic conversions2) if the expressions have struct/union type, the common type is that struct/union type3) if the expressions are both void, the entire conditional operator expression is a void expression4) if one is a pointer and the other is a null pointer constantor a nullptr_t value(since C23), the type is the type of that pointer5) if both are pointers, the result is the pointer to the type that combines cvr-qualifiers of both pointed-to types (that is, if one is const int\* and the other is volatile int\*, the result is const volatile int\*), and if the types were different, the pointed-to type is the composite type.6) if one is a pointer to void, the result is a pointer to void with combined cvr-qualifiers

|  |  |
| --- | --- |
| 7) if both have nullptr_t type, the common type is also nullptr_t | (since C23) |

```
#define ICE(x) (sizeof(*(1 ? ((void*)((x) * 0l)) : (int*)1)))
 
// if x is an Integer Constant Expression then macro expands to
 
sizeof(*(1 ? NULL : (int *) 1))  // (void *)((x)*0l)) -> NULL
 
// according to point (4) this further converts into
 
sizeof(int)
 
// if x is not an Integer Constant Expression then macro expands to
// according to point (6)
 
(sizeof(*(void *)(x))           // Error due incomplete type

```

#### Notes

The conditional operator is never an lvalue expression, although it may return objects of struct/union type. The only other expressions that may return structs are assignment, comma, function call, and compound literal.

Note that in C++, it may be an lvalue expression.

See operator precedence for the details on the relative precedence of this operator and assignment.

Conditional operator has right-to-left associativity, which allows chaining

Run this code

```
#include <assert.h>
 
enum vehicle { bus, airplane, train, car, horse, feet };
 
enum vehicle choose(char arg)
{
    return arg == 'B' ? bus      :
           arg == 'A' ? airplane :
           arg == 'T' ? train    :
           arg == 'C' ? car      :
           arg == 'H' ? horse    :
                        feet     ;
}
 
int main(void)
{
    assert(choose('H') == horse && choose('F') == feet);
}

```

### `sizeof` operator

See sizeof operator

### `_Alignof` operator

See _Alignof operator

### `typeof` operators

See typeof operators

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.5.2.2 Function calls (p: TBD)

:   - 6.5.3.4 The sizeof and _Alignof operators (p: TBD)

:   - 6.5.4 Cast operators (p: TBD)

:   - 6.5.15 Conditional operator (p: TBD)

:   - 6.5.17 Comma operator (p: TBD)

:   - 6.7.3.5 Typeof specifiers (p: 115-118)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.5.2.2 Function calls (p: 58-59)

:   - 6.5.3.4 The sizeof and _Alignof operators (p: 64-65)

:   - 6.5.4 Cast operators (p: 65-66)

:   - 6.5.15 Conditional operator (p: 71-72)

:   - 6.5.17 Comma operator (p: 75)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.5.2.2 Function calls (p: 81-82)

:   - 6.5.3.4 The sizeof and _Alignof operators (p: 90-91)

:   - 6.5.4 Cast operators (p: 91)

:   - 6.5.15 Conditional operator (p: 100)

:   - 6.5.17 Comma operator (p: 105)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.5.2.2 Function calls (p: 71-72)

:   - 6.5.3.4 The sizeof operator (p: 80-81)

:   - 6.5.4 Cast operators (p: 81)

:   - 6.5.15 Conditional operator (p: 90-91)

:   - 6.5.17 Comma operator (p: 94)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.3.2.2 Function calls

:   - 3.3.3.4 The sizeof operator

:   - 3.3.4 Cast operators

:   - 3.3.15 Conditional operator

:   - 3.3.17 Comma operator

### See also

- Operator precedence

| Common operators | | | | | | |
| --- | --- | --- | --- | --- | --- | --- |
| assignment | increment decrement | arithmetic | logical | comparison | member access | ****other**** |
| a = b  a += b  a -= b  a \*= b  a /= b  a %= b  a &= b  a |= b  a ^= b  a <<= b  a >>= b | ++a  --a  a++  a-- | +a  -a  a + b  a - b  a \* b  a / b  a % b  ~a  a & b  a | b  a ^ b  a << b  a >> b | !a  a && b  a || b | a == b  a != b  a < b  a > b  a <= b  a >= b | a[b]  \*a  &a  a->b  a.b | a(...)  a, b  (type) a  a ? b : c  sizeof   _Alignof (since C11) (until C23)   alignof (since C23) |

|  |  |
| --- | --- |
| C++ documentation for Other operators | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/operator_other&oldid=161471>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 October 2023, at 14:33.