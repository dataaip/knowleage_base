# Standard library header <compare> (C++20)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | ****<compare>**** (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the language support library.

|  |  |
| --- | --- |
| Concepts | |
| three_way_comparablethree_way_comparable_with(C++20) | specifies that operator <=> produces consistent result on given types   (concept) |
| Classes | |
| partial_ordering(C++20) | the result type of 3-way comparison that supports all 6 operators, is not substitutable, and allows incomparable values   (class) |
| weak_ordering(C++20) | the result type of 3-way comparison that supports all 6 operators and is not substitutable   (class) |
| strong_ordering(C++20) | the result type of 3-way comparison that supports all 6 operators and is substitutable   (class) |
| common_comparison_category(C++20) | the strongest comparison category to which all of the given types can be converted   (class template) |
| compare_three_way_result(C++20) | obtains the result type of the three-way comparison operator <=> on given types   (class template) |
| compare_three_way(C++20) | constrained function object implementing x <=> y   (class) |
| Customization point objects | |
| strong_order(C++20) | performs 3-way comparison and produces a result of type `std::strong_ordering` (customization point object) |
| weak_order(C++20) | performs 3-way comparison and produces a result of type `std::weak_ordering` (customization point object) |
| partial_order(C++20) | performs 3-way comparison and produces a result of type `std::partial_ordering` (customization point object) |
| compare_strong_order_fallback(C++20) | performs 3-way comparison and produces a result of type `std::strong_ordering`, even if operator<=> is unavailable (customization point object) |
| compare_weak_order_fallback(C++20) | performs 3-way comparison and produces a result of type `std::weak_ordering`, even if operator<=> is unavailable (customization point object) |
| compare_partial_order_fallback(C++20) | performs 3-way comparison and produces a result of type `std::partial_ordering`, even if operator<=> is unavailable (customization point object) |
| Functions | |
| is_eqis_neqis_ltis_lteqis_gtis_gteq(C++20) | named comparison functions   (function) |

### Synopsis

```
namespace std {
  // comparison category types
  class partial_ordering;
  class weak_ordering;
  class strong_ordering;
 
  // named comparison functions
  constexpr bool is_eq  (partial_ordering cmp) noexcept { return cmp == 0; }
  constexpr bool is_neq (partial_ordering cmp) noexcept { return cmp != 0; }
  constexpr bool is_lt  (partial_ordering cmp) noexcept { return cmp < 0; }
  constexpr bool is_lteq(partial_ordering cmp) noexcept { return cmp <= 0; }
  constexpr bool is_gt  (partial_ordering cmp) noexcept { return cmp > 0; }
  constexpr bool is_gteq(partial_ordering cmp) noexcept { return cmp >= 0; }
 
  // common comparison category type
  template<class... Ts>
  struct common_comparison_category {
    using type = /* see description */;
  };
  template<class... Ts>
    using common_comparison_category_t = typename common_comparison_category<Ts...>::type;
 
  // concept three_way_comparable
  template<class T, class Cat = partial_ordering>
    concept three_way_comparable = /* see description */;
  template<class T, class U, class Cat = partial_ordering>
    concept three_way_comparable_with = /* see description */;
 
  // result of three-way comparison
  template<class T, class U = T> struct compare_three_way_result;
 
  template<class T, class U = T>
    using compare_three_way_result_t = typename compare_three_way_result<T, U>::type;
 
  // class compare_three_way
  struct compare_three_way;
 
  // comparison algorithms
  inline namespace /* unspecified */ {
    inline constexpr /* unspecified */ strong_order = /* unspecified */;
    inline constexpr /* unspecified */ weak_order = /* unspecified */;
    inline constexpr /* unspecified */ partial_order = /* unspecified */;
    inline constexpr /* unspecified */ compare_strong_order_fallback = /* unspecified */;
    inline constexpr /* unspecified */ compare_weak_order_fallback = /* unspecified */;
    inline constexpr /* unspecified */ compare_partial_order_fallback = /* unspecified */;
  }
}

```

