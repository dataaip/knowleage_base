# std::unordered_map<Key,T,Hash,KeyEqual,Allocator>::insert

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_map::unordered_map | | | | | | unordered_map::~unordered_map | | | | | | unordered_map::operator= | | | | | | unordered_map::get_allocator | | | | | | Iterators | | | | | | unordered_map::beginunordered_map::cbegin | | | | | | unordered_map::endunordered_map::cend | | | | | | Capacity | | | | | | unordered_map::size | | | | | | unordered_map::max_size | | | | | | unordered_map::empty | | | | | | Modifiers | | | | | | unordered_map::clear | | | | | | unordered_map::erase | | | | | | unordered_map::swap | | | | | | unordered_map::extract(C++17) | | | | | | unordered_map::merge(C++17) | | | | | | ****unordered_map::insert**** | | | | | | unordered_map::insert_range(C++23) | | | | | | unordered_map::insert_or_assign(C++17) | | | | | | unordered_map::emplace | | | | | | unordered_map::emplace_hint | | | | | | unordered_map::try_emplace(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_map::at | | | | | | [unordered_map::operator[]](operator_at.html "cpp/container/unordered map/operator at") | | | | | | unordered_map::count | | | | | | unordered_map::find | | | | | | unordered_map::contains(C++20) | | | | | | unordered_map::equal_range | | | | | | Bucket interface | | | | | | unordered_map::begin(size_type)unordered_map::cbegin(size_type) | | | | | | unordered_map::end(size_type)unordered_map::cend(size_type) | | | | | | unordered_map::bucket_count | | | | | | unordered_map::max_bucket_count | | | | | | unordered_map::bucket_size | | | | | | unordered_map::bucket | | | | | | Hash policy | | | | | | unordered_map::load_factor | | | | | | unordered_map::max_load_factor | | | | | | unordered_map::rehash | | | | | | unordered_map::reserve | | | | | | Observers | | | | | | unordered_map::hash_function | | | | | | unordered_map::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_map) | | | | | | erase_if(std::unordered_map)(C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| std::pair<iterator, bool> insert( const value_type& value ); | (1) | (since C++11) |
| std::pair<iterator, bool> insert( value_type&& value ); | (2) | (since C++17) |
| template< class P >  std::pair<iterator, bool> insert( P&& value ); | (3) | (since C++11) |
| iterator insert( const_iterator hint, const value_type& value ); | (4) | (since C++11) |
| iterator insert( const_iterator hint, value_type&& value ); | (5) | (since C++17) |
| template< class P >  iterator insert( const_iterator hint, P&& value ); | (6) | (since C++11) |
| template< class InputIt >  void insert( InputIt first, InputIt last ); | (7) | (since C++11) |
| void insert( std::initializer_list<value_type> ilist ); | (8) | (since C++11) |
| insert_return_type insert( node_type&& nh ); | (9) | (since C++17) |
| iterator insert( const_iterator hint, node_type&& nh ); | (10) | (since C++17) |
|  |  |  |

Inserts element(s) into the container, if the container doesn't already contain an element with an equivalent key.

1-3) Inserts value. Overload (3) is equivalent to emplace(std::forward<P>(value)) and only participates in overload resolution if std::is_constructible<value_type, P&&>::value == true.4-6) Inserts value, using hint as a non-binding suggestion to where the search should start. Overload (6) is equivalent to emplace_hint(hint, std::forward<P>(value)) and only participates in overload resolution if std::is_constructible<value_type, P&&>::value == true.7) Inserts elements from range ``first`,`last`)`. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending [LWG2844). If ``first`,`last`)` is not a [valid range, or first and/or last are iterators into \*this, the behavior is undefined.8) Inserts elements from initializer list ilist. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).9) If nh is an empty node handle, does nothing. Otherwise, inserts the element owned by nh into the container , if the container doesn't already contain an element with a key equivalent to nh.key(). The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().10) If nh is an empty node handle, does nothing and returns the end iterator. Otherwise, inserts the element owned by nh into the container, if the container doesn't already contain an element with a key equivalent to nh.key(), and returns the iterator pointing to the element with key equivalent to nh.key()(regardless of whether the insert succeeded or failed). If the insertion succeeds, nh is moved from, otherwise it retains ownership of the element. hint is used as a non-binding suggestion to where the search should start. The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().

