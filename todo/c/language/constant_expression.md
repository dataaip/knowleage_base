# Constant expressions

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
| ****constant expressions**** | | | | |
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

Several varieties of expressions are known as **constant expressions**

### Preprocessor constant expression

The expression following `#if` or `#elif` must expand to

- operators other than assignment, increment, decrement, function-call, or comma whose arguments are preprocessor constant expressions
- integer constants
- character constants
- the special preprocessor operator `defined`

Character constants, when evaluated in `#if`-expressions, may be interpreted in the source
character set, the execution character set, or some other implementation-defined character set.

|  |  |
| --- | --- |
| Integer arithmetic in `#if`-expressions is performed using the semantics of intmax_t for signed types and uintmax_t for unsigned types. | (since C99) |

### Integer constant expression

An integer constant expression is an expression that consists only of

- operators other than assignment, increment, decrement, function-call, or comma, except that cast operators can only cast arithmetic types to integer types unless they are part of an operand to a sizeof , _Alignof(since C11)(until C23), alignas(since C23) or typeof/typeof_unqual(since C23) operator.
- integer constants
- enumeration constants
- character constants
- floating constants, but only if they are immediately used as operands of casts to integer type
- `sizeof` operators whose operands are not VLA(since C99)

|  |  |
| --- | --- |
| - _Alignof(until C23)alignas(since C23) operators | (since C11) |

|  |  |
| --- | --- |
| - named and compound literal constants that are of integer type or that are of arithmetic type and are the immediate operands of casts | (since C23) |

Integer constant expressions are evaluated at compile time. The following contexts require expressions that are known as **integer constant expressions**:

- The size of a bit-field.
- The value of an enumeration constant
- The `case` label of a switch statement
- The size of a non-VLA(since C99) array
- Integer to pointer implicit conversion.

|  |  |
| --- | --- |
| - The index in an array designator | (since C99) |
| - The first argument of `_Static_assert` - The integer argument of `_Alignof`(until C23)`alignof`(since C23) | (since C11) |
| - The number of bits N of a bit-precise integer type (_BitInt(N)) | (since C23) |

### Static initializer

Expressions that are used in the initializers of objects with static and thread_local storage duration or declared with the constexpr storage-class specifier(since C23) must be either string literals or expressions that may be one of the following

1) **arithmetic constant expression**, which is an expression of any arithmetic type that consists of

:   - operators other than assignment, increment, decrement, function-call, or comma, except that cast operators must be converting arithmetic types to other arithmetic types unless they are part of an operand to a sizeof , _Alignof(since C11)(until C23), alignof(since C23) or typeof/typeof_unqual(since C23) operator
    - integer constants
    - floating constants
    - enumeration constants
    - character constants
    - `sizeof` operators whose operands are not VLA(since C99)

|  |  |
| --- | --- |
| - `_Alignof`(until C23)`alignof`(since C23) operators | (since C11) |

|  |  |
| --- | --- |
| - named or compound literal constants of arithmetic type | (since C23) |

2) a null pointer constant (e.g. NULL)3) **address constant expression**, which is

:   - a null pointer
    - lvalue designating an object of static storage duration or a function designator, converted to a pointer either

    :   - by using the unary address-of operator
        - by casting an integer constant to a pointer
        - by array-to-pointer or function-to-pointer implicit conversion

4) **address constant expression** of some complete object type, plus or minus an **integer constant expression**

|  |  |
| --- | --- |
| 5) a **named constant** which is, an identifier that is - an enumeration constant - a predefined constant (one of true, false or nullptr) - declared with storage-class specifier constexpr and has an object type or a postfix expression that applies the `.` member access operator to a named constant of structure or union type, even recursively.6) a **compound literal constant**, which is - a compound literal with storage-class specifier constexpr - a postfix expression that applies the `.` member access operator to a compound literal constant of structure or union type, even recursively.  A **structure or union constant** is a named constant or compound literal constant with structure or union type, respectively. If the member-access operator `.` accesses a member of a union constant, the accessed member shall be the same as the member that is initialized by the union constant’s initializer. | (since C23) |

7) constant expression of one of the other forms accepted by the implementation.

Unlike with integer constant expressions, static initializer expressions are not required to be evaluated at compile time; the compiler is at liberty to turn such initializers into executable code which is invoked prior to program startup.

```
static int i = 2 || 1 / 0; // initializes i to value 1

```

|  |  |
| --- | --- |
|  | This section is incomplete Reason: other mini-examples |

The value of a floating-point static initializer is never less accurate than the value of the same expression executed at run time, but it may be better.

### Floating-point constant expressions

Arithmetic constant expressions of floating-point types that are not used in static initializers are always evaluated as-if during run-time and are affected by the current rounding (if FENV_ACCESS is on) and report errors as specified in math_errhandling.

```
void f(void)
{
#pragma STDC FENV_ACCESS ON
    static float x = 0.0 / 0.0; // static initializer: does not raise an exception
    float w[] = { 0.0 / 0.0 };  // raises an exception
    float y = 0.0 / 0.0;        // raises an exception
    double z = 0.0 / 0.0;       // raises an exception
}

```

### Notes

If an expression evaluates to a value that is not representable by its type, it cannot be used as a constant expression.

Implementations may accept other forms of constant expressions. However, these constant expressions are not considered as integer constant expressions, arithmetic constant expressions, or address constant expressions, and thus cannot be used in the contexts requiring these kinds of constant expressions. For example, int arr[(int)+1.0]; declares a VLA.

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.6 Constant expressions (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.6 Constant expressions (p: 76-77)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.6 Constant expressions (p: 106-107)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.6 Constant expressions (p: 95-96)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.4 CONSTANT EXPRESSIONS

### See also

|  |  |
| --- | --- |
| C++ documentation for Constant expressions | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/constant_expression&oldid=178464>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 December 2024, at 22:06.