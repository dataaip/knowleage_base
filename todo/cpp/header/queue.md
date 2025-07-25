# Standard library header <queue>

From cppreference.com
< cpp‎ | header
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

Standard library headers

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | ****<queue>**** | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the containers library.

|  |  |
| --- | --- |
| Includes | |
| <compare>(C++20) | Three-way comparison operator support |
| <initializer_list>(C++11) | std::initializer_list class template |
| Classes | |
| queue | adapts a container to provide queue (FIFO data structure)   (class template) |
| priority_queue | adapts a container to provide priority queue   (class template) |
| std::uses_allocator<std::queue>(C++11) | specializes the std::uses_allocator type trait   (class template specialization) |
| std::uses_allocator<std::priority_queue>(C++11) | specializes the std::uses_allocator type trait   (class template specialization) |
| Functions | |
| operator==operator!=operator<operator<=operator>operator>=operator<=>(C++20) | lexicographically compares the values of two `queue`s   (function template) |
| std::swap(std::queue)(C++11) | specializes the std::swap algorithm   (function template) |
| std::swap(std::priority_queue)(C++11) | specializes the std::swap algorithm   (function template) |

### Synopsis

```
#include <compare>
#include <initializer_list>
 
namespace std {
  // class template queue
  template<class T, class Container = deque<T>>
  class queue;
 
  template<class T, class Container>
  bool operator==(const queue<T, Container>& x, const queue<T, Container>& y);
  template<class T, class Container>
  bool operator!=(const queue<T, Container>& x, const queue<T, Container>& y);
  template<class T, class Container>
  bool operator<(const queue<T, Container>& x, const queue<T, Container>& y);
  template<class T, class Container>
  bool operator>(const queue<T, Container>& x, const queue<T, Container>& y);
  template<class T, class Container>
  bool operator<=(const queue<T, Container>& x, const queue<T, Container>& y);
  template<class T, class Container>
  bool operator>=(const queue<T, Container>& x, const queue<T, Container>& y);
  template<class T, three_way_comparable Container>
  compare_three_way_result_t<Container> operator<=>(const queue<T, Container>& x,
                                                    const queue<T, Container>& y);
 
  template<class T, class Container>
  void swap(queue<T, Container>& x, queue<T, Container>& y) noexcept(noexcept(x.swap(y)));
  template<class T, class Container, class Alloc>
  struct uses_allocator<queue<T, Container>, Alloc>;
 
  // formatter specialization for queue
  template<class CharT, class T, formattable<CharT> Container>
  struct formatter<queue<T, Container>, CharT>;
 
  // class template priority_queue
  template<class T,
           class Container = vector<T>,
           class Compare   = less<typename Container::value_type>>
  class priority_queue;
 
  template<class T, class Container, class Compare>
  void swap(priority_queue<T, Container, Compare>& x,
            priority_queue<T, Container, Compare>& y) noexcept(noexcept(x.swap(y)));
  template<class T, class Container, class Compare, class Alloc>
  struct uses_allocator<priority_queue<T, Container, Compare>, Alloc>;
 
  // formatter specialization for priority_queue
  template<class CharT, class T, formattable<CharT> Container, class Compare>
  struct formatter<priority_queue<T, Container, Compare>, CharT>;
}

```

#### Class template std::queue

