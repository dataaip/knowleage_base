# std::expected<T,E>::expected

From cppreference.com
< cpp‎ | utility‎ | expected
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

Utilities library

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Language support | | | | | | Type support (basic types, RTTI) | | | | | | Library feature-test macros (C++20) | | | | | | Program utilities | | | | | | Coroutine support (C++20) | | | | | | Variadic functions | | | | | | is_constant_evaluated(C++20) | | | | | | is_within_lifetime(C++26) | | | | | | initializer_list(C++11) | | | | | | source_location(C++20) | | | | | | Three-way comparison | | | | | | three_way_comparablethree_way_comparable_with(C++20)(C++20) | | | | | | strong_ordering(C++20) | | | | | | weak_ordering(C++20) | | | | | | partial_ordering(C++20) | | | | | | common_comparison_category(C++20) | | | | | | compare_three_way_result(C++20) | | | | | | compare_three_way(C++20) | | | | | | strong_order(C++20) | | | | | | weak_order(C++20) | | | | | | partial_order(C++20) | | | | | | compare_strong_order_fallback(C++20) | | | | | | compare_weak_order_fallback(C++20) | | | | | | compare_partial_order_fallback(C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_eqis_ltis_lteq(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_neqis_gtis_gteq(C++20)(C++20)(C++20) | | | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | General utilities | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function objects | | | | | | Bit manipulation (C++20) | | | | | | bitset | | | | | | hash(C++11) | | | | | | | Relational operators (deprecated in C++20) | | | | | | |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator!=rel_ops::operator> | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rel_ops::operator<=rel_ops::operator>= | | | | | | | Integer comparison functions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_equalcmp_lesscmp_less_than(C++20)(C++20)(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | cmp_not_equalcmp_greatercmp_greater_than(C++20)(C++20)(C++20) | | | | | | | in_range(C++20) | | | | | | Swap and type operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | swap | | | | | | ranges::swap(C++20) | | | | | | exchange(C++14) | | | | | | declval(C++11) | | | | | | to_underlying(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | forward(C++11) | | | | | | forward_like(C++23) | | | | | | move(C++11) | | | | | | move_if_noexcept(C++11) | | | | | | as_const(C++17) | | | | | | | Common vocabulary types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | pair | | | | | | tuple(C++11) | | | | | | optional(C++17) | | | | | | any(C++17) | | | | | | variant(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | tuple_size(C++11) | | | | | | tuple_element(C++11) | | | | | | apply(C++17) | | | | | | make_from_tuple(C++17) | | | | | | expected(C++23) | | | | | | |  | | | | | |  | | | | | |  | | | | | | |

std::expected

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| ****expected::expected**** | | | | |
| expected::~expected | | | | |
| expected::operator= | | | | |
| Observers | | | | |
| expected::operator->expected::operator\* | | | | |
| expected::operator boolexpected::has_value | | | | |
| expected::value | | | | |
| expected::error | | | | |
| expected::value_or | | | | |
| expected::error_or | | | | |
| Monadic operations | | | | |
| expected::and_then | | | | |
| expected::or_else | | | | |
| expected::transform | | | | |
| expected::transform_error | | | | |
| Modifiers | | | | |
| expected::emplace | | | | |
| expected::swap | | | | |
| Non-member functions | | | | |
| operator==(std::expected) | | | | |
| swap(std::expected) | | | | |
| Helper classes | | | | |
| unexpected | | | | |
| bad_expected_access | | | | |
| unexpect_tunexpect | | | | |

|  |  |  |
| --- | --- | --- |
| Main template |  |  |
| constexpr expected(); | (1) | (since C++23) |
| constexpr expected( const expected& other ); | (2) | (since C++23) |
| constexpr expected( expected&& other ) noexcept(/\* see below \*/); | (3) | (since C++23) |
| template< class U, class G >  constexpr expected( const expected<U, G>& other ); | (4) | (since C++23)  (conditionally explicit) |
| template< class U, class G >  constexpr expected( expected<U, G>&& other ); | (5) | (since C++23)  (conditionally explicit) |
| template< class U = T >  constexpr explicit(!std::is_convertible_v<U, T>) expected( U&& v ); | (6) | (since C++23) |
| template< class G >  constexpr explicit(!std::is_convertible_v<const G&, E>)     expected( const std::unexpected<G>& e ); | (7) | (since C++23) |
| template< class G >  constexpr explicit(!std::is_convertible_v<G, E>)     expected( std::unexpected<G>&& e ); | (8) | (since C++23) |
| template< class... Args >  constexpr explicit expected( std::in_place_t, Args&&... args ); | (9) | (since C++23) |
| template< class U, class... Args >  constexpr explicit      expected( std::in_place_t, std::initializer_list<U> il, Args&&... args ); | (10) | (since C++23) |
| template< class... Args >  constexpr explicit expected( std::unexpect_t, Args&&... args ); | (11) | (since C++23) |
| template< class U, class... Args >  constexpr explicit      expected( std::unexpect_t, std::initializer_list<U> il, Args&&... args ); | (12) | (since C++23) |
| void partial specialization |  |  |
| constexpr expected(); | (13) | (since C++23) |
| constexpr expected( const expected& other ); | (14) | (since C++23) |
| constexpr expected( expected&& other )      noexcept(std::is_nothrow_move_constructible_v<E>); | (15) | (since C++23) |
| template< class U, class G >  constexpr explicit(!std::is_convertible_v<const G&, E>)     expected( const expected<U, G>& other ); | (16) | (since C++23) |
| template< class U, class G >  constexpr explicit(!std::is_convertible_v<G, E>)     expected( expected<U, G>&& other ); | (17) | (since C++23) |
| template< class G >  constexpr explicit(!std::is_convertible_v<const G&, E>)     expected( const std::unexpected<G>& e ); | (18) | (since C++23) |
| template< class G >  constexpr explicit(!std::is_convertible_v<G, E>)     expected( std::unexpected<G>&& e ); | (19) | (since C++23) |
| template< class... Args >  constexpr explicit expected( std::in_place_t ); | (20) | (since C++23) |
| template< class... Args >  constexpr explicit expected( std::unexpect_t, Args&&... args ); | (21) | (since C++23) |
| template< class U, class... Args >  constexpr explicit      expected( std::unexpect_t, std::initializer_list<U> il, Args&&... args ); | (22) | (since C++23) |
|  |  |  |

Constructs a new `expected` object.

### Parameters

|  |  |  |
| --- | --- | --- |
| other | - | another `expected` object whose contained value is copied |
| e | - | `std::unexpected` object whose contained value is copied |
| v | - | value with which to initialize the contained value |
| args | - | arguments with which to initialize the contained value |
| il | - | initializer list with which to initialize the contained value |

### Effects

#### Primary template constructors

| Overload | Initialization method | Initializer for... | | `has_value()` after construction |
| --- | --- | --- | --- | --- |
| the expected value | the unexpected value |
| (1) | Value | (empty) | - | true |
| (2) | Direct (non-list) | \*other | other.error() | other.has_value()   - If true, only initializes the expected value. - If false, only initializes the unexpected value. |
| (3) | std::move(\*other) | std::move(other.error()) |
| (4) | std::forward<const U&>     (\*other) | std::forward<const G&>     (other.error()) |
| (5) | std::forward<U>(\*other) | std::forward<G>     (other.error()) |
| (6) | std::forward<U>(v) | - | true |
| (7) | - | std::forward<const G&>     (e.error()) | false |
| (8) | std::forward<G>(e.error()) |
| (9) | std::forward<Args>(args)... | - | true |
| (10) | il, std::forward<Args>(args)... |
| (11) | - | std::forward<Args>(args)... | false |
| (12) | il, std::forward<Args>(args)... |

#### void partial specialization constructors

| Overload | Initialization method | Initializer for the unexpected value | `has_value()` after construction |
| --- | --- | --- | --- |
| (13) | N/A | - | true |
| (14) | Direct (non-list) | rhs.error() | other.has_value()   - If false, initializes the unexpected value. |
| (15) | std::move(rhs.error) |
| (16) | std::forward<const G&>(rhs.error()) |
| (17) | std::forward<G>(rhs.error()) |
| (18) | std::forward<const G&>(e.error()) | false |
| (19) | std::forward<G>(e.error()) |
| (20) | N/A | - | true |
| (21) | Direct (non-list) | std::forward<Args>(args)... | false |
| (22) | il, std::forward<Args>(args)... |

### Constraints and supplement information

#### Primary template constructors

1) This overload participates in overload resolution only if std::is_default_constructible_v<T> is true.2) This constructor is defined as deleted unless std::is_copy_constructible_v<T> and std::is_copy_constructible_v<E> are both true. This constructor is trivial if std::is_trivially_copy_constructible_v<T> and std::is_trivially_copy_constructible_v<E> are both true.3) This overload participates in overload resolution only if std::is_move_constructible_v<T> and std::is_move_constructible_v<E> are both true. This constructor is trivial if std::is_trivially_move_constructible_v<T> and std::is_trivially_move_constructible_v<E> are both true.4,5) These overloads participate in overload resolution only if all following conditions are satisfied:

- For overload (4), std::is_constructible_v<T, const U&> and std::is_constructible_v<E, const G&> are both true.
- For overload (5), std::is_constructible_v<T, U> and std::is_constructible_v<E, G> are both true.
- If `T` is not (possibly cv-qualified) bool, the following 8 values are all false:
  - std::is_constructible_v<T, std::expected<U, G>&>
  - std::is_constructible_v<T, std::expected<U, G>>
  - std::is_constructible_v<T, const std::expected<U, G>&>
  - std::is_constructible_v<T, const std::expected<U, G>>
  - std::is_convertible_v<std::expected<U, G>&, T>
  - std::is_convertible_v<std::expected<U, G>, T>
  - std::is_convertible_v<const std::expected<U, G>&, T>
  - std::is_convertible_v<const std::expected<U, G>, T>
- The following 4 values are all false:
  - std::is_constructible_v<std::unexpected<E>, std::expected<U, G>&>
  - std::is_constructible_v<std::unexpected<E>, std::expected<U, G>>
  - std::is_constructible_v<std::unexpected<E>, const std::expected<U, G>&>
  - std::is_constructible_v<std::unexpected<E>, const std::expected<U, G>>
4) This constructor is explicit if std::is_convertible_v<const U&, T> or std::is_convertible_v<const G&, E> is false.5) This constructor is explicit if std::is_convertible_v<U, T> or std::is_convertible_v<G, E> is false.6) This overload participates in overload resolution only if all following conditions are satisfied:

