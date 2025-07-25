# Pack indexing (since C++26)

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `new` expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `delete` expression | | | | | |
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

Declarations

|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Overview | | | | | | Declaration syntax | | | | | | **decl-specifier-seq** | | | | | | Declarator | | | | | | Conflicting declarations | | | | | | Specifiers | | | | | | typedef | | | | | | inline | | | | | | virtual function specifier | | | | | | explicit function specifier | | | | | | friend | | | | | | constexpr(C++11) | | | | | | consteval(C++20) | | | | | | constinit(C++20) | | | | | | Storage class specifiers | | | | | | Translation-unit-local (C++20) | | | | | | class/struct | | | | | | union | | | | | | enum | | | | | | decltype(C++11) | | | | | | auto(C++11) | | | | | | alignas(C++11) | | | | | | constvolatile | | | | | | Pack indexing specifier (C++26) | | | | | | Elaborated type specifier | | | | | | Attributes (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Declarators | | | | | | Reference | | | | | | Pointer | | | | | | Array | | | | | | Block declarations | | | | | | Simple-declaration | | | | | | →Structured binding declaration (C++17) | | | | | | Alias declaration (C++11) | | | | | | Namespace alias definition | | | | | | using declaration | | | | | | `using` directive | | | | | | static_assert declaration (C++11) | | | | | | asm declaration | | | | | | Opaque enum declaration (C++11) | | | | | | Other declarations | | | | | | Namespace definition | | | | | | Function declaration | | | | | | Class template declaration | | | | | | Function template declaration | | | | | | Explicit template instantiation (C++11) | | | | | | Explicit template specialization | | | | | | Linkage specification | | | | | | Attribute declaration (C++11) | | | | | | Empty declaration | | | | | |  | | | | | |

 Expressions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | Constant expressions | | | | | | Primary expressions | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Lambda expressions (C++11) | | | | | | Requires expressions (C++20) | | | | | | Pack indexing expression (C++26) | | | | | | Potentially-evaluated expressions | | | | | |
| Literals | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Integer literals | | | | | | Floating-point literals | | | | | | Boolean literals | | | | | | Character literals | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Escape sequences | | | | | | String literals | | | | | | Null pointer literal (C++11) | | | | | | User-defined literal (C++11) | | | | | |
| Operators | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Assignment operators | | | | | | Increment and decrement | | | | | | Arithmetic operators | | | | | | Logical operators | | | | | | Comparison operators | | | | | | Member access operators | | | | | | Other operators | | | | | | `new`-expression | | | | | | `delete`-expression | | | | | | `throw`-expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `alignof` | | | | | | `sizeof` | | | | | | `sizeof...` (C++11) | | | | | | `typeid` | | | | | | `noexcept` (C++11) | | | | | | Fold expressions (C++17) | | | | | | Alternative representations of operators | | | | | | Precedence and associativity | | | | | | Operator overloading | | | | | | Default comparisons (C++20) | | | | | |
| Conversions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | Explicit conversions | | | | | | Usual arithmetic conversions | | | | | | User-defined conversion | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const_cast` | | | | | | `static_cast` | | | | | | `dynamic_cast` | | | | | | `reinterpret_cast` | | | | | |

 Templates

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Parameters and arguments | | | | |
| Class templates | | | | |
| Function templates | | | | |
| Class member templates | | | | |
| Variable templates (C++14) | | | | |
| Template argument deduction | | | | |
| Class template argument deduction (C++17) | | | | |
| Explicit (full) specialization | | | | |
| Partial specialization | | | | |
| Dependent names | | | | |
| Packs (C++11) | | | | |
| `sizeof...` (C++11) | | | | |
| Fold expressions (C++17) | | | | |
| ****Pack indexing**** (C++26) | | | | |
| SFINAE | | | | |
| Constraints and concepts (C++20) | | | | |
| Requires expression (C++20) | | | | |

Accesses the element of a pack at a specified index.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| id-expression `...[` expression `]` | (1) |  |
|  | | | | | | | | | |
| typedef-name `...[` expression `]` | (2) |  |
|  | | | | | | | | | |

1) Pack indexing expression2) Pack indexing specifier

|  |  |  |
| --- | --- | --- |
| typedef-name | - | an identifier or a simple-template-id that names a pack |
| id-expression | - | an id-expression that names a pack |
| expression | - | a converted constant expression I of type std::size_t designated as index where I is within the range `[`​0​`,`sizeof...(P)`)` for some pack P in pack indexing |

### Explanation

Pack indexing is a **pack expansion** of the unexpanded pack followed by an ellipsis and index inside the subscript. There are two kinds of pack indexing: pack indexing expression and pack indexing specifier.

Let `P` be a non-empty pack containing `P0, P1, ..., Pn-1` and `I` be a valid index, the instantiation of the expansion `P...[I]` yields the pack element `PI` of `P`.

Indexing a pack with non-constant expression index `I` is not allowed.

```
int runtime_idx();
 
void bar(auto... args)
{
    auto a = args...[0];
    const int n = 1;
    auto b = args...[n];
    int m = 2;
    auto c = args...[m]; // error: 'm' is not a constant expression
    auto d = args...[runtime_idx()]; // error: 'runtime_idx()' is not a constant expression
}

```

Indexing a pack of template template parameters is not possible.

```
template <template <typename...> typename... Temps>
using A = Temps...[0]<>; // error: 'Temps' is a pack of template template parameters
 
template <template <typename...> typename... Temps>
using B = Temps<>...[0]; // error: 'Temps<>' doesn't denote pack name 
                         // although it is a simple-template-id

```

### Pack indexing expression

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| id-expression `...[` expression `]` |  |  |
|  | | | | | | | | | |

Pack indexing expression denotes the **id-expression**, the expression of pack element `PI`. The id-expression shall be introduced by the declaration of:

- non-type template parameter pack,
- function parameter pack,
- lambda init-capture pack, or
- structured binding pack.

```
template <std::size_t I, typename... Ts>
constexpr auto element_at(Ts... args)
{
    // 'args' introduced in function parameter pack declaration
    return args...[I];
}
 
static_assert(element_at<0>(3, 5, 9) == 3);
static_assert(element_at<2>(3, 5, 9) == 9);
static_assert(element_at<3>(3, 5, 9) == 4); // error:  out of bounds
static_assert(element_at<0>() == 1); // error: out of bounds, empty pack
 
template <std::size_t I, typename Tup>
constexpr auto structured_binding_element_at(Tup tup)
{
    auto [...elems] = tup;
    // 'elems' introduced in structured binding pack declaration
    return elems...[I];
}
 
struct A { bool a; int b; };
 
static_assert(structured_binding_element_at<0>(A {true, 4}) == true);
static_assert(structured_binding_element_at<1>(A {true, 4}) == 4);
 
// 'Vals' introduced in non-type template parameter pack declaration
template <std::size_t I, std::size_t... Vals>
constexpr std::size_t double_at = Vals...[I] * 2; // OK
 
template <std::size_t I, typename... Args>
constexpr auto foo(Args... args)
{
    return ...members = args
    {
        // 'members' introduced in lambda init-capture pack
        return members...[I] + op;
    };
}
 
static_assert(foo<0>(4, "Hello", true)(5) == 9);
static_assert(foo<1>(3, std::string("C++"))("26") == "C++26");

```

Indexing pack of complex expressions other than id-expression is not allowed.

```
template <std::size_t I, auto... Vals>
constexpr auto identity_at = (Vals)...[I]; // error
// use 'Vals...[I]' instead
 
template <std::size_t I, std::size_t... Vals>
constexpr std::size_t triple_at = (Vals * 3)...[I]; // error
// use 'Vals...[I] * 3' instead
 
template <std::size_t I, typename... Args>
constexpr decltype(auto) get(Args&&... args) noexcept
{
    return std::forward<Args>(args)...[I]; // error
    // use 'std::forward<Args...[I]>(args...[I])' instead
}

```

Applying `decltype` to pack indexing expression is the same as applying `decltype` to id-expression.

```
void f() 
{
    [](auto... args)
    {
        using T0 = decltype(args...[0]);   // 'T0' is 'double'
        using T1 = decltype((args...[0])); // 'T1' is 'double&'
    }(3.14);
}

```

### Pack indexing specifier

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| typedef-name `...[` expression `]` |  |  |
|  | | | | | | | | | |

Pack indexing specifier denotes the **computed-type-specifier**, the type of pack element `PI`. The typedef-name shall be introduced by the declaration of type template parameter pack.

```
template <typename... Ts>
using last_type_t = Ts...[sizeof...(Ts) - 1];
 
static_assert(std::is_same_v<last_type_t<>, int>); // error: out of bounds
static_assert(std::is_same_v<last_type_t<int>, int>);
static_assert(std::is_same_v<last_type_t<bool, char>, char>);
static_assert(std::is_same_v<last_type_t<float, int, bool*>, bool*>);

```

Pack indexing specifier can appear as:

- a simple type specifier,
- a base class specifier,
- a nested name specifier, or
- the type of an explicit destructor call.

Pack indexing specifier can be used in function or constructor parameter list to establish non-deduced contexts in template argument deduction.

```
template <typename...>
struct type_seq {};
 
template <typename... Ts>
auto f(Ts...[0] arg, type_seq<Ts...>)
{
    return arg;
}
 
// OK: "Hello" is implicitly converted to 'std::string_view'
std::same_as<std::string_view> auto a = f("Hello", type_seq<std::string_view>{});
 
// Error: "Ok" is not convertible to 'int'
std::same_as<int> auto b = f("Ok", type_seq<int, const char*>{});

```

### Notes

Before C++26, Ts...[N] was a valid syntax for declaring function parameter pack of unnamed arrays of size N, where the parameter types were further adjusted to pointers. Since C++26, Ts...[1] is interpreted as a pack indexing specifier which would change the behavior below to #2. To preserve the first behavior, the function parameter pack must be named, or manually adjusted to a pack of pointer types.

```
template <typename... Ts>
void f(Ts... [1]);
 
template <typename... Ts>
void g(Ts... args[1]);
 
template <typename... Ts>
void h(Ts*...); // clearer but more permissive: Ts... can contain cv void or function types
 
void foo() 
{
    f<char, bool>(nullptr, nullptr);
    // behavior #1 (before C++26):
    //  calls void 'f<char, bool>(char*, bool*)' (aka 'f<char, bool>(char[1], bool[1])')
    // behavior #2 (since C++26): 
    //  error: supposedly called 'void f<char, bool>(bool)'
    //  but provided with 2 arguments instead of 1
 
    g<char, bool>(nullptr, nullptr);
    // calls 'g<char, bool>(char*, bool*)' (aka 'g<char, bool>(char[1], bool[1])')
 
    h<char, bool>(nullptr, nullptr);
    // calls 'h<char, bool>(char*, bool*)'
}

```

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_pack_indexing` | `202311L` | (C++26) | Pack indexing |

### Example

Run this code

```
#include <tuple>
 
template <std::size_t... Indices, typename Decomposable>
constexpr auto splice(Decomposable d)
{
    auto [...elems] = d;
    return std::make_tuple(elems...[Indices]...);
}
 
struct Point
{
    int x;
    int y;
    int z;
};
 
int main() 
{
    constexpr Point p { .x = 1, .y = 4, .z = 3 };
    static_assert(splice<2, 1, 0>(p) == std::make_tuple(3, 4, 1));
    static_assert(splice<1, 1, 0, 0>(p) == std::make_tuple(4, 4, 1, 1));
}

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/pack_indexing&oldid=178140>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 3 December 2024, at 22:17.