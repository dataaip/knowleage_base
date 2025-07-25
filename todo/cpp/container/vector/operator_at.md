# std::vector<T,Allocator>::operator[]

From cppreference.com
< cpp‎ | container‎ | vector
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

std::vector

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | vector::vector | | | | | | vector::~vector | | | | | | vector::operator= | | | | | | vector::assign | | | | | | vector::assign_range(C++23) | | | | | | vector::get_allocator | | | | | | Element access | | | | | | ****vector::operator[]**** | | | | | | vector::at | | | | | | vector::data | | | | | | vector::front | | | | | | vector::back | | | | | | Iterators | | | | | | vector::beginvector::cbegin(C++11) | | | | | | vector::endvector::cend(C++11) | | | | | | vector::rbeginvector::crbegin(C++11) | | | | | | vector::rendvector::crend(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | vector::empty | | | | | | vector::size | | | | | | vector::max_size | | | | | | vector::reserve | | | | | | vector::capacity | | | | | | vector::shrink_to_fit(DR\*) | | | | | | Modifiers | | | | | | vector::clear | | | | | | vector::erase | | | | | | vector::insert | | | | | | vector::insert_range(C++23) | | | | | | vector::append_range(C++23) | | | | | | vector::emplace(C++11) | | | | | | vector::emplace_back(C++11) | | | | | | vector::push_back | | | | | | vector::pop_back | | | | | | vector::resize | | | | | | vector::swap | | | | | |  | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::vector) | | | | | | erase(std::vector)erase_if(std::vector)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| reference operator[]( size_type pos ); | (1) | (constexpr since C++20) |
| const_reference operator[]( size_type pos ) const; | (2) | (constexpr since C++20) |
|  |  |  |

Returns a reference to the element at specified location pos. No bounds checking is performed.

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | position of the element to return |

### Return value

Reference to the requested element.

### Complexity

Constant.

### Notes

Unlike [std::map::operator[]](../map/operator_at.html "cpp/container/map/operator at"), this operator never inserts a new element into the container. Accessing a nonexistent element through this operator is undefined behavior.

### Example

The following code uses operator[] to read from and write to a std::vector<int>:

Run this code

```
#include <vector>
#include <iostream>
 
int main()
{
    std::vector<int> numbers{2, 4, 6, 8};
 
    std::cout << "Second element: " << numbers[1] << '\n';
 
    numbers[0] = 5;
 
    std::cout << "All numbers:";
    for (auto i : numbers)
        std::cout << ' ' << i;
    std::cout << '\n';
}
 
// Since C++20 std::vector can be used in constexpr context:
#if defined(__cpp_lib_constexpr_vector) and defined(__cpp_consteval)
// Gets the sum of all primes in [0, N) using sieve of Eratosthenes
consteval auto sum_of_all_primes_up_to(unsigned N)
{
    if (N < 2)
        return 0ULL;
 
    std::vector<bool> is_prime(N, true);
    is_prime[0] = is_prime[1] = false;
 
    auto propagate_non_primality = & n)
    {
        for (decltype(N) m = n + n; m < is_prime.size(); m += n)
            is_prime[m] = false;
    };
 
    auto sum{0ULL};
    for (decltype(N) n{2}; n != N; ++n)
        if (is_prime[n])
        {
            sum += n;
            propagate_non_primality(n);
        }
 
    return sum;
} //< vector's memory is released here
 
static_assert(sum_of_all_primes_up_to(42) == 0xEE);
static_assert(sum_of_all_primes_up_to(100) == 0x424);
static_assert(sum_of_all_primes_up_to(1001) == 76127);
#endif

```

Output:

```
Second element: 4
All numbers: 5 4 6 8

```

### See also

|  |  |
| --- | --- |
| at | access specified element with bounds checking   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/vector/operator_at&oldid=120372>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 June 2020, at 07:08.