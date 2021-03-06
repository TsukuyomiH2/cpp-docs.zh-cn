---
description: 了解详细信息：链接器工具警告 LNK4006
title: 链接器工具警告 LNK4006
ms.date: 11/04/2016
f1_keywords:
- LNK4006
helpviewer_keywords:
- LNK4006
ms.assetid: 3a637d17-1676-4ea6-bd8b-290137d28d3b
ms.openlocfilehash: 526b3f380ef7e05448280094f360c145d7f21c04
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97332011"
---
# <a name="linker-tools-warning-lnk4006"></a>链接器工具警告 LNK4006

已在对象中定义了符号;已忽略第二个定义

以修饰形式显示的给定 `symbol` 被多次定义。 遇到此警告时， `symbol` 将添加两次，但只使用其第一个窗体。

如果尝试将两个导入库合并为一个，则可以收到此警告。

如果要重新生成 C 运行时库，可以忽略此消息。

### <a name="to-fix-by-using-the-following-possible-solutions"></a>使用以下可能的解决方案进行修复

1. 给定的 `symbol` 可能是通过使用 [/gy](../../build/reference/gy-enable-function-level-linking.md)编译创建的打包函数。 此符号包含在多个文件中，但在两个编译之间发生了更改。 重新编译包含的所有文件 `symbol` 。

1. 给定的 `symbol` 在不同库中的两个成员对象中的定义可能不同。

1. 绝对可能定义了两次，每个定义中的值不同。

1. 如果在组合库时接收到错误消息，则 `symbol` 在要添加到的库中已经存在。
