# C 语言参考

来自 [cppreference.com](https://en.cppreference.com/w/c)

---

## 内容概览

| 类别                     | 子项                   | 子项                | 子项                 | 子项                           |
|--------------------------|------------------------|---------------------|----------------------|--------------------------------|
| 编译器支持               | GCC                    | Clang               | MSVC                 | Intel                          |
| 语言基础                 | 基本概念               | 关键字              | 预处理器             | 表达式                         |
|                          | 声明                   | 初始化              | 函数                 | 语句                           |
| 头文件                   | 标准库头文件           | 用户定义头文件      |                      |                                |
| 类型支持                 | 基本数据类型           | 枚举类型            | 结构体               | 联合体                         |
| 程序工具                 | 命令行参数             | 环境变量            | 进程控制             | 时间与日期                     |
| 可变参数函数支持         | va_list                | va_start            | va_arg               | va_end                         |
| 错误处理                 | perror                 | errno               | strerror             |                                |
| 动态内存管理             | malloc                 | calloc              | realloc              | free                           |
| 字符串库                 | 空字符结尾字符串       | 单字节字符          | 多字节字符           | 宽字符                         |
| 算法库                   | qsort                  | bsearch             | 搜索算法             | 排序算法                       |
| 数值计算                 | 数学函数               | 浮点环境            | 伪随机数生成         | 复数运算                       |
|                          | 类型泛型数学宏         | 位操作              | 检查型整数算术       |                                |
| 日期与时间工具           | time                   | ctime               | localtime            | mktime                         |
| 输入/输出支持            | 文件操作               | 格式化输入输出      | 字符输入输出         | 字符串输入输出                 |
| 本地化支持               | setlocale              | localeconv          | LC_*                 |                                |
| 并发支持（C11）          | _Atomic                | mtx_t               | cnd_t                | thrd_t                         |
| 技术规范                 | 动态内存扩展           | 浮点扩展，第一部分  | 浮点扩展，第四部分   |                                |
| 符号索引                 |                        |                     |                      |                                |

---

## 版本与标准支持

**C 标准演进**：C89、C95、C99、C11、C17、C23  
**当前文档支持的编译器特性**：C99、C23

### 编译器支持

- **GCC (GNU Compiler Collection)**: 一个广泛使用的开源编译器套件，支持多种编程语言，包括 C 和 C++。它支持最新的 C23 标准。
- **Clang**: 由 LLVM 项目开发的编译器前端，支持 C、C++、Objective-C 等语言。Clang 提供了快速的编译速度和强大的静态分析工具。
- **MSVC (Microsoft Visual C++)**: Microsoft 的 C/C++ 编译器，广泛用于 Windows 平台开发。它支持最新的 C23 标准，并提供了集成开发环境 (IDE)。
- **Intel**: Intel 的编译器套件，针对 Intel 架构进行了优化。支持 C 和 C++ 语言，并提供了一些独特的性能优化选项。

---

## 主要章节结构

### 语言基础（Language）

#### 基本概念

C 语言是一种过程式编程语言，强调低级内存操作。程序由函数组成，函数可以调用其他函数。C 语言没有内置的类或对象的概念，但可以通过结构体和指针来模拟面向对象编程的一些特性。

#### 关键字

C 语言的关键字是预定义的标识符，具有特殊的含义。例如：
- `int`: 声明整数类型变量。
- `char`: 声明字符类型变量。
- `float`, `double`: 声明浮点类型变量。
- `if`, `else`, `switch`, `case`: 控制流程。
- `for`, `while`, `do-while`: 循环控制。
- `return`: 从函数返回值。

#### 预处理器

C 语言的预处理器在编译之前对源代码进行处理。常用的预处理指令包括：
- `#include`: 包含头文件。
- `#define`: 定义宏。
- `#ifdef`, `#ifndef`, `#endif`: 条件编译。
- `#pragma`: 发出编译器特定的指令。

**示例**:
```c
#include <stdio.h>
#define PI 3.14159

int main() {
    #ifdef DEBUG
        printf("Debug mode\n");
    #endif
    printf("Value of PI: %f\n", PI);
    return 0;
}
```

#### 表达式

表达式是由操作数和运算符组成的序列，用于计算值。常见的运算符包括：
- 算术运算符: `+`, `-`, `*`, `/`, `%`
- 关系运算符: `==`, `!=`, `<`, `>`, `<=`, `>=`
- 逻辑运算符: `&&`, `||`, `!`
- 位运算符: `&`, `|`, `^`, `~`, `<<`, `>>`
- 赋值运算符: `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `&=`, `|=`, `^=`, `<<=`, `>>=`

**示例**:
```c
int a = 5, b = 3;
int sum = a + b; // 算术运算
int is_equal = (a == b); // 关系运算
int and_result = (a > 0 && b > 0); // 逻辑运算
int bitwise_or = (a | b); // 位运算
a += 2; // 赋值运算
```

#### 声明

声明用于向编译器介绍变量、函数或类型的存在。常见的声明包括：
- 变量声明: `int x;`
- 函数声明: `int add(int, int);`
- 结构体声明: `struct Point { int x, y; };`
- 联合体声明: `union Data { int i; float f; char str[20]; };`
- 枚举声明: `enum Color { RED, GREEN, BLUE };`

**示例**:
```c
#include <stdio.h>

// 结构体声明
struct Point {
    int x;
    int y;
};

// 枚举声明
enum Color {
    RED,
    GREEN,
    BLUE
};

// 函数声明
int add(int a, int b);

int main() {
    struct Point p1;
    enum Color myColor = GREEN;

    p1.x = 10;
    p1.y = 20;

    printf("Point coordinates: (%d, %d)\n", p1.x, p1.y);
    printf("Color value: %d\n", myColor);

    int result = add(5, 3);
    printf("Sum: %d\n", result);

    return 0;
}

// 函数定义
int add(int a, int b) {
    return a + b;
}
```

#### 初始化

初始化是在声明时给变量赋初始值的过程。可以使用多种方式初始化变量：
- 直接初始化: `int x = 10;`
- 复合初始化: `int arr[5] = {1, 2, 3, 4, 5};`
- 结构体初始化: `struct Point p = {10, 20};`
- 指针初始化: `int *ptr = NULL;`

**示例**:
```c
#include <stdio.h>

int main() {
    // 直接初始化
    int x = 10;

    // 复合初始化
    int arr[5] = {1, 2, 3, 4, 5};

    // 结构体初始化
    struct Point p = {10, 20};

    // 指针初始化
    int *ptr = NULL;

    printf("x: %d\n", x);
    for (int i = 0; i < 5; i++) {
        printf("arr[%d]: %d\n", i, arr[i]);
    }
    printf("Point coordinates: (%d, %d)\n", p.x, p.y);
    printf("Pointer value: %p\n", (void*)ptr);

    return 0;
}
```

#### 函数

函数是可重用的代码块，执行特定的任务。函数声明包括返回类型、函数名和参数列表。函数定义包括函数体。

**示例**:
```c
#include <stdio.h>

// 函数声明
int add(int a, int b);

int main() {
    int result = add(5, 3);
    printf("Sum: %d\n", result);
    return 0;
}

// 函数定义
int add(int a, int b) {
    return a + b;
}
```

#### 语句

语句是程序的基本执行单元。常见的语句包括:
- 表达式语句: `x = 10;`
- 复合语句: `{ int x = 10; x++; }`
- 控制流程语句: `if`, `switch`, `for`, `while`, `do-while`
- 跳转语句: `break`, `continue`, `return`, `goto`

**示例**:
```c
#include <stdio.h>

int main() {
    int x = 10;

    // 表达式语句
    x++;

    // 复合语句
    {
        int y = 5;
        y++;
        printf("y: %d\n", y);
    }

    // 控制流程语句
    if (x > 5) {
        printf("x is greater than 5\n");
    }

    switch (x) {
        case 10:
            printf("x is 10\n");
            break;
        default:
            printf("x is not 10\n");
            break;
    }

    // 跳转语句
    for (int i = 0; i < 5; i++) {
        if (i == 3) {
            continue;
        }
        printf("i: %d\n", i);
        if (i == 4) {
            break;
        }
    }

    return 0;
}
```

### 头文件（Headers）

头文件包含函数声明、宏定义、类型定义等。通过 `#include` 指令引入头文件。标准库头文件通常以 `.h` 为扩展名，用户定义的头文件也可以使用任意扩展名。

**示例**:
```c
#include <stdio.h> // 标准库头文件
#include "mylib.h" // 用户定义头文件
```

### 类型支持（Type support）

#### 基本数据类型

C 语言的基本数据类型包括:
- `int`: 整数类型，大小通常为 4 字节。
- `char`: 字符类型，大小通常为 1 字节。
- `float`: 单精度浮点数，大小通常为 4 字节。
- `double`: 双精度浮点数，大小通常为 8 字节。
- `void`: 表示无类型。

**示例**:
```c
#include <stdio.h>

int main() {
    int i = 10;
    char c = 'A';
    float f = 3.14;
    double d = 3.14159;
    void *v = NULL;

    printf("int: %d\n", i);
    printf("char: %c\n", c);
    printf("float: %f\n", f);
    printf("double: %lf\n", d);
    printf("void*: %p\n", v);

    return 0;
}
```

#### 枚举类型

枚举类型用于定义一组命名的整数常量。枚举类型的值默认从 0 开始递增。

**示例**:
```c
#include <stdio.h>

enum Color {
    RED,
    GREEN,
    BLUE
};

int main() {
    enum Color myColor = GREEN;

    printf("Color value: %d\n", myColor);

    return 0;
}
```

#### 结构体

结构体用于将不同类型的数据组合在一起。每个成员可以有不同的类型。

**示例**:
```c
#include <stdio.h>

struct Point {
    int x;
    int y;
};

int main() {
    struct Point p1;
    p1.x = 10;
    p1.y = 20;

    printf("Point coordinates: (%d, %d)\n", p1.x, p1.y);

    return 0;
}
```

#### 联合体

联合体类似于结构体，但所有成员共享同一块内存空间。联合体的大小等于其最大成员的大小。

**示例**:
```c
#include <stdio.h>

union Data {
    int i;
    float f;
    char str[20];
};

int main() {
    union Data data;

    data.i = 10;
    printf("data.i: %d\n", data.i);

    data.f = 220.5;
    printf("data.f: %f\n", data.f);

    strcpy(data.str, "C Programming");
    printf("data.str: %s\n", data.str);

    // 注意: 此时 data.i 和 data.f 的值已改变
    printf("data.i: %d\n", data.i);
    printf("data.f: %f\n", data.f);

    return 0;
}
```

### 程序工具（Program utilities）

#### 命令行参数

命令行参数允许用户在运行程序时传递参数。`main` 函数可以接受两个参数: `argc` 和 `argv`。

**示例**:
```c
#include <stdio.h>

int main(int argc, char *argv[]) {
    printf("Number of arguments: %d\n", argc);
    for (int i = 0; i < argc; i++) {
        printf("Argument %d: %s\n", i, argv[i]);
    }
    return 0;
}
```

#### 环境变量

环境变量是操作系统提供的全局变量，可以在程序中访问。使用 `getenv` 函数获取环境变量的值。

**示例**:
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    char *path = getenv("PATH");
    if (path != NULL) {
        printf("PATH: %s\n", path);
    } else {
        printf("PATH environment variable not found\n");
    }
    return 0;
}
```

#### 进程控制

进程控制函数允许程序创建、等待和终止子进程。常用的函数包括 `fork`, `wait`, `exec`.

**示例**:
```c
#include <stdio.h>
#include <unistd.h>
#include <sys/wait.h>

