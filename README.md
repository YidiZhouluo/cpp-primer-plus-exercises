# C++ Primer Plus Program Listings

## 中文说明

### 项目简介

这个仓库用于记录我学习《C++ Primer Plus》过程中手动编写和整理的书中“程序清单”代码。项目使用 CMake 管理多个独立的 C++ 示例程序，并主要在 CLion 中编写、构建和运行。

当前仓库仅记录书中的程序清单代码，不包含课后练习、复习题、编程练习或书籍原文内容。

### 内容范围

- 收录范围：书中出现的程序清单代码。
- 暂不收录：课后练习、复习题、编程练习答案。
- 不包含：书籍 PDF、扫描件、章节原文或其他受版权保护的材料。

### 项目结构

目录结构按照章节划分。每个章节目录中，文件名采用以下固定格式：

```text
章节内序号_程序名.cpp
```

例如：

```text
2.1_myfirst.cpp
2.2_carrots.cpp
```

当前结构：

```text
C++PrimePlus/
|-- Chapter2 Getting Started with C++/
|   |-- 2.1_myfirst.cpp
|   |-- 2.2_carrots.cpp
|   |-- 2.3_getinfo.cpp
|   |-- 2.4_sqrt.cpp
|   |-- 2.5_ourfunc.cpp
|   `-- 2.6_convert.cpp
|-- CMakeLists.txt
|-- LICENSE
|-- README.md
|-- main.cpp
|-- .clang-format
`-- .gitignore
```

### CMake 构建目标

每个程序清单通常对应一个独立的 CMake 可执行目标。

| 源文件 | CMake 目标 |
| --- | --- |
| `2.1_myfirst.cpp` | `myfirst` |
| `2.2_carrots.cpp` | `carrots` |
| `2.3_getinfo.cpp` | `getinfo` |
| `2.4_sqrt.cpp` | `sqrt` |
| `2.5_ourfunc.cpp` | `ourfunc` |
| `2.6_convert.cpp` | `convert` |

### 构建环境

- C++11 或更高版本
- CMake
- CLion 或其他支持 CMake 的 C++ IDE

### 构建与运行

在项目根目录执行：

```bash
cmake -S . -B build
cmake --build build
```

也可以在 CLion 中直接打开项目根目录，等待 CMake 加载完成后选择对应的运行目标。

### 当前进度

- Chapter 2: Getting Started with C++
  - 已记录程序清单 2.1 至 2.6。

### 仓库维护规范

- 只提交源代码、CMake 配置、格式化配置、许可证和说明文档。
- 不提交本地构建目录，例如 `cmake-build-debug/`、`build/`、`out/`。
- 不提交编译产物，例如 `.exe`、`.obj`、`.o`。
- 不提交本地 IDE 配置目录，例如 `.idea/`。
- 新增程序清单时，同步更新 `CMakeLists.txt` 和 README 中的目录与目标表。

### 版权说明

本仓库仅用于个人学习记录。仓库中的代码为学习过程中手动整理和编写的程序清单代码，不包含书籍原文、扫描件、PDF 或其他受版权保护的材料。

---

## English

### Project Overview

This repository records the program listing code that I manually write and organize while studying *C++ Primer Plus*. The project uses CMake to manage multiple independent C++ example programs and is mainly written, built, and run in CLion.

At this stage, this repository only contains program listings from the book. It does not include end-of-chapter exercises, review questions, programming exercise solutions, or original book text.

### Content Scope

- Included: program listing code from the book.
- Not included for now: end-of-chapter exercises, review questions, or programming exercise answers.
- Excluded: book PDFs, scans, chapter text, or other copyrighted materials.

### Project Structure

The directory structure is organized by chapter. Inside each chapter directory, file names follow this fixed format:

```text
chapter-listing-number_program-name.cpp
```

For example:

```text
2.1_myfirst.cpp
2.2_carrots.cpp
```

Current structure:

```text
C++PrimePlus/
|-- Chapter2 Getting Started with C++/
|   |-- 2.1_myfirst.cpp
|   |-- 2.2_carrots.cpp
|   |-- 2.3_getinfo.cpp
|   |-- 2.4_sqrt.cpp
|   |-- 2.5_ourfunc.cpp
|   `-- 2.6_convert.cpp
|-- CMakeLists.txt
|-- LICENSE
|-- README.md
|-- main.cpp
|-- .clang-format
`-- .gitignore
```

### CMake Build Targets

Each program listing usually corresponds to an independent CMake executable target.

| Source File | CMake Target |
| --- | --- |
| `2.1_myfirst.cpp` | `myfirst` |
| `2.2_carrots.cpp` | `carrots` |
| `2.3_getinfo.cpp` | `getinfo` |
| `2.4_sqrt.cpp` | `sqrt` |
| `2.5_ourfunc.cpp` | `ourfunc` |
| `2.6_convert.cpp` | `convert` |

### Build Environment

- C++11 or later
- CMake
- CLion or another C++ IDE with CMake support

### Build and Run

Run the following commands from the project root:

```bash
cmake -S . -B build
cmake --build build
```

You can also open the project root directory directly in CLion, wait for CMake to finish loading, and then select the target you want to run.

### Current Progress

- Chapter 2: Getting Started with C++
  - Program listings 2.1 to 2.6 have been recorded.

### Repository Maintenance Rules

- Commit only source code, CMake configuration, formatting configuration, license, and documentation.
- Do not commit local build directories such as `cmake-build-debug/`, `build/`, and `out/`.
- Do not commit compiled artifacts such as `.exe`, `.obj`, and `.o`.
- Do not commit local IDE configuration directories such as `.idea/`.
- When adding a new program listing, update both `CMakeLists.txt` and the directory/target sections in this README.

### Copyright Notice

This repository is only for personal study records. The code in this repository is manually organized and written while studying the program listings. It does not include book text, scans, PDFs, or other copyrighted materials.
