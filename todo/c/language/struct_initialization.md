# Struct and union initialization

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

 Initialization

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Explicit initialization | | | | |
| Implicit initialization | | | | |
| Empty initialization | | | | |
| Scalar initialization | | | | |
| Array initialization | | | | |
| ****Struct and union initialization**** | | | | |

When initializing an object of struct or union type, the initializer must be a non-empty,(until C23) brace-enclosed, comma-separated list of initializers for the members:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `=` `{` expression `,` `...` `}` | (1) | (until C99) |
|  | | | | | | | | | |
| `=` `{` designator(optional) expression `,` `...` `}` | (2) | (since C99) |
|  | | | | | | | | | |
| `=` `{` `}` | (3) | (since C23) |
|  | | | | | | | | | |

where the designator is a sequence (whitespace-separated or adjacent) of individual member designators of the form `.` member and array designators of the form `[` index `]`.

All members that are not initialized explicitly are empty-initialized.

### Explanation

When initializing a union, the initializer list must have only one member, which initializes the first member of the union unless a designated initializer is used(since C99).

```
union { int x; char c[4]; }
  u = {1},           // makes u.x active with value 1
 u2 = { .c={'\1'} }; // makes u2.c active with value {'\1','\0','\0','\0'}

```

When initializing a struct, the first initializer in the list initializes the first declared member (unless a designator is specified)(since C99), and all subsequent initializers without designators (since C99)initialize the struct members declared after the one initialized by the previous expression.

```
struct point {double x,y,z;} p = {1.2, 1.3}; // p.x=1.2, p.y=1.3, p.z=0.0
div_t answer = {.quot = 2, .rem = -1 };      // order of elements in div_t may vary

```

|  |  |
| --- | --- |
| A designator causes the following initializer to initialize the struct member described by the designator. Initialization then continues forward in order of declaration, beginning with the next element declared after the one described by the designator.   ```text struct {int sec,min,hour,day,mon,year;} z    = {.day=31,12,2014,.sec=30,15,17}; // initializes z to {30,15,17,31,12,2014} ``` | (since C99) |

It's an error to provide more initializers than members.

### Nested initialization

If the members of the struct or union are arrays, structs, or unions, the corresponding initializers in the brace-enclosed list of initializers are any initializers that are valid for those members, except that their braces may be omitted as follows:

If the nested initializer begins with an opening brace, the entire nested initializer up to its closing brace initializes the corresponding member object. Each left opening brace establishes a new **current object**. The members of the current object are initialized in their natural order, unless designators are used(since C99): array elements in subscript order, struct members in declaration order, only the first declared member of any union. The subobjects within the current object that are not explicitly initialized by the closing brace are empty-initialized.

```
struct example {
    struct addr_t {
       uint32_t port;
    } addr;
    union {
       uint8_t a8[4];
       uint16_t a16[2];
    } in_u;
};
struct example ex = { // start of initializer list for struct example
                     { // start of initializer list for ex.addr
                        80 // initialized struct's only member
                     }, // end of initializer list for ex.addr
                     { // start of initializer-list for ex.in_u
                        {127,0,0,1} // initializes first element of the union
                     } };

```

If the nested initializer does not begin with an opening brace, only enough initializers from the list are taken to account for the elements or members of the member array, struct or union; any remaining initializers are left to initialize the next struct member:

```
struct example ex = {80, 127, 0, 0, 1}; // 80 initializes ex.addr.port
                                        // 127 initializes ex.in_u.a8[0]
                                        // 0 initializes ex.in_u.a8[1]
                                        // 0 initializes ex.in_u.a8[2]
                                        // 1 initializes ex.in_u.a8[3]

```

