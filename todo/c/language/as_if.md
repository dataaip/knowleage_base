# As-if rule

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

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ASCII | | | | |
| Character sets | | | | |
| Translation phases | | | | |
| Punctuation | | | | |
| Identifier | | | | |
| Scope | | | | |
| Lifetime | | | | |
| Lookup and name spaces | | | | |
| Type | | | | |
| Arithmetic types | | | | |
| Objects and alignment | | | | |
| The main() function | | | | |
| ****The as-if rule**** | | | | |
| Undefined behavior | | | | |
| Memory model and data races | | | | |

Allows any and all code transformations that do not change the observable behavior of the program.

### Explanation

The C compiler is permitted to perform any changes to the program as long as the following remains true:

|  |  |
| --- | --- |
| 1) At every sequence point, the values of all volatile objects are stable (previous evaluations are complete, new evaluations not started). | (until C11) |
| 1) Accesses (reads and writes) to volatile objects occur strictly according to the semantics of the expressions in which they occur. In particular, they are not reordered with respect to other volatile accesses on the same thread. | (since C11) |

2) At program termination, data written to files is exactly as if the program was executed as written.3) Prompting text which is sent to interactive devices will be shown before the program waits for input.

|  |  |
| --- | --- |
| 4) If the pragma #pragma STDC FENV_ACCESS is supported and is set to `ON`, the changes to the floating-point environment (floating-point exceptions and rounding modes) are guaranteed to be observed by the floating-point arithmetic operators and function calls as if executed as written, except that - the result of any floating-point expression other than cast and assignment may have range and precision of a floating-point type different from the type of the expression (see FLT_EVAL_METHOD), - notwithstanding the above, intermediate results of any floating-point expression may be calculated as if to infinite range and precision (unless #pragma STDC FP_CONTRACT is `OFF`). | (since C99) |

### Notes

|  |  |
| --- | --- |
|  | This section is incomplete Reason: fill out similar to cpp/language/as_if |

### See also

- Order of evaluation

|  |  |
| --- | --- |
| C++ documentation for as-if rule | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/as_if&oldid=154654>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 9 July 2023, at 10:46.