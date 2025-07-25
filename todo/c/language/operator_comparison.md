# Comparison operators

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
| ****comparison operators**** | | | | |
| arithmetic operators | | | | |
| assignment operators | | | | |
| increment and decrement | | | | |
| function call, comma, conditional operator | | | | |
| sizeof | | | | |
| _Alignof(C11\*) | | | | |
| cast operators | | | | |

Comparison operators are binary operators that test a condition and return ****1**** if that condition is logically ****true**** and ****0**** if that condition is ****false****.

| Operator | Operator name | Example | Description |
| --- | --- | --- | --- |
| == | equal to | a == b | ****a**** is equal to ****b**** |
| != | not equal to | a != b | ****a**** is not equal to ****b**** |
| < | less than | a < b | ****a**** is less than ****b**** |
| > | greater than | a > b | ****a**** is greater than ****b**** |
| <= | less than or equal to | a <= b | ****a**** is less than or equal to ****b**** |
| >= | greater than or equal to | a >= b | ****a**** is greater than or equal to ****b**** |

### Relational operators

The relational operator expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs `<` rhs | (1) |  |
|  | | | | | | | | | |
| lhs `>` rhs | (2) |  |
|  | | | | | | | | | |
| lhs `<=` rhs | (3) |  |
|  | | | | | | | | | |
| lhs `>=` rhs | (4) |  |
|  | | | | | | | | | |

1) less-than expression2) greater-than expression3) less or equal expression4) greater or equal expression

where

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | expressions that both have real type or both have pointer to object type |

The type of any relational operator expression is int, and its value (which is not an lvalue) is 1 when the specified relationship holds true and ​0​ when the specified relationship does not hold.

If lhs and rhs are expressions of any real type, then

- usual arithmetic conversions are performed
- the values of the operands after conversion are compared in the usual mathematical sense (except that positive and negative zeroes compare equal and any comparison involving a NaN value returns zero)

Note that complex and imaginary numbers cannot be compared with these operators.

If lhs and rhs are expressions of pointer type, they must be both pointers to objects of compatible types, except that qualifications of the pointed-to objects are ignored.

- a pointer to an object that is not an element of an array is treated as if it were pointing to an element of an array with one element
- if two pointers point to the same object, or both point one past the end of the same array, they compare equal
- if two pointers point to different elements of the same array, the one pointing at the element with the larger index compares greater.
- if one pointer points to the element of an array and the other pointer points one past the end of the same array, the one-past-the-end pointer compares greater
- if the two pointers point to members of the same struct, the pointer to the member declared later in the struct definition compares greater than then pointer to the member declared earlier.
- pointers to members of the same union compare equal
- all other pointer comparisons invoke undefined behavior

Run this code

```
#include <assert.h>
int main(void)
{
    assert(1 < 2);
    assert(2+2 <= 4.0); // int converts to double, two 4.0's compare equal
 
    struct { int x,y; } s;
    assert(&s.x < &s.y); // struct members compare in order of declaration
 
    double d = 0.0/0.0; // NaN
    assert( !(d < d) );
    assert( !(d > d) );
    assert( !(d <= d) );
    assert( !(d >= d) );
    assert( !(d == d) );
 
    float f = 0.1; // f = 0.100000001490116119384765625
    double g = 0.1; // g = 0.1000000000000000055511151231257827021181583404541015625
    assert(f > g); // different values
}

```

### Equality operators

The equality operator expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| lhs `==` rhs | (1) |  |
|  | | | | | | | | | |
| lhs `!=` rhs | (2) |  |
|  | | | | | | | | | |

1) equal-to expression2) not equal to expression

where

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| lhs, rhs | - | expressions that  - both have any arithmetic types (including complex and imaginary)  |  |  | | --- | --- | | - both have type nullptr_t - one has type nullptr_t and the other is a null pointer constant | (since C23) |  - both are pointers to objects or functions of compatible types, ignoring qualifiers of the pointed-to types - one is a pointer to object and the other is a pointer to (possibly qualified) void - one is a pointer to object or function and the other is a null pointer constant such as NULL or nullptr(since C23) |

