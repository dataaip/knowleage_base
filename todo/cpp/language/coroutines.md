# Coroutines (C++20)

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

 Functions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Declarations | | | | |
| Function declaration | | | | |
| Function parameter list | | | | |
| Function definition | | | | |
| Default arguments | | | | |
| Variadic arguments | | | | |
| `inline` specifier | | | | |
| Lambda expressions (C++11) | | | | |
| ****Coroutines**** (C++20) | | | | |
| Function calls | | | | |
| Argument-Dependent Lookup (ADL) | | | | |
| Function-call operator | | | | |
| Function objects | | | | |
| Overloading | | | | |
| Overload resolution | | | | |
| Operator overloading | | | | |
| Address of an overload set | | | | |

A coroutine is a function that can suspend execution to be resumed later. Coroutines are stackless: they suspend execution by returning to the caller, and the data that is required to resume execution is stored separately from the stack. This allows for sequential code that executes asynchronously (e.g. to handle non-blocking I/O without explicit callbacks), and also supports algorithms on lazy-computed infinite sequences and other uses.

A function is a coroutine if its definition contains any of the following:

- the co_await expression — to suspend execution until resumed

```
task<> tcp_echo_server()
{
    char data[1024];
    while (true)
    {
        std::size_t n = co_await socket.async_read_some(buffer(data));
        co_await async_write(socket, buffer(data, n));
    }
}

```

- the co_yield expression — to suspend execution returning a value

```
generator<unsigned int> iota(unsigned int n = 0)
{
    while (true)
        co_yield n++;
}

```

- the co_return statement — to complete execution returning a value

```
lazy<int> f()
{
    co_return 7;
}

```

Every coroutine must have a return type that satisfies a number of requirements, noted below.

### Restrictions

Coroutines cannot use variadic arguments, plain return statements, or placeholder return types (`auto` or Concept).

Consteval functions, constexpr functions, constructors, destructors, and the main function cannot be coroutines.

### Execution

Each coroutine is associated with

- the **promise object**, manipulated from inside the coroutine. The coroutine submits its result or exception through this object. Promise objects are in no way related to std::promise.
- the **coroutine handle**, manipulated from outside the coroutine. This is a non-owning handle used to resume execution of the coroutine or to destroy the coroutine frame.
- the **coroutine state**, which is internal, dynamically-allocated storage (unless the allocation is optimized out), object that contains

:   - the promise object
    - the parameters (all copied by value)
    - some representation of the current suspension point, so that a resume knows where to continue, and a destroy knows what local variables were in scope
    - local variables and temporaries whose lifetime spans the current suspension point.

When a coroutine begins execution, it performs the following:

- allocates the coroutine state object using operator new.
- copies all function parameters to the coroutine state: by-value parameters are moved or copied, by-reference parameters remain references (thus, may become dangling, if the coroutine is resumed after the lifetime of referred object ends — see below for examples).
- calls the constructor for the promise object. If the promise type has a constructor that takes all coroutine parameters, that constructor is called, with post-copy coroutine arguments. Otherwise the default constructor is called.
- calls promise.get_return_object() and keeps the result in a local variable. The result of that call will be returned to the caller when the coroutine first suspends. Any exceptions thrown up to and including this step propagate back to the caller, not placed in the promise.
- calls promise.initial_suspend() and `co_await`s its result. Typical `Promise` types either return a std::suspend_always, for lazily-started coroutines, or std::suspend_never, for eagerly-started coroutines.
- when co_await promise.initial_suspend() resumes, starts executing the body of the coroutine.

Some examples of a parameter becoming dangling:

