# Extending the namespace `std`

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

### Adding declarations to `std`

It is undefined behavior to add declarations or definitions to namespace `std` or to any namespace nested within `std`, with a few exceptions noted below.

```
#include <utility>
 
namespace std
{
    // a function definition added to namespace std: undefined behavior
    pair<int, int> operator+(pair<int, int> a, pair<int, int> b)
    {
        return {a.first + b.first, a.second + b.second};
    }
}

```

### Adding template specializations

#### Class templates

It is allowed to add template specializations for any standard library class template to the namespace `std` only if the declaration depends on at least one program-defined type and the specialization satisfies all requirements for the original template, except where such specializations are prohibited.

```
// Get the declaration of the primary std::hash template.
// We are not permitted to declare it ourselves.
// <typeindex> is guaranteed to provide such a declaration, 
// and is much cheaper to include than <functional>.
 
#include <typeindex> 
 
// Specialize std::hash so that MyType can be used as a key in 
// std::unordered_set and std::unordered_map.  Opening namespace
// std can accidentally introduce undefined behavior, and is not
// necessary for specializing class templates.
template<>
struct std::hash<MyType>
{
    std::size_t operator()(const MyType& t) const { return t.hash(); }
};

```

- Specializing the template std::complex for any type other than float, double, and long double is unspecified.

- Specializations of std::numeric_limits must define all members declared static const(until C++11)static constexpr(since C++11) in the primary template, in such a way that they are usable as integral constant expressions.

|  |  |
| --- | --- |
| - None of the templates defined in <type_traits> may be specialized for a program-defined type, except for std::common_type and std::basic_common_reference(since C++20). This includes the type traits and the class template std::integral_constant.  - Specializations of std::hash for program-defined types must satisfy Hash requirements.  - Specializations of std::atomic must have a deleted copy constructor, a deleted copy assignment operator, and a constexpr value constructor.  - Specializations of std::shared_ptr and std::weak_ptr must be CopyConstructible and CopyAssignable. In addition, specializations of std::shared_ptr must be LessThanComparable, and convertible to bool.  - Specializations of std::istreambuf_iterator must have a trivial copy constructor, a constexpr default constructor, and a trivial destructor. | (since C++11) |

|  |  |
| --- | --- |
| - std::unary_function and std::binary_function may not be specialized. | (until C++17) |

It is undefined behavior to declare a full or partial specialization of any member class template of a standard library class or class template.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: mini-example |

#### Function templates and member functions of templates

|  |  |
| --- | --- |
| It is allowed to add template specializations for any standard library function template to the namespace `std` only if the declaration depends on at least one program-defined type and the specialization satisfies all requirements for the original template, except where such specializations are prohibited. | (until C++20) |
| It is undefined behavior to declare a full specialization of any standard library function template. | (since C++20) |

|  |  |
| --- | --- |
|  | This section is incomplete Reason: mini-example |

It is undefined behavior to declare a full specialization of any member function of a standard library class template:

|  |  |
| --- | --- |
|  | This section is incomplete Reason: mini-example |

It is undefined behavior to declare a full specialization of any member function template of a standard library class or class template:

|  |  |
| --- | --- |
|  | This section is incomplete Reason: mini-example |

#### Variable templates

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| It is undefined behavior to declare a full or partial specialization of any standard library variable template, except where explicitly allowed.   |  |  | | --- | --- | |  | This section is incomplete Reason: mini-example |  |  |  | | --- | --- | | - Specializations of std::disable_sized_sentinel_for, std::ranges::disable_sized_range, std::ranges::enable_view and std::ranges::enable_borrowed_range shall be usable in constant expressions and have type const bool. And   - `std::disable_sized_sentinel_for` may be specialized for cv-unqualified non-array object types `S` and `I` at least one of which is a program-defined type.   - `std::ranges::disable_sized_range`, `std::ranges::enable_view` and `std::ranges::enable_borrowed_range` may be specialized for cv-unqualified program-defined types. - Every mathematical constant variable template may be partially or explicitly specialized, provided that the specialization depends on a program-defined type. | (since C++20) | | (since C++14) |

### Explicit instantiation of templates

It is allowed to explicitly instantiate a class (since C++20)template defined in the standard library only if the declaration depends on the name of at least one program-defined type and the instantiation meets the standard library requirements for the original template.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: mini-example |

### Other restrictions

The namespace `std` may not be declared as an inline namespace.

|  |  |
| --- | --- |
| Addressing restriction The behavior of a C++ program is unspecified (possibly ill-formed) if it explicitly or implicitly attempts to form a pointer, reference (for free functions and static member functions) or pointer-to-member (for non-static member functions) to a standard library function or an instantiation of a standard library function template, unless it is designated an **addressable function** (see below).  Following code was well-defined in C++17, but leads to unspecified behaviors and possibly fails to compile since C++20:   ```text #include <cmath> #include <memory>   int main() {     // by unary operator&     auto fptr0 = &static_cast<float(&)(float, float)>(std::betaf);       // by std::addressof     auto fptr1 = std::addressof(static_cast<float(&)(float, float)>(std::betaf));       // by function-to-pointer implicit conversion     auto fptr2 = static_cast<float(&)(float)>(std::riemann_zetaf);       // forming a reference     auto& fref = static_cast<float(&)(float)>(std::riemann_zetaf); } ```  Designated addressable functions  - I/O manipulators:   - `fmtflags` manipulators:     - std::boolalpha     - std::noboolalpha     - std::showbase     - std::noshowbase     - std::showpoint     - std::noshowpoint     - std::showpos     - std::noshowpos     - std::skipws     - std::noskipws     - std::uppercase     - std::nouppercase     - std::unitbuf     - std::nounitbuf   - `adjustfield` manipulators:     - std::internal     - std::left     - std::right   - `basefield` manipulators:     - std::dec     - std::hex     - std::oct   - `floatfield` manipulators:     - std::fixed     - std::scientific     - std::hexfloat     - std::defaultfloat   - `basic_istream` manipulators:     - std::ws   - `basic_ostream` manipulators:     - std::endl     - std::ends     - std::flush     - std::emit_on_flush     - std::noemit_on_flush     - std::flush_emit | (since C++20) |

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 120 | C++98 | users could explicitly instantiate standard library templates for non-user defined types | prohibited |
| LWG 232 | C++98 | users could explicitly specialize standard library templates if the declaration depends on a user-defined name of external linkage (which can refer to a non-user-defined type) | only allowed for user-defined types |
| LWG 422 | C++98 | users could specialize individual members or member templates without specializing the whole standard library class or class template | the behavior is undefined in this case |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/extending_std&oldid=170135>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 March 2024, at 13:18.