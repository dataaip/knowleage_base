# PImpl

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

"Pointer to implementation" or "pImpl" is a C++ programming technique that removes implementation details of a class from its object representation by placing them in a separate class, accessed through an opaque pointer:

```
// --------------------
// interface (widget.h)
struct widget
{
    // public members
private:
    struct impl; // forward declaration of the implementation class
    // One implementation example: see below for other design options and trade-offs
    std::experimental::propagate_const< // const-forwarding pointer wrapper
        std::unique_ptr<                // unique-ownership opaque pointer
            impl>> pImpl;               // to the forward-declared implementation class
};
 
// ---------------------------
// implementation (widget.cpp)
struct widget::impl
{
    // implementation details
};

```

This technique is used to construct C++ library interfaces with stable ABI and to reduce compile-time dependencies.

### Explanation

Because private data members of a class participate in its object representation, affecting size and layout, and because private member functions of a class participate in overload resolution (which takes place before member access checking), any change to those implementation details requires recompilation of all users of the class.

pImpl removes this compilation dependency; changes to the implementation do not cause recompilation. Consequently, if a library uses pImpl in its ABI, newer versions of the library may change the implementation while remaining ABI-compatible with older versions.

### Trade-offs

The alternatives to the pImpl idiom are

- inline implementation: private members and public members are members of the same class.
- pure abstract class (OOP factory): users obtain a unique pointer to a lightweight or abstract base class, the implementation details are in the derived class that overrides its virtual member functions.

#### Compilation firewall

In simple cases, both pImpl and factory method remove compile-time dependency between the implementation and the users of the class interface. Factory method creates a hidden dependency on the vtable, and so reordering, adding, or removing virtual member functions breaks the ABI. The pImpl approach has no hidden dependencies, however if the implementation class is a class template specialization, the compilation firewall benefit is lost: the users of the interface must observe the entire template definition in order to instantiate the correct specialization. A common design approach in this case is to refactor the implementation in a way that avoids parametrization, this is another use case for the C++ Core Guidelines:

- T.61 Do not over-parametrize members and
- T.84 Use a non-template core implementation to provide an ABI-stable interface.

For example, the following class template does not use the type `T` in its private member or in the body of `push_back`:

```
template<class T>
class ptr_vector
{
    std::vector<void*> vp;
public:
    void push_back(T* p)
    {
        vp.push_back(p);
    }
};

```

Therefore, private members can be transferred to implementation as-is, and `push_back` can forward to an implementation that does not use `T` in the interface either:

Run this code

```
// ---------------------
// header (ptr_vector.hpp)
#include <memory>
 
class ptr_vector_base
{
    struct impl; // does not depend on T
    std::unique_ptr<impl> pImpl;
protected:
    void push_back_fwd(void*);
    void print() const;
    // ... see implementation section for special member functions
public:
    ptr_vector_base();
    ~ptr_vector_base();
};
 
template<class T>
class ptr_vector : private ptr_vector_base
{
public:
    void push_back(T* p) { push_back_fwd(p); }
    void print() const { ptr_vector_base::print(); }
};
 
// -----------------------
// source (ptr_vector.cpp)
// #include "ptr_vector.hpp"
#include <iostream>
#include <vector>
 
struct ptr_vector_base::impl
{
    std::vector<void*> vp;
 
    void push_back(void* p)
    {
        vp.push_back(p);
    }
 
    void print() const
    {
        for (void const * const p: vp) std::cout << p << '\n';
    }
};
 
void ptr_vector_base::push_back_fwd(void* p) { pImpl->push_back(p); }
ptr_vector_base::ptr_vector_base() : pImpl{std::make_unique<impl>()} {}
ptr_vector_base::~ptr_vector_base() {}
void ptr_vector_base::print() const { pImpl->print(); }
 
// ---------------
// user (main.cpp)
// #include "ptr_vector.hpp"
 
int main()
{
    int x{}, y{}, z{};
    ptr_vector<int> v;
    v.push_back(&x);
    v.push_back(&y);
    v.push_back(&z);
    v.print();
}

```

Possible output:

```
0x7ffd6200a42c
0x7ffd6200a430
0x7ffd6200a434

```

#### Runtime overhead

- Access overhead: In pImpl, each call to a private member function indirects through a pointer. Each access to a public member made by a private member indirects through another pointer. Both indirections cross translation unit boundaries and so can only be optimized out by link-time optimization. Note that OO factory requires indirection across translation units to access both public data and implementation detail, and offers even fewer opportunities for the link time optimizer due to virtual dispatch.
- Space overhead: pImpl adds one pointer to the public component and, if any private member needs access to a public member, another pointer is either added to the implementation component or passed as a parameter for each call to the private member that requires it. If stateful custom allocators are supported, the allocator instance also has to be stored.
- Lifetime management overhead: pImpl (as well as OO factory) place the implementation object on the heap, which imposes significant runtime overhead at construction and destruction. This may be partially offset by custom allocators, since allocation size for pImpl (but not OO factory) is known at compile time.

