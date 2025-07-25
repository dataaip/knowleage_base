# Standard library header <flat_map> (C++23)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | ****<flat_map>**** (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the containers library.

|  |  |
| --- | --- |
| Includes | |
| <compare>(C++20) | Three-way comparison operator support |
| <initializer_list>(C++11) | std::initializer_list class template |
| Classes | |
| flat_map(C++23) | adapts two containers to provide a collection of key-value pairs, sorted by unique keys   (class template) |
| flat_multimap(C++23) | adapts two containers to provide a collection of key-value pairs, sorted by keys   (class template) |
| std::uses_allocator<std::flat_map>(C++23) | specializes the std::uses_allocator type trait   (class template specialization) |
| std::uses_allocator<std::flat_multimap>(C++23) | specializes the std::uses_allocator type trait   (class template specialization) |
| Functions | |
| erase_if(std::flat_map)(C++23) | erases all elements satisfying specific criteria   (function template) |
| erase_if(std::flat_multimap)(C++23) | erases all elements satisfying specific criteria   (function template) |
| Tags | |
| sorted_uniquesorted_unique_t(C++23) | indicates that elements of a range are sorted and unique (tag) |
| sorted_equivalentsorted_equivalent_t(C++23) | indicates that elements of a range are sorted (uniqueness is not required) (tag) |

### Synopsis

```
#include <compare>
#include <initializer_list>
 
namespace std {
  // class template flat_map
  template<class Key,
           class T,
           class Compare         = less<Key>,
           class KeyContainer    = vector<Key>,
           class MappedContainer = vector<T>>
  class flat_map;
 
  struct sorted_unique_t
  {
    explicit sorted_unique_t() = default;
  };
  inline constexpr sorted_unique_t sorted_unique{};
 
  template<class Key,
           class T,
           class Compare,
           class KeyContainer,
           class MappedContainer,
           class Allocator>
  struct uses_allocator<flat_map<Key, T, Compare, KeyContainer, MappedContainer>,
                        Allocator>;
 
  // erasure for flat_map
  template<class Key,
           class T,
           class Compare,
           class KeyContainer,
           class MappedContainer,
           class Predicate>
  typename flat_map<Key, T, Compare, KeyContainer, MappedContainer>::size_type erase_if(
    flat_map<Key, T, Compare, KeyContainer, MappedContainer>& c,
    Predicate pred);
 
  // class template flat_multimap
  template<class Key,
           class T,
           class Compare         = less<Key>,
           class KeyContainer    = vector<Key>,
           class MappedContainer = vector<T>>
  class flat_multimap;
 
  struct sorted_equivalent_t
  {
    explicit sorted_equivalent_t() = default;
  };
  inline constexpr sorted_equivalent_t sorted_equivalent{};
 
  template<class Key,
           class T,
           class Compare,
           class KeyContainer,
           class MappedContainer,
           class Allocator>
  struct uses_allocator<flat_multimap<Key, T, Compare, KeyContainer, MappedContainer>,
                        Allocator>;
 
  // erasure for flat_multimap
  template<class Key,
           class T,
           class Compare,
           class KeyContainer,
           class MappedContainer,
           class Predicate>
  typename flat_multimap<Key, T, Compare, KeyContainer, MappedContainer>::size_type
  erase_if(flat_multimap<Key, T, Compare, KeyContainer, MappedContainer>& c,
           Predicate pred);
}

```

#### Class template std::flat_map

