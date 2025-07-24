# C 参考手册

## 编译器支持

C语言的标准版本包括C89, C95, C99, C11, C17和C23。不同的编译器对这些标准的支持程度各不相同。例如，GCC和Clang都提供了广泛的C99支持，而Microsoft Visual C++直到较新的版本才完全支持C99标准。对于C23标准，大多数编译器目前仍处于实验性支持阶段。

## 语言特性

### 基本概念

C语言是一种过程式编程语言，其基本概念包括变量、常量、数据类型、表达式、控制结构和函数。例如：

```c
int main() {
    int a = 10; // 变量声明与初始化
    const int b = 20; // 常量声明
    if (a < b) { // 控制结构
        printf("a is less than b\n"); // 输出语句
    }
    return 0;
}
```

### 关键字

C语言有预定义的关键字，用于表示特定的功能。例如：

```c
int main() {
    register int i = 0; // register关键字建议编译器将变量存储在寄存器中
    volatile int j = 10; // volatile关键字告诉编译器变量可能在程序之外被修改
    static int k = 20; // static关键字声明静态局部变量或静态全局变量
    return 0;
}
```

### 预处理器

C语言使用预处理器来处理代码中的宏定义、文件包含、条件编译等。例如：

```c
#define PI 3.14159 // 宏定义
#include <stdio.h> // 文件包含

int main() {
    printf("The value of PI is %f\n", PI); // 使用宏
    #ifdef DEBUG // 条件编译
    printf("Debug mode\n");
    #endif
    return 0;
}
```

### 表达式

表达式是由操作数和操作符组成的语句，用于计算值。例如：

```c
int main() {
    int a = 10;
    int b = 5;
    int c = a + b; // 算术表达式
    int d = (a > b) ? a : b; // 条件表达式
    return 0;
}
```

### 声明

声明用于告诉编译器变量的名称和类型。例如：

```c
int a; // 声明一个整数变量
float b; // 声明一个浮点数变量
char c; // 声明一个字符变量
```

### 初始化

初始化是在声明变量时为其赋初值。例如：

```c
int a = 10; // 整数变量初始化
float b = 3.14; // 浮点数变量初始化
char c = 'A'; // 字符变量初始化
```

### 函数

函数是执行特定任务的代码块。例如：

```c
#include <stdio.h>

int add(int x, int y) { // 函数声明和定义
    return x + y;
}

int main() {
    int result = add(5, 3); // 调用函数
    printf("The result is %d\n", result);
    return 0;
}
```

### 语句

语句是C语言中最小的独立代码单元，包括表达式语句、复合语句、选择语句、迭代语句和跳转语句。例如：

```c
int main() {
    int a = 10;
    if (a > 5) { // 选择语句
        printf("a is greater than 5\n");
    } else {
        printf("a is not greater than 5\n");
    }

    for (int i = 0; i < 10; i++) { // 迭代语句
        printf("%d ", i);
    }

    return 0;
}
```

## 头文件

头文件包含了函数声明、宏定义和类型定义。例如：

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    printf("Hello, World!\n"); // 使用stdio.h中的函数
    int *ptr = malloc(sizeof(int)); // 使用stdlib.h中的函数
    free(ptr); // 使用stdlib.h中的函数
    return 0;
}
```

## 类型支持

C语言支持多种内置数据类型，包括整数类型、浮点类型和字符类型。例如：

```c
int a = 10; // 整数类型
float b = 3.14; // 浮点类型
double c = 2.718; // 双精度浮点类型
char d = 'A'; // 字符类型
```

## 程序实用工具

### 可变参数函数

可变参数函数允许函数接受可变数量的参数。例如：

```c
#include <stdarg.h>
#include <stdio.h>

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
    printf("Average: %f\n", average(3, 1.0, 2.0, 3.0));
    return 0;
}
```

### 诊断库

诊断库提供了报告错误和诊断信息的功能。例如：

```c
#include <errno.h>
#include <stdio.h>

int main() {
    FILE *file = fopen("nonexistentfile.txt", "r");
    if (!file) {
        perror("Failed to open file"); // 使用perror函数输出错误信息
    }
    return 0;
}
```

## 动态内存管理

动态内存管理允许程序在运行时分配和释放内存。例如：

```c
#include <stdlib.h>
#include <stdio.h>

