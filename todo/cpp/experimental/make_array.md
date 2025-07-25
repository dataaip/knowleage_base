# std::experimental::make_array

From cppreference.com
< cpp‎ | experimental
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Library fundamentals v2

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| experimental::propagate_const | | | | |
| experimental::not_fn | | | | |
| experimental::observer_ptr | | | | |
| ****experimental::make_array**** | | | | |
| experimental::to_array | | | | |
| experimental::ostream_joiner | | | | |
| experimental::gcd | | | | |
| experimental::lcm | | | | |
| experimental::source_location | | | | |
| experimental::randint | | | | |
| detection idiom | | | | |
| uniform container erasure | | | | |
| logical operator type traits | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/array>` |  |  |
| template< class D = void, class... Types >  constexpr std::array<VT /\* see below \*/, sizeof...(Types)> make_array( Types&&... t ); |  | (library fundamentals TS v2) |
|  |  |  |

Creates a std::array whose size is equal to the number of arguments and whose elements are initialized from the corresponding arguments. Returns std::array<VT, sizeof...(Types)>{std::forward<Types>(t)...}.

If `D` is void, then the deduced type `VT` is std::common_type_t<Types...>. Otherwise, it is `D`.

If `D` is void and any of std::decay_t<Types>... is a specialization of std::reference_wrapper, the program is ill-formed.

### Notes

`make_array` is removed in Library Fundamentals TS v3 because the deduction guide for `std::array` and std::to_array have been already in C++20.

### Possible implementation

|  |
| --- |
| ```text namespace details {     template<class> struct is_ref_wrapper : std::false_type{};     template<class T> struct is_ref_wrapper<std::reference_wrapper<T>> : std::true_type{};       template<class T>     using not_ref_wrapper = std::negation<is_ref_wrapper<std::decay_t<T>>>;       template<class D, class...> struct return_type_helper { using type = D; };     template<class... Types>     struct return_type_helper<void, Types...> : std::common_type<Types...>     {         static_assert(std::conjunction_v<not_ref_wrapper<Types>...>,                       "Types cannot contain reference_wrappers when D is void");     };       template<class D, class... Types>     using return_type = std::array<typename return_type_helper<D, Types...>::type,                                    sizeof...(Types)>; }   template<class D = void, class... Types> constexpr details::return_type<D, Types...> make_array(Types&&... t) {     return {std::forward<Types>(t)...}; } ``` |

### Example

Run this code

```
#include <experimental/array>
#include <iostream>
#include <type_traits>
 
int main()
{
    auto arr = std::experimental::make_array(1, 2, 3, 4, 5);
    bool is_array_of_5_ints = std::is_same<decltype(arr), std::array<int, 5>>::value;
    std::cout << "Returns an array of five ints? ";
    std::cout << std::boolalpha << is_array_of_5_ints << '\n';
}

```

Output:

```
Returns an array of five ints? true

```

### See also

|  |  |
| --- | --- |
| C++ documentation for `std::array` deduction guides | |
| to_array | creates a std::array object from a built-in array   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/make_array&oldid=154986>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 17 July 2023, at 02:14.