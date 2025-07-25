# Node handle (C++17)

From cppreference.com
< cpp‎ | container
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

|  |  |  |
| --- | --- | --- |
| template</\* unspecified \*/>  class /\*node-handle\*/; |  | (since C++17)  (exposition only\*) |
|  |  |  |

Associative containers std::set, std::map, std::multiset, std::multimap, std::unordered_set, std::unordered_map, std::unordered_multiset, std::unordered_multimap are node-based data structures, and their nodes can be extracted as an object of unspecified type known as **node handle**.

Node handle is a move-only type that owns and provides access to the element (the `value_type`) stored in the node, and provides non-const access to the key part of the element (the `key_type`) and the mapped part of the element (the `mapped_type`). If the node handle destructs while holding the node, the node is properly destructed using the appropriate allocator for the container. The node handle contains a copy of the container’s allocator. This is necessary so that the node handle can outlive the container.

The exact type of node handle (shown here as /\*node-handle\*/) is unspecified, but each container exposes its node handle type as the member `node_type`.

Node handles can be used to transfer ownership of an element between two associative containers with the same key, value, and allocator type (ignoring comparison or hash/equality), without invoking any copy/move operations on the container element (this kind of operation is known as "splicing"). Transfer between unique and non-unique containers is also permitted: a node handle from a std::map can be inserted into an std::multimap, but not into std::unordered_map or std::set.

A node handle may be empty, in which case it holds no element and no allocator. The default-constructed and moved-from node handle is empty. In addition, an empty node handle can be produced by a failed call to container member function `extract`.

Pointers and references to an element that are obtained while it is owned by a node handle are invalidated if the element is successfully inserted into a container.

For all map containers (std::map, std::multimap, std::unordered_map, and std::unordered_multimap) whose `key_type` is `K` and `mapped_type` is `T`, the behavior of operations involving node handles is undefined if a user-defined specialization of std::pair exists for std::pair<K, T> or std::pair<const K, T>.

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `key_type` (map containers only) | the key stored in the node |
| `mapped_type` (map containers only) | the mapped part of the element stored in the node |
| `value_type` (set containers only) | the element stored in the node |
| `allocator_type` | the allocator to be used when destroying the element |
| `container_node_type` (private) | a container node, the type is unspecified (exposition-only member type\*) |
| `ator_traits` (private) | allocator traits of type std::allocator_traits<allocator_type> (exposition-only member type\*) |

### Data members

|  |  |
| --- | --- |
| Member | Definition |
| typename ator_traits::template     rebind_traits<container_node_type>::pointer `ptr_`  (conditionally present) | TODO (exposition-only member object\*) |
| std::optional<allocator_type> `alloc_`  (conditionally present) | TODO (exposition-only member object\*) |

### Member functions

## constructors

|  |  |  |
| --- | --- | --- |
| constexpr /\*node-handle\*/() noexcept; | (1) |  |
| /\*node-handle\*/(/\*node-handle\*/&& nh) noexcept; | (2) |  |
|  |  |  |

1) The default constructor initializes the node handle to the empty state.2) The move constructor takes ownership of the container element from nh, move-constructs the member allocator, and leaves nh in the empty state.

### Parameters

|  |  |  |
| --- | --- | --- |
| nh | - | a node handle with the same type (not necessarily the same container) |

### Notes

Node handles are move-only, the copy constructor is not defined.

## operator=

|  |  |  |
| --- | --- | --- |
| /\*node-handle\*/& operator=(/\*node-handle\*/&& nh); |  |  |
|  |  |  |

- If the node handle is not empty,

:   - destroys the `value_type` subobject in the container element object managed by this node handle by calling `ator_traits::destroy`;
    - deallocates the container element by calling ator_traits::rebind_traits</\*container-node-type\*/>::deallocate;

- Acquires ownership of the container element from nh;
- If node handle was empty (and so did not contain an allocator) or if ator_traits::propagate_on_container_move_assignment is true, move-assigns the allocator from nh;
- sets nh to the empty state.

The behavior is undefined if the node is not empty and ator_traits::propagate_on_container_move_assignment is false and the allocators do not compare equal.

### Parameters

|  |  |  |
| --- | --- | --- |
| nh | - | node handle with the same type (not necessarily the same container) |

### Return

\*this

### Exceptions

Throws nothing.

### Notes

Node handles are move-only, the copy assignment is not defined.

## destructor

|  |  |  |
| --- | --- | --- |
| ~/\*node-handle\*/(); |  |  |
|  |  |  |

- If the node handle is not empty,

:   - destroys the `value_type` subobject in the container element object managed by this node handle by calling ator_traits::destroy;
    - deallocates the container element by calling ator_traits::rebind_traits</\*container-node-type\*/>::deallocate.

## empty

|  |  |  |
| --- | --- | --- |
| bool empty() const noexcept; |  |  |
|  |  |  |

Returns true if the node handle is empty, false otherwise.

## operator bool

|  |  |  |
| --- | --- | --- |
| explicit operator bool() const noexcept; |  |  |
|  |  |  |

Converts to false if the node handle is empty, true otherwise.

## get_allocator

|  |  |  |
| --- | --- | --- |
| allocator_type get_allocator() const; |  |  |
|  |  |  |

Returns a copy of the stored allocator (which is a copy of the allocator of the source container). The behavior is undefined if the node handle is empty.

### Exceptions

Throws nothing.

## value

|  |  |  |
| --- | --- | --- |
| value_type& value() const; |  | (set containers only) |
|  |  |  |

Returns a reference to the `value_type` subobject in the container element object managed by this node handle. The behavior is undefined if the node handle is empty.

### Exceptions

Throws nothing.

## key

|  |  |  |
| --- | --- | --- |
| key_type& key() const; |  | (map containers only) |
|  |  |  |

Returns a non-const reference to the `key_type` member of the `value_type` subobject in the container element object managed by this node handle. The behavior is undefined if the node handle is empty.

### Exceptions

Throws nothing.

### Notes

This function makes it possible to modify the key of a node extracted from a map, and then re-insert it into the map, without ever copying or moving the element.

## mapped

|  |  |  |
| --- | --- | --- |
| mapped_type& mapped() const; |  | (map containers only) |
|  |  |  |

Returns a reference to the `mapped_type` member of the `value_type` subobject in the container element object managed by this node handle. The behavior is undefined if the node handle is empty.

### Exceptions

Throws nothing.

## swap

|  |  |  |
| --- | --- | --- |
| void swap(/\*node-handle\*/& nh) noexcept(/\* see below \*/); |  |  |
|  |  |  |

- swaps ownership of container nodes;
- if one node is empty or if both nodes are non-empty and ator_traits::propagate_on_container_swap is true, swaps the allocators as well.

The behavior is undefined if both nodes are not empty and ator_traits::propagate_on_container_swap is false and the allocators do not compare equal.

### Exceptions

noexcept specification:noexcept(ator_traits::propagate_on_container_swap::value ||  
         ator_traits::is_always_equal::value)

### Non-member functions

## swap

|  |  |  |
| --- | --- | --- |
| friend void swap(/\*node-handle\*/& x, /\*node-handle\*/& y) noexcept(noexcept(x.swap(y))); |  |  |
|  |  |  |

Effectively executes x.swap(y).

This function is not visible to ordinary unqualified or qualified lookup, and can only be found by argument-dependent lookup when `node-handle` is an associated class of the arguments.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/node_handle&oldid=176688>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 October 2024, at 11:45.