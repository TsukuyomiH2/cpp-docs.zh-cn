---
description: 详细了解：编译器警告 (级别 4) C4610
title: 编译器警告（等级 4）C4610
ms.date: 11/04/2016
f1_keywords:
- C4610
helpviewer_keywords:
- C4610
ms.assetid: 23c1a16c-9ca9-4bf6-9911-a72b785560c2
ms.openlocfilehash: 6a655cbafc330738747120b3e768e06eefd6fcc0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97168301"
---
# <a name="compiler-warning-level-4-c4610"></a>编译器警告（等级 4）C4610

对象 "class" 永远不能实例化-需要用户定义的构造函数

类没有用户定义的构造函数或默认构造函数。 不执行实例化。 下面的示例生成 C4610：

```cpp
// C4610.cpp
// compile with: /W4
struct A {
   int &j;

   A& A::operator=( const A& );
};   // C4610

/* use this structure definition to resolve the warning
struct B {
   int &k;

   B(int i = 0) : k(i) {
   }

   B& B::operator=( const B& );
} b;
*/

int main() {
}
```
