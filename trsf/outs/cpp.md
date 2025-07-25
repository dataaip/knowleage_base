# C++ 参考文档

源自 cppreference.com

## C++

### 编译器支持
- **GCC**：GNU Compiler Collection，广泛用于Linux和Unix系统，支持多个C++标准，包括C++26。
- **Clang**：由LLVM项目开发，支持最新的C++标准，适用于Linux、macOS和Windows。
- **MSVC**：Microsoft Visual C++ Compiler，是微软提供的编译器，广泛应用于Windows平台开发，支持最新的C++标准。
- **Intel C++ Compiler**：提供高性能的代码优化，支持最新的C++标准。
- **Apple Clang**：苹果基于LLVM的Clang编译器，用于macOS和iOS开发。

### 独立环境与宿主环境
- **独立环境**：指在没有操作系统支持的情况下运行的环境，如嵌入式系统中的裸机编程。
- **宿主环境**：指依赖于操作系统的运行环境，如Windows、Linux等。

### 语言特性

#### C++版本支持
- **C++11**：引入了诸如`auto`关键字、lambda表达式、智能指针、右值引用和移动语义等特性。
- **C++14**：增加了泛型lambda、二进制字面量和变量模板等功能。
- **C++17**：引入了结构化绑定、`inline`变量、`constexpr` lambda、`if constexpr`等。
- **C++20**：带来了模块、概念、三路比较运算符、`std::span`、`coroutine`等重要特性。
- **C++23**：增加了`std::expected`、`std::flat_map`、`std::chrono::utc_clock`等。
- **C++26**：预计会引入`std::executors`、`std::text_encoding`、`std::stacktrace`等新特性。

#### 核心语言特性
- **关键字**：如`class`, `struct`, `namespace`, `template`等。
- **预处理器**：用于条件编译、宏定义等，如`#include`, `#define`, `#ifdef`等。
- **ASCII 码表**：定义了字符集及其编码方式。
- **基本概念**
  - **注释**：单行注释使用`//`，多行注释使用`/* */`。
  - **名称（查找规则）**：遵循作用域和命名空间规则。
  - **类型（基础类型）**：如`int`, `float`, `char`, `bool`等。
  - **`main`函数**：程序入口点。
- **表达式**
  - **值类别**：分为左值（lvalue）、右值（rvalue）、纯右值（prvalue）、将亡值（xvalue）和glvalue等。
  - **求值顺序**：在某些情况下未定义，程序员应避免依赖未定义行为。
  - **运算符（优先级）**：了解运算符优先级有助于编写正确的表达式。
  - **类型转换**：显式转换和隐式转换，如`static_cast`, `dynamic_cast`, `const_cast`等。
  - **字面量**：如整数字面量、浮点字面量、字符串字面量等。
- **语句**
  - **`if` - `switch`**：条件语句。
  - **`for` - 范围`for`循环（C++11）**：循环控制结构。
  - **`while` - `do-while`**：循环控制结构。
- **声明与初始化**
  - 声明变量类型和初始化方法。
- **函数与重载**
  - 函数定义、调用和重载机制。
- **类（联合体）**
  - 面向对象编程的基础，支持封装、继承和多态。
- **模板与异常**
  - 泛型编程和异常处理机制。
- **独立环境实现**
  - 如嵌入式系统中的特定实现细节。

### 标准库

#### 标准库头文件
- 提供各种功能的头文件，如`<iostream>`用于输入输出，`<vector>`用于动态数组等。

#### 命名需求
- 遵循命名约定，避免与标准库命名冲突。

#### 特性测试宏（C++20）
- 使用宏来检测编译器对特定特性的支持情况。

#### 语言支持库
- **程序工具**
  - **信号处理**：处理操作系统信号。
  - **非局部跳转**：如`setjmp`和`longjmp`。
- **基础内存管理**
  - 如`new`和`delete`。
- **可变参数函数**
  - 使用`va_list`处理可变数量的参数。
- **`source_location`（C++20）**
  - 提供源代码位置信息。
- **协程支持（C++20）**
  - 提供异步编程的支持。
- **比较工具（C++20）**
  - 提供`std::three_way_comparable`等工具。
- **类型支持 - `type_info`**
  - 提供运行时类型信息。
- **`numeric_limits` - 异常**
  - 提供数值类型的极限值。
- **`initializer_list`（C++11）**
  - 支持初始化列表。

#### 概念库（C++20）
- 定义和使用模板约束的概念。

