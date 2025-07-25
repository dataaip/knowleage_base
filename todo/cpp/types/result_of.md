# std::result_of, std::invoke_result

From cppreference.com
< cpp‎ | types
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

Metaprogramming library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Type traits | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Type categories | | | | | | is_void(C++11) | | | | | | is_null_pointer(C++11)(DR\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_array(C++11) | | | | | | is_pointer(C++11) | | | | | | is_enum(C++11) | | | | | | is_union(C++11) | | | | | | is_class(C++11) | | | | | | is_function(C++11) | | | | | | is_reference(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_object(C++11) | | | | | | is_scalar(C++11) | | | | | | is_compound(C++11) | | | | | | is_integral(C++11) | | | | | | is_floating_point(C++11) | | | | | | is_fundamental(C++11) | | | | | | is_arithmetic(C++11) | | | | | | | is_lvalue_reference(C++11) | | | | | | is_rvalue_reference(C++11) | | | | | | is_member_pointer(C++11) | | | | | | is_member_object_pointer(C++11) | | | | | | is_member_function_pointer(C++11) | | | | | | Type properties | | | | | | is_const(C++11) | | | | | | is_volatile(C++11) | | | | | | is_empty(C++11) | | | | | | is_polymorphic(C++11) | | | | | | is_final(C++14) | | | | | | is_abstract(C++11) | | | | | | is_aggregate(C++17) | | | | | | is_implicit_lifetime(C++23) | | | | | | is_trivial(C++11)(deprecated in C++26) | | | | | | is_trivially_copyable(C++11) | | | | | | is_standard_layout(C++11) | | | | | | is_literal_type(C++11)(until C++20\*) | | | | | | is_pod(C++11)(deprecated in C++20) | | | | | | is_signed(C++11) | | | | | | is_unsigned(C++11) | | | | | | is_bounded_array(C++20) | | | | | | is_unbounded_array(C++20) | | | | | | is_scoped_enum(C++23) | | | | | | has_unique_object_representations(C++17) | | | | | | Type trait constants | | | | | | integral_constantbool_constanttrue_typefalse_type(C++11)(C++17)(C++11)(C++11) | | | | | | Metafunctions | | | | | | conjunction(C++17) | | | | | | disjunction(C++17) | | | | | | negation(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Supported operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_constructibleis_trivially_constructibleis_nothrow_constructible(C++11)(C++11)(C++11) | | | | | | is_default_constructibleis_trivially_default_constructibleis_nothrow_default_constructible(C++11)(C++11)(C++11) | | | | | | is_copy_constructibleis_trivially_copy_constructibleis_nothrow_copy_constructible(C++11)(C++11)(C++11) | | | | | | is_move_constructibleis_trivially_move_constructibleis_nothrow_move_constructible(C++11)(C++11)(C++11) | | | | | | is_assignableis_trivially_assignableis_nothrow_assignable(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_copy_assignableis_trivially_copy_assignableis_nothrow_copy_assignable(C++11)(C++11)(C++11) | | | | | | is_move_assignableis_trivially_move_assignableis_nothrow_move_assignable(C++11)(C++11)(C++11) | | | | | | is_destructibleis_trivially_destructibleis_nothrow_destructible(C++11)(C++11)(C++11) | | | | | | has_virtual_destructor(C++11) | | | | | | is_swappable_withis_swappableis_nothrow_swappable_withis_nothrow_swappable(C++17)(C++17)(C++17)(C++17) | | | | | |  | | | | | | | Relationships and property queries | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_same(C++11) | | | | | | is_convertibleis_nothrow_convertible(C++11)(C++20) | | | | | | is_layout_compatible(C++20) | | | | | | is_pointer_interconvertible_base_of(C++20) | | | | | | is_pointer_interconvertible_with_class(C++20) | | | | | | is_corresponding_member(C++20) | | | | | | reference_constructs_from_temporary(C++23) | | | | | | reference_converts_from_temporary(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_base_of(C++11) | | | | | | is_virtual_base_of(C++26) | | | | | | alignment_of(C++11) | | | | | | rank(C++11) | | | | | | extent(C++11) | | | | | | is_invocableis_invocable_ris_nothrow_invocableis_nothrow_invocable_r(C++17)(C++17)(C++17)(C++17) | | | | | | | Type modifications | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_cvremove_constremove_volatile(C++11)(C++11)(C++11) | | | | | | add_cvadd_constadd_volatile(C++11)(C++11)(C++11) | | | | | | make_signed(C++11) | | | | | | make_unsigned(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_reference(C++11) | | | | | | add_lvalue_referenceadd_rvalue_reference(C++11)(C++11) | | | | | | remove_pointer(C++11) | | | | | | add_pointer(C++11) | | | | | | remove_extent(C++11) | | | | | | remove_all_extents(C++11) | | | | | |  | | | | | | | Type transformations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | aligned_storage(C++11)(deprecated in C++23) | | | | | | aligned_union(C++11)(deprecated in C++23) | | | | | | decay(C++11) | | | | | | remove_cvref(C++20) | | | | | | ****result_ofinvoke_result****(C++11)(until C++20\*)(C++17) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | conditional(C++11) | | | | | | common_type(C++11) | | | | | | common_reference(C++20) | | | | | | underlying_type(C++11) | | | | | | type_identity(C++20) | | | | | | enable_if(C++11) | | | | | | void_t(C++17) | | | | | | |
| Compile-time rational arithmetic | | | | |
| Compile-time integer sequences | | | | |
| integer_sequence(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<type_traits>` |  |  |
| template< class >  class result_of; // not defined    template< class F, class... ArgTypes > class result_of<F(ArgTypes...)>; | (1) | (since C++11)  (deprecated in C++17)  (removed in C++20) |
| template< class F, class... ArgTypes >  class invoke_result; | (2) | (since C++17) |
|  |  |  |

Deduces the return type of an `INVOKE` expression at compile time.

|  |  |
| --- | --- |
| `F` must be a callable type, reference to function, or reference to callable type. Invoking `F` with `ArgTypes...` must be a well-formed expression. | (since C++11) (until C++14) |
| `F` and all types in `ArgTypes` can be any complete type, array of unknown bound, or (possibly cv-qualified) `void`. | (since C++14) |

If the program adds specializations for any of the templates described on this page, the behavior is undefined.

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| `type` | the return type of the Callable type `F` if invoked with the arguments `ArgTypes...`. Only defined if F can be called with the arguments `ArgTypes...` in unevaluated context.(since C++14) |

### Helper types

|  |  |  |
| --- | --- | --- |
| template< class T >  using result_of_t = typename result_of<T>::type; | (1) | (since C++14)  (deprecated in C++17)  (removed in C++20) |
| template< class F, class... ArgTypes >  using invoke_result_t = typename invoke_result<F, ArgTypes...>::type; | (2) | (since C++17) |
|  |  |  |

### Possible implementation

```
namespace detail
{
    template<class T>
    struct is_reference_wrapper : std::false_type {};
    template<class U>
    struct is_reference_wrapper<std::reference_wrapper<U>> : std::true_type {};
 
    template<class T>
    struct invoke_impl
    {
        template<class F, class... Args>
        static auto call(F&& f, Args&&... args)
            -> decltype(std::forward<F>(f)(std::forward<Args>(args)...));
    };
 
    template<class B, class MT>
    struct invoke_impl<MT B::*>
    {
        template<class T, class Td = typename std::decay<T>::type,
            class = typename std::enable_if<std::is_base_of<B, Td>::value>::type>
        static auto get(T&& t) -> T&&;
 
        template<class T, class Td = typename std::decay<T>::type,
            class = typename std::enable_if<is_reference_wrapper<Td>::value>::type>
        static auto get(T&& t) -> decltype(t.get());
 
        template<class T, class Td = typename std::decay<T>::type,
            class = typename std::enable_if<!std::is_base_of<B, Td>::value>::type,
            class = typename std::enable_if<!is_reference_wrapper<Td>::value>::type>
        static auto get(T&& t) -> decltype(*std::forward<T>(t));
 
        template<class T, class... Args, class MT1,
            class = typename std::enable_if<std::is_function<MT1>::value>::type>
        static auto call(MT1 B::*pmf, T&& t, Args&&... args)
            -> decltype((invoke_impl::get(
                std::forward<T>(t)).*pmf)(std::forward<Args>(args)...));
 
        template<class T>
        static auto call(MT B::*pmd, T&& t)
            -> decltype(invoke_impl::get(std::forward<T>(t)).*pmd);
    };
 
    template<class F, class... Args, class Fd = typename std::decay<F>::type>
    auto INVOKE(F&& f, Args&&... args)
        -> decltype(invoke_impl<Fd>::call(std::forward<F>(f),
            std::forward<Args>(args)...));
} // namespace detail
 
// Minimal C++11 implementation:
template<class> struct result_of;
template<class F, class... ArgTypes>
struct result_of<F(ArgTypes...)>
{
    using type = decltype(detail::INVOKE(std::declval<F>(), std::declval<ArgTypes>()...));
};
 
// Conforming C++14 implementation (is also a valid C++11 implementation):
namespace detail
{
    template<typename AlwaysVoid, typename, typename...>
    struct invoke_result {};
    template<typename F, typename...Args>
    struct invoke_result<
        decltype(void(detail::INVOKE(std::declval<F>(), std::declval<Args>()...))),
            F, Args...>
    {
        using type = decltype(detail::INVOKE(std::declval<F>(), std::declval<Args>()...));
    };
} // namespace detail
 
template<class> struct result_of;
template<class F, class... ArgTypes>
struct result_of<F(ArgTypes...)> : detail::invoke_result<void, F, ArgTypes...> {};
 
template<class F, class... ArgTypes>
struct invoke_result : detail::invoke_result<void, F, ArgTypes...> {};

```

### Notes

As formulated in C++11, the behavior of `std::result_of` is undefined when `INVOKE(std::declval<F>(), std::declval<ArgTypes>()...)` is ill-formed (e.g. when F is not a callable type at all). C++14 changes that to a SFINAE (when F is not callable, `std::result_of<F(ArgTypes...)>` simply doesn't have the `type` member).

The motivation behind `std::result_of` is to determine the result of invoking a Callable, in particular if that result type is different for different sets of arguments.

F(Args...) is a function type with `Args...` being the argument types and `F` being the return type. As such, `std::result_of` suffers from several quirks that led to its deprecation in favor of `std::invoke_result` in C++17:

- `F` cannot be a function type or an array type (but can be a reference to them);
- if any of the `Args` has type "array of `T`" or a function type `T`, it is automatically adjusted to `T*`;
- neither `F` nor any of `Args...` can be an abstract class type;
- if any of `Args...` has a top-level cv-qualifier, it is discarded;
- none of `Args...` may be of type void.

To avoid these quirks, `result_of` is often used with reference types as `F` and `Args...`. For example:

```
template<class F, class... Args>
std::result_of_t<F&&(Args&&...)> // instead of std::result_of_t<F(Args...)>, which is wrong
    my_invoke(F&& f, Args&&... args)
    {
        /* implementation */
    }

```

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_result_of_sfinae` | `201210L` | (C++14) | `std::result_of` and SFINAE |
| `__cpp_lib_is_invocable` | `201703L` | (C++17) | std::is_invocable, `std::invoke_result` |

### Examples

Run this code

```
#include <iostream>
#include <type_traits>
 
struct S
{
    double operator()(char, int&);
    float operator()(int) { return 1.0; }
};
 
template<class T>
typename std::result_of<T(int)>::type f(T& t)
{
    std::cout << "overload of f for callable T\n";
    return t(0);
}
 
template<class T, class U>
int f(U u)
{
    std::cout << "overload of f for non-callable T\n";
    return u;
}
 
int main()
{
    // the result of invoking S with char and int& arguments is double
    std::result_of<S(char, int&)>::type d = 3.14; // d has type double
    static_assert(std::is_same<decltype(d), double>::value, "");
 
    // std::invoke_result uses different syntax (no parentheses)
    std::invoke_result<S,char,int&>::type b = 3.14;
    static_assert(std::is_same<decltype(b), double>::value, "");
 
    // the result of invoking S with int argument is float
    std::result_of<S(int)>::type x = 3.14; // x has type float
    static_assert(std::is_same<decltype(x), float>::value, "");
 
    // result_of can be used with a pointer to member function as follows
    struct C { double Func(char, int&); };
    std::result_of<decltype(&C::Func)(C, char, int&)>::type g = 3.14;
    static_assert(std::is_same<decltype(g), double>::value, "");
 
    f<C>(1); // may fail to compile in C++11; calls the non-callable overload in C++14
}

```

Output:

```
overload of f for non-callable T

```

### See also

|  |  |
| --- | --- |
| invokeinvoke_r(C++17)(C++23) | invokes any Callable object with given arguments and possibility to specify return type(since C++23)   (function template) |
| is_invocableis_invocable_ris_nothrow_invocableis_nothrow_invocable_r(C++17) | checks if a type can be invoked (as if by std::invoke) with the given argument types   (class template) |
| declval(C++11) | obtains a reference to an object of the template type argument for use in an unevaluated context   (function template) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/types/result_of&oldid=157519>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 29 August 2023, at 09:57.