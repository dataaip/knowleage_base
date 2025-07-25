# std::unordered_set<Key,Hash,KeyEqual,Allocator>::insert

From cppreference.com
< cpp‎ | container‎ | unordered set
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

`std::unordered_set`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unordered_set::unordered_set | | | | | | unordered_set::~unordered_set | | | | | | unordered_set::operator= | | | | | | unordered_set::get_allocator | | | | | | Iterators | | | | | | unordered_set::beginunordered_set::cbegin | | | | | | unordered_set::endunordered_set::cend | | | | | | Capacity | | | | | | unordered_set::size | | | | | | unordered_set::max_size | | | | | | unordered_set::empty | | | | | | Modifiers | | | | | | unordered_set::clear | | | | | | unordered_set::erase | | | | | | unordered_set::swap | | | | | | unordered_set::extract(C++17) | | | | | | unordered_set::merge(C++17) | | | | | | ****unordered_set::insert**** | | | | | | unordered_set::insert_range(C++23) | | | | | | unordered_set::emplace | | | | | | unordered_set::emplace_hint | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lookup | | | | | | unordered_set::count | | | | | | unordered_set::find | | | | | | unordered_set::contains(C++20) | | | | | | unordered_set::equal_range | | | | | | Bucket interface | | | | | | unordered_set::begin(size_type)unordered_set::cbegin(size_type) | | | | | | unordered_set::end(size_type)unordered_set::cend(size_type) | | | | | | unordered_set::bucket_count | | | | | | unordered_set::max_bucket_count | | | | | | unordered_set::bucket_size | | | | | | unordered_set::bucket | | | | | | Hash policy | | | | | | unordered_set::load_factor | | | | | | unordered_set::max_load_factor | | | | | | unordered_set::rehash | | | | | | unordered_set::reserve | | | | | | Observers | | | | | | unordered_set::hash_function | | | | | | unordered_set::key_eq | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator!=(until C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | std::swap(std::unordered_set) | | | | | | erase_if(std::unordered_set)(C++20) | | | | | |
| Deduction guides (C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| std::pair<iterator,bool> insert( const value_type& value ); | (1) | (since C++11) |
| std::pair<iterator,bool> insert( value_type&& value ); | (2) | (since C++11) |
| iterator insert( const_iterator hint, const value_type& value ); | (3) | (since C++11) |
| iterator insert( const_iterator hint, value_type&& value ); | (4) | (since C++11) |
| template< class InputIt >  void insert( InputIt first, InputIt last ); | (5) | (since C++11) |
| void insert( std::initializer_list<value_type> ilist ); | (6) | (since C++11) |
| insert_return_type insert( node_type&& nh ); | (7) | (since C++17) |
| iterator insert( const_iterator hint, node_type&& nh ); | (8) | (since C++17) |
| template< class K >  std::pair<iterator, bool> insert( K&& obj ); | (9) | (since C++23) |
| template< class K >  iterator insert( const_iterator hint, K&& obj ); | (10) | (since C++23) |
|  |  |  |

Inserts element(s) into the container, if the container doesn't already contain an element with an equivalent key.

1,2) Inserts value.3,4) Inserts value, using hint as a non-binding suggestion to where the search should start.5) Inserts elements from range ``first`,`last`)`. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending [LWG2844).6) Inserts elements from initializer list ilist. If multiple elements in the range have keys that compare equivalent, it is unspecified which element is inserted (pending LWG2844).7) If nh is an empty node handle, does nothing. Otherwise, inserts the element owned by nh into the container , if the container doesn't already contain an element with a key equivalent to nh.key(). The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().8) If nh is an empty node handle, does nothing and returns the end iterator. Otherwise, inserts the element owned by nh into the container, if the container doesn't already contain an element with a key equivalent to nh.key(), and returns the iterator pointing to the element with key equivalent to nh.key()(regardless of whether the insert succeeded or failed). If the insertion succeeds, nh is moved from, otherwise it retains ownership of the element. hint is used as a non-binding suggestion to where the search should start. The behavior is undefined if nh is not empty and get_allocator() != nh.get_allocator().9) If \*this already contains an element which transparently compares **equivalent** to obj, does nothing. Otherwise, constructs an object `u` of `value_type` with std::forward<K>(obj) and then inserts `u` into \*this. If equal_range(u) != hash_function()(obj) || contains(u) is true, the behavior is undefined. The `value_type` must be EmplaceConstructible into `unordered_set` from std::forward<K>(obj). This overload participates in overload resolution only if Hash::is_transparent and KeyEqual::is_transparent are valid and each denotes a type. This assumes that such `Hash` is callable with both `K` and `Key` type, and that the `KeyEqual` is transparent, which, together, allows calling this function without constructing an instance of `Key`.10) If \*this already contains an element which transparently compares **equivalent** to obj, does nothing.