```
#include <coroutine>
#include <iostream>
 
struct promise;
 
struct coroutine : std::coroutine_handle<promise>
{
    using promise_type = ::promise;
};
 
struct promise
{
    coroutine get_return_object() { return {coroutine::from_promise(*this)}; }
    std::suspend_always initial_suspend() noexcept { return {}; }
    std::suspend_always final_suspend() noexcept { return {}; }
    void return_void() {}
    void unhandled_exception() {}
};
 
struct S
{
    int i;
    coroutine f()
    {
        std::cout << i;
        co_return;
    }
};
 
void bad1()
{
    coroutine h = S{0}.f();
    // S{0} destroyed
    h.resume(); // resumed coroutine executes std::cout << i, uses S::i after free
    h.destroy();
}
 
coroutine bad2()
{
    S s{0};
    return s.f(); // returned coroutine can't be resumed without committing use after free
}
 
void bad3()
{
    coroutine h = [i = 0]() -> coroutine // a lambda that's also a coroutine
    {
        std::cout << i;
        co_return;
    }(); // immediately invoked
    // lambda destroyed
    h.resume(); // uses (anonymous lambda type)::i after free
    h.destroy();
}
 
void good()
{
    coroutine h = [](int i) -> coroutine // make i a coroutine parameter
    {
        std::cout << i;
        co_return;
    }(0);
    // lambda destroyed
    h.resume(); // no problem, i has been copied to the coroutine
                // frame as a by-value parameter
    h.destroy();
}

```

When a coroutine reaches a suspension point

- the return object obtained earlier is returned to the caller/resumer, after implicit conversion to the return type of the coroutine, if necessary.

When a coroutine reaches the co_return statement, it performs the following:

- calls promise.return_void() for

:   - co_return;
    - co_return expr; where expr has type void

- or calls promise.return_value(expr) for co_return expr; where expr has non-void type
- destroys all variables with automatic storage duration in reverse order they were created.
- calls promise.final_suspend() and co_awaits the result.

Falling off the end of the coroutine is equivalent to co_return;, except that the behavior is undefined if no declarations of `return_void` can be found in the scope of `Promise`. A function with none of the defining keywords in its function body is not a coroutine, regardless of its return type, and falling off the end results in undefined behavior if the return type is not (possibly cv-qualified) void.

```
// assuming that task is some coroutine task type
task<void> f()
{
    // not a coroutine, undefined behavior
}
 
task<void> g()
{
    co_return;  // OK
}
 
task<void> h()
{
    co_await g();
    // OK, implicit co_return;
}

```

If the coroutine ends with an uncaught exception, it performs the following:

- catches the exception and calls promise.unhandled_exception() from within the catch-block
- calls promise.final_suspend() and co_awaits the result (e.g. to resume a continuation or publish a result). It's undefined behavior to resume a coroutine from this point.

When the coroutine state is destroyed either because it terminated via co_return or uncaught exception, or because it was destroyed via its handle, it does the following:

- calls the destructor of the promise object.
- calls the destructors of the function parameter copies.
- calls operator delete to free the memory used by the coroutine state.
- transfers execution back to the caller/resumer.

### Dynamic allocation

Coroutine state is allocated dynamically via non-array operator new.

If the `Promise` type defines a class-level replacement, it will be used, otherwise global operator new will be used.

If the `Promise` type defines a placement form of operator new that takes additional parameters, and they match an argument list where the first argument is the size requested (of type std::size_t) and the rest are the coroutine function arguments, those arguments will be passed to operator new (this makes it possible to use leading-allocator-convention for coroutines).

The call to operator new can be optimized out (even if custom allocator is used) if

- The lifetime of the coroutine state is strictly nested within the lifetime of the caller, and
- the size of coroutine frame is known at the call site.

In that case, coroutine state is embedded in the caller's stack frame (if the caller is an ordinary function) or coroutine state (if the caller is a coroutine).

If allocation fails, the coroutine throws std::bad_alloc, unless the `Promise` type defines the member function Promise::get_return_object_on_allocation_failure(). If that member function is defined, allocation uses the nothrow form of operator new and on allocation failure, the coroutine immediately returns the object obtained from Promise::get_return_object_on_allocation_failure() to the caller, e.g.:

