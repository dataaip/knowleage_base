# std::multiset<Key,Compare,Allocator>::contains

From cppreference.com
< cpp‎ | container‎ | multiset
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

std::multiset

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multiset::multiset | | | | | | multiset::~multiset | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | multiset::operator= | | | | | | multiset::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | multiset::beginmultiset::cbegin(C++11) | | | | | | multiset::endmultiset::cend(C++11) | | | | | | multiset::rbeginmultiset::crbegin(C++11) | | | | | | multiset::rendmultiset::crend(C++11) | | | | | | Capacity | | | | | | multiset::size | | | | | | multiset::max_size | | | | | | multiset::empty | | | | | | Observers | | | | | | multiset::key_comp | | | | | | multiset::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | multiset::clear | | | | | | multiset::erase | | | | | | multiset::swap | | | | | | multiset::extract(C++17) | | | | | | multiset::merge(C++17) | | | | | | multiset::insert | | | | | | multiset::insert_range(C++23) | | | | | | multiset::emplace(C++11) | | | | | | multiset::emplace_hint(C++11) | | | | | | Lookup | | | | | | multiset::count | | | | | | multiset::find | | | | | | ****multiset::contains****(C++20) | | | | | | multiset::equal_range | | | | | | multiset::lower_bound | | | | | | multiset::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::multiset) | | | | | | erase_if(std::multiset)(C++20) | | | | | | operator==operator<=>(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| bool contains( const Key& key ) const; | (1) | (since C++20) |
| template< class K >  bool contains( const K& x ) const; | (2) | (since C++20) |
|  |  |  |

1) Checks if there is an element with key equivalent to key in the container.2) Checks if there is an element with key that compares **equivalent** to the value x. This overload participates in overload resolution only if the qualified-id Compare::is_transparent is valid and denotes a type. It allows calling this function without constructing an instance of `Key`.

### Parameters

|  |  |  |
| --- | --- | --- |
| key | - | key value of the element to search for |
| x | - | a value of any type that can be transparently compared with a key |

### Return value

true if there is such an element, otherwise false.

### Complexity

Logarithmic in the size of the container.

### Example

Run this code

```
#include <iostream>
#include <set>
 
int main()
{
    std::multiset<int> example{1, 2, 3, 4};
 
    for (int x : {2, 5})
        if (example.contains(x))
            std::cout << x << ": Found\n";
        else
            std::cout << x << ": Not found\n";
}

```

Output:

```
2: Found
5: Not found

```

### See also

|  |  |
| --- | --- |
| find | finds element with specific key   (public member function) |
| count | returns the number of elements matching specific key   (public member function) |
| equal_range | returns range of elements matching a specific key   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/multiset/contains&oldid=161967>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 November 2023, at 01:08.