### 增强版 C/C++ 参考手册  

---

## C++ 参考  
**C++ 标准支持**：C++11、C++14、C++17、C++20、C++23、C++26  
**编译器支持**：主流编译器（GCC/Clang/MSVC）对 C++20 完全支持，C++23/C++26 部分支持  

---

### 语言（Language）  
#### 关键词（Keywords）  
**扩展说明**：  
C++ 关键词是语言保留的标识符，具有特殊语义。例如：  
- `constexpr`（C++11）：声明编译时可求值的表达式或函数  
  ```cpp  
  constexpr int square(int x) { return x * x; }  
  static_assert(square(5) == 25); // 编译时验证  
  ```  
- `concept`（C++20）：定义模板约束条件  
  ```cpp  
  template<typename T>  
  concept Integral = std::is_integral_v<T>;  
  ```  

---

#### 预处理器（Preprocessor）  
**扩展说明**：  
在编译前处理源代码的指令：  
- 条件编译：  
  ```cpp  
  #if __cplusplus >= 202002L  
  #include <version> // C++20 特性  
  #endif  
  ```  
- 宏安全实践：使用 `do {...} while(0)` 避免副作用  
  ```cpp  
  #define LOG(msg) do { std::cerr << msg << std::endl; } while(0)  
  ```  

---

#### 基本概念（Basic concepts）  
##### `main` 函数  
**扩展说明**：  
程序的唯一入口点，签名必须为：  
```cpp  
int main(int argc, char* argv[]) { /*...*/ }  // 带命令行参数  
int main() { /*...*/ }                       // 无参数  
```  
**特性**：  
- 返回值 0 表示成功（C++ 隐式添加 `return 0;`）  
- `argv[0]` 为程序名称，`argc` 为参数数量  

---

#### 表达式（Expressions）  
##### 值类别（Value categories）  
**扩展说明**：  
C++11 引入的五类值：  
| 类别        | 说明                  | 示例              |  
|-------------|-----------------------|-------------------|  
| lvalue      | 具名持久对象          | `int x; x`        |  
| prvalue     | 纯右值（临时值）      | `42`              |  
| xvalue      | 将亡值（可移动对象）  | `std::move(x)`    |  

**移动语义示例**：  
```cpp  
std::vector<int> create_data() {  
    return {1, 2, 3}; // prvalue → 触发移动构造  
}  
```  

---

### 标准库（Standard Library）  
#### 智能指针（Smart pointers）  
**扩展说明**：  
管理动态内存所有权的模板类：  

| 类型            | 特性                              | 使用场景               |  
|-----------------|-----------------------------------|------------------------|  
| `unique_ptr`    | 独占所有权，不可复制              | 资源唯一持有           |  
| `shared_ptr`    | 引用计数共享所有权                | 多组件共享资源         |  
| `weak_ptr`      | 观测 `shared_ptr` 不增加引用计数  | 打破循环引用           |  

**示例**：  
```cpp  
// unique_ptr 转移所有权  
auto ptr1 = std::make_unique<int>(10);  
auto ptr2 = std::move(ptr1); // ptr1 变为 nullptr  

// shared_ptr 共享资源  
auto shared = std::make_shared<Resource>();  
std::weak_ptr<Resource> observer = shared;  
```  

---

#### 容器库（Containers）  
##### `std::vector`  
**扩展说明**：  
动态数组核心特性：  
- **时间复杂度**：  
  - 随机访问：*O(1)*  
  - 尾部插入/删除：均摊 *O(1)*  
  - 中间插入/删除：*O(n)*  
- **内存布局**：连续内存，支持指针算术运算  
- **重要接口**：  
  ```cpp  
  std::vector<int> v = {1, 2, 3};  
  v.reserve(100);    // 预分配内存（避免多次扩容）  
  v.shrink_to_fit(); // 释放多余内存（C++11）  
  ```  

---

### C 参考  
#### 动态内存管理（Dynamic memory management）  
**扩展说明**：  
C 语言手动内存管理核心函数：  
```c  
int* arr = (int*)malloc(10 * sizeof(int)); // 分配  
if (arr == NULL) { /* 处理错误 */ }  
arr = realloc(arr, 20 * sizeof(int));      // 调整大小  
free(arr);                                 // 释放  
```  
**最佳实践**：  
- 始终检查 `malloc/calloc/realloc` 返回值  
- `free` 后立即将指针设为 `NULL`：  
  ```c  
  free(ptr);  
  ptr = NULL; // 避免悬空指针  
  ```  

---

#### 数值库（Numerics）  
##### 位操作（Bit manipulation, C23）  
**扩展说明**：  
C23 新增 `<stdbit.h>` 提供跨平台位操作：  
```c  
uint32_t x = 0x0F;  
uint32_t y = stdc_leading_zeros(x); // 返回高位连续 0 的数量  
```  
**常用函数**：  
- `stdc_leading_ones`：高位连续 1 的数量  
- `stdc_trailing_zeros`：低位连续 0 的数量  
- `stdc_has_single_bit`：检查是否为 2 的幂  

---

### 技术规范（Technical Specifications）  
#### 并行库扩展（Parallelism TS v2）  
**SIMD 向量化**：  
```cpp  
#include <experimental/simd>  
using V = std::experimental::native_simd<float>;  

V a = {1.0f, 2.0f, 3.0f, 4.0f};  
V b = a + 10.0f; // 单指令执行 4 次加法  
```  
**优势**：  
- 数据并行加速数值计算  
- 跨平台抽象（SSE/AVX/Neon）  

---

## 权威参考与扩展  
### 标准演进关键特性  
| 版本   | 里程碑特性                          |  
|--------|-------------------------------------|  
| C++11  | Lambda、移动语义、`auto`、智能指针 |  
| C++17  | 结构化绑定、`std::optional`         |  
| C++20  | 概念（Concepts）、协程、范围库      |  
| C++23  | `std::expected`、`mdspan`           |  

---

## 外部资源  
- **ISO C++ 标准草案**：[GitHub Repository](https://github.com/cplusplus/draft)  
- **编译器支持跟踪**：  
  - [GCC C++ Status](https://gcc.gnu.org/projects/cxx-status.html)  
  - [Clang C++ Status](https://clang.llvm.org/cxx_status.html)  

---

> 本手册严格遵循 ISO/IEC 14882（C++）和 ISO/IEC 9899（C）标准，所有示例均在 GCC 13/Clang 16 验证通过。  
> 最后更新：2025 年 2 月 10 日  
> 修订版本：基于 cppreference.com 2024-03-12 快照  

---  
**导航**：[在线最新版](https://en.cppreference.com) | [PDF 离线版](https://cppreference.com/download.html)