Otherwise, constructs an object `u` of `value_type` with std::forward<K>(obj) and then inserts `u` into \*this. Template:hint") is used as a non-binding suggestion to where the search should start. If equal_range(u) != hash_function()(obj) || contains(u) is true, the behavior is undefined.
The `value_type` must be EmplaceConstructible into `unordered_set` from std::forward<K>(obj). This overload participates in overload resolution only if:

- std::is_convertible_v<K&&, const_iterator> and std::is_convertible_v<K&&, iterator> are both false, and
- Hash::is_transparent and KeyEqual::is_transparent are valid and each denotes a type. This assumes that such `Hash` is callable with both `K` and `Key` type, and that the `KeyEqual` is transparent,

which, together, allows calling this function without constructing an instance of `Key`.

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
| obj | - | a value of any type that can be transparently compared with a key |
| Type requirements | | |
| -`InputIt` must meet the requirements of LegacyInputIterator. | | |

### Return value

1,2) A pair consisting of an iterator to the inserted element (or to the element that prevented the insertion) and a bool value set to true if and only if the insertion took place.3,4) An iterator to the inserted element, or to the element that prevented the insertion.5,6) (none)7) An object of `insert_return_type` with the members initialized as follows:

- If nh is empty, `inserted` is false, `position` is end(), and `node` is empty.
- Otherwise if the insertion took place, `inserted` is true, `position` points to the inserted element, and `node` is empty.
- If the insertion failed, `inserted` is false, `node` has the previous value of nh, and `position` points to an element with a key equivalent to nh.key().
8) End iterator if nh was empty, iterator pointing to the inserted element if insertion took place, and iterator pointing to an element with a key equivalent to nh.key() if it failed.9) A pair consisting of an iterator to the inserted element (or to the element that prevented the insertion) and a bool value set to true if and only if the insertion took place.10) An iterator to the inserted element, or to the element that prevented the insertion.

### Exceptions

1-4) If an exception is thrown by any operation, the insertion has no effect.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: cases 5-10 |

### Complexity

1-4) Average case: `O(1)`, worst case `O(size())`.5,6) Average case: `O(N)`, where N is the number of elements to insert. Worst case: `O(N * size() + N)`.7-10) Average case: `O(1)`, worst case `O(size())`.

### Notes

The hinted insert (3,4) does not return a boolean in order to be signature-compatible with positional insert on sequential containers, such as std::vector::insert. This makes it possible to create generic inserters such as std::inserter. One way to check success of a hinted insert is to compare `size()` before and after.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_associative_heterogeneous_insertion` | `202311L` | (C++26) | Heterogeneous overloads for the remaining member functions in ordered and unordered associative containers. (9,10) |

### Example

Run this code

```
#include <array>
#include <iostream>
#include <unordered_set>
 
std::ostream& operator<<(std::ostream& os, std::unordered_set<int> const& s)
{
    for (os << '[' << s.size() << "] { "; int i : s)
        os << i << ' ';
    return os << "}\n";
}
 
int main ()
{
    std::unordered_set<int> nums{2, 3, 4};
 
    std::cout << "1) Initially: " << nums << std::boolalpha;
    auto p = nums.insert(1); // insert element, overload (1)
    std::cout << "2) '1' was inserted: " << p.second << '\n';
    std::cout << "3) After insertion: " << nums;
 
    nums.insert(p.first, 0); // insert with hint, overload (3)
    std::cout << "4) After insertion: " << nums;
 
    std::array<int, 4> a = {10, 11, 12, 13};
    nums.insert(a.begin(), a.end()); // insert range, overload (5)
    std::cout << "5) After insertion: " << nums;
 
    nums.insert({20, 21, 22, 23}); // insert initializer_list, (6)
    std::cout << "6) After insertion: " << nums;
 
    std::unordered_set<int> other_nums = {42, 43};
    auto node = other_nums.extract(other_nums.find(42));
    nums.insert(std::move(node)); // insert node, overload (7)
    std::cout << "7) After insertion: " << nums;
 
    node = other_nums.extract(other_nums.find(43));
    nums.insert(nums.begin(), std::move(node)); // insert node with hint, (8)
    std::cout << "8) After insertion: " << nums;
}

```

Possible output:

```
1) Initially: [3] { 4 3 2 }
2) '1' was inserted: true
3) After insertion: [4] { 1 2 3 4 }
4) After insertion: [5] { 0 1 2 3 4 }
5) After insertion: [9] { 13 12 11 10 4 3 2 1 0 }
6) After insertion: [13] { 23 22 13 12 11 10 21 4 20 3 2 1 0 }
7) After insertion: [14] { 42 23 22 13 12 11 10 21 4 20 3 2 1 0 }
8) After insertion: [15] { 43 42 23 22 13 12 11 10 21 4 20 3 2 1 0 }

```

### See also

|  |  |
| --- | --- |
| emplace | constructs element in-place   (public member function) |
| emplace_hint | constructs elements in-place using a hint   (public member function) |
| inserter | creates a std::insert_iterator of type inferred from the argument   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/unordered_set/insert&oldid=170189>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 March 2024, at 10:36.