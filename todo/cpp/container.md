# Containers library

From cppreference.com
< cpp
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
| ****Containers library**** | | | | |
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

****Containers library****

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

The Containers library is a generic collection of class templates and algorithms that allow programmers to easily implement common data structures like queues, lists and stacks. There are two(until C++11)three(since C++11) classes of containers:

- sequence containers,
- associative containers,

|  |  |
| --- | --- |
| - unordered associative containers, | (since C++11) |

each of which is designed to support a different set of operations.

The container manages the storage space that is allocated for its elements and provides member functions to access them, either directly or through iterators (objects with properties similar to pointers).

Most containers have at least several member functions in common, and share functionalities. Which container is the best for the particular application depends not only on the offered functionality, but also on its efficiency for different workloads.

### Sequence containers

Sequence containers implement data structures which can be accessed sequentially.

|  |  |
| --- | --- |
| array(C++11) | fixed-sized inplace contiguous array   (class template) |
| vector | dynamic contiguous array   (class template) |
| inplace_vector(C++26) | dynamically-resizable, fixed capacity, inplace contiguous array   (class template) |
| deque | double-ended queue   (class template) |
| forward_list(C++11) | singly-linked list   (class template) |
| list | doubly-linked list   (class template) |

### Associative containers

Associative containers implement sorted data structures that can be quickly searched (O(log n) complexity).

|  |  |
| --- | --- |
| set | collection of unique keys, sorted by keys   (class template) |
| map | collection of key-value pairs, sorted by keys, keys are unique   (class template) |
| multiset | collection of keys, sorted by keys   (class template) |
| multimap | collection of key-value pairs, sorted by keys   (class template) |

### Unordered associative containers (since C++11)

Unordered associative containers implement unsorted (hashed) data structures that can be quickly searched (O(1) average, O(n) worst-case complexity).

|  |  |
| --- | --- |
| unordered_set(C++11) | collection of unique keys, hashed by keys   (class template) |
| unordered_map(C++11) | collection of key-value pairs, hashed by keys, keys are unique   (class template) |
| unordered_multiset(C++11) | collection of keys, hashed by keys   (class template) |
| unordered_multimap(C++11) | collection of key-value pairs, hashed by keys   (class template) |

### Container adaptors

Container adaptors provide a different interface for sequential containers.

|  |  |
| --- | --- |
| stack | adapts a container to provide stack (LIFO data structure)   (class template) |
| queue | adapts a container to provide queue (FIFO data structure)   (class template) |
| priority_queue | adapts a container to provide priority queue   (class template) |
| flat_set(C++23) | adapts a container to provide a collection of unique keys, sorted by keys   (class template) |
| flat_map(C++23) | adapts two containers to provide a collection of key-value pairs, sorted by unique keys   (class template) |
| flat_multiset(C++23) | adapts a container to provide a collection of keys, sorted by keys   (class template) |
| flat_multimap(C++23) | adapts two containers to provide a collection of key-value pairs, sorted by keys   (class template) |

### Views (since C++20)

Views provide flexible facilities for interacting with one- or multi-dimensional views over a non-owning array of elements.

|  |  |
| --- | --- |
| span(C++20) | a non-owning view over a contiguous sequence of objects   (class template) |
| mdspan(C++23) | a multi-dimensional non-owning array view   (class template) |

### Iterator invalidation

Read-only methods never invalidate iterators or references. Methods which modify the contents of a container may invalidate iterators and/or references, as summarized in this table.