```
namespace std {
  template<class T, class Container = deque<T>>
  class queue
  {
  public:
    using value_type      = typename Container::value_type;
    using reference       = typename Container::reference;
    using const_reference = typename Container::const_reference;
    using size_type       = typename Container::size_type;
    using container_type  = Container;
 
  protected:
    Container c;
 
  public:
    queue()
      : queue(Container())
    {
    }
    explicit queue(const Container&);
    explicit queue(Container&&);
    template<class InputIter>
    queue(InputIter first, InputIter last);
    template<container-compatible-range<T> R>
    queue(from_range_t, R&& rg);
    template<class Alloc>
    explicit queue(const Alloc&);
    template<class Alloc>
    queue(const Container&, const Alloc&);
    template<class Alloc>
    queue(Container&&, const Alloc&);
    template<class Alloc>
    queue(const queue&, const Alloc&);
    template<class Alloc>
    queue(queue&&, const Alloc&);
    template<class InputIter, class Alloc>
    queue(InputIter first, InputIter last, const Alloc&);
    template<container-compatible-range<T> R, class Alloc>
    queue(from_range_t, R&& rg, const Alloc&);
 
    bool empty() const { return c.empty(); }
    size_type size() const { return c.size(); }
    reference front() { return c.front(); }
    const_reference front() const { return c.front(); }
    reference back() { return c.back(); }
    const_reference back() const { return c.back(); }
    void push(const value_type& x) { c.push_back(x); }
    void push(value_type&& x) { c.push_back(std::move(x)); }
    template<container-compatible-range<T> R>
    void push_range(R&& rg);
    template<class... Args>
    decltype(auto) emplace(Args&&... args)
    {
      return c.emplace_back(std::forward<Args>(args)...);
    }
    void pop() { c.pop_front(); }
    void swap(queue& q) noexcept(is_nothrow_swappable_v<Container>)
    {
      using std::swap;
      swap(c, q.c);
    }
  };
 
  template<class Container>
  queue(Container) -> queue<typename Container::value_type, Container>;
 
  template<class InputIter>
  queue(InputIter, InputIter) -> queue</*iter-value-type*/<InputIter>>;
 
  template<ranges::input_range R>
  queue(from_range_t, R&&) -> queue<ranges::range_value_t<R>>;
 
  template<class Container, class Allocator>
  queue(Container, Allocator) -> queue<typename Container::value_type, Container>;
 
  template<class InputIter, class Allocator>
  queue(InputIter, InputIter, Allocator)
    -> queue</*iter-value-type*/<InputIter>,
             deque</*iter-value-type*/<InputIter>, Allocator>>;
 
  template<ranges::input_range R, class Allocator>
  queue(from_range_t, R&&, Allocator)
    -> queue<ranges::range_value_t<R>, deque<ranges::range_value_t<R>, Allocator>>;
 
  template<class T, class Container, class Alloc>
  struct uses_allocator<queue<T, Container>, Alloc>
    : uses_allocator<Container, Alloc>::type
  {};
}

```

#### Class template std::priority_queue

