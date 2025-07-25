# operator==,!=,<,<=,>,>=,<=>(std::array)

From cppreference.com
< cpp‎ | container‎ | array
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

Containers library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Sequence | | | | |
| array(C++11) | | | | |
| vector | | | | |
| vector<bool> | | | | |
| inplace_vector(C++26) | | | | |
| deque | | | | |
| forward_list(C++11) | | | | |
| list | | | | |
| Associative | | | | |
| set | | | | |
| multiset | | | | |
| map | | | | |
| multimap | | | | |
| Unordered associative | | | | |
| unordered_set(C++11) | | | | |
| unordered_multiset(C++11) | | | | |
| unordered_map(C++11) | | | | |
| unordered_multimap(C++11) | | | | |
| Adaptors | | | | |
| stack | | | | |
| queue | | | | |
| priority_queue | | | | |
| flat_set(C++23) | | | | |
| flat_multiset(C++23) | | | | |
| flat_map(C++23) | | | | |
| flat_multimap(C++23) | | | | |
| Views | | | | |
| span(C++20) | | | | |
| mdspan(C++23) | | | | |
| Tables | | | | |
| Iterator invalidation | | | | |
| Member function table | | | | |
| Non-member function table | | | | |

std::array

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | array::at | | | | | | [array::operator[]](operator_at.html "cpp/container/array/operator at") | | | | | | array::front | | | | | | array::back | | | | | | array::data | | | | | | Operations | | | | | | array::fill | | | | | | array::swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | array::beginarray::cbegin | | | | | | array::endarray::cend | | | | | | array::rbeginarray::crbegin | | | | | | array::rendarray::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | array::empty | | | | | | array::size | | | | | | array::max_size | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****operator==operator<=>****(C++20) | | | | | | get(std::array) | | | | | | swap(std::array) | | | | | | to_array(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****operator|=operator<operator>operator<=operator>=****(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Helper classes | | | | |
| tuple_size<std::array> | | | | |
| tuple_element<std::array> | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<array>` |  |  |
| template< class T, std::size_t N >  bool operator==( const std::array<T, N>& lhs, const std::array<T, N>& rhs ); | (1) | (since C++11)  (constexpr since C++20) |
| template< class T, std::size_t N >  bool operator!=( const std::array<T, N>& lhs, const std::array<T, N>& rhs ); | (2) | (since C++11)  (until C++20) |
| template< class T, std::size_t N >  bool operator<( const std::array<T, N>& lhs, const std::array<T, N>& rhs ); | (3) | (since C++11)  (until C++20) |
| template< class T, std::size_t N >  bool operator<=( const std::array<T, N>& lhs, const std::array<T, N>& rhs ); | (4) | (since C++11)  (until C++20) |
| template< class T, std::size_t N >  bool operator>( const std::array<T, N>& lhs, const std::array<T, N>& rhs ); | (5) | (since C++11)  (until C++20) |
| template< class T, std::size_t N >  bool operator>=( const std::array<T, N>& lhs, const std::array<T, N>& rhs ); | (6) | (since C++11)  (until C++20) |
| template< class T, std::size_t N >  constexpr synth-three-way-result<T>      operator<=>( const std::array<T, N>& lhs, const std::array<T, N>& rhs ); | (7) | (since C++20) |
|  |  |  |

Compares the contents of two `array`s.

1,2) Checks if the contents of lhs and rhs are equal, that is, they have the same number of elements and each element in lhs compares equal with the element in rhs at the same position.3-6) Compares the contents of lhs and rhs lexicographically. The comparison is performed by a function equivalent to std::lexicographical_compare.7) Compares the contents of lhs and rhs lexicographically. The comparison is performed as if by calling std::lexicographical_compare_three_way(lhs.begin(), lhs.end(),  
rhs.begin(), rhs.end(),**synth-three-way**). The return type is the return type of **synth-three-way** (i.e., **synth-three-way-result** ﻿<T>). If none of the following conditions is satisfied, the behavior is undefined:

- `T` models `three_way_comparable`.
- `<` is defined for values of type (possibly const-qualified) `T`, and `<` is a total ordering relationship.

|  |  |
| --- | --- |
| The `<`, `<=`, `>`, `>=`, and `!=` operators are synthesized from operator<=> and operator== respectively. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | `array`s whose contents to compare |
| -`T` must meet the requirements of EqualityComparable in order to use overloads (1,2). | | |
| -`T` must meet the requirements of LessThanComparable in order to use overloads (3-6). The ordering relation must establish total order. | | |

### Return value

1) true if the contents of the `array`s are equal, false otherwise.2) true if the contents of the `array`s are not equal, false otherwise.3) true if the contents of the lhs are lexicographically **less** than the contents of rhs, false otherwise.4) true if the contents of the lhs are lexicographically **less** than or **equal** to the contents of rhs, false otherwise.5) true if the contents of the lhs are lexicographically **greater** than the contents of rhs, false otherwise.6) true if the contents of the lhs are lexicographically **greater** than or **equal** to the contents of rhs, false otherwise.7) The relative order of the first pair of non-equivalent elements in lhs and rhs if there are such elements, lhs.size() <=> rhs.size() otherwise.

### Complexity

Linear in the size of the `array`.

### Notes

|  |  |
| --- | --- |
| The relational operators are defined in terms of the element type's operator<. | (until C++20) |
| The relational operators are defined in terms of **synth-three-way**, which uses operator<=> if possible, or operator< otherwise.  Notably, if the element does not itself provide operator<=>, but is implicitly convertible to a three-way comparable type, that conversion will be used instead of operator<. | (since C++20) |

### Example

Run this code

```
#include <cassert>
#include <compare>
#include <array>
 
int main()
{
    const std::array
        a{1, 2, 3},
        b{1, 2, 3},
        c{7, 8, 9};
 
    assert
    (""
        "Compare equal containers:" &&
        (a != b) == false &&
        (a == b) == true &&
        (a < b) == false &&
        (a <= b) == true &&
        (a > b) == false &&
        (a >= b) == true &&
        (a <=> b) != std::weak_ordering::less &&
        (a <=> b) != std::weak_ordering::greater &&
        (a <=> b) == std::weak_ordering::equivalent &&
        (a <=> b) >= 0 &&
        (a <=> b) <= 0 &&
        (a <=> b) == 0 &&
 
        "Compare non equal containers:" &&
        (a != c) == true &&
        (a == c) == false &&
        (a < c) == true &&
        (a <= c) == true &&
        (a > c) == false &&
        (a >= c) == false &&
        (a <=> c) == std::weak_ordering::less &&
        (a <=> c) != std::weak_ordering::equivalent &&
        (a <=> c) != std::weak_ordering::greater &&
        (a <=> c) < 0 &&
        (a <=> c) != 0 &&
        (a <=> c) <= 0 &&
    "");
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3431 | C++20 | operator<=> did not require `T` to model `three_way_comparable` | requires |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/array/operator_cmp&oldid=116774>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 February 2020, at 08:12.