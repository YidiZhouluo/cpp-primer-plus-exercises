# C++ Primer Plus Program Listings

## 中文说明

### 项目简介

这个仓库用于记录我学习《C++ Primer Plus》过程中手动整理和编写的书中“程序清单”代码。

当前仓库仅记录书里的程序清单代码，不涉及课后练习、复习题、编程练习答案，也不包含书籍原文、PDF、扫描件或其他受版权保护的材料。

### 目录范式

仓库按章节组织，每个章节使用一个独立目录：

```text
Chapter<章节号> <章节英文标题>/
```

章节目录中包含：

```text
<程序清单编号>_<程序名>.cpp
CMakeLists.txt
```

例如：

```text
Chapter3 Dealing with Data/
|-- 3.1_limits.cpp
|-- 3.2_exceed.cpp
`-- CMakeLists.txt
```

根目录只保留项目级文件：

```text
C++PrimePlus/
|-- Chapter2 Getting Started with C++/
|-- Chapter3 Dealing with Data/
|-- CMakeLists.txt
|-- LICENSE
|-- README.md
|-- .clang-format
`-- .gitignore
```

### CMake 组织方式

根目录 `CMakeLists.txt` 只负责项目配置和引入章节目录：

```cmake
add_subdirectory("Chapter2 Getting Started with C++")
add_subdirectory("Chapter3 Dealing with Data")
```

每个章节目录下的 `CMakeLists.txt` 负责声明该章节的程序清单可执行目标。例如：

```cmake
add_executable(limits 3.1_limits.cpp)
add_executable(exceed 3.2_exceed.cpp)
```

这样后续新增程序清单时，通常只需要：

- 在对应章节目录中添加新的 `.cpp` 文件。
- 在该章节的 `CMakeLists.txt` 中添加对应的 `add_executable(...)`。
- 只有新增章节目录、调整目录规范或修改仓库说明时，才需要更新本 README。

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

在 CLion 中，可以直接打开项目根目录，等待 CMake 加载完成后选择对应的运行目标。

### 当前收录范围

目前已开始整理以下章节的程序清单：

| 章节目录 | 内容 |
| --- | --- |
| `Chapter2 Getting Started with C++/` | Chapter 2: Getting Started with C++ |
| `Chapter3 Dealing with Data/` | Chapter 3: Dealing with Data |

具体程序清单文件和可执行目标，以各章节目录中的 `.cpp` 文件和 `CMakeLists.txt` 为准。

### 仓库维护规范

- 只提交源代码、CMake 配置、格式化配置、许可证和说明文档。
- 不提交本地构建目录，例如 `cmake-build-debug/`、`build/`、`out/`。
- 不提交编译产物，例如 `.exe`、`.obj`、`.o`。
- 不提交本地 IDE 配置目录，例如 `.idea/`。
- README 尽量保持为长期说明文档，不为每个新增程序清单频繁修改。

### 版权说明

本仓库仅用于个人学习记录。仓库中的代码为学习过程中手动整理和编写的程序清单代码，不包含书籍原文、扫描件、PDF 或其他受版权保护的材料。

---

## English

### Project Overview

This repository records the program listing code that I manually organize and write while studying *C++ Primer Plus*.

At this stage, this repository only contains program listings from the book. It does not include end-of-chapter exercises, review questions, programming exercise answers, original book text, PDFs, scans, or other copyrighted materials.

### Directory Convention

The repository is organized by chapter. Each chapter uses an independent directory:

```text
Chapter<chapter-number> <chapter-title>/
```

Each chapter directory contains:

```text
<program-listing-number>_<program-name>.cpp
CMakeLists.txt
```

For example:

```text
Chapter3 Dealing with Data/
|-- 3.1_limits.cpp
|-- 3.2_exceed.cpp
`-- CMakeLists.txt
```

The root directory only keeps project-level files:

```text
C++PrimePlus/
|-- Chapter2 Getting Started with C++/
|-- Chapter3 Dealing with Data/
|-- CMakeLists.txt
|-- LICENSE
|-- README.md
|-- .clang-format
`-- .gitignore
```

### CMake Organization

The root `CMakeLists.txt` only handles project-level configuration and includes chapter directories:

```cmake
add_subdirectory("Chapter2 Getting Started with C++")
add_subdirectory("Chapter3 Dealing with Data")
```

Each chapter-level `CMakeLists.txt` declares the executable targets for that chapter's program listings. For example:

```cmake
add_executable(limits 3.1_limits.cpp)
add_executable(exceed 3.2_exceed.cpp)
```

With this structure, adding a new program listing usually only requires:

- Adding a new `.cpp` file to the corresponding chapter directory.
- Adding the matching `add_executable(...)` entry to that chapter's `CMakeLists.txt`.
- Updating this README only when adding a new chapter, changing the directory convention, or changing the repository description.

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

In CLion, open the project root directory directly, wait for CMake to finish loading, and then select the target you want to run.

### Current Scope

The following chapters have been started:

| Chapter Directory | Content |
| --- | --- |
| `Chapter2 Getting Started with C++/` | Chapter 2: Getting Started with C++ |
| `Chapter3 Dealing with Data/` | Chapter 3: Dealing with Data |

The exact program listing files and executable targets are defined by the `.cpp` files and `CMakeLists.txt` inside each chapter directory.

### Repository Maintenance Rules

- Commit only source code, CMake configuration, formatting configuration, license, and documentation.
- Do not commit local build directories such as `cmake-build-debug/`, `build/`, and `out/`.
- Do not commit compiled artifacts such as `.exe`, `.obj`, and `.o`.
- Do not commit local IDE configuration directories such as `.idea/`.
- Keep this README as long-term documentation and avoid updating it for every newly added program listing.

### Copyright Notice

This repository is only for personal study records. The code in this repository is manually organized and written while studying the program listings. It does not include book text, scans, PDFs, or other copyrighted materials.
