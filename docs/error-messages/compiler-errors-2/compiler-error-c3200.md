---
description: 了解更多：编译器错误 C3200
title: 编译器错误 C3200
ms.date: 11/04/2016
f1_keywords:
- C3200
helpviewer_keywords:
- C3200
ms.assetid: 44bb5e77-f0ec-421c-a732-b9ee7c0a3529
ms.openlocfilehash: c693878628ff0bd9dddcb2f100ca652910b0fb89
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97330660"
---
# <a name="compiler-error-c3200"></a>编译器错误 C3200

"template"：模板参数 "parameter" 的模板参数无效，应为类模板

向类模板传递的参数无效。 类模板需要模板作为参数。 在下面的示例中，调用 `Y<int, int> aY` 将生成 C3200。 第一个参数必须是模板，如 `Y<X, int> aY` 。

```cpp
// C3200.cpp
template<typename T>
class X
{
};

template<template<typename U> class T1, typename T2>
class Y
{
};

int main()
{
   Y<int, int> y;   // C3200
}
```
