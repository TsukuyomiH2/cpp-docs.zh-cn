---
description: 了解详细信息： C/c + + 代码分析概述
title: C/C++ 代码分析概述
ms.date: 04/28/2018
ms.topic: conceptual
helpviewer_keywords:
- annotations, code analysis
- build integration, code analysis
- C/C++ code analysis
- IDE, code analysis
- pragma directive, code analysis
- code analysis, C/C++
- code analysis tool
- command line, code analysis
- C++, code analysis
- check-in policies, code analysis
- '#pragma directives, code analysis'
- C, code analysis
ms.assetid: 81f0c9e8-f471-4de5-aac4-99db336a8809
ms.openlocfilehash: 4d018185e74926c880f8a174eb81cea344167782
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97323296"
---
# <a name="code-analysis-for-cc-overview"></a>C/C++ 代码分析概述

C/c + + 代码分析工具提供有关 C/c + + 源代码中可能存在的缺陷的信息。 工具报告的常见编码错误包括缓冲区溢出、内存未初始化、null 指针取消引用以及内存和资源泄漏。 该工具还可以对 [C++ Core Guidelines](https://github.com/isocpp/CppCoreGuidelines/blob/master/CppCoreGuidelines.md)运行检查。

## <a name="ide-integrated-development-environment-integration"></a>IDE (集成开发环境) 集成

代码分析工具完全集成在 Visual Studio IDE 中。

在生成过程中，源代码产生的任何警告都显示在错误列表中。 你可以导航到导致该警告的源代码并查看更多信息，了解相关原因和找出问题可能的解决方案。

## <a name="command-line-support"></a>命令行支持

还可以从命令行使用分析工具，如以下示例中所示：

```cmd
C:\>cl /analyze Sample.cpp
```

**Visual Studio 2017 版本15.7 及更高版本：** 你可以从命令行运行该工具，其中包含任何生成系统，包括 CMake。

## <a name="pragma-support"></a>#pragma 支持

您可以使用 `#pragma` 指令将警告视为错误; 启用或禁用警告，并禁止显示单个代码行的警告。 有关详细信息，请参阅 [Pragma 指令和 __Pragma 关键字](../preprocessor/pragma-directives-and-the-pragma-keyword.md)。

## <a name="annotation-support"></a>批注支持

注释可以提高代码分析的准确性。 注释可以提供有关函数参数和返回类型的先决条件和后置条件的其他信息。 有关详细信息，请参阅 [使用 SAL 注释减少 C/c + + 代码缺陷](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)。

## <a name="run-analysis-tool-as-part-of-check-in-policy"></a>根据签入策略运行代码分析

建议要求所有源代码签入均满足特定策略。 具体而言，建议确保在最近的本地生成过程中运行分析。 有关启用代码分析签入策略的详细信息，请参阅 [创建和使用代码分析 Check-In 策略](/visualstudio/code-quality/how-to-create-or-update-standard-code-analysis-check-in-policies)。

## <a name="team-build-integration"></a>Team Build 集成

在 Azure DevOps 生成过程中，可以使用生成系统的集成功能来运行代码分析工具。 有关详细信息，请参阅 [Azure Pipelines](/azure/devops/pipelines/index)。

## <a name="see-also"></a>请参阅

- [快速入门： C/c + + 代码分析](quick-start-code-analysis-for-c-cpp.md)
- [演练：分析 C/c + + 代码的缺陷](walkthrough-analyzing-c-cpp-code-for-defects.md)
- [C/C++ 代码分析警告](code-analysis-for-c-cpp-warnings.md)
- [使用 C++ Core Guidelines 检查器](using-the-cpp-core-guidelines-checkers.md)
- [C++ Core Guidelines 检查器参考](code-analysis-for-cpp-corecheck.md)
- [使用规则集指定要运行的 c + + 规则](using-rule-sets-to-specify-the-cpp-rules-to-run.md)
- [使用代码分析工具分析驱动程序质量](/windows-hardware/drivers/develop/analyzing-driver-quality-by-using-code-analysis-tools)
- [驱动程序的代码分析警告](/windows-hardware/drivers/devtest/prefast-for-drivers-warnings)
