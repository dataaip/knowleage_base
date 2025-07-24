# C 与 C++ 参考手册

来自 [cppreference.com](https://en.cppreference.com)

---

## C++ 参考

**C++11、C++14、C++17、C++20、C++23、C++26**  
**编译器支持情况：C++11、C++14、C++17、C++20、C++23、C++26**

---

### 语言（Language）

#### 关键字（Keywords）

C++ 提供了一系列关键字，用于定义程序的基本结构和功能。例如：

- `class`, `struct`: 定义用户自定义的数据类型。
- `namespace`: 用于避免命名冲突。
- `inline`: 建议编译器将函数内联展开。
- `static`: 可用于定义静态成员或静态局部变量。
- `const`: 声明常量，不可修改。
- `volatile`: 告知编译器该变量可能会被外部因素改变。
- `template`: 定义泛型编程的模板。

#### 预处理器（Preprocessor）

预处理器在编译之前对源代码进行处理。常用指令包括：

- `#include`: 包含头文件。
- `#define`: 定义宏。
- `#ifdef`, `#ifndef`, `#else`, `#endif`: 条件编译。
- `#pragma`: 提供特定编译器指令。

示例：
```cpp
#define PI 3.14159
#ifdef DEBUG
    // 调试模式下的代码
#endif
```

#### ASCII 字符表（ASCII chart）

ASCII 字符集包含 128 个字符，从 0 到 127，包括控制字符（如换行、回车）和可打印字符（如字母、数字、符号）。

#### 基本概念（Basic concepts）

##### 注释（Comments）

注释用于解释代码，不参与编译。

- 单行注释：`// 这是单行注释`
- 多行注释：`/* 这是多行注释 */`

##### 名称（查找规则，Names (lookup)）

名称查找规则决定了如何解析变量、函数等标识符。

- 作用域：块级作用域（`{}` 内），文件作用域。
- 名称隐藏：内部作用域中的同名标识符会隐藏外部作用域中的标识符。

##### 类型（基本类型，Types (fundamental types)）

C++ 的基本数据类型包括：

- 整数类型：`char`, `short`, `int`, `long`, `long long`。
- 浮点类型：`float`, `double`, `long double`。
- 布尔类型：`bool`。
- 空类型：`void`。

##### `main` 函数（The `main` function）

`main` 函数是程序的入口点。其标准形式为：
```cpp
int main() {
    // 程序代码
    return 0;
}
```

#### 表达式（Expressions）

##### 值类别（Value categories）

值类别定义了表达式的分类方式，包括：

- 左值（Lvalue）：具有持久存储的对象。
- 右值（Rvalue）：临时对象。
- 将亡值（Xvalue）：将要销毁的对象。
- 纯右值（Prvalue）：不具名的对象。
- 通用左值（GLvalue）：左值或将亡值。
- 通用右值（GRvalue）：右值或将亡值。

##### 求值顺序（Evaluation order）

求值顺序决定了表达式中子表达式的计算顺序。标准并未规定大部分表达式的求值顺序，以提高优化空间。

##### 运算符（优先级，Operators (precedence)）

运算符优先级决定了表达式中运算符的结合顺序。例如：

- `* / %` 优先级高于 `+ -`。
- `&&` 优先级高于 `||`。
- `?:` 三元运算符优先级低于赋值运算符。

##### 类型转换（Conversions）

类型转换分为隐式转换和显式转换。例如：

- 隐式转换：`int a = 3.14;`（浮点数到整数）。
- 显式转换：`int b = static_cast<int>(3.14);`。

##### 字面量（Literals）

字面量是直接出现在代码中的固定值，如整数、浮点数、字符、字符串等。

#### 语句（Statements）

##### `if` 与 `switch`

条件语句用于根据条件执行不同的代码块。例如：
```cpp
if (x > 0) {
    // x 大于 0 时执行
} else if (x == 0) {
    // x 等于 0 时执行
} else {
    // x 小于 0 时执行
}

switch (x) {
    case 1:
        // x 等于 1 时执行
        break;
    case 2:
        // x 等于 2 时执行
        break;
    default:
        // 其他情况
        break;
}
```

##### `for` 与基于范围的 `for` 循环（C++11 起）

循环语句用于重复执行一段代码。例如：
```cpp
for (int i = 0; i < 10; ++i) {
    // 循环体
}

for (auto& elem : container) {
    // 遍历容器中的每个元素
}
```

##### `while` 与 `do`-`while`

循环语句用于重复执行一段代码，直到条件不再满足。例如：
```cpp
while (condition) {
    // 循环体
}

do {
    // 循环体
} while (condition);
```

#### 声明与初始化（Declarations − Initialization）

声明定义了变量或函数的存在，初始化赋予它们初始值。例如：
```cpp
int x;          // 声明
int y = 10;     // 声明并初始化
int z{20};      // 统一初始化
int a = {30};   // 统一初始化
```

#### 函数与重载（Functions − Overloading）

函数可以有相同的名称但参数列表不同（重载）。例如：
```cpp
void print(int x) {
    std::cout << "Integer: " << x << std::endl;
}

void print(double x) {
    std::cout << "Double: " << x << std::endl;
}
```

#### 类（包括联合体，Classes (unions)）

类用于定义复杂的数据结构。联合体是一种特殊类，其中所有成员共享同一块内存空间。例如：
```cpp
class Point {
public:
    int x, y;
    void move(int dx, int dy) {
        x += dx;
        y += dy;
    }
};

union Data {
    int i;
    float f;
    char str[20];
};
```

#### 模板与异常处理（Templates − Exceptions）

模板允许编写通用代码，异常处理用于处理运行时错误。例如：
```cpp
template<typename T>
T max(T a, T b) {
    return (a > b) ? a : b;
}

try {
    // 可能抛出异常的代码
} catch (const std::exception& e) {
    // 处理异常
}
```

#### 独立实现（Freestanding implementations）

独立实现不需要标准库，适用于嵌入式系统。例如，编写操作系统内核时可能使用独立实现。

---

### 标准库（Standard Library）

#### 标准库头文件（Standard library (headers)）

标准库提供了许多头文件，如 `<iostream>`、`<vector>`、`<algorithm>` 等，用于各种功能。

#### 命名需求（Named requirements）

命名需求定义了标准库中各种类型的接口要求。例如，`CopyConstructible` 表示类型必须可以复制构造。

#### 特性测试宏（Feature test macros, C++20 起）

特性测试宏用于检测编译器是否支持特定 C++ 标准特性。例如：
```cpp
#if defined(__cpp_concepts)
    // 使用概念
#endif
```

---

### 语言与标准库共用组件

#### 语言支持库（Language support library）

##### 程序工具（Program utilities）

###### 信号处理（Signals）

信号处理用于响应操作系统信号。例如，捕获 `SIGINT` 信号：
```cpp
#include <csignal>
#include <iostream>

void signalHandler(int signum) {
    std::cout << "Interrupt signal (" << signum << ") received.\n";
}

int main() {
    std::signal(SIGINT, signalHandler);
    while(1){
       std::cout << "Going to sleep...." << std::endl;
       std::sleep(1);
    }
}
```

###### 非局部跳转（Non-local jumps）

非局部跳转允许程序从一个函数跳转到另一个函数。例如，使用 `setjmp` 和 `longjmp`：
```cpp
#include <csetjmp>
#include <cstdio>

jmp_buf jumpBuffer;

void secondFunction() {
    std::printf("Inside secondFunction\n");
    longjmp(jumpBuffer, 1);
}

void firstFunction() {
    std::printf("Inside firstFunction\n");
    secondFunction();
}

int main() {
    if (setjmp(jumpBuffer) != 0) {
        std::printf("Back in main\n");
    } else {
        firstFunction();
    }
    return 0;
}
```

##### 基本内存管理（Basic memory management）

包括动态内存分配和释放函数，如 `new`、`delete`、`malloc`、`free`。

##### 可变参数函数（Variadic functions）

可变参数函数可以接受任意数量的参数。例如，使用 `va_list`：
```cpp
#include <cstdarg>
#include <cstdio>

double average(int count, ...) {
    va_list args;
    double sum = 0;
    va_start(args, count);
    for (int i = 0; i < count; ++i) {
        sum += va_arg(args, int);
    }
    va_end(args);
    return sum / count;
}

int main() {
    printf("%f\n", average(3, 1, 2, 3)); // 输出 2.0
    return 0;
}
```

##### `source_location`（C++20 起）

`source_location` 提供了源代码位置的信息。例如：
```cpp
#include <iostream>
#include <source_location>

void log(const std::string& msg,
         const std::source_location location = std::source_location::current()) {
    std::cout << "File: "
              << location.file_name() << "("
              << location.line() << ":"
              << location.column() << ") `"
              << location.function_name() << "`: "
              << msg << '\n';
}

