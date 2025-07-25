# Standard library header <future> (C++11)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | <numeric> | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | ****<future>**** (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the thread support library.

|  |  |
| --- | --- |
| Classes | |
| promise(C++11) | stores a value for asynchronous retrieval   (class template) |
| packaged_task(C++11) | packages a function to store its return value for asynchronous retrieval   (class template) |
| future(C++11) | waits for a value that is set asynchronously   (class template) |
| shared_future(C++11) | waits for a value (possibly referenced by other futures) that is set asynchronously   (class template) |
| launch(C++11) | specifies the launch policy for std::async   (enum) |
| future_status(C++11) | specifies the results of timed waits performed on std::future and std::shared_future   (enum) |
| future_error(C++11) | reports an error related to futures or promises   (class) |
| future_errc(C++11) | identifies the future error codes   (enum) |
| std::uses_allocator<std::promise>(C++11) | specializes the std::uses_allocator type trait   (class template specialization) |
| std::uses_allocator<std::packaged_task>(C++11) (until C++17) | specializes the std::uses_allocator type trait   (class template specialization) |
| Functions | |
| async(C++11) | runs a function asynchronously (potentially in a new thread) and returns a std::future that will hold the result   (function template) |
| future_category(C++11) | identifies the future error category   (function) |
| std::swap(std::promise)(C++11) | specializes the std::swap algorithm   (function template) |
| std::swap(std::packaged_task)(C++11) | specializes the std::swap algorithm   (function template) |

### Synopsis

```
namespace std {
  enum class future_errc {
    broken_promise = /* implementation-defined */,
    future_already_retrieved = /* implementation-defined */,
    promise_already_satisfied = /* implementation-defined */,
    no_state = /* implementation-defined */
  };
 
  enum class launch : /* unspecified */ {
    async = /* unspecified */,
    deferred = /* unspecified */,
    /* implementation-defined */
  };
 
  enum class future_status {
    ready,
    timeout,
    deferred
  };
 
  template<> struct is_error_code_enum<future_errc> : public true_type { };
  error_code make_error_code(future_errc e) noexcept;
  error_condition make_error_condition(future_errc e) noexcept;
 
  const error_category& future_category() noexcept;
 
  class future_error;
 
  template<class R> class promise;
  template<class R> class promise<R&>;
  template<> class promise<void>;
 
  template<class R>
    void swap(promise<R>& x, promise<R>& y) noexcept;
 
  template<class R, class Alloc>
    struct uses_allocator<promise<R>, Alloc>;
 
  template<class R> class future;
  template<class R> class future<R&>;
  template<> class future<void>;
 
  template<class R> class shared_future;
  template<class R> class shared_future<R&>;
  template<> class shared_future<void>;
 
  template<class> class packaged_task;  // not defined
  template<class R, class... ArgTypes>
    class packaged_task<R(ArgTypes...)>;
 
  template<class R, class... ArgTypes>
    void swap(packaged_task<R(ArgTypes...)>&, packaged_task<R(ArgTypes...)>&) noexcept;
 
  template<class F, class... Args>
    future<invoke_result_t<decay_t<F>, decay_t<Args>...>>
      async(F&& f, Args&&... args);
  template<class F, class... Args>
    future<invoke_result_t<decay_t<F>, decay_t<Args>...>>
      async(launch policy, F&& f, Args&&... args);
}

```

#### Class std::future_error

```
namespace std {
  class future_error : public logic_error {
  public:
    explicit future_error(future_errc e);
 
    const error_code& code() const noexcept;
    const char*       what() const noexcept;
 
  private:
    error_code ec_;             // exposition only
  };
}

```

#### Class template std::promise

```
namespace std {
  template<class R>
  class promise {
  public:
    promise();
    template<class Allocator>
      promise(allocator_arg_t, const Allocator& a);
    promise(promise&& rhs) noexcept;
    promise(const promise&) = delete;
    ~promise();
 
    // assignment
    promise& operator=(promise&& rhs) noexcept;
    promise& operator=(const promise&) = delete;
    void swap(promise& other) noexcept;
 
    // retrieving the result
    future<R> get_future();
 
    // setting the result
    void set_value(/* see description */);
    void set_exception(exception_ptr p);
 
    // setting the result with deferred notification
    void set_value_at_thread_exit(/* see description */);
    void set_exception_at_thread_exit(exception_ptr p);
  };
 
  template<class R>
    void swap(promise<R>& x, promise<R>& y) noexcept;
 
  template<class R, class Alloc>
    struct uses_allocator<promise<R>, Alloc>;
}

```

#### Class template std::future

```
namespace std {
  template<class R>
  class future {
  public:
    future() noexcept;
    future(future&&) noexcept;
    future(const future&) = delete;
    ~future();
    future& operator=(const future&) = delete;
    future& operator=(future&&) noexcept;
    shared_future<R> share() noexcept;
 
    // retrieving the value
    /* see description */ get();
 
    // functions to check state
    bool valid() const noexcept;
 
    void wait() const;
    template<class Rep, class Period>
      future_status wait_for(const chrono::duration<Rep, Period>& rel_time) const;
    template<class Clock, class Duration>
      future_status wait_until(const chrono::time_point<Clock, Duration>& abs_time) const;
  };
}

```

#### Class template std::shared_future

```
namespace std {
  template<class R>
  class shared_future {
  public:
    shared_future() noexcept;
    shared_future(const shared_future& rhs) noexcept;
    shared_future(future<R>&&) noexcept;
    shared_future(shared_future&& rhs) noexcept;
    ~shared_future();
    shared_future& operator=(const shared_future& rhs) noexcept;
    shared_future& operator=(shared_future&& rhs) noexcept;
 
    // retrieving the value
    /* see description */ get() const;
 
    // functions to check state
    bool valid() const noexcept;
 
    void wait() const;
    template<class Rep, class Period>
      future_status wait_for(const chrono::duration<Rep, Period>& rel_time) const;
    template<class Clock, class Duration>
      future_status wait_until(const chrono::time_point<Clock, Duration>& abs_time) const;
  };
}

```

#### Class template std::packaged_task

```
namespace std {
  template<class> class packaged_task;  // not defined
 
  template<class R, class... ArgTypes>
  class packaged_task<R(ArgTypes...)> {
  public:
    // construction and destruction
    packaged_task() noexcept;
    template<class F>
      explicit packaged_task(F&& f);
    ~packaged_task();
 
    // no copy
    packaged_task(const packaged_task&) = delete;
    packaged_task& operator=(const packaged_task&) = delete;
 
    // move support
    packaged_task(packaged_task&& rhs) noexcept;
    packaged_task& operator=(packaged_task&& rhs) noexcept;
    void swap(packaged_task& other) noexcept;
 
    bool valid() const noexcept;
 
    // result retrieval
    future<R> get_future();
 
    // execution
    void operator()(ArgTypes... );
    void make_ready_at_thread_exit(ArgTypes...);
 
    void reset();
  };
 
  template<class R, class... ArgTypes>
  packaged_task(R (*)(ArgTypes...)) -> packaged_task<R(ArgTypes...)>;
 
  template<class F> packaged_task(F) -> packaged_task</* see description */>;
 
  template<class R, class... ArgTypes>
    void swap(packaged_task<R(ArgTypes...)>& x, packaged_task<R(ArgTypes...)>& y) noexcept;
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/future&oldid=163996>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 November 2023, at 07:22.