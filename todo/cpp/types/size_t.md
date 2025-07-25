# std::size_t

From cppreference.com
< cpp‎ | types
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

Type support

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic types | | | | |
| Fixed width integer types (C++11) | | | | |
| Fixed width floating-point types (C++23) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ptrdiff_t | | | | | | ****size_t**** | | | | | | max_align_t(C++11) | | | | | | byte(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | nullptr_t(C++11) | | | | | | offsetof | | | | | | NULL | | | | | |  | | | | | |
| Numeric limits | | | | |
| numeric_limits | | | | |
| C numeric limits interface | | | | |
| Runtime type information | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | type_info | | | | | | type_index(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | bad_typeid | | | | | | bad_cast | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<cstddef>` |  |  |
| Defined in header `<cstdio>` |  |  |
| Defined in header `<cstdlib>` |  |  |
| Defined in header `<cstring>` |  |  |
| Defined in header `<ctime>` |  |  |
|  |  |  |
| Defined in header `<cuchar>` |  | (since C++17) |
|  |  |  |
| Defined in header `<cwchar>` |  |  |
| typedef /\* implementation-defined \*/ size_t; |  |  |
|  |  |  |

`std::size_t` is the unsigned integer type of the result of the following operators:

- sizeof

|  |  |
| --- | --- |
| - sizeof... - alignof | (since C++11) |

If a program attempts to form an oversized type (i.e., the number of bytes in its object representation exceeds the maximum value representable in `std::size_t`), the program is ill-formed.

|  |  |
| --- | --- |
| The bit width of `std::size_t` is not less than 16. | (since C++11) |

### Notes

`std::size_t` can store the maximum size of a theoretically possible object of any type (including array). On many platforms (an exception is systems with segmented addressing) `std::size_t` can safely store the value of any non-member pointer, in which case it is synonymous with std::uintptr_t.

`std::size_t` is commonly used for array indexing and loop counting. Programs that use other types, such as unsigned int, for array indexing may fail on, e.g. 64-bit systems when the index exceeds UINT_MAX or if it relies on 32-bit modular arithmetic.

When indexing C++ containers, such as std::string, std::vector, etc, the appropriate type is the nested type `size_type` provided by such containers. It is usually defined as a synonym for `std::size_t`.

It is unspecified whether the declaration of `std::size_t` is available in any other standard library header. An implementation may avoid introducing this name even when the standard requires `std::size_t` to be used.

|  |  |
| --- | --- |
| The integer literal suffix for `std::size_t` is any combination of `z` or `Z` with `u` or `U` (i.e. `zu`, `zU`, `Zu`, `ZU`, `uz`, `uZ`, `Uz`, or `UZ`). | (since C++23) |

### Example

Run this code

```
#include <array>
#include <cstddef>
#include <iostream>
 
int main()
{
    std::array<std::size_t, 10> a;
 
    // Example with C++23 std::size_t literal
    for (auto i = 0uz; i != a.size(); ++i)
        std::cout << (a[i] = i) << ' ';
    std::cout << '\n';
 
    // Example of decrementing loop
    for (std::size_t i = a.size(); i--;)
        std::cout << a[i] << ' ';
    std::cout << '\n';
 
    // Note the naive decrementing loop:
    //  for (std::size_t i = a.size() - 1; i >= 0; --i) ...
    // is an infinite loop, because unsigned numbers are always non-negative
}

```

Output:

```
0 1 2 3 4 5 6 7 8 9
9 8 7 6 5 4 3 2 1 0

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 1122 | C++98 | `std::size_t` was circularly defined[[1]](size_t.html#cite_note-1) | it is implementation-defined |
| CWG 1464 | C++98 | object size might be not representable in `std::size_t` | such type is ill-formed |

1. ↑ The definition of `std::size_t` was exactly the same as the definition of `size_t` in C, which is “the result type of sizeof”. There is no circular definition in C because the result type of `sizeof` in C is an implementation-defined unsigned integer type.

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 6.8.4 Compound types [basic.compound] (p: 79-80)

:   - 7.6.2.5 Sizeof [expr.sizeof] (p: 136)

:   - 7.6.2.6 Alignof [expr.alignof] (p: 136)

:   - 17.2.4 Sizes, alignments, and offsets [support.types.layout] (p: 504-505)

- C++20 standard (ISO/IEC 14882:2020):

:   - 6.8.3 Compound types [basic.compound] (p: 75-76)

:   - 7.6.2.5 Sizeof [expr.sizeof] (p: 129-130)

:   - 7.6.2.6 Alignof [expr.alignof] (p: 130)

:   - 17.2.4 Sizes, alignments, and offsets [support.types.layout] (p: 507-508)

- C++17 standard (ISO/IEC 14882:2017):

:   - 6.9.2 Compound types [basic.compound] (p: 81-82)

:   - 8.3.3 Sizeof [expr.sizeof] (p: 121-122)

:   - 8.3.6 Alignof [expr.alignof] (p: 129)

:   - 21.2.4 Sizes, alignments, and offsets [support.types.layout] (p: 479)

- C++14 standard (ISO/IEC 14882:2014):

:   - 3.9.2 Compound types [basic.compound] (p: 73-74)

:   - 5.3.3 Sizeof [expr.sizeof] (p: 109-110)

:   - 5.3.6 Alignof [expr.alignof] (p: 116)

:   - 18.2 Types [support.types] (p: 443-444)

- C++11 standard (ISO/IEC 14882:2011):

:   - 5.3.3 Sizeof [expr.sizeof] (p: 111)

:   - 5.3.6 Alignof [expr.alignof] (p: 116)

:   - 18.2 Types [support.types] (p: 454-455)

- C++03 standard (ISO/IEC 14882:2003):

:   - 5.3.3 Sizeof [expr.sizeof] (p: 79)

- C++98 standard (ISO/IEC 14882:1998):

:   - 5.3.3 Sizeof [expr.sizeof] (p: 77)

### See also

|  |  |
| --- | --- |
| ptrdiff_t | signed integer type returned when subtracting two pointers   (typedef) |
| offsetof | byte offset from the beginning of a standard-layout type to specified member   (function macro) |
| integer literals | binary,(since C++14) decimal, octal, or hexadecimal numbers of integer type |
| C documentation for size_t | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/types/size_t&oldid=178870>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 December 2024, at 18:15.