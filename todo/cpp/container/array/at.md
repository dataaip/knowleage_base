# std::array<T,N>::at

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | ****array::at**** | | | | | | [array::operator[]](operator_at.html "cpp/container/array/operator at") | | | | | | array::front | | | | | | array::back | | | | | | array::data | | | | | | Operations | | | | | | array::fill | | | | | | array::swap | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | array::beginarray::cbegin | | | | | | array::endarray::cend | | | | | | array::rbeginarray::crbegin | | | | | | array::rendarray::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | array::empty | | | | | | array::size | | | | | | array::max_size | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | get(std::array) | | | | | | swap(std::array) | | | | | | to_array(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator|=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Helper classes | | | | |
| tuple_size<std::array> | | | | |
| tuple_element<std::array> | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| reference at( size_type pos ); | (1) | (since C++11)  (constexpr since C++17) |
| const_reference at( size_type pos ) const; | (2) | (since C++11)  (constexpr since C++14) |
|  |  |  |

Returns a reference to the element at specified location pos, with bounds checking.

If pos is not within the range of the container, an exception of type std::out_of_range is thrown.

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | position of the element to return |

### Return value

Reference to the requested element

### Exceptions

std::out_of_range if pos >= size().

### Complexity

Constant.

### Example

Run this code

```
#include <chrono>
#include <cstddef>
#include <iostream>
#include <array>
#include <stdexcept>
 
int main()
{
    std::array<int, 6> data{1, 2, 4, 5, 5, 6};
 
    // Set element 1
    data.at(1) = 88;
 
    // Read element 2
    std::cout << "Element at index 2 has value " << data.at(2) << '\n';
 
    std::cout << "data size = " << data.size() << '\n';
 
    try
    {
        // Try to set an element at random position >= size()
        auto moon_phase = []
        {
            return std::chrono::system_clock::now().time_since_epoch().count() % 8;
        };
        data.at(data.size() + moon_phase()) = 13;
    }
    catch(const std::out_of_range& ex)
    {
        std::cout << ex.what() << '\n';
    }
 
    // Print final values
    std::cout << "data:";
    for (int elem : data)
        std::cout << ' ' << elem;
    std::cout << '\n';
}

```

Possible output:

```
Element at index 2 has value 4
data size = 6
array::at: __n (which is 8) >= _Nm (which is 6)
data: 1 88 4 5 5 6

```

### See also

|  |  |
| --- | --- |
| [operator[]](operator_at.html "cpp/container/array/operator at") | access specified element   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/array/at&oldid=122662>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 24 September 2020, at 10:13.