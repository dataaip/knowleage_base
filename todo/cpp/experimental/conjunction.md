# std::experimental::conjunction

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
| experimental::make_array | | | | |
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
| Defined in header `<experimental/type_traits>` |  |  |
| template< class... B >  struct conjunction; |  | (library fundamentals TS v2) |
|  |  |  |

Forms the logical conjunction of the type traits `B...`, effectively performing a logical AND on the sequence of traits.

The specialization std::experimental::conjunction<B1, ..., BN> has a public and unambiguous base that is

- if sizeof...(B) == 0, std::true_type; otherwise
- the first type `Bi` in `B1, ..., BN` for which bool(Bi::value) == false, or `BN` if there is no such type.

The member names of the base class, other than `conjunction` and `operator=`, are not hidden and are unambiguously available in `conjunction`.

Conjunction is short-circuiting: if there is a template type argument `Bi` with bool(Bi::value) == false, then instantiating conjunction<B1, ..., BN>::value does not require the instantiation of Bj::value for j > i.

### Template parameters

|  |  |  |
| --- | --- | --- |
| B... | - | every template argument `Bi` for which Bi::value is instantiated must be usable as a base class and define member `value` that is convertible to bool |

### Helper variable template

|  |  |  |
| --- | --- | --- |
| template< class... B >  constexpr bool conjunction_v = conjunction<B...>::value; |  | (library fundamentals TS v2) |
|  |  |  |

### Possible implementation

|  |
| --- |
| ```text template<class...> struct conjunction : std::true_type {}; template<class B1> struct conjunction<B1> : B1 {}; template<class B1, class... Bn> struct conjunction<B1, Bn...>      : std::conditional_t<bool(B1::value), conjunction<Bn...>, B1> {}; ``` |

### Notes

A specialization of `conjunction` does not necessarily inherit from either std::true_type or std::false_type: it simply inherits from the first B whose ::value, converted to bool, is false, or from the very last B when all of them convert to true. For example, conjunction<std::integral_constant<int, 2>, std::integral_constant<int, 4>>::value is 4.

### Example

Run this code

```
#include <experimental/type_traits>
#include <iostream>
 
// func is enabled if all Ts... have the same type
template<typename T, typename... Ts>
constexpr std::enable_if_t<std::experimental::conjunction_v<std::is_same<T, Ts>...>>
func(T, Ts...)
{
    std::cout << "All types are the same.\n";
}
 
template<typename T, typename... Ts>
constexpr std::enable_if_t<!std::experimental::conjunction_v<std::is_same<T, Ts>...>>
func(T, Ts...)
{
    std::cout << "Types differ.\n";
}
 
int main()
{
    func(1, 2'7, 3'1);    
    func(1, 2.7, '3');    
}

```

Output:

```
All types are the same.
Types differ.

```

### See also

|  |  |
| --- | --- |
| conjunction(C++17) | variadic logical AND metafunction   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/conjunction&oldid=154750>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 July 2023, at 10:05.