int main() {
    log("Hello, world!");
    return 0;
}
```

##### 协程支持（Coroutine support, C++20 起）

协程是一种允许函数暂停和恢复执行的机制。例如：
```cpp
#include <coroutine>
#include <iostream>

struct ReturnObject {
    struct promise_type {
        ReturnObject get_return_object() { return {}; }
        std::suspend_never initial_suspend() { return {}; }
        std::suspend_never final_suspend() noexcept { return {}; }
        void return_void() {}
        void unhandled_exception() {}
    };
};

ReturnObject counter() {
    for (int i = 0;; ++i) {
        co_yield i;
    }
}

int main() {
    auto gen = counter();
    for (int i = 0; i < 5; ++i) {
        std::cout << gen.promise().current_value << std::endl;
    }
    return 0;
}
```

##### 比较工具（Comparison utilities, C++20 起）

提供了一系列比较操作工具，如 `std::three_way_comparable`。

##### 类型支持（Type support）与 `type_info`

提供了一些类型相关的工具，如 `std::type_index`、`std::is_same`。

##### `numeric_limits` 与 `exception`

`numeric_limits` 提供了数值类型的极限值信息。`exception` 定义了异常处理的基础类。

##### `initializer_list`（C++11 起）

`initializer_list` 允许传递一组相同类型的值。例如：
```cpp
#include <initializer_list>
#include <iostream>

