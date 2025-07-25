# fsetpos

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
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Functions | | | | | | File access | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fopenfopen_s(C11) | | | | | | freopenfreopen_s(C11) | | | | | | fwide(C95) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | setbuf | | | | | | setvbuf | | | | | | fclose | | | | | | fflush | | | | | |  | | | | | | | Unformatted input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetc | | | | | | fgets | | | | | | fputc | | | | | | fputs | | | | | | getchar | | | | | | getsgets_s(until C11)(C11) | | | | | | putchar | | | | | | puts | | | | | | ungetc | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fgetwcgetwc(C95)(C95) | | | | | | fgetws(C95) | | | | | | fputwcputwc(C95)(C95) | | | | | | fputws(C95) | | | | | | getwchar(C95) | | | | | | putwchar(C95) | | | | | | ungetwc(C95) | | | | | |  | | | | | | | Formatted input | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | scanffscanfsscanfscanf_sfscanf_ssscanf_s(C11)(C11)(C11) | | | | | | wscanffwscanfswscanfwscanf_sfwscanf_sswscanf_s(C95)(C95)(C95)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vscanfvfscanfvsscanfvscanf_svfscanf_svsscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | vwscanfvfwscanfvswscanfvwscanf_svfwscanf_svswscanf_s(C99)(C99)(C99)(C11)(C11)(C11) | | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Direct input/output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fread | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | fwrite | | | | | | | Formatted output | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | printffprintfsprintfsnprintfprintf_sfprintf_ssprintf_ssnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | wprintffwprintfswprintfwprintf_sfwprintf_sswprintf_ssnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | vprintfvfprintfvsprintfvsnprintfvprintf_svfprintf_svsprintf_svsnprintf_s(C99)(C11)(C11)(C11)(C11) | | | | | | vwprintfvfwprintfvswprintfvwprintf_svfwprintf_svswprintf_svsnwprintf_s(C95)(C95)(C95)(C11)(C11)(C11)(C11) | | | | | | | File positioning | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ftell | | | | | | fgetpos | | | | | | fseek | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ****fsetpos**** | | | | | | rewind | | | | | |  | | | | | | | Error handling | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | clearerr | | | | | | feof | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | ferror | | | | | | perror | | | | | | | Operations on files | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | remove | | | | | | tmpfiletmpfile_s(C11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | rename | | | | | | tmpnamtmpnam_s(C11) | | | | | | |

|  |  |  |
| --- | --- | --- |
| Defined in header `<stdio.h>` |  |  |
| int fsetpos( FILE\* stream, const fpos_t\* pos ); |  |  |
|  |  |  |

Sets the file position indicator and the multibyte parsing state (if any) for the file stream stream according to the value pointed to by pos.

Besides establishing new parse state and position, a call to this function undoes the effects of ungetc and clears the end-of-file state, if it is set.

If a read or write error occurs, the error indicator (ferror) for the stream is set.

### Parameters

|  |  |  |
| --- | --- | --- |
| stream | - | file stream to modify |
| pos | - | pointer to a fpos_t object to use as new value of file position indicator |

### Return value

​0​ upon success, nonzero value otherwise.

### Notes

After seeking to a non-end position in a wide stream, the next call to any output function may render the remainder of the file undefined, e.g. by outputting a multibyte sequence of a different length.

### Example

`fsetpos` with error checking

Run this code

```
#include <stdio.h>
#include <stdlib.h>
 
int main(void)
{
    // Prepare an array of FP (floating-point) values.
    #define SIZE 5
    double A[SIZE] = {1.0, 2.0, 3.0, 4.0, 5.0};
    // Write array to a file.
    FILE * fp = fopen("test.bin", "wb");
    fwrite(A,sizeof(double),SIZE,fp);
    fclose (fp);
 
    // Read the FP values into array B.
    double B[SIZE];
    fp = fopen("test.bin","rb");
    fpos_t pos;
    if (fgetpos(fp, &pos)) // current position: start of file
    {
        perror("fgetpos()");
        fprintf(stderr, "fgetpos() failed in file %s at line # %d\n",
                __FILE__, __LINE__ - 3);
        exit(EXIT_FAILURE);
    }
 
    int ret_code = fread(B,sizeof(double),1,fp); // read one FP value
    // current position: after reading one f-p value
    printf("%.1f; read count = %d\n", B[0], ret_code); // print one FP value and ret_code
 
    if (fsetpos(fp, &pos)) // reset current position to start of file
    {
        if (ferror(fp))
        {
            perror("fsetpos()");
            fprintf(stderr, "fsetpos() failed in file %s at line # %d\n", __FILE__,
                    __LINE__ - 5);
            exit(EXIT_FAILURE);
        }
    }
 
    ret_code = fread(B, sizeof(double), 1, fp); // reread first FP value
    printf("%.1f; read count = %d\n", B[0], ret_code); // print one FP value and ret_code
    fclose(fp);
 
    return EXIT_SUCCESS;
}

```

Possible output:

```
1.0; read count = 1
1.0; read count = 1

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 7.21.9.3 The fsetpos function (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 7.21.9.3 The fsetpos function (p: TBD)

- C11 standard (ISO/IEC 9899:2011):

:   - 7.21.9.3 The fsetpos function (p: 337)

- C99 standard (ISO/IEC 9899:1999):

:   - 7.19.9.3 The fsetpos function (p: 303)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 4.9.9.3 The fsetpos function

### See also

|  |  |
| --- | --- |
| fgetpos | gets the file position indicator   (function) |
| ftell | returns the current file position indicator   (function) |
| fseek | moves the file position indicator to a specific location in a file   (function) |
| C++ documentation for fsetpos | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/io/fsetpos&oldid=178687>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 21 December 2024, at 15:22.