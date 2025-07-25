# Data-parallel types (SIMD) (since C++26)

From cppreference.com
< cpp‎ | numeric
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

Numerics library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Common mathematical functions | | | | |
| Mathematical special functions (C++17) | | | | |
| Mathematical constants (C++20) | | | | |
| Basic linear algebra algorithms (C++26) | | | | |
| ****Data-parallel types (SIMD)**** (C++26) | | | | |
| Floating-point environment (C++11) | | | | |
| Complex numbers | | | | |
| Numeric array (`valarray`) | | | | |
| Pseudo-random number generation | | | | |
| Bit manipulation (C++20) | | | | |
| Factor operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | gcd(C++17) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lcm(C++17) | | | | | |
| Interpolations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | midpoint(C++20) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | lerp(C++20) | | | | | |
| Saturation arithmetic | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | add_sat(C++26) | | | | | | sub_sat(C++26) | | | | | | saturate_cast(C++26) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | mul_sat(C++26) | | | | | | div_sat(C++26) | | | | | |  | | | | | |
| Generic numeric operations | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | iota(C++11) | | | | | | ranges::iota(C++23) | | | | | | accumulate | | | | | | inner_product | | | | | | adjacent_difference | | | | | | partial_sum | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | reduce(C++17) | | | | | | transform_reduce(C++17) | | | | | | inclusive_scan(C++17) | | | | | | exclusive_scan(C++17) | | | | | | transform_inclusive_scan(C++17) | | | | | | transform_exclusive_scan(C++17) | | | | | |

****Data-parallel types (SIMD)****

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Main classes | | | | | | basic_simdsimd | | | | | | basic_simd_masksimd_mask") | | | | | | Load and store flags | | | | | | simd_flagssimd_flag_defaultsimd_flag_convertsimd_flag_alignedsimd_flag_overaligned") | | | | | | Load and store | | | | | | simd_unchecked_loadsimd_partial_load") | | | | | | simd_unchecked_storesimd_partial_store") | | | | | | Casts | | | | | | simd_split") | | | | | | simd_cat") | | | | | |  | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Algorithms | | | | | | minmaxminmax") | | | | | | clamp") | | | | | | simd_select") | | | | | | Reductions | | | | | | all_ofany_ofnone_of") | | | | | | reducereduce_minreduce_max") | | | | | | reduce_min_indexreduce_max_index") | | | | | | reduce_count") | | | | | | Traits | | | | | | simd_alignment") | | | | | | rebind_simd") | | | | | | resize_simd") | | | | | |

The library provides data-parallel types and operations on these types: portable types for explicitly stating data-parallelism and structuring data through data-parallel execution resources where available, such as SIMD registers and instructions or execution units that are driven by a common instruction decoder.

All standard integer types, character types, and most floating-point types are **vectorizable types**. Vectorizable floating-point types include float, double, and the selected extended floating-point types std::float16_t, std::float32_t, and std::float64_t if defined.

A **data-parallel type** consists of one or more elements of an underlying vectorizable type, called the **element type**. The number of elements, called the **width**, is constant for each data-parallel type.

The data-parallel type refers to all enabled specializations of the class templates `basic_simd` and `basic_simd_mask`.

A **data-parallel object** of data-parallel type behaves analogously to objects of type `T`. But while `T` stores and manipulates a single value, the data-parallel type with the element type `T` stores and manipulates multiple values.

Every operation on a data-parallel object acts **element-wise** (except for horizontal operations, such as reductions, which are clearly marked as such) applying to each element of the object or to corresponding elements of two objects. Each such application is unsequenced with respect to the others. This simple rule expresses data-parallelism and will be used by the compiler to generate SIMD instructions and/or independent execution streams.

All operations (except non-constexpr math function overloads) on data-parallel objects are constexpr: it is possible to create and use data-parallel objects in the evaluation of a constant expression.

Alias templates `simd` and `simd_mask` are defined to allow users to specify the width to a certain size. The default width is determined by the implementation at compile-time.

|  |  |
| --- | --- |
| Defined in header `<simd>` | |

### Main classes

