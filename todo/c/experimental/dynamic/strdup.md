# strdup

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
| ****strdup**** | | | | |
| strndup | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string.h>` |  |  |
| char \* strdup( const char \*str1 ); |  | (dynamic memory TR) |
|  |  |  |

Returns a pointer to a null-terminated byte string, which is a duplicate
of the string pointed to by `str1`. The returned pointer must be passed to free to avoid a memory leak.

If an error occurs, a null pointer is returned and errno may be set.

As all functions from Dynamic Memory TR, `strdup` is only guaranteed to be available if __STDC_ALLOC_LIB__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT2__ to the integer constant 1 before including `string.h`.

### Parameters

|  |  |  |
| --- | --- | --- |
| str1 | - | pointer to the null-terminated byte string to duplicate |

### Return value

A pointer to the newly allocated string, or a null pointer if an error occurred.

### Notes

The function is identical to the POSIX strdup.

### Example

Run this code

```
#ifdef __STDC_ALLOC_LIB__
#define __STDC_WANT_LIB_EXT2__ 1
#else
#define _POSIX_C_SOURCE 200809L
#endif
 
#include <string.h>
#include <assert.h>
#include <stdlib.h>
 
int main(void)
{
    const char *s1 = "String";
    char *s2 = strdup(s1);
    assert(strcmp(s1, s2) == 0);
    free(s2);
}

```

### See also

|  |  |
| --- | --- |
| strndup(dynamic memory TR) | allocate a copy of a string up to specified size   (function) |
| strcpystrcpy_s(C11) | copies one string to another   (function) |
| malloc | allocates memory   (function) |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/experimental/dynamic/strdup&oldid=123996>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 12 November 2020, at 11:47.