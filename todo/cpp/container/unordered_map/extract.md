# std::unordered_map<Key,T,Hash,KeyEqual,Allocator>::extract

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_map::unordered_map | | | | | | unordered_map::~unordered_map | | | | | | unordered_map::operator= | | | | | | unordered_map::get_allocator | | | | | | Iterators | | | | | | unordered_map::beginunordered_map::cbegin | | | | | | unordered_map::endunordered_map::cend | | | | | | Capacity | | | | | | unordered_map::size | | | | | | unordered_map::max_size | | | | | | unordered_map::empty | | | | | | Modifiers | | | | | | unordered_map::clear | | | | | | unordered_map::erase | | | | | | unordered_map::swap | | | | | | ****unordered_map::extract****(C++17) | | | | | | unordered_map::merge(C++17) | | | | | | unordered_map::insert | | | | | | unordered_map::insert_range(C++23) | | | | | | unordered_map::insert_or_assign(C++17) | | | | | | unordered_map::emplace | | | | | | unordered_map::emplace_hint | | | | | | unordered_map::try_emplace(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_map::at | | | | | | [unordered_map::operator[]](operator_at.html "cpp/container/unordered map/operator at") | | | | | | unordered_map::count | | | | | | unordered_map::find | | | | | | unordered_map::contains(C++20) | | | | | | unordered_map::equal_range | | | | | | Bucket interface | | | | | | unordered_map::begin(size_type)unordered_map::cbegin(size_type) | | | | | | unordered_map::end(size_type)unordered_map::cend(size_type) | | | | | | unordered_map::bucket_count | | | | | | unordered_map::max_bucket_count | | | | | | unordered_map::bucket_size | | | | | | unordered_map::bucket | | | | | | Hash policy | | | | | | unordered_map::load_factor | | | | | | unordered_map::max_load_factor | | | | | | unordered_map::rehash | | | | | | unordered_map::reserve | | | | | | Observers | | | | | | unordered_map::hash_function | | | | | | unordered_map::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_map) | | | | | | erase_if(std::unordered_map)(C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| node_type extract( const_iterator position ); | (1) | (since C++17) |
| node_type extract( const Key& k ); | (2) | (since C++17) |
| template< class K >  node_type extract( K&& x ); | (3) | (since C++23) |
|  |  |  |

1) Unlinks the node that contains the element pointed to by position and returns a node handle that owns it.2) If the container has an element with key equivalent to k, unlinks the node that contains that element from the container and returns a node handle that owns it. Otherwise, returns an empty node handle.3) Same as (2). This overload participates in overload resolution only if Hash::is_transparent and KeyEqual::is_transparent are valid and each denotes a type, and neither `iterator` nor `const_iterator` is implicitly convertible from `K`. This assumes that such `Hash` is callable with both `K` and `Key` type, and that the `KeyEqual` is transparent, which, together, allows calling this function without constructing an instance of `Key`.

In either case, no elements are copied or moved, only the internal pointers of the container nodes are repointed .

Extracting a node invalidates only the iterators to the extracted element, and preserves the relative order of the elements that are not erased. Pointers and references to the extracted element remain valid, but cannot be used while element is owned by a node handle: they become usable if the element is inserted into a container.

### Parameters

|  |  |  |
| --- | --- | --- |
| position | - | a valid iterator into this container |
| k | - | a key to identify the node to be extracted |
| x | - | a value of any type that can be transparently compared with a key identifying the node to be extracted |

### Return value

A node handle that owns the extracted element, or empty node handle in case the element is not found in (2,3).

### Exceptions

1) Throws nothing.2,3) Any exceptions thrown by the `Hash` and `KeyEqual` object.

### Complexity

1,2,3) Average case O(1), worst case O(size()).

### Notes

extract is the only way to change a key of a map element without reallocation:

```
std::map<int, std::string> m{{1, "mango"}, {2, "papaya"}, {3, "guava"}};
auto nh = m.extract(2);
nh.key() = 4;
m.insert(std::move(nh));
// m == {{1, "mango"}, {3, "guava"}, {4, "papaya"}}

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_associative_heterogeneous_erasure` | `202110L` | (C++23) | Heterogeneous erasure in associative containers and unordered associative containers, (3) |

### Example

Run this code

```
#include <algorithm>
#include <iostream>
#include <string_view>
#include <unordered_map>
 
void print(std::string_view comment, const auto& data)
{
    std::cout << comment;
    for (auto [k, v] : data)
        std::cout << ' ' << k << '(' << v << ')';
 
    std::cout << '\n';
}
 
int main()
{
    std::unordered_map<int, char> cont{{1, 'a'}, {2, 'b'}, {3, 'c'}};
 
    print("Start:", cont);
 
    // Extract node handle and change key
    auto nh = cont.extract(1);
    nh.key() = 4;
 
    print("After extract and before insert:", cont);
 
    // Insert node handle back
    cont.insert(std::move(nh));
 
    print("End:", cont);
}

```

Possible output:

```
Start: 1(a) 2(b) 3(c)
After extract and before insert: 2(b) 3(c)
End: 2(b) 3(c) 4(a)

```

### See also

|  |  |
| --- | --- |
| merge(C++17) | splices nodes from another container   (public member function) |
| insert | inserts elements or nodes(since C++17)   (public member function) |
| erase | erases elements   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_map/extract&oldid=134477>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 October 2021, at 00:45.