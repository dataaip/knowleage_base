# Transactional memory (TM TS)

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

 Statements

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Labels | | | | |
| label : statement | | | | |
| Expression statements | | | | |
| expression ; | | | | |
| Compound statements | | | | |
| `{` statement... `}` | | | | |
| Selection statements | | | | |
| if | | | | |
| switch | | | | |
| Iteration statements | | | | |
| while | | | | |
| do while | | | | |
| for | | | | |
| range for (C++11) | | | | |
| Jump statements | | | | |
| break | | | | |
| continue | | | | |
| return | | | | |
| goto | | | | |
| Declaration statements | | | | |
| declaration ; | | | | |
| Try blocks | | | | |
| try block | | | | |
| ****Transactional memory**** | | | | |
| `synchronized`, `atomic_commit`, etc (TM TS) | | | | |

Transactional memory is a concurrency synchronization mechanism that combines groups of statements in transactions, that are

- atomic (either all statements occur, or nothing occurs)
- isolated (statements in a transaction may not observe half-written writes made by another transaction, even if they execute in parallel)

Typical implementations use hardware transactional memory where supported and to the limits that it is available (e.g. until the changeset is saturated) and fall back to software transactional memory, usually implemented with optimistic concurrency: if another transaction updated some of the variables used by a transaction, it is silently retried. For that reason, retriable transactions ("atomic blocks") can only call transaction-safe functions.

Note that accessing a variable in a transaction and out of a transaction without other external synchronization is a data race.

If feature testing is supported, the features described here are indicated by the macro constant __cpp_transactional_memory with a value equal or greater 201505.

### Synchronized blocks

`synchronized` compound-statement

Executes the compound statement as if under a global lock: all outermost synchronized blocks in the program execute in a single total order. The end of each synchronized block synchronizes with the beginning of the next synchronized block in that order. Synchronized blocks that are nested within other synchronized blocks have no special semantics.

Synchronized blocks are not transactions (unlike the atomic blocks below) and may call transaction-unsafe functions.

Run this code

```
#include <iostream>
#include <thread>
#include <vector>
 
int f()
{
    static int i = 0;
    synchronized { // begin synchronized block
        std::cout << i << " -> ";
        ++i;       // each call to f() obtains a unique value of i
        std::cout << i << '\n';
        return i;  // end synchronized block
    }
}
 
int main()
{
    std::vector<std::thread> v(10);
    for (auto& t : v)
        t = std::thread([] { for (int n = 0; n < 10; ++n) f(); });
    for (auto& t : v)
        t.join();
}

```

Output:

```
0 -> 1
1 -> 2
2 -> 3
...
99 -> 100

```

Leaving a synchronized block by any means (reaching the end, executing goto, break, continue, or return, or throwing an exception) exits the block and synchronizes-with the next block in the single total order if the exited block was an outer block. The behavior is undefined if std::longjmp is used to exit a synchronized block.

Entering a synchronized block by goto or switch is not allowed.

Although synchronized blocks execute as-if under a global lock, the implementations are expected to examine the code within each block and use optimistic concurrency (backed up by hardware transactional memory where available) for transaction-safe code and minimal locking for non-transaction safe code. When a synchronized block makes a call to a non-inlined function, the compiler may have to drop out of speculative execution and hold a lock around the entire call unless the function is declared `transaction_safe` (see below) or the attribute `[[optimize_for_synchronized]]` (see below) is used.

### Atomic blocks

|  |  |
| --- | --- |
|  | This section is incomplete |

`atomic_noexcept` compound-statement

`atomic_cancel` compound-statement

`atomic_commit` compound-statement

1) If an exception is thrown, std::abort is called.2) If an exception is thrown, std::abort is called, unless the exception is one of the exceptions used for transaction cancellation (see below) in which case the transaction is **cancelled**: the values of all memory locations in the program that were modified by side effects of the operations of the atomic block are restored to the values they had at the time the start of the atomic block was executed, and the exception continues stack unwinding as usual.3) If an exception is thrown, the transaction is committed normally.

The exceptions used for transaction cancellation in `atomic_cancel` blocks are std::bad_alloc, std::bad_array_new_length, std::bad_cast, std::bad_typeid, std::bad_exception, std::exception and all standard library exceptions derived from it, and the special exception type std::tx_exception<T>.

The compound-statement in an atomic block is not allowed to execute any expression or statement or call any function that isn't `transaction_safe` (this is a compile time error).

```
// each call to f() retrieves a unique value of i, even when done in parallel
int f()
{
    static int i = 0;
    atomic_noexcept { // begin transaction
//  printf("before %d\n", i); // error: cannot call a non transaction-safe function
        ++i;
        return i; // commit transaction
    }
}

```

Leaving an atomic block by any means other than exception (reaching the end, goto, break, continue, return) commits the transaction. The behavior is undefined if std::longjmp is used to exit an atomic block.

### Transaction-safe functions

|  |  |
| --- | --- |
|  | This section is incomplete |

A function can be explicitly declared to be transaction-safe by using the keyword transaction_safe in its declaration.

