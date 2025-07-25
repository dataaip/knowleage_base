# std::optional

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | ****optional****(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

****std::optional****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| optional::optional | | | | |
| optional::~optional | | | | |
| optional::operator= | | | | |
| Observers | | | | |
| optional::operator->optional::operator\* | | | | |
| optional::operator booloptional::has_value | | | | |
| optional::value | | | | |
| optional::value_or | | | | |
| Iterators | | | | |
| optional::begin(C++26) | | | | |
| optional::end(C++26) | | | | |
| Monadic operations | | | | |
| optional::and_then(C++23) | | | | |
| optional::transform(C++23) | | | | |
| optional::or_else(C++23) | | | | |
| Modifiers | | | | |
| optional::emplace | | | | |
| optional::swap | | | | |
| optional::reset | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | | | | |
| make_optional | | | | |
| swap(std::optional) | | | | |
| Deduction guides | | | | |
| Helper classes | | | | |
| hash<std::optional> | | | | |
| nullopt_t | | | | |
| in_place_t | | | | |
| bad_optional_access | | | | |
| Helper objects | | | | |
| nullopt | | | | |
| in_place | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<optional>` |  |  |
| template< class T >  class optional; |  | (since C++17) |
|  |  |  |

The class template `std::optional` manages an **optional** contained value, i.e. a value that may or may not be present.

A common use case for `optional` is the return value of a function that may fail. As opposed to other approaches, such as std::pair<T, bool>, `optional` handles expensive-to-construct objects well and is more readable, as the intent is expressed explicitly.

Any instance of `optional<T>` at any given point in time either **contains a value** or **does not contain a value**.

If an `optional<T>` **contains a value**, the value is guaranteed to be nested within the `optional` object, which means that no dynamic memory allocation ever takes place. Thus, an `optional` object models an object, not a pointer, even though operator\*() and operator->() are defined.

When an object of type `optional<T>` is contextually converted to bool, the conversion returns true if the object **contains a value** and false if it **does not contain a value**.

The `optional` object **contains a value** in the following conditions:

- The object is initialized with/assigned from a value of type `T` or another `optional` that **contains a value**.

The object **does not contain a value** in the following conditions:

- The object is default-initialized.
- The object is initialized with/assigned from a value of type std::nullopt_t or an `optional` object that **does not contain a value**.
- The member function reset() is called.

|  |  |
| --- | --- |
| The `optional` object is a `view` that contains either one element if it **contains a value**, or otherwise zero elements if it **does not contain a value**. The lifetime of the contained element is bound to the object. | (since C++26) |

There are no optional references, functions, arrays, or **cv** void; a program is ill-formed if it instantiates an `optional` with such a type. In addition, a program is ill-formed if it instantiates an `optional` with the (possibly cv-qualified) tag types std::nullopt_t or std::in_place_t.

### Template parameters

|  |  |  |
| --- | --- | --- |
| T | - | the type of the value to manage initialization state for. The type must meet the requirements of Destructible (in particular, array and reference types are not allowed). |

### Member types

|  |  |
| --- | --- |
| Member name | Definition |
| `value_type` | `T` |
| `iterator` (since C++26) | implementation-defined LegacyRandomAccessIterator, ConstexprIterator, and `contiguous_iterator` whose `value_type` and `reference` are std::remove_cv_t<T> and T&, respectively. |
| `const_iterator` (since C++26) | implementation-defined LegacyRandomAccessIterator, ConstexprIterator, and `contiguous_iterator` whose `value_type` and `reference` are std::remove_cv_t<T> and const T&, respectively. |

All requirements on the iterator types of a Container apply to the `iterator` type of `optional` as well.

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the `optional` object   (public member function) |
| (destructor) | destroys the contained value, if there is one   (public member function) |
| operator= | assigns contents   (public member function) |
| Iterators | |
| begin(C++26) | returns an iterator to the beginning   (public member function) |
| end(C++26) | returns an iterator to the end   (public member function) |
| Observers | |
| operator->operator\* | accesses the contained value   (public member function) |
| operator boolhas_value | checks whether the object contains a value   (public member function) |
| value | returns the contained value   (public member function) |
| value_or | returns the contained value if available, another value otherwise   (public member function) |
| Monadic operations | |
| and_then(C++23) | returns the result of the given function on the contained value if it exists, or an empty `optional` otherwise   (public member function) |
| transform(C++23) | returns an `optional` containing the transformed contained value if it exists, or an empty `optional` otherwise   (public member function) |
| or_else(C++23) | returns the `optional` itself if it contains a value, or the result of the given function otherwise   (public member function) |
| Modifiers | |
| swap | exchanges the contents   (public member function) |
| reset | destroys any contained value   (public member function) |
| emplace | constructs the contained value in-place   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++17)(C++17)(C++17)(C++17)(C++17)(C++17)(C++20) | compares `optional` objects   (function template) |
| make_optional(C++17) | creates an `optional` object   (function template) |
| std::swap(std::optional)(C++17) | specializes the std::swap algorithm   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::hash<std::optional>(C++17) | hash support for ****std::optional****   (class template specialization) |
| nullopt_t(C++17) | indicator of an `std::optional` that does not contain a value   (class) |
| bad_optional_access(C++17) | exception indicating checked access to an optional that doesn't contain a value   (class) |

### Helpers

|  |  |
| --- | --- |
| nullopt(C++17) | an object of type `nullopt_t`   (constant) |
| in_placein_place_typein_place_indexin_place_tin_place_type_tin_place_index_t(C++17) | in-place construction tag (tag) |

### Helper specializations

|  |  |  |
| --- | --- | --- |
| template< class T >  constexpr bool ranges::enable_view<std::optional<T>> = true; |  | (since C++26) |
|  |  |  |

This specialization of ranges::enable_view makes `optional` satisfy `view`.

|  |  |  |
| --- | --- | --- |
| template< class T >  constexpr auto format_kind<std::optional<T>> = range_format::disabled; |  | (since C++26) |
|  |  |  |

This specialization of format_kind disables the range formatting support of `optional`.

### Deduction guides

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_optional` | `201606L` | (C++17) | `std::optional` |
| `202106L` | (C++23) (DR20) | Fully constexpr |
| `202110L` | (C++23) | Monadic operations |
| `__cpp_lib_optional_range_support` | `202406L` | (C++26) | Range support for `std::optional` |

### Example

Run this code

```
#include <iostream>
#include <optional>
#include <string>
 
// optional can be used as the return type of a factory that may fail
std::optional<std::string> create(bool b)
{
    if (b)
        return "Godzilla";
    return {};
}
 
// std::nullopt can be used to create any (empty) std::optional
auto create2(bool b)
{
    return b ? std::optional<std::string>{"Godzilla"} : std::nullopt;
}
 
int main()
{
    std::cout << "create(false) returned "
              << create(false).value_or("empty") << '\n';
 
    // optional-returning factory functions are usable as conditions of while and if
    if (auto str = create2(true))
        std::cout << "create2(true) returned " << *str << '\n';
}

```

Output:

```
create(false) returned empty
create2(true) returned Godzilla

```

### See also

|  |  |
| --- | --- |
| variant(C++17) | a type-safe discriminated union   (class template) |
| any(C++17) | objects that hold instances of any CopyConstructible type   (class) |
| expected(C++23) | a wrapper that contains either an expected or error value   (class template) |
| ranges::single_viewviews::single(C++20) | a `view` that contains a single element of a specified value (class template) (customization point object) |
| ranges::empty_viewviews::empty(C++20) | an empty `view` with no elements (class template) (variable template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/optional&oldid=179516>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 January 2025, at 14:20.