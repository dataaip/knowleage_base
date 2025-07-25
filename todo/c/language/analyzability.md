# Analyzability

From cppreference.com
< c‎ | language
 C

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Language | | | | |
| Headers | | | | |
| Type support | | | | |
| Program utilities | | | | |
| Variadic function support | | | | |
| Error handling | | | | |
| Dynamic memory management | | | | |
| Strings library | | | | |
| Algorithms | | | | |
| Numerics | | | | |
| Date and time utilities | | | | |
| Input/output support | | | | |
| Localization support | | | | |
| Concurrency support (C11) | | | | |
| Technical Specifications | | | | |
| Symbol index | | | | |

 C language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Basic concepts | | | | |
| Keywords | | | | |
| Preprocessor | | | | |
| Statements | | | | |
| Expressions | | | | |
| Initialization | | | | |
| Declarations | | | | |
| Functions | | | | |
| Miscellaneous | | | | |
| History of C | | | | |
| Technical Specifications | | | | |

This optional extension to the C language limits the potential results of executing some forms of undefined behavior, which improves the effectiveness of static analysis of such programs. Analyzability is only guaranteed to be enabled if the predefined macro constant __STDC_ANALYZABLE__(C11) is defined by the compiler.

If the compiler supports analyzability, any language or library construct whose behavior is undefined is further classified between **critical** and **bounded** undefined behavior, and the behavior of all bounded UB cases is limited as specified below.

### Critical undefined behavior

Critical UB is undefined behavior that might perform a memory write or a volatile memory read out of bounds of any object. A program that has critical undefined behavior may be susceptible to security exploits.

Only the following undefined behaviors are critical:

- access to an object outside of its lifetime (e.g. through a dangling pointer)
- write to an object whose declarations are not compatible
- function call through a function pointer whose type is not compatible with the type of the function it points to
- lvalue expression is evaluated, but does not designate an object
- attempted modification of a string literal
- dereferencing an invalid (null, indeterminate, etc) or past-the-end pointer
- modification of a const object through a non-const pointer
- call to a standard library function or macro with an invalid argument
- call to a variadic standard library function with unexpected argument type (e.g. call to printf with an argument of the type that doesn't match its conversion specifier)
- longjmp where there is no setjmp up the calling scope, across threads, or from within the scope of a VM type.
- any use of the pointer that was deallocated by free or realloc
- any string or wide string library function accesses an array out of bounds

### Bounded undefined behavior

Bounded UB is undefined behavior that cannot perform an illegal memory write, although it may trap and may produce or store indeterminate values.

- All undefined behavior not listed as critical is bounded, including

:   - multithreaded data races
    - use of a indeterminate values with automatic storage duration
    - strict aliasing violations
    - misaligned object access
    - signed integer overflow
    - unsequenced side-effects modify the same scalar or modify and read the same scalar
    - floating-to-integer or pointer-to-integer conversion overflow
    - bitwise shift by a negative or too large bit count
    - integer division by zero
    - use of a void expression
    - direct assignment or memcpy of inexactly-overlapped objects
    - restrict violations
    - etc.. ALL undefined behavior that's not in the critical list.

### Notes

Bounded undefined behavior disables certain optimizations: compilation with analyzability enabled preserves source-code causality, which may be violated by undefined behavior otherwise.

Analyzability extension permits, as a form of implementation-defined behavior, for the runtime constraint handler to be invoked when a trap occurs.

### References

- C11 standard (ISO/IEC 9899:2011):

:   - 6.10.8.3/1 Conditional feature macros (p: 177)

:   - Annex L Analyzability (p: 652-653)

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/analyzability&oldid=76226>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 February 2015, at 06:09.