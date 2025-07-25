# Standard library header <stop_token> (C++20)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | ****<stop_token>**** (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the thread support library.

|  |  |
| --- | --- |
| Classes | |
| stop_token(C++20) | an interface for querying if a std::jthread cancellation request has been made   (class) |
| stop_source(C++20) | class representing a request to stop one or more std::jthreads   (class) |
| stop_callback(C++20) | an interface for registering callbacks on std::jthread cancellation   (class template) |
| never_stop_token(C++26) | provides a stop token interface that a stop is never possible nor requested   (class) |
| inplace_stop_token")(C++26) | a stop token that references stop state of its associated `std::inplace_stop_source` object   (class) |
| inplace_stop_source")(C++26) | a `stoppable-source` that is the sole owner of the stop state   (class) |
| inplace_stop_callback")(C++26) | a stop callback for `std::inplace_stop_token`   (class template) |
| Alias templates | |
| stop_callback_for_t(C++26) | obtains the callback type for a given stop token type (alias template) |
| Concepts | |
| stoppable_token(C++26) | specifies the basic interface of stop tokens which allows queries for stop requests and whether the stop request is possible   (concept) |
| unstoppable_token(C++26) | specifies a stop token that does not allow stopping   (concept) |
| Tags | |
| nostopstatenostopstate_t(C++20) | a tag used for `stop_source` to indicate no associated stop-state upon construction (tag) |

### Synopsis

```
namespace std {
  // stop token concepts
  template<class CallbackFn, class Token, class Init = CallbackFn>
    concept /*stoppable-callback-for*/ = /* see description */; // exposition only
 
  template<class Token>
    concept stoppable_token = /* see description */;
 
  template<class Token>
    concept unstoppable_token = /* see description */;
 
  template<class Source>
    concept /*stoppable-source*/ = /* see description */; // exposition only
 
  // class stop_token
  class stop_token;
 
  // class stop_source
  class stop_source;
 
  // no-shared-stop-state indicator
  struct nostopstate_t {
    explicit nostopstate_t() = default;
  };
  inline constexpr nostopstate_t nostopstate{};
 
  // class template stop_callback
  template<class Callback>
  class stop_callback;
 
  // class never_stop_token
  class never_stop_token;
 
  // class inplace_stop_token
  class inplace_stop_token;
 
  // class inplace_stop_source
  class inplace_stop_source;
 
  // class template inplace_stop_callback
  template<class CallbackFn>
    class inplace_stop_callback;
 
  template<class T, class CallbackFn>
    using stop_callback_for_t = T::template callback_type<CallbackFn>;
}

```

#### Stop token concepts

```
namespace std {
  template<class CallbackFn, class Token, class Init = CallbackFn>
    concept /*stoppable-callback-for*/ =                         // exposition only
      invocable<CallbackFn> &&
      constructible_from<CallbackFn, Init> &&
      requires { typename stop_callback_for_t<Token, CallbackFn>; } &&
      constructible_from<stop_callback_for_t<Token, CallbackFn>, const Token&, Init>;
 
  template<template<class> class>
    struct /*check-type-alias-exists*/;                          // exposition only
 
  template<class Token>
    concept stoppable_token = 
      requires (const Token tok) {
        typename /*check-type-alias-exists*/<Token::template callback_type>;
        { tok.stop_requested() } noexcept -> same_as<bool>;
        { tok.stop_possible() } noexcept -> same_as<bool>;
        { Token(tok) } noexcept; // see implicit expression variations
      } &&
      copyable<Token> &&
      equality_comparable<Token>;
 
  template<class Token>
    concept unstoppable_token = 
      stoppable_token<Token> &&
      requires (const Token tok) {
        requires bool_constant<(!tok.stop_possible())>::value;
      };
 
  template<class Source>
    concept /*stoppable-source*/ =                               // exposition only
      requires (Source& src, const Source csrc) {
        { csrc.get_token() } -> stoppable_token;
        { csrc.stop_possible() } noexcept -> same_as<bool>;
        { csrc.stop_requested() } noexcept -> same_as<bool>;
        { src.request_stop() } -> same_as<bool>;
      };
}

```

#### Class std::stop_token

```
namespace std {
  class stop_token {
  public:
    template<class CallbackFn>
      using callback_type = stop_callback<CallbackFn>;
 
    // constructors, copy, and assignment
    stop_token() noexcept = default;
 
    // member functions
    void swap(stop_token&) noexcept;
 
    // stop handling
    bool stop_requested() const noexcept;
    bool stop_possible() const noexcept;
 
    friend bool operator==(const stop_token& lhs, const stop_token& rhs) noexcept;
    friend void swap(stop_token& lhs, stop_token& rhs) noexcept;
 
  private:
    shared_ptr</*unspecified*/> stop_state_; // exposition only
  };
}

```

