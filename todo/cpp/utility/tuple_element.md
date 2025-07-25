# std::tuple_element

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | ****tuple_element****(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<tuple>` |  |  |
| Defined in header `<array>` |  |  |
| Defined in header `<utility>` |  |  |
| Defined in header `<ranges>` |  | (since C++20) |
| Defined in header `<complex>` |  | (since C++26) |
| template< std::size_t I, class T >  struct tuple_element; // not defined | (1) | (since C++11) |
| template< std::size_t I, class T >  struct tuple_element< I, const T > {      using type = typename          std::add_const<typename std::tuple_element<I, T>::type>::type; }; | (2) | (since C++11) |
| template< std::size_t I, class T >  struct tuple_element< I, volatile T > {      using type = typename          std::add_volatile<typename std::tuple_element<I, T>::type>::type; }; | (3) | (since C++11)  (deprecated in C++20) |
| template< std::size_t I, class T >  struct tuple_element< I, const volatile T > {      using type = typename          std::add_cv<typename std::tuple_element<I, T>::type>::type; }; | (4) | (since C++11)  (deprecated in C++20) |
|  |  |  |

Provides compile-time indexed access to the types of the elements of a tuple-like type.

1) The primary template is not defined. An explicit (full) or partial specialization is required to make a type tuple-like.2-4) Specializations for cv-qualified types simply add corresponding cv-qualifiers by default.

|  |  |
| --- | --- |
| `std::tuple_element` interacts with the core language: it can provide structured binding support in the tuple-like case. | (since C++17) |

### Specializations

The standard library provides following specializations for standard library types:

|  |  |
| --- | --- |
| std::tuple_element<std::tuple>(C++11) | obtains the type of the specified element   (class template specialization) |
| std::tuple_element<std::pair>(C++11) | obtains the type of the elements of `pair`   (class template specialization) |
| std::tuple_element<std::array>(C++11) | obtains the type of the elements of `array`   (class template specialization) |
| std::tuple_element<std::ranges::subrange>(C++20) | obtains the type of the iterator or the sentinel of a std::ranges::subrange   (class template specialization) |
| std::tuple_element<std::complex>(C++26) | obtains the underlying real and imaginary number type of a std::complex   (class template specialization) |

Users may specialize `std::tuple_element` for program-defined types to make them tuple-like.

In normal cases where the `get` functions returns reference members or reference to subobjects, only specializations for cv-unqualified types are needed to be customized.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| type | for a standard specialization, the type of `I`th element of the tuple-like type `T`, where `I` is in ``​0​`,`[std::tuple_size<T>::value`)` |

### Helper types

|  |  |  |
| --- | --- | --- |
| Defined in header `<tuple>` |  |  |
| template< std::size_t I, class T >  using tuple_element_t = typename tuple_element<I, T>::type; |  | (since C++14) |
|  |  |  |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_tuple_element_t` | `201402L` | (C++14) | `std::tuple_element_t` |

### Example

Run this code

```
#include <array>
#include <cstddef>
#include <iostream>
#include <ranges>
#include <tuple>
#include <type_traits>
#include <utility>
 
template<typename T1, typename T2, typename T3>
struct Triple
{
    T1 t1;
    T2 t2;
    T3 t3;
};
 
// A specialization of std::tuple_element for program-defined type Triple:
template<std::size_t I, typename T1, typename T2, typename T3>
    struct std::tuple_element<I, Triple<T1, T2, T3>>
    { static_assert(false, "Invalid index"); }; 
template<typename T1, typename T2, typename T3>
    struct std::tuple_element<0, Triple<T1, T2, T3>> { using type = T1; };
template<typename T1, typename T2, typename T3>
    struct std::tuple_element<1, Triple<T1, T2, T3>> { using type = T2; };
template<typename T1, typename T2, typename T3>
    struct std::tuple_element<2, Triple<T1, T2, T3>> { using type = T3; };
 
 
template<typename... Args> struct TripleTypes
{
    static_assert(3 == sizeof...(Args), "Expected exactly 3 type names");
    template<std::size_t N>
    using type = typename std::tuple_element_t<N, Triple<Args...>>;
};
 
int main()
{
    TripleTypes<char, int, float>::type<1> i{42};
    std::cout << i << '\n';
 
    using Tri = Triple<int, char, short>; //< Program-defined type
    static_assert(std::is_same_v<std::tuple_element_t<0, Tri>, int> &&
                  std::is_same_v<std::tuple_element_t<1, Tri>, char> &&
                  std::is_same_v<std::tuple_element_t<2, Tri>, short>);
 
    using Tuple = std::tuple<int, char, short>;
    static_assert(std::is_same_v<std::tuple_element_t<0, Tuple>, int> &&
                  std::is_same_v<std::tuple_element_t<1, Tuple>, char> &&
                  std::is_same_v<std::tuple_element_t<2, Tuple>, short>);
 
    using Array3 = std::array<int, 3>;
    static_assert(std::is_same_v<std::tuple_element_t<0, Array3>, int> &&
                  std::is_same_v<std::tuple_element_t<1, Array3>, int> &&
                  std::is_same_v<std::tuple_element_t<2, Array3>, int>);
 
    using Pair = std::pair<Tuple, Tri>;
    static_assert(std::is_same_v<std::tuple_element_t<0, Pair>, Tuple> &&
                  std::is_same_v<std::tuple_element_t<1, Pair>, Tri>);
 
    using Sub = std::ranges::subrange<int*, int*>;
    static_assert(std::is_same_v<std::tuple_element_t<0, Sub>, int*> &&
                  std::is_same_v<std::tuple_element_t<1, Sub>, int*>);
}

```

Output:

```
42

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2212 | C++11 | specializations for cv types were not required in some headers, which led to ambiguity | required |

### See also

|  |  |
| --- | --- |
| Structured binding (C++17) | binds the specified names to sub-objects or tuple elements of the initializer |
| tuple_size(C++11) | obtains the number of elements of a tuple-like type   (class template) |
| tuple_cat(C++11) | creates a `tuple` by concatenating any number of tuples   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/tuple_element&oldid=172990>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 June 2024, at 06:22.