# std::get(std::array)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | ****get(std::array)**** | | | | | | swap(std::array) | | | | | | to_array(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator|=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Helper classes | | | | |
| tuple_size<std::array> | | | | |
| tuple_element<std::array> | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<array>` |  |  |
| template< std::size_t I, class T, std::size_t N >  T& get( std::array<T,N>& a ) noexcept; | (1) | (since C++11)  (constexpr since C++14) |
| template< std::size_t I, class T, std::size_t N >  T&& get( std::array<T,N>&& a ) noexcept; | (2) | (since C++11)  (constexpr since C++14) |
| template< std::size_t I, class T, std::size_t N >  const T& get( const std::array<T,N>& a ) noexcept; | (3) | (since C++11)  (constexpr since C++14) |
| template< std::size_t I, class T, std::size_t N >  const T&& get( const std::array<T,N>&& a ) noexcept; | (4) | (since C++11)  (constexpr since C++14) |
|  |  |  |

Extracts the `I`th element from the array using tuple-like interface.

`I` must be an integer value in range ``​0​`,`N`)`. This is enforced at compile time as opposed to [at() or [operator[]](operator_at.html "cpp/container/array/operator at").

### Parameters

|  |  |  |
| --- | --- | --- |
| a | - | array whose contents to extract |

### Return value

A reference to the `I`th element of a.

### Complexity

Constant.

### Example

Run this code

```
#include <array>
#include <iostream>
 
constexpr std::array v{1, 2, 3};
static_assert(get<0>(v) == 1 && get<1>(v) == 2 && get<2>(v) == 3);
 
int main()
{
    std::array<int, 3> a;
 
    // set values:
    get<0>(a) = 1, get<1>(a) = 2, get<2>(a) = 3;
 
    // get values:
    std::cout << '(' << get<0>(a) << ',' << get<1>(a) << ',' << get<2>(a) << ")\n";
}

```

Output:

```
(1,2,3)

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2485 | C++11 | there are no overloads for const array&& | the overloads are added |

### See also

|  |  |
| --- | --- |
| Structured binding (C++17) | binds the specified names to sub-objects or tuple elements of the initializer |
| [operator[]](operator_at.html "cpp/container/array/operator at") | access specified element   (public member function) |
| at | access specified element with bounds checking   (public member function) |
| get(std::tuple)(C++11) | tuple accesses specified element   (function template) |
| get(std::pair)(C++11) | accesses an element of a `pair`   (function template) |
| get(std::variant)(C++17) | reads the value of the variant given the index or the type (if the type is unique), throws on error   (function template) |
| get(std::ranges::subrange)(C++20) | obtains iterator or sentinel from a std::ranges::subrange   (function template) |
| get(std::complex)(C++26) | obtains a reference to real or imaginary part from a std::complex   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/array/get&oldid=175376>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 August 2024, at 05:21.