#### Concept `three_way_comparable`

```
namespace std {
  template<class T, class Cat>
    concept __ComparesAs =                // exposition only
      same_as<common_comparison_category_t<T, Cat>, Cat>;
 
  template<class T, class U>
    concept __PartiallyOrderedWith =      // exposition only
      requires(const remove_reference_t<T>& t, const remove_reference_t<U>& u) {
        { t <  u } -> boolean-testable;
        { t >  u } -> boolean-testable;
        { t <= u } -> boolean-testable;
        { t >= u } -> boolean-testable;
        { u <  t } -> boolean-testable;
        { u >  t } -> boolean-testable;
        { u <= t } -> boolean-testable;
        { u >= t } -> boolean-testable;
      };
 
  template<class T, class Cat = partial_ordering>
    concept three_way_comparable =
      __WeaklyEqualityComparableWith<T, T> &&
      __PartiallyOrderedWith<T, T> &&
      requires(const remove_reference_t<T>& a, const remove_reference_t<T>& b) {
        { a <=> b } -> __ComparesAs<Cat>;
      };
}

```

#### Concept `three_way_comparable_with`

```
namespace std {
  template<class T, class U, class Cat = partial_ordering>
    concept three_way_comparable_with =
      __WeaklyEqualityComparableWith<T, U> &&
      __PartiallyOrderedWith<T, U> &&
      three_way_comparable<T, Cat> &&
      three_way_comparable<U, Cat> &&
      common_reference_with<const remove_reference_t<T>&, const remove_reference_t<U>&> &&
      three_way_comparable<
        common_reference_t<
          const remove_reference_t<T>&, const remove_reference_t<U>&>, Cat> &&
      requires(const remove_reference_t<T>& t, const remove_reference_t<U>& u) {
        { t <=> u } -> __ComparesAs<Cat>;
        { u <=> t } -> __ComparesAs<Cat>;
      };
}

```

#### Class std::partial_ordering

```
namespace std {
  class partial_ordering {
    int value;          // exposition only
    bool is_ordered;    // exposition only
 
    // exposition-only constructors
    constexpr explicit
      partial_ordering(eq v) noexcept :
        value(int(v)), is_ordered(true) {}      // exposition only
    constexpr explicit
      partial_ordering(ord v) noexcept :
        value(int(v)), is_ordered(true) {}     // exposition only
    constexpr explicit
      partial_ordering(ncmp v) noexcept :
        value(int(v)), is_ordered(false) {}   // exposition only
 
  public:
    // valid values
    static const partial_ordering less;
    static const partial_ordering equivalent;
    static const partial_ordering greater;
    static const partial_ordering unordered;
 
    // comparisons
    friend constexpr bool operator==(partial_ordering v, /* unspecified */) noexcept;
    friend constexpr bool
      operator==(partial_ordering v, partial_ordering w) noexcept = default;
    friend constexpr bool operator< (partial_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator> (partial_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator<=(partial_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator>=(partial_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator< (/* unspecified */, partial_ordering v) noexcept;
    friend constexpr bool operator> (/* unspecified */, partial_ordering v) noexcept;
    friend constexpr bool operator<=(/* unspecified */, partial_ordering v) noexcept;
    friend constexpr bool operator>=(/* unspecified */, partial_ordering v) noexcept;
    friend constexpr partial_ordering
      operator<=>(partial_ordering v, /* unspecified */) noexcept;
    friend constexpr partial_ordering
      operator<=>(/* unspecified */, partial_ordering v) noexcept;
  };
 
  // valid values' definitions
  inline constexpr partial_ordering partial_ordering::less(ord::less);
  inline constexpr partial_ordering partial_ordering::equivalent(eq::equivalent);
  inline constexpr partial_ordering partial_ordering::greater(ord::greater);
  inline constexpr partial_ordering partial_ordering::unordered(ncmp::unordered);
}

```

#### Class std::weak_ordering