```
namespace std {
  template<class T,
           class Container = vector<T>,
           class Compare   = less<typename Container::value_type>>
  class priority_queue
  {
  public:
    using value_type      = typename Container::value_type;
    using reference       = typename Container::reference;
    using const_reference = typename Container::const_reference;
    using size_type       = typename Container::size_type;
    using container_type  = Container;
    using value_compare   = Compare;
 
  protected:
    Container c;
    Compare comp;
 
  public:
    priority_queue()
      : priority_queue(Compare())
    {
    }
    explicit priority_queue(const Compare& x)
      : priority_queue(x, Container())
    {
    }
    priority_queue(const Compare& x, const Container&);
    priority_queue(const Compare& x, Container&&);
    template<class InputIter>
    priority_queue(InputIter first, InputIter last, const Compare& x = Compare());
    template<class InputIter>
    priority_queue(InputIter first, InputIter last, const Compare& x, const Container&);
    template<class InputIter>
    priority_queue(InputIter first, InputIter last, const Compare& x, Container&&);
    template<container-compatible-range<T> R>
    priority_queue(from_range_t, R&& rg, const Compare& x = Compare());
    template<class Alloc>
    explicit priority_queue(const Alloc&);
    template<class Alloc>
    priority_queue(const Compare&, const Alloc&);
    template<class Alloc>
    priority_queue(const Compare&, const Container&, const Alloc&);
    template<class Alloc>
    priority_queue(const Compare&, Container&&, const Alloc&);
    template<class Alloc>
    priority_queue(const priority_queue&, const Alloc&);
    template<class Alloc>
    priority_queue(priority_queue&&, const Alloc&);
    template<class InputIter, class Alloc>
    priority_queue(InputIter, InputIter, const Alloc&);
    template<class InputIter, class Alloc>
    priority_queue(InputIter, InputIter, const Compare&, const Alloc&);
    template<class InputIter, class Alloc>
    priority_queue(InputIter, InputIter, const Compare&, const Container&, const Alloc&);
    template<class InputIter, class Alloc>
    priority_queue(InputIter, InputIter, const Compare&, Container&&, const Alloc&);
    template<container-compatible-range<T> R, class Alloc>
    priority_queue(from_range_t, R&& rg, const Compare&, const Alloc&);
    template<container-compatible-range<T> R, class Alloc>
    priority_queue(from_range_t, R&& rg, const Alloc&);
 
    bool empty() const { return c.empty(); }
    size_type size() const { return c.size(); }
    const_reference top() const { return c.front(); }
    void push(const value_type& x);
    void push(value_type&& x);
    template<container-compatible-range<T> R>
    void push_range(R&& rg);
    template<class... Args>
    void emplace(Args&&... args);
    void pop();
    void swap(priority_queue& q) noexcept(
      is_nothrow_swappable_v<Container>&& is_nothrow_swappable_v<Compare>)
    {
      using std::swap;
      swap(c, q.c);
      swap(comp, q.comp);
    }
  };
 
  template<class Compare, class Container>
  priority_queue(Compare, Container)
    -> priority_queue<typename Container::value_type, Container, Compare>;
 
  template<class InputIter,
           class Compare   = less</*iter-value-type*/<InputIter>>,
           class Container = vector</*iter-value-type*/<InputIter>>>
  priority_queue(InputIter, InputIter, Compare = Compare(), Container = Container())
    -> priority_queue</*iter-value-type*/<InputIter>, Container, Compare>;
 
  template<ranges::input_range R, class Compare = less<ranges::range_value_t<R>>>
  priority_queue(from_range_t, R&&, Compare = Compare())
    -> priority_queue<ranges::range_value_t<R>,
                      vector<ranges::range_value_t<R>>,
                      Compare>;
 
  template<class Compare, class Container, class Allocator>
  priority_queue(Compare, Container, Allocator)
    -> priority_queue<typename Container::value_type, Container, Compare>;
 
  template<class InputIter, class Allocator>
  priority_queue(InputIter, InputIter, Allocator)
    -> priority_queue</*iter-value-type*/<InputIter>,
                      vector</*iter-value-type*/<InputIter>, Allocator>,
                      less</*iter-value-type*/<InputIter>>>;
 
  template<class InputIter, class Compare, class Allocator>
  priority_queue(InputIter, InputIter, Compare, Allocator)
    -> priority_queue</*iter-value-type*/<InputIter>,
                      vector</*iter-value-type*/<InputIter>, Allocator>,
                      Compare>;
 
  template<class InputIter, class Compare, class Container, class Allocator>
  priority_queue(InputIter, InputIter, Compare, Container, Allocator)
    -> priority_queue<typename Container::value_type, Container, Compare>;
 
  template<ranges::input_range R, class Compare, class Allocator>
  priority_queue(from_range_t, R&&, Compare, Allocator)
    -> priority_queue<ranges::range_value_t<R>,
                      vector<ranges::range_value_t<R>, Allocator>,
                      Compare>;
 
  template<ranges::input_range R, class Allocator>
  priority_queue(from_range_t, R&&, Allocator)
    -> priority_queue<ranges::range_value_t<R>,
                      vector<ranges::range_value_t<R>, Allocator>>;
 
  // no equality is provided
 
  template<class T, class Container, class Compare, class Alloc>
  struct uses_allocator<priority_queue<T, Container, Compare>, Alloc>
    : uses_allocator<Container, Alloc>::type
  {};
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/queue&oldid=164387>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 November 2023, at 03:54.