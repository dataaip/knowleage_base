# std::set<Key,Compare,Allocator>::value_comp

From cppreference.com
< cpp‎ | container‎ | set
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

std::set

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set::set | | | | | | set::~set | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | set::operator= | | | | | | set::get_allocator | | | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | set::beginset::cbegin(C++11) | | | | | | set::endset::cend(C++11) | | | | | | set::rbeginset::crbegin(C++11) | | | | | | set::rendset::crend(C++11) | | | | | | Capacity | | | | | | set::size | | | | | | set::max_size | | | | | | set::empty | | | | | | Observers | | | | | | set::key_comp | | | | | | ****set::value_comp**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | set::clear | | | | | | set::erase | | | | | | set::swap | | | | | | set::extract(C++17) | | | | | | set::merge(C++17) | | | | | | set::insert | | | | | | set::insert_range(C++23) | | | | | | set::emplace(C++11) | | | | | | set::emplace_hint(C++11) | | | | | | Lookup | | | | | | set::count | | | | | | set::find | | | | | | set::contains(C++20) | | | | | | set::equal_range | | | | | | set::lower_bound | | | | | | set::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::set) | | | | | | erase_if(std::set)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| std::set::value_compare value_comp() const; |  |  |
|  |  |  |

Returns the function object that compares the values. It is the same as key_comp.

### Parameters

(none)

### Return value

The value comparison function object.

### Complexity

Constant.

### Example

Run this code

```
#include <iostream>
#include <set>
#include <utility>
 
// Example module 97 key compare function
struct ModCmp
{
    bool operator()(int lhs, int rhs) const
    {
        return (lhs % 97) < (rhs % 97);
    }
};
 
int main()
{
    std::set<int, ModCmp> cont{1, 2, 3, 4, 5};
 
    // Same behaviour as key_comp()
    auto comp_func = cont.value_comp();
 
    for (const int val{100}; const int key : cont)
    {
        const bool before = comp_func(key, val);
        const bool after = comp_func(val, key);
 
        std::cout << "Key (" << key << ") ";
        if (!before && !after)
            std::cout << "equivalent to key (" << val << ")\n";
        else if (before)
            std::cout << "goes before key (" << val << ")\n";
        else if (after)
            std::cout << "goes after key (" << val << ")\n";
        else
            std::unreachable();
    }
}

```

Output:

```
Key (1) goes before key (100)
Key (2) goes before key (100)
Key (3) equivalent to key (100)
Key (4) goes after key (100)
Key (5) goes after key (100)

```

### See also

|  |  |
| --- | --- |
| key_comp | returns the function that compares keys   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/set/value_comp&oldid=135450>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 November 2021, at 18:40.