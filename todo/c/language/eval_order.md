# Order of evaluation

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
| ****evaluation order and sequence points**** | | | | |
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
| function call, comma, conditional operator | | | | |
| sizeof | | | | |
| _Alignof(C11\*) | | | | |
| cast operators | | | | |

Order of evaluation of the operands of any C operator, including the order of evaluation of function arguments in a function-call expression, and the order of evaluation of the subexpressions within any expression is unspecified (except where noted below). The compiler will evaluate them in any order, and may choose another order when the same expression is evaluated again.

There is no concept of left-to-right or right-to-left evaluation in C, which is not to be confused with left-to-right and right-to-left associativity of operators: the expression `f1() + f2() + f3()` is parsed as `(f1() + f2()) + f3()` due to left-to-right associativity of operator+, but the function call to `f3` may be evaluated first, last, or between `f1()` or `f2()` at run time.

### Definitions

#### Evaluations

There are two kinds of evaluations performed by the compiler for each expression or subexpression (both of which are optional):

- **value computation**: calculation of the value that is returned by the expression. This may involve determination of the identity of the object (lvalue evaluation) or reading the value previously assigned to an object (rvalue evaluation)
- **side effect**: access (read or write) to an object designated by a volatile lvalue, modification (writing) to an object, atomic synchronization(since C11), modifying a file, modifying the floating-point environment (if supported), or calling a function that does any of those operations.

If no side effects are produced by an expression and the compiler can determine that the value is not used, the expression may not be evaluated.

#### Ordering

"sequenced-before" is an asymmetric, transitive, pair-wise relationship between evaluations within the same thread (it may extend across threads if atomic types and memory barriers are involved).

- If a **sequence point** is present between the subexpressions E1 and E2, then both value computation and side effects of E1 are **sequenced-before** every value computation and side effect of E2

|  |  |
| --- | --- |
| - If evaluation A is sequenced before evaluation B, then evaluation of A will be complete before evaluation of B begins. - If A is not sequenced before B and B is sequenced before A, then evaluation of B will be complete before evaluation of A begins. - If A is not sequenced before B and B is not sequenced before A, then two possibilities exist:   - evaluations of A and B are unsequenced: they may be performed in any order and may overlap (within a single thread of execution, the compiler may interleave the CPU instructions that comprise A and B)   - evaluations of A and B are indeterminably-sequenced: they may be performed in any order but may not overlap: either A will be complete before B, or B will be complete before A. The order may be the opposite the next time the same expression is evaluated. | (since C11) |

### Rules

1) There is a sequence point after the evaluation of all function arguments and of the function designator, and before the actual function call.2) There is a sequence point after evaluation of the first (left) operand and before evaluation of the second (right) operand of the following binary operators: `&&` (logical AND), `||` (logical OR), and `,` (comma).3) There is a sequence point after evaluation of the first (left) operand and before evaluation of the second or third operand (whichever is evaluated) of the conditional operator `?:`4) There is a sequence point after the evaluation of a full expression (an expression that is not a subexpression: typically something that ends with a semicolon or a controlling statement of `if`/`switch`/`while`/`do`) and before the next full expression.

|  |  |
| --- | --- |
| 5) There is a sequence point at the end of a full declarator.6) There is a sequence point immediately before the return of a library function.7) There is a sequence point after the action associated with each conversion specifier in formatted I/O (in particular, it is well-formed for scanf to write different fields into the same variable and for printf to read and modify or modify the same variable more than once using %n)8) There are sequence points before and immediately after each call to a comparison function made by the library functions qsort and bsearch, as well as between any call to the comparison function and the movement of the associated objects made by qsort | (since C99) |
| 9) The value computations (but not the side-effects) of the operands to any operator are sequenced before the value computation of the result of the operator (but not its side-effects).10) The side effect (modification of the left argument) of the direct assignment operator and of all compound assignment operators is sequenced after the value computation (but not the side effects) of both left and right arguments.11) The value computation of the postincrement and postdecrement operators is sequenced before its side-effect.12) A function call that is not sequenced before or sequenced after another function call is indeterminately sequenced (CPU instructions that constitute different function calls cannot be interleaved, even if the functions are inlined)13) In initialization list expressions, all evaluations are indeterminately sequenced14) With respect to an indeterminately-sequenced function call, the operation of compound assignment operators, and both prefix and postfix forms of increment and decrement operators are single evaluations. | (since C11) |

### Undefined behavior

1) If a side effect on a scalar object is unsequenced relative to another side effect on the same scalar object, the behavior is undefined.

```
i = ++i + i++; // undefined behavior
i = i++ + 1; // undefined behavior
f(++i, ++i); // undefined behavior
f(i = -1, i = -1); // undefined behavior

```

2) If a side effect on a scalar object is unsequenced relative to a value computation using the value of the same scalar object, the behavior is undefined.

```
f(i, i++); // undefined behavior
a[i] = i++; // undefined bevahior

```

3) The above rules apply as long as at least one allowable ordering of subexpressions permits such an unsequenced side-effect.

### See also

Operator precedence which defines how expressions are built from their source code representation.

|  |  |
| --- | --- |
| C++ documentation for Order of evaluation | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/eval_order&oldid=159432>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 September 2023, at 19:09.