void print(std::initializer_list<int> vals) {
    for (int val : vals) {
        std::cout << val << " ";
    }
    std::cout << std::endl;
}

int main() {
    print({1, 2, 3, 4});
    return 0;
}
```

#### 概念库（Concepts library, C++20 起）

概念库提供了一种定义和检查类型约束的方式。例如：
```cpp
#include <concepts>

template<std::integral T>
T add(T a, T b) {
    return a + b;
}

int main() {
    std::cout << add(1, 2) << std::endl;
    // std::cout << add(1.0, 2.0) << std::endl; // 编译错误
    return 0;
}
```

#### 诊断库（Diagnostics library）

##### 断言（Assertions）

断言用于调试，当条件为假时终止程序。例如：
```cpp
#include <cassert>

int main() {
    assert(1 == 1); // 通过
    // assert(1 == 2); // 失败
    return 0;
}
```

##### 系统错误（System error, C++11 起）

提供了一个统一的系统错误处理框架。例如：
```cpp
#include <cerrno>
#include <iostream>
#include <system_error>

int main() {
    errno = ENOENT;
    std::error_code ec(errno, std::generic_category());
    std::cout << ec.message() << std::endl; // 输出 "No such file or directory"
    return 0;
}
```

##### 异常类型（Exception types）

定义了标准异常类型，如 `std::runtime_error`、`std::logic_error`。

##### 错误码（Error numbers）

提供了标准的错误码枚举，如 `std::errc`。

##### `basic_stacktrace`（C++23 起）

`basic_stacktrace` 提供了栈跟踪信息。例如：
```cpp
#include <stacktrace>
#include <iostream>

void bar() {
    std::stacktrace st = std::stacktrace::current();
    std::cout << st << std::endl;
}

void foo() {
    bar();
}

int main() {
    foo();
    return 0;
}
```

##### 调试支持（Debugging support, C++26 起）

提供了更强大的调试工具，如 `std::debug` 命名空间。

#### 内存管理库（Memory management library）

##### 分配器（Allocators）

分配器用于管理内存分配和释放。例如，自定义分配器：
```cpp
#include <memory>
#include <iostream>

