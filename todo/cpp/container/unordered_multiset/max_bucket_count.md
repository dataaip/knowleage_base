# std::unordered_multiset<Key,Hash,KeyEqual,Allocator>::max_bucket_count

From cppreference.com
< cpp‎ | container‎ | unordered multiset
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

`std::unordered_multiset`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_multiset::unordered_multiset | | | | | | unordered_multiset::~unordered_multiset | | | | | | unordered_multiset::operator= | | | | | | unordered_multiset::get_allocator | | | | | | Iterators | | | | | | unordered_multiset::beginunordered_multiset::cbegin | | | | | | unordered_multiset::endunordered_multiset::cend | | | | | | Capacity | | | | | | unordered_multiset::size | | | | | | unordered_multiset::max_size | | | | | | unordered_multiset::empty | | | | | | Modifiers | | | | | | unordered_multiset::clear | | | | | | unordered_multiset::insert | | | | | | unordered_multiset::insert_range(C++23) | | | | | | unordered_multiset::emplace | | | | | | unordered_multiset::emplace_hint | | | | | | unordered_multiset::erase | | | | | | unordered_multiset::swap | | | | | | unordered_multiset::extract(C++17) | | | | | | unordered_multiset::merge(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_multiset::count | | | | | | unordered_multiset::find | | | | | | unordered_multiset::contains(C++20) | | | | | | unordered_multiset::equal_range | | | | | | Bucket interface | | | | | | unordered_multiset::begin(size_type)unordered_multiset::cbegin(size_type) | | | | | | unordered_multiset::end(size_type)unordered_multiset::cend(size_type) | | | | | | unordered_multiset::bucket_count | | | | | | ****unordered_multiset::max_bucket_count**** | | | | | | unordered_multiset::bucket_size | | | | | | unordered_multiset::bucket | | | | | | Hash policy | | | | | | unordered_multiset::load_factor | | | | | | unordered_multiset::max_load_factor | | | | | | unordered_multiset::rehash | | | | | | unordered_multiset::reserve | | | | | | Observers | | | | | | unordered_multiset::hash_function | | | | | | unordered_multiset::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_multiset) | | | | | | erase_if(std::unordered_multiset)(C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| size_type max_bucket_count() const; |  | (since C++11) |
|  |  |  |

Returns the maximum number of buckets the container is able to hold due to system or library implementation limitations.

### Parameters

(none)

### Return value

Maximum number of buckets.

### Complexity

Constant.

### Example

Run this code

```
#include <iostream>
#include <unordered_set>
 
int main()
{
    struct Ha { std::size_t operator()(long x) const { return std::hash<long>{}(x); }; };
 
    auto c1 = std::unordered_multiset<char>{};
    auto c2 = std::unordered_multiset<long>{};
    auto c3 = std::unordered_multiset<long, std::hash<int>>{};
    auto c4 = std::unordered_multiset<long, Ha>{};
 
    std::cout
        << "Max bucket count of\n" << std::hex << std::showbase
        << "c1: " << c1.max_bucket_count() << '\n'
        << "c2: " << c2.max_bucket_count() << '\n'
        << "c3: " << c3.max_bucket_count() << '\n'
        << "c4: " << c4.max_bucket_count() << '\n'
        ;
}

```

Possible output:

```
Max bucket count of
c1: 0xfffffffffffffff
c2: 0xfffffffffffffff
c3: 0xfffffffffffffff
c4: 0xaaaaaaaaaaaaaaa

```

### See also

|  |  |
| --- | --- |
| bucket_count | returns the number of buckets   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_multiset/max_bucket_count&oldid=136013>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 December 2021, at 07:38.