```
struct Coroutine::promise_type
{
    /* ... */
 
    // ensure the use of non-throwing operator-new
    static Coroutine get_return_object_on_allocation_failure()
    {
        std::cerr << __func__ << '\n';
        throw std::bad_alloc(); // or, return Coroutine(nullptr);
    }
 
    // custom non-throwing overload of new
    void* operator new(std::size_t n) noexcept
    {
        if (void* mem = std::malloc(n))
            return mem;
        return nullptr; // allocation failure
    }
};

```

### Promise

The `Promise` type is determined by the compiler from the return type of the coroutine using std::coroutine_traits.

Formally, let

- `R` and `Args...` denote the return type and parameter type list of a coroutine respectively,
- `ClassT` denote the class type to which the coroutine belongs if it is defined as a non-static member function,
- cv denote the cv-qualification declared in the function declaration if it is defined as a non-static member function,

its `Promise` type is determined by:

- std::coroutine_traits<R, Args...>::promise_type, if the coroutine is not defined as an implicit object member function,
- std::coroutine_traits<R,cvClassT&, Args...>::promise_type, if the coroutine is defined as an implicit object member function that is not rvalue-reference-qualified,
- std::coroutine_traits<R,cvClassT&&, Args...>::promise_type, if the coroutine is defined as an implicit object member function that is rvalue-reference-qualified.

For example:

| If the coroutine is defined as ... | then its `Promise` type is ... |
| --- | --- |
| task<void> foo(int x); | std::coroutine_traits<task<void>, int>::promise_type |
| task<void> Bar::foo(int x) const; | std::coroutine_traits<task<void>, const Bar&, int>::promise_type |
| task<void> Bar::foo(int x) &&; | std::coroutine_traits<task<void>, Bar&&, int>::promise_type |

### co_await

The unary operator co_await suspends a coroutine and returns control to the caller.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `co_await` expr |  |  |
|  | | | | | | | | | |

A co_await expression can only appear in a potentially-evaluated expression within a regular function body (including the function body of a lambda expression), and cannot appear

- in a handler,
- in a declaration statement, unless it appears in an initializer of that declaration statement,
- in the simple declaration of an init-statement (see `if`, `switch`, `for` and range-for), unless it appears in an initializer of that init-statement,
- in a default argument, or
- in the initializer of a block-scope variable with static or thread storage duration.

First, expr is converted to an awaitable as follows:

- if expr is produced by an initial suspend point, a final suspend point, or a yield expression, the awaitable is expr, as-is.
- otherwise, if the current coroutine's `Promise` type has the member function `await_transform`, then the awaitable is promise.await_transform(expr).
- otherwise, the awaitable is expr, as-is.

Then, the awaiter object is obtained, as follows:

- if overload resolution for operator co_await gives a single best overload, the awaiter is the result of that call:

:   - awaitable.operator co_await() for member overload,
    - operator co_await(static_cast<Awaitable&&>(awaitable)) for the non-member overload.

- otherwise, if overload resolution finds no operator co_await, the awaiter is awaitable, as-is.
- otherwise, if overload resolution is ambiguous, the program is ill-formed.

If the expression above is a prvalue, the awaiter object is a temporary materialized from it. Otherwise, if the expression above is a glvalue, the awaiter object is the object to which it refers.

