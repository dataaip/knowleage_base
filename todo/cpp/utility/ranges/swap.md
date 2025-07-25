# std::ranges::swap

From cppreference.com
< cpp‎ | utility
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ****ranges::swap****(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<concepts>` |  |  |
| namespace ranges {  inline namespace /\* unspecified \*/ {          inline constexpr /\* unspecified \*/ swap = /\* unspecified \*/;      } } |  | (since C++20)  (customization point object) |
| Call signature |  |  |
| template< class T, class U >  constexpr void ranges::swap( T&& t, U&& u ) noexcept(/\* see below \*/); |  | (since C++20) |
|  |  |  |

Exchanges the values referenced by t and u.

ranges::swap(t, u) is expression-equivalent to:

1. (void)swap(t, u), if t or u has class or enumeration type, and that expression is valid, where the overload resolution is performed within namespace `std::ranges` with the additional candidate template<class T> void swap(T&, T&) = delete;.
   - If the function selected by overload resolution does not exchange the values referenced by t and u, the program is ill-formed; no diagnostic required.
2. Otherwise, (void)ranges::swap_ranges(t, u), if t and u are lvalue arrays of equal extent (but possibly different element types) and ranges::swap(\*t, \*u) is a valid expression, except that noexcept((void)ranges::swap_ranges(t, u)) is equal to noexcept(ranges::swap(\*t, \*u)).
3. Otherwise, an expression which exchanges the referenced values of t and u, if they are both lvalues of the same type `V` that models std::move_constructible<V> and std::assignable_from<V&, V>.
   - The result of applying the `noexcept` operator to that expression is equal to std::is_nothrow_move_constructible_v<V> && std::is_nothrow_move_assignable_v<V>.
   - That expression is a constant expression if
     - `V` is a LiteralType,
     - both t = std::move(u)) and u = std::move(t) are constant subexpressions, and
     - the full-expressions of the initializers in the following declarations are constant subexpressions:
       - V v1(std::move(t));
       - V v2(std::move(u));
4. Otherwise, ranges::swap(t, u) is ill-formed, which can result in substitution failure when ranges::swap(t, u) appears in the immediate context of a template instantiation.

### Customization point objects

The name `ranges::swap` denotes a **customization point object**, which is a const function object of a literal `semiregular` class type. For exposition purposes, the cv-unqualified version of its type is denoted as `__swap_fn`.

All instances of `__swap_fn` are equal. The effects of invoking different instances of type `__swap_fn` on the same arguments are equivalent, regardless of whether the expression denoting the instance is an lvalue or rvalue, and is const-qualified or not (however, a volatile-qualified instance is not required to be invocable). Thus, `ranges::swap` can be copied freely and its copies can be used interchangeably.

Given a set of types `Args...`, if std::declval<Args>()... meet the requirements for arguments to `ranges::swap` above, `__swap_fn` models

- std::invocable<__swap_fn, Args...>,
- std::invocable<const __swap_fn, Args...>,
- std::invocable<__swap_fn&, Args...>, and
- std::invocable<const __swap_fn&, Args...>.

Otherwise, no function call operator of `__swap_fn` participates in overload resolution.

### Example

Run this code

```
#include <array>
#include <concepts>
#include <iostream>
#include <ranges>
#include <string_view>
#include <vector>
 
void print(std::string_view name, 
           std::ranges::common_range auto const& p, 
           std::ranges::common_range auto const& q)
{
    std::cout << name << "1{ ";
    for (auto const& i : p)
        std::cout << i << ' ';
    std::cout << "}, " << name << "2{ ";
    for (auto const& i : q)
        std::cout << i << ' ';
    std::cout << "}\n";
}
 
void print(std::string_view name, int p, int q)
{
    std::cout << name << "1 = " << p << ", " << name << "2 = " << q << '\n';
}
 
struct IntLike
{
    int v;
};
 
void swap(IntLike& lhs, int& rhs)
{
    std::swap(lhs.v, rhs);
}
 
void swap(int& lhs, IntLike& rhs)
{
    std::swap(lhs, rhs.v);
}
 
std::ostream& operator<<(std::ostream& out, IntLike i)
{
    return out << i.v;
}
 
int main()
{
    std::vector a1{10, 11, 12}, a2{13, 14};
    std::ranges::swap(a1, a2);
    print("a", a1, a2);
 
    std::array b1{15, 16, 17}, b2{18, 19, 20};
    std::ranges::swap(b1, b2);
    print("b", b1, b2);
 
    // std::array c1{1, 2, 3}; std::array c2{4, 5};
    // std::ranges::swap(c1, c2); // error: no swap found by ADL
 
    int d1[]{21, 22, 23}, d2[]{24, 25, 26};
    std::ranges::swap(d1, d2);
    print("d", d1, d2);
 
    // int e1[]{1, 2, 3}, e2[]{4, 5};
    // std::ranges::swap(e1, e2); // error: extents mismatch
 
    // char f1[]{1, 2, 3};
    // int  f2[]{4, 5, 6};
    // std::ranges::swap(f1, f2); // error: no swap(*f1, *f2) found by ADL
 
    IntLike g1[]{1, 2, 3};
    int     g2[]{4, 5, 6};
    std::ranges::swap(g1, g2); // heterogeneous swap supported
    print("g", g1, g2);
 
    int h1{27}, h2{28};
    std::ranges::swap(h1, h2);
    print("h", h1, h2);
}

```

Output:

```
a1{ 13 14 }, a2{ 10 11 12 }
b1{ 18 19 20 }, b2{ 15 16 17 }
d1{ 24 25 26 }, d2{ 21 22 23 }
g1{ 4 5 6 }, g2{ 1 2 3 }
h1 = 28, h2 = 27

```

### See also

|  |  |
| --- | --- |
| swappableswappable_with(C++20) | specifies that a type can be swapped or that two types can be swapped with each other   (concept) |
| swap | swaps the values of two objects   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/ranges/swap&oldid=151405>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 May 2023, at 18:50.