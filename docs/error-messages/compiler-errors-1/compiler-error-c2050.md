---
description: 了解更多：编译器错误 C2050
title: 编译器错误 C2050
ms.date: 11/04/2016
f1_keywords:
- C2050
helpviewer_keywords:
- C2050
ms.assetid: 66aaed7d-00db-4ce1-a9d6-4447c1cf07ce
ms.openlocfilehash: a6e6221b0985ee509953b517ae04de9f0962fe3a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97175035"
---
# <a name="compiler-error-c2050"></a>编译器错误 C2050

switch 表达式不是整型

**`switch`** 表达式的计算结果为非整数值。 若要解决此错误，请在 switch 语句中仅使用整数值。

下面的示例生成 C2050：

```cpp
// C2050.cpp
int main() {
   int a = 1;
   switch ("a") {   // C2050
      case 1:
         a = 0;
      default:
         a = 2;
   }
}
```

可能的解决方法：

```cpp
// C2050b.cpp
int main() {
   int a = 1;
   switch (a) {
      case 1:
         a = 0;
      default:
         a = 2;
   }
}
```