Then, awaiter.await_ready() is called (this is a short-cut to avoid the cost of suspension if it's known that the result is ready or can be completed synchronously). If its result, contextually-converted to bool is false then

:   The coroutine is suspended (its coroutine state is populated with local variables and current suspension point).
:   awaiter.await_suspend(handle) is called, where handle is the coroutine handle representing the current coroutine. Inside that function, the suspended coroutine state is observable via that handle, and it's this function's responsibility to schedule it to resume on some executor, or to be destroyed (returning false counts as scheduling)

    - if `await_suspend` returns void, control is immediately returned to the caller/resumer of the current coroutine (this coroutine remains suspended), otherwise
    - if `await_suspend` returns bool,

    :   - the value true returns control to the caller/resumer of the current coroutine
        - the value false resumes the current coroutine.

    - if `await_suspend` returns a coroutine handle for some other coroutine, that handle is resumed (by a call to handle.resume()) (note this may chain to eventually cause the current coroutine to resume).
    - if `await_suspend` throws an exception, the exception is caught, the coroutine is resumed, and the exception is immediately re-thrown.

Finally, awaiter.await_resume() is called (whether the coroutine was suspended or not), and its result is the result of the whole co_await expr expression.

If the coroutine was suspended in the co_await expression, and is later resumed, the resume point is immediately before the call to awaiter.await_resume().

Note that the coroutine is fully suspended before entering awaiter.await_suspend(). Its handle can be shared with another thread and resumed before the await_suspend() function returns. (Note that the default memory safety rules still apply, so if a coroutine handle is shared across threads without a lock, the awaiter should use at least release semantics and the resumer should use at least acquire semantics.) For example, the coroutine handle can be put inside a callback, scheduled to run on a threadpool when async I/O operation completes. In that case, since the current coroutine may have been resumed and thus executed the awaiter object's destructor, all concurrently as await_suspend() continues its execution on the current thread, await_suspend() should treat \*this as destroyed and not access it after the handle was published to other threads.

### Example

Run this code

```
#include <coroutine>
#include <iostream>
#include <stdexcept>
#include <thread>
 
auto switch_to_new_thread(std::jthread& out)
{
    struct awaitable
    {
        std::jthread* p_out;
        bool await_ready() { return false; }
        void await_suspend(std::coroutine_handle<> h)
        {
            std::jthread& out = *p_out;
            if (out.joinable())
                throw std::runtime_error("Output jthread parameter not empty");
            out = std::jthread([h] { h.resume(); });
            // Potential undefined behavior: accessing potentially destroyed *this
            // std::cout << "New thread ID: " << p_out->get_id() << '\n';
            std::cout << "New thread ID: " << out.get_id() << '\n'; // this is OK
        }
        void await_resume() {}
    };
    return awaitable{&out};
}
 
struct task
{
    struct promise_type
    {
        task get_return_object() { return {}; }
        std::suspend_never initial_suspend() { return {}; }
        std::suspend_never final_suspend() noexcept { return {}; }
        void return_void() {}
        void unhandled_exception() {}
    };
};
 
task resuming_on_new_thread(std::jthread& out)
{
    std::cout << "Coroutine started on thread: " << std::this_thread::get_id() << '\n';
    co_await switch_to_new_thread(out);
    // awaiter destroyed here
    std::cout << "Coroutine resumed on thread: " << std::this_thread::get_id() << '\n';
}
 
int main()
{
    std::jthread out;
    resuming_on_new_thread(out);
}

```

Possible output:

```
Coroutine started on thread: 139972277602112
New thread ID: 139972267284224
Coroutine resumed on thread: 139972267284224

```

Note: the awaiter object is part of coroutine state (as a temporary whose lifetime crosses a suspension point) and is destroyed before the co_await expression finishes. It can be used to maintain per-operation state as required by some async I/O APIs without resorting to additional dynamic allocations.

The standard library defines two trivial awaitables: std::suspend_always and std::suspend_never.

|  |  |
| --- | --- |
|  | This section is incomplete Reason: examples |

| Demo of promise_type::await_transform and a program provided awaiter |
| --- |
| ExampleRun this code  ```text #include <cassert> #include <coroutine> #include <iostream>   struct tunable_coro {     // An awaiter whose "readiness" is determined via constructor's parameter.     class tunable_awaiter     {         bool ready_;     public:         explicit(false) tunable_awaiter(bool ready) : ready_{ready} {}         // Three standard awaiter interface functions:         bool await_ready() const noexcept { return ready_; }         static void await_suspend(std::coroutine_handle<>) noexcept {}         static void await_resume() noexcept {}     };       struct promise_type     {         using coro_handle = std::coroutine_handle<promise_type>;         auto get_return_object() { return coro_handle::from_promise(*this); }         static auto initial_suspend() { return std::suspend_always(); }         static auto final_suspend() noexcept { return std::suspend_always(); }         static void return_void() {}         static void unhandled_exception() { std::terminate(); }         // A user provided transforming function which returns the custom awaiter:         auto await_transform(std::suspend_always) { return tunable_awaiter(!ready_); }         void disable_suspension() { ready_ = false; }     private:         bool ready_{true};     };       tunable_coro(promise_type::coro_handle h) : handle_(h) { assert(h); }       // For simplicity, declare these 4 special functions as deleted:     tunable_coro(tunable_coro const&) = delete;     tunable_coro(tunable_coro&&) = delete;     tunable_coro& operator=(tunable_coro const&) = delete;     tunable_coro& operator=(tunable_coro&&) = delete;       ~tunable_coro()     {         if (handle_)             handle_.destroy();     }       void disable_suspension() const     {         if (handle_.done())             return;         handle_.promise().disable_suspension();         handle_();     }       bool operator()()     {         if (!handle_.done())             handle_();         return !handle_.done();     } private:     promise_type::coro_handle handle_; };   tunable_coro generate(int n) {     for (int i{}; i != n; ++i)     {         std::cout << i << ' ';         // The awaiter passed to co_await goes to promise_type::await_transform which         // issues tunable_awaiter that initially causes suspension (returning back to         // main at each iteration), but after a call to disable_suspension no suspension         // happens and the loop runs to its end without returning to main().         co_await std::suspend_always{};     } }   int main() {     auto coro = generate(8);     coro(); // emits only one first element == 0     for (int k{}; k < 4; ++k)     {         coro(); // emits 1 2 3 4, one per each iteration         std::cout << ": ";     }     coro.disable_suspension();     coro(); // emits the tail numbers 5 6 7 all at ones } ```   Output:   ```text 0 1 : 2 : 3 : 4 : 5 6 7 ``` |

### co_yield

`co_yield` expression returns a value to the caller and suspends the current coroutine: it is the common building block of resumable generator functions.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `co_yield` expr |  |  |
|  | | | | | | | | | |
| `co_yield` braced-init-list |  |  |
|  | | | | | | | | | |

It is equivalent to

```
co_await promise.yield_value(expr)

```

A typical generator's `yield_value` would store (copy/move or just store the address of, since the argument's lifetime crosses the suspension point inside the `co_await`) its argument into the generator object and return std::suspend_always, transferring control to the caller/resumer.

