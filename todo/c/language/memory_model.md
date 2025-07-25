# Memory model

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
| The as-if rule | | | | |
| Undefined behavior | | | | |
| ****Memory model and data races**** | | | | |

Defines the semantics of computer memory storage for the purpose of the C abstract machine.

The data storage (memory) available to a C program is one or more contiguous sequences of **bytes**. Each byte in memory has a unique **address**.

### Byte

A **byte** is the smallest addressable unit of memory. It is defined as a contiguous sequence of bits, large enough to hold any member of the **basic execution character set** (the 96 characters that are required to be single-byte). C supports bytes of sizes 8 bits and greater.

The types char, unsigned char, and signed char use one byte for both storage and value representation. The number of bits in a byte is accessible as CHAR_BIT.

For use of bytes to representation values of other fundamental types (including big-endian and little-endian memory layouts), see object representation

### Memory location

A **memory location** is

- an object of scalar type (arithmetic type, pointer type, enumeration type)
- or the largest contiguous sequence of bit-fields of non-zero length

```
struct S
{
    char a;     // memory location #1
    int b : 5;  // memory location #2
    int c : 11, // memory location #2 (continued)
          : 0,
        d : 8;  // memory location #3
    struct
    {
        int ee : 8; // memory location #4
    } e;
} obj; // The object 'obj' consists of 4 separate memory locations

```

|  |  |  |  |
| --- | --- | --- | --- |
| Threads and data races A thread of execution is a flow of control within a program that begins with the invocation of a top-level function by thrd_create or other means.  Any thread can potentially access any object in the program (objects with automatic and thread-local storage duration may still be accessed by another thread through a pointer).  Different threads of execution are always allowed to access (read and modify) different **memory locations** concurrently, with no interference and no synchronization requirements. (note that it is not safe to concurrently update two non-atomic bit-fields in the same structure if all members declared between them are also (non-zero-length) bit-fields, no matter what the sizes of those intervening bit-fields happen to be)  When an evaluation of an expression writes to a memory location and another evaluation reads or modifies the same memory location, the expressions are said to **conflict**. A program that has two conflicting evaluations has a **data race** unless either   - both conflicting evaluations are atomic operations - one of the conflicting evaluations **happens-before** another (see memory_order)   If a data race occurs, the behavior of the program is undefined. (in particular, mtx_unlock is **synchronized-with**, and therefore, **happens-before** mtx_lock of the same mutex by another thread, which makes it possible to use mutex locks to guard against data races)  |  |  | | --- | --- | |  | This section is incomplete Reason: small example or two |  Memory order When a thread reads a value from a memory location, it may see the initial value, the value written in the same thread, or the value written in another thread. See memory_order for details on the order in which writes made from threads become visible to other threads. | (since C11) |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 3.6 byte (p: TBD)

:   - 3.14 memory location (p: TBD)

:   - 5.1.2.4 Multi-threaded executions and data races (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 3.6 byte (p: TBD)

:   - 3.14 memory location (p: TBD)

:   - 5.1.2.4 Multi-threaded executions and data races (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 3.6 byte (p: 4)

:   - 3.14 memory location (p: 5)

:   - 5.1.2.4 Multi-threaded executions and data races (p: 17-21)

- C99 standard (ISO/IEC 9899:1999):

:   - 3.6 byte (p: 4)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 1.6 DEFINITIONS OF TERMS

### See also

|  |  |
| --- | --- |
| C++ documentation for Memory model | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/memory_model&oldid=175727>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 September 2024, at 13:39.