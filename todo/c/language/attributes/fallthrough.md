# C attribute: fallthrough (since C23)

From cppreference.com
< c‎ | language‎ | attributes
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

 Declarations

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Pointer | | | | |
| Array | | | | |
| enum | | | | |
| struct | | | | |
| union | | | | |
| Bit-field | | | | |
| Atomic types (C11) | | | | |
| const | | | | |
| constexpr(C23) | | | | |
| volatile | | | | |
| restrict(C99) | | | | |
| Alignment specifiers | | | | |
| Storage duration and linkage | | | | |
| External and tentative definitions | | | | |
| typedef | | | | |
| Static assertions | | | | |
| Attributes (C23) | | | | |

 Attributes

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| deprecated(C23) | | | | |
| ****fallthrough****(C23) | | | | |
| nodiscard(C23) | | | | |
| maybe_unused(C23) | | | | |
| noreturn_Noreturn(C23)(C23)(deprecated) | | | | |
| unsequenced(C23) | | | | |
| reproducible(C23) | | | | |

Indicates that the fall through from the previous case label is intentional and should not be diagnosed by a compiler that warns on fallthrough.

### Syntax

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `[[` `fallthrough` `]]` `[[` `__fallthrough__` `]]` |  |  |
|  | | | | | | | | | |

### Explanation

May only be used in an attribute declaration to create a **fallthrough declaration** ([[fallthrough]];).

A fallthrough declaration may only be used in a switch statement, where the next block item (statement, declaration, or label) to be encounted is a statement with a `case` or `default` label for that switch statement.

Indicates that the fall through from the previous case label is intentional and should not be diagnosed by a compiler that warns on fallthrough.

### Example

Run this code

```
#include <stdbool.h>
 
void g(void) {}
void h(void) {}
void i(void) {}
 
void f(int n) {
  switch (n) {
    case 1:
    case 2:
      g();
     [[fallthrough]];
    case 3: // no warning on fallthrough
      h();
    case 4: // compiler may warn on fallthrough
      if(n < 3) {
          i();
          [[fallthrough]]; // OK
      }
      else {
          return;
      }
    case 5:
      while (false) {
        [[fallthrough]]; // ill-formed: no subsequent case or default label
      }
    case 6:
      [[fallthrough]]; // ill-formed: no subsequent case or default label
  }
}
 
int main(void) {}

```

### See also

|  |  |
| --- | --- |
| C++ documentation for fallthrough | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/attributes/fallthrough&oldid=124533>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 27 November 2020, at 07:31.