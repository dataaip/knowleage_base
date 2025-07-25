# Utility library

From cppreference.com
< cpp
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
| ****General utilities library**** | | | | |
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

****Utilities library****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

C++ includes a variety of utility libraries that provide functionality ranging from bit-counting to partial function application. These libraries can be broadly divided into two groups:

- language support libraries, and
- general-purpose libraries.

## Language support

Language support libraries provide classes and functions that interact closely with language features and support common language idioms.

### Type support

Basic types (e.g. std::size_t, std::nullptr_t), RTTI (e.g. std::type_info)

### Metaprogramming (since C++11)

Type traits (e.g. std::is_integral, std::rank), compile-time constants (e.g. std::integer_sequence, std::ratio)

### Constant evaluation context (since C++20)

|  |  |
| --- | --- |
| Defined in header `<type_traits>` | |
| is_constant_evaluated(C++20) | detects whether the call occurs within a constant-evaluated context   (function) |
| is_within_lifetime(C++26) | checks whether a pointer is within the object's lifetime at compile time   (function) |

### Implementation properties (since C++20)

The header <version> supplies implementation-dependent information about the C++ standard library (such as the version number and release date). It also defines the library feature-test macros.

### Program utilities

Termination (e.g. std::abort, std::atexit), environment (e.g. std::system), signals (e.g. std::raise)

### Dynamic memory management

Smart pointers (e.g. std::shared_ptr), allocators (e.g. std::allocator or std::pmr::memory_resource), C-style memory management (e.g. std::malloc)

### Error handling

Exceptions (e.g. std::exception, std::terminate), assertions (e.g. assert)

### Source code information capture (since C++20)

|  |  |
| --- | --- |
| Defined in header `<source_location>` | |
| source_location(C++20) | a class representing information about the source code, such as file names, line numbers, and function names   (class) |

### Initializer lists (since C++11)

|  |  |
| --- | --- |
| Defined in header `<initializer_list>` | |
| initializer_list(C++11) | references a temporary array created in list-initialization   (class template) |

### Three-way comparison (since C++20)

|  |  |
| --- | --- |
| Defined in header `<compare>` | |
| three_way_comparablethree_way_comparable_with(C++20) | specifies that operator <=> produces consistent result on given types   (concept) |
| partial_ordering(C++20) | the result type of 3-way comparison that supports all 6 operators, is not substitutable, and allows incomparable values   (class) |
| weak_ordering(C++20) | the result type of 3-way comparison that supports all 6 operators and is not substitutable   (class) |
| strong_ordering(C++20) | the result type of 3-way comparison that supports all 6 operators and is substitutable   (class) |
| is_eqis_neqis_ltis_lteqis_gtis_gteq(C++20) | named comparison functions   (function) |
| compare_three_way(C++20) | constrained function object implementing x <=> y   (class) |
| compare_three_way_result(C++20) | obtains the result type of the three-way comparison operator <=> on given types   (class template) |
| common_comparison_category(C++20) | the strongest comparison category to which all of the given types can be converted   (class template) |
| strong_order(C++20) | performs 3-way comparison and produces a result of type `std::strong_ordering` (customization point object) |
| weak_order(C++20) | performs 3-way comparison and produces a result of type `std::weak_ordering` (customization point object) |
| partial_order(C++20) | performs 3-way comparison and produces a result of type `std::partial_ordering` (customization point object) |
| compare_strong_order_fallback(C++20) | performs 3-way comparison and produces a result of type `std::strong_ordering`, even if operator<=> is unavailable (customization point object) |
| compare_weak_order_fallback(C++20) | performs 3-way comparison and produces a result of type `std::weak_ordering`, even if operator<=> is unavailable (customization point object) |
| compare_partial_order_fallback(C++20) | performs 3-way comparison and produces a result of type `std::partial_ordering`, even if operator<=> is unavailable (customization point object) |

### Coroutine support (since C++20)

Types for coroutine support, e.g. std::coroutine_traits, std::coroutine_handle.

### Variadic functions

Support for functions that take an arbitrary number of parameters (via e.g. va_start, va_arg, va_end).

## General-purpose utilities

### Swap

|  |  |
| --- | --- |
| Defined in header `<utility>` | |
| swap | swaps the values of two objects   (function template) |
| exchange(C++14) | replaces the argument with a new value and returns its previous value   (function template) |
| Defined in header `<concepts>` | |
| ranges::swap(C++20) | swaps the values of two objects (customization point object) |

