# strndup

From cppreference.com
< c‎ | experimental‎ | dynamic
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

 Technical Specifications

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Extensions for embedded processors") | | | | |
| Dynamic memory extensions | | | | |
| Floating-point extensions part 1: Binary floating-point | | | | |
| Floating-point extensions part 4: Supplementary functions | | | | |

 Dynamic memory extensions

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| fmemopen") | | | | |
| open_memstreamopen_wmemstream") | | | | |
| asprintfaswprintfvasprintfvaswprintf | | | | |
| getlinegetwlinegetdelimgetwdelim | | | | |
| strdup | | | | |
| ****strndup**** | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string.h>` |  |  |
| char \*strndup( const char \*str, size_t size ); |  | (dynamic memory TR) |
|  |  |  |

Returns a pointer to a null-terminated byte string, which contains copies of at most `size` bytes from the string pointed to by `str`. If the null terminator is not encountered in the first `size` bytes, it is added to the duplicated string.

The returned pointer must be passed to free to avoid a memory leak.

If an error occurs, a null pointer is returned and errno may be set.

As all functions from Dynamic Memory TR, `strndup` is only guaranteed to be available if __STDC_ALLOC_LIB__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT2__ to the integer constant 1 before including `string.h`.

### Parameters

|  |  |  |
| --- | --- | --- |
| str | - | pointer to the null-terminated byte string to duplicate |
| size | - | max number of bytes to copy from `str` |

### Return value

A pointer to the newly allocated string, or a null pointer if an error occurred.

### Notes

The function is identical to the POSIX strndup except that it is allowed, but not required to set errno on error.

### Example

Run this code

```
#ifdef __STDC_ALLOC_LIB__
#define __STDC_WANT_LIB_EXT2__ 1
#else
#define _POSIX_C_SOURCE 200809L
#endif
 
#include <string.h>
#include <stdio.h>
#include <stdlib.h>
 
int main(void)
{
    const char *s1 = "String";
    char *s2 = strndup(s1, 2);
    printf("strndup(\"String\", 2) == %s\n", s2);
    free(s2);
}

```

Output:

```
strndup("String", 2) == St

```

### See also

|  |  |
| --- | --- |
| strdup(dynamic memory TR) | allocate a copy of a string   (function) |
| strncpystrncpy_s(C11) | copies a certain amount of characters from one string to another   (function) |
| malloc | allocates memory   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/experimental/dynamic/strndup&oldid=123997>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 November 2020, at 11:49.