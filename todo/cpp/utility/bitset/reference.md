# std::bitset<N>::reference

From cppreference.com
< cpp‎ | utility‎ | bitset
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

std::bitset

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| ****bitset::reference**** | | | | |
| Member functions | | | | |
| bitset::bitset | | | | |
| bitset::operator==bitset::operator!=(until C++20) | | | | |
| Element access | | | | |
| [bitset::operator[]](operator_at.html "cpp/utility/bitset/operator at") | | | | |
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
| class reference; |  |  |
|  |  |  |

The std::bitset class includes `std::bitset::reference` as a publicly-accessible nested class. This class is used as a proxy object to allow users to interact with individual bits of a bitset, since standard C++ types (like references and pointers) are not built with enough precision to specify individual bits.

The primary use of `std::bitset::reference` is to provide an lvalue that can be returned from [`operator[]`](operator_at.html "cpp/utility/bitset/operator at").

Any reads or writes to a bitset that happen via a `std::bitset::reference` potentially read or write to the entire underlying bitset.

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs the reference. There is no default constructor. The copy constructor is implicitly declared(until C++11)defaulted(since C++11). There may be internal constructor that is accessible only to std::bitset itself.   (public member function) |
| ****(destructor)**** | destroys the reference   (public member function) |
| operator= | assigns a bool to the referenced bit   (public member function) |
| ****operator bool**** | returns the referenced bit   (public member function) |
| operator~ | returns inverted referenced bit   (public member function) |
| flip | flips the referenced bit   (public member function) |

## std::bitset<N>::reference::~reference

|  |  |  |
| --- | --- | --- |
| ~reference(); |  | (constexpr since C++23) |
|  |  |  |

Destroys the reference.

## std::bitset<N>::reference::operator=

|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| reference& operator=( bool x ); |  | (until C++11) |
| reference& operator=( bool x ) noexcept; |  | (since C++11)  (constexpr since C++23) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| reference& operator=( const reference& x ); |  | (until C++11) |
| reference& operator=( const reference& x ) noexcept; |  | (since C++11)  (constexpr since C++23) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Assigns a value to the referenced bit.

### Parameters

|  |  |  |
| --- | --- | --- |
| x | - | value to assign |

### Return value

\*this

## std::bitset<N>::reference::operator bool

|  |  |  |
| --- | --- | --- |
| operator bool() const; |  | (until C++11) |
| operator bool() const noexcept; |  | (since C++11)  (constexpr since C++23) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Returns the value of the referenced bit.

### Parameters

(none)

### Return value

The referenced bit.

## std::bitset<N>::reference::operator~

|  |  |  |
| --- | --- | --- |
| bool operator~() const; |  | (until C++11) |
| bool operator~() const noexcept; |  | (since C++11)  (constexpr since C++23) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Returns the inverse of the referenced bit.

### Parameters

(none)

### Return value

The inverse of the referenced bit.

## std::bitset<N>::reference::flip

|  |  |  |
| --- | --- | --- |
| reference& flip(); |  | (until C++11) |
| reference& flip() noexcept; |  | (since C++11)  (constexpr since C++23) |
|  |  |  |
| --- | --- | --- |
|  |  |  |

Inverts the referenced bit.

### Parameters

(none)

### Return value

\*this

### Example

Run this code

```
#include <bitset>
#include <iostream>
 
int main()
{
    std::bitset<4> bs{0b1110};
    std::bitset<4>::reference ref = bs[2];
 
    auto info = &
    {
        std::cout << id << ") bs: " << bs << "; ref bit: " << ref << '\n';
    };
 
    info(1);
    ref = false;
    info(2);
    ref = true;
    info(3);
    ref.flip();
    info(4);
    ref = bs[1]; // operator=( const reference& x )
    info(5);
 
    std::cout << "6) ~ref bit: " << ~ref << '\n';
}

```

Output:

```
1) bs: 1110; ref bit: 1
2) bs: 1010; ref bit: 0
3) bs: 1110; ref bit: 1
4) bs: 1010; ref bit: 0
5) bs: 1110; ref bit: 1
6) ~ref bit: 0

```

### See also

|  |  |
| --- | --- |
| [operator[]](operator_at.html "cpp/utility/bitset/operator at") | accesses specific bit   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/bitset/reference&oldid=178105>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 December 2024, at 17:22.