---
description: 了解更多：编译器错误 C3874
title: 编译器错误 C3874
ms.date: 11/04/2016
f1_keywords:
- C3874
helpviewer_keywords:
- C3874
ms.assetid: fd55fc05-69a7-4237-b3b7-dca1d5400b4f
ms.openlocfilehash: c9e0b498d5daf5066c0e224c99dc6af47d689adc
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97274562"
---
# <a name="compiler-error-c3874"></a>编译器错误 C3874

"function" 的返回类型应为 "int" 而不是 "type"

函数没有编译器所需的返回类型。

下面的示例生成 C3874：

```cpp
// C3874b.cpp
double main()
{   // C3874
}
```
