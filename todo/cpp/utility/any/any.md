# std::any::any

From cppreference.com
< cpp‎ | utility‎ | any
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

std::any

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****any::any**** | | | | |
| any::~any | | | | |
| any::operator= | | | | |
| Modifiers | | | | |
| any::emplace | | | | |
| any::reset | | | | |
| any::swap | | | | |
| Observers | | | | |
| any::has_value | | | | |
| any::type | | | | |
| Non-member functions | | | | |
| swap(std::any) | | | | |
| any_cast | | | | |
| make_any | | | | |
| Helper classes | | | | |
| bad_any_cast | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr any() noexcept; | (1) | (since C++17) |
| any( const any& other ); | (2) | (since C++17) |
| any( any&& other ) noexcept; | (3) | (since C++17) |
| template< class ValueType >  any( ValueType&& value ); | (4) | (since C++17) |
| template< class ValueType, class... Args >  explicit any( std::in_place_type_t<ValueType>, Args&&... args ); | (5) | (since C++17) |
| template< class ValueType, class U, class... Args >  explicit any( std::in_place_type_t<ValueType>, std::initializer_list<U> il,               Args&&... args ); | (6) | (since C++17) |
|  |  |  |

Constructs a new `any` object.

1) Constructs an empty object.2,3) Copies (2) or moves (3) content of other into a new instance, so that any content is equivalent in both type and value to those of other prior to the constructor call, or empty if other is empty. Formally,2) If other is empty, the constructed object is empty. Otherwise, equivalent to any(std::in_place_type<T>, std::any_cast<const T&>(other)), where `T` is the type of the object contained in other.3) If other is empty, the constructed object is empty. Otherwise, the constructed object contains either the object contained in other, or an object of the same type constructed from the object contained in other, considering that object as an rvalue.4) Constructs an object with initial content an object of type std::decay_t<ValueType>, direct-initialized from std::forward<ValueType>(value).

- This overload participates in overload resolution only if std::decay_t<ValueType> is not the same type as `any` nor a specialization of std::in_place_type_t, and std::is_copy_constructible_v<std::decay_t<ValueType>> is true.
5) Constructs an object with initial content an object of type std::decay_t<ValueType>, direct-non-list-initialized from std::forward<Args>(args)....

- This overload participates in overload resolution only if std::is_constructible_v<std::decay_t<ValueType>, Args...> and std::is_copy_constructible_v<std::decay_t<ValueType>> are both true.
6) Constructs an object with initial content an object of type std::decay_t<ValueType>, direct-non-list-initialized from il, std::forward<Args>(args)....

- This overload participates in overload resolution only if std::is_constructible_v<std::decay_t<ValueType>, std::initializer_list<U>&, Args...> and std::is_copy_constructible_v<std::decay_t<ValueType>> are both true.

### Template parameters

|  |  |  |
| --- | --- | --- |
| ValueType | - | contained value type |
| Type requirements | | |
| -`std::decay_t<ValueType>` must meet the requirements of CopyConstructible. | | |

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `any` object to copy or move from |
| value | - | value to initialize the contained value with |
| il, args | - | arguments to be passed to the constructor of the contained object |

### Exceptions

2,4-6) Throws any exception thrown by the constructor of the contained type.

### Notes

Because the default constructor is constexpr, static `std::any`s are initialized as part of static non-local initialization, before any dynamic non-local initialization begins. This makes it safe to use an object of type `std::any` in a constructor of any static object.

### Example

Run this code

```
#include <boost/core/demangle.hpp>
 
#include <any>
#include <initializer_list>
#include <iostream>
#include <memory>
#include <set>
#include <string>
#include <utility>
 
struct A
{
    int age;
    std::string name;
    double salary;
 
#if __cpp_aggregate_paren_init < 201902L
    // Required before C++20 for in-place construction
    A(int age, std::string name, double salary)
        : age(age), name(std::move(name)), salary(salary) {}
#endif
};
 
// Using abi demangle to print nice type name of instance of any holding
void printType(const std::any& a)
{
    std::cout << boost::core::demangle(a.type().name()) << '\n';
}
 
int main()
{
    // Constructor #4: std::any holding int
    std::any a1{7};
 
    // Constructor #5: std::any holding A, constructed in place
    std::any a2(std::in_place_type<A>, 30, "Ada", 1000.25);
 
    // Constructor #6: std::any holding a set of A with custom comparison
    auto lambda = [](auto&& l, auto&& r){ return l.age < r.age; };
    std::any a3(
        std::in_place_type<std::set<A, decltype(lambda)>>,
        {
            A{39, std::string{"Ada"}, 100.25},
            A{20, std::string{"Bob"}, 75.5}
        },
        lambda);
 
    printType(a1);
    printType(a2);
    printType(a3);
}

```

Possible output:

```
int
A
std::set<A, main::{lambda(auto:1&&, auto:2&&)#1}, std::allocator<A> >

```

### See also

|  |  |
| --- | --- |
| operator= | assigns an `any` object   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/any/any&oldid=179367>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 January 2025, at 06:44.