```
namespace std {
  template<class Key,
           class T,
           class Compare         = less<Key>,
           class KeyContainer    = vector<Key>,
           class MappedContainer = vector<T>>
  class flat_map
  {
  public:
    // types
    using key_type               = Key;
    using mapped_type            = T;
    using value_type             = pair<key_type, mapped_type>;
    using key_compare            = Compare;
    using reference              = pair<const key_type&, mapped_type&>;
    using const_reference        = pair<const key_type&, const mapped_type&>;
    using size_type              = size_t;
    using difference_type        = ptrdiff_t;
    using iterator               = /* implementation-defined */;
    using const_iterator         = /* implementation-defined */;
    using reverse_iterator       = std::reverse_iterator<iterator>;
    using const_reverse_iterator = std::reverse_iterator<const_iterator>;
    using key_container_type     = KeyContainer;
    using mapped_container_type  = MappedContainer;
 
    class value_compare
    {
    private:
      key_compare comp; // exposition only
      value_compare(key_compare c)
        : comp(c)
      {
      } // exposition only
 
    public:
      bool operator()(const_reference x, const_reference y) const
      {
        return comp(x.first, y.first);
      }
    };
 
    struct containers
    {
      key_container_type keys;
      mapped_container_type values;
    };
 
    // constructors
    flat_map()
      : flat_map(key_compare())
    {
    }
 
    explicit flat_map(const key_compare& comp)
      : c()
      , compare(comp)
    {
    }
 
    flat_map(key_container_type key_cont,
             mapped_container_type mapped_cont,
             const key_compare& comp = key_compare());
 
    flat_map(sorted_unique_t,
             key_container_type key_cont,
             mapped_container_type mapped_cont,
             const key_compare& comp = key_compare());
 
    template<class InputIter>
    flat_map(InputIter first, InputIter last, const key_compare& comp = key_compare())
      : c()
      , compare(comp)
    {
      insert(first, last);
    }
 
    template<class InputIter>
    flat_map(sorted_unique_t s,
             InputIter first,
             InputIter last,
             const key_compare& comp = key_compare())
      : c()
      , compare(comp)
    {
      insert(s, first, last);
    }
 
    template<container-compatible-range<value_type> R>
    flat_map(from_range_t fr, R&& rg)
      : flat_map(fr, std::forward<R>(rg), key_compare())
    {
    }
    template<container-compatible-range<value_type> R>
    flat_map(from_range_t, R&& rg, const key_compare& comp)
      : flat_map(comp)
    {
      insert_range(std::forward<R>(rg));
    }
 
    flat_map(initializer_list<value_type> il, const key_compare& comp = key_compare())
      : flat_map(il.begin(), il.end(), comp)
    {
    }
 
    flat_map(sorted_unique_t s,
             initializer_list<value_type> il,
             const key_compare& comp = key_compare())
      : flat_map(s, il.begin(), il.end(), comp)
    {
    }
 
    // constructors with allocators
 
    template<class Alloc>
    explicit flat_map(const Alloc& a);
    template<class Alloc>
    flat_map(const key_compare& comp, const Alloc& a);
    template<class Alloc>
    flat_map(const key_container_type& key_cont,
             const mapped_container_type& mapped_cont,
             const Alloc& a);
    template<class Alloc>
    flat_map(const key_container_type& key_cont,
             const mapped_container_type& mapped_cont,
             const key_compare& comp,
             const Alloc& a);
    template<class Alloc>
    flat_map(sorted_unique_t,
             const key_container_type& key_cont,
             const mapped_container_type& mapped_cont,
             const Alloc& a);
    template<class Alloc>
    flat_map(sorted_unique_t,
             const key_container_type& key_cont,
             const mapped_container_type& mapped_cont,
             const key_compare& comp,
             const Alloc& a);
    template<class Alloc>
    flat_map(const flat_map&, const Alloc& a);
    template<class Alloc>
    flat_map(flat_map&&, const Alloc& a);
    template<class InputIter, class Alloc>
    flat_map(InputIter first, InputIter last, const Alloc& a);
    template<class InputIter, class Alloc>
    flat_map(InputIter first, InputIter last, const key_compare& comp, const Alloc& a);
    template<class InputIter, class Alloc>
    flat_map(sorted_unique_t, InputIter first, InputIter last, const Alloc& a);
    template<class InputIter, class Alloc>
    flat_map(sorted_unique_t,
             InputIter first,
             InputIter last,
             const key_compare& comp,
             const Alloc& a);
    template<container-compatible-range<value_type> R, class Alloc>
    flat_map(from_range_t, R&& rg, const Alloc& a);
    template<container-compatible-range<value_type> R, class Alloc>
    flat_map(from_range_t, R&& rg, const key_compare& comp, const Alloc& a);
    template<class Alloc>
    flat_map(initializer_list<value_type> il, const Alloc& a);
    template<class Alloc>
    flat_map(initializer_list<value_type> il, const key_compare& comp, const Alloc& a);
    template<class Alloc>
    flat_map(sorted_unique_t, initializer_list<value_type> il, const Alloc& a);
    template<class Alloc>
    flat_map(sorted_unique_t,
             initializer_list<value_type> il,
             const key_compare& comp,
             const Alloc& a);
 
    flat_map& operator=(initializer_list<value_type>);
 
    // iterators
    iterator begin() noexcept;
    const_iterator begin() const noexcept;
    iterator end() noexcept;
    const_iterator end() const noexcept;
 
    reverse_iterator rbegin() noexcept;
    const_reverse_iterator rbegin() const noexcept;
    reverse_iterator rend() noexcept;
    const_reverse_iterator rend() const noexcept;
 
    const_iterator cbegin() const noexcept;
    const_iterator cend() const noexcept;
    const_reverse_iterator crbegin() const noexcept;
    const_reverse_iterator crend() const noexcept;
 
    // capacity
    bool empty() const noexcept;
    size_type size() const noexcept;
    size_type max_size() const noexcept;
 
    // element access
    mapped_type& operator[](const key_type& x);
    mapped_type& operator[](key_type&& x);
    template<class K>
    mapped_type& operator[](K&& x);
    mapped_type& at(const key_type& x);
    const mapped_type& at(const key_type& x) const;
    template<class K>
    mapped_type& at(const K& x);
    template<class K>
    const mapped_type& at(const K& x) const;
 
    // modifiers
    template<class... Args>
    pair<iterator, bool> emplace(Args&&... args);
    template<class... Args>
    iterator emplace_hint(const_iterator position, Args&&... args);
 
    pair<iterator, bool> insert(const value_type& x) { return emplace(x); }
    pair<iterator, bool> insert(value_type&& x) { return emplace(std::move(x)); }
    iterator insert(const_iterator position, const value_type& x)
    {
      return emplace_hint(position, x);
    }
    iterator insert(const_iterator position, value_type&& x)
    {
      return emplace_hint(position, std::move(x));
    }
 
    template<class P>
    pair<iterator, bool> insert(P&& x);
    template<class P>
    iterator insert(const_iterator position, P&&);
    template<class InputIter>
    void insert(InputIter first, InputIter last);
    template<class InputIter>
    void insert(sorted_unique_t, InputIter first, InputIter last);
    template<container-compatible-range<value_type> R>
    void insert_range(R&& rg);
 
    void insert(initializer_list<value_type> il) { insert(il.begin(), il.end()); }
    void insert(sorted_unique_t s, initializer_list<value_type> il)
    {
      insert(s, il.begin(), il.end());
    }
 
    containers extract() &&;
    void replace(key_container_type&& key_cont, mapped_container_type&& mapped_cont);
 
    template<class... Args>
    pair<iterator, bool> try_emplace(const key_type& k, Args&&... args);
    template<class... Args>
    pair<iterator, bool> try_emplace(key_type&& k, Args&&... args);
    template<class K, class... Args>
    pair<iterator, bool> try_emplace(K&& k, Args&&... args);
    template<class... Args>
    iterator try_emplace(const_iterator hint, const key_type& k, Args&&... args);
    template<class... Args>
    iterator try_emplace(const_iterator hint, key_type&& k, Args&&... args);
    template<class K, class... Args>
    iterator try_emplace(const_iterator hint, K&& k, Args&&... args);
    template<class M>
    pair<iterator, bool> insert_or_assign(const key_type& k, M&& obj);
    template<class M>
    pair<iterator, bool> insert_or_assign(key_type&& k, M&& obj);
    template<class K, class M>
    pair<iterator, bool> insert_or_assign(K&& k, M&& obj);
    template<class M>
    iterator insert_or_assign(const_iterator hint, const key_type& k, M&& obj);
    template<class M>
    iterator insert_or_assign(const_iterator hint, key_type&& k, M&& obj);
    template<class K, class M>
    iterator insert_or_assign(const_iterator hint, K&& k, M&& obj);
 
    iterator erase(iterator position);
    iterator erase(const_iterator position);
    size_type erase(const key_type& x);
    template<class K>
    size_type erase(K&& x);
    iterator erase(const_iterator first, const_iterator last);
 
    void swap(flat_map& y) noexcept;
    void clear() noexcept;
 
    // observers
    key_compare key_comp() const;
    value_compare value_comp() const;
 
    const key_container_type& keys() const noexcept { return c.keys; }
    const mapped_container_type& values() const noexcept { return c.values; }
 
    // map operations
    iterator find(const key_type& x);
    const_iterator find(const key_type& x) const;
    template<class K>
    iterator find(const K& x);
    template<class K>
    const_iterator find(const K& x) const;
 
    size_type count(const key_type& x) const;
    template<class K>
    size_type count(const K& x) const;
 
    bool contains(const key_type& x) const;
    template<class K>
    bool contains(const K& x) const;
 
    iterator lower_bound(const key_type& x);
    const_iterator lower_bound(const key_type& x) const;
    template<class K>
    iterator lower_bound(const K& x);
    template<class K>
    const_iterator lower_bound(const K& x) const;
 
    iterator upper_bound(const key_type& x);
    const_iterator upper_bound(const key_type& x) const;
    template<class K>
    iterator upper_bound(const K& x);
    template<class K>
    const_iterator upper_bound(const K& x) const;
 
    pair<iterator, iterator> equal_range(const key_type& x);
    pair<const_iterator, const_iterator> equal_range(const key_type& x) const;
    template<class K>
    pair<iterator, iterator> equal_range(const K& x);
    template<class K>
    pair<const_iterator, const_iterator> equal_range(const K& x) const;
 
    friend bool operator==(const flat_map& x, const flat_map& y);
 
    friend /*synth-three-way-result*/<value_type> operator<=>(const flat_map& x,
                                                              const flat_map& y);
 
    friend void swap(flat_map& x, flat_map& y) noexcept { x.swap(y); }
 
  private:
    containers c;        // exposition only
    key_compare compare; // exposition only
 
    struct key_equiv
    { // exposition only
      key_equiv(key_compare c)
        : comp(c)
      {
      }
      bool operator()(const_reference x, const_reference y) const
      {
        return !comp(x.first, y.first) && !comp(y.first, x.first);
      }
      key_compare comp;
    };
  };
 
  template<class KeyContainer,
           class MappedContainer,
           class Compare = less<typename KeyContainer::value_type>>
  flat_map(KeyContainer, MappedContainer, Compare = Compare())
    -> flat_map<typename KeyContainer::value_type,
                typename MappedContainer::value_type,
                Compare,
                KeyContainer,
                MappedContainer>;
 
  template<class KeyContainer, class MappedContainer, class Allocator>
  flat_map(KeyContainer, MappedContainer, Allocator)
    -> flat_map<typename KeyContainer::value_type,
                typename MappedContainer::value_type,
                less<typename KeyContainer::value_type>,
                KeyContainer,
                MappedContainer>;
  template<class KeyContainer, class MappedContainer, class Compare, class Allocator>
  flat_map(KeyContainer, MappedContainer, Compare, Allocator)
    -> flat_map<typename KeyContainer::value_type,
                typename MappedContainer::value_type,
                Compare,
                KeyContainer,
                MappedContainer>;
 
  template<class KeyContainer,
           class MappedContainer,
           class Compare = less<typename KeyContainer::value_type>>
  flat_map(sorted_unique_t, KeyContainer, MappedContainer, Compare = Compare())
    -> flat_map<typename KeyContainer::value_type,
                typename MappedContainer::value_type,
                Compare,
                KeyContainer,
                MappedContainer>;
 
  template<class KeyContainer, class MappedContainer, class Allocator>
  flat_map(sorted_unique_t, KeyContainer, MappedContainer, Allocator)
    -> flat_map<typename KeyContainer::value_type,
                typename MappedContainer::value_type,
                less<typename KeyContainer::value_type>,
                KeyContainer,
                MappedContainer>;
  template<class KeyContainer, class MappedContainer, class Compare, class Allocator>
  flat_map(sorted_unique_t, KeyContainer, MappedContainer, Compare, Allocator)
    -> flat_map<typename KeyContainer::value_type,
                typename MappedContainer::value_type,
                Compare,
                KeyContainer,
                MappedContainer>;
 
  template<class InputIter, class Compare = less</*iter-key-type*/<InputIter>>>
  flat_map(InputIter, InputIter, Compare = Compare())
    -> flat_map</*iter-key-type*/<InputIter>, /*iter-mapped-type*/<InputIter>, Compare>;
 
  template<class InputIter, class Compare = less</*iter-key-type*/<InputIter>>>
  flat_map(sorted_unique_t, InputIter, InputIter, Compare = Compare())
    -> flat_map</*iter-key-type*/<InputIter>, /*iter-mapped-type*/<InputIter>, Compare>;
 
  template<ranges::input_range R,
           class Compare   = less</*range-key-type*/<R>>,
           class Allocator = allocator<byte>>
  flat_map(from_range_t, R&&, Compare = Compare(), Allocator = Allocator()) -> flat_map<
    /*range-key-type*/<R>,
    /*range-mapped-type*/<R>,
    Compare,
    vector</*range-key-type*/<R>, /*alloc-rebind*/<Allocator, /*range-key-type*/<R>>>,
    vector</*range-mapped-type*/<R>,
           /*alloc-rebind*/<Allocator, /*range-mapped-type*/<R>>>>;
 
  template<ranges::input_range R, class Allocator>
  flat_map(from_range_t, R&&, Allocator) -> flat_map<
    /*range-key-type*/<R>,
    /*range-mapped-type*/<R>,
    less</*range-key-type*/<R>>,
    vector</*range-key-type*/<R>, /*alloc-rebind*/<Allocator, /*range-key-type*/<R>>>,
    vector</*range-mapped-type*/<R>,
           /*alloc-rebind*/<Allocator, /*range-mapped-type*/<R>>>>;
 
  template<class Key, class T, class Compare = less<Key>>
  flat_map(initializer_list<pair<Key, T>>, Compare = Compare())
    -> flat_map<Key, T, Compare>;
 
  template<class Key, class T, class Compare = less<Key>>
  flat_map(sorted_unique_t, initializer_list<pair<Key, T>>, Compare = Compare())
    -> flat_map<Key, T, Compare>;
 
  template<class Key,
           class T,
           class Compare,
           class KeyContainer,
           class MappedContainer,
           class Allocator>
  struct uses_allocator<flat_map<Key, T, Compare, KeyContainer, MappedContainer>,
                        Allocator>
    : bool_constant<uses_allocator_v<KeyContainer, Allocator> &&
                    uses_allocator_v<MappedContainer, Allocator>>
  {};
}

```

