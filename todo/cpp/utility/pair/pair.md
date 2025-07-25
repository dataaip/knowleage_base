# std::pair<T1,T2>::pair

From cppreference.com
< cpp‎ | utility‎ | pair
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

std::pair

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****pair::pair**** | | | | |
| pair::operator= | | | | |
| pair::swap(C++11) | | | | |
| Non-member functions | | | | |
| make_pair | | | | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| swap(std::pair)(C++11) | | | | |
| get(std::pair)(C++11) | | | | |
| Helper classes | | | | |
| tuple_size<std::pair>(C++11) | | | | |
| tuple_element<std::pair>(C++11) | | | | |
| basic_common_reference<std::pair>(C++23) | | | | |
| common_type<std::pair>(C++23) | | | | |
| formatter<std::pair>(C++23) | | | | |
| piecewise_construct_t(C++11) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| pair(); | (1) | (constexpr since C++11)  (conditionally explicit since C++11) |
| pair( const T1& x, const T2& y ); | (2) | (conditionally explicit since C++11) (constexpr since C++14) |
|  |  |  |
| --- | --- | --- |
|  | (3) |  |
| template< class U1, class U2 >  pair( U1&& x, U2&& y ); |  | (since C++11)  (until C++23)  (constexpr since C++14) (conditionally explicit) |
| template< class U1 = T1, class U2 = T2 >  constexpr pair( U1&& x, U2&& y ); |  | (since C++23)  (conditionally explicit) |
|  |  |  |
| --- | --- | --- |
| template< class U1, class U2 >  constexpr pair( pair<U1, U2>& p ); | (4) | (since C++23)  (conditionally explicit) |
| template< class U1, class U2 >  pair( const pair<U1, U2>& p ); | (5) | (conditionally explicit since C++11) (constexpr since C++14) |
| template< class U1, class U2 >  pair( pair<U1, U2>&& p ); | (6) | (constexpr since C++14)  (conditionally explicit since C++11) |
| template< class U1, class U2 >  constexpr pair( const pair<U1, U2>&& p ); | (7) | (since C++23)  (conditionally explicit) |
| template< pair-like P >  constexpr pair ( P&& u ); | (8) | (since C++23)  (conditionally explicit) |
| template< class... Args1, class... Args2 >  pair( std::piecewise_construct_t,        std::tuple<Args1...> first_args, std::tuple<Args2...> second_args ); | (9) | (since C++11)  (constexpr since C++20) |
| pair( const pair& p ) = default; | (10) |  |
| pair( pair&& p ) = default; | (11) | (since C++11) |
|  |  |  |

Constructs a new pair.

1) Default constructor. Value-initializes both elements of the pair, `first` and `second`.

|  |  |
| --- | --- |
| This constructor participates in overload resolution if and only if std::is_default_constructible_v<T1> and std::is_default_constructible_v<T2> are both true.  This constructor is explicit if and only if either `T1` or `T2` is not implicitly default-constructible. | (since C++11) |

2) Initializes `first` with x and `second` with y.

|  |  |
| --- | --- |
| This constructor participates in overload resolution if and only if std::is_copy_constructible_v<T1> and std::is_copy_constructible_v<T2> are both true.  This constructor is explicit if and only if std::is_convertible_v<const T1&, T1> is false or std::is_convertible_v<const T2&, T2> is false. | (since C++11) |

3) Initializes `first` with std::forward<U1>(x) and `second` with std::forward<U2>(y). This constructor participates in overload resolution if and only if std::is_constructible_v<T1, U1> and std::is_constructible_v<T2, U2> are both true. This constructor is explicit if and only if std::is_convertible_v<U1, T1> is false or std::is_convertible_v<U2, T2> is false.

|  |  |
| --- | --- |
| This constructor is defined as deleted if the initialization of `first` or `second` would bind a reference to temporary object. | (since C++23) |

4) Initializes `first` with p.first and `second` with p.second. This constructor participates in overload resolution if and only if std::is_constructible_v<T1, U1&> and std::is_constructible_v<T2, U2&> are both true. This constructor is explicit if and only if std::is_convertible_v<U1&, T1> is false or std::is_convertible_v<U2&, T2> is false. This constructor is defined as deleted if the initialization of `first` or `second` would bind a reference to temporary object.5) Initializes `first` with p.first and `second` with p.second.

|  |  |
| --- | --- |
| This constructor participates in overload resolution if and only if std::is_constructible_v<T1, const U1&> and std::is_constructible_v<T2, const U2&> are both true.  This constructor is explicit if and only if std::is_convertible_v<const U1&, T1> is false or std::is_convertible_v<const U2&, T2> is false. | (since C++11) |