Run this code

```
#include <coroutine>
#include <cstdint>
#include <exception>
#include <iostream>
 
template<typename T>
struct Generator
{
    // The class name 'Generator' is our choice and it is not required for coroutine
    // magic. Compiler recognizes coroutine by the presence of 'co_yield' keyword.
    // You can use name 'MyGenerator' (or any other name) instead as long as you include
    // nested struct promise_type with 'MyGenerator get_return_object()' method.
    // (Note: It is necessary to adjust the declarations of constructors and destructors
    //  when renaming.)
 
    struct promise_type;
    using handle_type = std::coroutine_handle<promise_type>;
 
    struct promise_type // required
    {
        T value_;
        std::exception_ptr exception_;
 
        Generator get_return_object()
        {
            return Generator(handle_type::from_promise(*this));
        }
        std::suspend_always initial_suspend() { return {}; }
        std::suspend_always final_suspend() noexcept { return {}; }
        void unhandled_exception() { exception_ = std::current_exception(); } // saving
                                                                              // exception
 
        template<std::convertible_to<T> From> // C++20 concept
        std::suspend_always yield_value(From&& from)
        {
            value_ = std::forward<From>(from); // caching the result in promise
            return {};
        }
        void return_void() {}
    };
 
    handle_type h_;
 
    Generator(handle_type h) : h_(h) {}
    ~Generator() { h_.destroy(); }
    explicit operator bool()
    {
        fill(); // The only way to reliably find out whether or not we finished coroutine,
                // whether or not there is going to be a next value generated (co_yield)
                // in coroutine via C++ getter (operator () below) is to execute/resume
                // coroutine until the next co_yield point (or let it fall off end).
                // Then we store/cache result in promise to allow getter (operator() below
                // to grab it without executing coroutine).
        return !h_.done();
    }
    T operator()()
    {
        fill();
        full_ = false; // we are going to move out previously cached
                       // result to make promise empty again
        return std::move(h_.promise().value_);
    }
 
private:
    bool full_ = false;
 
    void fill()
    {
        if (!full_)
        {
            h_();
            if (h_.promise().exception_)
                std::rethrow_exception(h_.promise().exception_);
            // propagate coroutine exception in called context
 
            full_ = true;
        }
    }
};
 
Generator<std::uint64_t>
fibonacci_sequence(unsigned n)
{
    if (n == 0)
        co_return;
 
    if (n > 94)
        throw std::runtime_error("Too big Fibonacci sequence. Elements would overflow.");
 
    co_yield 0;
 
    if (n == 1)
        co_return;
 
    co_yield 1;
 
    if (n == 2)
        co_return;
 
    std::uint64_t a = 0;
    std::uint64_t b = 1;
 
    for (unsigned i = 2; i < n; ++i)
    {
        std::uint64_t s = a + b;
        co_yield s;
        a = b;
        b = s;
    }
}
 
int main()
{
    try
    {
        auto gen = fibonacci_sequence(10); // max 94 before uint64_t overflows
 
        for (int j = 0; gen; ++j)
            std::cout << "fib(" << j << ")=" << gen() << '\n';
    }
    catch (const std::exception& ex)
    {
        std::cerr << "Exception: " << ex.what() << '\n';
    }
    catch (...)
    {
        std::cerr << "Unknown exception.\n";
    }
}

```