#### 诊断库
- **断言 - 系统错误（C++11）**
  - 提供断言和错误码处理。
- **异常类型 - 错误码**
  - 提供标准异常类型和错误码。
- **`basic_stacktrace`（C++23）**
  - 提供堆栈跟踪支持。
- **调试支持（C++26）**
  - 提供调试工具和接口。

#### 内存管理库
- **分配器 - 智能指针**
  - 如`std::allocator`, `std::unique_ptr`, `std::shared_ptr`。
- **内存资源（C++17）**
  - 提供更细粒度的内存管理。

#### 元编程库（C++11）
- **类型特性 - `ratio`**
  - 提供编译时常量比率。
- **`integer_sequence`（C++14）**
  - 提供编译时常量整数序列。

#### 通用工具库
- **函数对象 - 哈希（C++11）**
  - 提供哈希函数对象。
- **交换 - 类型操作（C++11）**
  - 提供`std::swap`等工具。
- **整数比较（C++20）**
  - 提供`std::cmp_less`等比较函数。
- **`pair` - `tuple`（C++11）**
  - 提供简单的容器。
- **`optional`（C++17）**
  - 提供可选值。
- **`expected`（C++23）**
  - 提供预期值或错误。
- **`variant`（C++17） - `any`（C++17）**
  - 提供类型安全的联合体。
- **`bitset` - 位操作（C++20）**
  - 提供位操作工具。

#### 容器库
- **`vector` - `deque` - `array`（C++11）**
  - 提供动态数组、双端队列和固定大小数组。
- **`list` - `forward_list`（C++11）**
  - 提供双向链表和单向链表。
- **`map` - `multimap` - `set` - `multiset`**
  - 提供有序关联容器。
- **`unordered_map`（C++11） `unordered_multimap`（C++11）**
  - 提供无序关联容器。
- **`unordered_set`（C++11） `unordered_multiset`（C++11）**
  - 提供无序集合。
- **容器适配器**
  - 如`stack`, `queue`, `priority_queue`。
- **`span`（C++20） - `mdspan`（C++23）**
  - 提供视图容器。

#### 迭代器库
- 提供遍历容器的方式。

#### 范围库（C++20）
- **范围工厂 - 范围适配器**
  - 提供便捷的范围操作。
- **`generator`（C++23）**
  - 提供生成器支持。

#### 算法库
- **数值算法**
  - 提供常用的数值算法。
- **执行策略（C++17）**
  - 提供并行和矢量化执行策略。
- **约束算法（C++20）**
  - 提供带有约束的算法。

#### 字符串库
- **`basic_string` - `char_traits`**
  - 提供字符串类。
- **`basic_string_view`（C++17）**
  - 提供轻量级的字符串视图。

#### 文本处理库
- **基础数值转换（C++17）**
  - 提供数值转换工具。
- **格式化（C++20）**
  - 提供格式化字符串工具。
- **区域设置 - 字符分类**
  - 提供本地化支持。
- **`text_encoding`（C++26）**
  - 提供文本编码支持。
- **正则表达式（C++11）**
  - 提供正则表达式匹配工具。
  - **`basic_regex` - 算法**
    - 提供正则表达式类和算法。
  - **默认正则表达式语法**
    - 提供默认的正则表达式语法。
- **空终止序列工具：**
  - **`byte` - 多字节 - 宽字符**
    - 提供字节、多字节和宽字符支持。

#### 数值计算库
- **常用数学函数**
  - 提供三角函数、指数函数等。
- **特殊数学函数（C++17）**
  - 提供误差函数、贝塞尔函数等。
- **数学常量（C++20）**
  - 提供数学常量。
- **基础线性代数算法（C++26）**
  - 提供线性代数算法。
- **数据并行类型（SIMD）（C++26）**
  - 提供SIMD支持。
- **伪随机数生成**
  - 提供伪随机数生成器。
- **浮点环境（C++11）**
  - 提供浮点环境控制。
- **`complex` - `valarray`**
  - 提供复数和数值数组支持。

#### 日期时间库
- **日历（C++20） - 时区（C++20）**
  - 提供日历和时区支持。

#### 输入输出库
- **打印函数（C++23）**
  - 提供打印函数。
- **基于流的I/O - I/O操作符**
  - 提供流式输入输出。
- **`basic_istream` - `basic_ostream`**
  - 提供输入输出流类。
- **同步输出（C++20）**
  - 提供同步输出支持。
- **文件系统（C++17）**
  - 提供文件系统操作。

