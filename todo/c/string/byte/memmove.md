# memmove, memmove_s

From cppreference.com
< c‎ | string‎ | byte
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

 Strings library

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Null-terminated byte strings | | | | |
| Null-terminated multibyte strings | | | | |
| Null-terminated wide strings | | | | |

 Null-terminated byte strings

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Functions | | | | |
| Character manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | isalnum | | | | | | isalpha | | | | | | islower | | | | | | isupper | | | | | | isdigit | | | | | | isxdigit | | | | | | isblank(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | iscntrl | | | | | | isgraph | | | | | | isspace | | | | | | isprint | | | | | | ispunct | | | | | | tolower | | | | | | toupper | | | | | |
| Conversions to and from numeric formats | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | atoiatolatoll(C99) | | | | | | atof | | | | | | strtolstrtoll(C99) | | | | | | strtoulstrtoull(C99) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strtoimaxstrtoumax(C99)(C99) | | | | | | strtofstrtodstrtold(C99)(C99) | | | | | | strfromfstrfromdstrfroml(C23)(C23)(C23) | | | | | |
| String manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strcpystrcpy_s(C11) | | | | | | strncpystrncpy_s(C11) | | | | | | strcatstrcat_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strncatstrncat_s(C11) | | | | | | strxfrm | | | | | | strdup(C23) | | | | | | strndup(C23) | | | | | |  | | | | | |
| String examination | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | strlenstrnlen_s(C11) | | | | | | strcmp | | | | | | strncmp | | | | | | strcoll | | | | | | strchr | | | | | | strrchr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | strspn | | | | | | strcspn | | | | | | strpbrk | | | | | | strstr | | | | | | strtokstrtok_s(C11) | | | | | |  | | | | | |
| Memory manipulation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | memchr | | | | | | memcmp | | | | | | memsetmemset_explicitmemset_s(C23)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | memcpymemcpy_s(C11) | | | | | | ****memmovememmove_s****(C11) | | | | | | memccpy(C23) | | | | | |
| Miscellaneous | | | | |
| strerrorstrerror_sstrerrorlen_s(C11)(C11) | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<string.h>` |  |  |
| void\* memmove( void\* dest, const void\* src, size_t count ); | (1) |  |
| errno_t memmove_s(void\* dest, rsize_t destsz, const void\* src, rsize_t count); | (2) | (since C11) |
|  |  |  |

1) Copies count characters from the object pointed to by src to the object pointed to by dest. Both objects are interpreted as arrays of unsigned char. The objects may overlap: copying takes place as if the characters were copied to a temporary character array and then the characters were copied from the array to dest. The behavior is undefined if access occurs beyond the end of the dest array. The behavior is undefined if either dest or src is an invalid or null pointer.2) Same as (1), except when detecting the following errors at runtime, it zeroes out the entire destination range dest, dest + destsz) (if both dest and destsz are valid) and calls the currently installed [constraint handler function:

:   - dest or src is a null pointer
    - destsz or count is greater than RSIZE_MAX
    - count is greater than destsz (buffer overflow would occur)

 The behavior is undefined if the size of the character array pointed to by dest < count <= destsz; in other words, an erroneous value of destsz does not expose the impending buffer overflow.

:   As with all bounds-checked functions, `memmove_s` is only guaranteed to be available if __STDC_LIB_EXT1__ is defined by the implementation and if the user defines __STDC_WANT_LIB_EXT1__ to the integer constant 1 before including <string.h>.

### Parameters

|  |  |  |
| --- | --- | --- |
| dest | - | pointer to the object to copy to |
| destsz | - | max number of bytes to modify in the destination (typically the size of the destination object) |
| src | - | pointer to the object to copy from |
| count | - | number of bytes to copy |

### Return value

1) Returns a copy of dest2) Returns zero on success and non-zero value on error. Also on error, if dest is not a null pointer and destsz is valid, writes destsz zero bytes in to the destination array.

### Notes

`memmove` may be used to set the effective type of an object obtained by an allocation function.

Despite being specified "as if" a temporary buffer is used, actual implementations of this function do not incur the overhead or double copying or extra memory. A common approach (glibc and bsd libc) is to copy bytes forwards from the beginning of the buffer if the destination starts before the source, and backwards from the end otherwise, with a fall back to the more efficient memcpy when there is no overlap at all.

Where strict aliasing prohibits examining the same memory as values of two different types, `memmove` may be used to convert the values.

### Example

Run this code

```
#define __STDC_WANT_LIB_EXT1__ 1
#include <inttypes.h>
#include <stdint.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
 
int main(void)
{
    char str[] = "1234567890";
    puts(str);
    memmove(str + 4, str + 3, 3); // copy from [4,5,6] to [5,6,7]
    puts(str);
 
    // setting effective type of allocated memory to be int
    int* p = malloc(3 * sizeof(int)); // allocated memory has no effective type
    int arr[3] = {1, 2, 3};
    memmove(p, arr, 3 * sizeof(int)); // allocated memory now has an effective type
 
    // reinterpreting data
    double d = 0.1;
    // int64_t n = *(int64_t*)(&d); // strict aliasing violation
    int64_t n;
    memmove(&n, &d, sizeof d); // OK
    printf("%a is %" PRIx64 " as an int64_t\n", d, n);
 
#ifdef __STDC_LIB_EXT1__
    set_constraint_handler_s(ignore_handler_s);
    char src[] = "aaaaaaaaaa";
    char dst[] = "xyxyxyxyxy";
    int r = memmove_s(dst, sizeof dst, src, 5);
    printf("dst = \"%s\", r = %d\n", dst, r);
    r = memmove_s(dst, 5, src, 10); // count is greater than destsz
    printf("dst = \"");
    for (size_t ndx = 0; ndx < sizeof dst; ++ndx)
    {
        char c = dst[ndx];
        c ? printf("%c", c) : printf("\\0");
    }
    printf("\", r = %d\n", r);
#endif
}

```

Possible output:

```
1234567890
1234456890
0x1.999999999999ap-4 is 3fb999999999999a as an int64_t
dst = "aaaaayxyxy", r = 0
dst = "\0\0\0\0\0yxyxy", r = 22

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.24.2.2 The memmove function (p: TBD)

:   - K.3.7.1.2 The memmove_s function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.24.2.2 The memmove function (p: 264)

:   - K.3.7.1.2 The memmove_s function (p: 446)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.24.2.2 The memmove function (p: 363)

:   - K.3.7.1.2 The memmove_s function (p: 615)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.21.2.2 The memmove function (p: 326)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.11.2.2 The memmove function

### See also

|  |  |
| --- | --- |
| memcpymemcpy_s(C11) | copies one buffer to another   (function) |
| wmemmovewmemmove_s(C95)(C11) | copies a certain amount of wide characters between two, possibly overlapping, arrays   (function) |
| C++ documentation for memmove | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/string/byte/memmove&oldid=178699>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 December 2024, at 20:29.