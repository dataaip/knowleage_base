# std::map<Key,T,Compare,Allocator>::operator[]

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
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Element access | | | | | | map::at | | | | | | ****map::operator[]**** | | | | | | Iterators | | | | | | map::beginmap::cbegin(C++11) | | | | | | map::endmap::cend(C++11) | | | | | | map::rbeginmap::crbegin(C++11) | | | | | | map::rendmap::crend(C++11) | | | | | | Capacity | | | | | | map::size | | | | | | map::max_size | | | | | | map::empty | | | | | | Observers | | | | | | map::key_comp | | | | | | map::value_comp | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | map::clear | | | | | | map::insert | | | | | | map::erase | | | | | | map::swap | | | | | | map::extract(C++17) | | | | | | map::merge(C++17) | | | | | | map::insert_range(C++23) | | | | | | map::insert_or_assign(C++17) | | | | | | map::emplace(C++11) | | | | | | map::emplace_hint(C++11) | | | | | | map::try_emplace(C++17) | | | | | | Lookup | | | | | | map::count | | | | | | map::find | | | | | | map::contains(C++20) | | | | | | map::equal_range | | | | | | map::lower_bound | | | | | | map::upper_bound | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | std::swap(std::map) | | | | | | erase_if(std::map)(C++20) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| T& operator[]( const Key& key ); | (1) |  |
| T& operator[]( Key&& key ); | (2) | (since C++11) |
| template< class K >  T& operator[]( K&& x ); | (3) | (since C++26) |
|  |  |  |

Returns a reference to the value that is mapped to a key equivalent to key or x respectively, performing an insertion if such key does not already exist.

|  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1) Inserts value_type(key, T()) if the key does not exist.  |  |  |  | | --- | --- | --- | | -`key_type` must meet the requirements of CopyConstructible. | | | | -`mapped_type` must meet the requirements of CopyConstructible and DefaultConstructible. | | |  If an insertion is performed, the mapped value is value-initialized (default-constructed for class types, zero-initialized otherwise) and a reference to it is returned. | (until C++11) |
| 1) Inserts a `value_type` object constructed in-place from std::piecewise_construct, std::forward_as_tuple(key), std::tuple<>() if the key does not exist. Equivalent to return this->try_emplace(key).first->second;.(since C++17)When the default allocator is used, this results in the key being copy constructed from `key` and the mapped value being value-initialized.  |  |  |  | | --- | --- | --- | | -`value_type` must be EmplaceConstructible from std::piecewise_construct, std::forward_as_tuple(key), std::tuple<>(). When the default allocator is used, this means that `key_type` must be CopyConstructible and `mapped_type` must be DefaultConstructible. | | |  2) Inserts a `value_type` object constructed in-place from std::piecewise_construct, std::forward_as_tuple(std::move(key)), std::tuple<>() if the key does not exist. Equivalent to return this->try_emplace(std::move(key)).first->second;.(since C++17) When the default allocator is used, this results in the key being move constructed from `key` and the mapped value being value-initialized.  |  |  |  | | --- | --- | --- | | -`value_type` must be EmplaceConstructible from std::piecewise_construct, std::forward_as_tuple(std::move(key)), std::tuple<>(). When the default allocator is used, this means that `key_type` must be MoveConstructible and `mapped_type` must be DefaultConstructible. | | | | (since C++11) |

3) Inserts a `value_type` object constructed in-place if there is no key that transparently compares **equivalent** to the value x. Equivalent to return this->try_emplace(std::forward<K>(x)).first->second;.
This overload participates in overload resolution only if the qualified-id Compare::is_transparent is valid and denotes a type. It allows calling this function without constructing an instance of `Key`.

No iterators or references are invalidated.

### Parameters

|  |  |  |
| --- | --- | --- |
| key | - | the key of the element to find |
| x | - | a value of any type that can be transparently compared with a key |

### Return value

1,2) A reference to the mapped value of the new element if no element with key key existed. Otherwise, a reference to the mapped value of the existing element whose key is equivalent to key.3) A reference to the mapped value of the new element if no element with key that compares equivalent to the value x existed. Otherwise, a reference to the mapped value of the existing element whose key compares equivalent to x.

### Exceptions

If an exception is thrown by any operation, the insertion has no effect.

### Complexity

Logarithmic in the size of the container.

### Notes

In the published C++11 and C++14 standards, this function was specified to require `mapped_type` to be DefaultInsertable and `key_type` to be CopyInsertable or MoveInsertable into \*this. This specification was defective and was fixed by LWG issue 2469, and the description above incorporates the resolution of that issue.

However, one implementation (libc++) is known to construct the `key_type` and `mapped_type` objects via two separate allocator `construct()` calls, as arguably required by the standards as published, rather than emplacing a `value_type` object.

operator[] is non-const because it inserts the key if it doesn't exist. If this behavior is undesirable or if the container is const, `at` may be used.

|  |  |
| --- | --- |
| `insert_or_assign` returns more information than operator[] and does not require default-constructibility of the mapped type. | (since C++17) |

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_associative_heterogeneous_insertion` | `202311L` | (C++26) | Heterogeneous overloads for the remaining member functions in ordered and unordered associative containers. (3) |

### Example

Run this code

```
#include <iostream>
#include <string>
#include <map>
 
void println(auto const comment, auto const& map)
{
    std::cout << comment << '{';
    for (const auto& pair : map)
        std::cout << '{' << pair.first << ": " << pair.second << '}';
    std::cout << "}\n";
}
 
int main()
{
    std::map<char, int> letter_counts{{'a', 27}, {'b', 3}, {'c', 1}};
 
    println("letter_counts initially contains: ", letter_counts);
 
    letter_counts['b'] = 42; // updates an existing value
    letter_counts['x'] = 9;  // inserts a new value
 
    println("after modifications it contains: ", letter_counts);
 
    // count the number of occurrences of each word
    // (the first call to operator[] initialized the counter with zero)
    std::map<std::string, int>  word_map;
    for (const auto& w : {"this", "sentence", "is", "not", "a", "sentence",
                          "this", "sentence", "is", "a", "hoax"})
        ++word_map[w];
    word_map["that"]; // just inserts the pair {"that", 0}
 
    for (const auto& [word, count] : word_map)
        std::cout << count << " occurrence(s) of word '" << word << "'\n";
}

```

Output:

```
letter_counts initially contains: {{a: 27}{b: 3}{c: 1}}
after modifications it contains: {{a: 27}{b: 42}{c: 1}{x: 9}}
2 occurrence(s) of word 'a'
1 occurrence(s) of word 'hoax'
2 occurrence(s) of word 'is'
1 occurrence(s) of word 'not'
3 occurrence(s) of word 'sentence'
0 occurrence(s) of word 'that'
2 occurrence(s) of word 'this'

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 334 | C++98 | the effect of overload (1) was simply returning (\*((insert(std::make_pair(x, T()))).first)).second | provided its own description instead |

### See also

|  |  |
| --- | --- |
| at | access specified element with bounds checking   (public member function) |
| insert_or_assign(C++17) | inserts an element or assigns to the current element if the key already exists   (public member function) |
| try_emplace(C++17) | inserts in-place if the key does not exist, does nothing if the key exists   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/map/operator_at&oldid=135923>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 November 2021, at 18:46.