template<class T>
class MyAllocator {
public:
    using value_type = T;

    MyAllocator() = default;

    template<class U>
    constexpr MyAllocator(const MyAllocator<U>&) noexcept {}

    T* allocate(std::size_t n) {
        if (n > std::numeric_limits<std::size_t>::max() / sizeof(T)) throw std::bad_alloc();
        if (auto p = static_cast<T*>(std::malloc(n * sizeof(T)))) {
            return p;
        }
        throw std::bad_alloc();
    }

    void deallocate(T* p, std::size_t) noexcept {
        std::free(p);
    }
};

template<class T, class U>
bool operator==(const MyAllocator<T>&, const MyAllocator<U>&) { return true; }

template<class T, class U>
bool operator!=(const MyAllocator<T>&, const MyAllocator<U>&) { return false; }

int main() {
    std::allocator<int> alloc;
    int* p = alloc.allocate(10);
    for (int i = 0; i < 10; ++i) {
        alloc.construct(&p[i], i);
    }
    for (int i = 0; i < 10; ++i) {
        std::cout << p[i] << " ";
    }
    std::cout << std::endl;
    for (int i = 0; i < 10; ++i) {
        alloc.destroy(&p[i]);
    }
    alloc.deallocate(p, 10);
    return 0;
}
```

##### 智能指针（Smart pointers）

智能指针自动管理动态分配的内存，避免内存泄漏。例如：
```cpp
#include <memory>
#include <iostream>

class MyClass {
public:
    MyClass() { std::cout << "Constructor called" << std::endl; }
    ~MyClass() { std::cout << "Destructor called" << std::endl; }
};

int main() {
    std::shared_ptr<MyClass> ptr1 = std::make_shared<MyClass>();
    std::shared_ptr<MyClass> ptr2 = ptr1;
    std::cout << "Shared reference count: " << ptr1.use_count() << std::endl;
    return 0;
}
```

##### 内存资源（Memory resources, C++17 起）

内存资源提供了一种更细粒度的内存管理方式。例如：
```cpp
#include <memory_resource>
#include <iostream>
#include <vector>

int main() {
    std::pmr::unsynchronized_pool_resource pool;
    std::pmr::vector<int> vec(&pool);
    vec.push_back(1);
    vec.push_back(2);
    vec.push_back(3);
    for (int i : vec) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    return 0;
}
```

#### 元编程库（Metaprogramming library, C++11 起）

##### 类型特性（Type traits）

类型特性提供了一种在编译时检查和操作类型的方式。例如：
```cpp
#include <type_traits>
#include <iostream>

template<typename T>
void printType() {
    if constexpr (std::is_integral_v<T>) {
        std::cout << "Integral type" << std::endl;
    } else if constexpr (std::is_floating_point_v<T>) {
        std::cout << "Floating point type" << std::endl;
    } else {
        std::cout << "Other type" << std::endl;
    }
}

int main() {
    printType<int>();    // Integral type
    printType<double>(); // Floating point type
    printType<std::string>(); // Other type
    return 0;
}
```

##### 比例库（`ratio`）

比例库提供了表示和操作比例的方式。例如：
```cpp
#include <ratio>
#include <iostream>

int main() {
    using r1 = std::ratio<1, 2>;
    using r2 = std::ratio<3, 4>;
    using r3 = std::ratio_multiply<r1, r2>;
    std::cout << r3::num << "/" << r3::den << std::endl; // 输出 "3/8"
    return 0;
}
```

##### 整数序列（`integer_sequence`, C++14 起）

整数序列用于生成一系列整数。例如：
```cpp
#include <utility>
#include <iostream>

template<typename T, T... Is>
void printSequence(std::integer_sequence<T, Is...>) {
    ((std::cout << Is << " "), ...);
    std::cout << std::endl;
}

