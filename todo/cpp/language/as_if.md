# The as-if rule

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

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ASCII | | | | |
| Punctuation | | | | |
| Names and identifiers | | | | |
| Types | | | | |
| Fundamental types | | | | |
| Objects | | | | |
| Scope | | | | |
| Object lifetime | | | | |
| Storage duration and linkage | | | | |
| Definitions and ODR | | | | |
| Name lookup | | | | |
| Qualified name lookup | | | | |
| Unqualified name lookup | | | | |
| ****The as-if rule**** | | | | |
| Undefined behavior | | | | |
| Memory model | | | | |
| Multi-threaded executions and data races (C++11) | | | | |
| Character sets and encodings | | | | |
| Phases of translation | | | | |
| The `main` function | | | | |
| Modules (C++20) | | | | |

Allows any and all code transformations that do not change the observable behavior of the program.

### Explanation

The C++ compiler is permitted to perform any changes to the program as long as the following remains true:

|  |  |
| --- | --- |
| 1) At every sequence point, the values of all volatile objects are stable (previous evaluations are complete, new evaluations not started). | (until C++11) |
| 1) Accesses (reads and writes) to volatile objects occur strictly according to the semantics of the expressions in which they occur. In particular, they are not reordered with respect to other volatile accesses on the same thread. | (since C++11) |

2) At program termination, data written to files is exactly as if the program was executed as written.3) Prompting text which is sent to interactive devices will be shown before the program waits for input.4) If the ISO C pragma #pragma STDC FENV_ACCESS is supported and is set to `ON`, the changes to the floating-point environment (floating-point exceptions and rounding modes) are guaranteed to be observed by the floating-point arithmetic operators and function calls as if executed as written, except that

:   - the result of any floating-point expression other than cast and assignment may have range and precision of a floating-point type different from the type of the expression (see FLT_EVAL_METHOD),
    - notwithstanding the above, intermediate results of any floating-point expression may be calculated as if to infinite range and precision (unless #pragma STDC FP_CONTRACT is `OFF`).

### Notes

Because the compiler is (usually) unable to analyze the code of an external library to determine whether it does or does not perform I/O or volatile access, third-party library calls also aren't affected by optimization. However, standard library calls may be replaced by other calls, eliminated, or added to the program during optimization. Statically-linked third-party library code may be subject to link-time optimization.

Programs with undefined behavior, e.g. due to access to an array out of bounds, modification of a const object, evaluation order violations, etc, are free from the as-if rule: they often change observable behavior when recompiled with different optimization settings. For example, if a test for signed integer overflow relies on the result of that overflow, e.g. if (n + 1 < n) abort();, it is removed entirely by some compilers because signed overflow is undefined behavior and the optimizer is free to assume it never happens and the test is redundant.

Copy elision is an exception from the as-if rule: the compiler may remove calls to move- and copy-constructors and the matching calls to the destructors of temporary objects even if those calls have observable side effects.

|  |  |
| --- | --- |
| New-expression has another exception from the as-if rule: the compiler may remove calls to the replaceable allocation functions even if a user-defined replacement is provided and has observable side-effects. | (since C++14) |

The count and order of floating-point exceptions can be changed by optimization as long as the state as observed by the next floating-point operation is as if no optimization took place:

```
#pragma STDC FENV_ACCESS ON
for (i = 0; i < n; ++i)
    x + 1; // x + 1 is dead code, but may raise FP exceptions
           // (unless the optimizer can prove otherwise). However, executing it n times
           // will raise the same exception over and over. So this can be optimized to:
if (0 < n)
    x + 1;

```

### Example

Run this code

```
int& preinc(int& n) { return ++n; }
int add(int n, int m) { return n + m; }
 
// volatile input to prevent constant folding
volatile int input = 7;
 
// volatile output to make the result a visible side-effect
volatile int result;
 
int main()
{
    int n = input;
// using built-in operators would invoke undefined behavior
//  int m = ++n + ++n;
// but using functions makes sure the code executes as-if 
// the functions were not overlapped
    int m = add(preinc(n), preinc(n));
    result = m;
}

```

Output:

```
# full code of the main() function as produced by the GCC compiler
# x86 (Intel) platform:
        movl    input(%rip), %eax   # eax = input
        leal    3(%rax,%rax), %eax  # eax = 3 + eax + eax
        movl    %eax, result(%rip)  # result = eax
        xorl    %eax, %eax          # eax = 0 (the return value of main())
        ret
 
# PowerPC (IBM) platform:
        lwz 9,LC..1(2)
        li 3,0          # r3 = 0 (the return value of main())
        lwz 11,0(9)     # r11 = input;
        slwi 11,11,1    # r11 = r11 << 1;
        addi 0,11,3     # r0 = r11 + 3;
        stw 0,4(9)      # result = r0;
        blr
 
# Sparc (Sun) platform:
        sethi   %hi(result), %g2
        sethi   %hi(input), %g1
        mov     0, %o0                 # o0 = 0 (the return value of main)
        ld      [%g1+%lo(input)], %g1  # g1 = input
        add     %g1, %g1, %g1          # g1 = g1 + g1
        add     %g1, 3, %g1            # g1 = 3 + g1
        st      %g1, [%g2+%lo(result)] # result = g1
        jmp     %o7+8
        nop
 
# in all cases, the side effects of preinc() were eliminated, and the
# entire main() function was reduced to the equivalent of result = 2 * input + 3;

```

### See also

- copy elision

|  |  |
| --- | --- |
| C documentation for as-if rule | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/as_if&oldid=154651>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 July 2023, at 09:41.