### Type operations (since C++11)

|  |  |
| --- | --- |
| Defined in header `<utility>` | |
| forward(C++11) | forwards a function argument and use the type template argument to preserve its value category   (function template) |
| forward_like(C++23) | forwards a function argument as if casting it to the value category and constness of the expression of specified type template argument   (function template) |
| move(C++11) | converts the argument to an xvalue   (function template) |
| move_if_noexcept(C++11) | converts the argument to an xvalue if the move constructor does not throw   (function template) |
| as_const(C++17) | obtains a reference to const to its argument   (function template) |
| declval(C++11) | obtains a reference to an object of the template type argument for use in an unevaluated context   (function template) |
| to_underlying(C++23) | converts an enumeration to its underlying type   (function template) |

### Integer comparison functions (since C++20)

|  |  |
| --- | --- |
| Defined in header `<utility>` | |
| cmp_equalcmp_not_equalcmp_lesscmp_greatercmp_less_equalcmp_greater_equal(C++20) | compares two integer values, ensuring that signed negative numbers are less than unsigned numbers   (function template) |
| in_range(C++20) | checks if an integer value is in the range of a given integer type   (function template) |

### Relational operators (until C++20)

|  |  |
| --- | --- |
| Defined in header `<utility>` | |
| Defined in namespace `std::rel_ops` | |
| operator!=operator>operator<=operator>=(deprecated in C++20) | automatically generates comparison operators based on user-defined operator== and operator<   (function template) |

### Construction tags (since C++11)

|  |  |
| --- | --- |
| Defined in header `<utility>` | |
| piecewise_constructpiecewise_construct_t(C++11) | piecewise construction tag (tag) |
| in_placein_place_typein_place_indexin_place_tin_place_type_tin_place_index_t(C++17) | in-place construction tag (tag) |
| nontype  nontype_t(C++26) | value construction tag  (tag) |

### Pairs and tuples

|  |  |
| --- | --- |
| Defined in header `<utility>` | |
| pair | implements binary tuple, i.e. a pair of values   (class template) |
| Defined in header `<tuple>` | |
| tuple(C++11) | implements fixed size container, which holds elements of possibly different types   (class template) |
| apply(C++17) | calls a function with a tuple of arguments   (function template) |
| make_from_tuple(C++17) | construct an object with a tuple of arguments   (function template) |
| Tuple protocol (since C++11) | |
| Defined in header `<tuple>` | |
| Defined in header `<utility>` | |
| Defined in header `<array>` | |
| Defined in header `<ranges>` | |
| Defined in header `<complex>` | |
| tuple_size(C++11) | obtains the number of elements of a tuple-like type   (class template) |
| tuple_element(C++11) | obtains the element types of a tuple-like type   (class template) |

### Sum types and type erased wrappers (since C++17)

|  |  |
| --- | --- |
| Defined in header `<optional>` | |
| optional(C++17) | a wrapper that may or may not hold an object   (class template) |
|  | |
| Defined in header `<expected>` | |
| expected(C++23) | a wrapper that contains either an expected or error value   (class template) |
|  | |
| Defined in header `<variant>` | |
| variant(C++17) | a type-safe discriminated union   (class template) |
|  | |
| Defined in header `<any>` | |
| any(C++17) | objects that hold instances of any CopyConstructible type   (class) |

### Bitset

|  |  |
| --- | --- |
| Defined in header `<bitset>` | |
| bitset | implements constant length bit array   (class template) |

### Bit manipulation (since C++20)

The header <bit> provides several function templates to access, manipulate, and process individual bits and bit sequences. The byte ordering (endianness) of scalar types can be inspected via std::endian facility.

### Function objects (since C++11)

Partial function application (e.g. std::bind) and related utilities: utilities for binding such as std::ref and std::placeholders, polymorphic function wrappers: std::function, predefined functors (e.g. std::plus, std::equal_to), pointer-to-member to function converters std::mem_fn.

### Hash support (since C++11)

|  |  |
| --- | --- |
| Defined in header `<functional>` | |
| hash(C++11) | hash function object   (class template) |

### See also

|  |  |
| --- | --- |
| C documentation for Utility library | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility&oldid=179910>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 January 2025, at 11:50.