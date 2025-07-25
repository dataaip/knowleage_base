# std::allocate_shared, std::allocate_shared_for_overwrite

From cppreference.com
< cpp‎ | memory‎ | shared ptr
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

std::shared_ptr

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| shared_ptr::shared_ptr | | | | |
| shared_ptr::~shared_ptr | | | | |
| shared_ptr::operator= | | | | |
| Modifiers | | | | |
| shared_ptr::reset | | | | |
| shared_ptr::swap | | | | |
| Observers | | | | |
| shared_ptr::get | | | | |
| shared_ptr::operator\*shared_ptr::operator-> | | | | |
| [shared_ptr::operator[]](operator_at.html "cpp/memory/shared ptr/operator at")(C++17) | | | | |
| shared_ptr::use_count | | | | |
| shared_ptr::unique(until C++20\*) | | | | |
| shared_ptr::operator bool | | | | |
| shared_ptr::owner_before | | | | |
| shared_ptr::owner_hash(C++26) | | | | |
| shared_ptr::owner_equal(C++26) | | | | |
| Non-member functions | | | | |
| swap(std::shared_ptr) | | | | |
| make_sharedmake_shared_for_overwrite(C++20) | | | | |
| ****allocate_sharedallocate_shared_for_overwrite****(C++20) | | | | |
| static_pointer_castdynamic_pointer_castconst_pointer_castreinterpret_pointer_cast(C++17) | | | | |
| get_deleter | | | | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | |
| operator<< | | | | |
| atomic_xxxfunctions (until C++26\*) | | | | |
| Helper classes | | | | |
| atomic<std::shared_ptr>(C++20) | | | | |
| hash<std::shared_ptr> | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<memory>` |  |  |
| template< class T, class Alloc, class... Args >  shared_ptr<T> allocate_shared( const Alloc& alloc, Args&&... args ); | (1) | (since C++11)  (T is non-array) |
| template< class T, class Alloc >  shared_ptr<T> allocate_shared( const Alloc& alloc, std::size_t N ); | (2) | (since C++20)  (T is U[]) |
| template< class T, class Alloc >  shared_ptr<T> allocate_shared( const Alloc& alloc ); | (3) | (since C++20)  (T is U[N]) |
| template< class T, class Alloc >  shared_ptr<T> allocate_shared( const Alloc& alloc, std::size_t N, const std::remove_extent_t<T>& u ); | (4) | (since C++20)  (T is U[]) |
| template< class T, class Alloc >  shared_ptr<T> allocate_shared( const Alloc& alloc, const std::remove_extent_t<T>& u ); | (5) | (since C++20)  (T is U[N]) |
| template< class T, class Alloc >  shared_ptr<T> allocate_shared_for_overwrite( const Alloc& alloc ); | (6) | (since C++20)  (T is not U[]) |
| template< class T, class Alloc >  shared_ptr<T> allocate_shared_for_overwrite( const Alloc& alloc, std::size_t N ); | (7) | (since C++20)  (T is U[]) |
|  |  |  |

1) Constructs an object of type `T` and wraps it in a std::shared_ptr using args as the parameter list for the constructor of `T`. The object is constructed as if by the expression ::new (pv) T(v)(until C++20)std::allocator_traits<A2>::construct(a, pv, v)(since C++20), where `pv` is an internal void\* pointer to storage suitable to hold an object of type `T` and `a` is a copy of the allocator rebound to std::remove_cv_t<T>. The storage is typically larger than `sizeof(T)` in order to use one allocation for both the control block of the shared pointer and the `T` object. The std::shared_ptr constructor called by this function enables `shared_from_this` with a pointer to the newly constructed object of type `T`. All memory allocation is done using a copy of alloc, which must satisfy the Allocator requirements. This overload participates in overload resolution only if T is not an array type.2,3) Same as (1), but the object constructed is a possibly-multidimensional array whose every non-array element is initialized as if by the expression std::allocator_traits<A2>::construct(a2, pv) where `a2` of type `A2` is the copy of the allocator rebound to manage objects of type std::remove_cv_t<std::remove_all_extents_t<T>>. The overload (2) creates an array of size N along its first dimension. The array elements are initialized in ascending order of their addresses, and when their lifetime ends are destroyed in the reverse order of their original construction.4,5) Same as (2,3), but the elements of the array are initialized from the default value u. If std::remove_extent_t<T> is not itself an array type, then this is performed as if by the same allocator expression as in (1), except that the allocator is rebound to the std::remove_cv_t<std::remove_all_extents_t<T>>. Otherwise, this is performed as if by initializing every non-array element of the (possibly multidimensional) array with the corresponding element from u using the same allocator expression as in (1), except that the allocator is rebound to the type std::remove_cv_t<std::remove_all_extents_t<T>>. The overload (4) creates an array of size N along the first dimension. The array elements are initialized in ascending order of their addresses, and when their lifetime ends are destroyed in the reverse order of their original construction.6) Same as (1) if `T` is not an array type and (3) if `T` is `U[N]`, except that the created object is default-initialized.7) Same as (2), except that the individual array elements are default-initialized.

For `allocate_shared`, the object (or the individual array elements for (2-5))(since C++20) are destroyed via the expression std::allocator_traits<A2>::destroy(a, p), where `p` is a pointer to the object and `a` is a copy of the allocator passed to `allocate_shared`, rebound to the type of the object being destroyed.

|  |  |
| --- | --- |
| For `allocate_shared_for_overwrite`, the object (or individual elements if `T` is an array type) will be destroyed by p->~X(), where `p` is a pointer to the object and `X` is its type. | (since C++20) |

### Parameters

|  |  |  |
| --- | --- | --- |
| alloc | - | the Allocator to use |
| args... | - | list of arguments with which an instance of `T` will be constructed |
| N | - | array size to use |
| u | - | the initial value to initialize every element of the array |

### Return value

std::shared_ptr of an instance of type `T`.

### Exceptions

Can throw the exceptions thrown from Alloc::allocate() or from the constructor of `T`. If an exception is thrown, (1) has no effect. If an exception is thrown during the construction of the array, already-initialized elements are destroyed in reverse order(since C++20).

### Notes

Like std::make_shared, this function typically performs only one allocation, and places both the `T` object and the control block in the allocated memory block (the standard recommends but does not require this, all known implementations do this). A copy of alloc is stored as part of the control block so that it can be used to deallocate it once both shared and weak reference counts reach zero.

Unlike the `std::shared_ptr` `constructors`, `std::allocate_shared` does not accept a separate custom deleter: the supplied allocator is used for destruction of the control block and the `T` object, and for deallocation of their shared memory block.

|  |  |
| --- | --- |
| std::shared_ptr supports array types (as of C++17), but `std::allocate_shared` does not. This functionality is supported by `boost::allocate_shared`. | (until C++20) |

A constructor **enables `shared_from_this`** with a pointer ptr of type `U*` means that it determines if `U` has an unambiguous and accessible(since C++17) base class that is a specialization of std::enable_shared_from_this, and if so, the constructor evaluates 
if (ptr != nullptr && ptr->`weak_this` ﻿.expired())  
ptr->`weak_this`= std::shared_ptr<std::remove_cv_t<U>>  
(\*this, const_cast<std::remove_cv_t<U>\*>(ptr));
.

The assignment to the `weak_this` is not atomic and conflicts with any potentially concurrent access to the same object. This ensures that future calls to shared_from_this() would share ownership with the std::shared_ptr created by this raw pointer constructor.

The test ptr->`weak_this` ﻿.expired() in the code above makes sure that `weak_this` is not reassigned if it already indicates an owner. This test is required as of C++17.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_smart_ptr_for_overwrite` | `202002L` | (C++20) | Smart pointer creation with default initialization (`std::allocate_shared_for_overwrite`, std::make_shared_for_overwrite, std::make_unique_for_overwrite); overloads (6,7) |