|  |  |
| --- | --- |
| This constructor is defined as deleted if the initialization of `first` or `second` would bind a reference to temporary object. | (since C++23) |

6) Initializes `first` with std::forward<U1>(p.first) and `second` with std::forward<U2>(p.second). This constructor participates in overload resolution if and only if std::is_constructible_v<T1, U1> and std::is_constructible_v<T2, U2> are both true. This constructor is explicit if and only if std::is_convertible_v<U1, T1> is false or std::is_convertible_v<U2, T2> is false.

|  |  |
| --- | --- |
| This constructor is defined as deleted if the initialization of `first` or `second` would bind a reference to temporary object. | (since C++23) |

7) Initializes `first` with std::forward<const U1>(p.first) and `second` with std::forward<const U2>(p.second). This constructor participates in overload resolution if and only if std::is_constructible_v<T1, U1> and std::is_constructible_v<T2, U2> are both true. This constructor is explicit if and only if std::is_convertible_v<const U1, T1> is false or std::is_convertible_v<const U2, T2> is false. This constructor is defined as deleted if the initialization of `first` or `second` would bind a reference to temporary object.8) Given u1 as std::get<0>(std::forward(u)) and u2 as std::get<1>(std::forward(u)), denote their types as `U1` and `U2` respectively. Initializes `first` with u1 and `second` with u2. This constructor participates in overload resolution if and only if

- std::remove_cvref(P) is not a specialization of std::ranges::subrange,
- std::is_constructible_v<T1, U1> is true, and
- std::is_constructible_v<T2, U2 is true.
 This constructor is explicit if and only if std::is_convertible_v<U1, T1> is false or std::is_convertible_v<U2, T2> is false. This constructor is defined as deleted if the initialization of `first` or `second` would bind a reference to temporary object.9) Forwards the elements of first_args to the constructor of `first` and forwards the elements of second_args to the constructor of `second`. This is the only non-default constructor that can be used to create a pair of non-copyable non-movable types. The program is ill-formed if `first` or `second` is a reference and bound to a temporary object.10) Copy constructor is implicitly declared(until C++11)defaulted, and is constexpr if copying of both elements satisfies the requirements on constexpr functions(since C++11).11) Move constructor is defaulted, and is constexpr if moving of both elements satisfies the requirements on constexpr functions.

### Parameters

|  |  |  |
| --- | --- | --- |
| x | - | value to initialize the first element of this pair |
| y | - | value to initialize the second element of this pair |
| p | - | pair of values used to initialize both elements of this pair |
| u | - | **pair-like** object of values used to initialize both elements of this pair |
| first_args | - | tuple of constructor arguments to initialize the first element of this pair |
| second_args | - | tuple of constructor arguments to initialize the second element of this pair |

### Exceptions

Does not throw exceptions unless one of the specified operations (e.g. constructor of an element) throws.

### Example

Run this code

```
#include <complex>
#include <iostream>
#include <string>
#include <tuple>
#include <utility>
 
int main()
{
    auto print = [](auto rem, auto const& pair)
    {
        std::cout << rem << "(" << pair.first << ", " << pair.second << ")\n";
    };
 
    std::pair<int, float> p1;
    print("(1) Value-initialized: ", p1);
 
    std::pair<int, double> p2{42, 3.1415};
    print("(2) Initialized with two values: ", p2);
 
    std::pair<char, int> p4{p2};
    print("(4) Implicitly converted: ", p4);
 
    std::pair<std::complex<double>, std::string> p6
        {std::piecewise_construct, std::forward_as_tuple(0.123, 7.7),
            std::forward_as_tuple(10, 'a')};
    print("(8) Piecewise constructed: ", p6);
}

```

Possible output:

```
(1) Value-initialized: (0, 0)
(2) Initialized with two values: (42, 3.1415)
(4) Implicitly converted: (*, 3)
(8) Piecewise constructed: ((0.123,7.7), aaaaaaaaaa)

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 265 | C++98 | the default constructor copy-initialized `first` and `second` with T1() and T2() respectively (thus required `T1` and `T2` to be CopyConstructible) | `first` and `second` are value-initialized |
| LWG 2510 | C++11 | the default constructor was implicit | made conditionally-explicit |
| N4387 | C++11 | some constructors were implicit-only, preventing some uses | constructors made conditionally-explicit |

### See also

|  |  |
| --- | --- |
| make_pair | creates a `pair` object of type, determined by the argument types   (function template) |
| (constructor) | constructs a new `tuple`   (public member function of `std::tuple<Types...>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/pair/pair&oldid=173323>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 July 2024, at 02:20.