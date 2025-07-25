# std::queue<T,Container>::swap

From cppreference.com
< cpp‎ | container‎ | queue
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

`std::queue`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| queue::queue | | | | |
| queue::~queue | | | | |
| queue::operator= | | | | |
| Element access | | | | |
| queue::front | | | | |
| queue::back | | | | |
| Capacity | | | | |
| queue::empty | | | | |
| queue::size | | | | |
| Modifiers | | | | |
| queue::push | | | | |
| queue::push_range(C++23) | | | | |
| queue::emplace(C++11) | | | | |
| queue::pop | | | | |
| ****queue::swap****(C++11) | | | | |
| Non-member functions | | | | |
| swap(std::queue)(C++11) | | | | |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(C++20) | | | | |
| Helper classes | | | | |
| uses_allocator<std::queue>(C++11) | | | | |
| formatter<std::queue>(C++23) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| void swap( queue& other ) noexcept(/\* see below \*/); |  | (since C++11) |
|  |  |  |

Exchanges the contents of the container adaptor with those of `other`. Effectively calls

```
using std::swap;
swap(c, other.c);

```

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | container adaptor to exchange the contents with |

### Return value

(none)

### Exceptions

|  |  |
| --- | --- |
| noexcept specification:noexcept(noexcept(swap(c, other.c))) In the expression above, the identifier `swap` is looked up in the same manner as the one used by the C++17 std::is_nothrow_swappable trait. | (since C++11) (until C++17) |
| noexcept specification:noexcept(std::is_nothrow_swappable_v<Container>) | (since C++17) |

### Complexity

Same as underlying container (typically constant).

### Notes

Some implementations (e.g. libc++) provide the `swap` member function as an extension to pre-C++11 modes.

### Example

Run this code

```
#include <iostream>
#include <concepts>
#include <queue>
#include <string>
#include <string_view>
#include <vector>
 
template<typename Adaptor>
requires (std::ranges::input_range<typename Adaptor::container_type>)
void print(std::string_view name, const Adaptor& adaptor)
{
    struct Printer : Adaptor // to use protected Adaptor::Container c;
    {
        void print(std::string_view name) const
        {
            std::cout << name << " [" << std::size(this->c) << "]: ";
            for (auto const& elem : this->c)
                std::cout << elem << ' ';
            std::cout << '\n';
        }
    };
 
    static_cast<Printer const&>(adaptor).print(name);
}
 
int main()
{
    std::vector<std::string> v1{"1","2","3","4"},
                             v2{"Ɐ","B","Ɔ","D","Ǝ"};
 
    std::queue s1(std::move(v1));
    std::queue s2(std::move(v2));
 
    print("s1", s1);
    print("s2", s2);
 
    s1.swap(s2);
 
    print("s1", s1);
    print("s2", s2);
}

```

Output:

```
s1 [4]: 4 3 2 1
s2 [5]: Ǝ D Ɔ B Ɐ
s1 [5]: Ǝ D Ɔ B Ɐ
s2 [4]: 4 3 2 1

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 2456 | C++11 | the `noexcept` specification is ill-formed | made to work |

### See also

|  |  |
| --- | --- |
| std::swap(std::queue)(C++11) | specializes the std::swap algorithm   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/queue/swap&oldid=135389>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 November 2021, at 07:17.