#### Class template std::flat_multimap

```
namespace std {
  template<class Key,
           class T,
           class Compare         = less<Key>,
           class KeyContainer    = vector<Key>,
           class MappedContainer = vector<T>>
  class flat_multimap
  {
  public:
    // types
    using key_type               = Key;
    using mapped_type            = T;
    using value_type             = pair<key_type, mapped_type>;
    using key_compare            = Compare;
    using reference              = pair<const key_type&, mapped_type&>;
    using const_reference        = pair<const key_type&, const mapped_type&>;
    using size_type              = size_t;
    using difference_type        = ptrdiff_t;
    using iterator               = /* implementation-defined */;
    using const_iterator         = /* implementation-defined */;
    using reverse_iterator       = std::reverse_iterator<iterator>;
    using const_reverse_iterator = std::reverse_iterator<const_iterator>;
    using key_container_type     = KeyContainer;
    using mapped_container_type  = MappedContainer;
 
    class value_compare
    {
    private:
      key_compare comp; // exposition only
      value_compare(key_compare c)
        : comp(c)
      {
      } // exposition only
 
    public:
      bool operator()(const_reference x, const_reference y) const
      {
        return comp(x.first, y.first);
      }
    };
 
    struct containers
    {
      key_container_type keys;
      mapped_container_type values;
    };
 
    // constructors
    flat_multimap()
      : flat_multimap(key_compare())
    {
    }
 
    explicit flat_multimap(const key_compare& comp)
      : c()
      , compare(comp)
    {
    }
 
    flat_multimap(key_container_type key_cont,
                  mapped_container_type mapped_cont,
                  const key_compare& comp = key_compare());
 
    flat_multimap(sorted_equivalent_t,
                  key_container_type key_cont,
                  mapped_container_type mapped_cont,
                  const key_compare& comp = key_compare());
 
    template<class InputIter>
    flat_multimap(InputIter first,
                  InputIter last,
                  const key_compare& comp = key_compare())
      : c()
      , compare(comp)
    {
      insert(first, last);
    }
 
    template<class InputIter>
    flat_multimap(sorted_equivalent_t s,
                  InputIter first,
                  InputIter last,
                  const key_compare& comp = key_compare())
      : c()
      , compare(comp)
    {
      insert(s, first, last);
    }
 
    template<container-compatible-range<value_type> R>
    flat_multimap(from_range_t fr, R&& rg)
      : flat_multimap(fr, std::forward<R>(rg), key_compare())
    {
    }
    template<container-compatible-range<value_type> R>
    flat_multimap(from_range_t, R&& rg, const key_compare& comp)
      : flat_multimap(comp)
    {
      insert_range(std::forward<R>(rg));
    }
 
    flat_multimap(initializer_list<value_type> il,
                  const key_compare& comp = key_compare())
      : flat_multimap(il.begin(), il.end(), comp)
    {
    }
 
    flat_multimap(sorted_equivalent_t s,
                  initializer_list<value_type> il,
                  const key_compare& comp = key_compare())
      : flat_multimap(s, il.begin(), il.end(), comp)
    {
    }
 
    // constructors with allocators
 
    template<class Alloc>
    explicit flat_multimap(const Alloc& a);
    template<class Alloc>
    flat_multimap(const key_compare& comp, const Alloc& a);
    template<class Alloc>
    flat_multimap(const key_container_type& key_cont,
                  const mapped_container_type& mapped_cont,
                  const Alloc& a);
    template<class Alloc>
    flat_multimap(const key_container_type& key_cont,
                  const mapped_container_type& mapped_cont,
                  const key_compare& comp,
                  const Alloc& a);
    template<class Alloc>
    flat_multimap(sorted_equivalent_t,
                  const key_container_type& key_cont,
                  const mapped_container_type& mapped_cont,
                  const Alloc& a);
    template<class Alloc>
    flat_multimap(sorted_equivalent_t,
                  const key_container_type& key_cont,
                  const mapped_container_type& mapped_cont,
                  const key_compare& comp,
                  const Alloc& a);
    template<class Alloc>
    flat_multimap(const flat_multimap&, const Alloc& a);
    template<class Alloc>
    flat_multimap(flat_multimap&&, const Alloc& a);
    template<class InputIter, class Alloc>
    flat_multimap(InputIter first, InputIter last, const Alloc& a);
    template<class InputIter, class Alloc>
    flat_multimap(InputIter first,
                  InputIter last,
                  const key_compare& comp,
                  const Alloc& a);
    template<class InputIter, class Alloc>
    flat_multimap(sorted_equivalent_t, InputIter first, InputIter last, const Alloc& a);
    template<class InputIter, class Alloc>
    flat_multimap(sorted_equivalent_t,
                  InputIter first,
                  InputIter last,
                  const key_compare& comp,
                  const Alloc& a);
    template<container-compatible-range<value_type> R, class Alloc>
    flat_multimap(from_range_t, R&& rg, const Alloc& a);
    template<container-compatible-range<value_type> R, class Alloc>
    flat_multimap(from_range_t, R&& rg, const key_compare& comp, const Alloc& a);
    template<class Alloc>
    flat_multimap(initializer_list<value_type> il, const Alloc& a);
    template<class Alloc>
    flat_multimap(initializer_list<value_type> il,
                  const key_compare& comp,
                  const Alloc& a);
    template<class Alloc>
    flat_multimap(sorted_equivalent_t, initializer_list<value_type> il, const Alloc& a);
    template<class Alloc>
    flat_multimap(sorted_equivalent_t,
                  initializer_list<value_type> il,
                  const key_compare& comp,
                  const Alloc& a);
 
    flat_multimap& operator=(initializer_list<value_type>);
 
    // iterators
    iterator begin() noexcept;
    const_iterator begin() const noexcept;
    iterator end() noexcept;
    const_iterator end() const noexcept;
 
    reverse_iterator rbegin() noexcept;
    const_reverse_iterator rbegin() const noexcept;
    reverse_iterator rend() noexcept;
    const_reverse_iterator rend() const noexcept;
 
    const_iterator cbegin() const noexcept;
    const_iterator cend() const noexcept;
    const_reverse_iterator crbegin() const noexcept;
    const_reverse_iterator crend() const noexcept;
 
    // capacity
    bool empty() const noexcept;
    size_type size() const noexcept;
    size_type max_size() const noexcept;
 
    // modifiers
    template<class... Args>
    iterator emplace(Args&&... args);
    template<class... Args>
    iterator emplace_hint(const_iterator position, Args&&... args);
 
    iterator insert(const value_type& x) { return emplace(x); }
    iterator insert(value_type&& x) { return emplace(std::move(x)); }
    iterator insert(const_iterator position, const value_type& x)
    {
      return emplace_hint(position, x);
    }
    iterator insert(const_iterator position, value_type&& x)
    {
      return emplace_hint(position, std::move(x));
    }
 
    template<class P>
    iterator insert(P&& x);
    template<class P>
    iterator insert(const_iterator position, P&&);
    template<class InputIter>
    void insert(InputIter first, InputIter last);
    template<class InputIter>
    void insert(sorted_equivalent_t, InputIter first, InputIter last);
    template<container-compatible-range<value_type> R>
    void insert_range(R&& rg);
 
    void insert(initializer_list<value_type> il) { insert(il.begin(), il.end()); }
    void insert(sorted_equivalent_t s, initializer_list<value_type> il)
    {
      insert(s, il.begin(), il.end());
    }
 
    containers extract() &&;
    void replace(key_container_type&& key_cont, mapped_container_type&& mapped_cont);
 
    iterator erase(iterator position);
    iterator erase(const_iterator position);
    size_type erase(const key_type& x);
    template<class K>
    size_type erase(K&& x);
    iterator erase(const_iterator first, const_iterator last);
 
    void swap(flat_multimap&) noexcept;
    void clear() noexcept;
 
    // observers
    key_compare key_comp() const;
    value_compare value_comp() const;
 
    const key_container_type& keys() const noexcept { return c.keys; }
    const mapped_container_type& values() const noexcept { return c.values; }
 
    // map operations
    iterator find(const key_type& x);
    const_iterator find(const key_type& x) const;
    template<class K>
    iterator find(const K& x);
    template<class K>
    const_iterator find(const K& x) const;
 
    size_type count(const key_type& x) const;
    template<class K>
    size_type count(const K& x) const;
 
    bool contains(const key_type& x) const;
    template<class K>
    bool contains(const K& x) const;
 
    iterator lower_bound(const key_type& x);
    const_iterator lower_bound(const key_type& x) const;
    template<class K>
    iterator lower_bound(const K& x);
    template<class K>
    const_iterator lower_bound(const K& x) const;
 
    iterator upper_bound(const key_type& x);
    const_iterator upper_bound(const key_type& x) const;
    template<class K>
    iterator upper_bound(const K& x);
    template<class K>
    const_iterator upper_bound(const K& x) const;
 
    pair<iterator, iterator> equal_range(const key_type& x);
    pair<const_iterator, const_iterator> equal_range(const key_type& x) const;
    template<class K>
    pair<iterator, iterator> equal_range(const K& x);
    template<class K>
    pair<const_iterator, const_iterator> equal_range(const K& x) const;
 
    friend bool operator==(const flat_multimap& x, const flat_multimap& y);
 
    friend /*synth-three-way-result*/<value_type> operator<=>(const flat_multimap& x,
                                                              const flat_multimap& y);
 
    friend void swap(flat_multimap& x, flat_multimap& y) noexcept { x.swap(y); }
 
  private:
    containers c;        // exposition only
    key_compare compare; // exposition only
  };
 
  template<class KeyContainer,
           class MappedContainer,
           class Compare = less<typename KeyContainer::value_type>>
  flat_multimap(KeyContainer, MappedContainer, Compare = Compare())
    -> flat_multimap<typename KeyContainer::value_type,
                     typename MappedContainer::value_type,
                     Compare,
                     KeyContainer,
                     MappedContainer>;
 
  template<class KeyContainer, class MappedContainer, class Allocator>
  flat_multimap(KeyContainer, MappedContainer, Allocator)
    -> flat_multimap<typename KeyContainer::value_type,
                     typename MappedContainer::value_type,
                     less<typename KeyContainer::value_type>,
                     KeyContainer,
                     MappedContainer>;
  template<class KeyContainer, class MappedContainer, class Compare, class Allocator>
  flat_multimap(KeyContainer, MappedContainer, Compare, Allocator)
    -> flat_multimap<typename KeyContainer::value_type,
                     typename MappedContainer::value_type,
                     Compare,
                     KeyContainer,
                     MappedContainer>;
 
  template<class KeyContainer,
           class MappedContainer,
           class Compare = less<typename KeyContainer::value_type>>
  flat_multimap(sorted_equivalent_t, KeyContainer, MappedContainer, Compare = Compare())
    -> flat_multimap<typename KeyContainer::value_type,
                     typename MappedContainer::value_type,
                     Compare,
                     KeyContainer,
                     MappedContainer>;
 
  template<class KeyContainer, class MappedContainer, class Allocator>
  flat_multimap(sorted_equivalent_t, KeyContainer, MappedContainer, Allocator)
    -> flat_multimap<typename KeyContainer::value_type,
                     typename MappedContainer::value_type,
                     less<typename KeyContainer::value_type>,
                     KeyContainer,
                     MappedContainer>;
  template<class KeyContainer, class MappedContainer, class Compare, class Allocator>
  flat_multimap(sorted_equivalent_t, KeyContainer, MappedContainer, Compare, Allocator)
    -> flat_multimap<typename KeyContainer::value_type,
                     typename MappedContainer::value_type,
                     Compare,
                     KeyContainer,
                     MappedContainer>;
 
  template<class InputIter, class Compare = less</*iter-key-type*/<InputIter>>>
  flat_multimap(InputIter, InputIter, Compare = Compare())
    -> flat_multimap</*iter-key-type*/<InputIter>,
                     /*iter-mapped-type*/<InputIter>,
                     Compare>;
 
  template<class InputIter, class Compare = less</*iter-key-type*/<InputIter>>>
  flat_multimap(sorted_equivalent_t, InputIter, InputIter, Compare = Compare())
    -> flat_multimap</*iter-key-type*/<InputIter>,
                     /*iter-mapped-type*/<InputIter>,
                     Compare>;
 
  template<ranges::input_range R,
           class Compare   = less</*range-key-type*/<R>>,
           class Allocator = allocator<byte>>
  flat_multimap(from_range_t, R&&, Compare = Compare(), Allocator = Allocator())
    -> flat_multimap<
      /*range-key-type*/<R>,
      /*range-mapped-type*/<R>,
      Compare,
      vector</*range-key-type*/<R>, /*alloc-rebind*/<Allocator, /*range-key-type*/<R>>>,
      vector</*range-mapped-type*/<R>,
             /*alloc-rebind*/<Allocator, /*range-mapped-type*/<R>>>>;
 
  template<ranges::input_range R, class Allocator>
  flat_multimap(from_range_t, R&&, Allocator) -> flat_multimap<
    /*range-key-type*/<R>,
    /*range-mapped-type*/<R>,
    less</*range-key-type*/<R>>,
    vector</*range-key-type*/<R>, /*alloc-rebind*/<Allocator, /*range-key-type*/<R>>>,
    vector</*range-mapped-type*/<R>,
           /*alloc-rebind*/<Allocator, /*range-mapped-type*/<R>>>>;
 
  template<class Key, class T, class Compare = less<Key>>
  flat_multimap(initializer_list<pair<Key, T>>, Compare = Compare())
    -> flat_multimap<Key, T, Compare>;
 
  template<class Key, class T, class Compare = less<Key>>
  flat_multimap(sorted_equivalent_t, initializer_list<pair<Key, T>>, Compare = Compare())
    -> flat_multimap<Key, T, Compare>;
 
  template<class Key,
           class T,
           class Compare,
           class KeyContainer,
           class MappedContainer,
           class Allocator>
  struct uses_allocator<flat_multimap<Key, T, Compare, KeyContainer, MappedContainer>,
                        Allocator>
    : bool_constant<uses_allocator_v<KeyContainer, Allocator> &&
                    uses_allocator_v<MappedContainer, Allocator>>
  {};
}

```

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 24.6.4 Header `<flat_map>` synopsis [flat.map.syn]

:   - 24.6.9.2 Definition [flat.map.defn]

:   - 24.6.10.2 Definition [flat.multimap.defn]

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/flat_map&oldid=165997>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 December 2023, at 06:46.