On the other hand, pImpl classes are move-friendly; refactoring a large class as movable pImpl may improve performance of algorithms that manipulate containers holding such objects, although movable pImpl has an additional source of runtime overhead: any public member function that is permitted on a moved-from object and needs access to private implementation incurs a null pointer check.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: Microbenchmark?) |

#### Maintenance overhead

Use of pImpl requires a dedicated translation unit (a header-only library cannot use pImpl), introduces an additional class, a set of forwarding functions, and, if allocators are used, exposes the implementation detail of allocator use in the public interface.

Since virtual members are part of the interface component of pImpl, mocking a pImpl implies mocking the interface component alone. A testable pImpl is typically designed to allow full test coverage through the available interface.

### Implementation

As the object of the interface type controls the lifetime of the object of the implementation type, the pointer to implementation is usually std::unique_ptr.

Because std::unique_ptr requires that the pointed-to type is a complete type in any context where the deleter is instantiated, the special member functions must be user-declared and defined out-of-line, in the implementation file, where the implementation class is complete.

Because when const member function calls a function through a non-const member pointer, the non-const overload of the implementation function is called, the pointer has to be wrapped in std::experimental::propagate_const or equivalent.

All private data members and all private non-virtual member functions are placed in the implementation class. All public, protected, and virtual members remain in the interface class (see GOTW #100 for the discussion of the alternatives).

If any of the private members needs to access a public or protected member, a reference or pointer to the interface may be passed to the private function as a parameter. Alternatively, the back-reference may be maintained as part of the implementation class.

If non-default allocators are intended to be supported for the allocation of the implementation object, any of the usual allocator awareness patterns may be utilized, including allocator template parameter defaulting to std::allocator and constructor argument of type std::pmr::memory_resource\*.

### Notes

|  |  |
| --- | --- |
|  | This section is incomplete Reason: note connection to value-semantic polymorphism |

### Example

Demonstrates a pImpl with const propagation, with back-reference passed as a parameter, without allocator awareness, and move-enabled without runtime checks:

Run this code

```
// ----------------------
// interface (widget.hpp)
#include <experimental/propagate_const>
#include <iostream>
#include <memory>
 
class widget
{
    class impl;
    std::experimental::propagate_const<std::unique_ptr<impl>> pImpl;
public:
    void draw() const; // public API that will be forwarded to the implementation
    void draw();
    bool shown() const { return true; } // public API that implementation has to call
 
    widget(); // even the default ctor needs to be defined in the implementation file
              // Note: calling draw() on default constructed object is UB
    explicit widget(int);
    ~widget(); // defined in the implementation file, where impl is a complete type
    widget(widget&&); // defined in the implementation file
                      // Note: calling draw() on moved-from object is UB
    widget(const widget&) = delete;
    widget& operator=(widget&&); // defined in the implementation file
    widget& operator=(const widget&) = delete;
};
 
// ---------------------------
// implementation (widget.cpp)
// #include "widget.hpp"
 
class widget::impl
{
    int n; // private data
public:
    void draw(const widget& w) const
    {
        if (w.shown()) // this call to public member function requires the back-reference 
            std::cout << "drawing a const widget " << n << '\n';
    }
 
    void draw(const widget& w)
    {
        if (w.shown())
            std::cout << "drawing a non-const widget " << n << '\n';
    }
 
    impl(int n) : n(n) {}
};
 
void widget::draw() const { pImpl->draw(*this); }
void widget::draw() { pImpl->draw(*this); }
widget::widget() = default;
widget::widget(int n) : pImpl{std::make_unique<impl>(n)} {}
widget::widget(widget&&) = default;
widget::~widget() = default;
widget& widget::operator=(widget&&) = default;
 
// ---------------
// user (main.cpp)
// #include "widget.hpp"
 
int main()
{
    widget w(7);
    const widget w2(8);
    w.draw();
    w2.draw();
}

```

Output:

```
drawing a non-const widget 7
drawing a const widget 8

```

|  |  |
| --- | --- |
|  | This section is incomplete Reason: describe yet another alternative — "fast PImpl". The main difference is that the memory for the implementation is reserved in a data member that is an opaque C-array (inside the PImpl class definition), while in cpp file that memory is mapped (via `reinterpret_cast` or placement-`new`) to the implementation structure. This approach has it's own pros and cons, in particular, an obvious **pro** is no extra allocation, on condition that enough memory was initially reserved at **design-time** of the PImpl class. (Whereas among **cons** is reduced move-friendliness.) |

### External links

|  |  |
| --- | --- |
| 1. | GotW #28 : The Fast Pimpl Idiom. |
| 2. | GotW #100: Compilation Firewalls. |
| 3. | The Pimpl Pattern - what you should know. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/pimpl&oldid=178591>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 December 2024, at 14:03.