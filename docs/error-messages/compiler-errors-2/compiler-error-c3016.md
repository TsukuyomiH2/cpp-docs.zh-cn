---
description: 了解更多：编译器错误 C3016
title: 编译器错误 C3016
ms.date: 11/04/2016
f1_keywords:
- C3016
helpviewer_keywords:
- C3016
ms.assetid: 3423467e-e8bb-4f35-b4db-7925cafa74c1
ms.openlocfilehash: e45425946993caa43cfaf1a19730ef5414a6f2d5
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97285859"
---
# <a name="compiler-error-c3016"></a>编译器错误 C3016

“var”: OpenMP "for" 语句中的索引变量必须是有符号的整型

OpenMP 语句中的索引变量 **`for`** 必须是有符号整数类型。

下面的示例生成 C3016：

```cpp
// C3016.cpp
// compile with: /openmp
int main()
{
   #pragma omp parallel
   {
      unsigned int i = 0;
      // Try the following line instead:
      // int i = 0;

      #pragma omp for
      for (i = 0; i <= 10; ++i)   // C3016
      {
      }
   }
}
```
