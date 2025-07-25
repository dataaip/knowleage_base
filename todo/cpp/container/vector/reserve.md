# std::vector<T,Allocator>::reserve

From cppreference.com
< cpp‎ | container‎ | vector
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

std::vector

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | vector::vector | | | | | | vector::~vector | | | | | | vector::operator= | | | | | | vector::assign | | | | | | vector::assign_range(C++23) | | | | | | vector::get_allocator | | | | | | Element access | | | | | | [vector::operator[]](operator_at.html "cpp/container/vector/operator at") | | | | | | vector::at | | | | | | vector::data | | | | | | vector::front | | | | | | vector::back | | | | | | Iterators | | | | | | vector::beginvector::cbegin(C++11) | | | | | | vector::endvector::cend(C++11) | | | | | | vector::rbeginvector::crbegin(C++11) | | | | | | vector::rendvector::crend(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | vector::empty | | | | | | vector::size | | | | | | vector::max_size | | | | | | ****vector::reserve**** | | | | | | vector::capacity | | | | | | vector::shrink_to_fit(DR\*) | | | | | | Modifiers | | | | | | vector::clear | | | | | | vector::erase | | | | | | vector::insert | | | | | | vector::insert_range(C++23) | | | | | | vector::append_range(C++23) | | | | | | vector::emplace(C++11) | | | | | | vector::emplace_back(C++11) | | | | | | vector::push_back | | | | | | vector::pop_back | | | | | | vector::resize | | | | | | vector::swap | | | | | |  | | | | | |  | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::vector) | | | | | | erase(std::vector)erase_if(std::vector)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| void reserve( size_type new_cap ); |  | (constexpr since C++20) |
|  |  |  |

Increase the capacity of the vector (the total number of elements that the vector can hold without requiring reallocation) to a value that's greater or equal to new_cap. If new_cap is greater than the current capacity(), new storage is allocated, otherwise the function does nothing.

`reserve()` does not change the size of the vector.

If new_cap is greater than capacity(), all iterators (including the `end()` iterator) and all references to the elements are invalidated. Otherwise, no iterators or references are invalidated.

After a call to `reserve()`, insertions will not trigger reallocation unless the insertion would make the size of the vector greater than the value of capacity().

### Parameters

|  |  |  |
| --- | --- | --- |
| new_cap | - | new capacity of the vector, in number of elements |
| Type requirements | | |
| -`T` must meet the requirements of MoveInsertable into \*this. (since C++11) | | |

### Return value

(none)

### Exceptions

- std::length_error if new_cap > max_size().
- Any exception thrown by `Allocator::allocate()` (typically std::bad_alloc).

If an exception is thrown, this function has no effect (strong exception guarantee).

|  |  |
| --- | --- |
| If `T`'s move constructor is not noexcept and T is not CopyInsertable into \*this, vector will use the throwing move constructor. If it throws, the guarantee is waived and the effects are unspecified. | (since C++11) |

### Complexity

At most linear in the size() of the container.

### Notes

Correctly using `reserve()` can prevent unnecessary reallocations, but inappropriate uses of `reserve()` (for instance, calling it before every push_back() call) may actually increase the number of reallocations (by causing the capacity to grow linearly rather than exponentially) and result in increased computational complexity and decreased performance. For example, a function that receives an arbitrary vector by reference and appends elements to it should usually **not** call `reserve()` on the vector, since it does not know of the vector's usage characteristics.

When inserting a range, the range version of insert() is generally preferable as it preserves the correct capacity growth behavior, unlike `reserve()` followed by a series of push_back()s.

`reserve()` cannot be used to reduce the capacity of the container; to that end shrink_to_fit() is provided.

### Example

Run this code

```
#include <cstddef>
#include <iostream>
#include <new>
#include <vector>
 
// minimal C++11 allocator with debug output
template<class Tp>
struct NAlloc
{
    typedef Tp value_type;
 
    NAlloc() = default;
    template<class T>
    NAlloc(const NAlloc<T>&) {}
 
    Tp* allocate(std::size_t n)
    {
        n *= sizeof(Tp);
        Tp* p = static_cast<Tp*>(::operator new(n));
        std::cout << "allocating " << n << " bytes @ " << p << '\n';
        return p;
    }
 
    void deallocate(Tp* p, std::size_t n)
    {
        std::cout << "deallocating " << n * sizeof *p << " bytes @ " << p << "\n\n";
        ::operator delete(p);
    }
};
 
template<class T, class U>
bool operator==(const NAlloc<T>&, const NAlloc<U>&) { return true; }
 
template<class T, class U>
bool operator!=(const NAlloc<T>&, const NAlloc<U>&) { return false; }
 
int main()
{
    constexpr int max_elements = 32;
 
    std::cout << "using reserve: \n";
    {
        std::vector<int, NAlloc<int>> v1;
        v1.reserve(max_elements); // reserves at least max_elements * sizeof(int) bytes
 
        for (int n = 0; n < max_elements; ++n)
            v1.push_back(n);
    }
 
    std::cout << "not using reserve: \n";
    {
        std::vector<int, NAlloc<int>> v1;
 
        for (int n = 0; n < max_elements; ++n)
        {
            if (v1.size() == v1.capacity())
                std::cout << "size() == capacity() == " << v1.size() << '\n';
            v1.push_back(n);
        }
    }
}

```

Possible output:

```
using reserve: 
allocating 128 bytes @ 0xa6f840
deallocating 128 bytes @ 0xa6f840
 
not using reserve: 
size() == capacity() == 0
allocating 4 bytes @ 0xa6f840
 
size() == capacity() == 1
allocating 8 bytes @ 0xa6f860
deallocating 4 bytes @ 0xa6f840
 
size() == capacity() == 2
allocating 16 bytes @ 0xa6f840
deallocating 8 bytes @ 0xa6f860
 
size() == capacity() == 4
allocating 32 bytes @ 0xa6f880
deallocating 16 bytes @ 0xa6f840
 
size() == capacity() == 8
allocating 64 bytes @ 0xa6f8b0
deallocating 32 bytes @ 0xa6f880
 
size() == capacity() == 16
allocating 128 bytes @ 0xa6f900
deallocating 64 bytes @ 0xa6f8b0
 
deallocating 128 bytes @ 0xa6f900

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 329 | C++98 | reallocation might be triggered if an insertion makes the size of the vector greater than the size specified in the most recent call to `reserve()` | only triggers if the size of the vector becomes greater than capacity() |
| LWG 2033 | C++11 | `T` was not required to be MoveInsertable | required |

### See also

|  |  |
| --- | --- |
| capacity | returns the number of elements that can be held in currently allocated storage   (public member function) |
| max_size | returns the maximum possible number of elements   (public member function) |
| resize | changes the number of elements stored   (public member function) |
| shrink_to_fit(DR\*) | reduces memory usage by freeing unused memory   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/vector/reserve&oldid=171517>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 May 2024, at 15:05.