int main() {
    pid_t pid = fork();

    if (pid == 0) {
        // 子进程
        printf("Child process\n");
        execlp("/bin/ls", "ls", "-l", NULL);
    } else if (pid > 0) {
        // 父进程
        printf("Parent process, waiting for child to finish\n");
        wait(NULL);
        printf("Child process finished\n");
    } else {
        // 错误处理
        perror("fork");
    }

    return 0;
}
```

#### 时间与日期

时间与日期函数允许程序获取当前时间、格式化时间字符串等。常用的函数包括 `time`, `ctime`, `localtime`, `mktime`.

**示例**:
```c
#include <stdio.h>
#include <time.h>

int main() {
    time_t rawtime;
    struct tm *timeinfo;

    time(&rawtime);
    timeinfo = localtime(&rawtime);

    printf("Current local time and date: %s", asctime(timeinfo));

    timeinfo->tm_hour = 12;
    timeinfo->tm_min = 0;
    timeinfo->tm_sec = 0;
    time_t newtime = mktime(timeinfo);

    printf("New time: %s", asctime(localtime(&newtime)));

    return 0;
}
```

### 可变参数函数支持（Variadic functions）

可变参数函数允许函数接受任意数量和类型的参数。常用的宏包括 `va_list`, `va_start`, `va_arg`, `va_end`.

**示例**:
```c
#include <stdio.h>
#include <stdarg.h>

