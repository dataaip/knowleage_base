# Static storage duration

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

An object whose identifier is declared without the storage-class specifier _Thread_local, and either with external or internal linkage or with the storage-class specifier static, has static storage duration. Its lifetime is the entire execution of the program and its stored value is initialized only once, prior to program startup.

### Notes

Since its stored value is initialized only once, an object with static storage duration can profile the invocations of a function.

The other use of the keyword static is file scope.

### Example

Run this code

```
#include <stdio.h>
 
void f (void)
{
    static int count = 0;   // static variable   
    int i = 0;              // automatic variable
    printf("%d %d\n", i++, count++);
}
 
int main(void)
{
    for (int ndx=0; ndx<10; ++ndx)
        f();
}

```

Output:

```
0 0
0 1
0 2
0 3
0 4
0 5
0 6
0 7
0 8
0 9

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/static_storage_duration&oldid=109385>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 19 February 2019, at 09:12.