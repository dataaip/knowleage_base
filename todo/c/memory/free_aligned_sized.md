# free_aligned_sized

From cppreference.com
< c‎ | memory
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

 Dynamic memory management

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| malloc | | | | |
| calloc | | | | |
| realloc | | | | |
| free | | | | |
| free_sized(C23) | | | | |
| ****free_aligned_sized****(C23) | | | | |
| aligned_alloc(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdlib.h>` |  |  |
| void free_aligned_sized( void\* ptr, size_t alignment, size_t size ); |  | (since C23) |
|  |  |  |

If ptr is a null pointer or the result obtained from a call to aligned_alloc, where alignment is equal to the requested allocation alignment and size is equal to the requested allocation size, this function is equivalent to free(ptr). Otherwise, the behavior is undefined.

The result of an malloc, calloc, or realloc call may not be passed to `free_aligned_sized`.

`free_aligned_sized` is thread-safe: it behaves as though only accessing the memory locations visible through its argument, and not any static storage.

A call to `free_aligned_sized` that deallocates a region of memory **synchronizes-with** a call to any subsequent allocation function that allocates the same or a part of the same region of memory. This synchronization occurs after any access to the memory by the deallocating function and before any access to the memory by the allocation function. There is a single total order of all allocation and deallocation functions operating on each particular region of memory.

### Parameters

|  |  |  |
| --- | --- | --- |
| ptr | - | pointer to the memory to deallocate |
| alignment | - | alignment of memory to deallocate |
| size | - | size of memory to deallocate |

### Return value

(none)

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: no example |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.24.3.5 The free_sized function (p: 366)

### See also

|  |  |
| --- | --- |
| aligned_alloc(C11) | allocates aligned memory   (function) |
| free | deallocates previously allocated memory   (function) |
| free_sized(C23) | deallocates previously allocated sized memory   (function) |
| malloc | allocates memory   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/memory/free_aligned_sized&oldid=175230>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 August 2024, at 19:54.