double average(int count, ...) {
    va_list args;
    double sum = 0;

    va_start(args, count);
    for (int i = 0; i < count; i++) {
        sum += va_arg(args, double);
    }
    va_end(args);

    return sum / count;
}

int main() {
    printf("Average: %f\n", average(3, 1.5, 2.5, 3.5));
    return 0;
}
```

### 诊断库（Diagnostics library）

诊断库提供了错误处理和调试功能。常用的函数包括 `perror`, `strerror`.

**示例**:
```c
#include <stdio.h>
#include <errno.h>
#include <string.h>

int main() {
    FILE *file = fopen("nonexistentfile.txt", "r");
    if (file == NULL) {
        perror("Error opening file");
        printf("Error number: %d\n", errno);
        printf("Error message: %s\n", strerror(errno));
    }
    return 0;
}
```

### 动态内存管理（Dynamic memory management）

动态内存管理允许程序在运行时分配和释放内存。常用的函数包括 `malloc`, `calloc`, `realloc`, `free`.

**示例**:
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n = 5;
    int *arr = (int *)malloc(n * sizeof(int));
    if (arr == NULL) {
        perror("Memory allocation failed");
        return 1;
    }

    for (int i = 0; i < n; i++) {
        arr[i] = i + 1;
    }

    printf("Array contents:\n");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    n = 10;
    arr = (int *)realloc(arr, n * sizeof(int));
    if (arr == NULL) {
        perror("Memory reallocation failed");
        return 1;
    }

    for (int i = 5; i < n; i++) {
        arr[i] = i + 1;
    }

    printf("Resized array contents:\n");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    free(arr);
    return 0;
}
```

