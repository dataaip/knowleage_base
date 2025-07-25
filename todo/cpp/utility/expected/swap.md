# std::expected<T,E>::swap

From cppreference.com
< cpp‎ | utility‎ | expected
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

Utilities library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

std::expected

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| expected::expected | | | | |
| expected::~expected | | | | |
| expected::operator= | | | | |
| Observers | | | | |
| expected::operator->expected::operator\* | | | | |
| expected::operator boolexpected::has_value | | | | |
| expected::value | | | | |
| expected::error | | | | |
| expected::value_or | | | | |
| expected::error_or | | | | |
| Monadic operations | | | | |
| expected::and_then | | | | |
| expected::or_else | | | | |
| expected::transform | | | | |
| expected::transform_error | | | | |
| Modifiers | | | | |
| expected::emplace | | | | |
| ****expected::swap**** | | | | |
| Non-member functions | | | | |
| operator==(std::expected) | | | | |
| swap(std::expected) | | | | |
| Helper classes | | | | |
| unexpected | | | | |
| bad_expected_access | | | | |
| unexpect_tunexpect | | | | |

|  |  |  |
| --- | --- | --- |
| Primary template |  |  |
| constexpr void swap( expected& other ) noexcept(/\* see below \*/); | (1) | (since C++23) |
| void partial specialization |  |  |
| constexpr void swap( expected& other ) noexcept(/\* see below \*/); | (2) | (since C++23) |
|  |  |  |

Swaps the contents with those of other.

1) The contained values are swapped as follows:

| Value of  `has_value()` | Value of other.has_value() | |
| --- | --- | --- |
| true | false |
| true | using std::swap; swap(`val`, rhs.`val`); | see below |
| false | other.swap(\*this); | using std::swap; swap(`unex`, rhs.`unex`); |

 If `has_value()` is true and other.has_value() is false, equivalent to:

// Case 1: the move constructions of unexpected values are non-throwing:  
// “other.unex” will be restored if the construction of “other.val” fails  
if constexpr (std::is_nothrow_move_constructible_v<E>)  
{  
E temp(std::move(other.`unex`));  
std::destroy_at(std::addressof(other.`unex`));  
try  
{  
std::construct_at(std::addressof(other.`val`), std::move(`val`)); // may throw  
std::destroy_at(std::addressof(`val`));  
std::construct_at(std::addressof(`unex`), std::move(temp));  
}  
catch(...)  
{  
std::construct_at(std::addressof(other.`unex`), std::move(temp));  
throw;  
}  
}  
// Case 2: the move constructions of expected values are non-throwing:  
// “this->val” will be restored if the construction of “this->unex” fails  
else  
{  
T temp(std::move(`val`));  
std::destroy_at(std::addressof(`val`));  
try  
{  
std::construct_at(std::addressof(`unex`), std::move(other.`unex`)); // may throw  
std::destroy_at(std::addressof(other.`unex`));  
std::construct_at(std::addressof(other.`val`), std::move(temp));  
}  
catch(...)  
{  
std::construct_at(std::addressof(`val`), std::move(temp));  
throw;  
}  
}  
`has_val`= false;  
rhs.`has_val`= true;

 This overload participates in overload resolution only if all following values are true:

- std::is_swappable_v<T>
- std::is_swappable_v<E>
- std::is_move_constructible_v<T> && std::is_move_constructible_v<E>
- std::is_nothrow_move_constructible_v<T> || std::is_nothrow_move_constructible_v<E>
2) The unexpected values are swapped as follows:

| Value of  `has_value()` | Value of other.has_value() | |
| --- | --- | --- |
| true | false |
| true | using std::swap; swap(`val`, rhs.`val`); | std::construct_at(std::addressof(`unex`), std::move(rhs.`unex`)); std::destroy_at(std::addressof(rhs.`unex`)); `has_val`= false; rhs.`has_val`= true; |
| false | other.swap(\*this); | using std::swap; swap(`unex`, rhs.`unex`); |

 This overload participates in overload resolution only if std::is_swappable_v<E> and std::is_move_constructible_v<E> are both true.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | the `expected` object to exchange the contents with |

### Exceptions

1)noexcept specification:noexcept(  

std::is_nothrow_move_constructible_v<T> && std::is_nothrow_swappable_v<T> &&  
    std::is_nothrow_move_constructible_v<E> && std::is_nothrow_swappable_v<E>

)2)noexcept specification:noexcept(  

std::is_nothrow_move_constructible_v<E> && std::is_nothrow_swappable_v<E>

)

### Example

Run this code

```
#include <expected>
#include <iostream>
#include <string>
 
using Ex = std::expected<std::string, int>;
 
void show(const Ex& ex1, const Ex& ex2)
{
    for (int i{}; i < 2; ++i)
    {
        std::cout << (i ? "ex2" : "ex1");
        if (const Ex& ex = (i ? ex2 : ex1); ex.has_value())
            std::cout << ".has_value() = " << *ex << '\n';
        else
            std::cout << ".error() = " << ex.error() << '\n';
    }
}
 
int main()
{
    Ex ex1("\N{CAT FACE}");
    Ex ex2{"\N{GREEN HEART}"};
    show(ex1, ex2);
    ex1.swap(ex2);
    std::cout << "ex1.swap(ex2);\n";
    show(ex1, ex2);
    std::cout << '\n';
 
    ex2 = std::unexpected(13);
    show(ex1, ex2);
    std::cout << "ex1.swap(ex2);\n";
    ex1.swap(ex2);
    show(ex1, ex2);
    std::cout << '\n';
 
    ex2 = std::unexpected(19937);
    show(ex1, ex2);
    std::cout << "ex1.swap(ex2);\n";
    ex1.swap(ex2);
    show(ex1, ex2);
}

```

Output:

```
ex1.has_value() = 🐱
ex2.has_value() = 💚
ex1.swap(ex2);
ex1.has_value() = 💚
ex2.has_value() = 🐱
 
ex1.has_value() = 💚
ex2.error() = 13
ex1.swap(ex2);
ex1.error() = 13
ex2.has_value() = 💚
 
ex1.error() = 13
ex2.error() = 19937
ex1.swap(ex2);
ex1.error() = 19937
ex2.error() = 13

```

### See also

|  |  |
| --- | --- |
| swap(std::expected)(C++23) | specializes the std::swap algorithm   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/expected/swap&oldid=173358>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 July 2024, at 10:58.