### Example

Run this code

```
#include <cstddef>
#include <iostream>
#include <memory>
#include <memory_resource>
#include <vector>
 
class Value
{
    int i;
 
public:
    Value(int i) : i(i) { std::cout << "Value(), i = " << i << '\n'; }
    ~Value() { std::cout << "~Value(), i = " << i << '\n'; }
    void print() const { std::cout << "i = " << i << '\n'; }
};
 
int main()
{
    // Create a polymorphic allocator using the monotonic buffer resource
    std::byte buffer[sizeof(Value) * 8];
    std::pmr::monotonic_buffer_resource resource(buffer, sizeof(buffer));
    std::pmr::polymorphic_allocator<Value> allocator(&resource);
 
    std::vector<std::shared_ptr<Value>> v;
 
    for (int i{}; i != 4; ++i)
        // Use std::allocate_shared with the custom allocator
        v.emplace_back(std::allocate_shared<Value>(allocator, i));
 
    for (const auto& sp : v)
        sp->print();
 
} //< All shared pointers will automatically clean up when they go out of scope.

```

Output:

```
Value(), i = 0
Value(), i = 1
Value(), i = 2
Value(), i = 3
i = 0
i = 1
i = 2
i = 3
~Value(), i = 0
~Value(), i = 1
~Value(), i = 2
~Value(), i = 3

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs new `shared_ptr`   (public member function) |
| make_sharedmake_shared_for_overwrite(C++20) | creates a shared pointer that manages a new object   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/memory/shared_ptr/allocate_shared&oldid=176735>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 October 2024, at 16:10.