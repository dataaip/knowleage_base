# std::inplace_vector<T,N>::swap

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | inplace_vector::inplace_vector | | | | | | inplace_vector::~inplace_vector | | | | | | inplace_vector::operator= | | | | | | inplace_vector::assign | | | | | | inplace_vector::assign_range | | | | | | Size and capacity | | | | | | inplace_vector::empty | | | | | | inplace_vector::size | | | | | | inplace_vector::max_size | | | | | | inplace_vector::capacity | | | | | | inplace_vector::resize | | | | | | inplace_vector::reserve | | | | | | inplace_vector::shrink_to_fit | | | | | | Iterators | | | | | | inplace_vector::begininplace_vector::cbegin | | | | | | inplace_vector::endinplace_vector::cend | | | | | | inplace_vector::rbegininplace_vector::crbegin | | | | | | inplace_vector::rendinplace_vector::crend | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | inplace_vector::at | | | | | | [inplace_vector::operator[]](operator_at.html "cpp/container/inplace vector/operator at") | | | | | | inplace_vector::front | | | | | | inplace_vector::back | | | | | | inplace_vector::data | | | | | | Modifiers | | | | | | inplace_vector::clear | | | | | | inplace_vector::erase | | | | | | ****inplace_vector::swap**** | | | | | | inplace_vector::insert | | | | | | inplace_vector::insert_range | | | | | | inplace_vector::emplace | | | | | | inplace_vector::emplace_back | | | | | | inplace_vector::try_emplace_back | | | | | | inplace_vector::unchecked_emplace_back | | | | | | inplace_vector::push_back | | | | | | inplace_vector::try_push_back | | | | | | inplace_vector::unchecked_push_back | | | | | | inplace_vector::pop_back | | | | | | inplace_vector::append_range | | | | | | inplace_vector::try_append_range | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | erase(std::inplace_vector)erase_if(std::inplace_vector) | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| constexpr void swap( inplace_vector& other ) noexcept(/\* see below \*/); |  | (since C++26) |
|  |  |  |

Exchanges the contents of the container with those of other. Does not cause iterators and references to associate with the other container.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | container to exchange the contents with |

### Return value

(none)

### Exceptions

noexcept specification:noexcept(N == 0 ||  
         (std::is_nothrow_swappable_v<T> && std::is_nothrow_move_constructible_v<T>))

### Complexity

Linear in size of the container.

### Example

Run this code

```
#include <inplace_vector>
#include <print>
 
int main()
{
    std::inplace_vector<int, 3> a1{1, 2, 3}, a2{4, 5, 6};
 
    auto i1 = a1.begin();
    auto i2 = a2.begin();
    int& r1 = a1[1];
    int& r2 = a2[1];
 
    auto print_them_all = &
    {
        std::println("{}a1 = {}, a2 = {}, *i1 = {}, *i2 = {}, r1 = {}, r2 = {}",
                     rem, a1, a2, *i1, *i2, r1, r2);
    };
 
    print_them_all("Before swap:\n");
    a1.swap(a2);
    print_them_all("After swap:\n");
 
    // Note that after swap() iterators and references stay associated with their
    // original sites, e.g., i1 points to element a1[0], r1 refers to a1[1].
}

```

Output:

```
Before swap:
a1 = [1, 2, 3], a2 = [4, 5, 6], *i1 = 1, *i2 = 4, r1 = 2, r2 = 5
After swap:
a1 = [4, 5, 6], a2 = [1, 2, 3], *i1 = 4, *i2 = 1, r1 = 5, r2 = 2

```

### See also

|  |  |
| --- | --- |
| std::swap(std::inplace_vector)(C++26) | specializes the std::swap algorithm   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector/swap&oldid=175276>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 August 2024, at 22:33.