# std::flat_set<Key,Compare,KeyContainer>::replace

From cppreference.com
< cpp‎ | container‎ | flat set
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

std::flat_set

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_set::flat_set | | | | | | flat_set::operator= | | | | | | Iterators | | | | | | flat_set::beginflat_set::cbegin | | | | | | flat_set::endflat_set::cend | | | | | | flat_set::rbeginflat_set::crbegin | | | | | | flat_set::rendflat_set::crend | | | | | | Capacity | | | | | | flat_set::size | | | | | | flat_set::max_size | | | | | | flat_set::empty | | | | | | Observers | | | | | | flat_set::key_comp | | | | | | flat_set::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | flat_set::clear | | | | | | flat_set::insert | | | | | | flat_set::insert_range | | | | | | flat_set::emplace | | | | | | flat_set::emplace_hint | | | | | | flat_set::erase | | | | | | flat_set::swap | | | | | | flat_set::extract | | | | | | ****flat_set::replace**** | | | | | | Lookup | | | | | | flat_set::count | | | | | | flat_set::find | | | | | | flat_set::contains | | | | | | flat_set::equal_range | | | | | | flat_set::lower_bound | | | | | | flat_set::upper_bound | | | | | | | Non-member functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_set) | | | | | | erase_if(std::flat_set) | | | | | | |
| Helper classes | | | | |
| uses_allocator<std::flat_set> | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| void replace( container_type&& cont ); |  | (since C++23) |
|  |  |  |

Replaces the underlying container `c`. Equivalent to:
c = std::move(cont);.

The elements of cont must be sorted with respect to `compare`, and cont must not contain equal elements. Otherwise, the behavior is undefined.

### Parameters

|  |  |  |
| --- | --- | --- |
| cont | - | a sorted container of type `KeyContainer`, the contents of which will be moved into \*this |

### Return value

(none)

### Complexity

Equals to complexity of std::move applied to adapted container.

### Example

Run this code

```
#include <algorithm>
#include <cassert>
#include <flat_set>
#include <print>
#include <vector>
 
int main()
{
    std::vector<int> keys{1, 2, 3};
    assert(std::ranges::is_sorted(keys));
 
    std::flat_set<int> set;
    assert(set.empty());
 
    set.replace(keys);
    assert(set.size() == 3);
    assert(keys.empty());
 
    std::println("{}", set); // set.keys()
}

```

Output:

```
[1, 2, 3]

```

### See also

|  |  |
| --- | --- |
| extract | extracts the underlying container   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_set/replace&oldid=169483>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 February 2024, at 14:17.