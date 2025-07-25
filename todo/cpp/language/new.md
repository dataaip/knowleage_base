# `new` expression

From cppreference.com
< cpp‎ | language
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

C++ language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General topics | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Preprocessor | | | | | | Comments | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Keywords | | | | | | Escape sequences | | | | | |
| Flow control | | | | |
| Conditional execution statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | switch | | | | | |
| Iteration statements (loops) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | for | | | | | | range-`for` (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | while | | | | | | `do-while` | | | | | |
| Jump statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | continue - break | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | goto - return | | | | | |
| Functions | | | | |
| Function declaration | | | | |
| Lambda function expression | | | | |
| `inline` specifier | | | | |
| Dynamic exception specifications (until C++17\*) | | | | |
| `noexcept` specifier (C++11) | | | | |
| Exceptions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `throw`-expression | | | | | | `try` block | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | `catch` handler | | | | | |
| Namespaces | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace declaration | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace aliases | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Fundamental types | | | | | | Enumeration types | | | | | | Function types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class/struct types | | | | | | Union types | | | | | |  | | | | | |
| Specifiers | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const`/`volatile` | | | | | | decltype (C++11) | | | | | | auto (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | constexpr (C++11) | | | | | | consteval (C++20) | | | | | | constinit (C++20) | | | | | |
| Storage duration specifiers | | | | |
| Initialization | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default-initialization | | | | | | Value-initialization | | | | | | Zero-initialization | | | | | | Copy-initialization | | | | | | Direct-initialization | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Aggregate initialization | | | | | | List-initialization (C++11) | | | | | | Constant initialization | | | | | | Reference initialization | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Expressions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operators | | | | | | Operator precedence | | | | | |
| Alternative representations | | | | |
| Literals | | | | |
| Boolean - Integer - Floating-point | | | | |
| Character - String - nullptr (C++11) | | | | |
| User-defined (C++11) | | | | |
| Utilities | | | | |
| Attributes (C++11) | | | | |
| Types | | | | |
| `typedef` declaration | | | | |
| Type alias declaration (C++11) | | | | |
| Casts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | static_cast | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Explicit conversions | | | | | | dynamic_cast | | | | | | reinterpret_cast | | | | | |
| Memory allocation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****`new` expression**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `delete` expression | | | | | |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | Constructors | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Access specifiers | | | | | | `friend` specifier | | | | | |  | | | | | |
| Class-specific function properties | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Virtual function | | | | | | `override` specifier (C++11) | | | | | | `final` specifier (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | explicit (C++11) | | | | | | static | | | | | |  | | | | | |
| Special member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default constructor | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | Destructor | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | Constant expressions | | | | | | Primary expressions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lambda expressions (C++11) | | | | | | Requires expressions (C++20) | | | | | | Pack indexing expression (C++26) | | | | | | Potentially-evaluated expressions | | | | | |
| Literals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integer literals | | | | | | Floating-point literals | | | | | | Boolean literals | | | | | | Character literals | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Escape sequences | | | | | | String literals | | | | | | Null pointer literal (C++11) | | | | | | User-defined literal (C++11) | | | | | |
| Operators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | ****`new`-expression**** | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

Creates and initializes objects with dynamic storage duration, that is, objects whose lifetime is not necessarily limited by the scope in which they were created.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `::`(optional) `new` `(`type ﻿`)` new-initializer ﻿(optional) | (1) |  |
|  | | | | | | | | | |
| `::`(optional) `new` type new-initializer ﻿(optional) | (2) |  |
|  | | | | | | | | | |
| `::`(optional) `new` `(`placement-args ﻿`)` `(`type ﻿`)` new-initializer ﻿(optional) | (3) |  |
|  | | | | | | | | | |
| `::`(optional) `new` `(`placement-args ﻿`)` type new-initializer ﻿(optional) | (4) |  |
|  | | | | | | | | | |

1,2) Attempts to create an object of type, denoted by the type-id type, which may be array type, and may include a placeholder type specifier(since C++11), or include a class template name whose argument is to be deduced by class template argument deduction(since C++17).3,4) Same as (1,2), but provides additional arguments to the allocation function, see placement new.

### Explanation

|  |  |  |
| --- | --- | --- |
| type | - | the target type-id |
| new-initializer | - | a parentheses-enclosed expression list or a brace-enclosed initializer list(since C++11) |
| placement-args | - | additional placement arguments |

The new expression attempts to allocate storage and then attempts to construct and initialize either a single unnamed object, or an unnamed array of objects in the allocated storage. The new expression returns a prvalue pointer to the constructed object or, if an array of objects was constructed, a pointer to the initial element of the array.

Syntax (1) or (3) is required if type includes parentheses:

```
new int(*[10])();    // error: parsed as (new int) (*[10]) ()
new (int (*[10])()); // okay: allocates an array of 10 pointers to functions

```

In addition, type is parsed greedily: it will be taken include every token that can be a part of a declarator:

```
new int + 1; // okay: parsed as (new int) + 1, increments a pointer returned by new int
new int * 1; // error: parsed as (new int*) (1)

```

The new-initializer is not optional if

- type is an array of unknown bound,

|  |  |
| --- | --- |
| - a placeholder is used in type, that is, auto or decltype(auto)(since C++14), possibly combined with a type constraint(since C++20), | (since C++11) |
| - a class template is used in type whose arguments need to be deduced. | (since C++17) |

```
double* p = new double[]{1, 2, 3}; // creates an array of type double[3]
auto p = new auto('c');            // creates a single object of type char. p is a char*
 
auto q = new std::integral auto(1);         // OK: q is an int*
auto q = new std::floating_point auto(true) // ERROR: type constraint not satisfied
 
auto r = new std::pair(1, true); // OK: r is a std::pair<int, bool>*
auto r = new std::vector;        // ERROR: element type can't be deduced

```

### Dynamic arrays

If type is an array type, all dimensions other than the first must be specified as positive integral constant expression(until C++14)converted constant expression of type std::size_t(since C++14), but (only when using un-parenthesized syntaxes (2) and (4)) the first dimension may be an expression of integral type, enumeration type, or class type with a single non-explicit conversion function to integral or enumeration type(until C++14)any expression convertible to std::size_t(since C++14). This is the only way to directly create an array with size defined at runtime, such arrays are often referred to as **dynamic arrays**:

```
int n = 42;
double a[n][5]; // error
auto p1 = new  double[n][5];  // OK
auto p2 = new  double[5][n];  // error: only the first dimension may be non-constant
auto p3 = new (double[n][5]); // error: syntax (1) cannot be used for dynamic arrays

```

|  |  |
| --- | --- |
| The behavior is undefined if the value in the first dimension (converted to integral or enumeration type if needed) is negative. | (until C++11) |
| In the following cases the value of the expression specifying the first dimension is invalid:   - the expression is of non-class type and its value before conversion to std::size_t is negative; - the expression is of class type and its value after user-defined conversion function and before the second standard conversion is negative; - the value of the expression is larger than some implementation-defined limit; - the value is smaller than the number of array elements provided in the brace-enclosed initializer list (including the terminating '\0' on a string literal).   If the value in the first dimension is invalid for any of these reasons,   - if, after conversion to std::size_t, the first dimension is a core constant expression and it is potentially evaluated, the program is ill-formed, - otherwise, if the allocation function that would have been called is non-throwing (including std::nothrow overloads not declared noexcept), the new expression returns the null pointer of the required result type, - otherwise, the new expression does not call the allocation function, and instead throws an exception of a type that would match a handler of type std::bad_array_new_length. | (since C++11) |

The first dimension of zero is acceptable, and the allocation function is called.

|  |  |
| --- | --- |
| If new-initializer is a braced-enclosed initializer list, and the first dimension is potentially evaluated and not a core constant expression, the semantic constraints of copy-initializing a hypothetical element of the array from an empty initializer list are checked. | (since C++11) |

### Allocation

The new expression allocates storage by calling the appropriate allocation function. If type is a non-array type, the name of the function is operator new. If type is an array type, the name of the function is operator new[].

As described in allocation function, the C++ program may provide global and class-specific replacements for these functions. If the new expression begins with the optional :: operator, as in ::new T or ::new T[n], class-specific replacements will be ignored (the function is looked up in global scope). Otherwise, if `T` is a class type, lookup begins in the class scope of `T`.

When calling the allocation function, the new expression passes the number of bytes requested as the first argument, of type std::size_t, which is exactly sizeof(T) for non-array `T`.

Array allocation may supply unspecified overhead, which may vary from one call to new to the next, unless the allocation function selected is the standard non-allocating form. The pointer returned by the new expression will be offset by that value from the pointer returned by the allocation function. Many implementations use the array overhead to store the number of objects in the array which is used by the [delete[]](delete.html "cpp/language/delete") expression to call the correct number of destructors. In addition, if the new expression is used to allocate an array of char, unsigned char, or std::byte(since C++17), it may request additional memory from the allocation function if necessary to guarantee correct alignment of objects of all types no larger than the requested array size, if one is later placed into the allocated array.

|  |  |
| --- | --- |
| new expressions are allowed to elide or combine allocations made through replaceable allocation functions. In case of elision, the storage may be provided by the compiler without making the call to an allocation function (this also permits optimizing out unused new expression). In case of combining, the allocation made by a new expression E1 may be extended to provide additional storage for another new expression E2 if all of the following is true: 1) The lifetime of the object allocated by E1 strictly contains the lifetime of the object allocated by E2.2) E1 and E2 would invoke the same replaceable global allocation function.3) For a throwing allocation function, exceptions in E1 and E2 would be first caught in the same handler. Note that this optimization is only permitted when new expressions are used, not any other methods to call a replaceable allocation function: delete[] new int[10]; can be optimized out, but operator delete(operator new(10)); cannot. | (since C++14) |
| During an evaluation of a constant expression, a call to an allocation function is always omitted. Only new expressions that would otherwise result in a call to a replaceable global allocation function can be evaluated in constant expressions. | (since C++20) |

#### Placement new

If placement-args are provided, they are passed to the allocation function as additional arguments. Such allocation functions are known as "placement new", after the standard allocation function void\* operator new(std::size_t, void\*), which simply returns its second argument unchanged. This is used to construct objects in allocated storage:

```
// within any block scope...
{
    // Statically allocate the storage with automatic storage duration
    // which is large enough for any object of type “T”.
    alignas(T) unsigned char buf[sizeof(T)];
 
    T* tptr = new(buf) T; // Construct a “T” object, placing it directly into your 
                          // pre-allocated storage at memory address “buf”.
 
    tptr->~T();           // You must **manually** call the object's destructor
                          // if its side effects is depended by the program.
}                         // Leaving this block scope automatically deallocates “buf”.

```

Note: this functionality is encapsulated by the member functions of the Allocator classes.

|  |  |
| --- | --- |
| When allocating an object whose alignment requirement exceeds __STDCPP_DEFAULT_NEW_ALIGNMENT__ or an array of such objects, the new expression passes the alignment requirement (wrapped in std::align_val_t) as the second argument for the allocation function (for placement forms, placement-arg appear after the alignment, as the third, fourth, etc arguments). If overload resolution fails (which happens when a class-specific allocation function is defined with a different signature, since it hides the globals), overload resolution is attempted a second time, without alignment in the argument list. This allows alignment-unaware class-specific allocation functions to take precedence over the global alignment-aware allocation functions. | (since C++17) |

```
new T;      // calls operator new(sizeof(T))
            // (C++17) or operator new(sizeof(T), std::align_val_t(alignof(T))))
new T[5];   // calls operator new[](sizeof(T)*5 + overhead)
            // (C++17) or operator new(sizeof(T)*5+overhead, std::align_val_t(alignof(T))))
new(2,f) T; // calls operator new(sizeof(T), 2, f)
            // (C++17) or operator new(sizeof(T), std::align_val_t(alignof(T)), 2, f)

```

If a non-throwing allocation function (e.g. the one selected by new(std::nothrow) T) returns a null pointer because of an allocation failure, then the new expression returns immediately, it does not attempt to initialize an object or to call a deallocation function. If a null pointer is passed as the argument to a non-allocating placement new expression, which makes the selected standard non-allocating placement allocation function return a null pointer, the behavior is undefined.

### Initialization

The object created by a new expression is initialized according to the following rules.

If type is not an array type, the single object is constructed in the acquired memory area:

- If new-initializer is absent, the object is default-initialized.
- If new-initializer is a parentheses-enclosed expression list, the object is direct-initialized.

|  |  |
| --- | --- |
| - If new-initializer is a braced-enclosed initializer list, the object is list-initialized. | (since C++11) |

If type is an array type, an array of objects is initialized:

- If new-initializer is absent, each element is default-initialized.

:   - Even if the first dimension is zero, the semantic constraints of default-initializing a hypothetical element still need to be met.

- If new-initializer is a pair of parentheses, each element is value-initialized.

:   - Even if the first dimension is zero, the semantic constraints of value-initializing a hypothetical element still need to be met.

|  |  |
| --- | --- |
| - If new-initializer is a braced-enclosed initializer list, the array is aggregate-initialized. | (since C++11) |
| - If new-initializer is a parentheses-enclosed non-empty expression list, the array is aggregate-initialized. | (since C++20) |

#### Initialization failure

If initialization terminates by throwing an exception (e.g. from the constructor), the program looks up a matching deallocation function, then:

- If a suitable deallocation function can be found, the deallocation function is called to free the memory in which the object was being constructed. After that, the exception continues to propagate in the context of the new expression.
- If no unambiguous matching deallocation function can be found, propagating the exception does not cause the object’s memory to be freed. It is only appropriate if the called allocation function does not allocate memory, otherwise it is likely to result in a memory leak.

The scope of the lookup of the matching deallocation function is determined as follows:

- If the new expression does not begin with `::`, and the allocated type is either a class type `T` or an array of class type `T`, a search is performed for the deallocation function’s name in the class scope of `T`.
- Otherwise, or if nothing is found in the `T`'s class scope, the deallocation function’s name is looked up by searching for it in the global scope.

For a non-placement allocation function, the normal deallocation function lookup is used to find the matching deallocation function (see delete-expression).

For a placement allocation function, the matching deallocation function must have the same number of parameter, and each parameter type except the first is identical to the corresponding parameter type of the allocation function (after parameter transformations).

- If the lookup finds a single matching deallocation function, that function will be called; otherwise, no deallocation function will be called.
- If the lookup finds a non-placement deallocation function and that function, considered as a placement deallocation function, would have been selected as a match for the allocation function, the program is ill-formed.

In any case, the matching deallocation function (if any) must be non-deleted and(since C++11) accessible from the point where the new expression appears.

```
struct S
{
    // Placement allocation function:
    static void* operator new(std::size_t, std::size_t);
 
    // Non-placement deallocation function:
    static void operator delete(void*, std::size_t);
};
 
S* p = new (0) S; // error: non-placement deallocation function matches
                  //        placement allocation function

```

If a deallocation function is called in a new expression (due to initialization failure), the arguments passed to that function are determined as follows:

- The first argument is the value (of type void\*) returned from the allocation function call.
- Other arguments (only for placement deallocation functions) are the placement-args passed to the placement allocation function.

If the implementation is allowed to introduce a temporary object or make a copy of any argument as part of the call to the allocation function, it is unspecified whether the same object is used in the call to both the allocation and deallocation functions.

### Memory leaks

The objects created by new expressions (objects with dynamic storage duration) persist until the pointer returned by the new expression is used in a matching delete-expression. If the original value of pointer is lost, the object becomes unreachable and cannot be deallocated: a **memory leak** occurs.

This may happen if the pointer is assigned to:

```
int* p = new int(7); // dynamically allocated int with value 7
p = nullptr; // memory leak

```

or if the pointer goes out of scope:

```
void f()
{
    int* p = new int(7);
} // memory leak

```

or due to exception:

```
void f()
{
    int* p = new int(7);
    g();      // may throw
    delete p; // okay if no exception
} // memory leak if g() throws

```

To simplify management of dynamically-allocated objects, the result of a new expression is often stored in a smart pointer: std::auto_ptr (until C++17)std::unique_ptr, or std::shared_ptr(since C++11). These pointers guarantee that the delete expression is executed in the situations shown above.

### Notes

Itanium C++ ABI requires that the array allocation overhead is zero if the element type of the created array is trivially destructible. So does MSVC.

Some implementations (e.g. MSVC before VS 2019 v16.7) require non-zero array allocation overhead on non-allocating placement array new if the element type is not trivially destructible, which is no longer conforming since CWG issue 2382.

A non-allocating placement array new expression that creates an array of unsigned char, or std::byte(since C++17) can be used to implicitly create objects on given region of storage: it ends lifetime of objects overlapping with the array, and then implicitly creates objects of implicit-lifetime types in the array.

std::vector offers similar functionality for one-dimensional dynamic arrays.

### Keywords

new

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 74 | C++98 | value in the first dimension must have integral type | enumeration types permitted |
| CWG 299 | C++98 | value in the first dimension must have integral or enumeration type | class types with a single conversion function to integral or enumeration type permitted |
| CWG 624 | C++98 | the behavior was unspecified when the size of the allocated object would exceed the implementation-defined limit | no storage is obtained and an exception is thrown in this case |
| CWG 1748 | C++98 | non-allocating placement new need to check if the argument is null | undefined behavior for null argument |
| CWG 1992 | C++11 | new (std::nothrow) int[N] could throw std::bad_array_new_length | changed to return a null pointer |
| CWG 2102 | C++98 | it was unclear whether default/value-initialization is required to be well-formed when initializing empty arrays | required |
| CWG 2382 | C++98 | non-allocating placement array new could require allocation overhead | such allocation overhead disallowed |
| CWG 2392 | C++11 | the program might be ill-formed even if the first dimension is not potentially-evaluated | well-formed in this case |
| P1009R2 | C++11 | the array bound could not be deduced in a new expression | deduction permitted |

### See also

- constructor
- copy elision
- default constructor
- `delete`
- destructor
- initialization
  - aggregate initialization
  - default initialization
  - direct initialization
  - list initialization
  - value initialization
Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/new&oldid=178509>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 December 2024, at 16:50.