int main() {
    printSequence(std::make_integer_sequence<int, 5>{}); // 输出 "0 1 2 3 4"
    return 0;
}
```

#### 通用工具库（General utilities library）

##### 函数对象（Function objects）

函数对象是一种可以像函数一样调用的对象。例如：
```cpp
#include <functional>
#include <iostream>

int main() {
    std::plus<int> add;
    std::cout << add(1, 2) << std::endl; // 输出 3
    return 0;
}
```

##### 哈希（`hash`, C++11 起）

哈希提供了将对象映射到整数的方式。例如：
```cpp
#include <unordered_set>
#include <string>
#include <iostream>

int main() {
    std::unordered_set<std::string> set;
    set.insert("hello");
    set.insert("world");
    for (const auto& s : set) {
        std::cout << s << std::endl;
    }
    return 0;
}
```

##### 交换操作（Swap）

提供了 `std::swap` 函数用于交换两个对象的值。例如：
```cpp
#include <utility>
#include <iostream>

int main() {
    int a = 1, b = 2;
    std::swap(a, b);
    std::cout << a << " " << b << std::endl; // 输出 "2 1"
    return 0;
}
```

##### 类型操作（Type operations, C++11 起）

提供了许多类型操作工具，如 `std::remove_reference`、`std::is_same`。

##### 整数比较（Integer comparison, C++20 起）

提供了安全的整数比较函数，如 `std::cmp_less`、`std::cmp_equal`。

##### `pair` 与 `tuple`（C++11 起）

`pair` 和 `tuple` 用于存储多个值。例如：
```cpp
#include <tuple>
#include <iostream>

int main() {
    std::tuple<int, double, std::string> t(1, 2.0, "hello");
    int a;
    double b;
    std::string c;
    std::tie(a, b, c) = t;
    std::cout << a << " " << b << " " << c << std::endl; // 输出 "1 2 hello"
    return 0;
}
```

##### `optional`（C++17 起）

`optional` 用于表示可能不存在的值。例如：
```cpp
#include <optional>
#include <iostream>

int main() {
    std::optional<int> opt;
    if (opt.has_value()) {
        std::cout << opt.value() << std::endl;
    } else {
        std::cout << "No value" << std::endl;
    }
    opt = 10;
    std::cout << opt.value() << std::endl; // 输出 10
    return 0;
}
```

##### `expected`（C++23 起）

`expected` 用于表示可能成功的值或错误信息。例如：
```cpp
#include <expected>
#include <iostream>
#include <string>

int main() {
    std::expected<int, std::string> exp = 10;
    if (exp.has_value()) {
        std::cout << exp.value() << std::endl; // 输出 10
    } else {
        std::cout << exp.error() << std::endl;
    }
    return 0;
}
```

##### `variant`（C++17 起）与 `any`（C++17 起）

`variant` 和 `any` 用于存储不同类型的数据。例如：
```cpp
#include <variant>
#include <any>
#include <iostream>
#include <string>

int main() {
    std::variant<int, double, std::string> var = 10;
    std::visit([](auto&& arg) { std::cout << arg << std::endl; }, var); // 输出 10

    std::any anyVal = 20;
    std::cout << std::any_cast<int>(anyVal) << std::endl; // 输出 20
    return 0;
}
```

##### `bitset` 与 位操作（Bit manipulation, C++20 起）

`bitset` 提供了一种高效的位操作方式。例如：
```cpp
#include <bitset>
#include <iostream>

int main() {
    std::bitset<8> bits("11001010");
    std::cout << bits << std::endl; // 输出 "11001010"
    std::cout << bits.count() << std::endl; // 输出 4
    return 0;
}
```

#### 容器库（Containers library）

##### `vector`、`deque`、`array`（C++11 起）

`vector`、`deque` 和 `array` 是常用的序列容器。例如：
```cpp
#include <vector>
#include <deque>
#include <array>
#include <iostream>

int main() {
    std::vector<int> vec = {1, 2, 3};
    std::deque<int> deq = {4, 5, 6};
    std::array<int, 3> arr = {7, 8, 9};
    for (int i : vec) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    for (int i : deq) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    for (int i : arr) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    return 0;
}
```

##### `list`、`forward_list`（C++11 起）

`list` 和 `forward_list` 是链表容器。例如：
```cpp
#include <list>
#include <forward_list>
#include <iostream>

