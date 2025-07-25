# std::deque<T,Allocator>::shrink_to_fit

From cppreference.com
< cpp‎ | container‎ | deque
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

std::deque

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member types | | | | |
| Member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | deque::deque | | | | | | deque::~deque | | | | | | deque::operator= | | | | | | deque::assign | | | | | | deque::assign_range(C++23) | | | | | | deque::get_allocator | | | | | | Element access | | | | | | deque::at | | | | | | [deque::operator[]](operator_at.html "cpp/container/deque/operator at") | | | | | | deque::front | | | | | | deque::back | | | | | | Iterators | | | | | | deque::begindeque::cbegin(C++11) | | | | | | deque::enddeque::cend(C++11) | | | | | | deque::rbegindeque::crbegin(C++11) | | | | | | deque::renddeque::crend(C++11) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Capacity | | | | | | deque::empty | | | | | | deque::size | | | | | | deque::max_size | | | | | | ****deque::shrink_to_fit****(DR\*) | | | | | | Modifiers | | | | | | deque::clear | | | | | | deque::insert | | | | | | deque::insert_range(C++23) | | | | | | deque::emplace | | | | | | deque::erase | | | | | | deque::push_front | | | | | | deque::emplace_front(C++11) | | | | | | deque::prepend_range(C++23) | | | | | | deque::pop_front | | | | | | deque::push_back | | | | | | deque::emplace_back(C++11) | | | | | | deque::append_range(C++23) | | | | | | deque::pop_back | | | | | | deque::resize | | | | | | deque::swap | | | | | |
| Non-member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator==operator<=>(C++20) | | | | | | swap(std::deque) | | | | | | erase(std::deque)erase_if(std::deque)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | operator!=operator<operator>operator<=operator>=(until C++20)(until C++20)(until C++20)(until C++20)(until C++20) | | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| void shrink_to_fit(); |  |  |
|  |  |  |

Requests the removal of unused capacity.

It is a non-binding request to reduce the memory usage without changing the size of the sequence. It depends on the implementation whether the request is fulfilled.

All iterators (including the `end()` iterator) and all references to the elements are invalidated.

|  |  |
| --- | --- |
| If `T` is not MoveInsertable into std::deque<T, Allocator>, the behavior is undefined. | (since C++11) |

### Complexity

At most linear in the size of the container.

|  |  |
| --- | --- |
| Exceptions If an exception is thrown other than by the move constructor of a non-CopyInsertable `T`, there are no effects. | (since C++11) |

### Notes

In libstdc++, `shrink_to_fit()` is not available in C++98 mode.

### Example

Run this code

```
#include <cstddef>
#include <deque>
#include <iostream>
#include <new>
 
// Minimal C++11 allocator with debug output.
template<class Tp>
struct NAlloc
{
    typedef Tp value_type;
 
    NAlloc() = default;
 
    template<class T> NAlloc(const NAlloc<T>&) {}
 
    Tp* allocate(std::size_t n)
    {
        n *= sizeof(Tp);
        std::cout << "allocating " << n << " bytes\n";
        return static_cast<Tp*>(::operator new(n));
    }
 
    void deallocate(Tp* p, std::size_t n)
    {
        std::cout << "deallocating " << n*sizeof*p << " bytes\n";
        ::operator delete(p);
    }
};
template<class T, class U>
bool operator==(const NAlloc<T>&, const NAlloc<U>&) { return true; }
template<class T, class U>
bool operator!=(const NAlloc<T>&, const NAlloc<U>&) { return false; }
 
int main()
{
    // std::queue has no capacity() function (like std::vector).
    // Because of this, we use a custom allocator to show the
    // working of shrink_to_fit.
 
    std::cout << "Default-construct deque:\n";
    std::deque<int, NAlloc<int>> deq;
 
    std::cout << "\nAdd 300 elements:\n";
    for (int i = 1000; i < 1300; ++i)
        deq.push_back(i);
 
    std::cout << "\nPop 100 elements:\n";
    for (int i = 0; i < 100; ++i)
        deq.pop_front();
 
    std::cout << "\nRun shrink_to_fit:\n";
    deq.shrink_to_fit();
 
    std::cout << "\nDestroy deque as it goes out of scope:\n";
}

```

Possible output:

```
Default-construct deque:
allocating 64 bytes
allocating 512 bytes
 
Add 300 elements:
allocating 512 bytes
allocating 512 bytes
 
Pop 100 elements:
 
Run shrink_to_fit:
allocating 64 bytes
allocating 512 bytes
allocating 512 bytes
deallocating 512 bytes
deallocating 512 bytes
deallocating 512 bytes
deallocating 64 bytes
 
Destroy deque as it goes out of scope:
deallocating 512 bytes
deallocating 512 bytes
deallocating 64 bytes

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 850 | C++98 | `std::deque` lacked explicit shrink-to-fit operations | provided |
| LWG 2033 | C++98 C++11 | 1. the complexity requirement was missing (C++98) 2. `T` was not required to be MoveInsertable (C++11) | 1. added 2. required |
| LWG 2223 | C++98 C++11 | 1. references, pointers, and iterators were not invalidated (C++98) 2. there was no exception safety guarantee (C++11) | 1. they may be invalidated 2. added |

### See also

|  |  |
| --- | --- |
| size | returns the number of elements   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/deque/shrink_to_fit&oldid=135179>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 11 November 2021, at 17:52.