|  |  |
| --- | --- |
| When designators are nested, the designators for the members follow the designators for the enclosing structs/unions/arrays. Within any nested bracketed initializer list, the outermost designator refers to the **current object** and selects the subobject to be initialized within the **current object** only.   ```text struct example ex2 = { // current object is ex2, designators are for members of example                        .in_u.a8[0]=127, 0, 0, 1, .addr=80};  struct example ex3 = {80, .in_u={ // changes current object to the union ex.in_u                            127,                            .a8[2]=1 // this designator refers to the member of in_u                       } }; ```   If any subobject is explicitly initialized twice (which may happen when designators are used), the initializer that appears later in the list is the one used (the earlier initializer may not be evaluated):   ```text struct {int n;} s = {printf("a\n"), // this may be printed or skipped                      .n=printf("b\n")}; // always printed ```   Although any non-initialized subobjects are initialized implicitly, implicit initialization of a subobject never overrides explicit initialization of the same subobject if it appeared earlier in the initializer list (choose clang to observe the correct output): Run this code  ```text #include <stdio.h> typedef struct { int k; int l; int a[2]; } T; typedef struct { int i;  T t; } S; T x = {.l = 43, .k = 42, .a[1] = 19, .a[0] = 18 };  // x initialized to {42, 43, {18, 19} } int main(void) {     S l = { 1,          // initializes l.i to 1            .t = x,      // initializes l.t to {42, 43, {18, 19} }            .t.l = 41,   // changes l.t to {42, 41, {18, 19} }            .t.a[1] = 17 // changes l.t to {42, 41, {18, 17} }           };     printf("l.t.k is %d\n", l.t.k); // .t = x sets l.t.k to 42 explicitly                                     // .t.l = 41 would zero out l.t.k implicitly } ```   Output:   ```text l.t.k is 42 ```   However, when an initializer begins with a left open brace, its **current object** is fully re-initialized and any prior explicit initializers for any of its subobjects are ignored:   ```text struct fred { char s[4]; int n; }; struct fred x[ ] = { { { "abc" }, 1 }, // inits x[0] to { {'a','b','c','\0'}, 1 }                       [0].s[0] = 'q'   // changes x[0] to { {'q','b','c','\0'}, 1 }                    }; struct fred y[ ] = { { { "abc" }, 1 }, // inits y[0] to { {'a','b','c','\0'}, 1 }                      [0] = { // current object is now the entire y[0] object                              .s[0] = 'q'                              } // replaces y[0] with { {'q','\0','\0','\0'}, 0 }                     }; ``` | (since C99) |

### Notes

The initializer list may have a trailing comma, which is ignored.

```
struct {double x,y;} p = {1.0,
                          2.0, // trailing comma OK
                          };

```

|  |  |
| --- | --- |
| In C, the braced list of initializers cannot be empty (note that C++ allows empty lists, and also note that a struct in C cannot be empty): | (until C23) |
| The initializer list can be empty in C as in C++: | (since C23) |

```
struct {int n;} s = {0}; // OK
struct {int n;} s = {}; // Error until C23: initializer-list cannot be empty
                        // OK since C23: s.n is initialized to 0
struct {} s = {}; // Error: struct cannot be empty

```

|  |  |
| --- | --- |
| Every expression in the initializer list must be a constant expression when initializing aggregates of any storage duration. | (until C99) |
| As with all other initialization, every expression in the initializer list must be a constant expression when initializing aggregates of static or thread-local(since C11) storage duration:   ```text static struct {char* p} s = {malloc(1)}; // error ```   The order of evaluation of the subexpressions in any initializer is indeterminately sequenced (but not in C++ since C++11):   ```text int n = 1; struct {int x,y;} p = {n++, n++}; // unspecified, but well-defined behavior:                                   // n is incremented twice in arbitrary order                                   // p equal {1,2} and {2,1} are both valid ``` | (since C99) |

### Example

|  |  |
| --- | --- |
|  | This section is incomplete Reason: more practical examples, perhaps initialize some socket structs |

Run this code

```
#include <stdio.h>
#include <time.h>
 
int main(void)
{
    char buff[70];
    // designated initializers simplify the use of structs whose
    // order of members is unspecified
    struct tm my_time = { .tm_year=2012-1900, .tm_mon=9, .tm_mday=9,
                          .tm_hour=8, .tm_min=10, .tm_sec=20 };
    strftime(buff, sizeof buff, "%A %c", &my_time);
    puts(buff);
}

```

Possible output:

```
Sunday Sun Oct  9 08:10:20 2012

```

### References

- C17 standard (ISO/IEC 9899:2018):

:   - 6.7.9/12-39 Initialization (p: 101-105)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.7.9/12-38 Initialization (p: 140-144)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.7.8/12-38 Initialization (p: 126-130)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 6.5.7 Initialization

### See also

|  |  |
| --- | --- |
| C++ documentation for Aggregate initialization | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/struct_initialization&oldid=146997>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 26 January 2023, at 04:21.