#### 并发支持库（C++11）
- **`thread` - `jthread`（C++20）**
  - 提供线程支持。
- **`atomic` - `atomic_flag`**
  - 提供原子操作。
- **`atomic_ref`（C++20） - 内存顺序**
  - 提供原子引用。
- **互斥锁 - 信号量（C++20）**
  - 提供互斥锁和信号量。
- **条件变量 - 期值**
  - 提供条件变量。
- **`latch`（C++20） - `barrier`（C++20）**
  - 提供同步原语。
- **安全资源回收（C++26）**
  - 提供资源回收支持。

#### 执行支持库（C++26）
- 提供执行策略和任务调度支持。

## 技术规范

### 标准库扩展
- **库基础技术规范**
  - `resource_adaptor` - `invocation_type`

### 标准库扩展 v2
- **库基础技术规范 v2**
  - `propagate_const` - `ostream_joiner` - `randint`
  - `observer_ptr` - 检测惯用法

### 标准库扩展 v3
- **库基础技术规范 v3**
  - `scope_exit` - `scope_fail` - `scope_success` - `unique_resource`

### 并行库扩展 v2（并行技术规范 v2）
- `simd`

### 并发库扩展（并发技术规范）
### 事务内存（TM 技术规范）
### 反射（反射技术规范）

## 外部链接
- **非 ANSI/ISO 标准库**：第三方库。
- **索引**：标准库符号索引。
- **std 符号索引**：标准库符号索引。

[检索自](https://en.cppreference.com/mwiki/index.php?title=cpp&oldid=97601)

---

### 导航

- [在线版本](#)
- [离线版本](#) 获取于 2025-02-09 16:39

- 本页面最后修改于 2017年12月16日 22:24。

---

## 示例代码

### C++11 Lambda表达式
```cpp
#include <iostream>
#include <vector>
#include <algorithm>

int main() {
    std::vector<int> vec = {1, 2, 3, 4, 5};

    // 使用Lambda表达式过滤出偶数
    auto is_even = [](int x) { return x % 2 == 0; };
    std::vector<int> even_vec;
    std::copy_if(vec.begin(), vec.end(), std::back_inserter(even_vec), is_even);

    // 输出结果
    for (int num : even_vec) {
        std::cout << num << " ";
    }
    return 0;
}
```

### C++17 Structured Bindings
```cpp
#include <iostream>
#include <tuple>

int main() {
    std::tuple<int, double, std::string> t(1, 2.5, "Hello");

    // 使用结构化绑定
    auto [a, b, c] = t;

    std::cout << a << ", " << b << ", " << c << std::endl;
    return 0;
}
```

### C++20 Concepts
```cpp
#include <iostream>
#include <concepts>

// 定义一个概念
template<typename T>
concept Integral = std::is_integral_v<T>;

// 使用概念约束模板函数
template<Integral T>
T add(T a, T b) {
    return a + b;
}

int main() {
    int x = 10, y = 20;
    std::cout << add(x, y) << std::endl; // 正确

    // double z = 10.5;
    // std::cout << add(x, z) << std::endl; // 编译错误
    return 0;
}
```

### C++20 Coroutines
```cpp
#include <coroutine>
#include <iostream>

// 定义一个协程
struct Generator {
    struct promise_type {
        int current_value;

        std::suspend_always initial_suspend() { return {}; }
        std::suspend_always final_suspend() noexcept { return {}; }
        std::suspend_always yield_value(int value) {
            current_value = value;
            return {};
        }
        void return_void() {}
        Generator get_return_object() { return Generator{this}; }
        bool await_ready() { return false; }
        void await_suspend(std::coroutine_handle<>) {}
        void await_resume() {}

        static std::suspend_never get_return_object_on_allocation_failure() = delete;
    };

    std::coroutine_handle<promise_type> coro;

    Generator(promise_type* p) : coro(std::coroutine_handle<promise_type>::from_promise(*p)) {}
    ~Generator() { if (coro) coro.destroy(); }

    bool next() {
        coro.resume();
        return !coro.done();
    }

    int value() const { return coro.promise().current_value; }
};

Generator fibonacci(int n) {
    int a = 0, b = 1;
    for (int i = 0; i < n; ++i) {
        co_yield a;
        int temp = a;
        a = b;
        b += temp;
    }
}

int main() {
    for (Generator fib = fibonacci(10); fib.next();) {
        std::cout << fib.value() << " ";
    }
    return 0;
}
```

通过这些扩展和示例，文档的内容变得更加丰富和详细，便于理解和应用。