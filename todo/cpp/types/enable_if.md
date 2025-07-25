# std::enable_if

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Type categories | | | | | | is_void(C++11) | | | | | | is_null_pointer(C++11)(DR\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_array(C++11) | | | | | | is_pointer(C++11) | | | | | | is_enum(C++11) | | | | | | is_union(C++11) | | | | | | is_class(C++11) | | | | | | is_function(C++11) | | | | | | is_reference(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_object(C++11) | | | | | | is_scalar(C++11) | | | | | | is_compound(C++11) | | | | | | is_integral(C++11) | | | | | | is_floating_point(C++11) | | | | | | is_fundamental(C++11) | | | | | | is_arithmetic(C++11) | | | | | | | is_lvalue_reference(C++11) | | | | | | is_rvalue_reference(C++11) | | | | | | is_member_pointer(C++11) | | | | | | is_member_object_pointer(C++11) | | | | | | is_member_function_pointer(C++11) | | | | | | Type properties | | | | | | is_const(C++11) | | | | | | is_volatile(C++11) | | | | | | is_empty(C++11) | | | | | | is_polymorphic(C++11) | | | | | | is_final(C++14) | | | | | | is_abstract(C++11) | | | | | | is_aggregate(C++17) | | | | | | is_implicit_lifetime(C++23) | | | | | | is_trivial(C++11)(deprecated in C++26) | | | | | | is_trivially_copyable(C++11) | | | | | | is_standard_layout(C++11) | | | | | | is_literal_type(C++11)(until C++20\*) | | | | | | is_pod(C++11)(deprecated in C++20) | | | | | | is_signed(C++11) | | | | | | is_unsigned(C++11) | | | | | | is_bounded_array(C++20) | | | | | | is_unbounded_array(C++20) | | | | | | is_scoped_enum(C++23) | | | | | | has_unique_object_representations(C++17) | | | | | | Type trait constants | | | | | | integral_constantbool_constanttrue_typefalse_type(C++11)(C++17)(C++11)(C++11) | | | | | | Metafunctions | | | | | | conjunction(C++17) | | | | | | disjunction(C++17) | | | | | | negation(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Supported operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_constructibleis_trivially_constructibleis_nothrow_constructible(C++11)(C++11)(C++11) | | | | | | is_default_constructibleis_trivially_default_constructibleis_nothrow_default_constructible(C++11)(C++11)(C++11) | | | | | | is_copy_constructibleis_trivially_copy_constructibleis_nothrow_copy_constructible(C++11)(C++11)(C++11) | | | | | | is_move_constructibleis_trivially_move_constructibleis_nothrow_move_constructible(C++11)(C++11)(C++11) | | | | | | is_assignableis_trivially_assignableis_nothrow_assignable(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_copy_assignableis_trivially_copy_assignableis_nothrow_copy_assignable(C++11)(C++11)(C++11) | | | | | | is_move_assignableis_trivially_move_assignableis_nothrow_move_assignable(C++11)(C++11)(C++11) | | | | | | is_destructibleis_trivially_destructibleis_nothrow_destructible(C++11)(C++11)(C++11) | | | | | | has_virtual_destructor(C++11) | | | | | | is_swappable_withis_swappableis_nothrow_swappable_withis_nothrow_swappable(C++17)(C++17)(C++17)(C++17) | | | | | |  | | | | | | | Relationships and property queries | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_same(C++11) | | | | | | is_convertibleis_nothrow_convertible(C++11)(C++20) | | | | | | is_layout_compatible(C++20) | | | | | | is_pointer_interconvertible_base_of(C++20) | | | | | | is_pointer_interconvertible_with_class(C++20) | | | | | | is_corresponding_member(C++20) | | | | | | reference_constructs_from_temporary(C++23) | | | | | | reference_converts_from_temporary(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_base_of(C++11) | | | | | | is_virtual_base_of(C++26) | | | | | | alignment_of(C++11) | | | | | | rank(C++11) | | | | | | extent(C++11) | | | | | | is_invocableis_invocable_ris_nothrow_invocableis_nothrow_invocable_r(C++17)(C++17)(C++17)(C++17) | | | | | | | Type modifications | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_cvremove_constremove_volatile(C++11)(C++11)(C++11) | | | | | | add_cvadd_constadd_volatile(C++11)(C++11)(C++11) | | | | | | make_signed(C++11) | | | | | | make_unsigned(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_reference(C++11) | | | | | | add_lvalue_referenceadd_rvalue_reference(C++11)(C++11) | | | | | | remove_pointer(C++11) | | | | | | add_pointer(C++11) | | | | | | remove_extent(C++11) | | | | | | remove_all_extents(C++11) | | | | | |  | | | | | | | Type transformations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | aligned_storage(C++11)(deprecated in C++23) | | | | | | aligned_union(C++11)(deprecated in C++23) | | | | | | decay(C++11) | | | | | | remove_cvref(C++20) | | | | | | result_ofinvoke_result(C++11)(until C++20\*)(C++17) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | conditional(C++11) | | | | | | common_type(C++11) | | | | | | common_reference(C++20) | | | | | | underlying_type(C++11) | | | | | | type_identity(C++20) | | | | | | ****enable_if****(C++11) | | | | | | void_t(C++17) | | | | | | |
| Compile-time rational arithmetic | | | | |
| Compile-time integer sequences | | | | |
| integer_sequence(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<type_traits>` |  |  |
| template< bool B, class T = void >  struct enable_if; |  | (since C++11) |
|  |  |  |

If `B` is true, `std::enable_if` has a public member typedef `type`, equal to `T`; otherwise, there is no member typedef.

This metafunction is a convenient way to leverage SFINAE prior to C++20's concepts, in particular for conditionally removing functions from the candidate set based on type traits, allowing separate function overloads or specializations based on those different type traits.

`std::enable_if` can be used in many forms, including:

- as an additional function argument (not applicable to most operator overloads),
- as a return type (not applicable to constructors and destructors),
- as a class template or function template parameter.

If the program adds specializations for `std::enable_if`, the behavior is undefined.

### Member types

|  |  |
| --- | --- |
| Type | Definition |
| `type` | either `T` or no such member, depending on the value of `B` |

### Helper types

|  |  |  |
| --- | --- | --- |
| template< bool B, class T = void >  using enable_if_t = typename enable_if<B,T>::type; |  | (since C++14) |
|  |  |  |

### Possible implementation

|  |
| --- |
| ```text template<bool B, class T = void> struct enable_if {};   template<class T> struct enable_if<true, T> { typedef T type; }; ``` |

### Notes

A common mistake is to declare two function templates that differ only in their default template arguments. This does not work because the declarations are treated as redeclarations of the same function template (default template arguments are not accounted for in function template equivalence).

```
/* WRONG */
 
struct T
{
    enum { int_t, float_t } type;
 
    template<typename Integer,
             typename = std::enable_if_t<std::is_integral<Integer>::value>>
    T(Integer) : type(int_t) {}
 
    template<typename Floating,
             typename = std::enable_if_t<std::is_floating_point<Floating>::value>>
    T(Floating) : type(float_t) {} // error: treated as redefinition
};
 
/* RIGHT */
 
struct T
{
    enum { int_t, float_t } type;
 
    template<typename Integer,
             std::enable_if_t<std::is_integral<Integer>::value, bool> = true>
    T(Integer) : type(int_t) {}
 
    template<typename Floating,
             std::enable_if_t<std::is_floating_point<Floating>::value, bool> = true>
    T(Floating) : type(float_t) {} // OK
};

```

Care should be taken when using `enable_if` in the type of a template non-type parameter of a namespace-scope function template. Some ABI specifications like the Itanium ABI do not include the instantiation-dependent portions of non-type template parameters in the mangling, meaning that specializations of two distinct function templates might end up with the same mangled name and be erroneously linked together. For example:

```
// first translation unit
 
struct X
{
    enum { value1 = true, value2 = true };
};
 
template<class T, std::enable_if_t<T::value1, int> = 0>
void func() {} // #1
 
template void func<X>(); // #2
 
// second translation unit
 
struct X
{
    enum { value1 = true, value2 = true };
};
 
template<class T, std::enable_if_t<T::value2, int> = 0>
void func() {} // #3
 
template void func<X>(); // #4

```

The function templates #1 and #3 have different signatures and are distinct templates. Nonetheless, #2 and #4, despite being instantiations of different function templates, have the same mangled name in the Itanium C++ ABI (`_Z4funcI1XLi0EEvv`), meaning that the linker will erroneously consider them to be the same entity.

### Example

Run this code

```
#include <iostream>
#include <new>
#include <string>
#include <type_traits>
 
namespace detail
{ 
    void* voidify(const volatile void* ptr) noexcept { return const_cast<void*>(ptr); } 
}
 
// #1, enabled via the return type
template<class T>
typename std::enable_if<std::is_trivially_default_constructible<T>::value>::type 
    construct(T*) 
{
    std::cout << "default constructing trivially default constructible T\n";
}
 
// same as above
template<class T>
typename std::enable_if<!std::is_trivially_default_constructible<T>::value>::type 
    construct(T* p) 
{
    std::cout << "default constructing non-trivially default constructible T\n";
    ::new(detail::voidify(p)) T;
}
 
// #2
template<class T, class... Args>
std::enable_if_t<std::is_constructible<T, Args&&...>::value> // Using helper type
    construct(T* p, Args&&... args) 
{
    std::cout << "constructing T with operation\n";
    ::new(detail::voidify(p)) T(static_cast<Args&&>(args)...);
}
 
// #3, enabled via a parameter
template<class T>
void destroy(
    T*, 
    typename std::enable_if<
        std::is_trivially_destructible<T>::value
    >::type* = 0)
{
    std::cout << "destroying trivially destructible T\n";
}
 
// #4, enabled via a non-type template parameter
template<class T,
         typename std::enable_if<
             !std::is_trivially_destructible<T>{} &&
             (std::is_class<T>{} || std::is_union<T>{}),
             bool>::type = true>
void destroy(T* t)
{
    std::cout << "destroying non-trivially destructible T\n";
    t->~T();
}
 
// #5, enabled via a type template parameter
template<class T,
	 typename = std::enable_if_t<std::is_array<T>::value>>
void destroy(T* t) // note: function signature is unmodified
{
    for (std::size_t i = 0; i < std::extent<T>::value; ++i)
        destroy((*t)[i]);
}
 
/*
template<class T,
	 typename = std::enable_if_t<std::is_void<T>::value>>
void destroy(T* t) {} // error: has the same signature with #5
*/
 
// the partial specialization of A is enabled via a template parameter
template<class T, class Enable = void>
class A {}; // primary template
 
template<class T>
class A<T, typename std::enable_if<std::is_floating_point<T>::value>::type>
{}; // specialization for floating point types
 
int main()
{
    union { int i; char s[sizeof(std::string)]; } u;
 
    construct(reinterpret_cast<int*>(&u));
    destroy(reinterpret_cast<int*>(&u));
 
    construct(reinterpret_cast<std::string*>(&u), "Hello");
    destroy(reinterpret_cast<std::string*>(&u));
 
    A<int>{}; // OK: matches the primary template
    A<double>{}; // OK: matches the partial specialization
}

```

Output:

```
default constructing trivially default constructible T
destroying trivially destructible T
constructing T with operation
destroying non-trivially destructible T

```

### See also

|  |  |
| --- | --- |
| void_t(C++17) | void variadic alias template  (alias template) |

- static_assert
- SFINAE
- Constraints and Concepts
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/types/enable_if&oldid=171705>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 May 2024, at 05:40.