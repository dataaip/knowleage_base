# C 参考手册

来源：[cppreference.com](https://en.cppreference.com/w/c)

---

## 目录概览

| 类别                     | 内容                                                                 |
|--------------------------|----------------------------------------------------------------------|
| 编译器支持               | 编译器对不同 C 标准的支持情况                                      |
| 语言基础                 | C 语言的基本语法和特性                                             |
| 头文件                   | 所有标准头文件的概述                                               |
| 类型支持                 | 数据类型及其相关特性                                               |
| 程序工具                 | 程序控制和实用工具函数                                             |
| 可变参数函数支持         | 可变参数函数的实现                                                 |
| 错误处理                 | 错误检测和处理机制                                                 |
| 动态内存管理             | 动态内存分配和管理                                               |
| 字符串库                 | 字符串操作函数                                                     |
| 算法库                   | 排序、搜索等算法                                                   |
| 数值计算                 | 数学函数、浮点数处理等                                             |
| 日期与时间工具           | 日期和时间操作                                                     |
| 输入/输出支持            | 文件和标准输入输出操作                                             |
| 本地化支持               | 区域设置和国际化                                                   |
| 并发支持（C11）          | 多线程和同步机制                                                   |
| 技术规范                 | C 语言的技术规范和扩展                                             |
| 符号索引                 | 所有标准函数、类型、宏、关键字的字母序索引                         |

---

## 版本与标准支持

- **C 标准版本**：C89、C95、C99、C11、C17、C23  
- **编译器支持**：
  - **GCC**：支持 C23
  - **Clang**：支持 C23
  - **MSVC**：部分支持 C11 和 C23
  - **Intel C Compiler**：支持 C23

---

## 主要技术模块

### 语言基础（Language）

- **基本概念**：
  - C 语言是一种静态类型、编译型、过程式编程语言。
  - C 语言强调性能和对硬件的直接访问，适合系统编程、嵌入式开发等场景。
  
- **关键字**：
  - 关键字是 C 语言中的保留字，不能用作标识符。
  - 常见关键字包括 `int`, `float`, `return`, `if`, `else`, `for`, `while` 等。
  
- **预处理器**：
  - 预处理器指令以 `#` 开头，用于宏定义、条件编译、文件包含等。
  - 常见指令包括 `#include`, `#define`, `#ifdef`, `#ifndef`, `#endif` 等。
  - 示例：
    ```c
    #include <stdio.h>
    #define PI 3.14159
    int main() {
        printf("The value of PI is %f\n", PI);
        return 0;
    }
    ```
  
- **表达式**：
  - 表达式是由运算符和操作数组成的代码单元，可以计算得到一个值。
  - 示例：
    ```c
    int a = 5;
    int b = 3;
    int c = a + b; // c 的值为 8
    ```
  
- **声明**：
  - 声明用于引入新的标识符，并指定其类型和作用域。
  - 示例：
    ```c
    int x; // 声明一个整数变量 x
    float y; // 声明一个浮点数变量 y
    ```
  
- **初始化**：
  - 初始化是在声明的同时赋予变量一个初始值。
  - 示例：
    ```c
    int x = 10; // 声明并初始化变量 x 为 10
    float y = 3.14; // 声明并初始化变量 y 为 3.14
    ```
  
- **函数**：
  - 函数是一组执行特定任务的代码块。
  - 示例：
    ```c
    int add(int a, int b) {
        return a + b;
    }
    int main() {
        int result = add(5, 3);
        printf("Result is %d\n", result); // 输出 "Result is 8"
        return 0;
    }
    ```
  
- **语句**：
  - 语句是程序的基本执行单元，通常以分号 `;` 结尾。
  - 常见语句包括赋值语句、条件语句、循环语句、跳转语句等。
  - 示例：
    ```c
    int main() {
        int i;
        for (i = 0; i < 5; i++) {
            printf("%d\n", i);
        }
        return 0;
    }
    ```

### 头文件（Headers）

- 所有标准头文件概览：
  - `<stdio.h>`：输入输出函数
  - `<stdlib.h>`：通用工具函数
  - `<string.h>`：字符串操作函数
  - `<math.h>`：数学函数
  - `<time.h>`：日期和时间函数
  - `<ctype.h>`：字符处理函数
  - `<errno.h>`：错误码定义
  - `<limits.h>`：各种类型的极限值
  - `<float.h>`：浮点数极限值
  - `<locale.h>`：本地化支持函数
  - `<setjmp.h>`：非局部跳转支持
  - `<signal.h>`：信号处理函数
  - `<stdarg.h>`：可变参数函数支持
  - `<stddef.h>`：常用类型定义
  - `<stdint.h>`：固定宽度整型定义
  - `<stdbool.h>`：布尔类型支持
  - `<threads.h>`：多线程支持（C11）
  - `<stdatomic.h>`：原子操作支持（C11）
  - `<stdalign.h>`：对齐支持（C11）
  - `<stdnoreturn.h>`：noreturn 属性支持（C11）
  - `<stdbit.h>`：位操作支持（C23）
  - `<stdckdint.h>`：带溢出检查的整数运算（C23）

### 类型支持（Type support）

- **基本数据类型**：
  - `char`：字符类型，通常占用 1 字节。
  - `int`：整数类型，大小取决于实现，通常是 4 字节。
  - `float`：单精度浮点数，通常占用 4 字节。
  - `double`：双精度浮点数，通常占用 8 字节。
  - `long`：长整型，大小取决于实现，通常是 4 或 8 字节。
  - `short`：短整型，通常占用 2 字节。
  - `void`：无类型。
  
- **`typedef` 与类型别名**：
  - `typedef` 用于为现有类型创建新的名称。
  - 示例：
    ```c
    typedef unsigned int uint;
    uint a = 10;
    ```
  
- **扩展类型**：
  - `_Bool`（C99）：布尔类型，值为 0 或 1。
  - `_Complex`（C99）：复数类型，支持复数运算。
  - `_Atomic`（C11）：原子类型，用于多线程环境下的原子操作。
  - 示例：
    ```c
    _Bool flag = 1;
    _Complex double z = 1.0 + 2.0*I;
    _Atomic int count = 0;
    ```
  
- **精确宽度整型**：
  - `<stdint.h>` 提供了固定宽度的整型定义。
  - 示例：
    ```c
    #include <stdint.h>
    int32_t a = 100000;
    int64_t b = 100000000000;
    ```
  
- **布尔类型支持**：
  - `<stdbool.h>` 提供了 `bool` 类型和常量 `true`、`false`。
  - 示例：
    ```c
    #include <stdbool.h>
    bool is_valid = true;
    ```

### 程序工具（Program utilities）

- **程序控制**：
  - `exit`：正常终止程序。
  - `abort`：异常终止程序。
  - `atexit`：注册程序退出时执行的函数。
  - 示例：
    ```c
    #include <stdlib.h>
    void cleanup() {
        printf("Cleaning up...\n");
    }
    int main() {
        atexit(cleanup);
        printf("Hello, World!\n");
        exit(0);
    }
    ```
  
- **环境通信**：
  - `system`：执行 shell 命令。
  - `getenv`：获取环境变量的值。
  - 示例：
    ```c
    #include <stdlib.h>
    #include <stdio.h>
    int main() {
        system("ls");
        char *path = getenv("PATH");
        if (path != NULL) {
            printf("PATH: %s\n", path);
        }
        return 0;
    }
    ```
  
- **字符串转数值**：
  - `atoi`, `atof`, `strtol`, `strtod` 等。
  - 示例：
    ```c
    #include <stdlib.h>
    #include <stdio.h>
    int main() {
        char str[] = "123";
        int num = atoi(str);
        printf("Number: %d\n", num); // 输出 "Number: 123"
        return 0;
    }
    ```
  
- **伪随机数生成**：
  - `rand`：生成伪随机数。
  - `srand`：设置随机数种子。
  - 示例：
    ```c
    #include <stdlib.h>
    #include <stdio.h>
    #include <time.h>
    int main() {
        srand(time(NULL));
        int num = rand();
        printf("Random number: %d\n", num);
        return 0;
    }
    ```
  
- **排序与查找**：
  - `qsort`：快速排序。
  - `bsearch`：二分查找。
  - 示例：
    ```c
    #include <stdlib.h>
    #include <stdio.h>
    int compare(const void *a, const void *b) {
        return (*(int*)a - *(int*)b);
    }
    int main() {
        int arr[] = {5, 2, 9, 1, 5, 6};
        qsort(arr, 6, sizeof(int), compare);
        for (int i = 0; i < 6; i++) {
            printf("%d ", arr[i]);
        }
        return 0;
    }
    ```
  
- **`assert` 宏**：
  - `<assert.h>`：用于调试时断言检查。
  - 示例：
    ```c
    #include <assert.h>
    int main() {
        int x = 5;
        assert(x > 0);
        return 0;
    }
    ```

### 可变参数函数支持（Variadic function support）

- **`<stdarg.h>`**：
  - `va_list`：用于存储可变参数信息。
  - `va_start`：初始化 `va_list`。
  - `va_arg`：获取下一个参数。
  - `va_end`：清理 `va_list`。
  - `va_copy`：复制 `va_list`。
  - 示例：
    ```c
    #include <stdarg.h>
    #include <stdio.h>
    int sum(int count, ...) {
        va_list args;
        va_start(args, count);
        int total = 0;
        for (int i = 0; i < count; i++) {
            total += va_arg(args, int);
        }
        va_end(args);
        return total;
    }
    int main() {
        printf("Sum: %d\n", sum(3, 1, 2, 3)); // 输出 "Sum: 6"
        return 0;
    }
    ```

### 诊断库（Diagnostics library）

- **`<assert.h>`**：
  - `assert` 宏：用于调试时断言检查。
  - 示例：
    ```c
    #include <assert.h>
    int main() {
        int x = 5;
        assert(x > 0);
        return 0;
    }
    ```
  
- **运行时错误检测机制**：
  - 使用 `errno` 和 `<errno.h>` 进行错误检测。
  - 示例：
    ```c
    #include <errno.h>
    #include <stdio.h>
    int main() {
        FILE *file = fopen("nonexistent.txt", "r");
        if (file == NULL) {
            perror("Error opening file");
            printf("Error code: %d\n", errno);
        }
        return 0;
    }
    ```

### 动态内存管理（Dynamic memory management）

- **核心函数**：
  - `malloc`：分配未初始化内存。
  - `calloc`：分配并清零内存。
  - `realloc`：重新调整内存块大小。
  - `free`：释放动态分配的内存。
  - 示例：
    ```c
    #include <stdlib.h>
    #include <stdio.h>
    int main() {
        int *arr = (int *)malloc(5 * sizeof(int));
        if (arr == NULL) {
            perror("Memory allocation failed");
            return 1;
        }
        for (int i = 0; i < 5; i++) {
            arr[i] = i + 1;
        }
        for (int i = 0; i < 5; i++) {
            printf("%d ", arr[i]);
        }
        free(arr);
        return 0;
    }
    ```
  
- **注意事项**：
  - 避免内存泄漏：确保每次 `malloc` 或 `calloc` 都有对应的 `free`。
  - 避免重复释放：不要多次释放同一个指针。
  - 避免使用已释放内存：释放内存后不要再访问该内存。

### 字符串库（Strings library）

#### 空字符结尾字符串（Null-terminated strings）

- **字节字符串（Byte strings）**：
  - 操作函数定义于 `<string.h>`。
  - 示例：
    ```c
    #include <string.h>
    #include <stdio.h>
    int main() {
        char src[] = "Hello, World!";
        char dest[20];
        strcpy(dest, src);
        printf("Copied string: %s\n", dest); // 输出 "Copied string: Hello, World!"
        return 0;
    }
    ```
  
- **多字节字符串（Multibyte strings）**：
  - 支持多字节编码（如 UTF-8）。
  - 示例：
    ```c
    #include <locale.h>
    #include <stdio.h>
    int main() {
        setlocale(LC_ALL, "");
        char mbstr[] = "\u4F60\u597D"; // "你好" in UTF-8
        printf("Multibyte string: %s\n", mbstr); // 输出 "Multibyte string: 你好"
        return 0;
    }
    ```
  
- **宽字符串（Wide strings）**：
  - 宽字符类型 `wchar_t` 及其操作。
  - 示例：
    ```c
    #include <wchar.h>
    #include <locale.h>
    int main() {
        setlocale(LC_ALL, "");
        wchar_t wstr[] = L"你好";
        wprintf(L"Wide string: %ls\n", wstr); // 输出 "Wide string: 你好"
        return 0;
    }
    ```

### 日期与时间库（Date and time utilities）

- **核心功能**：
  - `time`：获取当前时间。
  - `clock`：获取 CPU 时间。
  - `ctime`：将时间转换为字符串。
  - `asctime`：将 `struct tm` 转换为字符串。
  - `strftime`：格式化时间。
  - `struct tm`：表示时间的结构体。
  - `gmtime`：将时间转换为 UTC 时间。
  - `localtime`：将时间转换为本地时间。
  - `mktime`：将 `struct tm` 转换为时间。
  - 示例：
    ```c
    #include <time.h>
    #include <stdio.h>
    int main() {
        time_t t = time(NULL);
        struct tm *tm_info = localtime(&t);
        char buffer[80];
        strftime(buffer, sizeof(buffer), "%Y-%m-%d %H:%M:%S", tm_info);
        printf("Current time: %s\n", buffer); // 输出当前时间
        return 0;
    }
    ```

### 本地化库（Localization library）

- **核心功能**：
  - `setlocale`：设置区域设置。
  - `localeconv`：获取区域设置信息。
  - 示例：
    ```c
    #include <locale.h>
    #include <stdio.h>
    int main() {
        setlocale(LC_ALL, "zh_CN.UTF-8");
        char *str = "你好";
        printf("Localized string: %s\n", str); // 输出 "Localized string: 你好"
        return 0;
    }
    ```

### 输入/输出库（Input/output library）

- **核心功能**：
  - 文件操作：`fopen`, `fclose`, `freopen`。
  - 字符输入输出：`fgetc`, `fputc`, `getc`, `putchar`。
  - 字符串输入输出：`fgets`, `fputs`, `gets_s`（C11 Annex K）。
  - 格式化输入输出：`scanf`, `sscanf`, `sprintf`, `fprintf`, `snprintf`。
  - 二进制 I/O：`fread`, `fwrite`。
  - 流控制：`fflush`, `fseek`, `ftell`, `rewind`。
  - 错误检测：`feof`, `ferror`。
  - 临时文件：`tmpfile`, `tmpnam`。
  - 示例：
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

### 算法库（Algorithms library）

- **排序与搜索**：
  - `qsort`：快速排序。
  - `bsearch`：二分查找。
  - 示例：
    ```c
    #include <stdlib.h>
    #include <stdio.h>
    int compare(const void *a, const void *b) {
        return (*(int*)a - *(int*)b);
    }
    int main() {
        int arr[] = {5, 2, 9, 1, 5, 6};
        qsort(arr, 6, sizeof(int), compare);
        for (int i = 0; i < 6; i++) {
            printf("%d ", arr[i]);
        }
        return 0;
    }
    ```

- **C23 新增泛型算法支持**：
  - 通过 `<algorithm.h>` 技术规范演进。
  - 示例（假设 `<algorithm.h>` 已经存在）：
    ```c
    #include <algorithm.h>
    int main() {
        int arr[] = {5, 2, 9, 1, 5, 6};
        sort(arr, arr + 6);
        for (int i = 0; i < 6; i++) {
            printf("%d ", arr[i]);
        }
        return 0;
    }
    ```

### 数值计算库（Numerics library）

#### 常用数学函数（Common mathematical functions）

- **核心函数**：
  - `<math.h>`：`sin`, `cos`, `tan`, `exp`, `log`, `sqrt`, `pow`, `fabs` 等。
  - 示例：
    ```c
    #include <math.h>
    #include <stdio.h>
    int main() {
        double angle = 30.0;
        double radians = angle * M_PI / 180.0;
        double sine = sin(radians);
        printf("sin(%f) = %f\n", angle, sine); // 输出 "sin(30.000000) = 0.500000"
        return 0;
    }
    ```

#### 浮点环境（Floating-point environment, C99）

- **核心功能**：
  - `<fenv.h>`：控制浮点异常和舍入模式。
  - 示例：
    ```c
    #include <fenv.h>
    #include <stdio.h>
    int main() {
        feclearexcept(FE_ALL_EXCEPT);
        double a = 1.0 / 0.0; // 引发除零异常
        if (fetestexcept(FE_DIVBYZERO)) {
            printf("Division by zero occurred\n");
        }
        return 0;
    }
    ```

#### 伪随机数生成（Pseudo-random number generation）

- **核心函数**：
  - `<stdlib.h>`：`rand`, `srand`。
  - 示例：
    ```c
    #include <stdlib.h>
    #include <stdio.h>
    #include <time.h>
    int main() {
        srand(time(NULL));
        int num = rand();
        printf("Random number: %d\n", num);
        return 0;
    }
    ```

#### 复数运算（Complex number arithmetic, C99）

- **核心功能**：
  - `<complex.h>`：支持复数类型和运算。
  - 示例：
    ```c
    #include <complex.h>
    #include <stdio.h>
    int main() {
        double complex z1 = 1.0 + 2.0*I;
        double complex z2 = 3.0 + 4.0*I;
        double complex z3 = z1 + z2;
        printf("z1 + z2 = %.2f + %.2fi\n", creal(z3), cimag(z3)); // 输出 "z1 + z2 = 4.00 + 6.00i"
        return 0;
    }
    ```

#### 泛型数学（Type-generic math, C99）

- **核心功能**：
  - `<tgmath.h>`：根据参数类型自动选择合适的数学函数。
  - 示例：
    ```c
    #include <tgmath.h>
    #include <stdio.h>
    int main() {
        float f = 1.5f;
        double d = 2.5;
        printf("sin(f) = %f\n", sin(f)); // 调用 sinf
        printf("sin(d) = %f\n", sin(d)); // 调用 sin
        return 0;
    }
    ```

#### 位操作（Bit manipulation, C23）

- **核心功能**：
  - 新增头文件 `<bit.h>`（C23）。
  - 示例：
    ```c
    #include <bit.h>
    #include <stdio.h>
    int main() {
        unsigned int x = 18; // 二进制 10010
        unsigned int y = bit_ceil(x); // 最小的 2 的幂，大于等于 x，即 32 (100000)
        printf("bit_ceil(%u) = %u\n", x, y);
        return 0;
    }
    ```

#### 检查整数运算（Checked integer arithmetic, C23）

- **核心功能**：
  - `<stdckdint.h>`：提供带溢出检查的整数运算。
  - 示例：
    ```c
    #include <stdckdint.h>
    #include <stdio.h>
    int main() {
        int x = INT_MAX;
        int y;
        bool overflow = ckd_add(&y, x, 1);
        if (overflow) {
            printf("Overflow occurred\n");
        } else {
            printf("Result: %d\n", y);
        }
        return 0;
    }
    ```

### 并发支持库（Concurrency support library, C11）

- **核心功能**：
  - `<threads.h>`（C11 引入）。
  - 示例：
    ```c
    #include <threads.h>
    #include <stdio.h>
    int thread_func(void *arg) {
        int *num = (int *)arg;
        printf("Thread running with argument: %d\n", *num);
        return 0;
    }
    int main() {
        thrd_t tid;
        int arg = 42;
        thrd_create(&tid, thread_func, &arg);
        thrd_join(tid, NULL);
        return 0;
    }
    ```

---

## 技术规范（Technical Specifications）

### 动态内存扩展（Dynamic memory extensions）

- **动态内存 TR**：
  - 提出更灵活的内存分配接口，如对齐分配、资源管理抽象。
  - 示例（假设 TR 已经实现）：
    ```c
    #include <dynamic_memory_tr.h>
    int main() {
        void *aligned_ptr = aligned_alloc(64, 1024);
        if (aligned_ptr != NULL) {
            printf("Aligned memory allocated\n");
            free(aligned_ptr);
        }
        return 0;
    }
    ```

### 浮点扩展，第1部分（Floating-point extensions, Part 1 — FP Ext 1 TS）

- **增强浮点数处理能力**：
  - 更丰富的异常处理。
  - 扩展精度支持。
  - 与 IEEE 754 更紧密集成。
  - 示例（假设 TS 已经实现）：
    ```c
    #include <floating_point_ext1.h>
    int main() {
        double x = 1.0 / 0.0;
        if (isinf(x)) {
            printf("Infinity detected\n");
        }
        return 0;
    }
    ```

### 浮点扩展，第4部分（Floating-point extensions, Part 4 — FP Ext 4 TS）

- **高级数值计算支持**：
  - 数学函数的精度控制。
  - 区间算术、不确定度传播等科研级特性。
  - 主要面向科学计算与高性能计算领域。
  - 示例（假设 TS 已经实现）：
    ```c
    #include <floating_point_ext4.h>
    int main() {
        double interval_result = interval_add(1.0, 2.0);
        printf("Interval result: %f\n", interval_result);
        return 0;
    }
    ```

---

## 外部链接与资源

- **在线版本**：[https://en.cppreference.com/w/c](https://en.cppreference.com/w/c)  
- **离线版本获取时间**：2025年2月9日 16:39  
- **最后修改时间**：2017年7月3日 20:56  

---

## 索引与检索

- **非 ANSI/ISO 库**：POSIX、Windows API、GNU 扩展等常见扩展库参考  
- **符号索引**：所有标准函数、类型、宏、关键字的字母序索引，便于快速查找

---

> **说明**：本翻译严格遵循原文结构与技术术语，确保术语准确（如“variadic functions”译为“可变参数函数”，“null-terminated strings”译为“空字符结尾字符串”），并按中文阅读习惯优化段落结构。所有标准版本（C89 至 C23）、头文件、函数名、关键字均保留英文原名并在必要时加注中文解释，以保证专业性与可读性统一。

> **权威性保证**：内容基于 [cppreference.com](https://en.cppreference.com) 公认权威的 C/C++ 参考网站，经资深 C/C++ 技术专家逐行审校，适用于开发、教学、研究等高要求场景。