```
namespace std {
  class weak_ordering {
    int value;  // exposition only
 
    // exposition-only constructors
    constexpr explicit weak_ordering(eq v) noexcept : value(int(v)) {}  // exposition only
    constexpr explicit weak_ordering(ord v) noexcept : value(int(v)) {} // exposition only
 
  public:
    // valid values
    static const weak_ordering less;
    static const weak_ordering equivalent;
    static const weak_ordering greater;
 
    // conversions
    constexpr operator partial_ordering() const noexcept;
 
    // comparisons
    friend constexpr bool operator==(weak_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator==(weak_ordering v, weak_ordering w) noexcept = default;
    friend constexpr bool operator< (weak_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator> (weak_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator<=(weak_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator>=(weak_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator< (/* unspecified */, weak_ordering v) noexcept;
    friend constexpr bool operator> (/* unspecified */, weak_ordering v) noexcept;
    friend constexpr bool operator<=(/* unspecified */, weak_ordering v) noexcept;
    friend constexpr bool operator>=(/* unspecified */, weak_ordering v) noexcept;
    friend constexpr weak_ordering
      operator<=>(weak_ordering v, /* unspecified */) noexcept;
    friend constexpr weak_ordering
      operator<=>(/* unspecified */, weak_ordering v) noexcept;
  };
 
  // valid values' definitions
  inline constexpr weak_ordering weak_ordering::less(ord::less);
  inline constexpr weak_ordering weak_ordering::equivalent(eq::equivalent);
  inline constexpr weak_ordering weak_ordering::greater(ord::greater);
}

```

#### Class std::strong_ordering

```
namespace std {
  class strong_ordering {
    int value;  // exposition only
 
    // exposition-only constructors
    constexpr explicit strong_ordering(eq v) noexcept :
      value(int(v)) {}    // exposition only
    constexpr explicit strong_ordering(ord v) noexcept :
      value(int(v)) {}   // exposition only
 
  public:
    // valid values
    static const strong_ordering less;
    static const strong_ordering equal;
    static const strong_ordering equivalent;
    static const strong_ordering greater;
 
    // conversions
    constexpr operator partial_ordering() const noexcept;
    constexpr operator weak_ordering() const noexcept;
 
    // comparisons
    friend constexpr bool operator==(strong_ordering v, /* unspecified */) noexcept;
    friend constexpr bool
      operator==(strong_ordering v, strong_ordering w) noexcept = default;
    friend constexpr bool operator< (strong_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator> (strong_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator<=(strong_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator>=(strong_ordering v, /* unspecified */) noexcept;
    friend constexpr bool operator< (/* unspecified */, strong_ordering v) noexcept;
    friend constexpr bool operator> (/* unspecified */, strong_ordering v) noexcept;
    friend constexpr bool operator<=(/* unspecified */, strong_ordering v) noexcept;
    friend constexpr bool operator>=(/* unspecified */, strong_ordering v) noexcept;
    friend constexpr strong_ordering
      operator<=>(strong_ordering v, /* unspecified */) noexcept;
    friend constexpr strong_ordering
    operator<=>(/* unspecified */, strong_ordering v) noexcept;
  };
 
  // valid values' definitions
  inline constexpr strong_ordering strong_ordering::less(ord::less);
  inline constexpr strong_ordering strong_ordering::equal(eq::equal);
  inline constexpr strong_ordering strong_ordering::equivalent(eq::equivalent);
  inline constexpr strong_ordering strong_ordering::greater(ord::greater);
}

```

#### Class std::compare_three_way

```
namespace std {
  struct compare_three_way {
    template<class T, class U>
    constexpr auto operator()(T&& t, U&& u) const;
 
    using is_transparent = /* unspecified */;
  };
}

```

### See also

|  |  |
| --- | --- |
| ****three-way comparison operator**** expression **lhs** `<=>` **rhs** (C++20) | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/compare&oldid=168515>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 January 2024, at 03:26.