# std::tuple<Types...>::operator=

From cppreference.com
< cpp‎ | utility‎ | tuple
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

std::tuple

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| tuple::tuple | | | | |
| ****tuple::operator=**** | | | | |
| tuple::swap | | | | |
| Non-member functions | | | | |
| make_tuple | | | | |
| tie | | | | |
| forward_as_tuple | | | | |
| tuple_cat | | | | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| swap(std::tuple) | | | | |
| get(std::tuple) | | | | |
| Helper concepts | | | | |
| `tuple-like`(C++23) | | | | |
| Helper classes | | | | |
| tuple_size<std::tuple> | | | | |
| tuple_element<std::tuple> | | | | |
| uses_allocator<std::tuple> | | | | |
| basic_common_reference<std::tuple>(C++23) | | | | |
| common_type<std::tuple>(C++23) | | | | |
| formatter<std::tuple>(C++23) | | | | |
| ignore | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| tuple& operator=( const tuple& other ); | (1) | (since C++11)  (constexpr since C++20) |
| constexpr const tuple& operator=( const tuple& other ) const; | (2) | (since C++23) |
| tuple& operator=( tuple&& other ) noexcept(/\* see below \*/); | (3) | (since C++11)  (constexpr since C++20) |
| constexpr const tuple& operator=( tuple&& other ) const; | (4) | (since C++23) |
| template< class... UTypes >  tuple& operator=( const tuple<UTypes...>& other ); | (5) | (since C++11)  (constexpr since C++20) |
| template< class... UTypes >  constexpr const tuple& operator=( const tuple<UTypes...>& other ) const; | (6) | (since C++23) |
| template< class... UTypes >  tuple& operator=( tuple<UTypes...>&& other ); | (7) | (since C++11)  (constexpr since C++20) |
| template< class... UTypes >  constexpr const tuple& operator=( tuple<UTypes...>&& other ) const; | (8) | (since C++23) |
| template< class E1, class E2 >  tuple& operator=( const std::pair<E1, E2>& p ); | (9) | (since C++11)  (constexpr since C++20) |
| template< class E1, class E2 >  constexpr const tuple& operator=( const std::pair<E1, E2>& p ) const; | (10) | (since C++23) |
| template< class E1, class E2 >  tuple& operator=( std::pair<E1, E2>&& p ); | (11) | (since C++11)  (constexpr since C++20) |
| template< class E1, class E2 >  constexpr const tuple& operator=( std::pair<E1, E2>&& p ) const; | (12) | (since C++23) |
| template< tuple-like UTuple >  constexpr tuple& operator=( UTuple&& u ); | (13) | (since C++23) |
| template< tuple-like UTuple >  constexpr const tuple& operator=( UTuple&& u ) const; | (14) | (since C++23) |
|  |  |  |

Replaces the contents of the tuple with the contents of another tuple-like object.

In the descriptions that follow, let

- i be in the range ``​0​`,`sizeof...(Types)`)` in order,
- `Ti` be the `i`th type in the class template parameter pack `Types`, and
- `Ui` be the `i`th type in a function template parameter pack named `UTypes`,

where indexing is zero-based.

