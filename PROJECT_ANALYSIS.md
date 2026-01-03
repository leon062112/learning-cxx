# C++ 学习项目分析报告

## 项目概览

| 属性 | 值 |
|------|-----|
| **项目名称** | learning-cxx |
| **仓库** | [LearningInfiniTensor/learning-cxx](https://github.com/LearningInfiniTensor/learning-cxx) |
| **语言标准** | C++17 |
| **构建工具** | xmake |
| **练习数量** | 34 题 |
| **许可证** | MIT |

这是一个面向 C++ 初学者到中级学习者的渐进式学习项目，通过 34 个精心设计的练习题，系统地讲解 C++ 核心概念和现代 C++ 特性。

---

## 项目结构

```
learning-cxx/
├── .baidu-cc/               # Baidu Code Checker 配置
├── .github/                 # GitHub Actions CI 配置
├── exercises/               # 练习题目录 (34个练习)
│   ├── exercise.h           # 练习基础头文件 (ASSERT 宏)
│   ├── xmake.lua            # 练习题构建配置
│   ├── 00_hello_world/
│   ├── 01_variable&add/
│   └── ... (共34个练习目录)
├── learn/                   # 学习系统核心
│   ├── learn.cpp            # 学习程序入口
│   ├── summary.cpp          # 总结程序
│   ├── test.h               # 测试框架头文件
│   └── test.cpp             # 测试框架实现
├── xmake.lua                # 主构建文件
├── .clang-format            # 代码格式化配置
└── README.md                # 项目文档
```

---

## 练习题内容与学习路径

### 第一阶段：基础入门 (00-07)

| 题号 | 名称 | 知识点 | 练习目的 |
|------|------|--------|----------|
| 00 | hello_world | std::cout, 输出流 | 学会基本输出 |
| 01 | variable&add | 变量定义, 运算符 | 定义变量并计算 |
| 02 | function | 函数声明与定义 | 前向声明与函数实现 |
| 03 | argument&parameter | 值传递, 实参与形参 | 理解参数传递机制 |
| 04 | static | static 关键字 | 理解静态变量作用 |
| 05 | constexpr | 编译时常量, 编译期计算 | 编译期斐波那契数列 |
| 06 | array | 数组, sizeof, 三目运算符 | 数组缓存优化 |
| 07 | loop | 循环, static 缓存 | 循环缓存实现 |

### 第二阶段：指针与复合类型 (08-10)

| 题号 | 名称 | 知识点 | 练习目的 |
|------|------|--------|----------|
| 08 | pointer | 指针, 数组退化, 步长 | 指针与斐波那契判定 |
| 09 | enum&union | 枚举, 作用域枚举, 联合体, 类型双关 | 类型安全与类型转换 |
| 10 | trivial | Trivial类型, 结构体初始化 | 结构体缓存封装 |

### 第三阶段：面向对象编程 (11-19)

| 题号 | 名称 | 知识点 | 练习目的 |
|------|------|--------|----------|
| 11 | method | 成员函数 | 方法封装 |
| 12 | method_const | const 成员函数 | constexpr 对象方法 |
| 13 | class | 类, 访问控制, 构造器 | private 字段与构造器 |
| 14 | class_destruct | 析构函数, RAII, 动态内存 | 资源管理 |
| 15 | class_clone | 复制构造函数 | 对象复制 |
| 16 | class_move | 移动构造, 移动赋值, 右值引用 | 移动语义 |
| 17 | class_derive | 派生类, 继承, 对象切片 | 继承机制 |
| 18 | class_virtual | 虚函数, override, final | 多态 |
| 19 | class_virtual_destruct | 虚析构函数, static 成员 | 安全的多态析构 |

### 第四阶段：泛型编程 (20-23)

| 题号 | 名称 | 知识点 | 练习目的 |
|------|------|--------|----------|
| 20 | function_template | 函数模板 | 通用加法函数 |
| 21 | runtime_datatype | 标签化联合体, 类型判别 | 运行时类型分发 |
| 22 | class_template | 类模板 | 4D 张量类 |
| 23 | template_const | 非类型模板参数 | N 维张量索引计算 |

### 第五阶段：标准容器 (24-29)

| 题号 | 名称 | 知识点 | 练习目的 |
|------|------|--------|----------|
| 24 | std::array | 固定大小数组 | std::array API |
| 25 | std::vector | 动态数组, 容量管理 | vector 操作 |
| 26 | std::vector<bool> | 模板特化, 位压缩 | 特殊容器 |
| 27 | strides | 张量步长计算 | 多维数组索引 |
| 28 | std::string | 字符串, 字面量后缀 | string 类型 |
| 29 | std::map | 关联容器, 查找插入 | map 基本操作 |

### 第六阶段：智能指针与算法 (30-33)

| 题号 | 名称 | 知识点 | 练习目的 |
|------|------|--------|----------|
| 30 | std::unique_ptr | 独占所有权 | 所有权转移追踪 |
| 31 | std::shared_ptr | 共享所有权, weak_ptr | 引用计数 |
| 32 | std::transform | STL 算法 | 容器变换 |
| 33 | std::accumulate | STL 算法 | 累加计算 |

---

## 核心技术特性

### C++ 特性覆盖

1. **基础语法**: 变量、运算符、控制流
2. **函数**: 声明、定义、重载、默认参数
3. **类型系统**: 基础类型、复合类型、枚举、联合体
4. **内存管理**: 栈、堆、智能指针
5. **面向对象**: 封装、继承、多态
6. **模板编程**: 函数模板、类模板、模板特化
7. **STL**: 容器、迭代器、算法
8. **现代 C++**: constexpr、nullptr、auto、移动语义

### 教学特色

1. **渐进式设计**: 从简单到复杂，知识螺旋上升
2. **斐波那契主线**: 用同一算法逐步演进展示不同特性
3. **断言驱动**: 使用 ASSERT 宏验证理解
4. **实战导向**: 涉及张量计算等实际应用场景
5. **参考资料**: 每题配有 cppreference 链接

---

## 构建系统

### 主配置 (xmake.lua)

```lua
add_rules("mode.debug", "mode.release")
set_encodings("utf-8")
set_warnings("all")
set_languages("cxx17")

target("test")
    set_kind("static")
    add_defines(string.format("__XMAKE__=\"%s\"", os.scriptdir():gsub("\\", "/")))
    add_files("learn/test.cpp")

target("learn")
    set_kind("binary")
    add_deps("test")
    add_files("learn/learn.cpp")
    add_syslinks("stdc++fs")

target("summary")
    set_kind("binary")
    add_deps("test")
    add_files("learn/summary.cpp")
    add_syslinks("stdc++fs", "pthread")
```

### 练习配置 (exercises/xmake.lua)

- 定义 34 个 exercise00-exercise33 目标
- 每个练习独立构建和测试
- 中文注释说明每个练习主题

---

## 学习系统架构

### 核心文件

#### 1. learn/learn.cpp - 学习入口程序

```cpp
int main(int argc, char **argv) {
    if (argc != 2) {
        std::cerr << "Usage: xmake run learn <exercice number>" << std::endl;
        return EXIT_FAILURE;
    }
    int num;
    if (1 != std::sscanf(argv[1], "%d", &num)) {
        std::cerr << "Invalid exercise number: " << argv[1] << std::endl;
    };
    Log{Console{}} << num;
    return EXIT_SUCCESS;
}
```

#### 2. learn/summary.cpp - 总结程序

- 显示所有练习的通过/失败状态
- 支持并发测试
- 进度可视化显示

#### 3. learn/test.cpp - 测试框架实现

- `process_run()`: 执行 xmake 命令构建和运行练习
- `test_exercise()`: 测试单个练习并输出结果
- `Log::operator<<()`: 处理练习编号并执行测试

#### 4. learn/test.h - 测试框架头文件

定义 `Log` 类，支持多种输出模式（控制台/文件/空）

#### 5. exercises/exercise.h - ASSERT 宏

```cpp
#define ASSERT(COND, MSG)                                                                         \
    if (!(COND)) {                                                                                \
        std::cerr << "\x1b[31mAssertion failed at line #" << __LINE__ << ": \x1b[0m" << std::endl \
                  << std::endl                                                                    \
                  << #COND << std::endl                                                           \
                  << std::endl                                                                    \
                  << "\x1b[34mMessage:\x1b[0m" << std::endl                                       \
                  << std::endl                                                                    \
                  << MSG << std::endl                                                             \
                  << std::endl;                                                                   \
        exit(1);                                                                                  \
    }
```

---

## 使用方式

### 安装依赖

```bash
# 安装 xmake
# 安装 C++ 工具链 (MSVC/GCC/Clang)
```

### 构建项目

```bash
xmake
```

### 运行练习

```bash
xmake run learn <练习编号>  # 例如: xmake run learn 0
```

### 参数映射机制

```
命令行: 0
    ↓
learn.cpp: sscanf(argv[1], "%d", &num) → num = 0
    ↓
test.cpp: sprintf(str, "exercise%02d", 0) → "exercise00"
    ↓
xmake: xmake -P exercises exercise00
    ↓
exercises/xmake.lua: target("exercise00")
    ↓
运行: 00_hello_world/main.cpp
```

### 总结进度

```bash
xmake run summary           # 显示所有练习通过情况
```

---

## 工具链配置

### .clang-format (基于 LLVM 风格)

- 缩进: 4 空格
- 不使用 Tab
- 指针对齐: 右对齐 (int* a)
- 列限制: 无限制
- 命名空间缩进: 全部缩进

### CI/CD (.github/workflows/build.yml)

- 平台: Ubuntu, Windows
- 步骤: 安装 xmake → 构建 → 运行 summary
- 自动验证所有练习

---

## 项目特色与亮点

1. **系统性**: 从零基础到 STL 完整路径
2. **实用性**: 结合张量计算等实际场景
3. **自动化**: 完整的测试和 CI 体系
4. **文档化**: 每题配有官方文档链接
5. **渐进式**: 用斐波那契数列串联知识点

---

## 扩展计划

根据 TODO 注释，未来可能添加:
- Lambda 表达式
- deque 容器
- forward_list 容器
- 文件系统
- 线程
- 互斥锁

---

## 总结

这是一个设计精良的 C++ 教学项目，通过 34 个练习题系统地覆盖了现代 C++ 的核心特性。项目采用斐波那契数列作为主线，逐步展示从基础语法到高级模板编程的完整学习路径。配合 xmake 构建系统和自动化测试，为学习者提供了优秀的实践环境。
