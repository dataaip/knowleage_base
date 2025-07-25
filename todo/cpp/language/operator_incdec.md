# Increment/decrement operators

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | ****Increment and decrement**** | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

Increment/decrement operators increment or decrement the value of the object.

| Operator name | Syntax | Over​load​able | Prototype examples (for class T) | |
| --- | --- | --- | --- | --- |
| Inside class definition | Outside class definition |
| pre-increment | `++a` | Yes | T& T::operator++(); | T& operator++(T& a); |
| pre-decrement | `--a` | Yes | T& T::operator--(); | T& operator--(T& a); |
| post-increment | `a++` | Yes | T T::operator++(int); | T operator++(T& a, int); |
| post-decrement | `a--` | Yes | T T::operator--(int); | T operator--(T& a, int); |
| ****Notes****   - Prefix versions of the built-in operators return **references** and postfix versions return **values**, and typical user-defined overloads follow the pattern so that the user-defined operators can be used in the same manner as the built-ins. However, in a user-defined operator overload, any type can be used as return type (including void). - The int parameter is a dummy parameter used to differentiate between prefix and postfix versions of the operators. When the user-defined postfix operator is called, the value passed in that parameter is always zero, although it may be changed by calling the operator using function call notation (e.g., a.operator++(2) or operator++(a, 2)). | | | | |

### Prefix operators

The prefix increment and decrement expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `++` expression |  |  |
|  | | | | | | | | | |
| `--` expression |  |  |
|  | | | | | | | | | |

1) prefix increment (pre-increment)2) prefix decrement (pre-decrement)

#### Built-in prefix operators

1) The expression ++x is equivalent to x += 1, with the following exceptions:

|  |  |
| --- | --- |
| - If the type of expression is (possibly volatile-qualified) bool, expression is set to true. Such a increment is deprecated. | (until C++17) |
| - If the type of expression is (possibly cv-qualified) bool, the program is ill-formed. | (since C++17) |
| - If the type of expression is volatile-qualified, the increment is deprecated. | (since C++20) |

2) The expression --x is equivalent to x -= 1, with the following exceptions:

- If the type of expression is (possibly cv-qualified) bool, the program is ill-formed.

|  |  |
| --- | --- |
| - If the type of expression is volatile-qualified, the decrement is deprecated. | (since C++20) |

#### Overloads

In overload resolution against user-defined operators, for every optionally volatile-qualified arithmetic type `A` other than bool, and for every optionally volatile-qualified pointer `P` to optionally cv-qualified object type, the following function signatures participate in overload resolution:

|  |  |  |
| --- | --- | --- |
| A& operator++(A&) |  |  |
| bool& operator++(bool&) |  | (deprecated)(until C++17) |
| P& operator++(P&) |  |  |
| A& operator--(A&) |  |  |
| P& operator--(P&) |  |  |
|  |  |  |

### Postfix operators

The postfix increment and decrement expressions have the form

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| expression `++` |  |  |
|  | | | | | | | | | |
| expression `--` |  |  |
|  | | | | | | | | | |

1) postfix increment (post-increment)2) postfix decrement (post-decrement)

#### Built-in postfix operators

The result of postfix increment or decrement is the value obtained by applying the lvalue-to-rvalue conversion to expression (before modification). The type of the result is the cv-unqualified version of the type of expression.

If expression is not a modifiable lvalue of an arithmetic type other than (possibly cv-qualified) bool(since C++17), or a pointer to a complete object type, the program is ill-formed.

|  |  |
| --- | --- |
| If the type of expression is volatile-qualified, the increment or decrement is deprecated. | (since C++20) |

1) The value of expression is modified as if it were the operand of the prefix `++` operator.2) The value of expression is modified as if it were the operand of the prefix `--` operator.

The value computation of a postfix increment or decrement is sequenced before the modification of expression. With respect to an indeterminately-sequenced function call, the operation of a postfix increment or decrement is a single evaluation.

#### Overloads

In overload resolution against user-defined operators, for every optionally volatile-qualified arithmetic type `A` other than bool, and for every optionally volatile-qualified pointer `P` to optionally cv-qualified object type, the following function signatures participate in overload resolution:

|  |  |  |
| --- | --- | --- |
| A operator++(A&, int) |  |  |
| bool operator++(bool&, int) |  | (deprecated)(until C++17) |
| P operator++(P&, int) |  |  |
| A operator--(A&, int) |  |  |
| P operator--(P&, int) |  |  |
|  |  |  |

#### Example

Run this code

```
#include <iostream>
 
int main()
{
    int n1 = 1;
    int n2 = ++n1;
    int n3 = ++ ++n1;
    int n4 = n1++;
//  int n5 = n1++ ++;   // error
//  int n6 = n1 + ++n1; // undefined behavior
    std::cout << "n1 = " << n1 << '\n'
              << "n2 = " << n2 << '\n'
              << "n3 = " << n3 << '\n'
              << "n4 = " << n4 << '\n';
}

```

