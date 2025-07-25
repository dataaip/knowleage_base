# std::bind_front, std::bind_back

From cppreference.com
< cpp‎ | utility‎ | functional
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

Function objects

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function wrappers | | | | | | function(C++11) | | | | | | move_only_function(C++23) | | | | | | copyable_function(C++26) | | | | | | function_ref(C++26) | | | | | | mem_fn(C++11) | | | | | | bad_function_call(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Partial function application | | | | | | ****bind_frontbind_back****(C++20)(C++23) | | | | | | bind(C++11) | | | | | | is_bind_expression(C++11) | | | | | | is_placeholder(C++11) | | | | | | _1, _2, _3, ...(C++11) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Function invocation | | | | | | invokeinvoke_r(C++17)(C++23) | | | | | | Identity function object | | | | | | identity(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Reference wrappers | | | | | | reference_wrapper(C++11) | | | | | | refcref(C++11)(C++11) | | | | | | unwrap_referenceunwrap_ref_decay(C++20)(C++20) | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operator wrappers | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | plus | | | | | | minus | | | | | | negate | | | | | | multiplies | | | | | | divides | | | | | | modulus | | | | | | bit_and | | | | | | bit_or | | | | | | bit_not(C++14) | | | | | | bit_xor | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_to | | | | | | not_equal_to | | | | | | greater | | | | | | less | | | | | | greater_equal | | | | | | less_equal | | | | | | logical_and | | | | | | logical_or | | | | | | logical_not | | | | | |  | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Transparent operator wrappers | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | plus<>(C++14) | | | | | | minus<>(C++14) | | | | | | negate<>(C++14) | | | | | | multiplies<>(C++14) | | | | | | divides<>(C++14) | | | | | | modulus<>(C++14) | | | | | | bit_and<>(C++14) | | | | | | bit_or<>(C++14) | | | | | | bit_not<>(C++14) | | | | | | bit_xor<>(C++14) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | equal_to<>(C++14) | | | | | | not_equal_to<>(C++14) | | | | | | greater<>(C++14) | | | | | | less<>(C++14) | | | | | | greater_equal<>(C++14) | | | | | | less_equal<>(C++14) | | | | | | logical_and<>(C++14) | | | | | | logical_or<>(C++14) | | | | | | logical_not<>(C++14) | | | | | |  | | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Negators | | | | | | not_fn(C++17) | | | | | | Searchers | | | | | | default_searcher(C++17) | | | | | | boyer_moore_searcher(C++17) | | | | | | boyer_moore_horspool_searcher(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Constrained comparators | | | | | | ranges::equal_to(C++20) | | | | | | ranges::not_equal_to(C++20) | | | | | | ranges::greater(C++20) | | | | | | ranges::less(C++20) | | | | | | ranges::greater_equal(C++20) | | | | | | ranges::less_equal(C++20) | | | | | | compare_three_way(C++20) | | | | | |
| Old binders and adaptors | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | unary_function(until C++17\*) | | | | | | binary_function(until C++17\*) | | | | | | ptr_fun(until C++17\*) | | | | | | pointer_to_unary_function(until C++17\*) | | | | | | pointer_to_binary_function(until C++17\*) | | | | | | mem_fun(until C++17\*) | | | | | | mem_fun_tmem_fun1_tconst_mem_fun_tconst_mem_fun1_t(until C++17\*)(until C++17\*)(until C++17\*)(until C++17\*) | | | | | | not1(until C++20\*) | | | | | | not2(until C++20\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | binder1stbinder2nd(until C++17\*)(until C++17\*) | | | | | | bind1stbind2nd(until C++17\*)(until C++17\*) | | | | | |  | | | | | | mem_fun_ref(until C++17\*) | | | | | | mem_fun_ref_tmem_fun1_ref_tconst_mem_fun_ref_tconst_mem_fun1_ref_t(until C++17\*)(until C++17\*)(until C++17\*)(until C++17\*) | | | | | | unary_negate(until C++20\*) | | | | | | binary_negate(until C++20\*) | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<functional>` |  |  |
| `std::bind_front` |  |  |
| template< class F, class... Args >  constexpr /\* unspecified \*/ bind_front( F&& f, Args&&... args ); | (1) | (since C++20) |
| template< auto ConstFn, class... Args >  constexpr /\* unspecified \*/ bind_front( Args&&... args ); | (2) | (since C++26) |
| `std::bind_back` |  |  |
| template< class F, class... Args >  constexpr /\* unspecified \*/ bind_back( F&& f, Args&&... args ); | (3) | (since C++23) |
| template< auto ConstFn, class... Args >  constexpr /\* unspecified \*/ bind_back( Args&&... args ); | (4) | (since C++26) |
|  |  |  |

Function templates `std::bind_front` and `std::bind_back` generate a perfect forwarding call wrapper which allows to invoke the callable target with its (1,2) first or (3,4) last sizeof...(Args) parameters bound to args.

1,3) The call wrapper holds a copy of the target callable object f.2,4) The call wrapper does not hold a callable target (it is statically determined).1) std::bind_front(f, bound_args...)(call_args...) is expression-equivalent to std::invoke(f, bound_args..., call_args...).2) std::bind_front<ConstFn>(bound_args...)(call_args...) is expression-equivalent to std::invoke(ConstFn, bound_args..., call_args...).3) std::bind_back(f, bound_args...)(call_args...) is expression-equivalent to std::invoke(f, call_args..., bound_args...).4) std::bind_back<ConstFn>(bound_args...)(call_args...) is expression-equivalent to std::invoke(ConstFn, call_args..., bound_args...).

The following conditions must be true, otherwise the program is ill-formed:

- (1,3) std::is_constructible_v<std::decay_t<F>, F>,
- (1,3) std::is_move_constructible_v<std::decay_t<F>>,
- (2,4) If decltype(ConstFn) is a pointer or a pointer-to-member then `ConstFn` is not a null pointer,
- (std::is_constructible_v<std::decay_t<Args>, Args> && ...),
- (std::is_move_constructible_v<std::decay_t<Args>> && ...).

### Parameters

|  |  |  |
| --- | --- | --- |
| f | - | Callable object (function object, pointer to function, reference to function, pointer to member function, or pointer to data member) that will be bound to some arguments |
| args | - | list of the arguments to bind to the (1,2) first or (3,4) last sizeof...(Args) parameters of the callable target |
| Type requirements | | |
| -`std::decay_t<F>` must meet the requirements of MoveConstructible. | | |
| -`std::decay_t<Args>...` must meet the requirements of MoveConstructible. | | |
| -`decltype(ConstFn)` must meet the requirements of Callable. | | |

### Return value

A function object (the call wrapper) of type `T` that is unspecified, except that the types of objects returned by two calls to `std::bind_front` or `std::bind_back` with the same arguments are the same.

Let `bind-partial` be either `std::bind_front` or `std::bind_back`.

The returned object has the following properties:

## **bind-partial return type**

#### Member objects

The returned object behaves as if it holds:

1,3) A member object `fd` of type std::decay_t<F> direct-non-list-initialized from std::forward<F>(f), and1-4) An std::tuple object `tup` constructed with std::tuple<std::decay_t<Args>...>(std::forward<Args>(args)...), except that the returned object's assignment behavior is unspecified and the names are for exposition only.

#### Constructors

The return type of `bind-partial` behaves as if its copy/move constructors perform a memberwise copy/move. It is CopyConstructible if all of its member objects (specified above) are CopyConstructible, and is MoveConstructible otherwise.

#### Member function `operator()`

Given an object `G` obtained from an earlier call to (1,3) `bind-partial(f, args...)` or (2,4) `bind-partial<ConstFn>(args...)`, when a glvalue `g` designating `G` is invoked in a function call expression g(call_args...), an invocation of the stored object takes place, as if by:

1) std::invoke(g.fd, std::get<Ns>(g.tup)..., call_args...), when `bind-partial` is `std::bind_front`,2) std::invoke(ConstFn, std::get<Ns>(g.tup)..., call_args...), when `bind-partial` is `std::bind_front`,3) std::invoke(g.fd, call_args..., std::get<Ns>(g.tup)...), when `bind-partial` is `std::bind_back`,4) std::invoke(ConstFn, call_args..., std::get<Ns>(g.tup)...), when `bind-partial` is `std::bind_back`,

where

:   - `Ns` is an integer pack `0, 1, ..., (sizeof...(Args) - 1)`,
    - `g` is an lvalue in the std::invoke expression if it is an lvalue in the call expression, and is an rvalue otherwise. Thus std::move(g)(call_args...) can move the bound arguments into the call, where g(call_args...) would copy.

The program is ill-formed if `g` has volatile-qualified type.

The member operator() is noexcept if the std::invoke expression it calls is noexcept (in other words, it preserves the exception specification of the underlying call operator).

### Exceptions

1,3) Throw any exception thrown by calling the constructor of the stored function object.1-4) Throw any exception thrown by calling the constructor of any of the bound arguments.

### Notes

These function templates are intended to replace std::bind. Unlike `std::bind`, they do not support arbitrary argument rearrangement and have no special treatment for nested bind-expressions or std::reference_wrappers. On the other hand, they pay attention to the value category of the call wrapper object and propagate exception specification of the underlying call operator.

As described in std::invoke, when invoking a pointer to non-static member function or pointer to non-static data member, the first argument has to be a reference or pointer (including, possibly, smart pointer such as std::shared_ptr and std::unique_ptr) to an object whose member will be accessed.

The arguments to `std::bind_front` or `std::bind_back` are copied or moved, and are never passed by reference unless wrapped in std::ref or std::cref.

Typically, binding arguments to a function or a member function using (1) `std::bind_front` and (3) `std::bind_back` requires storing a function pointer along with the arguments, even though the language knows precisely which function to call without a need to dereference the pointer. To guarantee "zero cost" in those cases, C++26 introduces the versions (2,4) (that accept the callable object as an argument for non-type template parameter).

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_bind_front` | `201907L` | (C++20) | `std::bind_front`, (1) |
| `202306L` | (C++26) | Allow passing callable objects as non-type template arguments to `std::bind_front`, (2) |
| `__cpp_lib_bind_back` | `202202L` | (C++23) | `std::bind_back`, (3) |
| `202306L` | (C++26) | Allow passing callable objects as non-type template arguments to `std::bind_back`, (4) |

### Possible implementation

| (2) bind_front |
| --- |
| ```text namespace detail {     template<class T, class U>     struct copy_const         : std::conditional<std::is_const_v<T>, U const, U> {};       template<class T, class U,              class X = typename copy_const<std::remove_reference_t<T>, U>::type>     struct copy_value_category         : std::conditional<std::is_lvalue_reference_v<T&&>, X&, X&&> {};       template <class T, class U>     struct type_forward_like         : copy_value_category<T, std::remove_reference_t<U>> {};       template <class T, class U>     using type_forward_like_t = typename type_forward_like<T, U>::type; }   template<auto ConstFn, class... Args> constexpr auto bind_front(Args&&... args) {     using F = decltype(ConstFn);       if constexpr (std::is_pointer_v<F> or std::is_member_pointer_v<F>)         static_assert(ConstFn != nullptr);       return         [... bound_args(std::forward<Args>(args))]<class Self, class... T>         (             this Self&&, T&&... call_args         )         noexcept         (             std::is_nothrow_invocable_v<F,                 detail::type_forward_like_t<Self, std::decay_t<Args>>..., T...>         )         -> std::invoke_result_t<F,                 detail::type_forward_like_t<Self, std::decay_t<Args>>..., T...>         {             return std::invoke(ConstFn, std::forward_like<Self>(bound_args)...,                                std::forward<T>(call_args)...);         }; } ``` |
| (4) bind_back |
| ```text namespace detail { /* is the same as above */ }   template<auto ConstFn, class... Args> constexpr auto bind_back(Args&&... args) {     using F = decltype(ConstFn);       if constexpr (std::is_pointer_v<F> or std::is_member_pointer_v<F>)         static_assert(ConstFn != nullptr);       return         [... bound_args(std::forward<Args>(args))]<class Self, class... T>         (             this Self&&, T&&... call_args         )         noexcept         (             std::is_nothrow_invocable_v<F,                 detail::type_forward_like_t<Self, T..., std::decay_t<Args>>...>         )         -> std::invoke_result_t<F,                 detail::type_forward_like_t<Self, T..., std::decay_t<Args>>...>         {             return std::invoke(ConstFn, std::forward<T>(call_args)...,                                std::forward_like<Self>(bound_args)...);         }; } ``` |

### Example

Run this code

```
#include <cassert>
#include <functional>
 
int minus(int a, int b)
{
    return a - b;
}
 
struct S
{
    int val;
    int minus(int arg) const noexcept { return val - arg; }
};
 
int main()
{
    auto fifty_minus = std::bind_front(minus, 50);
    assert(fifty_minus(3) == 47); // equivalent to: minus(50, 3) == 47
 
    auto member_minus = std::bind_front(&S::minus, S{50});
    assert(member_minus(3) == 47); //: S tmp{50}; tmp.minus(3) == 47
 
    // Noexcept-specification is preserved:
    static_assert(!noexcept(fifty_minus(3)));
    static_assert(noexcept(member_minus(3)));
 
    // Binding of a lambda:
    auto plus = [](int a, int b) { return a + b; };
    auto forty_plus = std::bind_front(plus, 40);
    assert(forty_plus(7) == 47); // equivalent to: plus(40, 7) == 47
 
#if __cpp_lib_bind_front >= 202306L
    auto fifty_minus_cpp26 = std::bind_front<minus>(50);
    assert(fifty_minus_cpp26(3) == 47);
 
    auto member_minus_cpp26 = std::bind_front<&S::minus>(S{50});
    assert(member_minus_cpp26(3) == 47);
 
    auto forty_plus_cpp26 = std::bind_front<plus>(40);
    assert(forty_plus(7) == 47);
#endif
 
#if __cpp_lib_bind_back >= 202202L
    auto madd = [](int a, int b, int c) { return a * b + c; };
    auto mul_plus_seven = std::bind_back(madd, 7);
    assert(mul_plus_seven(4, 10) == 47); //: madd(4, 10, 7) == 47
#endif
 
#if __cpp_lib_bind_back >= 202306L
    auto mul_plus_seven_cpp26 = std::bind_back<madd>(7);
    assert(mul_plus_seven_cpp26(4, 10) == 47);
#endif
}

```

### References

- C++26 standard (ISO/IEC 14882:2026):

:   - TBD Function templates bind_front and bind_back [func.bind.partial]

- C++23 standard (ISO/IEC 14882:2024):

:   - 22.10.14 Function templates bind_front and bind_back [func.bind.partial]

- C++20 standard (ISO/IEC 14882:2020):

:   - 20.14.14 Function template bind_front [func.bind.front]

### See also

|  |  |
| --- | --- |
| bind(C++11) | binds one or more arguments to a function object   (function template) |
| mem_fn(C++11) | creates a function object out of a pointer to a member   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/utility/functional/bind_front&oldid=175561>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 August 2024, at 02:32.