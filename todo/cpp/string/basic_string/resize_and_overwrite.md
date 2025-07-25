# std::basic_string<CharT,Traits,Allocator>::resize_and_overwrite

From cppreference.com
< cpp‎ | string‎ | basic string
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

Strings library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Classes | | | | |
| basic_string | | | | |
| basic_string_view(C++17) | | | | |
| char_traits | | | | |

std::basic_string

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Member functions | | | | | | basic_string::basic_string | | | | | | basic_string::~basic_string | | | | | | basic_string::operator= | | | | | | basic_string::assign | | | | | | basic_string::assign_range(C++23) | | | | | | basic_string::get_allocator | | | | | | Element access | | | | | | basic_string::at | | | | | | [basic_string::operator[]](operator_at.html "cpp/string/basic string/operator at") | | | | | | basic_string::front(DR\*) | | | | | | basic_string::back(DR\*) | | | | | | basic_string::data | | | | | | basic_string::c_str | | | | | | basic_string::operator  basic_string_view(C++17) | | | | | | Iterators | | | | | | basic_string::beginbasic_string::cbegin(C++11) | | | | | | basic_string::endbasic_string::cend(C++11) | | | | | | basic_string::rbeginbasic_string::crbegin(C++11) | | | | | | basic_string::rendbasic_string::crend(C++11) | | | | | | Search | | | | | | basic_string::find | | | | | | basic_string::rfind | | | | | | basic_string::find_first_of | | | | | | basic_string::find_first_not_of | | | | | | basic_string::find_last_of | | | | | | basic_string::find_last_not_of | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Modifiers | | | | | | basic_string::clear | | | | | | basic_string::insert | | | | | | basic_string::insert_range(C++23) | | | | | | basic_string::erase | | | | | | basic_string::push_back | | | | | | basic_string::pop_back(DR\*) | | | | | | basic_string::append | | | | | | basic_string::append_range(C++23) | | | | | | basic_string::operator+= | | | | | | basic_string::replace | | | | | | basic_string::replace_with_range(C++23) | | | | | | basic_string::copy | | | | | | basic_string::resize | | | | | | ****basic_string::resize_and_overwrite****(C++23) | | | | | | basic_string::swap | | | | | | Capacity | | | | | | basic_string::empty | | | | | | basic_string::sizebasic_string::length | | | | | | basic_string::max_size | | | | | | basic_string::reserve | | | | | | basic_string::capacity | | | | | | basic_string::shrink_to_fit(DR\*) | | | | | | Operations | | | | | | basic_string::compare | | | | | | basic_string::starts_with(C++20) | | | | | | basic_string::ends_with(C++20) | | | | | | basic_string::contains(C++23) | | | | | | basic_string::substr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constants | | | | | | basic_string::npos | | | | | | Non-member functions | | | | | | operator+ | | | | | | swap(std::basic_string) | | | | | | erase(std::basic_string)erase_if(std::basic_string)(C++20)(C++20) | | | | | | I/O | | | | | | operator<<operator>> | | | | | | getline | | | | | | Comparison | | | | | | operator==operator!=operator<operator>operator<=operator>=operator<=>(until C++20)(until C++20)(until C++20)(until C++20)(until C++20)(C++20) | | | | | | Numeric conversions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stoistolstoll(C++11)(C++11)(C++11) | | | | | | stoulstoull(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stofstodstold(C++11)(C++11)(C++11) | | | | | | to_string(C++11) | | | | | | to_wstring(C++11) | | | | | | | Literals | | | | | | operator""s(C++14) | | | | | | Helper classes | | | | | | hash<std::basic_string>(C++11) | | | | | | Deduction guides (C++17) | | | | | |

|  |  |  |
| --- | --- | --- |
| template< class Operation >  constexpr void resize_and_overwrite( size_type count, Operation op ); |  | (since C++23) |
|  |  |  |

Resizes the string to contain at most count characters, using the user-provided operation op to modify the possibly indeterminate contents and set the length. This avoids the cost of initializing a suitably-sized std::string when it is intended to be used as a char array to be populated by, e.g., a C API call.

This function performs the following steps:

1. Obtains contiguous storage that contains count + 1 characters, and makes its first k characters equal to the first k characters of \*this, where k is the smaller of count and the result of size() before the call to `resize_and_overwrite`. Let p denote the pointer to the first character in the storage.
   - The equality is determined as if by checking this->compare(0, k, p, k) == 0.
   - The characters in `[`p + k`,`p + count`]` may have indeterminate values.
2. Evaluates std::move(op)(p, count), let r be the return value.
3. Replaces the contents of \*this with `[`p`,`p + r`)` (which sets the length of \*this to r). Invalidates all pointers and references to the range `[`p`,`p + count`]`.

If r is not of an integer-like type, the program is ill-formed.

If any of the following conditions is satisfied, the behavior is undefined:

- std::move(op)(p, count) throws an exception.
- std::move(op)(p, count) modifies p or count.
- r is not in the range `[`​0​`,`count`]`.
- Any character in range ``p`,`p + r`)` has an indeterminate value.

Implementations are recommended to avoid unnecessary copies and allocations by, e.g., making p equal to the pointer to beginning of storage of characters allocated for \*this after the call, which can be identical to the existing storage of \*this if count is less than or equal to capacity().

### Parameters

|  |  |  |
| --- | --- | --- |
| count | - | the maximal possible new size of the string |
| op | - | the function object used for setting the new contents of the string |

### Exceptions

[std::length_error if count > max_size().
Any exceptions thrown by corresponding `Allocator`.

If an exception is thrown from std::move(op)(p, count), the behavior is undefined. Otherwise, if an exception is thrown, this function has no effect.

### Notes

`resize_and_overwrite` invalidates all iterators, pointers, and references into \*this, regardless whether reallocation occurs. Implementations may assume that the contents of the string are not aliased after the call to `resize_and_overwrite`.

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_string_resize_and_overwrite` | `202110L` | (C++23) | `std::basic_string::resize_and_overwrite` |

### Example

Link to test the example: compiler explorer.

Run this code

```
#include <algorithm>
#include <cassert>
#include <cstddef>
#include <cstring>
#include <iomanip>
#include <iostream>
#include <string>
#include <string_view>
static_assert(__cpp_lib_string_resize_and_overwrite);
 
constexpr std::string_view fruits[]{"apple", "banana", "coconut", "date", "elderberry"};
 
int main()
{
    // A simple case, append only fruits[0]. The string size will be increased.
    std::string s{"Food: "};
    s.resize_and_overwrite(16, sz = s.size() noexcept
    {
        const auto to_copy = std::min(buf_size - sz, fruits[0].size());
        std::memcpy(buf + sz, fruits[0].data(), to_copy);
        return sz + to_copy;
    });
    std::cout << "1. " << std::quoted(s) << '\n';
 
    // The size shrinking case. Note, that the user's lambda is always invoked.
    s.resize_and_overwrite(10, [](char* buf, int n) noexcept
    {
        return std::find(buf, buf + n, ':') - buf;
    });
    std::cout << "2. " << std::quoted(s) << '\n';
 
    std::cout << "3. Copy data until the buffer is full. Print data and sizes.\n";
    std::string food{"Food:"};
    const auto resize_to{27};
    std::cout << "Initially, food.size: " << food.size()
              << ", food.capacity: " << food.capacity()
              << ", resize_to: " << resize_to
              << ", food: " << std::quoted(food) << '\n';
 
    food.resize_and_overwrite
    (
        resize_to,
        food_size = food.size() noexcept -> std::size_t
        {
            // p[0]..p[n] is the assignable range
            // p[0]..p[min(n, food_size) - 1] is the readable range
            // (contents initially equal to the original string)
 
            // Debug print:
            std::cout << "In Operation(); n: " << n << '\n';
 
            // Copy fruits to the buffer p while there is enough space.
            char* first = p + food_size;
 
            for (char* const end = p + n; const std::string_view fruit : fruits)
            {
                char* last = first + fruit.size() + 1;
                if (last > end)
                    break;
                *first++ = ' ';
                std::ranges::copy(fruit, first);
                first = last;
            }
 
            const auto final_size{static_cast<std::size_t>(first - p)};
 
            // Debug print:
            std::cout << "In Operation(); final_size: " << final_size << '\n';
 
            assert(final_size <= n);
            return final_size; // Return value is the actual new length
                               // of the string, must be in range 0..n
        }
    );
 
    std::cout << "Finally, food.size: " << food.size()
              << ", food.capacity: " << food.capacity()
              << ", food: " << std::quoted(food) << '\n';
}

```

Possible output:

```
1. "Food: apple"
2. "Food"
3. Copy data until the buffer is full. Print data and sizes.
Initially, food.size: 5, food.capacity: 15, resize_to: 27, food: "Food:"
In Operation(); n: 27
In Operation(); final_size: 26
Finally, food.size: 26, food.capacity: 30, food: "Food: apple banana coconut"

```

### See also

|  |  |
| --- | --- |
| resize | changes the number of characters stored   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/string/basic_string/resize_and_overwrite&oldid=180089>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 February 2025, at 06:55.