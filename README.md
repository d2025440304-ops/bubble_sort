# bubble_sort
# 🌟 Generic Bubble Sort — 一个类 `qsort` 的通用冒泡排序实现

> 用纯 C 语言手写一个支持任意类型（如 `int`、结构体等）的通用排序函数，深入理解 `qsort` 背后的泛型思想与回调机制。

![C](https://img.shields.io/badge/language-C-blue?logo=c)
![License](https://img.shields.io/badge/license-MIT-green)

## 💡 项目简介

本项目实现了一个名为 `bubble_sort` 的函数，其接口设计完全模仿标准库函数 `qsort`，但内部使用**冒泡排序算法**。它能够对：

- 整型数组（`int[]`）
- 结构体数组（如学生信息：姓名、年龄、GPA）

进行灵活排序，只需传入对应的**比较函数**即可。

通过本项目，你可以深入理解：
- `void*` 泛型编程
- 函数指针作为回调
- 内存逐字节操作（通用交换）
- C 语言如何实现“多态”排序

---

## 🧪 功能演示

### ✅ 支持的排序类型

| 数据类型       | 比较函数          | 排序方式     |
|----------------|-------------------|--------------|
| `int` 数组     | `cmp_int`         | 升序         |
| 结构体（姓名） | `cmp_stu_name`    | 字典序升序   |
| 结构体（年龄） | `cmp_stu_age`     | **降序**     |

### 🖥️ 示例输出

```text
1 2 3 4 5 6 7 9 
titi 14 6
wangwu 15 3
yiyi 16 4
