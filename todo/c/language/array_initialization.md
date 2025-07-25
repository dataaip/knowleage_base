# Array initialization

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
| ****Array initialization**** | | | | |
| Struct and union initialization | | | | |

When initializing an object of array type, the initializer must be either a string literal (optionally enclosed in braces) or be a brace-enclosed list of initialized for array members:

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `=` string-literal | (1) |  |
|  | | | | | | | | | |
| `=` `{` expression `,` `...` `}` | (2) | (until C99) |
|  | | | | | | | | | |
| `=` `{` designator(optional) expression `,` `...` `}` | (2) | (since C99) |
|  | | | | | | | | | |
| `=` `{` `}` | (3) | (since C23) |
|  | | | | | | | | | |

1) string literal initializer for character and wide character arrays2) comma-separated list of constant(until C99) expressions that are initializers for array elements, optionally using array designators of the form `[` constant-expression `]` `=` (since C99)3) empty initializer empty-initializes every element of the array

Arrays of known size and arrays of unknown size may be initialized, but not VLAs(since C99)(until C23). A VLA can only be empty-initialized.(since C23)

All array elements that are not initialized explicitly are empty-initialized.

### Initialization from strings

String literal (optionally enclosed in braces) may be used as the initializer for an array of matching type:

- ordinary string literals and UTF-8 string literals(since C11) can initialize arrays of any character type (char, signed char, unsigned char)
- L-prefixed wide string literals can be used to initialize arrays of any type compatible with (ignoring cv-qualifications) wchar_t

|  |  |
| --- | --- |
| - u-prefixed wide string literals can be used to initialize arrays of any type compatible with (ignoring cv-qualifications) char16_t - U-prefixed wide string literals can be used to initialize arrays of any type compatible with (ignoring cv-qualifications) char32_t | (since C11) |

Successive bytes of the string literal or wide characters of the wide string literal, including the terminating null byte/character, initialize the elements of the array:

```
char str[] = "abc"; // str has type char[4] and holds 'a', 'b', 'c', '\0'
wchar_t wstr[4] = L"猫"; // str has type wchar_t[4] and holds L'猫', '\0', '\0', '\0'

```

If the size of the array is known, it may be one less than the size of the string literal, in which case the terminating null character is ignored:

```
char str[3] = "abc"; // str has type char[3] and holds 'a', 'b', 'c'

```

Note that the contents of such array are modifiable, unlike when accessing a string literal directly with char\* str = "abc";.

### Initialization from brace-enclosed lists

When an array is initialized with a brace-enclosed list of initializers, the first initializer in the list initializes the array element at index zero (unless a designator is specified)(since C99), and each subsequent initializer without a designator (since C99)initializes the array element at index one greater than the one initialized by the previous initializer.

```
int x[] = {1,2,3}; // x has type int[3] and holds 1,2,3
int y[5] = {1,2,3}; // y has type int[5] and holds 1,2,3,0,0
int z[4] = {1}; // z has type int[4] and holds 1,0,0,0
int w[3] = {0}; // w has type int[3] and holds all zeroes

```

It's an error to provide more initializers than elements when initializing an array of known size (except when initializing character arrays from string literals).

|  |  |
| --- | --- |
| A designator causes the following initializer to initialize of the array element described by the designator. Initialization then continues forward in order, beginning with the next element after the one described by the designator.   ```text int n[5] = {[4]=5,[0]=1,2,3,4}; // holds 1,2,3,4,5   int a[MAX] = { // starts initializing a[0] = 1, a[1] = 3, ...     1, 3, 5, 7, 9, [MAX-5] = 8, 6, 4, 2, 0 }; // for MAX=6,  array holds 1,8,6,4,2,0 // for MAX=13, array holds 1,3,5,7,9,0,0,0,8,6,4,2,0 ("sparse array") ``` | (since C99) |

When initializing an array of unknown size, the largest subscript for which an initializer is specified determines the size of the array being declared.

### Nested arrays

