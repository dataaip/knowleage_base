# std::map<Key,T,Compare,Allocator>::find

From cppreference.com
< cpp‎ | container‎ | map
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

`std::map`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | map::map | | | | | | map::~map | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | map::operator= | | | | | | map::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | map::at | | | | | | [map::operator[]](operator_at.html "cpp/container/map/operator at") | | | | | | Iterators | | | | | | map::beginmap::cbegin(C++11) | | | | | | map::endmap::cend(C++11) | | | | | | map::rbeginmap::crbegin(C++11) | | | | | | map::rendmap::crend(C++11) | | | | | | Capacity | | | | | | map::size | | | | | | map::max_size | | | | | | map::empty | | | | | | Observers | | | | | | map::key_comp | | | | | | map::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | map::clear | | | | | | map::insert | | | | | | map::erase | | | | | | map::swap | | | | | | map::extract(C++17) | | | | | | map::merge(C++17) | | | | | | map::insert_range(C++23) | | | | | | map::insert_or_assign(C++17) | | | | | | map::emplace(C++11) | | | | | | map::emplace_hint(C++11) | | | | | | map::try_emplace(C++17) | | | | | | Lookup | | | | | | map::count | | | | | | ****map::find**** | | | | | | map::contains(C++20) | | | | | | map::equal_range | | | | | | map::lower_bound | | | | | | map::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::map) | | | | | | erase_if(std::map)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| iterator find( const Key& key ); | (1) |  |
| const_iterator find( const Key& key ) const; | (2) |  |
| template< class K >  iterator find( const K& x ); | (3) | (since C++14) |
| template< class K >  const_iterator find( const K& x ) const; | (4) | (since C++14) |
|  |  |  |

1,2) Finds an element with key equivalent to key.3,4) Finds an element with key that compares **equivalent** to the value x. This overload participates in overload resolution only if the qualified-id Compare::is_transparent is valid and denotes a type. It allows calling this function without constructing an instance of `Key`.

### Parameters

|  |  |  |
| --- | --- | --- |
| key | - | key value of the element to search for |
| x | - | a value of any type that can be transparently compared with a key |

### Return value

An iterator to the requested element. If no such element is found, past-the-end (see end()) iterator is returned.

### Complexity

Logarithmic in the size of the container.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_generic_associative_lookup` | `201304L` | (C++14) | Heterogeneous comparison lookup in associative containers; overloads (3,4) |

### Example

Run this code

```
#include <iostream>
#include <map>
 
struct LightKey
{
    int x;
};
 
struct FatKey
{
    int x;
    int data[1000]; // a heavy blob
};
 
// As detailed above, the container must use std::less<> (or other transparent
// Comparator) to access these overloads. This includes standard overloads,
// such as comparison between std::string and std::string_view.
bool operator<(const FatKey& fk, const LightKey& lk) { return fk.x < lk.x; }
bool operator<(const LightKey& lk, const FatKey& fk) { return lk.x < fk.x; }
bool operator<(const FatKey& fk1, const FatKey& fk2) { return fk1.x < fk2.x; }
 
int main()
{
    // Simple comparison demo.
    std::map<int, char> example{{1, 'a'}, {2, 'b'}};
 
    if (auto search = example.find(2); search != example.end())
        std::cout << "Found " << search->first << ' ' << search->second << '\n';
    else
        std::cout << "Not found\n";
 
    // Transparent comparison demo.
    std::map<FatKey, char, std::less<>> example2{{{1, {}}, 'a'}, {{2, {}}, 'b'}};
 
    LightKey lk = {2};
    if (auto search = example2.find(lk); search != example2.end())
        std::cout << "Found " << search->first.x << ' ' << search->second << '\n';
    else
        std::cout << "Not found\n";
 
    // Obtaining const iterators.
    // Compiler decides whether to return iterator of (non) const type by way of
    // accessing map; to prevent intentional modification, one of the simplest
    // options is to access the map via a constant reference.
    const auto& example2ref = example2;
    if (auto search = example2ref.find(lk); search != example2.end())
    {
        std::cout << "Found " << search->first.x << ' ' << search->second << '\n';
    //  search->second = 'c'; // error: assignment of member
                              // 'std::pair<const FatKey, char>::second'
                              // in read-only object
    }
}

```

Output:

```
Found 2 b
Found 2 b
Found 2 b

```

### See also

|  |  |
| --- | --- |
| at | access specified element with bounds checking   (public member function) |
| [operator[]](operator_at.html "cpp/container/map/operator at") | access or insert specified element   (public member function) |
| count | returns the number of elements matching specific key   (public member function) |
| equal_range | returns range of elements matching a specific key   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/map/find&oldid=128814>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 May 2021, at 11:12.