1) Copy assignment operator. Assigns each element of other to the corresponding element of \*this. This overload is defined as deleted unless [std::is_copy_assignable<Ti>::value is true for all `Ti`.2) Copy assignment operator for const-qualified operand. Assigns each element of other to the corresponding element of \*this. This overload participates in overload resolution only if std::is_copy_assignable_v<const Ti> is true for all `Ti`.3) Move assignment operator. For all i, assigns std::forward<Ti>(std::get<i>(other)) to std::get<i>(\*this). This overload participates in overload resolution only if std::is_move_assignable<Ti>::value is true for all `Ti`.4) Move assignment operator for const-qualified operand. For all i, assigns std::forward<Ti>(std::get<i>(other)) to std::get<i>(\*this). This overload participates in overload resolution only if std::is_assignable_v<const Ti&, Ti> is true for all `Ti`.5) For all i, assigns std::get<i>(other) to std::get<i>(\*this). This overload participates in overload resolution only if sizeof...(Types) == sizeof...(UTypes), and std::is_assignable<Ti&, const Ui&>::value is true for all corresponding pairs of types `Ti` and `Ui`.6) For all i, assigns std::get<i>(other) to std::get<i>(\*this). This overload participates in overload resolution only if sizeof...(Types) == sizeof...(UTypes), and std::is_assignable_v<const Ti&, const Ui&> is true for all corresponding pairs of types `Ti` and `Ui`.7) For all i, assigns std::forward<Ui>(std::get<i>(other)) to std::get<i>(\*this). This overload participates in overload resolution only if sizeof...(Types) == sizeof...(UTypes), and std::is_assignable<Ti&, Ui>::value is true for all corresponding pairs of types `Ti`and `Ui`.8) For all i, assigns std::forward<Ui>(std::get<i>(other)) to std::get<i>(\*this). This overload participates in overload resolution only if sizeof...(Types) == sizeof...(UTypes), and std::is_assignable_v<const Ti&, Ui> is true for all corresponding pairs of types `Ti` and `Ui`.9) Assigns p.first to the first element of \*this and p.second to the second element of \*this. This overload participates in overload resolution only if

- sizeof...(Types) == 2,
- std::is_assignable<T0&, const E1&>::value is true, and
- std::is_assignable<T1&, const E2&>::value is true.
10) Assigns p.first to the first element and p.second to the second element. This overload participates in overload resolution only if

- sizeof...(Types) == 2,
- std::is_assignable_v<const T0&, const E1&> is true, and
- std::is_assignable_v<const T1&, const E2&> is true.
11) Assigns std::forward<E1>(p.first) to the first element of \*this and std::forward<E2>(p.second) to the second element of \*this. This overload participates in overload resolution only if

- sizeof...(Types) == 2,
- std::is_assignable_v<T0&, E1> is true, and
- std::is_assignable_v<T1&, E2> is true.
12) Assigns std::forward<E1>(p.first) to the first element and std::forward<E2>(p.second) to the second element. This overload participates in overload resolution only if

- sizeof...(Types) == 2,
- std::is_assignable_v<const T0&, E1> is true, and
- std::is_assignable_v<const T1&, E2> is true.
13) For all i, assigns std::get<i>(std::forward<UTuple>(u)) to std::get<i>(\*this). This overload participates in overload resolution only if

- std::same_as<std::remove_cvref_t<UTuple>, std::tuple> is false,
- std::remove_cvref_t<UTuple> is not a specialization of std::ranges::subrange,
- sizeof...(Types) equals std::tuple_size_v<std::remove_cvref_t<UTuple>>, and
- std::is_assignable_v<Ti&, decltype(std::get<i>(std::forward<UTuple>(u)))> is true for all i.
14) For all i, assigns std::get<i>(std::forward<UTuple>(u)) to std::get<i>(\*this). This overload participates in overload resolution only if

- std::same_as<std::remove_cvref_t<UTuple>, std::tuple> is false,
- std::remove_cvref_t<UTuple> is not a specialization of std::ranges::subrange,
- sizeof...(Types) equals std::tuple_size_v<std::remove_cvref_t<UTuple>>, and
- std::is_assignable_v<const Ti&, decltype(std::get<i>(std::forward<UTuple>(u)))> is true for all i.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | tuple to replace the contents of this tuple |
| p | - | pair to replace the contents of this 2-tuple |
| u | - | `tuple-like` object to replace the contents of this tuple |

### Return value

\*this

### Exceptions

1,2) May throw implementation-defined exceptionsif the assignment of one of the types in `Types` throws an exception.3)noexcept specification:noexcept(  

std::is_nothrow_move_assignable<T0>::value &&  
    std::is_nothrow_move_assignable<T1>::value &&  
    std::is_nothrow_move_assignable<T2>::value &&  
    ...

)4-14) May throw implementation-defined exceptionsif the assignment of one of the types in `Types` throws an exception.

### Example

Run this code

