# std::vector<bool,Allocator>::swap

From cppreference.com
< cpp‎ | container‎ | vector bool
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

std::vector<bool>

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| vector<bool>::reference | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | vector::vector | | | | | | vector::~vector | | | | | | vector::operator= | | | | | | vector::assign | | | | | | vector::assign_range(C++23) | | | | | | vector::get_allocator | | | | | | Element access | | | | | | [vector::operator[]](../vector/operator_at.html "cpp/container/vector/operator at") | | | | | | vector::at | | | | | | vector::front | | | | | | vector::back | | | | | | Iterators | | | | | | vector::beginvector::cbegin(C++11) | | | | | | vector::endvector::cend(C++11) | | | | | | vector::rbeginvector::crbegin(C++11) | | | | | | vector::rendvector::crend(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | vector::empty | | | | | | vector::size | | | | | | vector::max_size | | | | | | vector::capacity | | | | | | vector::resize | | | | | | vector::reserve | | | | | | vector::shrink_to_fit(DR\*) | | | | | | Modifiers | | | | | | vector::clear | | | | | | vector::erase | | | | | | vector::insert | | | | | | vector::insert_range(C++23) | | | | | | vector::append_range(C++23) | | | | | | vector::emplace(C++11) | | | | | | vector::emplace_back(C++11) | | | | | | vector::push_back | | | | | | vector::pop_back | | | | | | vector::swap | | | | | | vector<bool>::flip | | | | | | ****vector<bool>::swap**** | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::vector<bool>) | | | | | | erase(std::vector<bool>)erase_if(std::vector<bool>)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Helper classes | | | | |
| hash<std::vector<bool>>(C++11) | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<vector>` |  |  |
| static void swap( reference x, reference y ); |  | (constexpr since C++20) |
|  |  |  |

Swaps the contents of x and y as if by bool b = x; x = y; y = b;.

### Parameters

|  |  |  |
| --- | --- | --- |
| x | - | `std::vector`<bool>::`reference` value to swap with y |
| y | - | `std::vector`<bool>::`reference` value to swap with x |

### Return value

(none)

### Complexity

Constant.

### Example

Run this code

```
#include <iostream>
#include <vector>
 
void println(std::string_view fmt, std::vector<bool> const& vb = {})
{
    for (std::cout << fmt; bool const e : vb)
        std::cout << e << ' ';
    std::cout << '\n';
}
 
int main()
{
    println("swap elements of the same vector:");
    std::vector<bool> x{1, 0};
    println("before swap, x: ", x);
    x.swap(x[0], x[1]); // same as std::vector<bool>::swap(x[0], x[1]);
    println("after swap,  x: ", x);
 
    println("swap elements of two different vectors:");
    std::vector<bool> y{0, 0, 1};
    println("before swap, x: ", x);
    println("before swap, y: ", y);
    y.swap(x[0], y[2]); // same as std::vector<bool>::swap(x[0], y[2]);
    println("after swap,  x: ", x);
    println("after swap,  y: ", y);
}

```

Output:

```
swap elements of the same vector:
before swap, x: 1 0 
after swap,  x: 0 1 
swap elements of two different vectors:
before swap, x: 0 1 
before swap, y: 0 0 1 
after swap,  x: 1 1 
after swap,  y: 0 0 0

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 814 | C++98 | the description of this member function was missing | added |

### See also

|  |  |
| --- | --- |
| reference | proxy class representing a reference to a single bool   (class) |
| swap | swaps the contents   (public member function of `std::vector<T,Allocator>`) |
| std::swap(std::vector) | specializes the std::swap algorithm   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/vector_bool/swap&oldid=178319>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 December 2024, at 15:02.