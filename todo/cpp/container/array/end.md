# std::array<T,N>::end, std::array<T,N>::cend

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | array::at | | | | | | [array::operator[]](operator_at.html "cpp/container/array/operator at") | | | | | | array::front | | | | | | array::back | | | | | | array::data | | | | | | Operations | | | | | | array::fill | | | | | | array::swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | array::beginarray::cbegin | | | | | | ****array::endarray::cend**** | | | | | | array::rbeginarray::crbegin | | | | | | array::rendarray::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | array::empty | | | | | | array::size | | | | | | array::max_size | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | get(std::array) | | | | | | swap(std::array) | | | | | | to_array(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator|=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Helper classes | | | | |
| tuple_size<std::array> | | | | |
| tuple_element<std::array> | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| iterator end() noexcept; | (1) | (since C++11)  (constexpr since C++17) |
| const_iterator end() const noexcept; | (2) | (since C++11)  (constexpr since C++17) |
| const_iterator cend() const noexcept; | (3) | (since C++11)  (constexpr since C++17) |
|  |  |  |

Returns an iterator to the element following the last element of the `array`.

This element acts as a placeholder; attempting to access it results in undefined behavior.

!range-begin-end.svg

### Parameters

(none)

### Return value

Iterator to the element following the last element.

### Complexity

Constant.

### Example

Run this code

```
#include <algorithm>
#include <array>
#include <iomanip>
#include <iostream>
 
int main()
{
    std::cout << std::boolalpha;
 
    std::array<int, 0> empty;
    std::cout << "1) "
              << (empty.begin() == empty.end()) << ' '     // true
              << (empty.cbegin() == empty.cend()) << '\n'; // true
    // *(empty.begin()) = 42; // => undefined behavior at run-time
 
 
    std::array<int, 4> numbers{5, 2, 3, 4};
    std::cout << "2) "
              << (numbers.begin() == numbers.end()) << ' '    // false
              << (numbers.cbegin() == numbers.cend()) << '\n' // false
              << "3) "
              << *(numbers.begin()) << ' '    // 5
              << *(numbers.cbegin()) << '\n'; // 5
 
    *numbers.begin() = 1;
    std::cout << "4) " << *(numbers.begin()) << '\n'; // 1
    // *(numbers.cbegin()) = 42; // compile-time error: 
                                 // read-only variable is not assignable
 
    // print out all elements
    std::cout << "5) ";
    std::for_each(numbers.cbegin(), numbers.cend(), [](int x)
    {
        std::cout << x << ' ';
    });
    std::cout << '\n';
 
    constexpr std::array constants{'A', 'B', 'C'};
    static_assert(constants.begin() != constants.end());   // OK
    static_assert(constants.cbegin() != constants.cend()); // OK
    static_assert(*constants.begin() == 'A');              // OK
    static_assert(*constants.cbegin() == 'A');             // OK
    // *constants.begin() = 'Z'; // compile-time error: 
                                 // read-only variable is not assignable
}

```

Output:

```
1) true true
2) false false
3) 5 5
4) 1
5) 1 2 3 4

```

### See also

|  |  |
| --- | --- |
| begincbegin | returns an iterator to the beginning   (public member function) |
| endcend(C++11)(C++14) | returns an iterator to the end of a container or array   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/array/end&oldid=122725>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 September 2020, at 07:43.