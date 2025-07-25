# operator==, !=, <, <=, >, >=, <=>(std::variant)

From cppreference.com
< cpp‎ | utility‎ | variant
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

std::variant

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| variant::variant | | | | |
| variant::~variant | | | | |
| variant::operator= | | | | |
| Observers | | | | |
| variant::index | | | | |
| variant::valueless_by_exception | | | | |
| Modifiers | | | | |
| variant::emplace | | | | |
| variant::swap | | | | |
| Visitation | | | | |
| variant::visit(C++26) | | | | |
| Non-member functions | | | | |
| visit(std::variant) | | | | |
| holds_alternative | | | | |
| get(std::variant) | | | | |
| get_if | | | | |
| ****operator==operator!=operator<operator<=operator>operator>=operator<=>****(C++20) | | | | |
| swap(std::variant) | | | | |
| Helper classes | | | | |
| monostate | | | | |
| bad_variant_access | | | | |
| variant_size | | | | |
| variant_alternative | | | | |
| hash<std::variant> | | | | |
| Helper objects | | | | |
| variant_npos | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<variant>` |  |  |
| template< class... Types >  constexpr bool operator==( const std::variant<Types...>& lhs, const std::variant<Types...>& rhs ); | (1) | (since C++17) |
| template< class... Types >  constexpr bool operator!=( const std::variant<Types...>& lhs, const std::variant<Types...>& rhs ); | (2) | (since C++17) |
| template< class... Types >  constexpr bool operator<( const std::variant<Types...>& lhs, const std::variant<Types...>& rhs ); | (3) | (since C++17) |
| template< class... Types >  constexpr bool operator>( const std::variant<Types...>& lhs, const std::variant<Types...>& rhs ); | (4) | (since C++17) |
| template< class... Types >  constexpr bool operator<=( const std::variant<Types...>& lhs, const std::variant<Types...>& rhs ); | (5) | (since C++17) |
| template< class... Types >  constexpr bool operator>=( const std::variant<Types...>& lhs, const std::variant<Types...>& rhs ); | (6) | (since C++17) |
| template< class... Types >  constexpr std::common_comparison_category_t                <std::compare_three_way_result_t<Types>...>      operator<=>( const std::variant<Types...>& lhs, const std::variant<Types...>& rhs ); | (7) | (since C++20) |
| Helper function template |  |  |
| template< std::size_t I, class... Types >  constexpr const std::variant_alternative_t<I, std::variant<Types...>>&     GET( const variant<Types...>& v ); | (8) | (exposition only\*) |
|  |  |  |

Performs comparison operations on std::variant objects.

1-7) Compares two std::variant objects lhs and rhs. The contained values are compared (using the corresponding operator of `T`) only if both lhs and rhs contain values corresponding to the same index. Otherwise,

- lhs is considered **equal to** rhs if, and only if, both lhs and rhs do not contain a value.
- lhs is considered **less than** rhs if, and only if, either rhs contains a value and lhs does not, or lhs.index() is less than rhs.index().
1-6) Let @ denote the corresponding comparison operator, for each of these functions:

|  |  |
| --- | --- |
| If, for some values of I, the corresponding expression `GET` ﻿<I>(lhs) @`GET` ﻿<I>(rhs) is ill-formed or its result is not convertible to bool, the program is ill-formed. | (until C++26) |
| This overload participates in overload resolution only if for all values of I, the corresponding expression `GET` ﻿<I>(lhs) @`GET` ﻿<I>(rhs) is well-formed and its result is convertible to bool. | (since C++26) |

8) The exposition-only function template `GET` behaves like `std::get(std::variant)`, except that std::bad_variant_access is never thrown. If I < sizeof...(Types) is false, the program is ill-formed. If I == v.index() is false, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs,rhs | - | variants to compare |

### Return value

| Operator | Both operands contains a value (let I be lhs.index() and J be rhs.index()) | | lhs or rhs is valueless (let lhs_empty be lhs.valueless_by_exception() and rhs_empty be rhs.valueless_by_exception()) |
| --- | --- | --- | --- |
| I and J are equal | I and J are unequal |
| == | `GET` ﻿<I>(lhs) ==`GET` ﻿<I>(rhs) | false | lhs_empty && rhs_empty |
| != | `GET` ﻿<I>(lhs) !=`GET` ﻿<I>(rhs) | true | lhs_empty != rhs_empty |
| < | `GET` ﻿<I>(lhs) <`GET` ﻿<I>(rhs) | lhs.index() < rhs.index() | lhs_empty && !rhs_empty |
| > | `GET` ﻿<I>(lhs) >`GET` ﻿<I>(rhs) | lhs.index() > rhs.index() | !lhs_empty && rhs_empty |
| <= | `GET` ﻿<I>(lhs) <=`GET` ﻿<I>(rhs) | lhs.index() < rhs.index() | lhs_empty |
| >= | `GET` ﻿<I>(lhs) >=`GET` ﻿<I>(rhs) | lhs.index() > rhs.index() | rhs_empty |
| <=> | `GET` ﻿<I>(lhs) <=>`GET` ﻿<I>(rhs) | lhs.index() <=> rhs.index() | see below |

For operator<=>:

- If only lhs is valueless, returns std::strong_ordering::less.
- If only rhs is valueless, returns std::strong_ordering::greater.
- If both lhs and rhs are valueless, returns std::strong_ordering::equal.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_constrained_equality` | `202403L` | (C++26) | constrained comparison operators for std::variant |

