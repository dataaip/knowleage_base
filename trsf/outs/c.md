### C 语言参考

摘自 [cppreference.com](https://en.cppreference.com/mwiki/index.php?title=c&oldid=94077)

## C 语言

### 核心分类

#### 编译器支持
编译器支持是指不同版本的 C 语言标准（如 C89、C95、C99、C11、C17、C23）在编译器中的实现情况。例如，GCC 和 Clang 是广泛使用的 C 语言编译器，它们都支持从 C99 到最新的 C23 标准。开发者可以根据项目需求选择合适的 C 标准版本进行开发。

#### 语言特性
语言特性包括基础概念、关键字、预处理器、表达式、声明、初始化、函数、语句等。这些特性共同构成了 C 语言的核心语法。

- **基础概念**：包括变量、常量、数据类型等基本编程元素。
- **关键字**：如 `int`, `char`, `if`, `else`, `for`, `while` 等，用于定义程序结构。
- **预处理器**：使用 `#include`, `#define`, `#ifdef` 等指令进行代码预处理。
- **表达式**：如算术表达式、逻辑表达式等，用于执行计算或逻辑判断。
- **声明**：定义变量、函数等的类型和名称。
- **初始化**：为变量赋予初始值。
- **函数**：封装代码块，可重复调用。
- **语句**：包括控制流程语句（如 `if`, `switch`, `for`, `while`）、跳转语句（如 `break`, `continue`, `return`）等。

**示例**：
```c
#include <stdio.h>

int main() {
    int a = 5; // 声明并初始化变量
    if (a > 0) { // 控制流程语句
        printf("a is positive\n");
    }
    return 0;
}
```

#### 头文件
头文件包含函数声明、宏定义、类型定义等，供源文件包含使用。常见的头文件有 `<stdio.h>`、`<stdlib.h>`、`<string.h>` 等。

**示例**：
```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n"); // 使用 stdio.h 中的 printf 函数
    return 0;
}
```

#### 类型支持
C 语言支持多种数据类型，包括基本数据类型（如 `int`, `char`, `float`, `double`）和复合数据类型（如结构体、联合体、枚举）。此外，还支持指针类型和数组类型。

**示例**：
```c
#include <stdio.h>

struct Point {
    int x;
    int y;
};

int main() {
    struct Point p1 = {10, 20};
    printf("Point coordinates: (%d, %d)\n", p1.x, p1.y);
    return 0;
}
```

#### 程序工具
程序工具包括标准库中提供的实用函数和宏，用于辅助程序开发。常见的工具包括内存管理、字符串处理、文件操作等。

**示例**：
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    char str[] = "Hello, World!";
    char *copy = malloc(strlen(str) + 1); // 动态内存分配
    strcpy(copy, str); // 字符串复制
    printf("Copied string: %s\n", copy);
    free(copy); // 释放内存
    return 0;
}
```

#### 可变参数函数
可变参数函数允许函数接受可变数量和类型的参数。C 标准库中的 `printf` 和 `scanf` 就是典型的可变参数函数。

**示例**：
```c
#include <stdio.h>
#include <stdarg.h>

void print_numbers(int count, ...) {
    va_list args;
    va_start(args, count);
    for (int i = 0; i < count; i++) {
        int num = va_arg(args, int);
        printf("%d ", num);
    }
    va_end(args);
    printf("\n");
}

int main() {
    print_numbers(3, 1, 2, 3); // 输出: 1 2 3
    return 0;
}
```

#### 错误处理
C 语言没有内置的异常处理机制，但可以通过返回值、全局变量（如 `errno`）和自定义错误处理函数来实现错误处理。

**示例**：
```c
#include <stdio.h>
#include <errno.h>
#include <string.h>

int divide(int numerator, int denominator) {
    if (denominator == 0) {
        errno = EINVAL; // 设置错误码
        return -1;
    }
    return numerator / denominator;
}

int main() {
    int result = divide(10, 0);
    if (result == -1 && errno != 0) {
        fprintf(stderr, "Error: %s\n", strerror(errno)); // 输出错误信息
    }
    return 0;
}
```

#### 动态内存管理
动态内存管理允许程序在运行时分配和释放内存。常用函数包括 `malloc`, `calloc`, `realloc`, `free`。

**示例**：
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n = 5;
    int *arr = (int *)malloc(n * sizeof(int)); // 分配内存
    if (arr == NULL) {
        fprintf(stderr, "Memory allocation failed\n");
        return 1;
    }
    for (int i = 0; i < n; i++) {
        arr[i] = i * 10;
    }
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
    free(arr); // 释放内存
    return 0;
}
```

#### 字符串库
字符串库提供了处理空终止字符串的函数，包括字节字符串、多字节字符串和宽字符串。

**示例**：
```c
#include <stdio.h>
#include <string.h>

int main() {
    char src[] = "Hello";
    char dest[10];
    strcpy(dest, src); // 字符串复制
    printf("Copied string: %s\n", dest);
    return 0;
}
```

