# std::flat_map<Key,T,Compare,KeyContainer,MappedContainer>::insert_or_assign

From cppreference.com
< cpp‎ | container‎ | flat map
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

std::flat_map

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_map::flat_map | | | | | | flat_map::operator= | | | | | | Element access | | | | | | flat_map::at | | | | | | [flat_map::operator[]](operator_at.html "cpp/container/flat map/operator at") | | | | | | Iterators | | | | | | flat_map::beginflat_map::cbegin | | | | | | flat_map::endflat_map::cend | | | | | | flat_map::rbeginflat_map::crbegin | | | | | | flat_map::rendflat_map::crend | | | | | | Lookup | | | | | | flat_map::count | | | | | | flat_map::find | | | | | | flat_map::contains | | | | | | flat_map::equal_range | | | | | | flat_map::lower_bound | | | | | | flat_map::upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | flat_map::size | | | | | | flat_map::max_size | | | | | | flat_map::empty | | | | | | Modifiers | | | | | | flat_map::clear | | | | | | flat_map::erase | | | | | | flat_map::swap | | | | | | flat_map::emplace | | | | | | flat_map::extract | | | | | | flat_map::replace | | | | | | flat_map::insert | | | | | | flat_map::insert_range | | | | | | ****flat_map::insert_or_assign**** | | | | | | flat_map::emplace_hint | | | | | | flat_map::try_emplace | | | | | | Observers | | | | | | flat_map::key_comp | | | | | | flat_map::keys | | | | | | flat_map::value_comp | | | | | | flat_map::values | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_map) | | | | | | erase_if(std::flat_map) | | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uses_allocator<std::flat_map> | | | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_unique_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| template< class M >  std::pair<iterator, bool> insert_or_assign( const key_type& k, M&& obj ); | (1) | (since C++23) |
| template< class M >  std::pair<iterator, bool> insert_or_assign( key_type&& k, M&& obj ); | (2) | (since C++23) |
| template< class K, class M >  std::pair<iterator, bool> insert_or_assign( K&& k, M&& obj ); | (3) | (since C++23) |
| template< class M >  iterator insert_or_assign( const_iterator hint, const key_type& k, M&& obj ); | (4) | (since C++23) |
| template< class M >  iterator insert_or_assign( const_iterator hint, key_type&& k, M&& obj ); | (5) | (since C++23) |
| template< class K, class M >  iterator insert_or_assign( const_iterator hint, K&& k, M&& obj ); | (6) | (since C++23) |
|  |  |  |

1,2) If a key equivalent to k already exists in the container, assigns std::forward<M>(obj) to the `mapped_type` corresponding to the key k. If the key does not exist, inserts the new value as if by

- (1,2) try_emplace(std::forward<decltype(k)>(k), std::forward<M>(obj)),
- (4,5) try_emplace(hint, std::forward<decltype(k)>(k), std::forward<M>(obj)).
 The program is ill-formed if either std::is_assignable_v<mapped_type&, M> or std::is_constructible_v<mapped_type, M> is false.3,6) If a key equivalent to k already exists in the container, assigns std::forward<M>(obj) to the `mapped_type` corresponding to the key k. Otherwise, equivalent to

- (3) try_emplace(std::forward<K>(k), std::forward<M>(obj)),
- (6) try_emplace(hint, std::forward<K>(k), std::forward<M>(obj)).
 The conversion from k into `key_type` must construct an object u, for which find(k) == find(u) is true. Otherwise, the behavior is undefined. These overloads participate in overload resolution only if :

- The qualified-id `Compare::is_transparent` is valid and denotes a type.
- std::is_constructible_v<key_type, K> is true.
- std::is_assignable_v<mapped_type&, M> is true.
- std::is_constructible_v<mapped_type, M> is true.

|  |  |
| --- | --- |
|  | Information on iterator invalidation is copied from here |

### Parameters

|  |  |  |
| --- | --- | --- |
| k | - | the key used both to look up and to insert if not found |
| hint | - | iterator to the position before which the new element will be inserted |
| obj | - | the value to insert or assign |

### Return value

1-3) The bool component is true if the insertion took place and false if the assignment took place. The iterator component is pointing at the element that was inserted or updated.4-6) Iterator pointing at the element that was inserted or updated.

### Complexity

1-3) Same as for `emplace`.4-6) Same as for `emplace_hint`.

### Notes

`insert_or_assign` returns more information than `operator`[] and does not require default-constructibility of the mapped type.

### Example

Run this code

```
#include <flat_map>
#include <iostream>
#include <string>
 
void print_node(const auto& node)
{
    std::cout << '[' << node.first << "] = " << node.second << '\n';
}
 
void print_result(auto const& pair)
{
    std::cout << (pair.second ? "inserted: " : "assigned: ");
    print_node(*pair.first);
}
 
int main()
{
    std::flat_map<std::string, std::string> map;
 
    print_result(map.insert_or_assign("a", "apple"));
    print_result(map.insert_or_assign("b", "banana"));
    print_result(map.insert_or_assign("c", "cherry"));
    print_result(map.insert_or_assign("c", "clementine"));
 
    for (const auto& node : map)
        print_node(node);
}

```

Output:

```
inserted: [a] = apple
inserted: [b] = banana
inserted: [c] = cherry
assigned: [c] = clementine
[a] = apple
[b] = banana
[c] = clementine

```

### See also

|  |  |
| --- | --- |
| [operator[]](operator_at.html "cpp/container/flat map/operator at") | access or insert specified element   (public member function) |
| at | access specified element with bounds checking   (public member function) |
| insert | inserts elements   (public member function) |
| emplace | constructs element in-place   (public member function) |
| try_emplace | inserts in-place if the key does not exist, does nothing if the key exists   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_map/insert_or_assign&oldid=171981>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 May 2024, at 23:18.