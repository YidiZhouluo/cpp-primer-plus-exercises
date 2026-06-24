# C++ Primer Plus Exercises

## 中文说明

### 项目简介

这个仓库用于记录我学习《C++ Primer Plus》过程中的代码练习。项目使用 CMake 管理多个独立的 C++ 示例程序，并主要在 CLion 中编写、构建和运行。

### 功能与内容

- 按章节整理 C++ 示例代码和练习代码。
- 每个练习文件通常对应一个独立的可执行程序。
- 使用 `CMakeLists.txt` 统一管理构建目标。
- 使用 `.clang-format` 保持代码格式一致。

### 项目结构

```text
C++PrimePlus/
├── Chapter2_Getting Started with C++/
│   ├── 2.1_myfirst.cpp
│   ├── 2.2_carrots.cpp
│   ├── 2.3_getinfo.cpp
│   └── 2.4_sqrt.cpp
├── CMakeLists.txt
├── main.cpp
├── .clang-format
├── .gitignore
└── README.md
```

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

构建完成后，可以在生成的 `build` 目录中运行对应的可执行文件。

在 CLion 中，可以直接打开项目根目录，等待 CMake 加载完成后选择对应的运行目标。

### 当前练习进度

- Chapter 2: Getting Started with C++

### 仓库维护规范

- 只提交源代码、CMake 配置、格式化配置和说明文档。
- 不提交本地构建目录，例如 `cmake-build-debug/`、`build/`。
- 不提交编译产物，例如 `.exe`、`.obj`、`.o`。
- 不提交本地 IDE 配置目录，例如 `.idea/`。

### 版权说明

本仓库仅包含个人学习过程中编写的练习代码。请勿上传书籍原文、扫描件、PDF 或其他受版权保护的材料。

---

## English

### Project Overview

This repository records my code exercises while studying *C++ Primer Plus*. The project uses CMake to manage multiple independent C++ example programs and is mainly written, built, and run in CLion.

### Features and Content

- Organizes C++ example and exercise code by chapter.
- Each exercise file usually corresponds to an independent executable program.
- Uses `CMakeLists.txt` to manage build targets.
- Uses `.clang-format` to keep code formatting consistent.

### Project Structure

```text
C++PrimePlus/
├── Chapter2_Getting Started with C++/
│   ├── 2.1_myfirst.cpp
│   ├── 2.2_carrots.cpp
│   ├── 2.3_getinfo.cpp
│   └── 2.4_sqrt.cpp
├── CMakeLists.txt
├── main.cpp
├── .clang-format
├── .gitignore
└── README.md
```

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

After the build is complete, run the corresponding executable file in the generated `build` directory.

In CLion, open the project root directory directly, wait for CMake to finish loading, and then select the target you want to run.

### Current Progress

- Chapter 2: Getting Started with C++

### Repository Maintenance Rules

- Commit only source code, CMake configuration, formatting configuration, and documentation.
- Do not commit local build directories such as `cmake-build-debug/` and `build/`.
- Do not commit compiled artifacts such as `.exe`, `.obj`, and `.o`.
- Do not commit local IDE configuration directories such as `.idea/`.

### Copyright Notice

This repository only contains exercise code written during personal study. Do not upload book text, scans, PDFs, or other copyrighted materials.