|  |  |
| --- | --- |
|  | This section is incomplete |

In a lambda declaration, it appears either immediately after the capture list, or immediately after the (keyword `mutable` (if one is used).

|  |  |
| --- | --- |
|  | This section is incomplete |

```
extern volatile int * p = 0;
struct S
{
    virtual ~S();
};
int f() transaction_safe
{
    int x = 0;  // ok: not volatile
    p = &x;     // ok: the pointer is not volatile
    int i = *p; // error: read through volatile glvalue
    S s;        // error: invocation of unsafe destructor
}

```

```
int f(int x) { // implicitly transaction-safe
    if (x <= 0)
        return 0;
    return x + f(x - 1);
}

```

If a function that is not transaction-safe is called through a reference or pointer to a transaction-safe function, the behavior is undefined.

Pointers to transaction-safe functions and pointers to transaction-safe member functions are implicitly convertible to pointers to functions and pointers to member functions respectively. It is unspecified if the resulting pointer compares equal to the original.

#### Transaction-safe virtual functions

|  |  |
| --- | --- |
|  | This section is incomplete |

If the final overrider of a `transaction_safe_dynamic` function is not declared `transaction_safe`, calling it in an atomic block is undefined behavior.

### Standard library

Besides introducing the new exception template std::tx_exception, the transactional memory technical specification makes the following changes to the standard library:

- makes the following functions explicitly `transaction_safe`:

:   - std::forward, std::move, std::move_if_noexcept, std::align, std::abort, global default operator new, global default operator delete, std::allocator::construct if the invoked constructor is transaction-safe, std::allocator::destroy if the invoked destructor is transaction-safe, std::get_temporary_buffer, std::return_temporary_buffer, std::addressof, std::pointer_traits::pointer_to, each non-virtual member function of all exception types that support transaction cancellation (see `atomic_cancel` above)

      |  |  |
      | --- | --- |
      |  | This section is incomplete Reason: there's more |

- makes the following functions explicitly `transaction_safe_dynamic`

:   - each virtual member function of all exception types that support transaction cancellation (see `atomic_cancel` above)

- requires that all operations that are transaction-safe on an Allocator X are transaction-safe on `X::rebind<>::other`

### Attributes

The attribute `[[optimize_for_synchronized]]` may be applied to a declarator in a function declaration and must appear on the first declaration of the function.

If a function is declared `[[optimize_for_synchronized]]` in one translation unit and the same function is declared without `[[optimize_for_synchronized]]` in another translation unit, the program is ill-formed; no diagnostic required.

It indicates that a the function definition should be optimized for invocation from a synchronized statement. In particular, it avoids serializing synchronized blocks that make a call to a function that is transaction-safe for the majority of calls, but not for all calls (e.g. hash table insertion that may have to rehash, allocator that may have to request a new block, a simple function that may rarely log).

```
std::atomic<bool> rehash{false};
 
// maintenance thread runs this loop
void maintenance_thread(void*)
{
    while (!shutdown)
    {
        synchronized
        {
            if (rehash)
            {
                hash.rehash();
                rehash = false;
            }
        }
    }
}
 
// worker threads execute hundreds of thousands of calls to this function 
// every second. Calls to insert_key() from synchronized blocks in other
// translation units will cause those blocks to serialize, unless insert_key()
// is marked [[optimize_for_synchronized]]
[[optimize_for_synchronized]] void insert_key(char* key, char* value)
{
    bool concern = hash.insert(key, value);
    if (concern)
        rehash = true;
}

```

GCC assembly without the attribute: the entire function is serialized

```
insert_key(char*, char*):
	subq	$8, %rsp
	movq	%rsi, %rdx
	movq	%rdi, %rsi
	movl	$hash, %edi
	call	Hash::insert(char*, char*)
	testb	%al, %al
	je	.L20
	movb	$1, rehash(%rip)
	mfence
.L20:
	addq	$8, %rsp
	ret


```

GCC assembly with the attribute:

```
transaction clone for insert_key(char*, char*):
	subq	$8, %rsp
	movq	%rsi, %rdx
	movq	%rdi, %rsi
	movl	$hash, %edi
	call	transaction clone for Hash::insert(char*, char*)
	testb	%al, %al
	je	.L27
	xorl	%edi, %edi
	call	_ITM_changeTransactionMode # Note: this is the serialization point
	movb	$1, rehash(%rip)
	mfence
.L27:
	addq	$8, %rsp
	ret


```

|  |  |
| --- | --- |
|  | This section is incomplete Reason: check assembly with trunk, also show caller-side changes |

### Notes

|  |  |
| --- | --- |
|  | This section is incomplete Reason: experience notes from Wyatt paper/talk |

### Keywords

atomic_cancel,
atomic_commit,
atomic_noexcept,
synchronized,
transaction_safe,
transaction_safe_dynamic

### Compiler support

This technical specification is supported by GCC as of version 6.1 (requires -fgnu-tm to enable). An older variant of this specification was supported in GCC as of 4.7.

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/transactional_memory&oldid=174915>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 13 August 2024, at 20:32.