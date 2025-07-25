# Binary resource inclusion (since C23)

From cppreference.com
< c‎ | preprocessor
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

 Preprocessor

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| #if#ifdef#ifndef#else#elif#elifdef#elifndef#endif(C23)(C23) | | | | |
| #define#undef#,## operators | | | | |
| #include__has_include(C23) | | | | |
| #error#warning(C23) | | | | |
| #pragma_Pragma(C99) | | | | |
| #line | | | | |
| ****#embed__has_embed****(C23)(C23) | | | | |

#embed is a preprocessor directive to include (binary) resources in the build, where a resource is defined as a source of data accessible from the translation environment.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `#embed <` h-char-sequence `>` embed-parameter-sequence ﻿(optional) new-line | (1) |  |
|  | | | | | | | | | |
| `#embed "` q-char-sequence `"` embed-parameter-sequence ﻿(optional) new-line | (2) |  |
|  | | | | | | | | | |
| `#embed` pp-tokens new-line | (3) |  |
|  | | | | | | | | | |
| `__has_embed` `(` `"` q-char-sequence `"` embed-parameter-sequence ﻿(optional) `)` `__has_embed` `(` `<` h-char-sequence `>` embed-parameter-sequence ﻿(optional) `)` | (4) |  |
|  | | | | | | | | | |
| `__has_embed` `(` string-literal pp-balanced-token-sequence ﻿(optional) `)` `__has_embed` `(` `<` h-pp-tokens `>` pp-balanced-token-sequence ﻿(optional) `)` | (5) |  |
|  | | | | | | | | | |

1) Searches for a resource identified uniquely by h-char-sequence and replaces the directive by a comma separated list of integers corresponding to the data of the resource.2) Searches for a resource identified by q-char-sequence and replaces the directive by a list of integers corresponding to the data of the resource. It may fallback to (1).3) If neither (1) nor (2) is matched, pp-tokens will undergo macro replacement. The directive after replacement will be tried to match with (1) or (2) again.4) Checks whether a resource is available for embedding, whether it is empty or not and whether the parameters passed are supported by the implementation.5) If (4) is not matched, h-pp-tokens and pp-balanced-token-sequence will undergo macro replacement. The directive after replacement will be tried to match with (4) again.

|  |  |  |
| --- | --- | --- |
| new-line | - | The new-line character |
| h-char-sequence | - | A sequence of one or more h-chars, where the appearance of any of the following causes undefined behavior:  - the character ' - the character " - the character \ - the character sequence // - the character sequence /\* |
| h-char | - | Any member of the source character set except new-line and > |
| q-char-sequence | - | A sequence of one or more q-chars, where the appearance of any of the following causes undefined behavior:  - the character ' - the character \ - the character sequence // - the character sequence /\* |
| q-char | - | Any member of the source character set except new-line and " |
| pp-tokens | - | A sequence of one or more preprocessing tokens |
| string-literal | - | A string literal |
| h-pp-tokens | - | A sequence of one or more preprocessing tokens except > |
| embed-parameter-sequence | - | A sequence of one or more pp-parameter ﻿s. Note that unlike an attribute-list, this sequence is not comma separated. |
| pp-parameter | - | An attribute-token (see: attributes) but comprised of preprocessing tokens instead of tokens. |
| pp-balanced-token-sequence | - | A balanced-token-sequence (see: attributes) but comprised of preprocessing tokens instead of tokens |

### Explanation

1) Searches for the resource identified by h-char-sequence in implementation-defined manner.2) Searches for the resource identified by q-char-sequence in implementation-defined manner. For (1,2), the implementations typically use a mechanism similar to, but distinct from, the implementation-defined search paths used for source file inclusion. The construct __has_embed(__FILE__ ... appears in one of the examples in the standard, suggesting, in case (2) at least, that the directory where the current file resides is expected to be searched.3) The preprocessing tokens after `embed` in the directive are processed just as in normal text (i.e., each identifier currently defined as a macro name is replaced by its replacement list of preprocessing tokens). The directive resulting after all replacements shall match one of the two previous forms. The method by which a sequence of preprocessing tokens between < and > preprocessing token pair or a pair of " characters is combined into a single header name preprocessing token is implementation-defined.4) The resource identified by h-char-sequence or q-char-sequence is searched for as if that preprocessing token sequence were the pp-tokens in syntax (3), except that no further macro expansion is performed. If such a directive would not satisfy the
syntactic requirements of an #embed directive, the program is ill-formed. The `__has__embed` expression evaluates to __STDC_EMBED_FOUND__ if the search for the resource succeeds, the resource is non empty and all the parameters are supported, to __STDC_EMBED_EMPTY__ if the resource is empty and all the parameters are supported, and to __STDC_EMBED_NOT_FOUND__ if the search fails or one of the parameters passed is not supported by the implementation.5) This form is considered only if syntax (4) does not match, in which case the preprocessing tokens are processed just as in normal text.

In the case the resource is not found or one of the parameters is not supported by the implementation, the program is ill-formed.

`__has_embed` can be expanded in the expression of #if and #elif. It is treated as a defined macro by #ifdef, #ifndef, #elifdef, #elifndef and defined but cannot be used anywhere else.