- std::is_same_v<std::remove_cvref_t<U>, std::in_place_t> is false.
- std::is_same_v<std::expected<T, E>, std::remove_cvref_t<U>> is false.
- std::is_constructible_v<T, U> is true.
- std::remove_cvref_t<U> is not a specialization of `std::unexpected`.
- If `T` is (possibly cv-qualified) bool, std::remove_cvref_t<U> is not a specialization of `std::expected`.
7) This overload participates in overload resolution only if std::is_constructible_v<E, const G&> is true.8) This overload participates in overload resolution only if std::is_constructible_v<E, G> is true.9) This overload participates in overload resolution only if std::is_constructible_v<T, Args...> is true.10) This overload participates in overload resolution only if std::is_constructible_v<T, std::initializer_list<U>&, Args...> is true.11) This overload participates in overload resolution only if std::is_constructible_v<E, Args...> is true.12) This overload participates in overload resolution only if std::is_constructible_v<E, std::initializer_list<U>&, Args...> is true.

#### void partial specialization constructors

14) This constructor is defined as deleted unless std::is_copy_constructible_v<E> is true. This constructor is trivial if std::is_trivially_copy_constructible_v<E> is true.15) This overload participates in overload resolution only if std::is_move_constructible_v<E> is true. This constructor is trivial if std::is_trivially_move_constructible_v<E> is true.16,17) These overloads participate in overload resolution only if all following conditions are satisfied:

