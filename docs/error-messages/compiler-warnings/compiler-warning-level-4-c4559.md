---
description: 详细了解：编译器警告 (级别 4) C4559
title: 编译器警告（等级 4）C4559
ms.date: 08/27/2018
f1_keywords:
- C4559
helpviewer_keywords:
- C4559
ms.assetid: ed542f60-454d-45cb-85da-987ede61b1ab
ms.openlocfilehash: 64a8da1a7719d515cc9ddb7b5b6c3e54309ef6cb
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97206625"
---
# <a name="compiler-warning-level-4-c4559"></a>编译器警告（等级 4）C4559

> "*function*"：重定义;函数获取 __declspec (*修饰符*) 

## <a name="remarks"></a>备注

重定义或重新声明了一个函数，但第二个定义或声明添加了 **`__declspec`** 修饰符 (*修饰符*) 。 此警告为信息性。 若要修复此警告，请删除其中一个定义。

## <a name="example"></a>示例

下面的示例生成 C4559：

```cpp
// C4559.cpp
// compile with: /W4 /LD
void f();
__declspec(noalias) void f();   // C4559
```