Output:

```
fib(0)=0
fib(1)=1
fib(2)=1
fib(3)=2
fib(4)=3
fib(5)=5
fib(6)=8
fib(7)=13
fib(8)=21
fib(9)=34

```

### Notes

| Feature-test macro | Value | Std | Feature |
| --- | --- | --- | --- |
| `__cpp_impl_coroutine` | `201902L` | (C++20) | Coroutines (compiler support) |
| `__cpp_lib_coroutine` | `201902L` | (C++20) | Coroutines (library support) |
| `__cpp_lib_generator` | `202207L` | (C++23) | std::generator: synchronous coroutine generator for ranges |

### Keywords

co_await,
co_return,
co_yield

### Library support

Coroutine support library defines several types providing compile and run-time support for coroutines.

### Defect reports

The following behavior-changing defect reports were applied retroactively to previously published C++ standards.

| DR | Applied to | Behavior as published | Correct behavior |
| --- | --- | --- | --- |
| CWG 2556 | C++20 | invalid `return_void` made the behavior of falling off the end of the coroutine undefined | the program is ill- formed in this case |
| CWG 2668 | C++20 | co_await could not appear in lambda expressions | allowed |
| CWG 2754 | C++23 | \*this was taken when constructing the promise object for explicit object member functions | \*this is not taken in this case |

### See also

|  |  |
| --- | --- |
| generator(C++23) | A `view` that represents synchronous ****coroutine**** generator   (class template) |

### External links

|  |  |
| --- | --- |
| 1. | Lewis Baker, 2017-2022 - Asymmetric Transfer. |
| 2. | David Mazières, 2021 - Tutorial on C++20 coroutines. |
| 3. | Chuanqi Xu & Yu Qi & Yao Han, 2021 - C++20 Principles and Applications of Coroutine. (Chinese) |
| 4. | Simon Tatham, 2023 - Writing custom C++20 coroutine systems. |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/coroutines&oldid=178595>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 20 December 2024, at 14:05.