|  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- |
| Category | Container | After ****insertion****, are... | | After ****erasure****, are... | | Conditionally |
| ****iterators**** valid? | ****references**** valid? | ****iterators**** valid? | ****references**** valid? |
| Sequence containers | array | N/A | | N/A | |  |
| vector | No | | N/A | | Insertion changed capacity |
| Yes | | Yes | | Before modified element(s) (for insertion only if capacity didn't change) |
| No | | No | | At or after modified element(s) |
| deque | No | Yes | Yes, except erased element(s) | | Modified first or last element |
| No | No | | Modified middle only |
| list | Yes | | Yes, except erased element(s) | |  |
| forward_list | Yes | | Yes, except erased element(s) | |  |
| Associative containers | set multiset map multimap | Yes | | Yes, except erased element(s) | |  |
| Unordered associative containers | unordered_set unordered_multiset unordered_map unordered_multimap | No | Yes | N/A | | Insertion caused rehash |
| Yes | Yes, except erased element(s) | | No rehash |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: add iterator invalidation for C++23 "flat" adaptors (std::flat_set etc) |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: add iterator invalidation for C++26 std::inplace_vector |

Here, ****insertion**** refers to any method which adds one or more elements to the container and ****erasure**** refers to any method which removes one or more elements from the container.

- Examples of insertion methods are std::set::insert, std::map::emplace, std::vector::push_back, and std::deque::push_front.

|  |  |
| --- | --- |
| - Note that [std::unordered_map::operator[]](container/unordered_map/operator_at.html "cpp/container/unordered map/operator at") also counts, as it may insert an element into the map. | (since C++11) |

- Examples of erasure methods are std::set::erase, std::vector::pop_back, std::deque::pop_front, and std::map::clear.
  - `clear` invalidates all iterators and references. Because it erases all elements, this technically complies with the rules above.

Unless otherwise specified (either explicitly or by defining a function in terms of other functions), passing a container as an argument to a library function never invalidate iterators to, or change the values of, objects within that container.

The past-the-end iterator deserves particular mention. In general this iterator is invalidated as though it were a normal iterator to a non-erased element. So std::set::end is never invalidated, std::unordered_set::end is invalidated only on rehash(since C++11), std::vector::end is always invalidated (since it is always after the modified elements), and so on.

There is one exception: an erasure which deletes the last element of a std::deque **does** invalidate the past-the-end iterator, even though it is not an erased element of the container (or an element at all). Combined with the general rules for std::deque iterators, the net result is that the only modifying operation which does **not** invalidate std::deque::end is an erasure which deletes the first element, but not the last.

|  |  |
| --- | --- |
| Thread safety  1. All container functions can be called concurrently by different threads on different containers. More generally, the C++ standard library functions do not read objects accessible by other threads unless those objects are directly or indirectly accessible via the function arguments, including the this pointer. 2. All const member functions can be called concurrently by different threads on the same container. In addition, the member functions `begin()`, `end()`, `rbegin()`, `rend()`, `front()`, `back()`, `data()`, `find()`, `lower_bound()`, `upper_bound()`, `equal_range()`, `at()`, and, except in associative containers, `operator[]`, behave as const for the purposes of thread safety (that is, they can also be called concurrently by different threads on the same container). More generally, the C++ standard library functions do not modify objects unless those objects are accessible, directly or indirectly, via the function's non-const arguments, including the this pointer. 3. Different elements in the same container can be modified concurrently by different threads, except for the elements of std::vector<bool> (for example, a vector of std::future objects can be receiving values from multiple threads). 4. Iterator operations (e.g. incrementing an iterator) read, but do not modify the underlying container, and may be executed concurrently with operations on other iterators on the same container, with the const member functions, or reads from the elements. Container operations that invalidate any iterators modify the container and cannot be executed concurrently with any operations on existing iterators even if those iterators are not invalidated. 5. Elements of the same container can be modified concurrently with those member functions that are not specified to access these elements. More generally, the C++ standard library functions do not read objects indirectly accessible through their arguments (including other elements of a container) except when required by its specification. 6. In any case, container operations (as well as algorithms, or any other C++ standard library functions) may be parallelized internally as long as this does not change the user-visible results (e.g. std::transform may be parallelized, but not std::for_each which is specified to visit each element of a sequence in order). | (since C++11) |

### Function table

Note: std::basic_string is not treated as a container by the standard but behaves much like one due to its similarity. It is listed as 'Pseudo container' here for convenience.

|  |  |
| --- | --- |
|  | - functions present in C++03 |
|  | - functions present since C++11 |
|  | - functions present since C++17 |
|  | - functions present since C++20 |
|  | - functions present since C++23 |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: Add C++26 "color" and fill member/non-member function table for std::inplace_vector |

#### Member function table

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | Pseudo container | Sequence containers | | | | | Associative containers | | | | Unordered associative containers | | | | Container adaptors | | | | | | |  | |
| Header | | `<string>` | `<array>` | `<vector>` | `<deque>` | `<forward_list>` | `<list>` | `<set>` | | `<map>` | | `<unordered_set>` | | `<unordered_map>` | | `<stack>` | `<queue>` | | `<flat_set>` | | `<flat_map>` | | Header | |
| Container | | |  | | --- | | ****basic_string**** | | |  | | --- | | ****array**** | | |  | | --- | | ****vector**** | | |  | | --- | | ****deque**** | | |  | | --- | | ****forward_list**** | | |  | | --- | | ****list**** | | |  | | --- | | ****set**** | | |  | | --- | | ****multiset**** | | |  | | --- | | ****map**** | | |  | | --- | | ****multimap**** | | |  | | --- | | ****unordered_set**** | | |  | | --- | | ****unordered_multiset**** | | |  | | --- | | ****unordered_map**** | | |  | | --- | | ****unordered_multimap**** | | |  | | --- | | ****stack**** | | |  | | --- | | ****queue**** | | |  | | --- | | ****priority_queue**** | | |  | | --- | | ****flat_set**** | | |  | | --- | | ****flat_multiset**** | | |  | | --- | | ****flat_map**** | | |  | | --- | | ****flat_multimap**** | | Container | |
|  | |  | | --- | | (constructor) | | |  | | --- | | basic_string | | (implicit) | |  | | --- | | vector | | |  | | --- | | deque | | |  | | --- | | forward_list | | |  | | --- | | list | | |  | | --- | | set | | |  | | --- | | multiset | | |  | | --- | | map | | |  | | --- | | multimap | | |  | | --- | | unordered_set | | |  | | --- | | unordered_multiset | | |  | | --- | | unordered_map | | |  | | --- | | unordered_multimap | | |  | | --- | | stack | | |  | | --- | | queue | | |  | | --- | | priority_queue | | |  | | --- | | flat_set | | |  | | --- | | flat_multiset | | |  | | --- | | flat_map | | |  | | --- | | flat_multimap | | |  | | --- | | (constructor) | |  |
| |  | | --- | | (destructor) | | |  | | --- | | ~basic_string | | (implicit) | |  | | --- | | ~vector | | |  | | --- | | ~deque | | |  | | --- | | ~forward_list | | |  | | --- | | ~list | | |  | | --- | | ~set | | |  | | --- | | ~multiset | | |  | | --- | | ~map | | |  | | --- | | ~multimap | | |  | | --- | | ~unordered_set | | |  | | --- | | ~unordered_multiset | | |  | | --- | | ~unordered_map | | |  | | --- | | ~unordered_multimap | | |  | | --- | | ~stack | | |  | | --- | | ~queue | | |  | | --- | | ~priority_queue | | |  | | --- | | ~flat_set | | |  | | --- | | ~flat_multiset | | |  | | --- | | ~flat_map | | |  | | --- | | ~flat_multimap | | |  | | --- | | (destructor) | |
| |  | | --- | | operator= | | |  | | --- | | operator= | | (implicit) | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | | |  | | --- | | operator= | |
| |  | | --- | | assign | | |  | | --- | | assign | |  | |  | | --- | | assign | | |  | | --- | | assign | | |  | | --- | | assign | | |  | | --- | | assign | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | assign | |
| |  | | --- | | assign_range | | |  | | --- | | assign_range | |  | |  | | --- | | assign_range | | |  | | --- | | assign_range | | |  | | --- | | assign_range | | |  | | --- | | assign_range | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | assign_range | |
| Iterators | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | |  |  |  | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | |  | | --- | | begin | | cbegin | | Iterators |
| |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | |  |  |  | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | | |  | | --- | | end | | cend | |
| |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | |  | |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | |  |  |  |  |  |  |  | |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | | |  | | --- | | rbegin | | crbegin | |
| |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | |  | |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | |  |  |  |  |  |  |  | |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | | |  | | --- | | rend | | crend | |
| Element   access | |  | | --- | | at | | |  | | --- | | at | | |  | | --- | | at | | |  | | --- | | at | | |  | | --- | | at | |  |  |  |  | |  | | --- | | at | |  |  |  | |  | | --- | | at | |  |  |  |  |  |  | |  | | --- | | at | |  | |  | | --- | | at | | Element   access |
| |  | | --- | | operator[] | | [|  | | --- | | operator[] |](string/basic_string/operator_at.html "cpp/string/basic string/operator at") | [|  | | --- | | operator[] |](container/array/operator_at.html "cpp/container/array/operator at") | [|  | | --- | | operator[] |](container/vector/operator_at.html "cpp/container/vector/operator at") | [|  | | --- | | operator[] |](container/deque/operator_at.html "cpp/container/deque/operator at") |  |  |  |  | [|  | | --- | | operator[] |](container/map/operator_at.html "cpp/container/map/operator at") |  |  |  | [|  | | --- | | operator[] |](container/unordered_map/operator_at.html "cpp/container/unordered map/operator at") |  |  |  |  |  |  | [|  | | --- | | operator[] |](container/flat_map/operator_at.html "cpp/container/flat map/operator at") |  | |  | | --- | | operator[] | |
| |  | | --- | | data | | |  | | --- | | data | | |  | | --- | | data | | |  | | --- | | data | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | data | |
| |  | | --- | | front | | |  | | --- | | front | | |  | | --- | | front | | |  | | --- | | front | | |  | | --- | | front | | |  | | --- | | front | | |  | | --- | | front | |  |  |  |  |  |  |  |  |  | |  | | --- | | front | | |  | | --- | | top | |  |  |  |  | |  | | --- | | front | |
| |  | | --- | | back | | |  | | --- | | back | | |  | | --- | | back | | |  | | --- | | back | | |  | | --- | | back | |  | |  | | --- | | back | |  |  |  |  |  |  |  |  | |  | | --- | | top | | |  | | --- | | back | |  |  |  |  |  | |  | | --- | | back | |
| Capacity | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | |  | | --- | | empty | | Capacity |
| |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | |  | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | | |  | | --- | | size | |
| |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | |  |  |  | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | | |  | | --- | | max_size | |
| |  | | --- | | resize | | |  | | --- | | resize | |  | |  | | --- | | resize | | |  | | --- | | resize | | |  | | --- | | resize | | |  | | --- | | resize | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | resize | |
| |  | | --- | | capacity | | |  | | --- | | capacity | |  | |  | | --- | | capacity | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | capacity | |
| |  | | --- | | reserve | | |  | | --- | | reserve | |  | |  | | --- | | reserve | |  |  |  |  |  |  |  | |  | | --- | | reserve | | |  | | --- | | reserve | | |  | | --- | | reserve | | |  | | --- | | reserve | |  |  |  |  |  |  |  | |  | | --- | | reserve | |
| |  | | --- | | shrink_to_fit | | |  | | --- | | shrink_to_fit | |  | |  | | --- | | shrink_to_fit | | |  | | --- | | shrink_to_fit | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | shrink_to_fit | |
| Modifiers | |  | | --- | | clear | | |  | | --- | | clear | |  | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | |  |  |  | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | |  | | --- | | clear | | Modifiers |
| |  | | --- | | insert | | |  | | --- | | insert | |  | |  | | --- | | insert | | |  | | --- | | insert | | |  | | --- | | insert_after | | |  | | --- | | insert | | |  | | --- | | insert | | |  | | --- | | insert | | |  | | --- | | insert | | |  | | --- | | insert | | |  | | --- | | insert | | |  | | --- | | insert | | |  | | --- | | insert | | |  | | --- | | insert | |  |  |  | |  | | --- | | insert | | |  | | --- | | insert | | |  | | --- | | insert | | |  | | --- | | insert | | |  | | --- | | insert | |
| |  | | --- | | insert_range | | |  | | --- | | insert_range | |  | |  | | --- | | insert_range | | |  | | --- | | insert_range | | |  | | --- | | insert_range_after | | |  | | --- | | insert_range | | |  | | --- | | insert_range | | |  | | --- | | insert_range | | |  | | --- | | insert_range | | |  | | --- | | insert_range | | |  | | --- | | insert_range | | |  | | --- | | insert_range | | |  | | --- | | insert_range | | |  | | --- | | insert_range | |  |  |  | |  | | --- | | insert_range | | |  | | --- | | insert_range | | |  | | --- | | insert_range | | |  | | --- | | insert_range | | |  | | --- | | insert_range | |
| |  | | --- | | insert_or_assign | |  |  |  |  |  |  |  |  | |  | | --- | | insert_or_assign | |  |  |  | |  | | --- | | insert_or_assign | |  |  |  |  |  |  | |  | | --- | | insert_or_assign | |  | |  | | --- | | insert_or_assign | |
| |  | | --- | | emplace | |  |  | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace_after | | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace | |  |  |  | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace | |
| |  | | --- | | emplace_hint | |  |  |  |  |  |  | |  | | --- | | emplace_hint | | |  | | --- | | emplace_hint | | |  | | --- | | emplace_hint | | |  | | --- | | emplace_hint | | |  | | --- | | emplace_hint | | |  | | --- | | emplace_hint | | |  | | --- | | emplace_hint | | |  | | --- | | emplace_hint | |  |  |  | |  | | --- | | emplace_hint | | |  | | --- | | emplace_hint | | |  | | --- | | emplace_hint | | |  | | --- | | emplace_hint | | |  | | --- | | emplace_hint | |
| |  | | --- | | try_emplace | |  |  |  |  |  |  |  |  | |  | | --- | | try_emplace | |  |  |  | |  | | --- | | try_emplace | |  |  |  |  |  |  | |  | | --- | | try_emplace | |  | |  | | --- | | try_emplace | |
| |  | | --- | | erase | | |  | | --- | | erase | |  | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase_after | | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | |  |  |  | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | |
| |  | | --- | | push_front | |  |  |  | |  | | --- | | push_front | | |  | | --- | | push_front | | |  | | --- | | push_front | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | push_front | |
| |  | | --- | | prepend_range | |  |  |  | |  | | --- | | prepend_range | | |  | | --- | | prepend_range | | |  | | --- | | prepend_range | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | prepend_range | |
| |  | | --- | | emplace_front | |  |  |  | |  | | --- | | emplace_front | | |  | | --- | | emplace_front | | |  | | --- | | emplace_front | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | emplace_front | |
| |  | | --- | | pop_front | |  |  |  | |  | | --- | | pop_front | | |  | | --- | | pop_front | | |  | | --- | | pop_front | |  |  |  |  |  |  |  |  |  | |  | | --- | | pop | | |  | | --- | | pop | |  |  |  |  | |  | | --- | | pop_front | |
| |  | | --- | | push_back | | |  | | --- | | push_back | |  | |  | | --- | | push_back | | |  | | --- | | push_back | |  | |  | | --- | | push_back | |  |  |  |  |  |  |  |  | |  | | --- | | push | | |  | | --- | | push | | |  | | --- | | push | |  |  |  |  | |  | | --- | | push_back | |
| |  | | --- | | append_range | | |  | | --- | | append_range | |  | |  | | --- | | append_range | | |  | | --- | | append_range | |  | |  | | --- | | append_range | |  |  |  |  |  |  |  |  | |  | | --- | | push_range | | |  | | --- | | push_range | | |  | | --- | | push_range | |  |  |  |  | |  | | --- | | append_range | |
| |  | | --- | | emplace_back | |  |  | |  | | --- | | emplace_back | | |  | | --- | | emplace_back | |  | |  | | --- | | emplace_back | |  |  |  |  |  |  |  |  | |  | | --- | | emplace | | |  | | --- | | emplace | | |  | | --- | | emplace | |  |  |  |  | |  | | --- | | emplace_back | |
| |  | | --- | | pop_back | | |  | | --- | | pop_back | |  | |  | | --- | | pop_back | | |  | | --- | | pop_back | |  | |  | | --- | | pop_back | |  |  |  |  |  |  |  |  | |  | | --- | | pop | |  |  |  |  |  |  | |  | | --- | | pop_back | |
| |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | |
| |  | | --- | | merge | |  |  |  |  | |  | | --- | | merge | | |  | | --- | | merge | | |  | | --- | | merge | | |  | | --- | | merge | | |  | | --- | | merge | | |  | | --- | | merge | | |  | | --- | | merge | | |  | | --- | | merge | | |  | | --- | | merge | | |  | | --- | | merge | |  |  |  |  |  |  |  | |  | | --- | | merge | |
| |  | | --- | | extract [[1]](container.html#cite_note-1) | |  |  |  |  |  |  | |  | | --- | | extract | | |  | | --- | | extract | | |  | | --- | | extract | | |  | | --- | | extract | | |  | | --- | | extract | | |  | | --- | | extract | | |  | | --- | | extract | | |  | | --- | | extract | |  |  |  |  |  |  |  | |  | | --- | | extract | |
| List operations | |  | | --- | | splice | |  |  |  |  | |  | | --- | | splice_after | | |  | | --- | | splice | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | splice | | List operations |
| |  | | --- | | remove | |  |  |  |  | |  | | --- | | remove | | |  | | --- | | remove | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | remove | |
| |  | | --- | | remove_if | |  |  |  |  | |  | | --- | | remove_if | | |  | | --- | | remove_if | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | remove_if | |
| |  | | --- | | reverse | |  |  |  |  | |  | | --- | | reverse | | |  | | --- | | reverse | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | reverse | |
| |  | | --- | | unique | |  |  |  |  | |  | | --- | | unique | | |  | | --- | | unique | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | unique | |
| |  | | --- | | sort | |  |  |  |  | |  | | --- | | sort | | |  | | --- | | sort | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | sort | |
| Bucket and Hash | |  | | --- | | begin(size_type) | | cbegin(size_type) | |  |  |  |  |  |  |  |  |  |  | |  | | --- | | begin(size_type) | | cbegin(size_type) | | |  | | --- | | begin(size_type) | | cbegin(size_type) | | |  | | --- | | begin(size_type) | | cbegin(size_type) | | |  | | --- | | begin(size_type) | | cbegin(size_type) | |  |  |  |  |  |  |  | |  | | --- | | begin(size_type) | | cbegin(size_type) | | Bucket and Hash |
| |  | | --- | | end(size_type) | | cend(size_type) | |  |  |  |  |  |  |  |  |  |  | |  | | --- | | end(size_type) | | cend(size_type) | | |  | | --- | | end(size_type) | | cend(size_type) | | |  | | --- | | end(size_type) | | cend(size_type) | | |  | | --- | | end(size_type) | | cend(size_type) | |  |  |  |  |  |  |  | |  | | --- | | end(size_type) | | cend(size_type) | |
| |  | | --- | | bucket_count | |  |  |  |  |  |  |  |  |  |  | |  | | --- | | bucket_count | | |  | | --- | | bucket_count | | |  | | --- | | bucket_count | | |  | | --- | | bucket_count | |  |  |  |  |  |  |  | |  | | --- | | bucket_count | |
| |  | | --- | | max_bucket_count | |  |  |  |  |  |  |  |  |  |  | |  | | --- | | max_bucket_count | | |  | | --- | | max_bucket_count | | |  | | --- | | max_bucket_count | | |  | | --- | | max_bucket_count | |  |  |  |  |  |  |  | |  | | --- | | max_bucket_count | |
| |  | | --- | | bucket_size | |  |  |  |  |  |  |  |  |  |  | |  | | --- | | bucket_size | | |  | | --- | | bucket_size | | |  | | --- | | bucket_size | | |  | | --- | | bucket_size | |  |  |  |  |  |  |  | |  | | --- | | bucket_size | |
| |  | | --- | | bucket | |  |  |  |  |  |  |  |  |  |  | |  | | --- | | bucket | | |  | | --- | | bucket | | |  | | --- | | bucket | | |  | | --- | | bucket | |  |  |  |  |  |  |  | |  | | --- | | bucket | |
| |  | | --- | | load_factor | |  |  |  |  |  |  |  |  |  |  | |  | | --- | | load_factor | | |  | | --- | | load_factor | | |  | | --- | | load_factor | | |  | | --- | | load_factor | |  |  |  |  |  |  |  | |  | | --- | | load_factor | |
| |  | | --- | | max_load_factor | |  |  |  |  |  |  |  |  |  |  | |  | | --- | | max_load_factor | | |  | | --- | | max_load_factor | | |  | | --- | | max_load_factor | | |  | | --- | | max_load_factor | |  |  |  |  |  |  |  | |  | | --- | | max_load_factor | |
| |  | | --- | | rehash | |  |  |  |  |  |  |  |  |  |  | |  | | --- | | rehash | | |  | | --- | | rehash | | |  | | --- | | rehash | | |  | | --- | | rehash | |  |  |  |  |  |  |  | |  | | --- | | rehash | |
| Lookup | |  | | --- | | count | |  |  |  |  |  |  | |  | | --- | | count | | |  | | --- | | count | | |  | | --- | | count | | |  | | --- | | count | | |  | | --- | | count | | |  | | --- | | count | | |  | | --- | | count | | |  | | --- | | count | |  |  |  | |  | | --- | | count | | |  | | --- | | count | | |  | | --- | | count | | |  | | --- | | count | | |  | | --- | | count | | Lookup |
| |  | | --- | | find | | |  | | --- | | find | |  |  |  |  |  | |  | | --- | | find | | |  | | --- | | find | | |  | | --- | | find | | |  | | --- | | find | | |  | | --- | | find | | |  | | --- | | find | | |  | | --- | | find | | |  | | --- | | find | |  |  |  | |  | | --- | | find | | |  | | --- | | find | | |  | | --- | | find | | |  | | --- | | find | | |  | | --- | | find | |
| |  | | --- | | contains | | |  | | --- | | contains | |  |  |  |  |  | |  | | --- | | contains | | |  | | --- | | contains | | |  | | --- | | contains | | |  | | --- | | contains | | |  | | --- | | contains | | |  | | --- | | contains | | |  | | --- | | contains | | |  | | --- | | contains | |  |  |  | |  | | --- | | contains | | |  | | --- | | contains | | |  | | --- | | contains | | |  | | --- | | contains | | |  | | --- | | contains | |
| |  | | --- | | lower_bound | |  |  |  |  |  |  | |  | | --- | | lower_bound | | |  | | --- | | lower_bound | | |  | | --- | | lower_bound | | |  | | --- | | lower_bound | |  |  |  |  |  |  |  | |  | | --- | | lower_bound | | |  | | --- | | lower_bound | | |  | | --- | | lower_bound | | |  | | --- | | lower_bound | | |  | | --- | | lower_bound | |
| |  | | --- | | upper_bound | |  |  |  |  |  |  | |  | | --- | | upper_bound | | |  | | --- | | upper_bound | | |  | | --- | | upper_bound | | |  | | --- | | upper_bound | |  |  |  |  |  |  |  | |  | | --- | | upper_bound | | |  | | --- | | upper_bound | | |  | | --- | | upper_bound | | |  | | --- | | upper_bound | | |  | | --- | | upper_bound | |
| |  | | --- | | equal_range | |  |  |  |  |  |  | |  | | --- | | equal_range | | |  | | --- | | equal_range | | |  | | --- | | equal_range | | |  | | --- | | equal_range | | |  | | --- | | equal_range | | |  | | --- | | equal_range | | |  | | --- | | equal_range | | |  | | --- | | equal_range | |  |  |  | |  | | --- | | equal_range | | |  | | --- | | equal_range | | |  | | --- | | equal_range | | |  | | --- | | equal_range | | |  | | --- | | equal_range | |
| Observers | |  | | --- | | key_comp | |  |  |  |  |  |  | |  | | --- | | key_comp | | |  | | --- | | key_comp | | |  | | --- | | key_comp | | |  | | --- | | key_comp | |  |  |  |  |  |  |  | |  | | --- | | key_comp | | |  | | --- | | key_comp | | |  | | --- | | key_comp | | |  | | --- | | key_comp | | |  | | --- | | key_comp | | Observers |
| |  | | --- | | value_comp | |  |  |  |  |  |  | |  | | --- | | value_comp | | |  | | --- | | value_comp | | |  | | --- | | value_comp | | |  | | --- | | value_comp | |  |  |  |  |  |  |  | |  | | --- | | value_comp | | |  | | --- | | value_comp | | |  | | --- | | value_comp | | |  | | --- | | value_comp | | |  | | --- | | value_comp | |
| |  | | --- | | hash_function | |  |  |  |  |  |  |  |  |  |  | |  | | --- | | hash_function | | |  | | --- | | hash_function | | |  | | --- | | hash_function | | |  | | --- | | hash_function | |  |  |  |  |  |  |  | |  | | --- | | hash_function | |
| |  | | --- | | key_eq | |  |  |  |  |  |  |  |  |  |  | |  | | --- | | key_eq | | |  | | --- | | key_eq | | |  | | --- | | key_eq | | |  | | --- | | key_eq | |  |  |  |  |  |  |  | |  | | --- | | key_eq | |
| Allocator | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | |  | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | | |  | | --- | | get_allocator | |  |  |  |  |  |  |  | |  | | --- | | get_allocator | | Allocator |
| Adaptors | |  | | --- | | extract [[2]](container.html#cite_note-2) | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | extract | | |  | | --- | | extract | | |  | | --- | | extract | | |  | | --- | | extract | | |  | | --- | | extract | | Adaptors |
| |  | | --- | | replace | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | replace | | |  | | --- | | replace | | |  | | --- | | replace | | |  | | --- | | replace | | |  | | --- | | replace | |
| Container | | |  | | --- | | ****basic_string**** | | |  | | --- | | ****array**** | | |  | | --- | | ****vector**** | | |  | | --- | | ****deque**** | | |  | | --- | | ****forward_list**** | | |  | | --- | | ****list**** | | |  | | --- | | ****set**** | | |  | | --- | | ****multiset**** | | |  | | --- | | ****map**** | | |  | | --- | | ****multimap**** | | |  | | --- | | ****unordered_set**** | | |  | | --- | | ****unordered_multiset**** | | |  | | --- | | ****unordered_map**** | | |  | | --- | | ****unordered_multimap**** | | |  | | --- | | ****stack**** | | |  | | --- | | ****queue**** | | |  | | --- | | ****priority_queue**** | | |  | | --- | | ****flat_set**** | | |  | | --- | | ****flat_multiset**** | | |  | | --- | | ****flat_map**** | | |  | | --- | | ****flat_multimap**** | | Container | |
| Header | | `<string>` | `<array>` | `<vector>` | `<deque>` | `<forward_list>` | `<list>` | `<set>` | | `<map>` | | `<unordered_set>` | | `<unordered_map>` | | `<stack>` | `<queue>` | | `<flat_set>` | | `<flat_map>` | | Header | |
|  | | Pseudo container | Sequence containers | | | | | Associative containers | | | | Unordered associative containers | | | | Container adaptors | | | | | | |  | |

- Note: functions in two different extract lines have different meanings and syntax:

1. ↑ e.g., node_type extract(const_iterator) or node_type extract(Key&)
2. ↑ e.g., container_type extract() &&

#### Non-member function table

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | Pseudo container | Sequence containers | | | | | Associative containers | | | | Unordered associative containers | | | | Container adaptors | | | | | | |  | |
| Header | | `<string>` | `<array>` | `<vector>` | `<deque>` | `<forward_list>` | `<list>` | `<set>` | | `<map>` | | `<unordered_set>` | | `<unordered_map>` | | `<stack>` | `<queue>` | | `<flat_set>` | | `<flat_map>` | | Header | |
| Container | | |  | | --- | | ****basic_string**** | | |  | | --- | | ****array**** | | |  | | --- | | ****vector**** | | |  | | --- | | ****deque**** | | |  | | --- | | ****forward_list**** | | |  | | --- | | ****list**** | | |  | | --- | | ****set**** | | |  | | --- | | ****multiset**** | | |  | | --- | | ****map**** | | |  | | --- | | ****multimap**** | | |  | | --- | | ****unordered_set**** | | |  | | --- | | ****unordered_multiset**** | | |  | | --- | | ****unordered_map**** | | |  | | --- | | ****unordered_multimap**** | | |  | | --- | | ****stack**** | | |  | | --- | | ****queue**** | | |  | | --- | | ****priority_queue**** | | |  | | --- | | ****flat_set**** | | |  | | --- | | ****flat_multiset**** | | |  | | --- | | ****flat_map**** | | |  | | --- | | ****flat_multimap**** | | Container | |
| Non-member function | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | |  | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | |  | | --- | | operator== | | Non-member function |
| |  | | --- | | operator!= (removed in C++20) | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | | |  | | --- | | operator!= | |  |  |  |  |  | |  | | --- | | operator!= (removed in C++20) | |
| |  | | --- | | operator< (removed in C++20) | | |  | | --- | | operator< | | |  | | --- | | operator< | | |  | | --- | | operator< | | |  | | --- | | operator< | | |  | | --- | | operator< | | |  | | --- | | operator< | | |  | | --- | | operator< | | |  | | --- | | operator< | | |  | | --- | | operator< | | |  | | --- | | operator< | |  |  |  |  | |  | | --- | | operator< | | |  | | --- | | operator< | |  |  |  |  |  | |  | | --- | | operator< (removed in C++20) | |
| |  | | --- | | operator<= (removed in C++20) | | |  | | --- | | operator<= | | |  | | --- | | operator<= | | |  | | --- | | operator<= | | |  | | --- | | operator<= | | |  | | --- | | operator<= | | |  | | --- | | operator<= | | |  | | --- | | operator<= | | |  | | --- | | operator<= | | |  | | --- | | operator<= | | |  | | --- | | operator<= | |  |  |  |  | |  | | --- | | operator<= | | |  | | --- | | operator<= | |  |  |  |  |  | |  | | --- | | operator<= (removed in C++20) | |
| |  | | --- | | operator> (removed in C++20) | | |  | | --- | | operator> | | |  | | --- | | operator> | | |  | | --- | | operator> | | |  | | --- | | operator> | | |  | | --- | | operator> | | |  | | --- | | operator> | | |  | | --- | | operator> | | |  | | --- | | operator> | | |  | | --- | | operator> | | |  | | --- | | operator> | |  |  |  |  | |  | | --- | | operator> | | |  | | --- | | operator> | |  |  |  |  |  | |  | | --- | | operator> (removed in C++20) | |
| |  | | --- | | operator>= (removed in C++20) | | |  | | --- | | operator>= | | |  | | --- | | operator>= | | |  | | --- | | operator>= | | |  | | --- | | operator>= | | |  | | --- | | operator>= | | |  | | --- | | operator>= | | |  | | --- | | operator>= | | |  | | --- | | operator>= | | |  | | --- | | operator>= | | |  | | --- | | operator>= | |  |  |  |  | |  | | --- | | operator>= | | |  | | --- | | operator>= | |  |  |  |  |  | |  | | --- | | operator>= (removed in C++20) | |
| |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | |  |  |  |  | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | |  | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | | |  | | --- | | operator<=> | |
| |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | | |  | | --- | | swap | |
| |  | | --- | | erase | | |  | | --- | | erase | |  | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | | |  | | --- | | erase | |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | |  | | --- | | erase | |
| |  | | --- | | erase_if | | |  | | --- | | erase_if | |  | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | |  |  |  | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | | |  | | --- | | erase_if | |
| Container | | |  | | --- | | ****basic_string**** | | |  | | --- | | ****array**** | | |  | | --- | | ****vector**** | | |  | | --- | | ****deque**** | | |  | | --- | | ****forward_list**** | | |  | | --- | | ****list**** | | |  | | --- | | ****set**** | | |  | | --- | | ****multiset**** | | |  | | --- | | ****map**** | | |  | | --- | | ****multimap**** | | |  | | --- | | ****unordered_set**** | | |  | | --- | | ****unordered_multiset**** | | |  | | --- | | ****unordered_map**** | | |  | | --- | | ****unordered_multimap**** | | |  | | --- | | ****stack**** | | |  | | --- | | ****queue**** | | |  | | --- | | ****priority_queue**** | | |  | | --- | | ****flat_set**** | | |  | | --- | | ****flat_multiset**** | | |  | | --- | | ****flat_map**** | | |  | | --- | | ****flat_multimap**** | | Container | |
| Header | | `<string>` | `<array>` | `<vector>` | `<deque>` | `<forward_list>` | `<list>` | `<set>` | | `<map>` | | `<unordered_set>` | | `<unordered_map>` | | `<stack>` | `<queue>` | | `<flat_set>` | | `<flat_map>` | | Header | |
|  | | Pseudo container | Sequence containers | | | | | Associative containers | | | | Unordered associative containers | | | | Container adaptors | | | | | | |  | |

|  |  |
| --- | --- |
| The `<`, `<=`, `>`, `>=`, and `!=` operators are synthesized from operator<=> and operator== respectively. | (since C++20) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 51 | C++98 | container iterators might be invalidated by arbitrary library operation | they are only invalidated when specified |

### See also

C++ named requirements:

- Container
- SequenceContainer
- ContiguousContainer
- ReversibleContainer
- AssociativeContainer
- AllocatorAwareContainer
- UnorderedAssociativeContainer

|  |  |
| --- | --- |
| valarray | numeric arrays, array masks and array slices   (class template) |
| basic_string | stores and manipulates sequences of characters   (class template) |
| basic_string_view(C++17) | read-only string view   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container&oldid=179897>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 28 January 2025, at 10:28.