```
#include <iostream>
#include <string>
#include <string_view>
#include <tuple>
#include <utility>
#include <vector>
 
// helper function to print std::vector<int>
std::ostream& operator<<(std::ostream& os, std::vector<int> const& v)
{
    os << '{';
    for (std::size_t t = 0; t != v.size(); ++t)
        os << v[t] << (t + 1 < v.size() ? ", " : "");
    return os << '}';
}
 
// helpers to print a tuple of any size
template<class... Args>
void print_tuple(std::string_view name, const std::tuple<Args...>& t)
{
    std::cout << name << " = {";
    std::apply(&
    {
        std::cout << arg;
        ((std::cout << ", " << args), ...);
    }, t);
    std::cout << '}';
}
 
template<class Tuple1, class Tuple2>
void print_tuples(std::string_view name1, const Tuple1& t1,
                  std::string_view name2, const Tuple2& t2)
{
    print_tuple(name1, t1);
    std::cout << ", ";
    print_tuple(name2, std::tuple(t2));
    std::cout << "\n\n";
}
 
int main()
{
    // Tuple to tuple examples //
    std::tuple<int, std::string, std::vector<int>>
        t1{1, "alpha", {1, 2, 3}},
        t2{2, "beta", {4, 5}};
    print_tuples("1) t1", t1, "t2", t2);
 
    // Normal copy assignment
    // operator=( const tuple& other );
    t1 = t2;
    print_tuples("2) t1 = t2;\n   t1", t1, "t2", t2);
 
    // Normal move assignment
    // operator=( tuple&& other );
    t1 = std::move(t2);
    print_tuples("3) t1 = std::move(t2);\n   t1", t1, "t2", t2);
 
    // Converting copy assignment
    // operator=( const tuple<UTypes...>& other );
    std::tuple<short, const char*, std::vector<int>> t3{3, "gamma", {6, 7, 8}};
    t1 = t3;
    print_tuples("4) t1 = t3;\n   t1", t1, "t3", t3);
 
    // Converting move assignment
    // operator=( tuple<UTypes...>&& other );
    t1 = std::move(t3);
    print_tuples("5) t1 = std::move(t3);\n   t1", t1, "t3", t3);
 
    // Pair to tuple examples //
    std::tuple<std::string, std::vector<int>> t4{"delta", {10, 11, 12}};
    std::pair<const char*, std::vector<int>> p1{"epsilon", {14, 15, 16}};
    print_tuples("6) t4", t4, "p1", p1);
 
    // Converting copy assignment from std::pair
    // operator=( const std::pair<U1, U2>& p );
    t4 = p1;
    print_tuples("7) t4 = p1;\n   t4", t4, "p1", p1);
 
    // Converting move assignment from std::pair
    // operator=( std::pair<U1, U2>&& p );
    t4 = std::move(p1);
    print_tuples("8) t4 = std::move(p1);\n   t4", t4, "p1", p1);
}

```

Possible output:

```
1) t1 = {1, alpha, {1, 2, 3}}, t2 = {2, beta, {4, 5}}
 
2) t1 = t2;
   t1 = {2, beta, {4, 5}}, t2 = {2, beta, {4, 5}}
 
3) t1 = std::move(t2);
   t1 = {2, beta, {4, 5}}, t2 = {2, , {}}
 
4) t1 = t3;
   t1 = {3, gamma, {6, 7, 8}}, t3 = {3, gamma, {6, 7, 8}}
 
5) t1 = std::move(t3);
   t1 = {3, gamma, {6, 7, 8}}, t3 = {3, gamma, {}}
 
6) t4 = {delta, {10, 11, 12}}, p1 = {epsilon, {14, 15, 16}}
 
7) t4 = p1;
   t4 = {epsilon, {14, 15, 16}}, p1 = {epsilon, {14, 15, 16}}
 
8) t4 = std::move(p1);
   t4 = {epsilon, {14, 15, 16}}, p1 = {epsilon, {}}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2729 | C++11 | operator= was unconstrained and might result in unnecessary undefined behavior | constrained |

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a new `tuple`   (public member function) |
| operator= | assigns the contents   (public member function of `std::pair<T1,T2>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/tuple/operator%3D&oldid=171724>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 May 2024, at 19:23.