# std::unordered_multimap<Key,T,Hash,KeyEqual,Allocator>::insert

From cppreference.com
< cpp‎ | container‎ | unordered multimap
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

`std::unordered_multimap`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_multimap::unordered_multimap | | | | | | unordered_multimap::~unordered_multimap | | | | | | unordered_multimap::operator= | | | | | | unordered_multimap::get_allocator | | | | | | Iterators | | | | | | unordered_multimap::beginunordered_multimap::cbegin | | | | | | unordered_multimap::endunordered_multimap::cend | | | | | | Capacity | | | | | | unordered_multimap::size | | | | | | unordered_multimap::max_size | | | | | | unordered_multimap::empty | | | | | | Modifiers | | | | | | unordered_multimap::clear | | | | | | ****unordered_multimap::insert**** | | | | | | unordered_multimap::insert_range(C++23) | | | | | | unordered_multimap::emplace | | | | | | unordered_multimap::emplace_hint | | | | | | unordered_multimap::erase | | | | | | unordered_multimap::swap | | | | | | unordered_multimap::extract(C++17) | | | | | | unordered_multimap::merge(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_multimap::count | | | | | | unordered_multimap::find | | | | | | unordered_multimap::contains(C++20) | | | | | | unordered_multimap::equal_range | | | | | | Bucket interface | | | | | | unordered_multimap::begin(size_type)unordered_multimap::cbegin(size_type) | | | | | | unordered_multimap::end(size_type)unordered_multimap::cend(size_type) | | | | | | unordered_multimap::bucket_count | | | | | | unordered_multimap::max_bucket_count | | | | | | unordered_multimap::bucket_size | | | | | | unordered_multimap::bucket | | | | | | Hash policy | | | | | | unordered_multimap::load_factor | | | | | | unordered_multimap::max_load_factor | | | | | | unordered_multimap::rehash | | | | | | unordered_multimap::reserve | | | | | | Observers | | | | | | unordered_multimap::hash_function | | | | | | unordered_multimap::key_eq | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_multimap) | | | | | | erase_if(std::unordered_multimap)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<unordered_map>` |  |  |
| iterator insert( const value_type& value ); | (1) | (since C++11) |
| iterator insert( value_type&& value ); | (2) | (since C++17) |
| template< class P >  iterator insert( P&& value ); | (3) | (since C++11) |
| iterator insert( const_iterator hint, const value_type& value ); | (4) | (since C++11) |
| iterator insert( const_iterator hint, value_type&& value ); | (5) | (since C++17) |
| template< class P >  iterator insert( const_iterator hint, P&& value ); | (6) | (since C++11) |
| template< class InputIt >  void insert( InputIt first, InputIt last ); | (7) | (since C++11) |
| void insert( std::initializer_list<value_type> ilist ); | (8) | (since C++11) |
| iterator insert( node_type&& nh ); | (9) | (since C++17) |
| iterator insert( const_iterator hint, node_type&& nh ); | (10) | (since C++17) |
|  |  |  |

Inserts element(s) into the container.

1-3) Inserts value. Overload (3) is equivalent to emplace(std::forward<P>(value)) and only participates in overload resolution if std::is_constructible<value_type, P&&>::value == true.4-6) Inserts value, using hint as a non-binding suggestion to where the search should start. Overload (6) is equivalent to emplace_hint(hint, std::forward<P>(value)) and only participates in overload resolution if std::is_constructible<value_type, P&&>::value == true.7) Inserts elements from range ``first`,`last`)`. If `[`first`,`last`)` is not a [valid range, or first and/or last are iterators into \*this, the behavior is undefined.8) Inserts elements from initializer list ilist.9) If nh is an empty node handle, does nothing. Otherwise, inserts the element owned by nh into the container and returns an iterator pointing at the inserted element. The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().10) If nh is an empty node handle, does nothing and returns the end iterator. Otherwise, inserts the element owned by nh into the container, and returns the iterator pointing to the element with key equivalent to nh.key(). hint is used as a non-binding suggestion to where the search should start. The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().

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

1-6) An iterator to the inserted element.7,8) (none)9,10) End iterator if nh was empty, iterator pointing to the inserted element otherwise.

### Exceptions

1-6) If an exception is thrown for any reason, these functions have no effect (strong exception safety guarantee).7,8) No exception safety guarantee.9,10) If an exception is thrown for any reason, these functions have no effect (strong exception safety guarantee).

### Complexity

1-6) Average case: `O(1)`, worst case `O(size())`.7,8) Average case: `O(N)`, where N is the number of elements to insert. Worst case: `O(N * size() + N)`.9,10) Average case: `O(1)`, worst case `O(size())`.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

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
| inserter | creates a std::insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_multimap/insert&oldid=168634>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 January 2024, at 13:36.