- For overload (16), std::is_constructible_v<E, const G&> is true.
- For overload (17), std::is_constructible_v<E, G> is true.
- std::is_void_v<U> is true.
- The following 4 values are all false:
  - std::is_constructible_v<std::unexpected<E>, std::expected<U, G>&>
  - std::is_constructible_v<std::unexpected<E>, std::expected<U, G>>
  - std::is_constructible_v<std::unexpected<E>, const std::expected<U, G>&>
  - std::is_constructible_v<std::unexpected<E>, const std::expected<U, G>>
18) This overload participates in overload resolution only if std::is_constructible_v<E, const G&> is true.19) This overload participates in overload resolution only if std::is_constructible_v<E, G> is true.21) This overload participates in overload resolution only if std::is_constructible_v<E, Args...> is true.22) This overload participates in overload resolution only if std::is_constructible_v<E, std::initializer_list<U>&, Args...> is true.

### Exceptions

#### Primary template constructors

1) Throws any exception thrown by the initialization of the expected value.2) Throws any exception thrown by the initialization of the expected or unexpected value.3) Throws any exception thrown by the initialization of the expected or unexpected value.noexcept specification:noexcept(std::is_nothrow_move_constructible_v<T>  
    && std::is_nothrow_move_constructible_v<E>)4,5) Throws any exception thrown by the initialization of the expected or unexpected value.6) Throws any exception thrown by the initialization of the expected value.7,8) Throws any exception thrown by the initialization of the unexpected value.9,10) Throws any exception thrown by the initialization of the expected value.11,12) Throws any exception thrown by the initialization of the unexpected value.

#### void partial specialization constructors

14-19) Throws any exception thrown by the initialization of the unexpected value.21,22) Throws any exception thrown by the initialization of the unexpected value.

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### See also

|  |  |
| --- | --- |
| unexpected(C++23) | represented as an unexpected value   (class template) |
| in_placein_place_typein_place_indexin_place_tin_place_type_tin_place_index_t(C++17) | in-place construction tag (tag) |
| unexpectunexpect_t(C++23) | in-place construction tag for unexpected value in `expected` (tag) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/expected/expected&oldid=179760>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 18 January 2025, at 21:56.