|  |  |
| --- | --- |
| basic_simd(C++26) | data-parallel vector type   (class template) |
| simd(C++26) | convenience alias template for `basic_simd` that can specify its width (alias template) |
| basic_simd_mask")(C++26) | data-parallel type with the element type bool   (class template) |
| simd_mask")(C++26) | convenience alias template for `basic_simd_mask` that can specify its width (alias template) |

### Load and store flags

|  |  |
| --- | --- |
| simd_flags")(C++26) | load and store flags for data-parallel types   (class template) |
| simd_flag_default")(C++26) | default flag used on load and store operations   (constant) |
| simd_flag_convert")(C++26) | flag enabling conversions that are not value-preserving on load and store operations   (constant) |
| simd_flag_aligned")(C++26) | flag indicating alignment of the load-store address to some specified storage to the value of `simd_alignment`   (constant) |
| simd_flag_overaligned")(C++26) | flag indicating alignment of the load-store address to some specified storage to the specified alignment (variable template) |

### Load and store operations

|  |  |
| --- | --- |
| simd_unchecked_loadsimd_partial_load")(C++26) | loads elements from a contiguous range to `basic_simd`   (function template) |
| simd_unchecked_storesimd_partial_store")(C++26) | stores elements from `basic_simd` to a contiguous range   (function template) |

### Casts

|  |  |
| --- | --- |
| simd_split")(C++26) | splits single data-parallel object to multiple ones   (function template) |
| simd_cat")(C++26) | concatenates multiple data-parallel objects into a single one   (function template) |

### Algorithms

|  |  |
| --- | --- |
| minmaxminmax")(C++26) | element-wise min/max operations for `basic_simd`   (function template) |
| clamp")(C++26) | element-wise clamp operation for `basic_simd`   (function template) |
| simd_select")(C++26) | element-wise selection using conditional operator   (function template) |

### Reductions

|  |  |
| --- | --- |
| reducereduce_minreduce_max")(C++26) | reduces all values in `basic_simd` over a specified binary operation to a single value   (function template) |
| all_ofany_ofnone_of")(C++26) | reductions of `basic_simd_mask` to bool   (function template) |
| reduce_count")(C++26) | reduction of `basic_simd_mask` to number of true values   (function template) |
| reduce_min_indexreduce_max_index")(C++26) | reductions of `basic_simd_mask` to the index of first or last true value   (function template) |

### Traits

|  |  |
| --- | --- |
| simd_alignment")(C++26) | obtains an appropriate alignment for `simd_flag_aligned`   (class template) |
| rebind_simd")(C++26) | changes element type of the data-parallel type   (class template) |
| resize_simd")(C++26) | changes the width of the data-parallel type   (class template) |

### Math functions

All functions in <cmath> are overloaded for `basic_simd`.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: description |

### Implementation details

#### ABI tags

The data-parallel types `basic_simd` and `basic_simd_mask` are associated with **ABI tags**. These tags are types that specify the size and binary representation of data-parallel objects. The design intends the size and binary representation to vary based on target architecture and compiler flags. The ABI tag, together with the element type, determines the width.

The ABI tag remains independent of machine instruction set selection. The chosen machine instruction set limits the usable ABI tag types. The ABI tags enable users to safely pass objects of data-parallel type across translation unit boundaries.

|  |  |
| --- | --- |
|  | This section is incomplete |

#### Exposition-only entities

|  |  |  |
| --- | --- | --- |
| using /\*simd-size-type\*/ = /\* see description \*/; | (1) | (exposition only\*) |
| template< std::size_t Bytes >  using /\*integer-from\*/ = /\* see description \*/; | (2) | (exposition only\*) |
| template< class T, class Abi >  constexpr /\*simd-size-type\*/ /\*simd-size-v\*/ = /\* see description \*/; | (3) | (exposition only\*) |
| template< class T >  constexpr std::size_t /\*mask-element-size\*/ = /\* see description \*/; | (4) | (exposition only\*) |
| template< class T >  concept /\*constexpr-wrapper-like\*/ = /\* see description \*/; | (5) | (exposition only\*) |
| template< class T >  using /\*deduced-simd-t\*/ = /\* see description \*/; | (6) | (exposition only\*) |
| template< class V, class T >  using /\*make-compatible-simd-t\*/ = /\* see description \*/; | (7) | (exposition only\*) |
|  |  |  |

