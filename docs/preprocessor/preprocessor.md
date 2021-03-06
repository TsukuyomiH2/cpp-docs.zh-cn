---
description: 了解更多：预处理器
title: 预处理器
ms.date: 08/29/2019
helpviewer_keywords:
- preprocessor
ms.assetid: e120eda3-b413-49f1-a07c-e9fb128cf500
ms.openlocfilehash: dd79766777926871e7bbf849f96420ef37052eba
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97202075"
---
# <a name="preprocessor"></a>预处理器

预处理器是将源文件的文本作为翻译的第一阶段操作的文本处理器。 预处理器不会分析源文本，但会将其分解为标记以定位宏调用。 尽管编译器一般会在其第一个传递中调用预处理器，但还是可以为了在不进行编译的情况下处理文本而单独调用预处理器。

预处理器的参考材料包括下列部分：

- [预处理器指令](../preprocessor/preprocessor-directives.md)

- [预处理器运算符](../preprocessor/preprocessor-operators.md)

- [预定义宏](../preprocessor/predefined-macros.md)

- [杂注](../preprocessor/pragma-directives-and-the-pragma-keyword.md)

**Microsoft 专用**

您可以在使用 [/e](../build/reference/e-preprocess-to-stdout.md) 或 [/EP](../build/reference/ep-preprocess-to-stdout-without-hash-line-directives.md) 编译器选项进行预处理后获取源代码的列表。 这两个选项都调用预处理器，并将生成的文本发送到标准输出设备（在大多数情况下为控制台）。 这两个选项之间的区别是 `/E` 包含 `#line` 指令，并将 `/EP` 这些指令抽出。

**结束 Microsoft 专用**

## <a name="special-terminology"></a><a name="_predir_special_terminology"></a> 特殊术语

在预处理器文档中，术语“自变量”指传递给函数的实体。 在某些情况下，它由 "实际" 或 "正式" 修改，后者描述函数调用中指定的参数表达式，以及在函数定义中指定的参数声明。

术语“变量”指简单的 C 类型数据对象。 术语 "对象" 指 c + + 对象和变量;这是一个包含项。

## <a name="see-also"></a>请参阅

[C/C++ 预处理器参考](../preprocessor/c-cpp-preprocessor-reference.md)\
[转换阶段](../preprocessor/phases-of-translation.md)