Output:

```
n1 = 5
n2 = 2
n3 = 4
n4 = 4

```

### Notes

Because of the side-effects involved, built-in increment and decrement operators must be used with care to avoid undefined behavior due to violations of sequencing rules.

Because a temporary copy of the object is constructed during post-increment and post-decrement, pre-increment or pre-decrement operators are usually more efficient in contexts where the returned value is not used.

### Standard library

Increment and decrement operators are overloaded for many standard library types. In particular, every LegacyIterator overloads operator++ and every LegacyBidirectionalIterator overloads operator--, even if those operators are no-ops for the particular iterator.

|  |  |
| --- | --- |
| overloads for arithmetic types | |
| operator++operator++(int)operator--operator--(int) | increments or decrements the atomic value by one   (public member function of `std::atomic<T>`) |
| operator++operator++(int)operator--operator--(int) | increments or decrements the tick count   (public member function of `std::chrono::duration<Rep,Period>`) |
| overloads for iterator types | |
| operator++operator++(int) | advances the iterator   (public member function of `std::raw_storage_iterator<OutputIt,T>`) |
| operator++operator++(int)operator+=operator+operator--operator--(int)operator-=operator- | advances or decrements the iterator   (public member function of `std::reverse_iterator<Iter>`) |
| operator++operator++(int)operator+=operator+operator--operator--(int)operator-=operator-(C++11) | advances or decrements the iterator   (public member function of `std::move_iterator<Iter>`) |
| operator++operator++(int) | no-op   (public member function of `std::front_insert_iterator<Container>`) |
| operator++operator++(int) | no-op   (public member function of `std::back_insert_iterator<Container>`) |
| operator++operator++(int) | no-op   (public member function of `std::insert_iterator<Container>`) |
| operator++operator++(int) | advances the iterator   (public member function of `std::istream_iterator<T,CharT,Traits,Distance>`) |
| operator++operator++(int) | no-op   (public member function of `std::ostream_iterator<T,CharT,Traits>`) |
| operator++operator++(int) | advances the iterator   (public member function of `std::istreambuf_iterator<CharT,Traits>`) |
| operator++operator++(int) | no-op   (public member function of `std::ostreambuf_iterator<CharT,Traits>`) |
| operator++operator++(int) | advances the iterator to the next match   (public member function of `std::regex_iterator<BidirIt,CharT,Traits>`) |
| operator++operator++(int) | advances the iterator to the next submatch   (public member function of `std::regex_token_iterator<BidirIt,CharT,Traits>`) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 2855 | C++98 | usual arithmetic conversions are applied for built-in pre-increment and pre-decrement, but were not applied for their postfix counterparts[[1]](operator_incdec.html#cite_note-1) | also applied |
| CWG 2901 | C++98 | lvalue-to-rvalue conversions were not applied for built-in post-increment and post-decrement | applied |

1. ↑ The prefix ++x is equivalent to x += 1, and the latter is applicable for usual arithmetic conversions (i.e. yield a common type between decltype(x) and int). However, the effect of the postfix x++ is simply “adding one to x”, there is no binary operator present, so no usual arithmetic conversions will take place.

### See also

Operator precedence

Operator overloading

| Common operators | | | | | | |
| --- | --- | --- | --- | --- | --- | --- |
| assignment | ****increment decrement**** | arithmetic | logical | comparison | member access | other |
| a = b  a += b  a -= b  a \*= b  a /= b  a %= b  a &= b  a |= b  a ^= b  a <<= b  a >>= b | ++a  --a  a++  a-- | +a  -a  a + b  a - b  a \* b  a / b  a % b  ~a  a & b  a | b  a ^ b  a << b  a >> b | !a  a && b  a || b | a == b  a != b  a < b  a > b  a <= b  a >= b  a <=> b | a[...]  \*a  &a  a->b  a.b  a->\*b  a.\*b | function call  a(...) |
| comma  a, b |
| conditional  a ? b : c |
| Special operators | | | | | | |
| static_cast converts one type to another related type  dynamic_cast converts within inheritance hierarchies  const_cast adds or removes cv-qualifiers  reinterpret_cast converts type to unrelated type  C-style cast converts one type to another by a mix of static_cast, const_cast, and reinterpret_cast  new creates objects with dynamic storage duration  delete destructs objects previously created by the new expression and releases obtained memory area  sizeof queries the size of a type  sizeof... queries the size of a pack (since C++11)  typeid queries the type information of a type  noexcept checks if an expression can throw an exception (since C++11)  alignof queries alignment requirements of a type (since C++11) | | | | | | |

|  |  |
| --- | --- |
| C documentation for Increment/decrement operators | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/operator_incdec&oldid=179769>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 January 2025, at 23:20.