1) /\*simd-size-type\*/ is an alias for for a signed integer type. The implementation is free to choose any signed integer type.2) /\*integer-from\*/<Bytes> is an alias for a signed integer type `T` such that sizeof(T) equals Bytes.3) /\*simd-size-v\*/<T, Abi> denotes the width of the enabled specialization `basic_simd<T, Abi>`, or ​0​ otherwise.4) If `T` denotes std::basic_simd_mask<Bytes, Abi>, /\*mask-element-size\*/<T> equals Bytes.5) The concept /\*constexpr-wrapper-like\*/ is defined as:

```
template< class T >
concept /*constexpr-wrapper-like*/ =
    std::convertible_to<T, decltype(T::value)> &&
    std::equality_comparable_with<T, decltype(T::value)> &&
    std::bool_constant<T() == T::value>::value &&
    std::bool_constant<static_cast<decltype(T::value)>(T()) == T::value>::value;

```

6) Let x be an lvalue of type const T. /\*deduced-simd-t\*/<T> is an alias equivalent to:

- decltype(x + x), if the type of x + x is an enabled specialization of `basic_simd`; otherwise
- void.
7) Let x be an lvalue of type const T. /\*make-compatible-simd-t\*/<V, T> is an alias equivalent to:

- /\*deduced-simd-t\*/<T>, if that type is not void, otherwise
- std::simd<decltype(x + x), V​::​size()>.

|  |  |  |
| --- | --- | --- |
| Math functions requirements |  |  |
| template< class V >  concept /\*simd-floating-point\*/ = /\* see description \*/; | (8) | (exposition only\*) |
| template< class... Ts >  concept /\*math-floating-point\*/ = /\* see description \*/; | (9) | (exposition only\*) |
| template< class... Ts >    requires /\*math-floating-point\*/<Ts...> using /\*math-common-simd-t\*/ = /\* see description \*/; | (10) | (exposition only\*) |
| template< class BinaryOp, class T >  concept /\*reduction-binary-operation\*/ = /\* see description \*/; | (11) | (exposition only\*) |
|  |  |  |

8) The concept /\*simd-floating-point\*/ is defined as:

```
template< class V >
concept /*simd-floating-point*/ =
    std::same_as<V, std::basic_simd<typename V::value_type, typename V::abi_type>> &&
    std::is_default_constructible_v<V> && 
    std::floating_point<typename V::value_type>;

```

9) The concept /\*math-floating-point\*/ is defined as:

```
template< class... Ts >
concept /*math-floating-point*/ =
    (/*simd-floating-point*/</*deduced-simd-t*/<Ts>> || ...);

```

10) Let `T0` denote Ts...[0], `T1` denote Ts...[1], and `TRest` denote a pack such that T0, T1, TRest... is equivalent to Ts.... Then, /\*math-common-simd-t\*/<Ts...> is an alias equivalent to:

- /\*deduced-simd-t\*/<T0>, if sizeof...(Ts) == 1 is true
- otherwise, std::common_type_t</\*deduced-simd-t\*/<T0>, /\*deduced-simd-t\*/<T1>>, if sizeof...(Ts) == 2 is true and /\*math-floating-point\*/<T0> && /\*math-floating-point\*/<T1> is true,
- otherwise, std::common_type_t</\*deduced-simd-t\*/<T0>, T1> if sizeof...(Ts) == 2 is true and /\*math-floating-point\*/<T0> is true,
- otherwise, std::common_type_t<T0, /\*deduced-simd-t\*/<T1>> if sizeof...(Ts) == 2 is true,
- otherwise, std::common_type_t</\*math-common-simd-t\*/<T0, T1>, TRest...>, if /\*math-common-simd-t\*/<T0, T1> is a valid type,
- otherwise, std::common_type_t</\*math-common-simd-t\*/<TRest...>, T0, T1>.
11) The concept /\*reduction-binary-operation\*/ is defined as:

```
template< class BinaryOp, class T >
concept /*reduction-binary-operation*/ =
    requires (const BinaryOp binary_op, const std::simd<T, 1> v) {
        { binary_op(v, v) } -> std::same_as<std::simd<T, 1>>;
    };

```