int main() {
    std::list<int> lst = {1, 2, 3};
    std::forward_list<int> flst = {4, 5, 6};
    for (int i : lst) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    for (int i : flst) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    return 0;
}
```

##### `map`、`multimap`、`set`、`multiset`

`map`、`multimap`、`set` 和 `multiset` 是关联容器。例如：
```cpp
#include <map>
#include <set>
#include <iostream>

int main() {
    std::map<std::string, int> m = {{"one", 1}, {"two", 2}};
    std::multimap<std::string, int> mm = {{"one", 1}, {"two", 2}, {"one", 3}};
    std::set<int> s = {1, 2, 3};
    std::multiset<int> ms = {1, 2, 2, 3};
    for (const auto& [k, v] : m) {
        std::cout << k << ": " << v << std::endl;
    }
    for (const auto& [k, v] : mm) {
        std::cout << k << ": " << v << std::endl;
    }
    for (int i : s) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    for (int i : ms) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    return 0;
}
```

##### 无序关联容器：

###### `unordered_map`（C++11 起）
###### `unordered_multimap`（C++11 起）
###### `unordered_set`（C++11 起）
###### `unordered_multiset`（C++11 起）

无序关联容器使用哈希表实现。例如：
```cpp
#include <unordered_map>
#include <unordered_set>
#include <iostream>

int main() {
    std::unordered_map<std::string, int> um = {{"one", 1}, {"two", 2}};
    std::unordered_multimap<std::string, int>umm = {{"one", 1}, {"two", 2}, {"one", 3}};
    std::unordered_set<int> us = {1, 2, 3};
    std::unordered_multiset<int>ums = {1, 2, 2, 3};
    for (const auto& [k, v] : um) {
        std::cout << k << ": " << v << std::endl;
    }
    for (const auto& [k, v] : umm) {
        std::cout << k << ": " << v << std::endl;
    }
    for (int i : us) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    for (int i : ums) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    return 0;
}
```

##### 容器适配器（Container adaptors）

容器适配器提供了特定接口的容器。例如：
```cpp
#include <stack>
#include <queue>
#include <iostream>

int main() {
    std::stack<int> stk;
    stk.push(1);
    stk.push(2);
    stk.push(3);
    while (!stk.empty()) {
        std::cout << stk.top() << " ";
        stk.pop();
    }
    std::cout << std::endl;

    std::queue<int> q;
    q.push(1);
    q.push(2);
    q.push(3);
    while (!q.empty()) {
        std::cout << q.front() << " ";
        q.pop();
    }
    std::cout << std::endl;

    std::priority_queue<int> pq;
    pq.push(1);
    pq.push(2);
    pq.push(3);
    while (!pq.empty()) {
        std::cout << pq.top() << " ";
        pq.pop();
    }
    std::cout << std::endl;
    return 0;
}
```

##### `span`（C++20 起）与 `mdspan`（C++23 起）

`span` 提供了一种轻量级的视图，而 `mdspan` 提供了多维数组视图。例如：
```cpp
#include <span>
#include <iostream>

int main() {
    int arr[] = {1, 2, 3, 4, 5};
    std::span<int> s(arr);
    for (int i : s) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    return 0;
}
```

#### 迭代器库（Iterators library）

迭代器用于遍历容器中的元素。例如：
```cpp
#include <vector>
#include <iostream>

int main() {
    std::vector<int> vec = {1, 2, 3};
    for (auto it = vec.begin(); it != vec.end(); ++it) {
        std::cout << *it << " ";
    }
    std::cout << std::endl;
    return 0;
}
```

#### 范围库（Ranges library, C++20 起）

范围库提供了一种更简洁的遍历和操作容器的方式。例如：
```cpp
#include <ranges>
#include <vector>
#include <iostream>

int main() {
    std::vector<int> vec = {1, 2, 3, 4, 5};
    auto even = vec | std::views::filter([](int x) { return x % 2 == 0; });
    for (int i : even) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    return 0;
}
```

##### 范围工厂（Range factories）
##### 范围适配器（Range adaptors）
##### `generator`（C++23 起）

#### 算法库（Algorithms library）

算法库提供了许多常用的算法。例如：
```cpp
#include <algorithm>
#include <vector>
#include <iostream>

