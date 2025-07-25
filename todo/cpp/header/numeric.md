# Standard library header <numeric>

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | <cfloat> | | | | | | <climits> | | | | | | <compare> (C++20) | | | | | | <coroutine> (C++20) | | | | | | <csetjmp> | | | | | | <csignal> | | | | | | <cstdarg> | | | | | | <cstddef> | | | | | | <cstdint> (C++11) | | | | | | <cstdlib> | | | | | | <exception> | | | | | | <initializer_list> (C++11) | | | | | | <limits> | | | | | | <new> | | | | | | <source_location> (C++20) | | | | | | <stdfloat> (C++23) | | | | | | <typeinfo> | | | | | | <version> (C++20) | | | | | | Concepts | | | | | | <concepts> (C++20) | | | | | | Diagnostics | | | | | | <cassert> | | | | | | <cerrno> | | | | | | <debugging> (C++26) | | | | | | <stacktrace> (C++23) | | | | | | <stdexcept> | | | | | | <system_error> (C++11) | | | | | | Memory management | | | | | | <memory> | | | | | | <memory_resource> (C++17) | | | | | | <scoped_allocator> (C++11) | | | | | | Metaprogramming | | | | | | <type_traits> (C++11) | | | | | | <ratio> (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | <any> (C++17) | | | | | | <bitset> | | | | | | <bit> (C++20) | | | | | | <charconv> (C++17) | | | | | | <expected> (C++23) | | | | | | <format> (C++20) | | | | | | <functional> | | | | | | <optional> (C++17) | | | | | | <tuple> (C++11) | | | | | | <typeindex> (C++11) | | | | | | <utility> | | | | | | <variant> (C++17) | | | | | | Containers | | | | | | <array> (C++11) | | | | | | <deque> | | | | | | <flat_map> (C++23) | | | | | | <flat_set> (C++23) | | | | | | <forward_list> (C++11) | | | | | | <inplace_vector> (C++26) | | | | | | <list> | | | | | | <map> | | | | | | <mdspan> (C++23) | | | | | | <queue> | | | | | | <set> | | | | | | <span> (C++20) | | | | | | <stack> | | | | | | <unordered_map> (C++11) | | | | | | <unordered_set> (C++11) | | | | | | <vector> | | | | | | Iterators | | | | | | <iterator> | | | | | | Ranges | | | | | | <generator> (C++23) | | | | | | <ranges> (C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | <algorithm> | | | | | | ****<numeric>**** | | | | | | Strings | | | | | | <cctype> | | | | | | <cstring> | | | | | | <cuchar> (C++11) | | | | | | <cwchar> | | | | | | <cwctype> | | | | | | <string_view> (C++17) | | | | | | <string> | | | | | | Text processing | | | | | | <clocale> | | | | | | <codecvt> (C++11/17/26\*) | | | | | | <locale> | | | | | | <regex> (C++11) | | | | | | <text_encoding> (C++26) | | | | | | Numerics | | | | | | <cfenv> (C++11) | | | | | | <cmath> | | | | | | <complex> | | | | | | <linalg> (C++26) | | | | | | <numbers> (C++20) | | | | | | <random> (C++11) | | | | | | <simd> (C++26) | | | | | | <valarray> | | | | | | Time | | | | | | <chrono> (C++11) | | | | | | <ctime> | | | | | | C compatibility | | | | | | <ccomplex> (C++11/17/20\*) | | | | | | <ciso646> (until C++20) | | | | | | <cstdalign> (C++11/17/20\*) | | | | | | <cstdbool> (C++11/17/20\*) | | | | | | <ctgmath> (C++11/17/20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Input/output | | | | | | <cinttypes> (C++11) | | | | | | <cstdio> | | | | | | <filesystem> (C++17) | | | | | | <fstream> | | | | | | <iomanip> | | | | | | <iosfwd> | | | | | | <iostream> | | | | | | <ios> | | | | | | <istream> | | | | | | <ostream> | | | | | | <print> (C++23) | | | | | | <spanstream> (C++23) | | | | | | <sstream> | | | | | | <streambuf> | | | | | | <strstream> (C++98/26\*) | | | | | | <syncstream> (C++20) | | | | | | Concurrency support | | | | | | <atomic> (C++11) | | | | | | <barrier> (C++20) | | | | | | <condition_variable> (C++11) | | | | | | <future> (C++11) | | | | | | <hazard_pointer> (C++26) | | | | | | <latch> (C++20) | | | | | | <mutex> (C++11) | | | | | | <rcu> (C++26) | | | | | | <semaphore> (C++20) | | | | | | <shared_mutex> (C++14) | | | | | | <stdatomic.h> (C++23) | | | | | | <stop_token> (C++20) | | | | | | <thread> (C++11) | | | | | | Execution support | | | | | | <execution> (C++17) | | | | | |  | | | | | |  | | | | | |

This header is part of the numeric library.

|  |  |
| --- | --- |
| Functions | |
| iota(C++11) | fills a range with successive increments of the starting value   (function template) |
| ranges::iota(C++23) | fills a range with successive increments of the starting value (algorithm function object) |
| accumulate | sums up or folds a range of elements   (function template) |
| reduce(C++17) | similar to std::accumulate, except out of order   (function template) |
| transform_reduce(C++17) | applies an invocable, then reduces out of order   (function template) |
| inner_product | computes the inner product of two ranges of elements   (function template) |
| adjacent_difference | computes the differences between adjacent elements in a range   (function template) |
| partial_sum | computes the partial sum of a range of elements   (function template) |
| inclusive_scan(C++17) | similar to std::partial_sum, includes the ith input element in the ith sum   (function template) |
| exclusive_scan(C++17) | similar to std::partial_sum, excludes the ith input element from the ith sum   (function template) |
| transform_inclusive_scan(C++17) | applies an invocable, then calculates inclusive scan   (function template) |
| transform_exclusive_scan(C++17) | applies an invocable, then calculates exclusive scan   (function template) |
| gcd(C++17) | computes the greatest common divisor of two integers   (function template) |
| lcm(C++17) | computes the least common multiple of two integers   (function template) |
| midpoint(C++20) | midpoint between two numbers or pointers   (function template) |
| add_sat(C++26) | saturating addition operation on two integers   (function template) |
| sub_sat(C++26) | saturating subtraction operation on two integers   (function template) |
| mul_sat(C++26) | saturating multiplication operation on two integers   (function template) |
| div_sat(C++26) | saturating division operation on two integers   (function template) |
| saturate_cast(C++26) | returns an integer value clamped to the range of another integer type   (function template) |

### Synopsis

```
namespace std {
  // accumulate
  template<class InputIt, class T>
    constexpr T accumulate(InputIt first, InputIt last, T init);
  template<class InputIt, class T, class BinaryOperation>
    constexpr T accumulate(InputIt first, InputIt last, T init, BinaryOperation binary_op);
 
  // reduce
  template<class InputIt>
    constexpr typename iterator_traits<InputIt>::value_type
      reduce(InputIt first, InputIt last);
  template<class InputIt, class T>
    constexpr T reduce(InputIt first, InputIt last, T init);
  template<class InputIt, class T, class BinaryOperation>
    constexpr T reduce(InputIt first, InputIt last, T init, BinaryOperation binary_op);
  template<class ExecutionPolicy, class ForwardIt>
    typename iterator_traits<ForwardIt>::value_type
      reduce(ExecutionPolicy&& exec,
             ForwardIt first, ForwardIt last);
  template<class ExecutionPolicy, class ForwardIt, class T>
    T reduce(ExecutionPolicy&& exec,
             ForwardIt first, ForwardIt last, T init);
  template<class ExecutionPolicy, class ForwardIt, class T, class BinaryOperation>
    T reduce(ExecutionPolicy&& exec,
             ForwardIt first, ForwardIt last, T init, BinaryOperation binary_op);
 
  // inner product
  template<class InputIt1, class InputIt2, class T>
    constexpr T inner_product(InputIt1 first1, InputIt1 last1,
                              InputIt2 first2, T init);
  template<class InputIt1, class InputIt2, class T,
           class BinaryOperation1, class BinaryOperation2>
    constexpr T inner_product(InputIt1 first1, InputIt1 last1,
                              InputIt2 first2, T init,
                              BinaryOperation1 binary_op1,
                              BinaryOperation2 binary_op2);
 
  // transform reduce
  template<class InputIt1, class InputIt2, class T>
    constexpr T transform_reduce(InputIt1 first1, InputIt1 last1,
                                 InputIt2 first2,
                                 T init);
  template<class InputIt1, class InputIt2, class T,
           class BinaryOperation1, class BinaryOperation2>
    constexpr T transform_reduce(InputIt1 first1, InputIt1 last1,
                                 InputIt2 first2,
                                 T init,
                                 BinaryOperation1 binary_op1,
                                 BinaryOperation2 binary_op2);
  template<class InputIt, class T,
           class BinaryOperation, class UnaryOperation>
    constexpr T transform_reduce(InputIt first, InputIt last,
                                 T init,
                                 BinaryOperation binary_op, UnaryOperation unary_op);
  template<class ExecutionPolicy,
           class ForwardIt1, class ForwardIt2, class T>
    T transform_reduce(ExecutionPolicy&& exec,
                       ForwardIt1 first1, ForwardIt1 last1,
                       ForwardIt2 first2,
                       T init);
  template<class ExecutionPolicy,
           class ForwardIt1, class ForwardIt2, class T,
           class BinaryOperation1, class BinaryOperation2>
    T transform_reduce(ExecutionPolicy&& exec,
                       ForwardIt1 first1, ForwardIt1 last1,
                       ForwardIt2 first2,
                       T init,
                       BinaryOperation1 binary_op1,
                       BinaryOperation2 binary_op2);
  template<class ExecutionPolicy,
           class ForwardIt, class T,
           class BinaryOperation, class UnaryOperation>
    T transform_reduce(ExecutionPolicy&& exec,
                       ForwardIt first, ForwardIt last,
                       T init,
                       BinaryOperation binary_op, UnaryOperation unary_op);
 
  // partial sum
  template<class InputIt, class OutputIt>
    constexpr OutputIt partial_sum(InputIt first,
                                   InputIt last,
                                   OutputIt result);
  template<class InputIt, class OutputIt, class BinaryOperation>
    constexpr OutputIt partial_sum(InputIt first,
                                   InputIt last,
                                   OutputIt result,
                                   BinaryOperation binary_op);
 
  // exclusive scan
  template<class InputIt, class OutputIt, class T>
    constexpr OutputIt exclusive_scan(InputIt first, InputIt last,
                                      OutputIt result,
                                      T init);
  template<class InputIt, class OutputIt, class T, class BinaryOperation>
    constexpr OutputIt exclusive_scan(InputIt first, InputIt last,
                                      OutputIt result,
                                      T init, BinaryOperation binary_op);
  template<class ExecutionPolicy, class ForwardIt1, class ForwardIt2, class T>
    ForwardIt2 exclusive_scan(ExecutionPolicy&& exec,
                              ForwardIt1 first, ForwardIt1 last,
                              ForwardIt2 result,
                              T init);
  template<class ExecutionPolicy, class ForwardIt1, class ForwardIt2, class T,
           class BinaryOperation>
    ForwardIt2 exclusive_scan(ExecutionPolicy&& exec,
                              ForwardIt1 first, ForwardIt1 last,
                              ForwardIt2 result,
                              T init, BinaryOperation binary_op);
 
  // inclusive scan
  template<class InputIt, class OutputIt>
    constexpr OutputIt inclusive_scan(InputIt first, InputIt last, OutputIt result);
  template<class InputIt, class OutputIt, class BinaryOperation>
    constexpr OutputIt inclusive_scan(InputIt first, InputIt last,
                                      OutputIt result,
                                      BinaryOperation binary_op);
  template<class InputIt, class OutputIt, class BinaryOperation, class T>
    constexpr OutputIt inclusive_scan(InputIt first, InputIt last,
                                      OutputIt result,
                                      BinaryOperation binary_op, T init);
  template<class ExecutionPolicy, class ForwardIt1, class ForwardIt2>
    ForwardIt2 inclusive_scan(ExecutionPolicy&& exec,
                              ForwardIt1 first, ForwardIt1 last,
                              ForwardIt2 result);
  template<class ExecutionPolicy, class ForwardIt1, class ForwardIt2,
           class BinaryOperation>
    ForwardIt2 inclusive_scan(ExecutionPolicy&& exec,
                              ForwardIt1 first, ForwardIt1 last,
                              ForwardIt2 result,
                              BinaryOperation binary_op);
  template<class ExecutionPolicy, class ForwardIt1, class ForwardIt2,
           class BinaryOperation, class T>
    ForwardIt2 inclusive_scan(ExecutionPolicy&& exec,
                              ForwardIt1 first, ForwardIt1 last,
                              ForwardIt2 result,
                              BinaryOperation binary_op, T init);
 
  // transform exclusive scan
  template<class InputIt, class OutputIt, class T,
           class BinaryOperation, class UnaryOperation>
    constexpr OutputIt transform_exclusive_scan(InputIt first, InputIt last,
                                                OutputIt result,
                                                T init,
                                                BinaryOperation binary_op,
                                                UnaryOperation unary_op);
  template<class ExecutionPolicy,
           class ForwardIt1, class ForwardIt2, class T,
           class BinaryOperation, class UnaryOperation>
    ForwardIt2 transform_exclusive_scan(ExecutionPolicy&& exec,
                                        ForwardIt1 first, ForwardIt1 last,
                                        ForwardIt2 result,
                                        T init,
                                        BinaryOperation binary_op,
                                        UnaryOperation unary_op);
 
  // transform inclusive scan
  template<class InputIt, class OutputIt,
           class BinaryOperation, class UnaryOperation>
    constexpr OutputIt transform_inclusive_scan(InputIt first, InputIt last,
                                                OutputIt result,
                                                BinaryOperation binary_op,
                                                UnaryOperation unary_op);
  template<class InputIt, class OutputIt,
           class BinaryOperation, class UnaryOperation, class T>
    constexpr OutputIt transform_inclusive_scan(InputIt first, InputIt last,
                                                OutputIt result,
                                                BinaryOperation binary_op,
                                                UnaryOperation unary_op,
                                                T init);
  template<class ExecutionPolicy,
           class ForwardIt1, class ForwardIt2,
           class BinaryOperation, class UnaryOperation>
    ForwardIt2 transform_inclusive_scan(ExecutionPolicy&& exec,
                                        ForwardIt1 first, ForwardIt1 last,
                                        ForwardIt2 result,
                                        BinaryOperation binary_op,
                                        UnaryOperation unary_op);
  template<class ExecutionPolicy,
           class ForwardIt1, class ForwardIt2,
           class BinaryOperation, class UnaryOperation, class T>
    ForwardIt2 transform_inclusive_scan(ExecutionPolicy&& exec,
                                        ForwardIt1 first, ForwardIt1 last,
                                        ForwardIt2 result,
                                        BinaryOperation binary_op,
                                        UnaryOperation unary_op,
                                        T init);
 
  // adjacent difference
  template<class InputIt, class OutputIt>
    constexpr OutputIt adjacent_difference(InputIt first, InputIt last,
                                           OutputIt result);
  template<class InputIt, class OutputIt, class BinaryOperation>
    constexpr OutputIt adjacent_difference(InputIt first, InputIt last,
                                           OutputIt result,
                                           BinaryOperation binary_op);
  template<class ExecutionPolicy, class ForwardIt1, class ForwardIt2>
    ForwardIt2 adjacent_difference(ExecutionPolicy&& exec,
                                   ForwardIt1 first, ForwardIt1 last,
                                   ForwardIt2 result);
  template<class ExecutionPolicy, class ForwardIt1, class ForwardIt2,
           class BinaryOperation>
    ForwardIt2 adjacent_difference(ExecutionPolicy&& exec,
                                   ForwardIt1 first, ForwardIt1 last,
                                   ForwardIt2 result,
                                   BinaryOperation binary_op);
 
  // iota
  template<class ForwardIt, class T>
    constexpr void iota(ForwardIt first, ForwardIt last, T value);
 
  namespace ranges {
    template<class O, class T>
      using iota_result = out_value_result<O, T>;
 
    template<input_or_output_iterator O, sentinel_for<O> S, weakly_incrementable T>
      requires indirectly_writable<O, const T&>
      constexpr iota_result<O, T> iota(O first, S last, T value);
 
    template<weakly_incrementable T, output_range<const T&> R>
      constexpr iota_result<borrowed_iterator_t<R>, T> iota(R&& r, T value);
  }
 
  // greatest common divisor
  template<class M, class N>
    constexpr common_type_t<M, N> gcd(M m, N n);
 
  // least common multiple
  template<class M, class N>
    constexpr common_type_t<M, N> lcm(M m, N n);
 
  // midpoint
  template<class T>
    constexpr T midpoint(T a, T b) noexcept;
  template<class T>
    constexpr T* midpoint(T* a, T* b);
 
  // saturation arithmetic
  template<class T>
    constexpr T add_sat(T x, T y) noexcept;           // freestanding
  template<class T>
    constexpr T sub_sat(T x, T y) noexcept;           // freestanding
  template<class T>
    constexpr T mul_sat(T x, T y) noexcept;           // freestanding
  template<class T>
    constexpr T div_sat(T x, T y) noexcept;           // freestanding
  template<class T, class U>
    constexpr T saturate_cast(U x) noexcept;          // freestanding
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/header/numeric&oldid=163892>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 November 2023, at 06:16.