/\*reduction-binary-operation\*/<BinaryOp, T> is modeled only if:

:   - `BinaryOp` is a binary element-wise operation that is commutative, and
    - An object of type `BinaryOp` is invocable with two arguments of type std::basic_simd<T, Abi> for unspecified ABI tag `Abi` that returns a std::basic_simd<T, Abi>.

|  |  |  |
| --- | --- | --- |
| SIMD ABI tags |  |  |
| template< class T >  using /\*native-abi\*/ = /\* see description \*/; | (12) | (exposition only\*) |
| template< class T, /\*simd-size-type\*/ N >  using /\*deduce-abi-t\*/ = /\* see description \*/; | (13) | (exposition only\*) |
|  |  |  |

12) /\*native-abi\*/<T> is an implementation-defined alias for an ABI tag. This is the primary ABI tag to use for efficient explicit vectorization. As a result, basic_simd<T, /\*native-abi\*/<T>> is an enabled specialization.13) /\*deduce-abi-t\*/<T, N> is an alias that names an ABI tag type such that:

- /\*simd-size-v\*/<T, /\*deduce-abi-t\*/<T, N>> equals N,
- std::basic_simd<T, /\*deduce-abi-t\*/<T, N>> is an enabled specialization, and
- std::basic_simd_mask<sizeof(T), /\*deduce-abi-t\*/</\*integer-from\*/<sizeof(T)>, N>> is an enabled specialization.

It is defined only if `T` is a vectorizable type, and N > 0 && N <= M is true, where M is an implementation-defined maximum that is at least 64 and can differ depending on `T`.

|  |  |  |
| --- | --- | --- |
| Load and store flags |  |  |
| struct /\*convert-flag\*/; | (14) | (exposition only\*) |
| struct /\*aligned-flag\*/; | (15) | (exposition only\*) |
| template< std::size_t N >  struct /\*overaligned-flag\*/; | (16) | (exposition only\*) |
|  |  |  |

14-16) These tag types are used as a template argument of `std::simd_flags`. See load and store flags") for their corresponding uses.

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_lib_simd` | `202411L` | (C++26) | Data-parallel types and operations |

### Example

Run this code

```
#include <iostream>
#include <simd>
#include <string_view>
 
void println(std::string_view name, auto const& a)
{
    std::cout << name << ": ";
    for (std::size_t i{}; i != a.size(); ++i)
        std::cout << a[i] << ' ';
    std::cout << '\n';
}
 
template<class A>
constexpr std::basic_simd<int, A> my_abs(std::basic_simd<int, A> x)
{
    return std::simd_select(x < 0, -x, x);
}
 
int main()
{
    constexpr std::simd<int> a = 1;
    println("a", a);
 
    constexpr std::simd<int> b([](int i) { return i - 2; });
    println("b", b);
 
    constexpr auto c = a + b;
    println("c", c);
 
    constexpr auto d = my_abs(c);
    println("d", d);
 
    constexpr auto e = d * d;
    println("e", e);
 
    constexpr auto inner_product = std::reduce(e);
    std::cout << "inner product: " << inner_product << '\n';
 
    constexpr std::simd<double, 16> x([](int i) { return i; });
    println("x", x);
    // overloaded math functions are defined in <simd>
    println("cos²(x) + sin²(x)", std::pow(std::cos(x), 2) + std::pow(std::sin(x), 2));
}

```

Output:

```
a: 1 1 1 1 
b: -2 -1 0 1 
c: -1 0 1 2 
d: 1 0 1 2 
e: 1 0 1 4 
inner product: 6
x: 0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 
cos²(x) + sin²(x): 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1 1

```

### See also

|  |  |
| --- | --- |
| valarray | numeric arrays, array masks and array slices   (class template) |

### External links

|  |  |
| --- | --- |
| 1. | The implementation of ISO/IEC TS 19570:2018 Section 9 "Data-Parallel Types" — github.com |
| 2. | TS implementation reach for GCC/libstdc++ (`std::experimental::simd` is shipping with GCC-11) — gcc.gnu.org |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/numeric/simd&oldid=178931>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 1 January 2025, at 10:29.