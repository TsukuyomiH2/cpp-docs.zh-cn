---
description: 了解详细信息：编译器警告 (等级 1) C4237
title: 编译器警告（等级 1）C4237
ms.date: 11/04/2016
f1_keywords:
- C4237
helpviewer_keywords:
- C4237
ms.assetid: f2e86c4b-80d8-460e-9429-83c5f3f5d7ca
ms.openlocfilehash: a83c40d54a5bd711fbc399ac4880a211f3cf9bd7
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97266242"
---
# <a name="compiler-warning-level-1-c4237"></a>编译器警告（等级 1）C4237

"关键字" 关键字目前尚不受支持，但保留以供将来使用

C + + 规范中的关键字未在 Microsoft c + + 编译器中实现，但关键字不可用作用户定义的符号。

下面的示例生成 C4237：

```cpp
// C4237.cpp
// compile with: /W1 /c
int export;   // C4237
```
