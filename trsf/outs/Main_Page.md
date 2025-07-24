# C 与 C++ 参考手册

来自 [cppreference.com](https://en.cppreference.com/)

---

## C++ 参考

**C++ 版本支持：** C++11、C++14、C++17、C++20、C++23、C++26  
**编译器支持：** C++11、C++14、C++17、C++20、C++23、C++26

---

### 语言（Language）

#### 关键词（Keywords）
C++ 关键词是具有特殊含义的保留字，不能用作标识符。例如，`class`, `namespace`, `public`, `private`, `template`, `auto` 等。这些关键词用于定义类、命名空间、访问控制、模板、自动类型推断等功能。

```cpp
// 使用 class 关键字定义一个简单的类
class MyClass {
public:
    int value;
};

// 使用 template 关键字定义一个模板函数
template<typename T>
T add(T a, T b) {
    return a + b;
}

// 使用 auto 关键字进行类型推断
auto result = add(1, 2); // result 的类型将被推断为 int
```

#### 预处理器（Preprocessor）
预处理器在编译过程的早期阶段对源代码进行文本替换和条件编译。常见的预处理器指令包括 `#include`, `#define`, `#ifdef`, `#ifndef`, `#endif` 等。

```cpp
// 使用 #include 包含标准库头文件
#include <iostream>

// 使用 #define 定义宏
#define PI 3.14159

// 使用 #ifdef 和 #endif 进行条件编译
#ifdef DEBUG
std::cout << "Debug mode is on." << std::endl;
#endif

int main() {
    std::cout << "PI is approximately " << PI << std::endl;
    return 0;
}
```

#### ASCII 字符表（ASCII chart）
ASCII（American Standard Code for Information Interchange）字符集包含了128个字符，每个字符对应一个唯一的数字。这些字符包括英文字母（大小写）、数字、标点符号和一些控制字符。

| 十进制 | 十六进制 | 字符 |
|--------|----------|------|
| 0      | 0x00     | NUL  |
| 1      | 0x01     | SOH  |
| ...    | ...      | ...  |
| 32     | 0x20     | (space) |
| 33     | 0x21     | !    |
| 34     | 0x22     | "    |
| ...    | ...      | ...  |
| 65     | 0x41     | A    |
| ...    | ...      | ...  |
| 97     | 0x61     | a    |
| ...    | ...      | ...  |

#### 基本概念（Basic concepts）

##### 注释（Comments）
注释用于向代码添加说明，分为单行注释（以 `//` 开头）和多行注释（以 `/*` 开始，以 `*/` 结束）。

```cpp
// 这是一个单行注释

/*
这是
一个多行
注释
*/
```

##### 名称（名称查找，Names and lookup）
名称查找是指编译器如何确定给定名称所指的具体实体。C++ 支持作用域规则，包括全局作用域、命名空间作用域、类作用域等。

```cpp
int x = 10; // 全局作用域中的 x

void func() {
    int x = 20; // 局部作用域中的 x
    std::cout << x << std::endl; // 输出 20，局部作用域优先
    std::cout << ::x << std::endl; // 输出 10，使用 :: 访问全局作用域中的 x
}
```

##### 类型（基本类型，Types and fundamental types）
C++ 提供了多种基本类型，如整数类型 (`int`, `short`, `long`)、浮点类型 (`float`, `double`)、布尔类型 (`bool`)、字符类型 (`char`) 等。

```cpp
int i = 10;          // 整数类型
float f = 3.14f;     // 浮点类型
double d = 3.14159;  // 双精度浮点类型
bool b = true;       // 布尔类型
char c = 'A';        // 字符类型
```

##### `main` 函数（The `main` function）
`main` 函数是程序的入口点，每个 C++ 程序都必须包含一个 `main` 函数。`main` 函数可以接受命令行参数，并返回一个整数值作为退出状态码。

```cpp
int main(int argc, char* argv[]) {
    if (argc > 1) {
        std::cout << "Arguments provided:" << std::endl;
        for (int i = 1; i < argc; ++i) {
            std::cout << argv[i] << std::endl;
        }
    } else {
        std::cout << "No arguments provided." << std::endl;
    }
    return 0; // 成功退出
}
```

#### 表达式（Expressions）

##### 值类别（Value categories）
C++ 中的表达式可以分为以下几种类别：左值（lvalue）、右值（rvalue）、纯右值（prvalue）、将亡值（xvalue）和泛左值（glvalue）。左值有持久的身份（地址），右值则是临时的，没有持久的身份。

```cpp
int a = 5;          // a 是一个左值
int&& r = std::move(a); // r 是一个将亡值引用，绑定到 a
int b = a + 3;      // a + 3 是一个纯右值
```

##### 求值顺序（Evaluation order）
求值顺序是指表达式中各个子表达式的计算顺序。C++ 标准对大多数情况下的求值顺序不作规定，除了某些特定情况（如逻辑运算符 `&&` 和 `||`）。

```cpp
int x = 10;
int y = 20;
int z = (x++, y++); // x++ 和 y++ 的顺序未指定，但最终 z 的值为 20
```

##### 运算符（优先级，Operators and precedence）
运算符决定了表达式中各个操作数之间的关系和计算顺序。C++ 中的运算符按优先级分为多个级别，从高到低排列。

```cpp
int a = 10;
int b = 20;
int c = a + b * 2; // 乘法优先级高于加法，c 的值为 50
```

##### 类型转换（Conversions）
类型转换是指将一个类型的值转换为另一个类型的值。C++ 支持隐式类型转换和显式类型转换（强制类型转换）。

```cpp
int a = 10;
double b = a; // 隐式类型转换，a 被提升为 double 类型
int c = static_cast<int>(b); // 显式类型转换，b 被转换为 int 类型
```

##### 字面量（Literals）
字面量是直接出现在源代码中的常量值。C++ 支持多种类型的字面量，如整数字面量、浮点字面量、字符字面量、字符串字面量等。

```cpp
int a = 42;         // 整数字面量
double b = 3.14;    // 浮点字面量
char c = 'A';       // 字符字面量
const char* str = "Hello, World!"; // 字符串字面量
```

#### 语句（Statements）

##### `if` – `switch`
`if` 语句用于根据条件执行不同的代码块，而 `switch` 语句用于根据变量的值选择不同的代码块执行。

```cpp
int score = 85;

if (score >= 90) {
    std::cout << "Grade: A" << std::endl;
} else if (score >= 80) {
    std::cout << "Grade: B" << std::endl;
} else {
    std::cout << "Grade: C or below" << std::endl;
}

switch (score / 10) {
    case 10:
    case 9:
        std::cout << "Excellent!" << std::endl;
        break;
    case 8:
        std::cout << "Good job!" << std::endl;
        break;
    default:
        std::cout << "Keep trying!" << std::endl;
        break;
}
```

##### `for` – 范围 `for`（range-`for`，C++11 起）
`for` 循环用于重复执行一段代码，范围 `for` 循环简化了遍历容器或数组的过程。

```cpp
for (int i = 0; i < 5; ++i) {
    std::cout << i << " ";
}
// 输出: 0 1 2 3 4

std::vector<int> vec = {10, 20, 30, 40, 50};
for (int value : vec) {
    std::cout << value << " ";
}
// 输出: 10 20 30 40 50
```

##### `while` – `do`-`while`
`while` 循环在条件为真时重复执行代码块，`do`-`while` 循环至少执行一次代码块，然后根据条件决定是否继续执行。

```cpp
int i = 0;
while (i < 5) {
    std::cout << i << " ";
    ++i;
}
// 输出: 0 1 2 3 4

i = 0;
do {
    std::cout << i << " ";
    ++i;
} while (i < 5);
// 输出: 0 1 2 3 4
```

#### 声明与初始化（Declarations – Initialization）
声明用于引入新的名称到程序中，初始化用于赋予新名称一个初始值。

```cpp
int a;            // 声明变量 a
int b = 10;       // 声明并初始化变量 b
int c(20);        // 使用构造函数语法初始化 c
int d{30};        // 使用统一初始化语法初始化 d
```

#### 函数与重载（Functions – Overloading）
函数是可重用的代码块，重载允许定义多个同名但参数列表不同的函数。

```cpp
void print(int a) {
    std::cout << "Integer: " << a << std::endl;
}

void print(double a) {
    std::cout << "Double: " << a << std::endl;
}

int main() {
    print(42);      // 调用 print(int)
    print(3.14);    // 调用 print(double)
    return 0;
}
```

#### 类（含联合体，Classes including unions）
类是用户自定义的数据类型，联合体是一种特殊的类，其中所有成员共享同一块内存空间。

```cpp
class Point {
public:
    int x, y;
    void setPoint(int x, int y) {
        this->x = x;
        this->y = y;
    }
};

union Data {
    int i;
    float f;
    char str[20];
};

int main() {
    Point p;
    p.setPoint(10, 20);
    std::cout << "Point: (" << p.x << ", " << p.y << ")" << std::endl;

    Data data;
    data.i = 10;
    std::cout << "Data as int: " << data.i << std::endl;
    data.f = 220.5;
    std::cout << "Data as float: " << data.f << std::endl;
    strcpy(data.str, "C Programming");
    std::cout << "Data as string: " << data.str << std::endl;
    return 0;
}
```

#### 模板与异常（Templates – Exceptions）
模板允许编写可以处理多种数据类型的代码，异常用于处理程序运行时可能出现的错误情况。

```cpp
template<typename T>
T max(T a, T b) {
    return (a > b) ? a : b;
}

void riskyFunction() {
    throw std::runtime_error("Something went wrong!");
}

int main() {
    std::cout << "Max of 5 and 10 is: " << max(5, 10) << std::endl;
    try {
        riskyFunction();
    } catch (const std::runtime_error& e) {
        std::cout << "Caught an exception: " << e.what() << std::endl;
    }
    return 0;
}
```

#### 独立运行环境实现（Freestanding implementations）
独立运行环境实现不依赖于操作系统，通常用于嵌入式系统。这种实现不需要标准库中的所有功能，只需要满足基本的语言特性。

```cpp
// freestanding 实现中的 main 函数可能看起来像这样
extern "C" void _start() {
    // 初始化硬件
    // 调用 main 函数
    main();
    // 清理工作
    // 无限循环
    while (true);
}
```

---

### 标准库（Standard Library）

#### 标准库头文件（Standard library headers）
标准库提供了丰富的头文件，涵盖了从输入输出到算法实现的各种功能。常见的头文件包括 `<iostream>`, `<vector>`, `<string>`, `<algorithm>` 等。

```cpp
#include <iostream>
#include <vector>
#include <string>
#include <algorithm>

int main() {
    std::vector<std::string> names = {"Alice", "Bob", "Charlie"};
    std::sort(names.begin(), names.end());
    for (const auto& name : names) {
        std::cout << name << std::endl;
    }
    return 0;
}
```

#### 命名需求（Named requirements）
命名需求定义了标准库组件所需满足的一组接口要求。例如，`CopyConstructible` 要求一个类型必须支持拷贝构造函数。

```cpp
class MyClass {
public:
    MyClass() {}
    MyClass(const MyClass&) = default; // 拷贝构造函数
};

static_assert(std::is_copy_constructible<MyClass>::value, "MyClass is not copy constructible");
```

#### 特性测试宏（Feature test macros，C++20 起）
特性测试宏用于检查编译器是否支持某个 C++ 标准特性。这些宏以 `__cpp_` 开头，后跟特性名称和年份。

```cpp
#if __cpp_concepts >= 201507
template<typename T>
concept Integral = std::is_integral_v<T>;

Integral auto add(Integral auto a, Integral auto b) {
    return a + b;
}
#endif
```

---

### 语言支持库（Language support library）

#### 程序工具（Program utilities）
程序工具提供了一些辅助程序执行的功能，如信号处理和非局部跳转。

```cpp
#include <csignal>
#include <iostream>

void signalHandler(int signum) {
    std::cout << "Interrupt signal (" << signum << ") received.\n";
    exit(signum);
}

int main() {
    signal(SIGINT, signalHandler);
    while(1) {
        std::cout << "Going to sleep...." << std::endl;
        sleep(1);
    }
    return 0;
}
```

#### 基本内存管理（Basic memory management）
基本内存管理提供了动态分配和释放内存的功能，包括 `new`, `delete`, `new[]`, `delete[]`。

```cpp
int* ptr = new int(10); // 动态分配一个 int
std::cout << *ptr << std::endl;
delete ptr; // 释放内存

int* arr = new int[5]; // 动态分配一个 int 数组
for (int i = 0; i < 5; ++i) {
    arr[i] = i * 10;
}
delete[] arr; // 释放数组内存
```

#### 可变参数函数（Variadic functions）
可变参数函数可以接受任意数量和类型的参数，使用 `...` 表示可变参数。

```cpp
#include <cstdarg>
#include <iostream>

double average(int count, ...) {
    va_list args;
    va_start(args, count);
    double sum = 0;
    for (int i = 0; i < count; ++i) {
        sum += va_arg(args, double);
    }
    va_end(args);
    return sum / count;
}

int main() {
    std::cout << "Average: " << average(3, 1.5, 2.5, 3.5) << std::endl;
    return 0;
}
```

#### `source_location`（C++20）
`source_location` 提供了获取当前源代码位置信息的功能，包括文件名、行号、列号等。

```cpp
#include <iostream>
#include <source_location>

void log(const std::string& message, const std::source_location& location = std::source_location::current()) {
    std::cout << "[" << location.file_name() << ":" << location.line() << "] " << message << std::endl;
}

int main() {
    log("Hello, World!");
    return 0;
}
```

#### 协程支持（Coroutine support，C++20）
协程是一种可以暂停和恢复执行的函数，用于异步编程和生成器模式。

```cpp
#include <coroutine>
#include <iostream>

struct Task {
    struct promise_type {
        Task get_return_object() { return {}; }
        std::suspend_never initial_suspend() { return {}; }
        std::suspend_never final_suspend() noexcept { return {}; }
        void return_void() {}
        void unhandled_exception() {}
    };
};

Task myCoroutine() {
    std::cout << "Coroutine started" << std::endl;
    co_await std::suspend_always{};
    std::cout << "Coroutine resumed" << std::endl;
}

int main() {
    auto coro = myCoroutine();
    // 这里可以执行其他任务
    std::cout << "Main continues" << std::endl;
    return 0;
}
```

#### 比较工具（Comparison utilities，C++20）
比较工具提供了通用的比较操作，支持三路比较运算符 `<=>`。

```cpp
#include <compare>

struct Point {
    int x, y;
    auto operator<=>(const Point&) const = default;
};

int main() {
    Point p1{1, 2}, p2{3, 4};
    if (p1 < p2) {
        std::cout << "p1 is less than p2" << std::endl;
    }
    return 0;
}
```

#### 类型支持（Type support）与 `type_info`
类型支持提供了各种类型相关的操作，`type_info` 用于获取类型信息。

```cpp
#include <typeinfo>
#include <iostream>

int main() {
    int i = 10;
    std::cout << "Type of i is " << typeid(i).name() << std::endl;
    return 0;
}
```

#### `numeric_limits` 与 `exception`
`numeric_limits` 提供了关于数值类型的属性信息，`exception` 提供了异常处理机制。

```cpp
#include <limits>
#include <iostream>

int main() {
    std::cout << "Max int: " << std::numeric_limits<int>::max() << std::endl;
    std::cout << "Min int: " << std::numeric_limits<int>::min() << std::endl;
    return 0;
}
```

#### `initializer_list`（C++11 起）
`initializer_list` 提供了一种方便的方式来传递一组初始化器。

```cpp
#include <iostream>
#include <initializer_list>

void print(std::initializer_list<int> values) {
    for (int value : values) {
        std::cout << value << " ";
    }
    std::cout << std::endl;
}

int main() {
    print({1, 2, 3, 4, 5});
    return 0;
}
```

---

### 概念库（Concepts library，C++20 起）

概念库提供了模板约束机制，使得模板可以更加明确地表达其要求。

```cpp
#include <concepts>
#include <iostream>

template<typename T>
concept Integral = std::is_integral_v<T>;

Integral auto add(Integral auto a, Integral auto b) {
    return a + b;
}

int main() {
    std::cout << add(1, 2) << std::endl;
    // std::cout << add(1.1, 2.2) << std::endl; // 编译错误，因为 1.1 和 2.2 不是 Integral 类型
    return 0;
}
```

---

### 诊断库（Diagnostics library）

#### 断言（Assertions）
断言用于在调试期间验证程序的假设，如果断言失败，则程序会终止并输出错误信息。

```cpp
#include <cassert>
#include <iostream>

int main() {
    int x = 10;
    assert(x > 0); // 如果 x <= 0，程序会终止并输出错误信息
    std::cout << "x is positive" << std::endl;
    return 0;
}
```

#### 系统错误（System error，C++11 起）
系统错误提供了处理操作系统级别的错误的功能。

```cpp
#include <iostream>
#include <system_error>

int main() {
    try {
        std::error_code ec;
        std::filesystem::path p("/nonexistent_file");
        std::filesystem::remove(p, ec);
        if (ec) {
            throw std::system_error(ec);
        }
    } catch (const std::system_error& e) {
        std::cout << "Error: " << e.what() << std::endl;
    }
    return 0;
}
```

#### 异常类型（Exception types）
异常类型定义了不同类型的异常，用于区分不同的错误情况。

```cpp
#include <iostream>
#include <stdexcept>

void riskyFunction() {
    throw std::runtime_error("Something went wrong!");
}

int main() {
    try {
        riskyFunction();
    } catch (const std::runtime_error& e) {
        std::cout << "Caught runtime_error: " << e.what() << std::endl;
    } catch (const std::exception& e) {
        std::cout << "Caught generic exception: " << e.what() << std::endl;
    }
    return 0;
}
```

#### 错误码（Error numbers）
错误码提供了操作系统级别的错误代码，用于表示特定的错误情况。

```cpp
#include <cerrno>
#include <cstring>
#include <iostream>
#include <fstream>

int main() {
    std::ifstream file("nonexistent_file.txt");
    if (!file.is_open()) {
        std::cout << "Error opening file: " << strerror(errno) << std::endl;
    }
    return 0;
}
```

#### `basic_stacktrace`（C++23 起）
`basic_stacktrace` 提供了获取当前调用栈信息的功能，用于调试和日志记录。

```cpp
#include <stacktrace>
#include <iostream>

void func2() {
    auto trace = std::stacktrace::current();
    std::cout << "Stack trace:\n" << trace << std::endl;
}

void func1() {
    func2();
}

int main() {
    func1();
    return 0;
}
```

#### 调试支持（Debugging support，C++26 起）
调试支持提供了更多调试相关功能，如断点、变量检查等。

```cpp
#include <iostream>
#include <debug>

int main() {
    int x = 10;
    std::cout << "x is " << x << std::endl;
    // 在此处设置断点进行调试
    return 0;
}
```

---

### 内存管理库（Memory management library）

#### 分配器（Allocators）
分配器负责管理内存的分配和释放，可以自定义分配器以满足特定需求。

```cpp
#include <memory>
#include <vector>
#include <iostream>

int main() {
    std::allocator<int> alloc;
    int* ptr = alloc.allocate(5);
    for (int i = 0; i < 5; ++i) {
        alloc.construct(ptr + i, i * 10);
    }
    for (int i = 0; i < 5; ++i) {
        std::cout << ptr[i] << " ";
    }
    std::cout << std::endl;
    for (int i = 0; i < 5; ++i) {
        alloc.destroy(ptr + i);
    }
    alloc.deallocate(ptr, 5);
    return 0;
}
```

#### 智能指针（Smart pointers）
智能指针自动管理动态分配的对象，避免内存泄漏。常见的智能指针包括 `std::unique_ptr`, `std::shared_ptr`, `std::weak_ptr`。

```cpp
#include <memory>
#include <iostream>

void useUniquePtr() {
    std::unique_ptr<int> ptr(new int(10));
    std::cout << *ptr << std::endl;
    // 当 ptr 离开作用域时，自动释放内存
}

void useSharedPtr() {
    std::shared_ptr<int> ptr1(new int(10));
    std::shared_ptr<int> ptr2 = ptr1; // 共享所有权
    std::cout << *ptr1 << " " << *ptr2 << std::endl;
    // 当最后一个 shared_ptr 离开作用域时，自动释放内存
}

int main() {
    useUniquePtr();
    useSharedPtr();
    return 0;
}
```

#### 内存资源（Memory resources，C++17 起）
内存资源提供了更灵活的内存管理机制，可以自定义内存池等。

```cpp
#include <memory_resource>
#include <iostream>
#include <vector>

int main() {
    std::pmr::unsynchronized_pool_resource pool;
    std::pmr::vector<int> vec(&pool);
    for (int i = 0; i < 10; ++i) {
        vec.push_back(i * 10);
    }
    for (int value : vec) {
        std::cout << value << " ";
    }
    std::cout << std::endl;
    return 0;
}
```

---

### 元编程库（Metaprogramming library，C++11 起）

#### 类型特性（Type traits）
类型特性提供了查询和操作类型属性的功能。

```cpp
#include <type_traits>
#include <iostream>

template<typename T>
void printTypeTraits() {
    std::cout << "is_integral: " << std::is_integral<T>::value << std::endl;
    std::cout << "is_floating_point: " << std::is_floating_point<T>::value << std::endl;
    std::cout << "is_pointer: " << std::is_pointer<T>::value << std::endl;
}

int main() {
    printTypeTraits<int>();
    printTypeTraits<double>();
    printTypeTraits<int*>();
    return 0;
}
```

#### 比例库（`ratio`）
比例库提供了精确的比例计算功能，常用于单位换算。

```cpp
#include <ratio>
#include <iostream>

using namespace std::ratio_literals;

int main() {
    std::ratio<1, 1000> milli;
    std::cout << "1 meter = " << (1 * 1m / milli) << " millimeters" << std::endl;
    return 0;
}
```

#### `integer_sequence`（C++14 起）
`integer_sequence` 提供了编译时整数序列，常用于元编程。

```cpp
#include <utility>
#include <iostream>

template<std::size_t... Is>
void printSequence(std::index_sequence<Is...>) {
    ((std::cout << Is << " "), ...);
    std::cout << std::endl;
}

int main() {
    printSequence(std::make_index_sequence<5>());
    return 0;
}
```

---

### 通用工具库（General utilities library）

#### 函数对象（Function objects）
函数对象是可调用的对象，可以像函数一样使用。

```cpp
#include <functional>
#include <iostream>

int main() {
    std::plus<int> plus;
    std::cout << "10 + 20 = " << plus(10, 20) << std::endl;
    return 0;
}
```

#### 哈希（`hash`，C++11 起）
哈希提供了将对象映射为整数的功能，常用于散列表等数据结构。

```cpp
#include <functional>
#include <iostream>
#include <string>

int main() {
    std::hash<std::string> hashFunc;
    std::cout << "Hash of 'hello': " << hashFunc("hello") << std::endl;
    return 0;
}
```

#### 交换（`swap`）与类型操作（Type operations，C++11 起）
`swap` 用于交换两个对象的值，类型操作提供了查询和操作类型属性的功能。

```cpp
#include <utility>
#include <iostream>

int main() {
    int a = 10, b = 20;
    std::swap(a, b);
    std::cout << "a: " << a << ", b: " << b << std::endl;

    std::cout << "is_same<int, long>: " << std::is_same<int, long>::value << std::endl;
    return 0;
}
```

#### 整数比较（Integer comparison，C++20 起）
整数比较提供了更安全的整数比较操作，避免溢出等问题。

```cpp
#include <compare>
#include <iostream>

int main() {
    int a = 10, b = 20;
    std::cout << "a <=> b: " << (a <=> b) << std::endl;
    return 0;
}
```

#### `pair` 与 `tuple`（C++11 起）
`pair` 和 `tuple` 提供了存储多个不同类型的对象的功能。

```cpp
#include <utility>
#include <tuple>
#include <iostream>

int main() {
    std::pair<int, std::string> p(1, "one");
    std::cout << p.first << " " << p.second << std::endl;

    std::tuple<int, std::string, double> t(1, "one", 1.1);
    std::cout << std::get<0>(t) << " " << std::get<1>(t) << " " << std::get<2>(t) << std::endl;
    return 0;
}
```

#### `optional`（C++17 起）
`optional` 提供了表示可选值的功能，可以包含或不包含值。

```cpp
#include <optional>
#include <iostream>

int main() {
    std::optional<int> opt;
    if (opt) {
        std::cout << "Value: " << *opt << std::endl;
    } else {
        std::cout << "No value" << std::endl;
    }

    opt = 42;
    if (opt) {
        std::cout << "Value: " << *opt << std::endl;
    }
    return 0;
}
```

#### `expected`（C++23 起）
`expected` 提供了表示函数结果或错误信息的功能，类似于 Rust 中的 `Result` 类型。

```cpp
#include <expected>
#include <iostream>
#include <string>

std::expected<int, std::string> riskyFunction(bool success) {
    if (success) {
        return 42;
    } else {
        return std::make_unexpected("Something went wrong!");
    }
}

int main() {
    auto result = riskyFunction(true);
    if (result) {
        std::cout << "Result: " << *result << std::endl;
    } else {
        std::cout << "Error: " << result.error() << std::endl;
    }

    auto error = riskyFunction(false);
    if (error) {
        std::cout << "Result: " << *error << std::endl;
    } else {
        std::cout << "Error: " << error.error() << std::endl;
    }
    return 0;
}
```

#### `variant`（C++17 起）与 `any`（C++17 起）
`variant` 和 `any` 提供了存储不同类型值的功能。

```cpp
#include <variant>
#include <any>
#include <iostream>

int main() {
    std::variant<int, std::string> var = 42;
    if (std::holds_alternative<int>(var)) {
        std::cout << "Value: " << std::get<int>(var) << std::endl;
    }

    var = "hello";
    if (std::holds_alternative<std::string>(var)) {
        std::cout << "Value: " << std::get<std::string>(var) << std::endl;
    }

    std::any anyVal = 3.14;
    if (anyVal.type() == typeid(double)) {
        std::cout << "Value: " << std::any_cast<double>(anyVal) << std::endl;
    }

    anyVal = "world";
    if (anyVal.type() == typeid(std::string)) {
        std::cout << "Value: " << std::any_cast<std::string>(anyVal) << std::endl;
    }
    return 0;
}
```

#### `bitset` 与 位操作（Bit manipulation，C++20 起）
`bitset` 提供了固定大小的位集合，位操作提供了对位进行操作的功能。

```cpp
#include <bitset>
#include <iostream>

int main() {
    std::bitset<8> bits("11001010");
    std::cout << "Bits: " << bits << std::endl;
    std::cout << "Count of 1s: " << bits.count() << std::endl;
    std::cout << "Bit at position 3: " << bits[3] << std::endl;
    bits.flip(); // 反转所有位
    std::cout << "Flipped bits: " << bits << std::endl;
    return 0;
}
```

---

### 容器库（Containers library）

#### `vector`、`deque`、`array`（C++11 起）
`vector`, `deque` 和 `array` 提供了动态数组功能。

```cpp
#include <vector>
#include <deque>
#include <array>
#include <iostream>

int main() {
    std::vector<int> vec = {1, 2, 3, 4, 5};
    std::deque<int> deq = {10, 20, 30, 40, 50};
    std::array<int, 5> arr = {100, 200, 300, 400, 500};

    for (int value : vec) {
        std::cout << value << " ";
    }
    std::cout << std::endl;

    for (int value : deq) {
        std::cout << value << " ";
    }
    std::cout << std::endl;

    for (int value : arr) {
        std::cout << value << " ";
    }
    std::cout << std::endl;

    return 0;
}
```

#### `list`、`forward_list`（C++11 起）
`list` 和 `forward_list` 提供了双向链表和单向链表功能。

```cpp
#include <list>
#include <forward_list>
#include <iostream>

int main() {
    std::list<int> lst = {1, 2, 3, 4, 5};
    std::forward_list<int> flst = {10, 20, 30, 40, 50};

    for (int value : lst) {
        std::cout << value << " ";
    }
    std::cout << std::endl;

    for (int value : flst) {
        std::cout << value << " ";
    }
    std::cout << std::endl;

    return 0;
}
```

#### `map`、`multimap`、`set`、`multiset`
`map`, `multimap`, `set` 和 `multiset` 提供了关联容器功能。

```cpp
#include <map>
#include <set>
#include <iostream>

int main() {
    std::map<std::string, int> m =