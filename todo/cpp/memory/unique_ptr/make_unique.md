# std::make_unique, std::make_unique_for_overwrite

From cppreference.com
< cpp‎ | memory‎ | unique ptr
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

std::unique_ptr

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| unique_ptr::unique_ptr | | | | |
| unique_ptr::~unique_ptr | | | | |
| unique_ptr::operator= | | | | |
| Modifiers | | | | |
| unique_ptr::release | | | | |
| unique_ptr::reset | | | | |
| unique_ptr::swap | | | | |
| Observers | | | | |
| unique_ptr::get | | | | |
| unique_ptr::get_deleter | | | | |
| unique_ptr::operator bool | | | | |
| unique_ptr::operator\*unique_ptr::operator-> | | | | |
| [unique_ptr::operator[]](operator_at.html "cpp/memory/unique ptr/operator at") | | | | |
| Non-member functions | | | | |
| ****make_uniquemake_unique_for_overwrite****(C++14)(C++20) | | | | |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(C++20) | | | | |
| operator<<(C++20) | | | | |
| swap(std::unique_ptr) | | | | |
| Helper classes | | | | |
| hash<std::unique_ptr> | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<memory>` |  |  |
|  |  |  |
| --- | --- | --- |
|  | (1) |  |
| template< class T, class... Args >  unique_ptr<T> make_unique( Args&&... args ); |  | (since C++14)  (until C++23)  (only for non-array types) |
| template< class T, class... Args >  constexpr unique_ptr<T> make_unique( Args&&... args ); |  | (since C++23)  (only for non-array types) |
|  |  |  |
| --- | --- | --- |
|  | (2) |  |
| template< class T >  unique_ptr<T> make_unique( std::size_t size ); |  | (since C++14)  (until C++23)  (only for array types with unknown bound) |
| template< class T >  constexpr unique_ptr<T> make_unique( std::size_t size ); |  | (since C++23)  (only for array types with unknown bound) |
|  |  |  |
| --- | --- | --- |
| template< class T, class... Args >  /\* unspecified \*/ make_unique( Args&&... args ) = delete; | (3) | (since C++14)  (only for array types with known bound) |
|  |  |  |
| --- | --- | --- |
|  | (4) |  |
| template< class T >  unique_ptr<T> make_unique_for_overwrite(); |  | (since C++20)  (until C++23)  (only for non-array types) |
| template< class T >  constexpr unique_ptr<T> make_unique_for_overwrite(); |  | (since C++23)  (only for non-array types) |
|  |  |  |
| --- | --- | --- |
|  | (5) |  |
| template< class T >  unique_ptr<T> make_unique_for_overwrite( std::size_t size ); |  | (since C++20)  (until C++23)  (only for array types with unknown bound) |
| template< class T >  constexpr unique_ptr<T> make_unique_for_overwrite( std::size_t size ); |  | (since C++23)  (only for array types with unknown bound) |
|  |  |  |
| --- | --- | --- |
| template< class T, class... Args >  /\* unspecified \*/ make_unique_for_overwrite( Args&&... args ) = delete; | (6) | (since C++20)  (only for array types with known bound) |
|  |  |  |

Constructs an object of type `T` and wraps it in a std::unique_ptr.

1) Constructs a non-array type `T`. The arguments args are passed to the constructor of `T`. This overload participates in overload resolution only if `T` is not an array type. The function is equivalent to:

```
unique_ptr<T>(new T(std::forward<Args>(args)...))

```

2) Constructs an array of the given dynamic size. The array elements are value-initialized. This overload participates in overload resolution only if `T` is an array of unknown bound. The function is equivalent to:

```
unique_ptr<T>(new std::remove_extent_t<T>[size]())

```

3,6) Construction of arrays of known bound is disallowed.4) Same as (1), except that the object is default-initialized. This overload participates in overload resolution only if `T` is not an array type. The function is equivalent to:

```
unique_ptr<T>(new T)

```

5) Same as (2), except that the array is default-initialized. This overload participates in overload resolution only if `T` is an array of unknown bound. The function is equivalent to:

```
unique_ptr<T>(new std::remove_extent_t<T>[size])