### 字符串库（Strings library）

#### 空字符结尾字符串

空字符结尾字符串是以空字符 (`\0`) 结尾的字符数组。常用的函数包括 `strlen`, `strcpy`, `strcat`, `strcmp`.

**示例**:
```c
#include <stdio.h>
#include <string.h>

int main() {
    char src[] = "Hello";
    char dest[20];

    strcpy(dest, src);
    strcat(dest, " World");

    printf("Source: %s\n", src);
    printf("Destination: %s\n", dest);
    printf("Length of destination: %lu\n", strlen(dest));
    printf("Comparison: %d\n", strcmp(src, dest));

    return 0;
}
```

#### 单字节字符（byte）

单字节字符是指占用一个字节的字符。常用字符集包括 ASCII 和扩展 ASCII.

**示例**:
```c
#include <stdio.h>

int main() {
    char ch = 'A';
    printf("Character: %c\n", ch);
    printf("ASCII value: %d\n", ch);
    return 0;
}
```

#### 多字节字符（multibyte）

多字节字符是指占用多个字节的字符。常用的编码包括 UTF-8 和 GBK.

**示例**:
```c
#include <stdio.h>
#include <wchar.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "");

    wchar_t wch = L'汉';
    printf("Wide character: %lc\n", wch);

    char mbch[10];
    wcstombs(mbch, &wch, sizeof(mbch));
    printf("Multibyte character: %s\n", mbch);

    return 0;
}
```

#### 宽字符（wide）

宽字符是指占用多个字节的字符类型 `wchar_t`. 常用函数包括 `wcslen`, `wcscpy`, `wcscat`, `wcscmp`.

**示例**:
```c
#include <stdio.h>
#include <wchar.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "");

    wchar_t src[] = L"你好";
    wchar_t dest[20];

    wcscpy(dest, src);
    wcscat(dest, L"世界");

    printf("Source: %ls\n", src);
    printf("Destination: %ls\n", dest);
    printf("Length of destination: %lu\n", wcslen(dest));
    printf("Comparison: %d\n", wcscmp(src, dest));

    return 0;
}
```

### 日期与时间库（Date and time library）

