---
title: C/C++ 属性 (Linux C++)
ms.date: 10/14/2020
description: 介绍 Visual Studio C/C++ 属性页上的 Linux 编译选项
ms.assetid: 4bb8894b-c874-4a68-935e-b127d54e484f
f1_keywords: []
ms.openlocfilehash: b8cb1d8c6c585262e966c3015660adeaeab60307
ms.sourcegitcommit: 9c2b3df9b837879cd17932ae9f61cdd142078260
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/29/2020
ms.locfileid: "92924552"
---
# <a name="cc-properties-linux-c"></a>C/C++ 属性 (Linux C++)

::: moniker range="msvc-140"

Linux 支持在 Visual Studio 2017 及更高版本中提供。

::: moniker-end

::: moniker range=">=msvc-150"

## <a name="general"></a>常规

| properties | 说明 | 选项 |
|--|--|--|
| 附加包含目录 | 指定要添加到包含路径的一个或多个目录。 使用分号来分隔多个目录。 (-I\[path])。 |
| 调试信息格式 | 指定编译器生成的调试信息的类型。 | **无** - 没有生成调试信息，因此编译可能会更快。<br/>**最少的调试信息** - 生成了最少的调试信息。<br/>完全调试信息 (DWARF2) - 生成了 DWARF2 调试信息。<br/> |
| 对象文件名 | 指定用于重写默认对象文件名的名称。 该名称可以是文件名，也可以是目录名。 (-o [name])。 |
| 警告级别 | 选择编译器对代码错误的严格程度。  将其他标志直接添加到附加选项。 （/w、/Weverything）。 | 关闭所有警告 - 禁用所有编译器警告。<br/>EnableAllWarnings - 启用所有警告，包括默认情况下禁用的警告。<br/> |
| 将警告视为错误 | 将所有编译器警告视为错误。 对于新项目，最好在所有编译中使用 /Werror。 解决所有警告，确保可能存在的难以发现的代码缺陷尽可能最少。 |
| C 其他警告 | 定义一组其他警告消息。 |
| C++ 其他警告 | 定义一组其他警告消息。 |
| 启用详细模式 | 启用详细模式后，打印出更多信息以诊断生成。 |
| C 编译器 | 指定编译 C 源文件期间要调用的程序，或远程系统上 C 编译器的路径。 |
| C++ 编译器 | 指定编译 C++ 源文件期间要调用的程序，或远程系统上 C++ 编译器的路径。 |
| 编译超时 | 远程编译超时（毫秒）。 |
| 复制对象文件 | 指定是否要将编译对象文件从远程系统复制到本地计算机。 |
| 最大并行编译作业数 | 要在编译过程中并行创建的进程数。 默认值为 1。 如果使用的是适用于 Linux 的 Windows 子系统 (WSL) 版本 1，则该数量限制为 64。 |
| 验证体系结构 | 指定是否检查项目的目标平台是否与远程系统匹配。|
| 启用地址擦除器 | 使用地址擦除器来编译程序，这是一个快速内存错误检测器，可发现运行时内存问题（如释放后使用），并执行边界检查。|

## <a name="optimization"></a>Optimization

| properties | 说明 | 选项 |
|--|--|--|
| Optimization | 指定应用程序的优化级别。 | 自定义 - 自定义优化。<br/>禁用 - 禁用优化。<br/>使大小最小化 - 优化尺寸。<br/>使速度最大化 - 优化速度。<br/>完全优化 - 成本高昂的优化。 |
| 严格别名 | 假设使用最严格的别名规则。  一种类型的对象将始终不会被假定具有与另一种类型的对象相同的地址。 |
| 展开循环 | 展开循环，以便以更大的代码大小为代价减少执行的分支数，从而使应用程序更快。 |
| 链接时间优化 | 通过允许优化器跨应用程序中的对象文件进行查看，来实现过程间优化。 |
| 省略框架指针 | 禁止在调用堆栈上创建帧指针。 |
| 无公共块 | 在对象文件的数据节中分配甚至取消初始化的全局变量，而不是以公共块的形式生成它们。 |

## <a name="preprocessor"></a>预处理器

| properties | 说明 |
|--|--|
| 预处理器定义 | 为源文件定义预处理符号。 (-D) |
| 取消定义预处理器定义 | 指定取消定义一个或多个预处理器。  (-U \[macro]) |
| 取消所有预处理器定义 | 取消定义以前定义的所有预处理器值。  (-undef) |
| 显示包含文件 | 生成包含文件的列表及编译器输出。  (-H) |

## <a name="code-generation"></a>代码生成

| properties | 说明 | 选项 |
|--|--|--|
| 位置无关代码 | 生成位置无关代码 (PIC) 以便在共享库中使用。 |
| 静态变量是线程安全的 | 发出额外代码以使用 C++ ABI 中指定的例程，实现局部静态变量的线程安全初始化。 | 否 - 禁用线程安全的静态变量。<br/>是 - 启用线程安全的静态变量。 |
| 浮点优化 | 通过放宽 IEEE-754 合规性来实现浮点优化。 |
| 内联方法已隐藏 | 启用时，内联方法的外联副本声明为 `private extern`。 |
| 默认隐藏的符号 | 除非使用 `__attribute` 宏明确标记为导出，否则所有符号都声明为 `private extern`。 |
| 启用 C++ 异常 | 指定编译器使用的异常处理模型。 | 否 - 禁用异常处理。<br/>**是** - 启用异常处理。 |

## <a name="language"></a>语言

| properties | 说明 | 选项 |
|--|--|--|
| 启用运行时类型信息 | 添加在运行时检查 C++ 对象类型（运行时类型信息）的代码。     （frtti、fno-rtti） |
| C 语言标准 | 确定 C 语言标准。 | **默认**<br/>C89 - C89 语言标准。<br/>C99 - C99 语言标准。<br/>C11 - C11 语言标准。<br/>C99 (GNU Dialect) - C99 (GNU Dialect) 语言标准。<br/>C11 (GNU Dialect) - C11 (GNU Dialect) 语言标准。 |
| C++ 语言标准 | 确定 C++ 语言标准。 | **默认**<br/>C++03 - C++03 语言标准。<br/>C++11 - C++11 语言标准。<br/>C++14 - C++14 语言标准。<br/>C++03 (GNU Dialect) - C++03 (GNU Dialect) 语言标准。<br/>C++11 (GNU Dialect) - C++11 (GNU Dialect) 语言标准。<br/>C++14 (GNU Dialect) - C++14 (GNU Dialect) 语言标准。 |

## <a name="advanced"></a>高级

| properties | 说明 | 选项 |
|--|--|--|
| 编译为 | 选择 .c 和 .cpp 文件的编译语言选项。 （-x c、-x c++） | 默认 - 根据 .c 或 .cpp 扩展名进行检测。<br/>编译为 C 代码 - 编译为 C 代码。<br/>编译为 C++ 代码 - 编译为 C++ 代码。 |
| 强制包含文件 | 指定一个或多个强制包含文件 (-include \[name]) |

::: moniker-end
