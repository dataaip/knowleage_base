# std::erase, std::erase_if(std::inplace_vector)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****erase(std::inplace_vector)erase_if(std::inplace_vector)**** | | | | | | swap(std::inplace_vector) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | |  | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<inplace_vector>` |  |  |
| template< class T, std::size_t N, class U = T >  constexpr typename std::inplace_vector<T, N>::size_type     erase( std::inplace_vector<T, N>& c, const U& value ); | (1) | (since C++26) |
| template< class T, std::size_t N, class Pred >  constexpr typename std::inplace_vector<T, N>::size_type     erase_if( std::inplace_vector<T, N>& c, Pred pred ); | (2) | (since C++26) |
|  |  |  |

1) Erases all elements that compare equal to value from the container. Equivalent to

```
auto it = std::remove(c.begin(), c.end(), value);
auto r = std::distance(it, c.end());
c.erase(it, c.end());
return r;

```

2) Erases all elements that satisfy the predicate pred from the container. Equivalent to

```
auto it = std::remove_if(c.begin(), c.end(), pred);
auto r = std::distance(it, c.end());
c.erase(it, c.end());
return r;

```

### Parameters

|  |  |  |
| --- | --- | --- |
| c | - | container from which to erase |
| value | - | value to be removed |
| pred | - | unary predicate which returns ​true if the element should be erased.   The expression pred(v) must be convertible to bool for every argument `v` of type (possibly const) `T`, regardless of value category, and must not modify `v`. Thus, a parameter type of T&is not allowed, nor is T unless for `T` a move is equivalent to a copy(since C++11). ​ |

### Return value

The number of erased elements.

### Complexity

Linear.

### Example

Run this code

```
#include <cassert>
#include <complex>
#include <inplace_vector>
#include <numeric>
#include <print>
 
int main()
{
    std::inplace_vector<int, 10> v(10, 0);
    std::ranges::iota(v, 0);
    std::println("Initially, v = {}", v);
 
    auto erased = std::erase(v, 3);
    std::println("After erase(v, 3), v = {}", v);
    assert(erased == 1);
 
    erased = std::erase_if(v, [](int x) { return x % 2 == 0; });
    std::println("After erasing all even numbers, v = {}", v);
    std::println("Erased even numbers: {}", erased);
 
    std::inplace_vector<std::complex<double>> nums{{2, 2}, {4, 2}, {4, 8}, {4, 2}};
    std::erase(nums, {4, 2}); // since U = T, the value type can be ommited
    std::println("After erase {4, 2}, nums = {}", nums);
}

```

Output:

```
Initially, v = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
After erase(v, 3), v = [0, 1, 2, 4, 5, 6, 7, 8, 9]
After erasing all even numbers, v = [1, 5, 7, 9]
Erased even numbers: 5
After erase {4, 2}, nums = [(2,2), (4,8)]

```

### See also

|  |  |
| --- | --- |
| removeremove_if | removes elements satisfying specific criteria   (function template) |
| ranges::removeranges::remove_if(C++20)(C++20) | removes elements satisfying specific criteria (algorithm function object) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/inplace_vector/erase2&oldid=175548>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 August 2024, at 13:37.