# std::stack<T,Container>::push

From cppreference.com
< cpp‎ | container‎ | stack
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

`std::stack`

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| stack::stack | | | | |
| stack::~stack | | | | |
| stack::operator= | | | | |
| Element access | | | | |
| stack::top | | | | |
| Capacity | | | | |
| stack::empty | | | | |
| stack::size | | | | |
| Modifiers | | | | |
| ****stack::push**** | | | | |
| stack::push_range(C++23) | | | | |
| stack::emplace(C++11) | | | | |
| stack::pop | | | | |
| stack::swap(C++11) | | | | |
| Non-member functions | | | | |
| swap(std::stack)(C++11) | | | | |
| operator==operator!=operator<operator>operator<=operator>=operator<=>(C++20) | | | | |
| Helper classes | | | | |
| uses_allocator<std::stack>(C++11) | | | | |
| formatter<std::stack>(C++23) | | | | |
| Deduction guides(C++17) | | | | |

|  |  |  |
| --- | --- | --- |
| void push( const value_type& value ); | (1) |  |
| void push( value_type&& value ); | (2) | (since C++11) |
|  |  |  |

Pushes the given element value to the top of the stack.

1) Equivalent to: c.push_back(value).2) Equivalent to: c.push_back(std::move(value)).

### Parameters

|  |  |  |
| --- | --- | --- |
| value | - | the value of the element to push |

### Return value

(none)

### Complexity

Equal to the complexity of Container::push_back.

### Example

This program implements the BrainHack DSL, when the use of std::stack is an idiomatic way to process paired brackets.

Run this code

```
#include <array>
#include <cstdint>
#include <iostream>
#include <map>
#include <stack>
#include <stdexcept>
#include <string_view>
 
class BrainHackInterpreter
{
    std::map<unsigned, unsigned> open_brackets, close_brackets;
    std::array<std::uint8_t, 32768> data_{0};
    unsigned program_{0};
    int pos_{0};
 
    void collect_brackets(const std::string_view program)
    {
        std::stack<unsigned> brackets_stack;
 
        for (auto pos{0U}; pos != program.length(); ++pos)
        {
            if (const char c{program[pos]}; '[' == c)
                brackets_stack.push(pos);
            else if (']' == c)
            {
                if (brackets_stack.empty())
                    throw std::runtime_error("Brackets [] do not match!");
                else
                {
                    open_brackets[brackets_stack.top()] = pos;
                    close_brackets[pos] = brackets_stack.top();
                    brackets_stack.pop();
                }
            }
        }
 
        if (!brackets_stack.empty())
            throw std::runtime_error("Brackets [] do not match!");
    }
 
    void check_data_pos(int pos)
    {
        if (pos < 0 or static_cast<int>(data_.size()) <= pos)
            throw std::out_of_range{"Data pointer out of bound!"};
    }
 
public:
    BrainHackInterpreter(const std::string_view program)
    {
        for (collect_brackets(program); program_ < program.length(); ++program_)
            switch (program[program_])
            {
                case '<':
                    check_data_pos(--pos_);
                    break;
                case '>':
                    check_data_pos(++pos_);
                    break;
                case '-':
                    --data_[pos_];
                    break;
                case '+':
                    ++data_[pos_];
                    break;
                case '.':
                    std::cout << data_[pos_];
                    break;
                case ',':
                    std::cin >> data_[pos_];
                    break;
                case '[':
                    if (data_[pos_] == 0)
                        program_ = open_brackets[program_];
                    break;
                case ']':
                    if (data_[pos_] != 0)
                        program_ = close_brackets[program_];
                    break;
            }
    }
};
 
int main()
{
    BrainHackInterpreter
    {
        "++++++++[>++>>++>++++>++++<<<<<-]>[<+++>>+++<-]>[<+"
        "+>>>+<<-]<[>+>+<<-]>>>--------.<<+++++++++.<<----.>"
        ">>>>.<<<------.>..++.<++.+.-.>.<.>----.<--.++.>>>+."
    };
    std::cout << '\n';
}

```

Output:

```
Hi, cppreference!

```

### See also

|  |  |
| --- | --- |
| emplace(C++11) | constructs element in-place at the top   (public member function) |
| pop | removes the top element   (public member function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/container/stack/push&oldid=122472>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 15 September 2020, at 04:37.