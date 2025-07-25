# Statements

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
| ****Statements**** | | | | |
| Expressions | | | | |
| Initialization | | | | |
| Declarations | | | | |
| Functions | | | | |
| Miscellaneous | | | | |
| History of C | | | | |
| Technical Specifications | | | | |

 ****Statements****

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Labels | | | | |
| label : statement | | | | |
| Expression statements | | | | |
| expression ; | | | | |
| Compound statements | | | | |
| { statement... } | | | | |
| Selection statements | | | | |
| if | | | | |
| switch | | | | |
| Iteration statements | | | | |
| while | | | | |
| do-while | | | | |
| for | | | | |
| Jump statements | | | | |
| break | | | | |
| continue | | | | |
| return | | | | |
| goto | | | | |

Statements are fragments of the C program that are executed in sequence. The body of any function is a compound statement, which, in turn is a sequence of statements and declarations:

```
int main(void)
{ // start of a compound statement
    int n = 1; // declaration (not a statement)
    n = n+1; // expression statement
    printf("n = %d\n", n); // expression statement
    return 0; // return statement
} // end of compound statement, end of function body

```

There are five types of statements:

1) compound statements2) expression statements3) selection statements4) iteration statements5) jump statements

|  |  |
| --- | --- |
| An attribute specifier sequence (attr-spec-seq) can be applied to an unlabeled statement, in which case (except for an expression statement) the attributes are applied to the respective statement. | (since C23) |

### Labels

Any statement can be **labeled**, by providing a name followed by a colon before the statement itself.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) identifier `:` | (1) |  |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `case` constant-expression `:` | (2) |  |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `default` `:` | (3) |  |
|  | | | | | | | | | |

1) Target for goto.2) Case label in a switch statement.3) Default label in a switch statement.

Any statement (but not a declaration) may be preceded by any number of **labels**, each of which declares identifier to be a label name, which must be unique within the enclosing function (in other words, label names have function scope).

Label declaration has no effect on its own, does not alter the flow of control, or modify the behavior of the statement that follows in any way.

|  |  |
| --- | --- |
| A label shall be followed by a statement. | (until C23) |
| A label can appear without its following statement. If a label appears alone in a block, it behaves as if it is followed by a null statement.  The optional attr-spec-seq is applied to the label. | (since C23) |

### Compound statements

A compound statement, or **block**, is a brace-enclosed sequence of statements and declarations.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| `{` statement `|` declaration...(optional) `}` |  | (until C23) |
|  | | | | | | | | | |
| attr-spec-seq(optional) `{` unlabeled-statement `|` label `|` declaration...(optional) `}` |  | (since C23) |
|  | | | | | | | | | |

The compound statement allows a set of declarations and statements to be grouped into one unit that can be used anywhere a single statement is expected (for example, in an if statement or an iteration statement):

```
if (expr) // start of if-statement
{ // start of block
  int n = 1; // declaration
  printf("%d\n", n); // expression statement
} // end of block, end of if-statement

```

Each compound statement introduces its own block scope.

The initializers of the variables with automatic storage duration declared inside a block and the VLA declarators are executed when flow of control passes over these declarations in order, as if they were statements:

```
int main(void)
{ // start of block
  { // start of block
       puts("hello"); // expression statement
       int n = printf("abc\n"); // declaration, prints "abc", stores 4 in n
       int a[n*printf("1\n")]; // declaration, prints "1", allocates 8*sizeof(int)
       printf("%zu\n", sizeof(a)); // expression statement
  } // end of block, scope of n and a ends
  int n = 7; // n can be reused
}

```

### Expression statements

An expression followed by a semicolon is a statement.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| expression(optional) `;` | (1) |  |
|  | | | | | | | | | |
| attr-spec-seq expression `;` | (2) | (since C23) |
|  | | | | | | | | | |

Most statements in a typical C program are expression statements, such as assignments or function calls.

An expression statement without an expression is called a **null statement**. It is often used to provide an empty body to a for or while loop. It can also be used to carry a label in the end of a compound statement or before a declaration:

```
puts("hello"); // expression statement
char *s;
while (*s++ != '\0')
    ; // null statement

```

|  |  |
| --- | --- |
| The optional attr-spec-seq is applied to the expression.  An attr-spec-seq followed by `;` does not form an expression statement. It forms an attribute declaration instead. | (since C23) |

### Selection statements

The selection statements choose between one of several statements depending on the value of an expression.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `if` `(` expression `)` statement | (1) |  |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `if` `(` expression `)` statement `else` statement | (2) |  |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `switch` `(` expression `)` statement | (3) |  |
|  | | | | | | | | | |

1) if statement2) if statement with an else clause3) switch statement

### Iteration statements

The iteration statements repeatedly execute a statement.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `while` `(` expression `)` statement | (1) |  |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `do` statement `while` `(` expression `)` `;` | (2) |  |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `for` `(` init-clause `;` expression(optional) `;` expression(optional) `)` statement | (3) |  |
|  | | | | | | | | | |

1) while loop2) do-while loop3) for loop

### Jump statements

The jump statements unconditionally transfer flow control.

|  |  |  |  |  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `break` `;` | (1) |  |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `continue` `;` | (2) |  |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `return` expression(optional) `;` | (3) |  |
|  | | | | | | | | | |
| attr-spec-seq(optional)(since C23) `goto` identifier `;` | (4) |  |
|  | | | | | | | | | |

1) break statement2) continue statement3) return statement with an optional expression4) goto statement

### References

- C23 standard (ISO/IEC 9899:2024):

:   - 6.8 Statements and blocks (p: TBD)

- C17 standard (ISO/IEC 9899:2018):

:   - 6.8 Statements and blocks (p: 106-112)

- C11 standard (ISO/IEC 9899:2011):

:   - 6.8 Statements and blocks (p: 146-154)

- C99 standard (ISO/IEC 9899:1999):

:   - 6.8 Statements and blocks (p: 131-139)

- C89/C90 standard (ISO/IEC 9899:1990):

:   - 3.6 STATEMENTS

### See also

|  |  |
| --- | --- |
| C++ documentation for Statements | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/language/statements&oldid=179343>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 7 January 2025, at 23:07.