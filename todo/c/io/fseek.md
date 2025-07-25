# fseek

From cppreference.com
< c‎ | io
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

 File input/output

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Types and objects | | | | |
| |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | stdinstdoutstderr | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | FILE | | | | | | fpos_t | | | | | |  | | | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopenfopen_s(C11) | | | | | | freopenfreopen_s(C11) | | | | | | fwide(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbuf | | | | | | setvbuf | | | | | | fclose | | | | | | fflush | | | | | |  | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetc | | | | | | fgets | | | | | | fputc | | | | | | fputs | | | | | | getchar | | | | | | getsgets_s(until C11)(C11) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc(C95)(C95) | | | | | | fgetws(C95) | | | | | | fputwcputwc(C95)(C95) | | | | | | fputws(C95) | | | | | | getwchar(C95) | | | | | | putwchar(C95) | | | | | | ungetwc(C95) | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanfscanf_sfscanf_ssscanf_s(C11)(C11)(C11) | | | | | | wscanffwscanfswscanfwscanf_sfwscanf_sswscanf_s(C95)(C95)(C95)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vscanfvfscanfvsscanfvscanf_svfscanf_svsscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | vwscanfvfwscanfvswscanfvwscanf_svfwscanf_svswscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | printffprintfsprintfsnprintfprintf_sfprintf_ssprintf_ssnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | wprintffwprintfswprintfwprintf_sfwprintf_sswprintf_ssnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vprintfvfprintfvsprintfvsnprintfvprintf_svfprintf_svsprintf_svsnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | vwprintfvfwprintfvswprintfvwprintf_svfwprintf_svswprintf_svsnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | | File positioning | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ftell | | | | | | fgetpos | | | | | | ****fseek**** | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fsetpos | | | | | | rewind | | | | | |  | | | | | | | Error handling | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clearerr | | | | | | feof | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ferror | | | | | | perror | | | | | | | Operations on files | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove | | | | | | tmpfiletmpfile_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rename | | | | | | tmpnamtmpnam_s(C11) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdio.h>` |  |  |
| int fseek( FILE\* stream, long offset, int origin ); |  |  |
| #define SEEK_SET    /\* unspecified \*/  #define SEEK_CUR    /\* unspecified \*/ #define SEEK_END    /\* unspecified \*/ |  |  |
|  |  |  |

Sets the file position indicator for the file stream stream to the value pointed to by offset.

If the stream is open in binary mode, the new position is exactly offset bytes measured from the beginning of the file if origin is SEEK_SET, from the current file position if origin is SEEK_CUR, and from the end of the file if origin is SEEK_END. Binary streams are not required to support SEEK_END, in particular if additional null bytes are output.

If the stream is open in text mode, the only supported values for offset are zero (which works with any origin) and a value returned by an earlier call to ftell on a stream associated with the same file (which only works with origin of SEEK_SET).

If the stream is wide-oriented, the restrictions of both text and binary streams apply (result of ftell is allowed with SEEK_SET and zero offset is allowed from SEEK_SET and SEEK_CUR, but not SEEK_END).

In addition to changing the file position indicator, `fseek` undoes the effects of ungetc and clears the end-of-file status, if applicable.

If a read or write error occurs, the error indicator for the stream (ferror) is set and the file position is unaffected.

### Parameters

|  |  |  |
| --- | --- | --- |
| stream | - | file stream to modify |
| offset | - | number of characters to shift the position relative to origin |
| origin | - | position to which offset is added. It can have one of the following values: SEEK_SET, SEEK_CUR, SEEK_END |

### Return value

​0​ upon success, nonzero value otherwise.

### Notes

After seeking to a non-end position in a wide stream, the next call to any output function may render the remainder of the file undefined, e.g. by outputting a multibyte sequence of a different length.

For text streams, the only valid values of offset are ​0​ (applicable to any origin) and a value returned by an earlier call to ftell (only applicable to SEEK_SET).

POSIX allows seeking beyond the existing end of file. If an output is performed after this seek, any read from the gap will return zero bytes. Where supported by the filesystem, this creates a **sparse file**.

POSIX also requires that `fseek` first performs fflush if there are any unwritten data (but whether the shift state is restored is implementation-defined).

POSIX specifies, that `fseek` should return -1 on error, and set errno to indicate the error.

On Windows, `_fseeki64` can be used to work with files larger than 2 GiB.

### Example

`fseek` with error checking:

Run this code

```
#include <stdio.h>
#include <stdlib.h>
 
int main(void)
{
    // Prepare an array of double values.
    #define SIZE 5
    double A[SIZE] = {1.0, 2.0, 3.0, 4.0, 5.0};
 
    // Write array to a file.
    FILE * fp = fopen("test.bin", "wb");
    fwrite(A, sizeof(double), SIZE, fp);
    fclose (fp);
 
    // Read the double values into array B.
    double B[SIZE];
    fp = fopen("test.bin", "rb");
 
    // Set the file position indicator in front of third double value.
    if (fseek(fp, sizeof(double) * 2L, SEEK_SET) != 0)
    {
        fprintf(stderr, "fseek() failed in file %s at line # %d\n",
                __FILE__, __LINE__ - 2);
        fclose(fp);
        return EXIT_FAILURE;
    }
 
    int ret_code = fread(B, sizeof(double), 1, fp); // reads one double value
    printf("ret_code == %d\n", ret_code);           // prints the number of values read
    printf("B[0] == %.1f\n", B[0]);                 // prints one value
 
    fclose(fp);
    return EXIT_SUCCESS;
}

```

Possible output:

```
ret_code == 1
B[0] == 3.0

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.23.9.2 The fseek function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.21.9.2 The fseek function (p: 245)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.21.9.2 The fseek function (p: 336-337)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.19.9.2 The fseek function (p: 302-303)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.9.9.2 The fseek function

### See also

|  |  |
| --- | --- |
| fsetpos | moves the file position indicator to a specific location in a file   (function) |
| fgetpos | gets the file position indicator   (function) |
| ftell | returns the current file position indicator   (function) |
| rewind | moves the file position indicator to the beginning in a file   (function) |
| C++ documentation for fseek | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/io/fseek&oldid=178171>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 5 December 2024, at 08:13.