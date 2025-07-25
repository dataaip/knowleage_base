# Fold expressions (since C++17)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | ****Fold expressions**** (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

 Templates

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Parameters and arguments | | | | |
| Class templates | | | | |
| Function templates | | | | |
| Class member templates | | | | |
| Variable templates (C++14) | | | | |
| Template argument deduction | | | | |
| Class template argument deduction (C++17) | | | | |
| Explicit (full) specialization | | | | |
| Partial specialization | | | | |
| Dependent names | | | | |
| Packs (C++11) | | | | |
| `sizeof...` (C++11) | | | | |
| ****Fold expressions**** (C++17) | | | | |
| Pack indexing (C++26) | | | | |
| SFINAE | | | | |
| Constraints and concepts (C++20) | | | | |
| Requires expression (C++20) | | | | |

Reduces (folds "enwiki:Fold (higher-order function)")) a pack over a binary operator.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `(` pack op `... )` | (1) |  |
|  | | | | | | | | | |
| `( ...` op pack `)` | (2) |  |
|  | | | | | | | | | |
| `(` pack op `...` op init `)` | (3) |  |
|  | | | | | | | | | |
| `(` init op `...` op pack `)` | (4) |  |
|  | | | | | | | | | |

1) Unary right fold.2) Unary left fold.3) Binary right fold.4) Binary left fold.

|  |  |  |
| --- | --- | --- |
| op | - | any of the following 32 **binary** operators: + - \* / % ^ & | = < > << >> += -= \*= /= %= ^= &= |= <<= >>= == != <= >= && || , .\* ->\*. In a binary fold, both ops must be the same. |
| pack | - | an expression that contains an unexpanded pack and does not contain an operator with precedence lower than cast at the top level (formally, a cast-expression) |
| init | - | an expression that does not contain an unexpanded pack and does not contain an operator with precedence lower than cast at the top level (formally, a cast-expression) |

Note that the opening and closing parentheses are a required part of the fold expression.

### Explanation

The instantiation of a **fold expression** expands the expression e as follows:

1) Unary right fold `(E` op `...)` becomes `(E1` op `(`... op `(EN-1` op `EN)))`2) Unary left fold `(...` op `E)` becomes `(((E1` op `E2)` op ...`)` op `EN)`3) Binary right fold `(E` op `...` op `I)` becomes `(E1` op `(`... op `(EN−1` op `(EN` op `I))))`4) Binary left fold `(I` op `...` op `E)` becomes `((((I` op `E1)` op `E2)` op ...`)` op `EN)`

(where `N` is the number of elements in the pack expansion)

For example,

```
template<typename... Args>
bool all(Args... args) { return (... && args); }
 
bool b = all(true, true, true, false);
// within all(), the unary left fold expands as
//  return ((true && true) && true) && false;
// b is false

```

When a unary fold is used with a pack expansion of length zero, only the following operators are allowed:

1) Logical AND (&&). The value for the empty pack is true.2) Logical OR (||). The value for the empty pack is false.3) The comma operator (,). The value for the empty pack is void().

### Notes

If the expression used as init or as pack has an operator with precedence below cast at the top level, it must be parenthesized:

```
template<typename... Args>
int sum(Args&&... args)
{
//  return (args + ... + 1 * 2);   // Error: operator with precedence below cast
    return (args + ... + (1 * 2)); // OK
}

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_fold_expressions` | `201603L` | (C++17) | Fold expressions |

### Example

Run this code

```
#include <climits>
#include <concepts>
#include <cstdint>
#include <iostream>
#include <limits>
#include <type_traits>
#include <utility>
#include <vector>
 
// Basic usage, folding variadic arguments over operator<< 
template<typename... Args>
void printer(Args&&... args)
{
    (std::cout << ... << args) << '\n';
}
 
// Folding an expression that uses the pack directly over operator,
template<typename... Ts>
void print_limits()
{
    ((std::cout << +std::numeric_limits<Ts>::max() << ' '), ...) << '\n';
}
 
// Both a fold over operator&& using the pack
// and over operator, using the variadic arguments
template<typename T, typename... Args>
void push_back_vec(std::vector<T>& v, Args&&... args)
{
    static_assert((std::is_constructible_v<T, Args&&> && ...));
    (v.push_back(std::forward<Args>(args)), ...);
}
 
// Using an integer sequence to execute an expression
// N times by folding a lambda over operator,
template<class T, std::size_t... dummy_pack>
constexpr T bswap_impl(T i, std::index_sequence<dummy_pack...>)
{
    T low_byte_mask = static_cast<unsigned char>(-1);
    T ret{};
    ([&]
    {
        (void)dummy_pack;
        ret <<= CHAR_BIT;
        ret |= i & low_byte_mask;
        i >>= CHAR_BIT;
    }(), ...);
    return ret;
}
 
constexpr auto bswap(std::unsigned_integral auto i)
{
    return bswap_impl(i, std::make_index_sequence<sizeof(i)>{});
}
 
int main()
{
    printer(1, 2, 3, "abc");
    print_limits<uint8_t, uint16_t, uint32_t>();
 
    std::vector<int> v;
    push_back_vec(v, 6, 2, 45, 12);
    push_back_vec(v, 1, 2, 9);
    for (int i : v)
        std::cout << i << ' ';
    std::cout << '\n';
 
    static_assert(bswap<std::uint16_t>(0x1234u) == 0x3412u);
    static_assert(bswap<std::uint64_t>(0x0123456789abcdefull) == 0xefcdab8967452301ULL);
}

```

Output:

```
123abc
255 65535 4294967295 
6 2 45 12 1 2 9

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 7.5.6 Fold expressions [expr.prim.fold]

- C++20 standard (ISO/IEC 14882:2020):

:   - 7.5.6 Fold expressions [expr.prim.fold]

- C++17 standard (ISO/IEC 14882:2017):

:   - 8.1.6 Fold expressions [expr.prim.fold]

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 2611 | C++17 | the expansion results of fold expressions were not enclosed with parentheses | enclosed with parentheses |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/fold&oldid=178139>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 December 2024, at 22:13.