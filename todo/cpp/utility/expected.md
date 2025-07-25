# std::expected

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | ****expected****(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

****std::expected****

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
| expected::swap | | | | |
| Non-member functions | | | | |
| operator==(std::expected) | | | | |
| swap(std::expected) | | | | |
| Helper classes | | | | |
| unexpected | | | | |
| bad_expected_access | | | | |
| unexpect_tunexpect | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<expected>` |  |  |
| template< class T, class E >  class expected; | (1) | (since C++23) |
| template< class T, class E >      requires std::is_void_v<T> class expected<T, E>; | (2) | (since C++23) |
|  |  |  |

The class template `std::expected` provides a way to represent either of two values: an **expected** value of type `T`, or an **unexpected** value of type `E`. `std::expected` is never valueless.

1) The main template. Contains the expected or unexpected value within its own storage. No dynamic memory allocation takes place.2) The void partial specialization. Represents an expected void value or contains the unexpected value within its own storage. No dynamic memory allocation takes place.

A program is ill-formed if it instantiates an `expected` with a reference type, a function type, or a specialization of std::unexpected. In addition, `T` must not be std::in_place_t or std::unexpect_t.

### Template parameters

|  |  |  |
| --- | --- | --- |
| T | - | the type of the expected value. The type must either be (possibly cv-qualified) void, or meet the Destructible requirements (in particular, array and reference types are not allowed). |
| E | - | the type of the unexpected value. The type must meet the Destructible requirements, and must be a valid template argument for std::unexpected (in particular, arrays, non-object types, and cv-qualified types are not allowed). |

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `value_type` | `T` |
| `error_type` | `E` |
| `unexpected_type` | `std::unexpected<E>` |

### Member alias templates

|  |  |
| --- | --- |
| Type | Definition |
| rebind<U> | std::expected<U, error_type> |

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| bool `has_val` | whether the `expected` object currently represents the expected value (exposition-only member object\*) |
| `T` `val` (main template only) | the expected value (exposition-only variant member object\*) |
| `E` `unex` | the unexpected value (exposition-only variant member object\*) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the `expected` object   (public member function) |
| (destructor) | destroys the `expected` object, along with its contained value   (public member function) |
| operator= | assigns contents   (public member function) |
| Observers | |
| operator->operator\* | accesses the expected value   (public member function) |
| operator boolhas_value | checks whether the object contains an expected value   (public member function) |
| value | returns the expected value   (public member function) |
| error | returns the unexpected value   (public member function) |
| value_or | returns the expected value if present, another value otherwise   (public member function) |
| error_or | returns the unexpected value if present, another value otherwise   (public member function) |
| Monadic operations | |
| and_then | returns the result of the given function on the expected value if it exists; otherwise, returns the `expected` itself   (public member function) |
| transform | returns an `expected` containing the transformed expected value if it exists; otherwise, returns the `expected` itself   (public member function) |
| or_else | returns the `expected` itself if it contains an expected value; otherwise, returns the result of the given function on the unexpected value   (public member function) |
| transform_error | returns the `expected` itself if it contains an expected value; otherwise, returns an `expected` containing the transformed unexpected value   (public member function) |
| Modifiers | |
| emplace | constructs the expected value in-place   (public member function) |
| swap | exchanges the contents   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==(C++23) | compares `expected` objects   (function template) |
| swap(std::expected)(C++23) | specializes the std::swap algorithm   (function) |

### Helper classes

|  |  |
| --- | --- |
| unexpected(C++23) | represented as an unexpected value   (class template) |
| bad_expected_access(C++23) | exception indicating checked access to an `expected` that contains an unexpected value   (class template) |
| unexpectunexpect_t(C++23) | in-place construction tag for unexpected value in `expected` (tag) |

### Notes

Types with the same functionality are called `Result` in Rust and `Either` in Haskell.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_expected` | `202202L` | (C++23) | class template `std::expected` and associated helper classes |
| `202211L` | (C++23) | Monadic functions for `std::expected` |

### Example

Run this code

```
#include <cmath>
#include <expected>
#include <iomanip>
#include <iostream>
#include <string_view>
 
enum class parse_error
{
    invalid_input,
    overflow
};
 
auto parse_number(std::string_view& str) -> std::expected<double, parse_error>
{
    const char* begin = str.data();
    char* end;
    double retval = std::strtod(begin, &end);
 
    if (begin == end)
        return std::unexpected(parse_error::invalid_input);
    else if (std::isinf(retval))
        return std::unexpected(parse_error::overflow);
 
    str.remove_prefix(end - begin);
    return retval;
}
 
int main()
{
    auto process = [](std::string_view str)
    {
        std::cout << "str: " << std::quoted(str) << ", ";
        if (const auto num = parse_number(str); num.has_value())
            std::cout << "value: " << *num << '\n';
            // If num did not have a value, dereferencing num
            // would cause an undefined behavior, and
            // num.value() would throw std::bad_expected_access.
            // num.value_or(123) uses specified default value 123.
        else if (num.error() == parse_error::invalid_input)
            std::cout << "error: invalid input\n";
        else if (num.error() == parse_error::overflow)
            std::cout << "error: overflow\n";
        else
            std::cout << "unexpected!\n"; // or invoke std::unreachable();
    };
 
    for (auto src : {"42", "42abc", "meow", "inf"})
        process(src);
}

```

Output:

```
str: "42", value: 42
str: "42abc", value: 42
str: "meow", error: invalid input
str: "inf", error: overflow

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 22.8 Expected objects [expected]

### See also

|  |  |
| --- | --- |
| variant(C++17) | a type-safe discriminated union   (class template) |
| optional(C++17) | a wrapper that may or may not hold an object   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/expected&oldid=178039>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 November 2024, at 18:35.