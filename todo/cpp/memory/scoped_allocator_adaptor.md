# std::scoped_allocator_adaptor

From cppreference.com
< cpp‎ | memory
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

Memory management library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **voidify**(exposition only\*) | | | | | | Uninitialized memory algorithms | | | | | | uninitialized_copy | | | | | | uninitialized_fill | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | destroy(C++17) | | | | | | destroy_at(C++17) | | | | | | uninitialized_copy_n(C++11) | | | | | | uninitialized_fill_n | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | destroy_n(C++17) | | | | | | construct_at(C++20) | | | | | | Constrained uninitialized memory algorithms | | | | | | ranges::uninitialized_copy(C++20) | | | | | | ranges::uninitialized_fill(C++20) | | | | | | ranges::uninitialized_move(C++20) | | | | | | ranges::construct_at(C++20) | | | | | | ranges::destroy(C++20) | | | | | | ranges::destroy_n(C++20) | | | | | | ranges::destroy_at(C++20) | | | | | | ranges::uninitialized_copy_n(C++20) | | | | | | ranges::uninitialized_fill_n(C++20) | | | | | | ranges::uninitialized_move_n(C++20) | | | | | | ranges::uninitialized_default_construct(C++20) | | | | | | ranges::uninitialized_value_construct(C++20) | | | | | | ranges::uninitialized_default_construct_n(C++20) | | | | | | ranges::uninitialized_value_construct_n(C++20) | | | | | | C Library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | malloc | | | | | | calloc | | | | | | realloc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | aligned_alloc(C++17) | | | | | | free | | | | | |  | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Allocators | | | | | | allocator | | | | | | allocator_traits(C++11) | | | | | | allocation_result(C++23) | | | | | | allocator_arg(C++11) | | | | | | uses_allocator(C++11) | | | | | | uses_allocator_construction_args(C++20) | | | | | | make_obj_using_allocator(C++20) | | | | | | uninitialized_construct_using_allocator(C++20) | | | | | | ****scoped_allocator_adaptor****(C++11) | | | | | | pmr::polymorphic_allocator(C++17) | | | | | | Memory resources | | | | | | pmr::memory_resource(C++17) | | | | | | pmr::get_default_resource(C++17) | | | | | | pmr::set_default_resource(C++17) | | | | | | pmr::new_delete_resource(C++17) | | | | | | pmr::null_memory_resource(C++17) | | | | | | pmr::synchronized_pool_resource(C++17) | | | | | | pmr::unsynchronized_pool_resource(C++17) | | | | | | pmr::monotonic_buffer_resource(C++17) | | | | | | pmr::pool_options(C++17) | | | | | | Garbage collection support | | | | | | declare_reachable(C++11)(until C++23) | | | | | | undeclare_reachable(C++11)(until C++23) | | | | | | declare_no_pointers(C++11)(until C++23) | | | | | | undeclare_no_pointers(C++11)(until C++23) | | | | | | pointer_safety(C++11)(until C++23) | | | | | | get_pointer_safety(C++11)(until C++23) | | | | | | Uninitialized storage | | | | | | raw_storage_iterator(until C++20\*) | | | | | | get_temporary_buffer(until C++20\*) | | | | | | return_temporary_buffer(until C++20\*) | | | | | | Explicit lifetime management | | | | | | start_lifetime_asstart_lifetime_as_array(C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Smart pointers | | | | | | unique_ptr(C++11) | | | | | | shared_ptr(C++11) | | | | | | weak_ptr(C++11) | | | | | | auto_ptr(until C++17\*) | | | | | | owner_less(C++11) | | | | | | owner_less<void>(C++17) | | | | | | owner_hash(C++26) | | | | | | owner_equal(C++26) | | | | | | enable_shared_from_this(C++11) | | | | | | bad_weak_ptr(C++11) | | | | | | default_delete(C++11) | | | | | | out_ptr_t(C++23) | | | | | | inout_ptr_t(C++23) | | | | | | Low level memory management | | | | | | operator new | | | | | | [operator new[]](new/operator_new.html "cpp/memory/new/operator new") | | | | | | operator delete | | | | | | [operator delete[]](new/operator_delete.html "cpp/memory/new/operator delete") | | | | | | get_new_handler(C++11) | | | | | | set_new_handler | | | | | | launder(C++17) | | | | | | bad_alloc | | | | | | bad_array_new_length(C++11) | | | | | | nothrow_t | | | | | | align_val_t(C++17) | | | | | | destroying_delete_t(C++20) | | | | | | new_handler | | | | | | nothrow | | | | | | Miscellaneous | | | | | | pointer_traits(C++11) | | | | | | to_address(C++20) | | | | | | addressof(C++11) | | | | | | align(C++11) | | | | | | assume_aligned(C++20) | | | | | | is_sufficiently_aligned(C++26) | | | | | |

****std::scoped_allocator_adaptor****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| scoped_allocator_adaptor::scoped_allocator_adaptor | | | | |
| scoped_allocator_adaptor::~scoped_allocator_adaptor | | | | |
| scoped_allocator_adaptor::operator= | | | | |
| scoped_allocator_adaptor::inner_allocator | | | | |
| scoped_allocator_adaptor::outer_allocator | | | | |
| scoped_allocator_adaptor::allocate | | | | |
| scoped_allocator_adaptor::deallocate | | | | |
| scoped_allocator_adaptor::max_size | | | | |
| scoped_allocator_adaptor::construct | | | | |
| scoped_allocator_adaptor::destroy | | | | |
| scoped_allocator_adaptor::select_on_container_copy_construction | | | | |
| **scoped_allocator_adaptor::outermost** **scoped_allocator_adaptor::outermost-construct** **scoped_allocator_adaptor::outermost-destroy** | | | | |
| Non-member functions | | | | |
| operator==operator!=(until C++20) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<scoped_allocator>` |  |  |
| template< class OuterAlloc, class... InnerAllocs >  class scoped_allocator_adaptor : public OuterAlloc; |  | (since C++11) |
|  |  |  |

The `std::scoped_allocator_adaptor` class template is an allocator which can be used with multilevel containers (vector of sets of lists of tuples of maps, etc). It is instantiated with one outer allocator type `OuterAlloc` and zero or more inner allocator types `InnerAlloc...`. A container constructed directly with a `scoped_allocator_adaptor` uses `OuterAlloc` to allocate its elements, but if an element is itself a container, it uses the first inner allocator. The elements of that container, if they are themselves containers, use the second inner allocator, etc. If there are more levels to the container than there are inner allocators, the last inner allocator is reused for all further nested containers.

The purpose of this adaptor is to correctly initialize stateful allocators in nested containers, such as when all levels of a nested container must be placed in the same shared memory segment. The adaptor's constructor takes the arguments for all allocators in the list, and each nested container obtains its allocator's state from the adaptor as needed.

For the purpose of `scoped_allocator_adaptor`, if the next inner allocator is `A`, any class `T` for which std::uses_allocator<T,A>::value == true participates in the recursion as if it was a container. Additionally, std::pair is treated as such a container by specific overloads of scoped_allocator_adaptor::construct.

Typical implementation holds an instance of a `std::scoped_allocator_adaptor<InnerAllocs...>` as a member object.

Note that std::pmr::polymorphic_allocators propagate to nested containers following uses-allocator construction and do not need (and do not work with) `std::scoped_allocator_adaptor`.

### Nested types

|  |  |
| --- | --- |
| Type | Definition |
| `outer_allocator_type` | `OuterAlloc` |
| `inner_allocator_type` | - scoped_allocator_adaptor<OuterAlloc> if sizeof...(InnerAllocs) is zero - scoped_allocator_adaptor<InnerAllocs...> otherwise |
| `value_type` | std::allocator_traits<OuterAlloc>::value_type |
| `size_type` | std::allocator_traits<OuterAlloc>::size_type |
| `difference_type` | std::allocator_traits<OuterAlloc>::difference_type |
| `pointer` | std::allocator_traits<OuterAlloc>::pointer |
| `const_pointer` | std::allocator_traits<OuterAlloc>::const_pointer |
| `void_pointer` | std::allocator_traits<OuterAlloc>::void_pointer |
| `const_void_pointer` | std::allocator_traits<OuterAlloc>::const_void_pointer |

Given the set of `OuterAlloc` and `InnerAlloc...` as `Allocs`:

|  |  |
| --- | --- |
| Type | Definition |
| `propagate_on_container_copy_assignment` | - std::true_type if there exists a type `A` in `Allocs` such that std::allocator_traits<A>::     propagate_on_container_copy_assignment::value is true - std::false_type otherwise |
| `propagate_on_container_move_assignment` | - std::true_type if there exists a type `A` in `Allocs` such that std::allocator_traits<A>::     propagate_on_container_move_assignment::value is true - std::false_type otherwise |
| `propagate_on_container_swap` | - std::true_type if there exists a type `A` in `Allocs` such that std::allocator_traits<A>::     propagate_on_container_swap::value is true - std::false_type otherwise |
| `is_always_equal` | - std::true_type if there exists a type `A` in `Allocs` such that std::allocator_traits<A>::     is_always_equal::value is true - std::false_type otherwise |

### Member functions

|  |  |
| --- | --- |
| (constructor) | creates a new `scoped_allocator_adaptor` object   (public member function) |
| (destructor) | destructs a `scoped_allocator_adaptor` object   (public member function) |
| operator= | assigns a `scoped_allocator_adaptor`   (public member function) |
| inner_allocator | obtains an `inner_allocator` reference   (public member function) |
| outer_allocator | obtains an `outer_allocator` reference   (public member function) |
| allocate | allocates uninitialized storage using the outer allocator   (public member function) |
| deallocate | deallocates storage using the outer allocator   (public member function) |
| max_size | returns the largest allocation size supported by the outer allocator   (public member function) |
| construct | constructs an object in allocated storage, passing the inner allocator to its constructor if appropriate   (public member function) |
| destroy | destructs an object in allocated storage   (public member function) |
| select_on_container_copy_construction | copies the state of `scoped_allocator_adaptor` and all its allocators   (public member function) |
| Exposition-only function templates | |
| ****outermost**** | obtains the outermost allocator (exposition-only member function\*) |
| ****outermost-construct**** | constructs an object using the outermost allocator (exposition-only member function\*) |
| ****outermost-destroy**** | destroys an object using the outermost allocator (exposition-only member function\*) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=(removed in C++20) | compares two `scoped_allocator_adaptor` objects   (function template) |

### Deduction guides(since C++17)

### Nested classes

|  |  |
| --- | --- |
| Class | Definition |
| `rebind` | template< class T >  struct rebind  {      using other = scoped_allocator_adaptor                        <std::allocator_traits<OuterAlloc>::template rebind_alloc<T>,                          InnerAllocs...>;  }; |

### Example

Run this code

```
#include <boost/interprocess/allocators/adaptive_pool.hpp>
#include <boost/interprocess/managed_shared_memory.hpp>
#include <scoped_allocator>
#include <vector>
 
namespace bi = boost::interprocess;
 
template<class T>
using alloc = bi::adaptive_pool<T, bi::managed_shared_memory::segment_manager>;
 
using ipc_row = std::vector<int, alloc<int>>;
 
using ipc_matrix = std::vector<ipc_row, std::scoped_allocator_adaptor<alloc<ipc_row>>>;
 
int main()
{
    bi::managed_shared_memory s(bi::create_only, "Demo", 65536);
 
    // create vector of vectors in shared memory
    ipc_matrix v(s.get_segment_manager());
 
    // for all these additions, the inner vectors obtain their allocator arguments
    // from the outer vector's scoped_allocator_adaptor
    v.resize(1);
    v[0].push_back(1);
    v.emplace_back(2);
    std::vector<int> local_row = {1, 2, 3};
    v.emplace_back(local_row.begin(), local_row.end());
 
    bi::shared_memory_object::remove("Demo");
}

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2108 | C++11 | there was no way to show if `scoped_allocator_adaptor` is stateless | provided `is_always_equal` |

### See also

|  |  |
| --- | --- |
| allocator_traits(C++11) | provides information about allocator types   (class template) |
| uses_allocator(C++11) | checks if the specified type supports uses-allocator construction   (class template) |
| allocator | the default allocator   (class template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/memory/scoped_allocator_adaptor&oldid=179773>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 January 2025, at 07:16.