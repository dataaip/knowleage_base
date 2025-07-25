# Standard library header <expected> (C++23)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | ****<expected>**** (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the general utility library.

|  |  |
| --- | --- |
| Classes | |
| expected(C++23) | a wrapper that contains either an expected or error value   (class template) |
| unexpected(C++23) | represented as an unexpected value   (class template) |
| bad_expected_access(C++23) | exception indicating checked access to an `expected` that contains an unexpected value   (class template) |
| unexpectunexpect_t(C++23) | in-place construction tag for unexpected value in `expected` (tag) |

### Synopsis

```
namespace std {
  // class template unexpected
  template<class E> class unexpected;
 
  // class template bad_expected_access
  template<class E> class bad_expected_access;
 
  // specialization of bad_expected_access for void
  template<> class bad_expected_access<void>;
 
  // in-place construction of unexpected values
  struct unexpect_t {
    explicit unexpect_t() = default;
  };
  inline constexpr unexpect_t unexpect{};
 
  // class template expected
  template<class T, class E> class expected;
 
  // partial specialization of expected for void types
  template<class T, class E> requires is_void_v<T> class expected<T, E>;
}

```

#### Class template std::unexpected

```
namespace std {
  template<class E>
  class unexpected {
  public:
    // constructors
    constexpr unexpected(const unexpected&) = default;
    constexpr unexpected(unexpected&&) = default;
    template<class... Args>
      constexpr explicit unexpected(in_place_t, Args&&...);
    template<class U, class... Args>
      constexpr explicit unexpected(in_place_t, initializer_list<U>, Args&&...);
    template<class Err = E>
      constexpr explicit unexpected(Err&&);
 
    // assignment
    constexpr unexpected& operator=(const unexpected&) = default;
    constexpr unexpected& operator=(unexpected&&) = default;
 
    // observer
    constexpr const E& error() const& noexcept;
    constexpr E& error() & noexcept;
    constexpr const E&& error() const&& noexcept;
    constexpr E&& error() && noexcept;
 
    // swap
    constexpr void swap(unexpected& other) noexcept(/* see description */);
 
    friend constexpr void swap(unexpected& x, unexpected& y) noexcept(noexcept(x.swap(y)));
 
    // equality operator
    template<class E2>
      friend constexpr bool operator==(const unexpected&, const unexpected<E2>&);
 
  private:
    E unex;    // exposition only
  };
 
  template<class E> 
    unexpected(E) -> unexpected<E>;
}

```

#### Class template std::bad_expected_access

```
namespace std {
  template<class E>
  class bad_expected_access : public bad_expected_access<void> {
  public:
 
    // explicit constructor
    explicit bad_expected_access(E);
 
    // observers
    const char* what() const noexcept override;
    E& error() & noexcept;
    const E& error() const& noexcept;
    E&& error() && noexcept;
    const E&&  error() const&& noexcept;
 
  private:
    E unex;              // exposition only
  };
}

```

#### Class template specialization std::bad_expected_access<void>

```
namespace std {
  template<>
  class bad_expected_access<void> : public exception {
  protected:
    // constructors
    bad_expected_access() noexcept;
    bad_expected_access(const bad_expected_access&);
    bad_expected_access(bad_expected_access&&);
    bad_expected_access& operator=(const bad_expected_access&);
    bad_expected_access& operator=(bad_expected_access&&);
 
    ~bad_expected_access();
 
  public:
    const char* what() const noexcept override;
  };
}

```

#### Class template std::expected

```
namespace std {
  template<class T, class E>
  class expected {
  public:
    using value_type = T;
    using error_type = E;
    using unexpected_type = unexpected<E>;
 
    template<class U>
    using rebind = expected<U, error_type>;
 
    // constructors
    constexpr expected();
    constexpr explicit(/* see description */) 
      expected(const expected&);
    constexpr explicit(/* see description */) 
      expected(expected&&) noexcept(/* see description */);
    template<class U, class G>
      constexpr explicit(/* see description */) expected(const expected<U, G>&);
    template<class U, class G>
      constexpr explicit(/* see description */) expected(expected<U, G>&&);
 
    template<class U = T>
      constexpr explicit(/* see description */) expected(U&& v);
 
    template<class G>
      constexpr expected(const unexpected<G>&);
    template<class G>
      constexpr expected(unexpected<G>&&);
 
    template<class... Args>
      constexpr explicit expected(in_place_t, Args&&...);
    template<class U, class... Args>
      constexpr explicit expected(in_place_t, initializer_list<U>, Args&&...);
    template<class... Args>
      constexpr explicit expected(unexpect_t, Args&&...);
    template<class U, class... Args>
      constexpr explicit expected(unexpect_t, initializer_list<U>, Args&&...);
 
    // destructor
    constexpr ~expected();
 
    // assignment
    constexpr expected& operator=(const expected&);
    constexpr expected& operator=(expected&&) noexcept(/* see description */);
    template<class U = T> constexpr expected& operator=(U&&);
    template<class G>
      constexpr expected& operator=(const unexpected<G>&);
    template<class G>
      constexpr expected& operator=(unexpected<G>&&);
 
    template<class... Args>
      constexpr T& emplace(Args&&...) noexcept;
    template<class U, class... Args>
      constexpr T& emplace(initializer_list<U>, Args&&...) noexcept;
 
    // swap
    constexpr void swap(expected&) noexcept(/* see description */);
    friend constexpr void swap(expected&, expected&) noexcept(/* see description */);
 
    // observers
    constexpr const T* operator->() const noexcept;
    constexpr T* operator->() noexcept;
    constexpr const T& operator*() const& noexcept;
    constexpr T& operator*() & noexcept;
    constexpr const T&& operator*() const&& noexcept;
    constexpr T&& operator*() && noexcept;
    constexpr explicit operator bool() const noexcept;
    constexpr bool has_value() const noexcept;
    constexpr const T& value() const&;
    constexpr T& value() &;
    constexpr const T&& value() const&&;
    constexpr T&& value() &&;
    constexpr const E& error() const&;
    constexpr E& error() &;
    constexpr const E&& error() const&&;
    constexpr E&& error() &&;
    template<class U> constexpr T value_or(U&&) const&;
    template<class U> constexpr T value_or(U&&) &&;
    template<class G = E> constexpr E error_or(G&&) const &;
    template<class G = E> constexpr E error_or(G&&) &&;
 
    // monadic operations
    template<class F> constexpr auto and_then(F&& f) &;
    template<class F> constexpr auto and_then(F&& f) &&;
    template<class F> constexpr auto and_then(F&& f) const &;
    template<class F> constexpr auto and_then(F&& f) const &&;
    template<class F> constexpr auto or_else(F&& f) &;
    template<class F> constexpr auto or_else(F&& f) &&;
    template<class F> constexpr auto or_else(F&& f) const &;
    template<class F> constexpr auto or_else(F&& f) const &&;
    template<class F> constexpr auto transform(F&& f) &;
    template<class F> constexpr auto transform(F&& f) &&;
    template<class F> constexpr auto transform(F&& f) const &;
    template<class F> constexpr auto transform(F&& f) const &&;
    template<class F> constexpr auto transform_error(F&& f) &;
    template<class F> constexpr auto transform_error(F&& f) &&;
    template<class F> constexpr auto transform_error(F&& f) const &;
    template<class F> constexpr auto transform_error(F&& f) const &&;
 
    // equality operators
    template<class T2, class E2> requires (!is_void_v<T2>)
      friend constexpr bool operator==(const expected& x, const expected<T2, E2>& y);
    template<class T2>
      friend constexpr bool operator==(const expected&, const T2&);
    template<class E2>
      friend constexpr bool operator==(const expected&, const unexpected<E2>&);
 
  private:
    bool has_val;       // exposition only
    union {
      T val;            // exposition only
      E unex;           // exposition only
    };
  };
}

```

