---
description: 了解更多：编译器错误 C2498
title: 编译器错误 C2498
ms.date: 11/04/2016
f1_keywords:
- C2498
helpviewer_keywords:
- C2498
ms.assetid: 0839f12c-aaa4-4a02-bb33-7f072715dd14
ms.openlocfilehash: e7cbb811cdaeea703d0f1da1c0f2012ebe8210fa
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97335096"
---
# <a name="compiler-error-c2498"></a>编译器错误 C2498

"function"： "novtable" 只能应用于类声明或定义

使用函数时，可能会导致此错误 `__declspec(novtable)` 。

## <a name="example"></a>示例

下面的示例生成 C2498：

```cpp
// C2498.cpp
// compile with: /c
void __declspec(novtable) f() {}   // C2498
class __declspec(novtable) A {};   // OK
```