A resource has an **implementation resource width** which is the implementation-defined size in bits of the located resource. Its **resource width** is the implementation resource width unless modified by a `limit` parameter. If the resource width is 0, the resource is considered empty. The **embed element width** is equal to CHAR_BIT unless modified by an implementation defined parameter. The resource width must be divisible by the embed element width.

The expansion of a #embed directive is a token sequence formed from the list of integer constant expressions described below. The group of tokens for each integer constant expression in the list is separated in the token sequence from the group of tokens for the previous integer constant expression in the list by a comma. The sequence neither begins nor ends in a comma. If the list of integer constant expressions is empty, the token sequence is empty. The directive is replaced by its expansion and, with the presence of certain embed parameters, additional or replacement token sequences.

The values of the integer constant expressions in the expanded sequence are determined by an implementation-defined mapping of the resource’s data. Each integer constant expression’s value is in the range ``0`,`2embed element width`)`. If:

1. The list of integer constant expressions is used to initialize an array of a type compatible with unsigned char, or compatible with char if char cannot hold negative values, and
2. The embed element width is equal to [CHAR_BIT,

then the contents of the initialized elements of the array are as-if the resource’s binary data is fread into the array at translation time.

Implementations are encouraged to take into account translation-time bit and byte orders as well as execution-time bit and byte orders to more appropriately represent the resource’s binary data from the directive. This maximizes the chance that, if the resource referenced at translation time through the #embed directive is the same one accessed through execution-time means, the data that is e.g. fread or similar into contiguous storage will compare bit-for-bit equal to an array of character type initialized from an #embed directive’s expanded contents.

### Parameters

The standard defines the parameters `limit`, `prefix`, `suffix` and `if_empty`. Any other parameter that appears in the directive must be implementation-defined, or the program is ill-formed. Implementation-defined embed parameters may change the semantics of the directive.

#### limit

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `limit(` constant-expression `)` | (1) |  |
|  | | | | | | | | | |
| `__limit__(` constant-expression `)` | (2) |  |
|  | | | | | | | | | |

The `limit` embed parameter can appear at most once in the embed parameter sequence. It must have an argument, which must be an integer (preprocessor) constant expression that evaluates to a non negative number and does not contain the token defined. The resource width is set to the minimum of the integer constant expression multiplied by the embed element width and the implementation resource width.

#### suffix

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `suffix(` pp-balanced-token-sequence ﻿(optional) `)` | (1) |  |
|  | | | | | | | | | |
| `__suffix__(` pp-balanced-token-sequence ﻿(optional) `)` | (2) |  |
|  | | | | | | | | | |

The `suffix` embed parameter can appear at most once in the embed parameter sequence. It must have a (possibly empty) preprocessor argument clause. If the resource is non empty, the contents of the parameter clause are placed immediately after the expansion of the directive. Otherwise, it has no effect.

#### prefix

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `prefix(` pp-balanced-token-sequence ﻿(optional) `)` | (1) |  |
|  | | | | | | | | | |
| `__prefix__(` pp-balanced-token-sequence ﻿(optional) `)` | (2) |  |
|  | | | | | | | | | |

The `prefix` embed parameter can appear at most once in the embed parameter sequence. It must have a (possibly empty) preprocessor argument clause. If the resource is non empty, the contents of the parameter clause are placed immediately before the expansion of the directive. Otherwise, it has no effect.

#### if_empty

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `if_empty(` pp-balanced-token-sequence ﻿(optional) `)` | (1) |  |
|  | | | | | | | | | |
| `__if_empty__(` pp-balanced-token-sequence ﻿(optional) `)` | (2) |  |
|  | | | | | | | | | |

The `if_empty` embed parameter can appear at most once in the embed parameter sequence. It must have a (possibly empty) preprocessor argument clause. If the resource is empty, the contents of the parameter clause replace the directive. Otherwise, it has no effect.

### Example

Run this code

```
#include <stdint.h>
#include <stdio.h>
 
const uint8_t image_data[] = {
#embed "image.png"
};
 
const char message[] = {
#embed "message.txt" if_empty('M', 'i', 's', 's', 'i', 'n', 'g', '\n')
,'\0' // null terminator
};
 
void dump(const uint8_t arr[], size_t size)
{
    for (size_t i = 0; i != size; ++i)
        printf("%02X%c", arr[i], (i + 1) % 16 ? ' ' : '\n');
    puts("");
}
 
int main()
{
    puts("image_data[]:");
    dump(image_data, sizeof image_data);
    puts("message[]:");
    dump((const uint8_t*)message, sizeof message);
}

```

Possible output:

```
image_data[]:
89 50 4E 47 0D 0A 1A 0A 00 00 00 0D 49 48 44 52
00 00 00 01 00 00 00 01 01 03 00 00 00 25 DB 56
...
message[]:
4D 69 73 73 69 6E 67 0A 00

```

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.4.7 Header names (p: 69)

:   - 6.10.1 Conditional inclusion (p: 165-169)

:   - 6.10.2 Binary resource inclusion (p: 170-177)

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/preprocessor/embed&oldid=160331>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 8 October 2023, at 13:40.