日期与时间库提供了处理日期和时间的函数。常用的函数包括 `time`, `ctime`, `localtime`, `mktime`.

**示例**:
```c
#include <stdio.h>
#include <time.h>

int main() {
    time_t rawtime;
    struct tm *timeinfo;

    time(&rawtime);
    timeinfo = localtime(&rawtime);

    printf("Current local time and date: %s", asctime(timeinfo));

    timeinfo->tm_hour = 12;
    timeinfo->tm_min = 0;
    timeinfo->tm_sec = 0;
    time_t newtime = mktime(timeinfo);

    printf("New time: %s", asctime(localtime(&newtime)));

    return 0;
}
```

### 本地化库（Localization library）

本地化库提供了处理不同语言和地区设置的功能。常用的函数包括 `setlocale`, `localeconv`.

**示例**:
```c
#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "");

    printf("Currency symbol: %s\n", localeconv()->currency_symbol);
    printf("Decimal point: %c\n", localeconv()->decimal_point);
    printf("Thousands separator: %c\n", localeconv()->thousands_sep);

    return 0;
}
```

### 输入/输出库（Input/output library）

输入/输出库提供了处理输入和输出的功能。常用的函数包括 `printf`, `scanf`, `fopen`, `fclose`, `fprintf`, `fscanf`.

**示例**:
```c
#include <stdio.h>

int main() {
    // 标准输入输出
    printf("Enter your name: ");
    char name[50];
    scanf("%s", name);
    printf("Hello, %s!\n", name);

    // 文件输入输出
    FILE *file = fopen("example.txt", "w");
    if (file == NULL) {
        perror("Error opening file");
        return 1;
    }

    fprintf(file, "This is a test file.\n");
    fclose(file);

    file = fopen("example.txt", "r");
    if (file == NULL) {
        perror("Error opening file");
        return 1;
    }

    char buffer[100];
    while (fgets(buffer, sizeof(buffer), file) != NULL) {
        printf("File content: %s", buffer);
    }
    fclose(file);

    return 0;
}
```

### 算法库（Algorithms library）

算法库提供了通用的算法函数。常用的函数包括 `qsort`, `bsearch`.

**示例**:
```c
#include <stdio.h>
#include <stdlib.h>

// 比较函数
int compare(const void *a, const void *b) {
    return (*(int*)a - *(int*)b);
}

int main() {
    int arr[] = {5, 3, 8, 6, 2};
    int n = sizeof(arr) / sizeof(arr[0]);

    // 排序
    qsort(arr, n, sizeof(int), compare);

    printf("Sorted array: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    // 查找
    int key = 6;
    int *result = (int*)bsearch(&key, arr, n, sizeof(int), compare);
    if (result != NULL) {
        printf("Found %d at index %ld\n", key, result - arr);
    } else {
        printf("%d not found\n", key);
    }

    return 0;
}
```

### 数值计算库（Numerics library）

#### 常用数学函数

数值计算库提供了各种数学函数。常用的函数包括 `sin`, `cos`, `tan`, `exp`, `log`, `sqrt`.

**示例**:
```c
#include <stdio.h>
#include <math.h>

int main() {
    double x = 2.0;

    printf("sin(%f): %f\n", x, sin(x));
    printf("cos(%f): %f\n", x, cos(x));
    printf("tan(%f): %f\n", x, tan(x));
    printf("exp(%f): %f\n", x, exp(x));
    printf("log(%f): %f\n", x, log(x));
    printf("sqrt(%f): %f\n", x, sqrt(x));

    return 0;
}
```

#### 浮点环境（C99 起）

浮点环境提供了处理浮点异常和舍入模式的功能。常用的函数包括 `feclearexcept`, `fegetround`, `fesetround`.