The type of any equality operator expression is int, and its value (which is not an lvalue) is 1 when the specified relationship holds true and ​0​ when the specified relationship does not hold.

- if both operands have arithmetic types, usual arithmetic conversions are performed and the resulting values are compared in the usual mathematical sense (except that positive and negative zeroes compare equal and any comparison involving a NaN value, including equality with itself, returns zero). In particular, values of complex type are equal if their real parts compare equal and their imaginary parts compare equal.

|  |  |
| --- | --- |
| - two nullptr_t value or one nullptr_t value and a null pointer constant compare equal | (since C23) |

- if one operand is a pointer and the other is a null pointer constant, the null pointer constant is first converted to the type of the pointer (which gives a null pointer value), and the two pointers are compared as described below
- if one operand is a pointer and the other is a pointer to void, the non-void pointer is converted to the pointer to void and the two pointers are compared as described below
- two pointers compare equal if any of the following is true:

:   - they are both null pointer values of their type
    - they are both pointers to the same object or function
    - one pointer is to a struct/union/array object and the other is to its first member/any member/first element
    - they are both pointing one past the last element of the same array
    - one is one past the end of an array, and the other is at the start of a different array (of the same type) that follows the first in a larger array or in a struct with no padding

(as with relational operators, pointers to objects that aren't elements of any array behave as pointers to elements of arrays of size 1)

#### Notes

Objects of struct type do not compare equal automatically, and comparing them with memcmp is not reliable because the padding bytes may have any values.

Because pointer comparison works with pointers to void, the macro NULL may be defined as (void\*)0 in C, although that would be invalid in C++ where void pointers do not implicitly convert to typed pointers

Care must be taken when comparing floating-point values for equality, because the results of many operations cannot be represented exactly and must be rounded. In practice, floating-point numbers are usually compared allowing for the difference of one or more units of the last place.

Run this code

```
#include <assert.h>
int main(void)
{
    assert(2+2 == 4.0); // int converts to double, two 4.0's compare equal
 
    int n[2][3] = {1,2,3,4,5,6};
    int* p1 = &n[0][2]; // last element in the first row
    int* p2 = &n[1][0]; // start of second row
    assert(p1+1 == p2); // compare equal
 
    double d = 0.0/0.0; // NaN
    assert( d != d ); // NaN does not equal itself
 
    float f = 0.1; // f = 0.100000001490116119384765625
    double g = 0.1; // g = 0.1000000000000000055511151231257827021181583404541015625
    assert(f != g); // different values
}

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.5.8 Relational operators (p: 68-69)

:   - 6.5.9 Equality operators (p: 69-70)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.5.8 Relational operators (p: 95-96)

:   - 6.5.9 Equality operators (p: 96-97)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.5.8 Relational operators (p: 85-86)

:   - 6.5.9 Equality operators (p: 86-87)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.3.8 Relational operators

:   - 3.3.9 Equality operators

### See also

Operator precedence

| Common operators | | | | | | |
| --- | --- | --- | --- | --- | --- | --- |
| assignment | increment decrement | arithmetic | logical | ****comparison**** | member access | other |
| a = b  a += b  a -= b  a \*= b  a /= b  a %= b  a &= b  a |= b  a ^= b  a <<= b  a >>= b | ++a  --a  a++  a-- | +a  -a  a + b  a - b  a \* b  a / b  a % b  ~a  a & b  a | b  a ^ b  a << b  a >> b | !a  a && b  a || b | a == b  a != b  a < b  a > b  a <= b  a >= b | a[b]  \*a  &a  a->b  a.b | a(...)  a, b  (type) a  a ? b : c  sizeof   _Alignof (since C11) (until C23)   alignof (since C23) |

|  |  |
| --- | --- |
| C++ documentation for Comparison operators | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/operator_comparison&oldid=152706>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 2 June 2023, at 12:02.