#### Class std::stop_source

```
namespace std {
  class stop_source {
  public:
    // constructors, copy, and assignment
    stop_source();
    explicit stop_source(nostopstate_t) noexcept {}
 
    // member functions
    void swap(stop_source&) noexcept;
 
    // stop handling
    stop_token get_token() const noexcept;
    bool stop_possible() const noexcept;
    bool stop_requested() const noexcept;
    bool request_stop() noexcept;
 
    friend bool
    operator==(const stop_source& lhs, const stop_source& rhs) noexcept;
    friend void swap(stop_source& lhs, stop_source& rhs) noexcept;
 
  private:
    shared_ptr</*unspecified*/> stop_state_; // exposition only
  };
}

```

#### Class template std::stop_callback

```
namespace std {
  template<class CallbackFn>
  class stop_callback {
  public:
    using callback_type = CallbackFn;
 
    // constructors and destructor
    template<class Init>
    explicit stop_callback(const stop_token& st, Init&& init)
        noexcept(is_nothrow_constructible_v<CallbackFn, Init>);
    template<class Init>
    explicit stop_callback(stop_token&& st, Init&& init)
        noexcept(is_nothrow_constructible_v<CallbackFn, Init>);
    ~stop_callback();
 
    stop_callback(const stop_callback&) = delete;
    stop_callback(stop_callback&&) = delete;
    stop_callback& operator=(const stop_callback&) = delete;
    stop_callback& operator=(stop_callback&&) = delete;
 
  private:
    CallbackFn callback_fn_;      // exposition only
  };
 
  template<class CallbackFn>
  stop_callback(stop_token, CallbackFn) -> stop_callback<CallbackFn>;
}

```

#### Class template std::never_stop_token

```
namespace std {
  class never_stop_token {
    struct /*callback-type*/ {       // exposition only
      explicit /*callback-type*/(never_stop_token, auto&&) noexcept {}
    };
 
  public:
    template<class>
      using callback_type = /*callback-type*/;
 
    static constexpr bool stop_requested() noexcept { return false; }
    static constexpr bool stop_posible() noexcept { return false; }
 
    bool operator==(const never_stop_token&) const = default;
  };
}

```

#### Class template std::inplace_stop_token

```
namespace std {
  class inplace_stop_token {
  public:
    template<class CallbackFn>
      using callback_type = inplace_stop_callback<CallbackFn>;
 
    inplace_stop_token() = default;
    bool operator==(const inplace_stop_token&) const = default;
 
    // member functions
    bool stop_requested() const noexcept;
    bool stop_possible() const noexcept;
    void swap(inplace_stop_token&) noexcept;
 
  private:
    const inplace_stop_source* stop_source_ = nullptr; // exposition only
  };
}

```

#### Class template std::inplace_stop_source

```
namespace std {
  class inplace_stop_source {
    // constructors, assignments, and destructor
    constexpr inplace_stop_source() noexcept;
 
    inplace_stop_source(inplace_stop_source&&) = delete;
    inplace_stop_source(const inplace_stop_source&) = delete;
    inplace_stop_source& operator=(inplace_stop_source&&) = delete;
    inplace_stop_source& operator=(const inplace_stop_source&) = delete;
    ~inplace_stop_source();
 
    // stop handling
    constexpr inplace_stop_token get_token() const noexcept;
    static constexpr bool stop_possible() noexcept { return true; }
    bool stop_requested() const noexcept;
    bool request_stop() noexcept;
  };
}

```

#### Class template std::inplace_stop_callback

```
namespace std {
  template<class CallbackFn>
  class inplace_stop_callback {
  public:
    using callback_type = CallbackFn;
 
    // constructors and destructor
    template<class Init>
    explicit inplace_stop_callback(inplace_stop_token st, Init&& init)
        noexcept(is_nothrow_constructible_v<CallbackFn, Init>);
    ~inplace_stop_callback();
 
    inplace_stop_callback(const inplace_stop_callback&) = delete;
    inplace_stop_callback(inplace_stop_callback&&) = delete;
    inplace_stop_callback& operator=(const inplace_stop_callback&) = delete;
    inplace_stop_callback& operator=(inplace_stop_callback&&) = delete;
 
  private:
    CallbackFn callback_fn_;      // exposition only
  };
 
  template<class CallbackFn>
  inplace_stop_callback(inplace_stop_token, CallbackFn) 
    -> inplace_stop_callback<CallbackFn>;
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/stop_token&oldid=177423>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 31 October 2024, at 18:49.