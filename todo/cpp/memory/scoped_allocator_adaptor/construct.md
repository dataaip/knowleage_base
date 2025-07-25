# std::scoped_allocator_adaptor<OuterAlloc,InnerAlloc...>::construct

From cppreference.com
< cpp‎ | memory‎ | scoped allocator adaptor
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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | **voidify**(exposition only\*) | | | | | | Uninitialized memory algorithms | | | | | | uninitialized_copy | | | | | | uninitialized_fill | | | | | | uninitialized_move(C++17) | | | | | | uninitialized_default_construct(C++17) | | | | | | uninitialized_value_construct(C++17) | | | | | | destroy(C++17) | | | | | | destroy_at(C++17) | | | | | | uninitialized_copy_n(C++11) | | | | | | uninitialized_fill_n | | | | | | uninitialized_move_n(C++17) | | | | | | uninitialized_default_construct_n(C++17) | | | | | | uninitialized_value_construct_n(C++17) | | | | | | destroy_n(C++17) | | | | | | construct_at(C++20) | | | | | | Constrained uninitialized memory algorithms | | | | | | ranges::uninitialized_copy(C++20) | | | | | | ranges::uninitialized_fill(C++20) | | | | | | ranges::uninitialized_move(C++20) | | | | | | ranges::construct_at(C++20) | | | | | | ranges::destroy(C++20) | | | | | | ranges::destroy_n(C++20) | | | | | | ranges::destroy_at(C++20) | | | | | | ranges::uninitialized_copy_n(C++20) | | | | | | ranges::uninitialized_fill_n(C++20) | | | | | | ranges::uninitialized_move_n(C++20) | | | | | | ranges::uninitialized_default_construct(C++20) | | | | | | ranges::uninitialized_value_construct(C++20) | | | | | | ranges::uninitialized_default_construct_n(C++20) | | | | | | ranges::uninitialized_value_construct_n(C++20) | | | | | | C Library | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | malloc | | | | | | calloc | | | | | | realloc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | aligned_alloc(C++17) | | | | | | free | | | | | |  | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Allocators | | | | | | allocator | | | | | | allocator_traits(C++11) | | | | | | allocation_result(C++23) | | | | | | allocator_arg(C++11) | | | | | | uses_allocator(C++11) | | | | | | uses_allocator_construction_args(C++20) | | | | | | make_obj_using_allocator(C++20) | | | | | | uninitialized_construct_using_allocator(C++20) | | | | | | scoped_allocator_adaptor(C++11) | | | | | | pmr::polymorphic_allocator(C++17) | | | | | | Memory resources | | | | | | pmr::memory_resource(C++17) | | | | | | pmr::get_default_resource(C++17) | | | | | | pmr::set_default_resource(C++17) | | | | | | pmr::new_delete_resource(C++17) | | | | | | pmr::null_memory_resource(C++17) | | | | | | pmr::synchronized_pool_resource(C++17) | | | | | | pmr::unsynchronized_pool_resource(C++17) | | | | | | pmr::monotonic_buffer_resource(C++17) | | | | | | pmr::pool_options(C++17) | | | | | | Garbage collection support | | | | | | declare_reachable(C++11)(until C++23) | | | | | | undeclare_reachable(C++11)(until C++23) | | | | | | declare_no_pointers(C++11)(until C++23) | | | | | | undeclare_no_pointers(C++11)(until C++23) | | | | | | pointer_safety(C++11)(until C++23) | | | | | | get_pointer_safety(C++11)(until C++23) | | | | | | Uninitialized storage | | | | | | raw_storage_iterator(until C++20\*) | | | | | | get_temporary_buffer(until C++20\*) | | | | | | return_temporary_buffer(until C++20\*) | | | | | | Explicit lifetime management | | | | | | start_lifetime_asstart_lifetime_as_array(C++23)(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Smart pointers | | | | | | unique_ptr(C++11) | | | | | | shared_ptr(C++11) | | | | | | weak_ptr(C++11) | | | | | | auto_ptr(until C++17\*) | | | | | | owner_less(C++11) | | | | | | owner_less<void>(C++17) | | | | | | owner_hash(C++26) | | | | | | owner_equal(C++26) | | | | | | enable_shared_from_this(C++11) | | | | | | bad_weak_ptr(C++11) | | | | | | default_delete(C++11) | | | | | | out_ptr_t(C++23) | | | | | | inout_ptr_t(C++23) | | | | | | Low level memory management | | | | | | operator new | | | | | | [operator new[]](../new/operator_new.html "cpp/memory/new/operator new") | | | | | | operator delete | | | | | | [operator delete[]](../new/operator_delete.html "cpp/memory/new/operator delete") | | | | | | get_new_handler(C++11) | | | | | | set_new_handler | | | | | | launder(C++17) | | | | | | bad_alloc | | | | | | bad_array_new_length(C++11) | | | | | | nothrow_t | | | | | | align_val_t(C++17) | | | | | | destroying_delete_t(C++20) | | | | | | new_handler | | | | | | nothrow | | | | | | Miscellaneous | | | | | | pointer_traits(C++11) | | | | | | to_address(C++20) | | | | | | addressof(C++11) | | | | | | align(C++11) | | | | | | assume_aligned(C++20) | | | | | | is_sufficiently_aligned(C++26) | | | | | |

std::scoped_allocator_adaptor

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
| ****scoped_allocator_adaptor::construct**** | | | | |
| scoped_allocator_adaptor::destroy | | | | |
| scoped_allocator_adaptor::select_on_container_copy_construction | | | | |
| **scoped_allocator_adaptor::outermost** **scoped_allocator_adaptor::outermost-construct** **scoped_allocator_adaptor::outermost-destroy** | | | | |
| Non-member functions | | | | |
| operator==operator!=(until C++20) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<scoped_allocator>` |  |  |
| template< class T, class... Args >  void construct( T\* p, Args&&... args ); | (1) |  |
| template< class T1, class T2, class... Args1, class... Args2 >  void construct( std::pair<T1, T2>\* p, std::piecewise_construct_t, std::tuple<Args1...> x, std::tuple<Args2...> y ); | (2) | (until C++20) |
| template< class T1, class T2 >  void construct( std::pair<T1, T2>\* p ); | (3) | (until C++20) |
| template< class T1, class T2, class U, class V >  void construct( std::pair<T1, T2>\* p, U&& x, V&& y ); | (4) | (until C++20) |
| template< class T1, class T2, class U, class V >  void construct( std::pair<T1, T2>\* p, const std::pair<U, V>& xy ); | (5) | (until C++20) |
| template< class T1, class T2, class U, class V >  void construct( std::pair<T1, T2>\* p, std::pair<U, V>&& xy ); | (6) | (until C++20) |
| Helper function templates |  |  |
| template < class T, class... Args >  std::tuple</\* see below \*/> /\*concat-args\*/( std::tuple<Args...>&& tup ); | (7) | (exposition only\*)  (until C++20) |
|  |  |  |

Constructs an object in allocated, but not initialized storage pointed to by p using the outer allocator and the provided constructor arguments. If the object is of a type that itself uses allocators, or if it is std::pair(until C++20), passes the inner allocator down to the constructed object.

1) Constructs an object of type `T` by uses-allocator construction at the uninitialized memory location indicated by p using the outermost allocator.

|  |  |
| --- | --- |
| Given std::uses_allocator<T, inner_allocator_type>::value as uses_inner:   - If uses_inner is false and std::is_constructible<T, Args...>::value is true, calls `outermost-construct` ﻿(p, std::forward<Args>(args)...). - Otherwise, if uses_inner and std::is_constructible<T, std::allocator_arg_t,                       inner_allocator_type&,                       Args...>::value are both true, calls `outermost-construct` ﻿(p, std::allocator_arg, inner_allocator(), std::forward<Args>(args)...). - Otherwise, if uses_inner and std::is_constructible<T, Args..., inner_allocator_type&>::value are both true, calls `outermost-construct` ﻿(p, std::forward<Args>(args)..., inner_allocator()). - Otherwise, the program is ill-formed.   This overload participates in overload resolution only if `T` is not a specialization of std::pair. | (until C++20) |
| Equivalent to  std::apply  (  p, this  {  `outermost-construct`  (p, std::forward<decltype(newargs)>(newargs)...);  },  std::uses_allocator_construction_args  (inner_allocator(), std::forward<Args>(args)...)  ); . | (since C++20) |

2-6) Constructs a std::pair object by uses-allocator construction at the uninitialized memory location indicated by p using the outermost allocator.2) Let xprime be `concat-args` ﻿<T1>(std::move(x)), yprime be `concat-args` ﻿<T2>(std::move(y)), calls `outermost-construct` ﻿(p, std::piecewise_construct, std::move(xprime), std::move(yprime)).3) Equivalent to construct(p, std::piecewise_construct, std::tuple<>(), std::tuple<>());.4-6) Equivalent to construct(p, std::piecewise_construct,  
          std::forward_as_tuple(xarg), std::forward_as_tuple(yarg));, where xarg and yarg are defined as follows:

| Overload | xarg | yarg |
| --- | --- | --- |
| (4) | std::forward<U>(x) | std::forward<V>(y) |
| (5) | xy.first | xy.second |
| (6) | std::forward<U>(xy.first) | std::forward<V>(xy.second) |

7) Merges the arguments contained in tup and additional arguments required by uses-allocator construction of an object of type `T`. Given std::uses_allocator<T, inner_allocator_type>::value as uses_inner:

- If uses_inner is false and std::is_constructible<T, Args...>::value is true, returns std::tuple<Args&&...>(std::move(tup)).
- Otherwise, if uses_inner and std::is_constructible<T, std::allocator_arg_t,  
                        inner_allocator_type&,  
                        Args...>::value are both true, returns std::tuple_cat(std::tuple<std::allocator_arg_t, inner_allocator_type&>  
                     (std::allocator_arg, inner_allocator()),  
                 std::tuple<Args&&...>(std::move(tup))).
- Otherwise, if uses_inner and std::is_constructible<T, Args..., inner_allocator_type&>::value are both true, returns std::tuple_cat(std::tuple<Args&&...>(std::move(tup)),  
                 std::tuple<inner_allocator_type&>(inner_allocator()).
- Otherwise, the program is ill-formed.

### Parameters

|  |  |  |
| --- | --- | --- |
| p | - | pointer to allocated, but not initialized storage |
| args | - | the constructor arguments to pass to the constructor of `T` |
| x | - | the constructor arguments to pass to the constructor of `T1` |
| y | - | the constructor arguments to pass to the constructor of `T2` |
| xy | - | the pair whose two members are the constructor arguments for `T1` and `T2` |
| tup | - | the arguments to be merged |

### Notes

This function is called (through std::allocator_traits) by any allocator-aware object, such as std::vector, that was given a std::scoped_allocator_adaptor as the allocator to use. Since `inner_allocator_type` is itself a specialization of std::scoped_allocator_adaptor, this function will also be called when the allocator-aware objects constructed through this function start constructing their own members.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2203 | C++11 | inner allocators were obtained by value-initializing an `inner_allocator_type` object | obtained by calling `inner_allocator()` |
| LWG 2511 (P0475R1) | C++11 | `concat-args` might copy elements of std::tuples | eliminated all element copy operations |
| LWG 2586 | C++11 | only constructions from `inner_allocator_type` rvalues were checked | checks constructions from non-const `inner_allocator_type` lvalues instead |
| LWG 2975 | C++11 | overload (1) was not constrained | constrained to refuse std::pair |

### See also

|  |  |
| --- | --- |
| construct[static] | constructs an object in the allocated storage   (function template) |
| construct(until C++20) | constructs an object in allocated storage   (public member function of `std::allocator<T>`) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/memory/scoped_allocator_adaptor/construct&oldid=177662>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 November 2024, at 16:44.