```

### Parameters

|  |  |  |
| --- | --- | --- |
| args | - | list of arguments with which an instance of `T` will be constructed |
| size | - | the length of the array to construct |

### Return value

std::unique_ptr of an instance of type `T`.

### Exceptions

May throw std::bad_alloc or any exception thrown by the constructor of `T`. If an exception is thrown, this function has no effect.

### Possible Implementation

| make_unique (1-3) |
| --- |
| ```text // C++14 make_unique namespace detail {     template<class>     constexpr bool is_unbounded_array_v = false;     template<class T>     constexpr bool is_unbounded_array_v<T[]> = true;       template<class>     constexpr bool is_bounded_array_v = false;     template<class T, std::size_t N>     constexpr bool is_bounded_array_v<T[N]> = true; } // namespace detail   template<class T, class... Args> std::enable_if_t<!std::is_array<T>::value, std::unique_ptr<T>> make_unique(Args&&... args) {     return std::unique_ptr<T>(new T(std::forward<Args>(args)...)); }   template<class T> std::enable_if_t<detail::is_unbounded_array_v<T>, std::unique_ptr<T>> make_unique(std::size_t n) {     return std::unique_ptr<T>(new std::remove_extent_t<T>[n]()); }   template<class T, class... Args> std::enable_if_t<detail::is_bounded_array_v<T>> make_unique(Args&&...) = delete; ``` |
| make_unique_for_overwrite (4-6) |
| ```text // C++20 make_unique_for_overwrite template<class T>     requires (!std::is_array_v<T>) std::unique_ptr<T> make_unique_for_overwrite() {     return std::unique_ptr<T>(new T); }   template<class T>     requires std::is_unbounded_array_v<T> std::unique_ptr<T> make_unique_for_overwrite(std::size_t n) {     return std::unique_ptr<T>(new std::remove_extent_t<T>[n]); }   template<class T, class... Args>     requires std::is_bounded_array_v<T> void make_unique_for_overwrite(Args&&...) = delete; ``` |

### Notes

Unlike std::make_shared (which has std::allocate_shared), `std::make_unique` does not have an allocator-aware counterpart. `allocate_unique` proposed in P0211 would be required to invent the deleter type `D` for the std::unique_ptr<T,D> it returns which would contain an allocator object and invoke both `destroy` and `deallocate` in its operator().

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_make_unique` | `201304L` | (C++14) | `std::make_unique`; overload (1) |
| `__cpp_lib_smart_ptr_for_overwrite` | `202002L` | (C++20) | Smart pointer creation with default initialization (std::allocate_shared_for_overwrite, std::make_shared_for_overwrite, `std::make_unique_for_overwrite`); overloads (4-6) |
| `__cpp_lib_constexpr_memory` | `202202L` | (C++23) | `constexpr` for overloads (1,2,4,5) |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: add more make_unique_for_overwrite() demos |

Run this code

```
#include <cstddef>
#include <iomanip>
#include <iostream>
#include <memory>
#include <utility>
 
struct Vec3
{
    int x, y, z;
 
    // Following constructor is no longer needed since C++20.
    Vec3(int x = 0, int y = 0, int z = 0) noexcept : x(x), y(y), z(z) {}
 
    friend std::ostream& operator<<(std::ostream& os, const Vec3& v)
    {
        return os << "{ x=" << v.x << ", y=" << v.y << ", z=" << v.z << " }";
    }
};
 
// Output Fibonacci numbers to an output iterator.
template<typename OutputIt>
OutputIt fibonacci(OutputIt first, OutputIt last)
{
    for (int a = 0, b = 1; first != last; ++first)
    {
        *first = b;
        b += std::exchange(a, b);
    }
    return first;
}
 
int main()
{
    // Use the default constructor.
    std::unique_ptr<Vec3> v1 = std::make_unique<Vec3>();
    // Use the constructor that matches these arguments.
    std::unique_ptr<Vec3> v2 = std::make_unique<Vec3>(0, 1, 2);
    // Create a unique_ptr to an array of 5 elements.
    std::unique_ptr<Vec3[]> v3 = std::make_unique<Vec3[]>(5);
 
    // Create a unique_ptr to an uninitialized array of 10 integers,
    // then populate it with Fibonacci numbers.
    std::unique_ptr<int[]> i1 = std::make_unique_for_overwrite<int[]>(10);
    fibonacci(i1.get(), i1.get() + 10);
 
    std::cout << "make_unique<Vec3>():      " << *v1 << '\n'
              << "make_unique<Vec3>(0,1,2): " << *v2 << '\n'
              << "make_unique<Vec3[]>(5):   ";
    for (std::size_t i = 0; i < 5; ++i)
        std::cout << std::setw(i ? 30 : 0) << v3[i] << '\n';
    std::cout << '\n';
 
    std::cout << "make_unique_for_overwrite<int[]>(10), fibonacci(...): [" << i1[0];
    for (std::size_t i = 1; i < 10; ++i)
        std::cout << ", " << i1[i];
    std::cout << "]\n";
}

```

Output:

```
make_unique<Vec3>():      { x=0, y=0, z=0 }
make_unique<Vec3>(0,1,2): { x=0, y=1, z=2 }
make_unique<Vec3[]>(5):   { x=0, y=0, z=0 }
                          { x=0, y=0, z=0 }
                          { x=0, y=0, z=0 }
                          { x=0, y=0, z=0 }
                          { x=0, y=0, z=0 }
 
make_unique_for_overwrite<int[]>(10), fibonacci(...): [1, 1, 2, 3, 5, 8, 13, 21, 34, 55]

```

### See also

|  |  |
| --- | --- |
| (constructor) | constructs a new `unique_ptr`   (public member function) |
| make_sharedmake_shared_for_overwrite(C++20) | creates a shared pointer that manages a new object   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/memory/unique_ptr/make_unique&oldid=160470>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 10 October 2023, at 10:56.