If the elements of an array are arrays, structs, or unions, the corresponding initializers in the brace-enclosed list of initializers are any initializers that are valid for those members, except that their braces may be omitted as follows:

If the nested initializer begins with an opening brace, the entire nested initializer up to its closing brace initializes the corresponding array element:

```
int y[4][3] = { // array of 4 arrays of 3 ints each (4x3 matrix)
    { 1 },      // row 0 initialized to {1, 0, 0}
    { 0, 1 },   // row 1 initialized to {0, 1, 0}
    { [2]=1 },  // row 2 initialized to {0, 0, 1}
};              // row 3 initialized to {0, 0, 0}

```

If the nested initializer does not begin with an opening brace, only enough initializers from the list are taken to account for the elements or members of the sub-array, struct or union; any remaining initializers are left to initialize the next array element:

```
int y[4][3] = {    // array of 4 arrays of 3 ints each (4x3 matrix)
1, 3, 5, 2, 4, 6, 3, 5, 7 // row 0 initialized to {1, 3, 5}
};                        // row 1 initialized to {2, 4, 6}
                          // row 2 initialized to {3, 5, 7}
                          // row 3 initialized to {0, 0, 0}
 
struct { int a[3], b; } w[] = { { 1 }, 2 }; // array of structs
   // { 1 } is taken to be a fully-braced initializer for element #0 of the array
   // that element is initialized to { {1, 0, 0}, 0}
   // 2 is taken to be the first initialized for element #1 of the array
   // that element is initialized { {2, 0, 0}, 0}

```

|  |  |
| --- | --- |
| Array designators may be nested; the bracketed constant expression for nested arrays follows the bracketed constant expression for the outer array:   ```text int y[4][3] = {[0][0]=1, [1][1]=1, [2][0]=1};  // row 0 initialized to {1, 0, 0}                                                // row 1 initialized to {0, 1, 0}                                                // row 2 initialized to {1, 0, 0}                                                // row 3 initialized to {0, 0, 0} ``` | (since C99) |

### Notes

The order of evaluation of subexpressions in an array initializer is indeterminately sequenced in C (but not in C++ since C++11):

```
int n = 1;
int a[2] = {n++, n++}; // unspecified, but well-defined behavior,
                       // n is incremented twice (in arbitrary order)
                       // a initialized to {1, 2} and to {2, 1} are both valid
puts((char[4]){'0'+n} + n++); // undefined behavior:
                              // increment and read from n are unsequenced

```

|  |  |
| --- | --- |
| In C, the braced list of an initializer cannot be empty. C++ allows empty list: | (until C23) |
| An empty initializer can be used to initialize an array: | (since C23) |

```
int a[3] = {0}; // valid C and C++ way to zero-out a block-scope array
int a[3] = {}; // valid C++ way to zero-out a block-scope array; valid in C since C23

```

As with all other initialization, every expression in the initializer list must be a constant expression when initializing arrays of static or thread-local storage duration:

```
static char* p[2] = {malloc(1), malloc(2)}; // error

```

### Example

Run this code

```
int main(void)
{
    // The following four array declarations are the same
    short q1[4][3][2] = {
        { 1 },
        { 2, 3 },
        { 4, 5, 6 }
    };
 
    short q2[4][3][2] = {1, 0, 0, 0, 0, 0, 2, 3, 0, 0, 0, 0, 4, 5, 6};
 
    short q3[4][3][2] = {
        {
            { 1 },
        },
        {
            { 2, 3 },
        },
        {
            { 4, 5 },
            { 6 },
        }
    };
 
    short q4[4][3][2] = {1, [1]=2, 3, [2]=4, 5, 6};
 
 
    // Character names can be associated with enumeration constants
    // using arrays with designators:
    enum { RED, GREEN, BLUE };
    const char *nm[] = {
        [RED] = "red",
        [GREEN] = "green",
        [BLUE] = "blue",
    };
}

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

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/array_initialization&oldid=144380>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 16 October 2022, at 11:04.