### Example

Run this code

```
#include <iostream>
#include <string>
#include <variant>
 
int main()
{
    std::cout << std::boolalpha;
    std::string cmp;
    bool result;
 
    auto print2 = &cmp, &result
    {
        std::cout << lhs << ' ' << cmp << ' ' << rhs << " : " << result << '\n';
    };
 
    std::variant<int, std::string> v1, v2;
 
    std::cout << "operator==\n";
    {
        cmp = "==";
 
        // by default v1 = 0, v2 = 0;
        result = v1 == v2; // true
        std::visit(print2, v1, v2);
 
        v1 = v2 = 1;
        result = v1 == v2; // true
        std::visit(print2, v1, v2);
 
        v2 = 2;
        result = v1 == v2; // false
        std::visit(print2, v1, v2);
 
        v1 = "A";
        result = v1 == v2; // false: v1.index == 1, v2.index == 0
        std::visit(print2, v1, v2);
 
        v2 = "B";
        result = v1 == v2; // false
        std::visit(print2, v1, v2);
 
        v2 = "A";
        result = v1 == v2; // true
        std::visit(print2, v1, v2);
    }
 
    std::cout << "operator<\n";
    {
        cmp = "<";
 
        v1 = v2 = 1;
        result = v1 < v2; // false
        std::visit(print2, v1, v2);
 
        v2 = 2;
        result = v1 < v2; // true
        std::visit(print2, v1, v2);
 
        v1 = 3;
        result = v1 < v2; // false
        std::visit(print2, v1, v2);
 
        v1 = "A"; v2 = 1;
        result = v1 < v2; // false: v1.index == 1, v2.index == 0
        std::visit(print2, v1, v2);
 
        v1 = 1; v2 = "A";
        result = v1 < v2; // true: v1.index == 0, v2.index == 1
        std::visit(print2, v1, v2);
 
        v1 = v2 = "A";
        result = v1 < v2; // false
        std::visit(print2, v1, v2);
 
        v2 = "B";
        result = v1 < v2; // true
        std::visit(print2, v1, v2);
 
        v1 = "C";
        result = v1 < v2; // false
        std::visit(print2, v1, v2);
    }
 
    {
        std::variant<int, std::string> v1;
        std::variant<std::string, int> v2;
    //  v1 == v2; // Compilation error: no known conversion
    }
 
    // TODO: C++20 three-way comparison operator <=> for variants
}

```

Output:

```
operator==
0 == 0 : true
1 == 1 : true
1 == 2 : false
A == 2 : false
A == B : false
A == A : true
operator<
1 < 1 : false
1 < 2 : true
3 < 2 : false
A < 1 : false
1 < A : true
A < A : false
A < B : true
C < B : false

```

### See also

|  |  |
| --- | --- |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++17)(C++17)(C++17)(C++17)(C++17)(C++17)(C++20) | compares `optional` objects   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/variant/operator_cmp&oldid=179395>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 January 2025, at 00:04.