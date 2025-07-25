# Atomic operations library

From cppreference.com
< c
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

 ****Atomic operations library****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types | | | | |
| memory_order | | | | |
| atomic_flag | | | | |
| Macros | | | | |
| ATOMIC_\*\*\*_LOCK_FREE | | | | |
| ATOMIC_FLAG_INIT | | | | |
| ATOMIC_VAR_INIT | | | | |
| kill_dependency | | | | |
| Functions | | | | |
| atomic_flag_test_and_set | | | | |
| atomic_flag_clear | | | | |
| atomic_init | | | | |
| atomic_is_lock_free | | | | |
| atomic_store | | | | |
| atomic_load | | | | |
| atomic_exchange | | | | |
| atomic_compare_exchange | | | | |
| atomic_fetch_add | | | | |
| atomic_fetch_sub | | | | |
| atomic_fetch_or | | | | |
| atomic_fetch_xor | | | | |
| atomic_fetch_and | | | | |
| atomic_thread_fence | | | | |
| atomic_signal_fence | | | | |

If the macro constant `__STDC_NO_ATOMICS__`(C11) is defined by the compiler, the header `<stdatomic.h>`, the keyword _Atomic, and all of the names listed here are not provided.

### Types

|  |  |
| --- | --- |
| Defined in header `<stdatomic.h>` | |
| memory_order(C11) | defines memory ordering constraints   (enum) |
| atomic_flag(C11) | lock-free atomic boolean flag  (struct) |

### Macros

|  |  |
| --- | --- |
| Defined in header `<stdatomic.h>` | |
| ATOMIC_BOOL_LOCK_FREEATOMIC_CHAR_LOCK_FREEATOMIC_CHAR16_T_LOCK_FREEATOMIC_CHAR32_T_LOCK_FREEATOMIC_WCHAR_T_LOCK_FREEATOMIC_SHORT_LOCK_FREEATOMIC_INT_LOCK_FREEATOMIC_LONG_LOCK_FREEATOMIC_LLONG_LOCK_FREEATOMIC_POINTER_LOCK_FREE(C11) | indicates that the given atomic type is lock-free   (macro constant) |
| ATOMIC_FLAG_INIT(C11) | initializes a new atomic_flag   (macro constant) |
| ATOMIC_VAR_INIT(C11)(deprecated in C17)(removed in C23) | initializes a new atomic object   (function macro) |
| kill_dependency(C11) | breaks a dependency chain for memory_order_consume   (function macro) |

### Functions

|  |  |
| --- | --- |
| Defined in header `<stdatomic.h>` | |
| atomic_flag_test_and_setatomic_flag_test_and_set_explicit(C11) | sets an atomic_flag to true and returns the old value   (function) |
| atomic_flag_clearatomic_flag_clear_explicit(C11) | sets an atomic_flag to false   (function) |
| atomic_init(C11) | initializes an existing atomic object   (function) |
| atomic_is_lock_free(C11) | indicates whether the atomic object is lock-free   (function) |
| atomic_storeatomic_store_explicit(C11) | stores a value in an atomic object   (function) |
| atomic_loadatomic_load_explicit(C11) | reads a value from an atomic object   (function) |
| atomic_exchangeatomic_exchange_explicit(C11) | swaps a value with the value of an atomic object   (function) |
| atomic_compare_exchange_strongatomic_compare_exchange_strong_explicitatomic_compare_exchange_weakatomic_compare_exchange_weak_explicit(C11) | swaps a value with an atomic object if the old value is what is expected, otherwise reads the old value   (function) |
| atomic_fetch_addatomic_fetch_add_explicit(C11) | atomic addition   (function) |
| atomic_fetch_subatomic_fetch_sub_explicit(C11) | atomic subtraction   (function) |
| atomic_fetch_oratomic_fetch_or_explicit(C11) | atomic bitwise OR   (function) |
| atomic_fetch_xoratomic_fetch_xor_explicit(C11) | atomic bitwise exclusive OR   (function) |
| atomic_fetch_andatomic_fetch_and_explicit(C11) | atomic bitwise AND   (function) |
| atomic_thread_fence(C11) | generic memory order-dependent fence synchronization primitive   (function) |
| atomic_signal_fence(C11) | fence between a thread and a signal handler executed in the same thread   (function) |

### Types

The standard library offers convenience typedefs for the core language atomic types.

|  |  |
| --- | --- |
| Typedef name | Full type name |
| `atomic_bool` | _Atomic _Bool |
| `atomic_char` | _Atomic char |
| `atomic_schar` | _Atomic signed char |
| `atomic_uchar` | _Atomic unsigned char |
| `atomic_short` | _Atomic short |
| `atomic_ushort` | _Atomic unsigned short |
| `atomic_int` | _Atomic int |
| `atomic_uint` | _Atomic unsigned int |
| `atomic_long` | _Atomic long |
| `atomic_ulong` | _Atomic unsigned long |
| `atomic_llong` | _Atomic long long |
| `atomic_ullong` | _Atomic unsigned long long |
| `atomic_char8_t` (C23) | _Atomic char8_t |
| `atomic_char16_t` | _Atomic char16_t |
| `atomic_char32_t` | _Atomic char32_t |
| `atomic_wchar_t` | _Atomic wchar_t |
| `atomic_int_least8_t` | _Atomic int_least8_t |
| `atomic_uint_least8_t` | _Atomic uint_least8_t |
| `atomic_int_least16_t` | _Atomic int_least16_t |
| `atomic_uint_least16_t` | _Atomic uint_least16_t |
| `atomic_int_least32_t` | _Atomic int_least32_t |
| `atomic_uint_least32_t` | _Atomic uint_least32_t |
| `atomic_int_least64_t` | _Atomic int_least64_t |
| `atomic_uint_least64_t` | _Atomic uint_least64_t |
| `atomic_int_fast8_t` | _Atomic int_fast8_t |
| `atomic_uint_fast8_t` | _Atomic uint_fast8_t |
| `atomic_int_fast16_t` | _Atomic int_fast16_t |
| `atomic_uint_fast16_t` | _Atomic uint_fast16_t |
| `atomic_int_fast32_t` | _Atomic int_fast32_t |
| `atomic_uint_fast32_t` | _Atomic uint_fast32_t |
| `atomic_int_fast64_t` | _Atomic int_fast64_t |
| `atomic_uint_fast64_t` | _Atomic uint_fast64_t |
| `atomic_intptr_t` | _Atomic intptr_t |
| `atomic_uintptr_t` | _Atomic uintptr_t |
| `atomic_size_t` | _Atomic size_t |
| `atomic_ptrdiff_t` | _Atomic ptrdiff_t |
| `atomic_intmax_t` | _Atomic intmax_t |
| `atomic_uintmax_t` | _Atomic uintmax_t |

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.17 Atomics <stdatomic.h> (p: TBD)

:   - 7.31.8 Atomics <stdatomic.h> (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.17 Atomics <stdatomic.h> (p: TBD)

:   - 7.31.8 Atomics <stdatomic.h> (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.17 Atomics <stdatomic.h> (p: 273-286)

:   - 7.31.8 Atomics <stdatomic.h> (p: 455-456)

### See also

|  |  |
| --- | --- |
| C++ documentation for Atomic operations library | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/atomic&oldid=156654>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 14 August 2023, at 02:08.