int main() {
    std::vector<int> vec = {3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5};
    std::sort(vec.begin(), vec.end());
    for (int i : vec) {
        std::cout << i << " ";
    }
    std::cout << std::endl;
    return 0;
}
```

##### 数值算法（Numeric algorithms）
##### 执行策略（Execution policies, C++17 起）
##### 约束算法（Constrained algorithms, C++20 起）

#### 字符串库（Strings library）

##### `basic_string` 与 `char_traits`
##### `basic_string_view`（C++17 起）

#### 文本处理库（Text processing library）

##### 基础数值转换（Primitive numeric conversions, C++17 起）
##### 格式化（Formatting, C++20 起）
##### 区域设置（`locale`）与 字符分类
##### 文本编码（`text_encoding`, C++26 起）
##### 正则表达式（Regular expressions, C++11 起）

###### `basic_regex` 与 相关算法
###### 默认正则表达式语法

##### 空字符结尾序列工具：

###### 字节（byte）
###### 多字节字符（multibyte）
###### 宽字符（wide）

#### 数值计算库（Numerics library）

##### 常用数学函数（Common math functions）
##### 特殊数学函数（Mathematical special functions, C++17 起）
##### 数学常量（Mathematical constants, C++20 起）
##### 基础线性代数算法（Basic linear algebra algorithms, C++26 起）
##### 数据并行类型（SIMD, C++26 起）
##### 伪随机数生成（Pseudo-random number generation）
##### 浮点环境（Floating-point environment, C++11 起）
##### `complex` 与 `valarray`

#### 日期与时间库（Date and time library）

##### 日历（Calendar, C++20 起）
##### 时区（Time zone, C++20 起）

#### 输入/输出库（Input/output library）

##### 打印函数（Print functions, C++23 起）
##### 基于流的 I/O 与 I/O 操纵符
##### `basic_istream` 与 `basic_ostream`
##### 同步输出（Synchronized output, C++20 起）
##### 文件系统（File systems, C++17 起）

#### 并发支持库（Concurrency support library, C++11 起）

##### `thread` 与 `jthread`（C++20 起）
##### `atomic` 与 `atomic_flag`
##### `atomic_ref`（C++20 起）与 内存顺序（`memory_order`）
##### 互斥量（Mutual exclusion）与 信号量（Semaphores, C++20 起）
##### 条件变量（Condition variables）与 未来对象（Futures）
##### `latch`（C++20 起）与 `barrier`（C++20 起）
##### 安全回收机制（Safe Reclamation, C++26 起）

#### 执行支持库（Execution support library, C++26 起）

---

### 技术规范（Technical Specifications）

#### 标准库扩展（Standard library extensions）  
（Library Fundamentals TS）

##### `resource_adaptor`
##### `invocation_type`

#### 标准库扩展 v2（Standard library extensions v2）  
（Library Fundamentals TS v2）

##### `propagate_const`
##### `ostream_joiner`
##### `randint`
##### `observer_ptr`
##### 探测惯用法（Detection idiom）

#### 标准库扩展 v3（Standard library extensions v3）  
（Library Fundamentals TS v3）

##### `scope_exit`
##### `scope_fail`
##### `scope_success`
##### `unique_resource`

#### 并行库扩展 v2（Parallelism library extensions v2）  
（Parallelism TS v2）

##### SIMD（`simd`）

#### 并发库扩展（Concurrency library extensions）  
（Concurrency TS）

#### 事务内存（Transactional Memory）  
（Transaction Memory TS）

#### 反射（Reflection）  
（Reflection TS）

---

### 外部链接
- 外部资源（External Links）
- 非 ANSI/ISO 库（Non-ANSI/ISO Libraries）
- 索引（Index）
- `std` 符号索引（std Symbol Index）

---

## C 语言参考

**C89、C95、C99、C11、C17、C23**  
**编译器支持情况：C99