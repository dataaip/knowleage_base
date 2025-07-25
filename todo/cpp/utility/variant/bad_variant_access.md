# std::bad_variant_access

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
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | | | | |
| swap(std::variant) | | | | |
| Helper classes | | | | |
| monostate | | | | |
| ****bad_variant_access**** | | | | |
| variant_size | | | | |
| variant_alternative | | | | |
| hash<std::variant> | | | | |
| Helper objects | | | | |
| variant_npos | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<variant>` |  |  |
| class bad_variant_access : public std::exception |  | (since C++17) |
|  |  |  |

`std::bad_variant_access` is the type of the exception thrown in the following situations:

- std::get(std::variant) called with an index or type that does not match the currently active alternative.
- `std::visit` called to visit a variant that is `valueless_by_exception`.

|  |  |
| --- | --- |
| - `std::variant::visit` called to visit a variant that is `valueless_by_exception`. | (since C++26) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new `bad_variant_access` object   (public member function) |
| operator= | replaces the `bad_variant_access` object   (public member function) |
| what | returns the explanatory string   (public member function) |

## std::bad_variant_access::bad_variant_access

|  |  |  |
| --- | --- | --- |
| bad_variant_access() noexcept; | (1) | (since C++17) |
| bad_variant_access( const bad_variant_access& other ) noexcept; | (2) | (since C++17) |
|  |  |  |

Constructs a new `bad_variant_access` object with an implementation-defined null-terminated byte string which is accessible through what().

1) Default constructor.2) Copy constructor. If \*this and other both have dynamic type `std::bad_variant_access` then std::strcmp(what(), other.what()) == 0.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another exception object to copy |

## std::bad_variant_access::operator=

|  |  |  |
| --- | --- | --- |
| bad_variant_access& operator=( const bad_variant_access& other ) noexcept; |  | (since C++17) |
|  |  |  |

Assigns the contents with those of other.If \*this and other both have dynamic type `std::bad_variant_access` then std::strcmp(what(), other.what()) == 0 after assignment.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another exception object to assign with |

### Return value

\*this

## std::bad_variant_access::what

|  |  |  |
| --- | --- | --- |
| virtual const char\* what() const noexcept; |  | (since C++17) |
|  |  |  |

Returns the explanatory string.

### Return value

Pointer to an implementation-defined null-terminated string with explanatory information. The string is suitable for conversion and display as a std::wstring. The pointer is guaranteed to be valid at least until the exception object from which it is obtained is destroyed, or until a non-const member function (e.g. copy assignment operator) on the exception object is called.

|  |  |
| --- | --- |
| The returned string is encoded with the ordinary literal encoding during constant evaluation. | (since C++26) |

### Notes

Implementations are allowed but not required to override `what()`.

## Inherited from std::exception

### Member functions

|  |  |
| --- | --- |
| (destructor)[virtual] | destroys the exception object   (virtual public member function of `std::exception`) |
| what[virtual] | returns an explanatory string   (virtual public member function of `std::exception`) |

### Example

Run this code

```
#include <iostream>
#include <variant>
 
int main()
{
    std::variant<int, float> v;
    v = 12;
    try
    {
        std::get<float>(v);
    }
    catch (const std::bad_variant_access& e)
    {
        std::cout << e.what() << '\n';
    }
}

```

Possible output:

```
bad_variant_access

```

### See also

|  |  |
| --- | --- |
| get(std::variant)(C++17) | reads the value of the variant given the index or the type (if the type is unique), throws on error   (function template) |
| visit(C++17) | calls the provided functor with the arguments held by one or more `variant`s   (function template) |
| visit(C++26) | calls the provided functor with the argument held by the `variant`   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/variant/bad_variant_access&oldid=178521>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 December 2024, at 17:22.