# std::unordered_map<Key,T,Hash,KeyEqual,Allocator>::merge

From cppreference.com
< cpp‎ | container‎ | unordered map
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

std::unordered_map

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_map::unordered_map | | | | | | unordered_map::~unordered_map | | | | | | unordered_map::operator= | | | | | | unordered_map::get_allocator | | | | | | Iterators | | | | | | unordered_map::beginunordered_map::cbegin | | | | | | unordered_map::endunordered_map::cend | | | | | | Capacity | | | | | | unordered_map::size | | | | | | unordered_map::max_size | | | | | | unordered_map::empty | | | | | | Modifiers | | | | | | unordered_map::clear | | | | | | unordered_map::erase | | | | | | unordered_map::swap | | | | | | unordered_map::extract(C++17) | | | | | | ****unordered_map::merge****(C++17) | | | | | | unordered_map::insert | | | | | | unordered_map::insert_range(C++23) | | | | | | unordered_map::insert_or_assign(C++17) | | | | | | unordered_map::emplace | | | | | | unordered_map::emplace_hint | | | | | | unordered_map::try_emplace(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_map::at | | | | | | [unordered_map::operator[]](operator_at.html "cpp/container/unordered map/operator at") | | | | | | unordered_map::count | | | | | | unordered_map::find | | | | | | unordered_map::contains(C++20) | | | | | | unordered_map::equal_range | | | | | | Bucket interface | | | | | | unordered_map::begin(size_type)unordered_map::cbegin(size_type) | | | | | | unordered_map::end(size_type)unordered_map::cend(size_type) | | | | | | unordered_map::bucket_count | | | | | | unordered_map::max_bucket_count | | | | | | unordered_map::bucket_size | | | | | | unordered_map::bucket | | | | | | Hash policy | | | | | | unordered_map::load_factor | | | | | | unordered_map::max_load_factor | | | | | | unordered_map::rehash | | | | | | unordered_map::reserve | | | | | | Observers | | | | | | unordered_map::hash_function | | | | | | unordered_map::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_map) | | | | | | erase_if(std::unordered_map)(C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| template< class H2, class P2 >  void merge( std::unordered_map<Key, T, H2, P2, Allocator>& source ); | (1) | (since C++17) |
| template< class H2, class P2 >  void merge( std::unordered_map<Key, T, H2, P2, Allocator>&& source ); | (2) | (since C++17) |
| template< class H2, class P2 >  void merge( std::unordered_multimap<Key, T, H2, P2, Allocator>& source ); | (3) | (since C++17) |
| template< class H2, class P2 >  void merge( std::unordered_multimap<Key, T, H2, P2, Allocator>&& source ); | (4) | (since C++17) |
|  |  |  |

Attempts to extract ("splice") each element in source and insert it into \*this using the hash function and key equality predicate of \*this.
If there is an element in \*this with key equivalent to the key of an element from source, then that element is not extracted from source.
No elements are copied or moved, only the internal pointers of the container nodes are repointed. All pointers and references to the transferred elements remain valid, but now refer into \*this, not into source. Iterators referring to the transferred elements and all iterators referring to \*this are invalidated. Iterators to elements remaining in source remain valid.

The behavior is undefined if get_allocator() != source.get_allocator().

### Parameters

|  |  |  |
| --- | --- | --- |
| source | - | compatible container to transfer the nodes from |

### Return value

(none)

### Complexity

Average case O(N), worst case O(N \* size() + N), where N is source.size().

### Example

Run this code

```
#include <iostream>
#include <string>
#include <unordered_map>
#include <utility>
 
// print out a std::pair
template<class Os, class U, class V>
Os& operator<<(Os& os, const std::pair<U,V>& p)
{
    return os << '{' << p.first << ", " << p.second << '}';
}
 
// print out an associative container
template<class Os, class K, class V>
Os& operator<<(Os& os, const std::unordered_map<K, V>& v)
{
    os << '[' << v.size() << "] {";
    bool o{};
    for (const auto& e : v)
        os << (o ? ", " : (o = 1, "")) << e;
    return os << "}\n";
}
 
int main()
{
    std::unordered_map<std::string, int>
        p{{"C", 3}, {"B", 2}, {"A", 1}, {"A", 0}},
        q{{"E", 6}, {"E", 7}, {"D", 5}, {"A", 4}};
 
    std::cout << "p: " << p << "q: " << q;
 
    p.merge(q);
 
    std::cout << "p.merge(q);\n" << "p: " << p << "q: " << q;
}

```

Possible output:

```
p: [3] {{A, 1}, {B, 2}, {C, 3}}
q: [3] {{A, 4}, {D, 5}, {E, 6}}
p.merge(q);
p: [5] {{E, 6}, {D, 5}, {A, 1}, {B, 2}, {C, 3}}
q: [1] {{A, 4}}

```

### See also

|  |  |
| --- | --- |
| extract(C++17) | extracts nodes from the container   (public member function) |
| insert | inserts elements or nodes(since C++17)   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_map/merge&oldid=135905>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 November 2021, at 13:13.