#### 算法库
C 标准库并没有专门的算法库，但提供了许多常用的数学函数和工具，如 `<math.h>` 提供的数学运算函数。

**示例**：
```c
#include <stdio.h>
#include <math.h>

int main() {
    double x = 2.0;
    double result = pow(x, 3); // 计算 x 的立方
    printf("2^3 = %f\n", result);
    return 0;
}
```

#### 数值计算
数值计算库提供了一系列数学运算函数，包括基本算术运算、三角函数、对数函数等。`<math.h>` 头文件包含了这些函数。

**示例**：
```c
#include <stdio.h>
#include <math.h>

int main() {
    double angle = M_PI / 4; // 45 度
    double sin_value = sin(angle);
    printf("sin(45 degrees) = %f\n", sin_value);
    return 0;
}
```

#### 日期时间工具
日期时间工具提供了处理日期和时间的函数，如 `<time.h>` 提供的时间操作函数。

**示例**：
```c
#include <stdio.h>
#include <time.h>

int main() {
    time_t rawtime;
    struct tm * timeinfo;

    time(&rawtime);
    timeinfo = localtime(&rawtime);

    printf("Current local time and date: %s", asctime(timeinfo));
    return 0;
}
```

#### 输入/输出支持
输入/输出支持包括文件操作和标准输入输出函数，如 `<stdio.h>` 提供的文件操作函数。

**示例**：
```c
#include <stdio.h>

int main() {
    FILE *file = fopen("example.txt", "w");
    if (file == NULL) {
        perror("Error opening file");
        return 1;
    }
    fprintf(file, "Hello, World!\n");
    fclose(file);
    return 0;
}
```

#### 本地化支持
本地化支持提供了处理不同语言和地区设置的函数，如 `<locale.h>` 提供的本地化函数。

**示例**：
```c
#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "en_US.UTF-8");
    printf("Locale set to en_US.UTF-8\n");
    return 0;
}
```

#### 并发支持 (C11)
C11 引入了多线程支持，包括线程创建、同步原语等。`<threads.h>` 头文件提供了这些功能。

**示例**：
```c
#include <stdio.h>
#include <threads.h>

int thread_func(void *arg) {
    int *num = (int *)arg;
    printf("Thread number: %d\n", *num);
    return 0;
}

int main() {
    thrd_t threads[5];
    int numbers[5] = {1, 2, 3, 4, 5};

    for (int i = 0; i < 5; i++) {
        thrd_create(&threads[i], thread_func, &numbers[i]);
    }

    for (int i = 0; i < 5; i++) {
        thrd_join(threads[i], NULL);
    }

    return 0;
}
```

#### 技术规范
技术规范提供了对 C 语言标准的补充和扩展，包括动态内存扩展、浮点扩展等。

- **动态内存扩展**（动态内存技术报告）
- **浮点扩展 Part 1**（FP Ext 1 技术规范）
- **浮点扩展 Part 4**（FP Ext 4 技术规范）

#### 符号索引
符号索引列出了标准库中的所有符号，方便开发者查找和使用。

### 标准版本与编译器支持

| 标准版本          | 语言特性分类                                                                                                                                                                                                                             | 库功能分类                                                                                                                                                                                                                                   |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| C89、C95、C99、C11、C17、C23 | **语言特性**<br>• 基础概念<br>• 关键字<br>• 预处理器<br>• 表达式<br>• 声明<br>• 初始化<br>• 函数<br>• 语句<br><br>**头文件**<br><br>**类型支持**                                                                                         | **程序工具**<br><br>**可变参数函数**<br><br>**诊断库**<br><br>**动态内存管理**<br><br>**字符串库**<br>• 空终止字符串：<br>   - 字节字符串<br>   - 多字节字符串<br>   - 宽字符串<br><br>**日期时间库**<br><br>**本地化库**<br><br>**输入/输出库** |
|                     | **算法库**<br><br>**数值计算库**<br>• 常用数学函数<br>• 浮点环境 (C99)<br>• 伪随机数生成<br>• 复数运算 (C99)<br>• 泛型数学 (C99)<br>• 位操作 (C23)<br>• 受检整数运算 (C23)<br><br>**并发支持库 (C11)**                                                                                       |                                                                                                                                                                                                                                            |

### 技术规范

| 技术规范                                                                 |
| ------------------------------------------------------------------------ |
| **动态内存扩展**（动态内存技术报告）                                     |
| **浮点扩展 Part 1**（FP Ext 1 技术规范）                                 |
| **浮点扩展 Part 4**（FP Ext 4 技术规范）                                 |

### 外部链接

- **在线版本**  
- **离线版本**（获取于 2025-02-09 16:39）  
- 本页面最后修改于 2017年7月3日 20:56 (UTC+8)

---

通过以上扩展和优化，文档变得更加详细、规范和易于阅读，涵盖了 C 语言的核心概念和技术细节。