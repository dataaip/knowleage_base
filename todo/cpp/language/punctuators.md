# Punctuation

From cppreference.com
< cpp‎ | language
C++

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Compiler support | | | | |
| Freestanding and hosted | | | | |
| Language | | | | |
| Standard library | | | | |
| Standard library headers | | | | |
| Named requirements | | | | |
| Feature test macros (C++20) | | | | |
| Language support library | | | | |
| Concepts library (C++20) | | | | |
| Diagnostics library | | | | |
| Memory management library | | | | |
| Metaprogramming library (C++11) | | | | |
| General utilities library | | | | |
| Containers library | | | | |
| Iterators library | | | | |
| Ranges library (C++20) | | | | |
| Algorithms library | | | | |
| Strings library | | | | |
| Text processing library | | | | |
| Numerics library | | | | |
| Date and time library | | | | |
| Input/output library | | | | |
| Filesystem library (C++17) | | | | |
| Concurrency support library (C++11) | | | | |
| Execution support library (C++26) | | | | |
| Technical specifications | | | | |
| Symbols index | | | | |
| External libraries | | | | |

C++ language

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| General topics | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Preprocessor | | | | | | Comments | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Keywords | | | | | | Escape sequences | | | | | |
| Flow control | | | | |
| Conditional execution statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | if | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | switch | | | | | |
| Iteration statements (loops) | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | for | | | | | | range-`for` (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | while | | | | | | `do-while` | | | | | |
| Jump statements | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | continue - break | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | goto - return | | | | | |
| Functions | | | | |
| Function declaration | | | | |
| Lambda function expression | | | | |
| `inline` specifier | | | | |
| Dynamic exception specifications (until C++17\*) | | | | |
| `noexcept` specifier (C++11) | | | | |
| Exceptions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `throw`-expression | | | | | | `try` block | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | |  | | | | | | `catch` handler | | | | | |
| Namespaces | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace declaration | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Namespace aliases | | | | | |
| Types | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Fundamental types | | | | | | Enumeration types | | | | | | Function types | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class/struct types | | | | | | Union types | | | | | |  | | | | | |
| Specifiers | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `const`/`volatile` | | | | | | decltype (C++11) | | | | | | auto (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | constexpr (C++11) | | | | | | consteval (C++20) | | | | | | constinit (C++20) | | | | | |
| Storage duration specifiers | | | | |
| Initialization | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default-initialization | | | | | | Value-initialization | | | | | | Zero-initialization | | | | | | Copy-initialization | | | | | | Direct-initialization | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Aggregate initialization | | | | | | List-initialization (C++11) | | | | | | Constant initialization | | | | | | Reference initialization | | | | | |  | | | | | |

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Expressions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Value categories | | | | | | Order of evaluation | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Operators | | | | | | Operator precedence | | | | | |
| Alternative representations | | | | |
| Literals | | | | |
| Boolean - Integer - Floating-point | | | | |
| Character - String - nullptr (C++11) | | | | |
| User-defined (C++11) | | | | |
| Utilities | | | | |
| Attributes (C++11) | | | | |
| Types | | | | |
| `typedef` declaration | | | | |
| Type alias declaration (C++11) | | | | |
| Casts | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Implicit conversions | | | | | | static_cast | | | | | | const_cast | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Explicit conversions | | | | | | dynamic_cast | | | | | | reinterpret_cast | | | | | |
| Memory allocation | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | `new` expression | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | `delete` expression | | | | | |
| Classes | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class declaration | | | | | | Constructors | | | | | | `this` pointer | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Access specifiers | | | | | | `friend` specifier | | | | | |  | | | | | |
| Class-specific function properties | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Virtual function | | | | | | `override` specifier (C++11) | | | | | | `final` specifier (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | explicit (C++11) | | | | | | static | | | | | |  | | | | | |
| Special member functions | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Default constructor | | | | | | Copy constructor | | | | | | Move constructor (C++11) | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Copy assignment | | | | | | Move assignment (C++11) | | | | | | Destructor | | | | | |
| Templates | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Class template | | | | | | Function template | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | Template specialization | | | | | | Parameter packs (C++11) | | | | | |
| Miscellaneous | | | | |
| |  |  |  |  |  | | --- | --- | --- | --- | --- | | Inline assembly | | | | | | |  |  |  |  |  | | --- | --- | --- | --- | --- | | History of C++ | | | | | |

 Basic Concepts

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| Comments | | | | |
| ASCII | | | | |
| ****Punctuation**** | | | | |
| Names and identifiers | | | | |
| Types | | | | |
| Fundamental types | | | | |
| Objects | | | | |
| Scope | | | | |
| Object lifetime | | | | |
| Storage duration and linkage | | | | |
| Definitions and ODR | | | | |
| Name lookup | | | | |
| Qualified name lookup | | | | |
| Unqualified name lookup | | | | |
| The as-if rule | | | | |
| Undefined behavior | | | | |
| Memory model | | | | |
| Multi-threaded executions and data races (C++11) | | | | |
| Character sets and encodings | | | | |
| Phases of translation | | | | |
| The `main` function | | | | |
| Modules (C++20) | | | | |

These are the punctuation symbols in C++. The meaning of each symbol is detailed in the linked pages.

### Preprocessing operators

Preprocessing operators are recognized by preprocessors.

#### # (including %:)

- Introduce a preprocessing directive.
- The preprocessing operator for stringification.

#### ##(including %:%:)

- The preprocessing operator for token pasting.

### Single-character operators and punctuators

#### { and } (including <% and %>)

- In a class definition, delimit the member specification.
- In an enumeration definition, delimit the enumerator list.
- Delimit a compound statement. The compound statement may be part of

:   - a function definition
    - a try block

|  |  |
| --- | --- |
| - a lambda expression | (since C++11) |

- Part of the aggregate initialization(until C++11)list-initialization(since C++11) syntax of an initializer.
- In a namespace definition, delimit the namespace body.
- In a language linkage specification, delimit the declarations.

|  |  |
| --- | --- |
| - In a requires expression, delimit the requirements. - In a compound requirement, delimit the expression. - In an export declaration, delimit the declarations. | (since C++20) |

#### [ and ] (including <: and :>)

- Subscript operator; part of operator[] in operator overloading.
- Part of array declarator in a declaration or a type-id (e.g. in a new expression).
- Part of new[] operator in operator overloading (allocation function).
- Part of delete[] operator in delete expression and operator overloading (deallocation function).

|  |  |
| --- | --- |
| - In a lambda expression, delimit the captures. - In an attribute specifier, delimit the attributes. | (since C++11) |
| - In a structured binding declaration, delimit the identifier list. | (since C++17) |
| - In a pack indexing, delimit converted constant expression representing an index. | (since C++26) |

#### ( and )

- In an expression, indicate grouping.
- Function call operator; part of operator() in operator overloading.
- In a function-style type cast, delimit the expression/initializers.
- In a `static_cast`, `const_cast`, `reinterpret_cast`, or `dynamic_cast`, delimit the expression.
- Delimit the operand of the following operators:

:   - `typeid`
    - `sizeof`

|  |  |
| --- | --- |
| - `sizeof...` - `alignof` - `noexcept` | (since C++11) |

- In a placement new expression, delimit the placement arguments.
- In a new expression, optionally delimit the type-id.
- In a new expression, delimit the initializers.
- In a C-style cast, delimit the type-id.
- In a declaration or a type-id, indicate grouping.
- Delimit the parameter list in

:   - a function declarator (in a declaration or a type-id)

|  |  |
| --- | --- |
| - a lambda expression | (since C++11) |
| - a user-defined deduction guide | (since C++17) |
| - a requires expression | (since C++20) |

- Part of the direct-initialization syntax of an initializer.
- In an asm declaration, delimit the string literal.
- In a member initializer list, delimit the initializers to a base or member.
- Delimit the controlling clause of a selection statement or iteration statement, including:

:   - `if` (except consteval if)(since C++23)
    - `switch`
    - `while`
    - `do-while`
    - `for`

|  |  |
| --- | --- |
| - range-based `for` | (since C++11) |

- In a handler, delimit the parameter declaration.
- In a function-like macro definition, delimit the macro parameters.
- In a function-like macro invocation, delimit the macro arguments or prevent commas from being interpreted as argument separators.
- Part of a `defined`, `__has_include`(since C++17), `__has_cpp_attribute`(since C++20) preprocessing operator.

|  |  |  |  |
| --- | --- | --- | --- |
| - In a `static_assert` declaration, delimit the operands. - Delimit the operand of the following specifiers:   - `decltype` - `noexcept` - `alignas`   |  |  | | --- | --- | | - `explicit` | (since C++20) |  - In an attribute, delimit the attribute arguments. | (since C++11) |
| - Part of `decltype(auto)` specifier. | (since C++14) |
| - Delimit a fold expression. | (since C++17) |
| - Part of __VA_OPT__ replacement in a variadic macro definition. | (since C++20) |

#### ;

- Indicate the end of

:   - a statement
    - a declaration or member declaration

|  |  |
| --- | --- |
| - a module declaration, import declaration, global module fragment introducer, or private module fragment introducer - a requirement | (since C++20) |

- Separate the condition and statement of a for statement.

#### :

- Part of conditional operator.
- Part of label declaration.
- In the base-clause of a class definition, introduce the base class.
- Part of access specifier in member specification.
- In a bit-field member declaration, introduce the width.
- In a constructor definition, introduce the member initializer list.

|  |  |
| --- | --- |
| - In a range-based for statement, separate the item-declaration and the range-initializer. - In the enum-base of an enumeration declaration, introduce the underlying type. | (since C++11) |
| - In an attribute specifier, separate the attribute-namespace and the attribute-list. | (since C++17) |
| - In a module declaration or import declaration of module partition, introduce the module partition name. - Part of a private module fragment introducer (module :private;). | (since C++20) |

#### ?

- Part of conditional operator.

#### .

- Member access operator.

|  |  |
| --- | --- |
| - In aggregate initialization, introduce a designator. - Part of module name or module partition name. | (since C++20) |

#### ~ (including compl)

- Unary complement operator (a.k.a. bitwise not operator); part of operator~ in operator overloading.
- Part of an identifier expression to name a destructor or pseudo-destructor.

#### ! (including not)

- Logical not operator; part of operator! in operator overloading.

|  |  |
| --- | --- |
| - Part of consteval if statement. | (since C++23) |

#### +

- Unary plus operator; part of operator+ in operator overloading.
- Binary plus operator; part of operator+ in operator overloading.

#### -

- Unary minus operator; part of operator- in operator overloading.
- Binary minus operator; part of operator- in operator overloading.

#### \*

- Indirection operator; part of operator\* in operator overloading.
- Multiplication operator; part of operator\* in operator overloading.
- Pointer operator or part of pointer-to-member operator in a declarator or in a type-id.

|  |  |
| --- | --- |
| - Part of \*this in a lambda capture list, to capture the current object by copy. | (since C++17) |

#### /

- Division operator; part of operator/ in operator overloading.

#### %

- Modulo operator; part of operator% in operator overloading.

#### ^ (including xor)

- Bitwise xor operator; part of operator^ in operator overloading.

#### & (including bitand)

- Address-of operator; part of operator& in operator overloading.
- Bitwise and operator; part of operator& in operator overloading.
- Lvalue-reference operator in a declarator or in a type-id.

|  |  |
| --- | --- |
| - In a lambda capture, indicate by-reference capture. - Ref-qualifier in member function declaration. | (since C++11) |

#### | (including bitor)

- Bitwise or operator; part of operator| in operator overloading.

#### =

- Simple assignment operator; part of operator= in operator overloading, which might be a special member function (copy assignment operatoror move assignment operator(since C++11)).
- Part of the copy-initialization and aggregate initialization(until C++11)copy-list-initialization(since C++11) syntax of an initializer.
- In a function declaration, introduce a default argument.
- In a template parameter list, introduce a default template argument.
- In a namespace alias definition, separate the alias and the aliased namespace.
- In an enum definition, introduce the value of enumerator.
- Part of pure-specifier in a pure virtual function declaration.

|  |  |
| --- | --- |
| - Capture default in lambda capture, to indicate by-copy capture. - Part of defaulted definition (=default;) or deleted definition (=delete;) in function definition. - In a type alias declaration, separate the alias and the aliased type. | (since C++11) |
| - In a concept definition, separate the concept name and the constraint expression. | (since C++20) |

#### <

- Less-than operator; part of operator< in operator overloading.
- In a `static_cast`, `const_cast`, `reinterpret_cast`, or `dynamic_cast`, introduce the type-id.
- Introduce a template argument list.
- Introduce a template parameter list in

:   - a template declaration
    - a partial specialization

|  |  |
| --- | --- |
| - a lambda expression | (since C++20) |

- Part of template<> in template specialization declaration.
- Introduce a header name in

:   - a #include directive

|  |  |
| --- | --- |
| - a __has_include preprocessing expression | (since C++17) |
| - an import declaration | (since C++20) |

#### >

- Greater-than operator; part of operator> in operator overloading.
- `static_cast`, `const_cast`, `reinterpret_cast`, or `dynamic_cast`, indicate the end of type-id.
- Indicate the end of a template argument list.
- Indicate the end of a template parameter list in

:   - a template declaration
    - a partial specialization

|  |  |
| --- | --- |
| - a lambda expression | (since C++20) |

- Part of template<> in template specialization declaration.
- Indicate the end of a header name in

:   - a #include directive

|  |  |
| --- | --- |
| - a __has_include preprocessing expression | (since C++17) |
| - an import declaration | (since C++20) |

#### ,

- Comma operator; part of operator, in operator overloading.
- List separator in

:   - the declarator list in a declaration
    - initializer list in initialization
    - the placement argument list in a placement new
    - the argument list in a function call expression
    - the enumerator list in an enum declaration
    - the base class list in a class declaration
    - the member initializer list in a constructor definition
    - a function parameter list
    - a template parameter list
    - a template argument list

|  |  |
| --- | --- |
| - a lambda capture list - an attribute list | (since C++11) |
| - the declarator list in a using-declaration - the identifier list in a structured binding declaration | (since C++17) |
| - the argument list in a multi-argument subscript expression | (since C++23) |

:   - the macro parameter list in a function-like macro definition
    - the macro argument list in a function-like macro invocation, unless found between the parentheses of an argument

|  |  |
| --- | --- |
| - In a `static_assert` declaration, separate the arguments. | (since C++11) |

### Multi-character operators and punctuators

#### ...

- In the parameter list of a function declaratoror lambda expression(since C++11)or user-defined deduction guide(since C++17), signify a variadic function.
- In a handler, signify catch-all handler.

|  |  |
| --- | --- |
| - In a macro definition, signify a variadic macro. - Indicate pack declaration and expansion. | (since C++11) |
| - In pack indexing expression and specifier. | (since C++26) |

#### ::

- Scope resolution operator in

:   - a qualified name
    - a pointer-to-member declaration
    - a `new` or `delete` expression, to indicate that only global allocation or deallocation functions are looked up

|  |  |
| --- | --- |
| - In an attribute, indicate attribute scope. | (since C++11) |
| - Part of nested namespace definition. | (since C++17) |

#### .\*

- Pointer-to-member access operator.

#### ->

- Member access operator; part of operator-> in operator overloading.

|  |  |
| --- | --- |
| - In a function declarator or lambda expression, introduce the trailing return type. | (since C++11) |
| - In a user-defined deduction guide, introduce the result type. | (since C++17) |
| - In a compound requirement, introduce the return type requirement. | (since C++20) |

#### ->\*

- Pointer-to-member access operator; part of operator->\* in operator overloading.

#### +=

- Compound assignment operator; part of operator+= in operator overloading.

#### -=

- Compound assignment operator; part of operator-= in operator overloading.

#### \*=

- Compound assignment operator; part of operator\*= in operator overloading.

#### /=

- Compound assignment operator; part of operator/= in operator overloading.

#### %=

- Compound assignment operator; part of operator%= in operator overloading.

#### ^= (including xor_eq)

- Compound assignment operator; part of operator^= in operator overloading.

#### &= (including and_eq)

- Compound assignment operator; part of operator&= in operator overloading.

#### |= (including or_eq)

- Compound assignment operator; part of operator|= in operator overloading.

#### ==

- Equality operator; part of operator== in operator overloading.

#### != (including not_eq)

- Inequality operator; part of operator!= in operator overloading.

#### <=

- Less-than-or-equal-to operator; part of operator<= in operator overloading.

#### >=

- Greater-than-or-equal-to operator; part of operator>= in operator overloading.

|  |  |
| --- | --- |
| <=>  - Three-way comparison (spaceship) operator; part of operator<=> in operator overloading. | (since C++20) |

#### && (including and)

- Logical and operator; part of operator&& in operator overloading.

|  |  |
| --- | --- |
| - Rvalue-reference operator in a declarator or in a type-id. - Ref-qualifier in member function declaration. | (since C++11) |

#### || (including or)

- Logical or operator; part of operator|| in operator overloading.

#### <<

- Bitwise shift operator; part of operator<< in operator overloading (bitwise operator or stream insertion operator).

#### >>

- Bitwise shift operator; part of operator>> in operator overloading (bitwise operator or stream extraction operator).

#### <<=

- Compound assignment operator; part of operator<<= in operator overloading.

#### >>=

- Compound assignment operator; part of operator>>= in operator overloading.

#### ++

- Increment operator; part of operator++ in operator overloading.

#### --

- Decrement operator; part of operator-- in operator overloading.

### References

- C++23 standard (ISO/IEC 14882:2024):

:   - 5.12 Operators and punctuators [lex.operators]

- C++20 standard (ISO/IEC 14882:2020):

:   - 5.12 Operators and punctuators [lex.operators]

- C++17 standard (ISO/IEC 14882:2017):

:   - 5.12 Operators and punctuators [lex.operators]

- C++14 standard (ISO/IEC 14882:2014):

:   - 2.13 Operators and punctuators [lex.operators]

- C++11 standard (ISO/IEC 14882:2011):

:   - 2.13 Operators and punctuators [lex.operators]

- C++03 standard (ISO/IEC 14882:2003):

:   - 2.12 Operators and punctuators [lex.operators]

- C++98 standard (ISO/IEC 14882:1998):

:   - 2.12 Operators and punctuators [lex.operators]

### See also

|  |  |
| --- | --- |
| Alternative representations | alternative spellings for certain operators |
| C documentation for Punctuation | |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=cpp/language/punctuators&oldid=173967>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 30 July 2024, at 18:12.