#### Partial specialization of std::expected for void types

```
namespace std {
  template<class T, class E> requires is_void_v<T>
  class expected<T, E> {
  public:
    using value_type = T;
    using error_type = E;
    using unexpected_type = unexpected<E>;
 
    template<class U>
    using rebind = expected<U, error_type>;
 
    // constructors
    constexpr expected() noexcept;
    constexpr explicit(/* see description */)
      expected(const expected&);
    constexpr explicit(/* see description */)
      expected(expected&&) noexcept(/* see description */);
    template<class U, class G>
      constexpr explicit(/* see description */) expected(const expected<U, G>&);
    template<class U, class G>
      constexpr explicit(/* see description */) expected(expected<U, G>&&);
 
    template<class G>
      constexpr expected(const unexpected<G>&);
    template<class G>
      constexpr expected(unexpected<G>&&);
 
    constexpr explicit expected(in_place_t) noexcept;
    template<class... Args>
      constexpr explicit expected(unexpect_t, Args&&...);
    template<class U, class... Args>
      constexpr explicit expected(unexpect_t, initializer_list<U>, Args&&...);
 
    // destructor
    constexpr ~expected();
 
    // assignment
    constexpr expected& operator=(const expected&);
    constexpr expected& operator=(expected&&) noexcept(/* see description */);
    template<class G>
      constexpr expected& operator=(const unexpected<G>&);
    template<class G>
      constexpr expected& operator=(unexpected<G>&&);
    constexpr void emplace() noexcept;
 
    // swap
    constexpr void swap(expected&) noexcept(/* see description */);
    friend constexpr void swap(expected&, expected&) noexcept(/* see description */);
 
    // observers
    constexpr explicit operator bool() const noexcept;
    constexpr bool has_value() const noexcept;
    constexpr void operator*() const noexcept;
    constexpr void value() const&;
    constexpr void value() &&;
    constexpr const E& error() const&;
    constexpr E& error() &;
    constexpr const E&& error() const&&;
    constexpr E&& error() &&;
    template<class G = E> constexpr E error_or(G&&) const &;
    template<class G = E> constexpr E error_or(G&&) &&;
 
    // monadic operations
    template<class F> constexpr auto and_then(F&& f) &;
    template<class F> constexpr auto and_then(F&& f) &&;
    template<class F> constexpr auto and_then(F&& f) const &;
    template<class F> constexpr auto and_then(F&& f) const &&;
    template<class F> constexpr auto or_else(F&& f) &;
    template<class F> constexpr auto or_else(F&& f) &&;
    template<class F> constexpr auto or_else(F&& f) const &;
    template<class F> constexpr auto or_else(F&& f) const &&;
    template<class F> constexpr auto transform(F&& f) &;
    template<class F> constexpr auto transform(F&& f) &&;
    template<class F> constexpr auto transform(F&& f) const &;
    template<class F> constexpr auto transform(F&& f) const &&;
    template<class F> constexpr auto transform_error(F&& f) &;
    template<class F> constexpr auto transform_error(F&& f) &&;
    template<class F> constexpr auto transform_error(F&& f) const &;
    template<class F> constexpr auto transform_error(F&& f) const &&;
 
    // equality operators
    template<class T2, class E2> requires is_void_v<T2>
      friend constexpr bool operator==(const expected& x, const expected<T2, E2>& y);
    template<class E2>
      friend constexpr bool operator==(const expected&, const unexpected<E2>&);
 
  private:
    bool has_val;        // exposition only
    union {
      E unex;            // exposition only
    };
  };
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/expected&oldid=163945>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 November 2023, at 06:59.