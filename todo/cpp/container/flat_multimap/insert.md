# std::flat_multimap<Key,T,Compare,KeyContainer,MappedContainer>::insert

From cppreference.com
< cpp‎ | container‎ | flat multimap
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

std::flat_multimap

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | flat_multimap::flat_multimap | | | | | | flat_multimap::operator= | | | | | | Modifiers | | | | | | flat_multimap::clear | | | | | | flat_multimap::erase | | | | | | flat_multimap::swap | | | | | | flat_multimap::extract | | | | | | flat_multimap::replace | | | | | | ****flat_multimap::insert**** | | | | | | flat_multimap::insert_range | | | | | | flat_multimap::emplace | | | | | | flat_multimap::emplace_hint | | | | | | Lookup | | | | | | flat_multimap::count | | | | | | flat_multimap::find | | | | | | flat_multimap::contains | | | | | | flat_multimap::equal_range | | | | | | flat_multimap::lower_bound | | | | | | flat_multimap::upper_bound | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Iterators | | | | | | flat_multimap::beginflat_multimap::cbegin | | | | | | flat_multimap::endflat_multimap::cend | | | | | | flat_multimap::rbeginflat_multimap::crbegin | | | | | | flat_multimap::rendflat_multimap::crend | | | | | | Capacity | | | | | | flat_multimap::size | | | | | | flat_multimap::max_size | | | | | | flat_multimap::empty | | | | | | Observers | | | | | | flat_multimap::key_comp | | | | | | flat_multimap::keys | | | | | | flat_multimap::value_comp | | | | | | flat_multimap::values | | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap(std::flat_multimap) | | | | | | erase_if(std::flat_multimap) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=> | | | | | | |
| Helper classes | | | | |
| |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | uses_allocator<std::flat_multimap> | | | | | | |
| Tags | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | sorted_equivalent_t | | | | | | |
| Deduction guides | | | | |

|  |  |  |
| --- | --- | --- |
| iterator insert( const value_type& value ); | (1) | (since C++23) |
| iterator insert( value_type&& value ); | (2) | (since C++23) |
| iterator insert( const_iterator pos, const value_type& value ); | (3) | (since C++23) |
| iterator insert( const_iterator pos, value_type&& value ); | (4) | (since C++23) |
| template< class P >  iterator insert( P&& x ); | (5) | (since C++23) |
| template< class P >  iterator insert( const_iterator pos, P&& x ); | (6) | (since C++23) |
| template< class InputIt >  void insert( InputIt first, InputIt last ); | (7) | (since C++23) |
| template< class InputIt >  void insert( std::sorted_equivalent_t, InputIt first, InputIt last ); | (8) | (since C++23) |
| void insert( std::initializer_list<key_type> ilist ); | (9) | (since C++23) |
| void insert( std::sorted_equivalent_t s, std::initializer_list<key_type> ilist ); | (10) | (since C++23) |
|  |  |  |

Inserts element(s) into the container.

1) Inserts value. Equivalent to return emplace(value);.2) Inserts value. Equivalent to return emplace(std::move(value));.3) Inserts value in the position as close as possible to the position just prior to pos. Equivalent to return emplace_hint(pos, value);.4) Inserts value in the position as close as possible to the position just prior to pos. Equivalent to return emplace_hint(pos, std::move(value));.5) Inserts `x` into \*this as if by emplace(std::forward<P>(x));. This overload participates in overload resolution only if std::is_constructible_v<pair<key_type, mapped_type>, P> is true.6) Inserts `x` into \*this in the position as close as possible to the position just prior to pos. Equivalent to return emplace_hint(position, std::forward<P>(x));. This overload participates in overload resolution only if std::is_constructible_v<pair<key_type, mapped_type>, P> is true.7) Inserts elements from range ``first`,`last`)` as if performing the following operations sequentially:

1. Adds elements to [`c` as if by  
   for (; first != last; ++first)  
   {  
       value_type value = \*first;  
       c.keys.insert(c.keys.end(), std::move(value.first));  
       c.values.insert(c.values.end(), std::move(value.second));  
   }
2. Sorts the range of newly inserted elements with respect to `value_comp`.
3. Merges the resulting sorted range and the sorted range of pre-existing elements into a single sorted range.
 May allocate memory during the in-place merge operation.8) Inserts elements from range ``first`,`last`)` as if performing the following operations sequentially:

1. Adds elements to [`c` as if by  
   for (; first != last; ++first)  
   {  
       value_type value = \*first;  
       c.keys.insert(c.keys.end(), std::move(value.first));  
       c.values.insert(c.values.end(), std::move(value.second));  
   }
2. Merges the sorted range of newly added elements and the sorted range of pre-existing elements into a single sorted range.
 May allocate memory during the in-place merge operation.9) Inserts elements from initializer list ilist. Equivalent to insert(ilist.begin(), ilist.end());.10) Inserts elements from initializer list ilist. Equivalent to insert(s, ilist.begin(), ilist.end());.

|  |  |
| --- | --- |
|  | Information on iterator invalidation is copied from here |

### Parameters

|  |  |  |
| --- | --- | --- |
| pos | - | an iterator to the position before which the new element will be inserted |
| value | - | an element value to insert |
| first, last | - | a range of elements to insert |
| ilist | - | an initializer list to insert the values from |
| x | - | a value of any type that can be transparently compared with a key |
| s | - | a disambiguation tag indicating that the input sequence is sorted (with respect to `value_comp()`) |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Return value

1-6) An iterator to the inserted element.7-10) (none)

### Exceptions

1-6) If an exception is thrown by any operation, the insertion has no effect.7-10) No exception safety guarantee. (?)

|  |  |
| --- | --- |
|  | This section is incomplete Reason: double check cases 7-10 |

### Complexity

1-6) Linear in `size()`.7) N + M·log(M), where `N` is the `size()` before the operation and `M` is std::distance(first, last).8) Linear in `size()`.9) N + M·log(M), where `N` is the `size()` before the operation and `M` is ilist.size().10) Linear in `N`, where `N` is `size()` after the operation.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| emplace | constructs element in-place   (public member function) |
| emplace_hint | constructs elements in-place using a hint   (public member function) |
| inserter | creates a std::insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/flat_multimap/insert&oldid=170226>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 March 2024, at 16:17.