int main() {
    int *arr = (int *)malloc(5 * sizeof(int)); // 动态分配内存
    if (arr == NULL) {
        fprintf(stderr, "Memory allocation failed\n");
        return 1;
    }

    for (int i = 0; i < 5; i++) {
        arr[i] = i * 10;
    }

    for (int i = 0; i < 5; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    free(arr); // 释放内存
    return 0;
}
```

## 字符串库

字符串库提供了处理字符串的各种函数。例如：

```c
#include <string.h>
#include <stdio.h>

int main() {
    char src[] = "Hello";
    char dest[10];
    strcpy(dest, src); // 使用strcpy函数复制字符串
    printf("Copied string: %s\n", dest);
    return 0;
}
```

## 算法库

算法库提供了各种算法函数，如排序、搜索等。例如：

```c
#include <stdio.h>
#include <stdlib.h>

int compare(const void *a, const void *b) {
    return (*(int*)a - *(int*)b);
}

int main() {
    int arr[] = {5, 2, 9, 1, 5, 6};
    qsort(arr, 6, sizeof(int), compare); // 使用qsort函数进行排序
    for (int i = 0; i < 6; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
    return 0;
}
```

## 数值库

数值库提供了各种数学函数和常量。例如：

```c
#include <math.h>
#include <stdio.h>

int main() {
    double num = 4.0;
    double square_root = sqrt(num); // 使用sqrt函数计算平方根
    printf("Square root of %.2f is %.2f\n", num, square_root);
    return 0;
}
```

## 日期和时间实用工具

日期和时间实用工具提供了处理日期和时间的各种函数。例如：

```c
#include <time.h>
#include <stdio.h>

int main() {
    time_t rawtime;
    struct tm * timeinfo;

    time(&rawtime); // 获取当前时间
    timeinfo = localtime(&rawtime); // 将时间转换为本地时间

    printf("Current local time and date: %s", asctime(timeinfo)); // 使用asctime函数输出时间
    return 0;
}
```

## 输入输出支持

输入输出支持提供了处理输入和输出的各种函数。例如：

```c
#include <stdio.h>

int main() {
    int num;
    printf("Enter an integer: ");
    scanf("%d", &num); // 使用scanf函数读取用户输入
    printf("You entered: %d\n", num);
    return 0;
}
```

## 国际化支持

国际化支持提供了处理多语言和多区域设置的各种函数。例如：

```c
#include <locale.h>
#include <stdio.h>

int main() {
    setlocale(LC_ALL, ""); // 设置区域为默认区域
    printf("Locale: %s\n", setlocale(LC_ALL, NULL)); // 输出当前区域设置
    return 0;
}
```

## 并发支持（C11）

并发支持提供了多线程编程的功能。例如：

```c
#include <stdio.h>
#include <stdlib.h>
#include <pthread.h>

void* thread_function(void* arg) {
    printf("Thread is running\n");
    return NULL;
}

int main() {
    pthread_t thread;
    pthread_create(&thread, NULL, thread_function, NULL); // 创建线程
    pthread_join(thread, NULL); // 等待线程结束
    return 0;
}
```

## 技术规范

技术规范提供了对C语言标准的补充和扩展。例如：

- **动态内存扩展**：提供了额外的内存管理功能。
- **浮点扩展**：提供了更高级的浮点运算支持。
- **复数运算**：提供了复数类型和运算支持。

## 符号索引

符号索引提供了对所有C语言符号的快速查找。例如：

- `malloc`：动态分配内存。
- `free`：释放动态分配的内存。
- `printf`：格式化输出到标准输出。
- `scanf`：格式化输入从标准输入。

---

### 导航

- [在线版本](https://en.cppreference.com/w/c)
- 离线版本检索于 2025-02-09 16:39。
- 该页面最后修改于 2017 年 7 月 3 日 20:56。

确保所有术语和概念均符合C/C++语言标准和专业文档的规范表达。

---

以上文档对C语言进行了详细的解释，并提供了丰富的示例，帮助读者更好地理解和掌握C语言的各种特性和功能。