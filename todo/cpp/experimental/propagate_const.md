# std::experimental::propagate_const

From cppreference.com
< cpp‎ | experimental
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

Experimental

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Technical Specification | | | | |
| Filesystem library (filesystem TS) | | | | |
| Library fundamentals (library fundamentals TS) | | | | |
| Library fundamentals 2 (library fundamentals TS v2) | | | | |
| Library fundamentals 3 (library fundamentals TS v3) | | | | |
| Extensions for parallelism (parallelism TS) | | | | |
| Extensions for parallelism 2 (parallelism TS v2) | | | | |
| Extensions for concurrency (concurrency TS) | | | | |
| Extensions for concurrency 2") (concurrency TS v2) | | | | |
| Concepts (concepts TS) | | | | |
| Ranges (ranges TS) | | | | |
| Reflection (reflection TS) | | | | |
| Mathematical special functions (special functions TR) | | | | |
| Experimental Non-TS | | | | |
| Pattern Matching") | | | | |
| Linear Algebra") | | | | |
| std::execution | | | | |
| Contracts") | | | | |
| 2D Graphics") | | | | |

Library fundamentals v2

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| ****experimental::propagate_const**** | | | | |
| experimental::not_fn | | | | |
| experimental::observer_ptr | | | | |
| experimental::make_array | | | | |
| experimental::to_array | | | | |
| experimental::ostream_joiner | | | | |
| experimental::gcd | | | | |
| experimental::lcm | | | | |
| experimental::source_location | | | | |
| experimental::randint | | | | |
| detection idiom | | | | |
| uniform container erasure | | | | |
| logical operator type traits | | | | |

****std::experimental::propagate_const****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Member functions | | | | |
| propagate_const::propagate_const | | | | |
| propagate_const::operator= | | | | |
| propagate_const::swap | | | | |
| Observers | | | | |
| propagate_const::get | | | | |
| propagate_const::operator bool | | | | |
| propagate_const::operator\*propagate_const::operator-> | | | | |
| propagate_const::operator element_type\*propagate_const::operator const element_type\* | | | | |
| Non-member functions | | | | |
| operator==operator!=operator<operator>operator<=operator>operator>= | | | | |
| swap | | | | |
| get_underlying | | | | |
| Helper classes | | | | |
| std::hash | | | | |
| std::equal_tostd::not_equal_tostd::lessstd::greaterstd::less_equalstd::greater_equal | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<experimental/propagate_const>` |  |  |
| template< class T >  class propagate_const; |  | (library fundamentals TS v2) |
|  |  |  |

`std::experimental::propagate_const` is a const-propagating wrapper for pointers and pointer-like objects. It treats the wrapped pointer as a pointer to `const` when accessed through a `const` access path, hence the name.

The class satisfies the requirements of MoveConstructible and MoveAssignable if the underlying pointer-like type satisfies the corresponding requirement, but `propagate_const` is neither CopyConstructible nor CopyAssignable.

|  |  |  |
| --- | --- | --- |
| Type requirements | | |
| -`T` must be cv-unqualified pointer-to-object type or a cv-unqualified pointer-like class type, as specified below. | | |

### Requirements on pointer-like class types

If `T` is a class type, it must satisfy the requirements in this subsection.

Given

- `t`, a modifiable lvalue expression of type `T`,
- `ct`, an lvalue of type const T that denotes the same object as `t` (equivalent to std::as_const(t) since C++17),
- `element_type`, an object type.

The following expressions must be valid and have their specified effects:

| Expression | Return type | Pre-conditions | Operational semantics |
| --- | --- | --- | --- |
| t.get() | element_type\* |  |  |
| ct.get() | element_type\* or const element_type\* |  | t.get() == ct.get() |
| \*t | element_type& | t.get() != nullptr | \*t refers to the same object as \*(t.get()) |
| \*ct | element_type& or const element_type& | ct.get() != nullptr | \*ct refers to the same object as \*(ct.get()) |
| t.operator->() | element_type\* | t.get() != nullptr | t.operator->() == t.get() |
| ct.operator->() | element_type\* or const element_type\* | ct.get() != nullptr | ct.operator->() == ct.get() |
| (bool)t | bool |  | (bool)t is equivalent to t.get() != nullptr |
| (bool)ct | bool |  | (bool)ct is equivalent to ct.get() != nullptr |

Further, `T` and const T shall be contextually convertible to bool.

In addition, if `T` is implicitly convertible to element_type\*, then (element_type\*)t shall be equal to t.get(). Similarly, if const T is implicitly convertible to const element_type\*, then (const element_type\*)ct shall be equal to ct.get().

### Member types

|  |  |
| --- | --- |
| Member type | Definition |
| element_type | std::remove_reference_t<decltype(\*std::declval<T&>())>, the type of the object pointed to by `T` |

### Member functions

|  |  |
| --- | --- |
| (constructor) | constructs a new `propagate_const`   (public member function) |
| (destructor)(implicitly declared) | destructs a `propagate_const`, destroying the contained pointer   (public member function) |
| operator= | assigns the `propagate_const` object   (public member function) |
| swap | swaps the wrapped pointer   (public member function) |
| Observers | |
| get | returns a pointer to the object pointed to by the wrapped pointer   (public member function) |
| operator bool | checks if the wrapped pointer is null   (public member function) |
| operator\*operator-> | dereferences the wrapped pointer   (public member function) |
| operator element_type\*operator const element_type\* | implicit conversion function to pointer   (public member function) |

### Non-member functions

|  |  |
| --- | --- |
| operator==operator!=operator<operator<=operator>operator>= | compares to another `propagate_const`, another pointer, or with nullptr   (function template) |
| std::experimental::swap(std::experimental::propagate_const) | specializes the `swap` algorithm   (function template) |
| get_underlying | retrieves a reference to the wrapped pointer-like object   (function template) |

### Helper classes

|  |  |
| --- | --- |
| std::hash<std::experimental::propagate_const> | hash support for `propagate_const`   (class template specialization) |
| std::equal_to<std::experimental::propagate_const>std::not_equal_to<std::experimental::propagate_const>std::less<std::experimental::propagate_const>std::greater<std::experimental::propagate_const>std::less_equal<std::experimental::propagate_const>std::greater_equal<std::experimental::propagate_const> | specializations of the standard comparison function objects for `propagate_const`   (class template specialization) |

### Example

Run this code

```
#include <experimental/propagate_const>
#include <iostream>
#include <memory>
 
struct X
{
    void g() const { std::cout << "X::g (const)\n"; }
    void g() { std::cout << "X::g (non-const)\n"; }
};
 
struct Y
{
    Y() : m_propConstX(std::make_unique<X>()), m_autoPtrX(std::make_unique<X>()) {}
 
    void f() const
    {
        std::cout << "Y::f (const)\n";
        m_propConstX->g();
        m_autoPtrX->g();
    }
 
    void f()
    {
        std::cout << "Y::f (non-const)\n";
        m_propConstX->g();
        m_autoPtrX->g();
    }
 
    std::experimental::propagate_const<std::unique_ptr<X>> m_propConstX;
    std::unique_ptr<X> m_autoPtrX;
};
 
int main()
{
    Y y;
    y.f();
 
    const Y cy;
    cy.f();
}

```

Output:

```
Y::f (non-const)
X::g (non-const)
X::g (non-const)
Y::f (const)
X::g (const)
X::g (non-const)

```

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| LWG 3136 | LFTSv2 | meaningless `T` like int\* const, void\*, or const PtrLike were allowed | disallowed |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/experimental/propagate_const&oldid=168558>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 January 2024, at 11:01.