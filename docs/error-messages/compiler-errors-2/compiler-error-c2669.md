---
description: 了解更多：编译器错误 C2669
title: 编译器错误 C2669
ms.date: 11/04/2016
f1_keywords:
- C2669
helpviewer_keywords:
- C2669
ms.assetid: f9cb8111-bcdc-484b-a863-2c42e15a0496
ms.openlocfilehash: 01b40131a2eef4ff83d10c5088b2cae3eb7e55e0
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97210642"
---
# <a name="compiler-error-c2669"></a>编译器错误 C2669

匿名联合中不允许使用成员函数

[匿名联合](../../cpp/unions.md#anonymous_unions) 不能具有成员函数。

## <a name="example"></a>示例

下面的示例生成 C2669：

```cpp
// C2669.cpp
struct X {
   union {
      int i;
      void f() {   // C2669, remove function
         i = 0;
      }
   };
};
```
