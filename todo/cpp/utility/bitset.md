# std::bitset

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | ****bitset**** | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

****std::bitset****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| bitset::reference | | | | |
| Member functions | | | | |
| bitset::bitset | | | | |
| bitset::operator==bitset::operator!=(until C++20) | | | | |
| Element access | | | | |
| [bitset::operator[]](bitset/operator_at.html "cpp/utility/bitset/operator at") | | | | |
| bitset::test | | | | |
| bitset::allbitset::anybitset::none(C++11) | | | | |
| bitset::count | | | | |
| Capacity | | | | |
| bitset::size | | | | |
| Modifiers | | | | |
| bitset::operator&=bitset::operator|=bitset::operator^=bitset::operator~ | | | | |
| bitset::operator<<=bitset::operator>>=bitset::operator<<bitset::operator>> | | | | |
| bitset::set | | | | |
| bitset::reset | | | | |
| bitset::flip | | | | |
| Conversions | | | | |
| bitset::to_string | | | | |
| bitset::to_ulong | | | | |
| bitset::to_ullong(C++11) | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator&operator|operator^ | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator<<operator>> | | | | | |  | | | | | |
| Helper classes | | | | |
| std::hash(C++11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<bitset>` |  |  |
| template< std::size_t N >  class bitset; |  |  |
|  |  |  |

The class template `bitset` represents a fixed-size sequence of `N` bits. Bitsets can be manipulated by standard logic operators and converted to and from strings and integers. For the purpose of the string representation and of naming directions for shift operations, the sequence is thought of as having its lowest indexed elements at the **right**, as in the binary representation of integers.

`bitset` meets the requirements of CopyConstructible and CopyAssignable.

|  |  |
| --- | --- |
| All member functions of `std::bitset` are constexpr: it is possible to create and use `std::bitset` objects in the evaluation of a constant expression. | (since C++23) |

### Template parameters

|  |  |  |
| --- | --- | --- |
| N | - | the number of bits to allocate storage for |

### Member types

|  |  |
| --- | --- |
| reference | proxy class representing a reference to a bit   (class) |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the bitset   (public member function) |
| operator==operator!=(removed in C++20) | compares the contents   (public member function) |
| Element access | |
| [operator[]](bitset/operator_at.html "cpp/utility/bitset/operator at") | accesses specific bit   (public member function) |
| test | accesses specific bit   (public member function) |
| allanynone | checks if all, any or none of the bits are set to true   (public member function) |
| count | returns the number of bits set to true   (public member function) |
| Capacity | |
| size | returns the number of bits that the bitset holds   (public member function) |
| Modifiers | |
| operator&=operator|=operator^=operator~ | performs binary AND, OR, XOR and NOT   (public member function) |
| operator<<=operator>>=operator<<operator>> | performs binary shift left and shift right   (public member function) |
| set | sets bits to true or given value   (public member function) |
| reset | sets bits to false   (public member function) |
| flip | toggles the values of bits   (public member function) |
| Conversions | |
| to_string | returns a string representation of the data   (public member function) |
| to_ulong | returns an unsigned long integer representation of the data   (public member function) |
| to_ullong(C++11) | returns an unsigned long long integer representation of the data   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator&operator|operator^ | performs binary logic operations on bitsets   (function template) |
| operator<<operator>> | performs stream input and output of bitsets   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::hash<std::bitset>(C++11) | hash support for ****std::bitset****   (class template specialization) |

### Notes

If the size of a bit-set is not known at compile time, or it is necessary to change its size at run-time, the dynamic types such as std::vector<bool> or `boost::dynamic_bitset<>` may be used instead.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_constexpr_bitset` | `202207L` | (C++23) | A more constexpr `std::bitset` |
| `__cpp_lib_bitset` | `202306L` | (C++26) | Interfacing `std::bitset` with std::string_view |

### Example

Run this code

```
#include <bitset>
#include <cassert>
#include <cstddef>
#include <iostream>
 
int main()
{
    typedef std::size_t length_t, position_t; // the hints
 
    // constructors:
    constexpr std::bitset<4> b1;
    constexpr std::bitset<4> b2{0xA}; // == 0B1010
    std::bitset<4> b3{"0011"}; // can also be constexpr since C++23
    std::bitset<8> b4{"ABBA", length_t(4), /*0:*/'A', /*1:*/'B'}; // == 0B0000'0110
 
    // bitsets can be printed out to a stream:
    std::cout << "b1:" << b1 << "; b2:" << b2 << "; b3:" << b3 << "; b4:" << b4 << '\n';
 
    // bitset supports bitwise operations:
    b3 |= 0b0100; assert(b3 == 0b0111);
    b3 &= 0b0011; assert(b3 == 0b0011);
    b3 ^= std::bitset<4>{0b1100}; assert(b3 == 0b1111);
 
    // operations on the whole set:
    b3.reset(); assert(b3 == 0);
    b3.set(); assert(b3 == 0b1111);
    assert(b3.all() && b3.any() && !b3.none());
    b3.flip(); assert(b3 == 0);
 
    // operations on individual bits:
    b3.set(position_t(1), true); assert(b3 == 0b0010);
    b3.set(position_t(1), false); assert(b3 == 0);
    b3.flip(position_t(2)); assert(b3 == 0b0100);
    b3.reset(position_t(2)); assert(b3 == 0);
 
    // subscript operator[] is supported:
    b3[2] = true; assert(true == b3[2]);
 
    // other operations:
    assert(b3.count() == 1);
    assert(b3.size() == 4);
    assert(b3.to_ullong() == 0b0100ULL);
    assert(b3.to_string() == "0100");
}

```

Output:

```
b1:0000; b2:1010; b3:0011; b4:00000110

```

### See also

|  |  |
| --- | --- |
| vector<bool> | space-efficient dynamic bitset   (class template specialization) |
| ****Bit manipulation**** (C++20) | utilities to access, manipulate, and process individual bits and bit sequences |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/bitset&oldid=177218>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 October 2024, at 16:08.