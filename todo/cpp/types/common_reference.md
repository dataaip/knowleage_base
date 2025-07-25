# std::common_reference

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Type categories | | | | | | is_void(C++11) | | | | | | is_null_pointer(C++11)(DR\*) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_array(C++11) | | | | | | is_pointer(C++11) | | | | | | is_enum(C++11) | | | | | | is_union(C++11) | | | | | | is_class(C++11) | | | | | | is_function(C++11) | | | | | | is_reference(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_object(C++11) | | | | | | is_scalar(C++11) | | | | | | is_compound(C++11) | | | | | | is_integral(C++11) | | | | | | is_floating_point(C++11) | | | | | | is_fundamental(C++11) | | | | | | is_arithmetic(C++11) | | | | | | | is_lvalue_reference(C++11) | | | | | | is_rvalue_reference(C++11) | | | | | | is_member_pointer(C++11) | | | | | | is_member_object_pointer(C++11) | | | | | | is_member_function_pointer(C++11) | | | | | | Type properties | | | | | | is_const(C++11) | | | | | | is_volatile(C++11) | | | | | | is_empty(C++11) | | | | | | is_polymorphic(C++11) | | | | | | is_final(C++14) | | | | | | is_abstract(C++11) | | | | | | is_aggregate(C++17) | | | | | | is_implicit_lifetime(C++23) | | | | | | is_trivial(C++11)(deprecated in C++26) | | | | | | is_trivially_copyable(C++11) | | | | | | is_standard_layout(C++11) | | | | | | is_literal_type(C++11)(until C++20\*) | | | | | | is_pod(C++11)(deprecated in C++20) | | | | | | is_signed(C++11) | | | | | | is_unsigned(C++11) | | | | | | is_bounded_array(C++20) | | | | | | is_unbounded_array(C++20) | | | | | | is_scoped_enum(C++23) | | | | | | has_unique_object_representations(C++17) | | | | | | Type trait constants | | | | | | integral_constantbool_constanttrue_typefalse_type(C++11)(C++17)(C++11)(C++11) | | | | | | Metafunctions | | | | | | conjunction(C++17) | | | | | | disjunction(C++17) | | | | | | negation(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Supported operations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_constructibleis_trivially_constructibleis_nothrow_constructible(C++11)(C++11)(C++11) | | | | | | is_default_constructibleis_trivially_default_constructibleis_nothrow_default_constructible(C++11)(C++11)(C++11) | | | | | | is_copy_constructibleis_trivially_copy_constructibleis_nothrow_copy_constructible(C++11)(C++11)(C++11) | | | | | | is_move_constructibleis_trivially_move_constructibleis_nothrow_move_constructible(C++11)(C++11)(C++11) | | | | | | is_assignableis_trivially_assignableis_nothrow_assignable(C++11)(C++11)(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_copy_assignableis_trivially_copy_assignableis_nothrow_copy_assignable(C++11)(C++11)(C++11) | | | | | | is_move_assignableis_trivially_move_assignableis_nothrow_move_assignable(C++11)(C++11)(C++11) | | | | | | is_destructibleis_trivially_destructibleis_nothrow_destructible(C++11)(C++11)(C++11) | | | | | | has_virtual_destructor(C++11) | | | | | | is_swappable_withis_swappableis_nothrow_swappable_withis_nothrow_swappable(C++17)(C++17)(C++17)(C++17) | | | | | |  | | | | | | | Relationships and property queries | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_same(C++11) | | | | | | is_convertibleis_nothrow_convertible(C++11)(C++20) | | | | | | is_layout_compatible(C++20) | | | | | | is_pointer_interconvertible_base_of(C++20) | | | | | | is_pointer_interconvertible_with_class(C++20) | | | | | | is_corresponding_member(C++20) | | | | | | reference_constructs_from_temporary(C++23) | | | | | | reference_converts_from_temporary(C++23) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | is_base_of(C++11) | | | | | | is_virtual_base_of(C++26) | | | | | | alignment_of(C++11) | | | | | | rank(C++11) | | | | | | extent(C++11) | | | | | | is_invocableis_invocable_ris_nothrow_invocableis_nothrow_invocable_r(C++17)(C++17)(C++17)(C++17) | | | | | | | Type modifications | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_cvremove_constremove_volatile(C++11)(C++11)(C++11) | | | | | | add_cvadd_constadd_volatile(C++11)(C++11)(C++11) | | | | | | make_signed(C++11) | | | | | | make_unsigned(C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove_reference(C++11) | | | | | | add_lvalue_referenceadd_rvalue_reference(C++11)(C++11) | | | | | | remove_pointer(C++11) | | | | | | add_pointer(C++11) | | | | | | remove_extent(C++11) | | | | | | remove_all_extents(C++11) | | | | | |  | | | | | | | Type transformations | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | aligned_storage(C++11)(deprecated in C++23) | | | | | | aligned_union(C++11)(deprecated in C++23) | | | | | | decay(C++11) | | | | | | remove_cvref(C++20) | | | | | | result_ofinvoke_result(C++11)(until C++20\*)(C++17) | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | conditional(C++11) | | | | | | common_type(C++11) | | | | | | ****common_reference****(C++20) | | | | | | underlying_type(C++11) | | | | | | type_identity(C++20) | | | | | | enable_if(C++11) | | | | | | void_t(C++17) | | | | | | |
| Compile-time rational arithmetic | | | | |
| Compile-time integer sequences | | | | |
| integer_sequence(C++14) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<type_traits>` |  |  |
| template< class... T >  struct common_reference; |  | (since C++20) |
|  |  |  |

Determines the common reference type of the types `T...`, that is, the type to which all the types in `T...` can be converted or bound. If such a type exists (as determined according to the rules below), the member `type` names that type. Otherwise, there is no member `type`. The behavior is undefined if any of the types in `T...` is an incomplete type other than (possibly cv-qualified) void.

When given reference types, `common_reference` attempts to find a reference type to which the supplied reference types can all be bound, but may return a non-reference type if it cannot find such a reference type.

- If sizeof...(T) is zero, there is no member `type`.
- If sizeof...(T) is one (i.e., `T...` contains only one type `T0`), the member `type` names the same type as T0.
- If sizeof...(T) is two (i.e., `T...` contains two types `T1` and `T2`):
  - Let type `S` be the **simple common reference type** of `T1` and `T2` (as defined below). The member type `type` names `S` if all of the conditions below are satisfied:
    - `T1` and `T2` are both reference types
    - `S` is well-formed

|  |  |
| --- | --- |
| - std::is_convertible_v<std::add_pointer_t<T1>, std::add_pointer_t<S>> and std::is_convertible_v<std::add_pointer_t<T2>, std::add_pointer_t<S>> are true; | (since C++23) |

:   - Otherwise, if std::basic_common_reference<std::remove_cvref_t<T1>, std::remove_cvref_t<T2>, T1Q, T2Q>::type exists, where `TiQ` is a unary alias template such that TiQ<U> is `U` with the addition of `Ti`'s cv- and reference qualifiers, then the member type `type` names that type;

- - Otherwise, if decltype(false? val<T1>() : val<T2>()), where `val` is a function template template<class T> T val();, is a valid type, then the member type `type` names that type;
  - Otherwise, if std::common_type_t<T1, T2> is a valid type, then the member type `type` names that type;
  - Otherwise, there is no member `type`.
- If sizeof...(T) is greater than two (i.e., `T...` consists of the types `T1, T2, R...`), then if std::common_reference_t<T1, T2> exists, the member `type` denotes std::common_reference_t<std::common_reference_t<T1, T2>, R...> if such a type exists. In all other cases, there is no member `type`.

The **simple common reference type** of two reference types `T1` and `T2` is defined as follows:

- If `T1` is `cv1 X&` and `T2` is `cv2 Y&` (i.e., both are lvalue reference types): their simple common reference type is decltype(false? std::declval<cv12 X&>() : std::declval<cv12 Y&>()), where **cv12** is the union of **cv1** and **cv2**, if that type exists and is a reference type;
- If `T1` and `T2` are both rvalue reference types: if the simple common reference type of `T1&` and `T2&` (determined according to the previous bullet) exists, then let `C` denote that type's corresponding rvalue reference type. If std::is_convertible_v<T1, C> and std::is_convertible_v<T2, C> are both true, then the simple common reference type of `T1` and `T2` is `C`;
- Otherwise, one of the two types must be an lvalue reference type `A&` and the other must be an rvalue reference type `B&&` (`A` and `B` might be cv-qualified). Let `D` denote the simple common reference type of A& and B const&, if any. If D exists and std::is_convertible_v<B&&, D> is true, then the simple common reference type is `D`;
- Otherwise, there's no simple common reference type.

See Conditional operator for the definition of the type of expression false ? X : Y like the ones used above.

### Member types

|  |  |
| --- | --- |
| Name | Definition |
| `type` | the common reference type for all `T...` |

### Helper types

|  |  |  |
| --- | --- | --- |
| template< class... T >  using common_reference_t = std::common_reference<T...>::type; |  |  |
| template< class T, class U, template<class> class TQual, template<class> class UQual >  struct basic_common_reference {}; |  |  |
|  |  |  |

The class template `basic_common_reference` is a customization point that allows users to influence the result of `common_reference` for user-defined types (typically proxy references). The primary template is empty.

### Specializations

A program may specialize std::basic_common_reference<T, U, TQual, UQual> on the first two parameters `T` and `U` if std::is_same_v<T, std::decay_t<T>> and std::is_same_v<U, std::decay_t<U>> are both true and at least one of them depends on a program-defined type.

If such a specialization has a member named `type`, it must be a public and unambiguous member that names a type to which both TQual<T> and UQual<U> are convertible. Additionally, std::basic_common_reference<T, U, TQual, UQual>::type and std::basic_common_reference<U, T, UQual, TQual>::type must denote the same type.

A program may not specialize `basic_common_reference` on the third or fourth parameters, nor may it specialize `common_reference` itself. A program that adds specializations in violation of these rules has undefined behavior.

The standard library provides following specializations of `basic_common_reference`:

|  |  |
| --- | --- |
| std::basic_common_reference<std::pair>(C++23) | determines the common reference type of two `pair`s   (class template specialization) |
| std::basic_common_reference<**tuple-like**>(C++23) | determines the common reference type of a `tuple` and a `tuple-like` type   (class template specialization) |
| std::basic_common_reference<std::reference_wrapper>(C++23) | determines the common reference type of `reference_wrapper` and non-`reference_wrapper`   (class template specialization) |

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_common_reference` | `202302L` | (C++23) | Make std::common_reference_t of std::reference_wrapper a reference type |

### Examples

Run this code

```
#include <concepts>
#include <type_traits>
 
static_assert(
    std::same_as<
        int&,
        std::common_reference_t<
            std::add_lvalue_reference_t<int>,
            std::add_lvalue_reference_t<int>&,
            std::add_lvalue_reference_t<int>&&,
            std::add_lvalue_reference_t<int>const,
            std::add_lvalue_reference_t<int>const&
        >
    >
);
 
int main() {}

```

### See also

|  |  |
| --- | --- |
| common_type(C++11) | determines the common type of a group of types   (class template) |
| common_reference_with(C++20) | specifies that two types share a common reference type   (concept) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/types/common_reference&oldid=170267>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 23 March 2024, at 00:36.