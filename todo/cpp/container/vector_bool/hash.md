# std::hash<std::vector<bool>>

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | vector::vector | | | | | | vector::~vector | | | | | | vector::operator= | | | | | | vector::assign | | | | | | vector::assign_range(C++23) | | | | | | vector::get_allocator | | | | | | Element access | | | | | | [vector::operator[]](../vector/operator_at.html "cpp/container/vector/operator at") | | | | | | vector::at | | | | | | vector::front | | | | | | vector::back | | | | | | Iterators | | | | | | vector::beginvector::cbegin(C++11) | | | | | | vector::endvector::cend(C++11) | | | | | | vector::rbeginvector::crbegin(C++11) | | | | | | vector::rendvector::crend(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | vector::empty | | | | | | vector::size | | | | | | vector::max_size | | | | | | vector::capacity | | | | | | vector::resize | | | | | | vector::reserve | | | | | | vector::shrink_to_fit(DR\*) | | | | | | Modifiers | | | | | | vector::clear | | | | | | vector::erase | | | | | | vector::insert | | | | | | vector::insert_range(C++23) | | | | | | vector::append_range(C++23) | | | | | | vector::emplace(C++11) | | | | | | vector::emplace_back(C++11) | | | | | | vector::push_back | | | | | | vector::pop_back | | | | | | vector::swap | | | | | | vector<bool>::flip | | | | | | vector<bool>::swap | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::vector<bool>) | | | | | | erase(std::vector<bool>)erase_if(std::vector<bool>)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Helper classes | | | | |
| ****hash<std::vector<bool>>****(C++11) | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<vector>` |  |  |
| template< class Allocator >  struct hash<std::vector<bool, Allocator>>; |  | (since C++11) |
|  |  |  |

The template specialization of std::hash for std::vector<bool> allows users to obtain hashes of objects of type std::vector<bool>.

### Example

Run this code

```
#include <iostream>
#include <unordered_set>
#include <vector>
 
using vb = std::vector<bool>;
 
vb to_vector_bool(unsigned n)
{
    vb v;
    do
    {
        v.push_back(n & 1);
        n >>= 1;
    }
    while (n);
    return v;
}
 
auto print(const vb& v, bool new_line = true)
{
    for (std::cout << "{ "; const bool e : v)
        std::cout << e << ' ';
    std::cout << '}' << (new_line ? '\n' : ' ');
}
 
int main()
{
    for (auto i{0U}; i != 8; ++i)
    {
        std::cout << std::hex << std::uppercase;
        vb v = to_vector_bool(i);
        std::cout << std::hash<vb>{}(v) << ' ' << std::dec;
        print(v);
    }
 
    // std::hash for vector<bool> makes it possible to keep them in
    // unordered_* associative containers, such as unordered_set.
 
    std::unordered_set v{vb{0}, vb{0, 0}, vb{1}, vb{1}, vb{1, 0}, vb{1, 1}};
 
    for (vb const& e : v)
        print(e, 0);
    std::cout << '\n';
}

```

Possible output:

```
6D09EE26D5863619 { 0 }
3C27D9F591D20E49 { 1 }
E74D3F72B7599C63 { 0 1 }
EE3BE81F55123770 { 1 1 }
3AAD2A2EDBEC6C35 { 0 0 1 }
EB057F773CB64C43 { 1 0 1 }
6E1354730102BE00 { 0 1 1 }
E2E622597C18899D { 1 1 1 }
{ 1 1 } { 1 0 } { 1 } { 0 0 } { 0 }

```

### See also

|  |  |
| --- | --- |
| hash(C++11) | hash function object   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/vector_bool/hash&oldid=165918>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 December 2023, at 19:26.