**示例**:
```c
#include <stdio.h>
#include <fenv.h>
#include <math.h>

int main() {
    // 清除所有浮点异常
    feclearexcept(FE_ALL_EXCEPT);

    // 计算除零
    double result = 1.0 / 0.0;

    // 检查是否发生除零异常
    if (fetestexcept(FE_DIVBYZERO)) {
        printf("Division by zero occurred\n");
    }

    // 获取当前舍入模式
    int rounding_mode = fegetround();
    switch (rounding_mode) {
        case FE_DOWNWARD:
            printf("Rounding mode: DOWNWARD\n");
            break;
        case FE_TONEAREST:
            printf("Rounding mode: TO_NEAREST\n");
            break;
        case FE_TOWARDZERO:
            printf("Rounding mode: TOWARD_ZERO\n");
            break;
        case FE_UPWARD:
            printf("Rounding mode: UPWARD\n");
            break;
        default:
            printf("Unknown rounding mode\n");
            break;
    }

    // 设置新的舍入模式
    fesetround(FE_DOWNWARD);
    printf("New rounding mode: DOWNWARD\n");

    return 0;
}
```

#### 伪随机数生成

伪随机数生成提供了生成伪随机数的功能。常用的函数包括 `rand`, `srand`.

**示例**:
```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    // 使用当前时间作为种子
    srand(time(NULL));

    // 生成随机数
    for (int i = 0; i < 5; i++) {
        int random_number = rand();
        printf("Random number %d: %d\n", i, random_number);
    }

    return 0;
}
```

#### 复数运算（C99 起）

复数运算提供了处理复数的功能。常用的类型和函数包括 `complex`, `creal`, `cimag`, `cabs`.

**示例**:
```c
#include <stdio.h>
#include <complex.h>
#include <math.h>

int main() {
    double complex z1 = 1.0 + 2.0*I;
    double complex z2 = 3.0 - 4.0*I;

    double complex z3 = z1 + z2;
    printf("z1 + z2 = %.2f + %.2fi\n", creal(z3), cimag(z3));

    double complex z4 = z1 * z2;
    printf("z1 * z2 = %.2f + %.2fi\n", creal(z4), cimag(z4));

    double complex z5 = cpow(z1, z2);
    printf("z1 ^ z2 = %.2f + %.2fi\n", creal(z5), cimag(z5));

    double abs_z1 = cabs(z1);
    printf("|z1| = %.2f\n", abs_z1);

    double complex z6 = csqrt(z1);
    printf("sqrt(z1) = %.2f + %.2fi\n", creal(z6), cimag(z6));

    return 0;
}
```

#### 类型泛型数学宏（C99 起）

类型泛型数学宏提供了类型无关的数学函数。常用的宏包括 `_Generic`, `_Complex`.

**示例**:
```c
#include <stdio.h>
#include <tgmath.h>

int main() {
    int i = 2;
    double d = 2.0;
    float f = 2.0f;

    printf("sqrt(%d) = %.2f\n", i, sqrt(i));
    printf("sqrt(%f) = %.2f\n", d, sqrt(d));
    printf("sqrt(%f) = %.2f\n", f, sqrt(f));

    double complex z = 2.0 + 3.0*I;
    double complex z_sqrt = sqrt(z);
    printf("sqrt(%.2f + %.2fi) = %.2f + %.2fi\n", creal(z), cimag(z), creal(z_sqrt), cimag(z_sqrt));

    return 0;
}
```

#### 位操作（C23 起）

位操作提供了对位进行操作的功能。常用的函数包括 `bitand`, `bitor`, `bitxor`, `compl`.

**示例**:
```c
#include <stdio.h>

int main() {
    unsigned int a = 0b1100;
    unsigned int b = 0b1010;

    unsigned int and_result = a bitand b;
    unsigned int or_result = a bitor b;
    unsigned int xor_result = a bitxor b;
    unsigned int compl_result = compl a;

    printf("a: %u\n", a);
    printf("b: %u\n", b);
    printf("a bitand b: %u\n", and_result);
    printf("a bitor b: %u\n", or_result);
    printf("a bitxor b: %u\n", xor_result);
    printf("compl a: %u\n", compl_result);

    return 0;
}
```

#### 检查型整数算术（Checked integer arithmetic，C23 起）

检查型整数算术提供了对整数运算进行边界检查的功能。常用的类型包括 `checked int`, `checked long`.

**示例**:
```c
#include <stdio.h>
#include <stdckdint.h>

int main() {
    checked int a = 10;
    checked int b = 20;
    checked int sum;
    int err = ckd_add(&sum, a, b);

    if (err == 0) {
        printf("Sum: %d\n", sum);
    } else {
        printf("Overflow occurred\n");
    }

    return 0;
}
```