If after the operation the new number of elements is greater than old `max_load_factor()` `*``bucket_count()` a rehashing takes place.  
If rehashing occurs (due to the insertion), all iterators are invalidated. Otherwise (no rehashing), iterators are not invalidated. If the insertion is successful, pointers and references to the element obtained while it is held in the node handle are invalidated, and pointers and references obtained to that element before it was extracted become valid.(since C++17)

### Parameters

|  |  |  |
| --- | --- | --- |
| hint | - | iterator, used as a suggestion as to where to insert the content |
| value | - | element value to insert |
| first, last | - | range of elements to insert |
| ilist | - | initializer list to insert the values from |
| nh | - | a compatible node handle |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Return value

1-3) A pair consisting of an iterator to the inserted element (or to the element that prevented the insertion) and a bool value set to true if and only if the insertion took place.4-6) An iterator to the inserted element, or to the element that prevented the insertion.7,8) (none)9) An object of `insert_return_type` with the members initialized as follows:

- If nh is empty, `inserted` is false, `position` is end(), and `node` is empty.
- Otherwise if the insertion took place, `inserted` is true, `position` points to the inserted element, and `node` is empty.
- If the insertion failed, `inserted` is false, `node` has the previous value of nh, and `position` points to an element with a key equivalent to nh.key().
10) End iterator if nh was empty, iterator pointing to the inserted element if insertion took place, and iterator pointing to an element with a key equivalent to nh.key() if it failed.

### Exceptions

1-6) If an exception is thrown for any reason, these functions have no effect (strong exception safety guarantee).7,8) No exception safety guarantee.9,10) If an exception is thrown for any reason, these functions have no effect (strong exception safety guarantee).

### Complexity

1-6) Average case: `O(1)`, worst case `O(size())`.7,8) Average case: `O(N)`, where N is the number of elements to insert. Worst case: `O(N * size() + N)`.9,10) Average case: `O(1)`, worst case `O(size())`.

### Notes

The hinted insert (4-6) does not return a boolean in order to be signature-compatible with positional insert on sequential containers, such as std::vector::insert. This makes it possible to create generic inserters such as std::inserter. One way to check success of a hinted insert is to compare `size()` before and after.

### Example

Run this code

```
#include <iostream>
#include <string>
#include <unordered_map>
 
int main ()
{
    std::unordered_map<int, std::string> dict = {{1, "one"}, {2, "two"}};
    dict.insert({3, "three"});
    dict.insert(std::make_pair(4, "four"));
    dict.insert({{4, "another four"}, {5, "five"}});
 
    const bool ok = dict.insert({1, "another one"}).second;
    std::cout << "inserting 1 => \"another one\" "
              << (ok ? "succeeded" : "failed") << '\n';
 
    std::cout << "contents:\n";
    for (auto& p : dict)
        std::cout << ' ' << p.first << " => " << p.second << '\n';
}

```

Possible output:

```
inserting 1 => "another one" failed
contents:
 5 => five
 1 => one
 2 => two
 3 => three
 4 => four

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2005 | C++11 | overloads (3,6) would only participate in overload resolution if `P` is implicitly convertible to `value_type` | only participates if `value_type` is constructible from `P&&` |

### See also

|  |  |
| --- | --- |
| emplace | constructs element in-place   (public member function) |
| emplace_hint | constructs elements in-place using a hint   (public member function) |
| insert_or_assign(C++17) | inserts an element or assigns to the current element if the key already exists   (public member function) |
| inserter | creates a std::insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_map/insert&oldid=170190>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 March 2024, at 10:38.