# File scope

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

If the declarator or type specifier that declares the identifier appears outside of any block or list of parameters, the identifier has file scope, which terminates at the end of the translation unit.

So, placement of an identifier's declaration (in a declarator or type specifier) outside any block or list of parameters means that the identifier has file scope. File scope of an identifier extends from the declaration to the end of the translation unit in which the declaration appears.

### Example

Identifiers a, b, f, and g have file scope.

Run this code

```
#include <stdio.h>
 
int a = 1;
static int b = 2;
 
void f (void) {printf("from function f()\n");}
static void g (void) {printf("from function g()\n");}
 
int main(void)
{
    f();
    g();
 
    return 0;
}
/* end of this translation unit, end of file scope */

```

Possible output:

```
from function f()
from function g()

```

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/file_scope&oldid=72742>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 22 September 2014, at 09:26.