### 并发支持库（Concurrency support library，C11 起）

#### 原子操作

原子操作提供了对共享数据进行原子操作的功能。常用的类型包括 `_Atomic`.

**示例**:
```c
#include <stdio.h>
#include <threads.h>
#include <stdatomic.h>

_Atomic int counter = 0;

int thread_func(void *arg) {
    for (int i = 0; i < 100000; i++) {
        atomic_fetch_add(&counter, 1);
    }
    return 0;
}

int main() {
    thrd_t threads[10];

    for (int i = 0; i < 10; i++) {
        thrd_create(&threads[i], thread_func, NULL);
    }

    for (int i = 0; i < 10; i++) {
        thrd_join(threads[i], NULL);
    }

    printf("Counter: %d\n", counter);

    return 0;
}
```

#### 互斥锁

互斥锁提供了对共享资源进行同步的功能。常用的类型包括 `mtx_t`.

**示例**:
```c
#include <stdio.h>
#include <threads.h>

mtx_t mutex;
int shared_data = 0;

int thread_func(void *arg) {
    mtx_lock(&mutex);
    for (int i = 0; i < 100000; i++) {
        shared_data++;
    }
    mtx_unlock(&mutex);
    return 0;
}

int main() {
    thrd_t threads[10];

    mtx_init(&mutex, mtx_plain);

    for (int i = 0; i < 10; i++) {
        thrd_create(&threads[i], thread_func, NULL);
    }

    for (int i = 0; i < 10; i++) {
        thrd_join(threads[i], NULL);
    }

    mtx_destroy(&mutex);

    printf("Shared data: %d\n", shared_data);

    return 0;
}
```

#### 条件变量

条件变量提供了线程间的同步机制。常用的类型包括 `cnd_t`.

**示例**:
```c
#include <stdio.h>
#include <threads.h>

mtx_t mutex;
cnd_t condition;
int ready = 0;

int producer_func(void *arg) {
    mtx_lock(&mutex);
    ready = 1;
    cnd_signal(&condition);
    mtx_unlock(&mutex);
    return 0;
}

int consumer_func(void *arg) {
    mtx_lock(&mutex);
    while (!ready) {
        cnd_wait(&condition, &mutex);
    }
    printf("Data is ready\n");
    mtx_unlock(&mutex);
    return 0;
}

int main() {
    thrd_t producer, consumer;

    mtx_init(&mutex, mtx_plain);
    cnd_init(&condition);

    thrd_create(&producer, producer_func, NULL);
    thrd_create(&consumer, consumer_func, NULL);

    thrd_join(producer, NULL);
    thrd_join(consumer, NULL);

    mtx_destroy(&mutex);
    cnd_destroy(&condition);

    return 0;
}
```

#### 线程

线程提供了并发执行的功能。常用的类型包括 `thrd_t`.

**示例**:
```c
#include <stdio.h>
#include <threads.h>

int thread_func(void *arg) {
    int id = *(int *)arg;
    printf("Thread %d is running\n", id);
    return 0;
}

int main() {
    thrd_t threads[5];
    int ids[5];

    for (int i = 0; i < 5; i++) {
        ids[i] = i;
        thrd_create(&threads[i], thread_func, &ids[i]);
    }

    for (int i = 0; i < 5; i++) {
        thrd_join(threads[i], NULL);
    }

    printf("All threads have finished\n");

    return 0;
}
```

---

## 技术规范（Technical Specifications）

### 动态内存扩展（Dynamic memory extensions，动态内存 TR）

动态内存扩展提供了对动态内存管理的扩展功能。常用的函数包括 `aligned_alloc`, `malloc_usable_size`.

**示例**:
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    size_t alignment = 16;
    size_t size = 100;

    void *ptr = aligned_alloc(alignment, size);
    if (ptr == NULL) {
        perror("aligned_alloc");
        return 1;
    }

    size_t usable_size = malloc_usable_size(ptr);
    printf("Usable size: %zu\n", usable_size);

    free(ptr);

    return 0;
}
```

### 浮点扩展，第一部分（Floating-point extensions, Part 1，FP Ext 1 TS）

浮点扩展提供了对浮点运算的扩展功能。常用的函数包括 `nextafter`, `remainder`.

**示例**:
```c
#include <stdio.h>
#include <