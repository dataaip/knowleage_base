# operator==,<=>(std::inplace_vector)

From cppreference.com
< cpp‎ | container‎ | inplace vector
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

std::inplace_vector

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_vector::inplace_vector | | | | | | inplace_vector::~inplace_vector | | | | | | inplace_vector::operator= | | | | | | inplace_vector::assign | | | | | | inplace_vector::assign_range | | | | | | Size and capacity | | | | | | inplace_vector::empty | | | | | | inplace_vector::size | | | | | | inplace_vector::max_size | | | | | | inplace_vector::capacity | | | | | | inplace_vector::resize | | | | | | inplace_vector::reserve | | | | | | inplace_vector::shrink_to_fit | | | | | | Iterators | | | | | | inplace_vector::begininplace_vector::cbegin | | | | | | inplace_vector::endinplace_vector::cend | | | | | | inplace_vector::rbegininplace_vector::crbegin | | | | | | inplace_vector::rendinplace_vector::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | inplace_vector::at | | | | | | [inplace_vector::operator[]](operator_at.html "cpp/container/inplace vector/operator at") | | | | | | inplace_vector::front | | | | | | inplace_vector::back | | | | | | inplace_vector::data | | | | | | Modifiers | | | | | | inplace_vector::clear | | | | | | inplace_vector::erase | | | | | | inplace_vector::swap | | | | | | inplace_vector::insert | | | | | | inplace_vector::insert_range | | | | | | inplace_vector::emplace | | | | | | inplace_vector::emplace_back | | | | | | inplace_vector::try_emplace_back | | | | | | inplace_vector::unchecked_emplace_back | | | | | | inplace_vector::push_back | | | | | | inplace_vector::try_push_back | | | | | | inplace_vector::unchecked_push_back | | | | | | inplace_vector::pop_back | | | | | | inplace_vector::append_range | | | | | | inplace_vector::try_append_range | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erase(std::inplace_vector)erase_if(std::inplace_vector) | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****operator==operator<=>**** | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr friend bool operator==( const std::inplace_vector<T, N>& lhs,                                    const std::inplace_vector<T, N>& rhs ); | (1) | (since C++26) |
| constexpr friend synth-three-way-result<T>      operator<=>( const std::inplace_vector<T, N>& lhs, const std::inplace_vector<T, N>& rhs ); | (2) | (since C++26) |
|  |  |  |

Compares the contents of two std::inplace_vectors.

1) Checks if the contents of lhs and rhs are equal, that is, they have the same number of elements and each element in lhs compares equal with the element in rhs at the same position.2) Compares the contents of lhs and rhs lexicographically. The comparison is performed as if by calling  
std::lexicographical_compare_three_way(lhs.begin(), lhs.end(),  
                                       rhs.begin(), rhs.end(), synth-three-way);. The return type is the return type of **synth-three-way** (i.e., **synth-three-way-result** ﻿<T>). At least one of the following conditions must be satisfied:

- `T` models `three_way_comparable`.
- `<` is defined for values of type (possibly const-qualified) `T`, and `<` is a total ordering relationship.

   Otherwise, the behavior is undefined.

The `<`, `<=`, `>`, `>=`, and `!=` operators are synthesized from operator<=> and operator== respectively.

### Parameters

|  |  |  |
| --- | --- | --- |
| lhs, rhs | - | std::inplace_vectors whose contents to compare |
| -`T` must meet the requirements of EqualityComparable in order to use overloads (1). | | |

### Return value

1) true if the contents of the std::inplace_vectors are equal, false otherwise.2) The relative order of the first pair of non-equivalent elements in lhs and rhs if there are such elements, lhs.size() <=> rhs.size() otherwise.

### Complexity

1) Constant if lhs and rhs are of different size, otherwise linear in the size of the std::inplace_vector.2) Linear in the size of the std::inplace_vector.

### Notes

The relational operators are defined in terms of **synth-three-way**, which uses operator<=> if possible, or operator< otherwise.

Notably, if the element does not itself provide operator<=>, but is implicitly convertible to a three-way comparable type, that conversion will be used instead of operator<.

### Example

Run this code

```
#include <inplace_vector>
 
int main()
{
    constexpr std::inplace_vector<int, 4>
        a{1, 2, 3},
        b{1, 2, 3},
        c{7, 8, 9, 10};
 
    static_assert
    (""
        "Compare equal containers:" &&
        (a != b) == false &&
        (a == b) == true &&
        (a < b) == false &&
        (a <= b) == true &&
        (a > b) == false &&
        (a >= b) == true &&
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
        (a <=> c) < 0 &&
        (a <=> c) != 0 &&
        (a <=> c) <= 0 &&
    "");
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector/operator_cmp&oldid=175563>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 August 2024, at 03:18.