---
description: 详细了解：编译器警告 (等级 2) C4250
title: 编译器警告（等级 2）C4250
ms.date: 11/04/2016
f1_keywords:
- C4250
helpviewer_keywords:
- C4250
ms.assetid: d47f7249-6b5a-414b-b2d4-56e5d246a782
ms.openlocfilehash: 04ffb555912c53cb4208cb82ba63c1424ef617e4
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97321860"
---
# <a name="compiler-warning-level-2-c4250"></a>编译器警告（等级 2）C4250

"class1"：通过控制继承 "class2：： member"

两个或多个成员具有相同的名称。 中的一个 `class2` 是继承的，因为它是包含此成员的其他类的基类。

若要取消 C4250，请使用 [警告](../../preprocessor/warning.md) 杂注。

由于虚拟基类在多个派生类之间共享，因此派生类中的名称支配基类中的名称。 例如，假设有以下类层次结构，则在菱形中继承了两个 func 定义： vbc：： func 通过弱类 ( # A1 实例，并通过主导类 ( # A3。 Func ( # A1 到钻石类对象的非限定调用始终调用 "为主导：： func ( # A3 实例"。  如果弱类要引入 func ( # A1 的实例，则这两个定义都不会成为主导的，并且调用会被标记为不明确。

## <a name="examples"></a>示例

```cpp
// C4250.cpp
// compile with: /c /W2
#include <stdio.h>
struct vbc {
   virtual void func() { printf("vbc::func\n"); }
};

struct weak : public virtual vbc {};

struct dominant : public virtual vbc {
   void func() { printf("dominant::func\n"); }
};

struct diamond : public weak, public dominant {};

int main() {
   diamond d;
   d.func();   // C4250
}
```

下面的示例生成 C4250。

```cpp
// C4250_b.cpp
// compile with: /W2 /EHsc
#include <iostream>
using namespace std;
class A {
public:
   virtual operator int () {
      return 2;
   }
};

class B : virtual public A {
public:
   virtual operator int () {
      return 3;
   }
};

class C : virtual public A {};

class E : public B, public C {};   // C4250

int main() {
   E eObject;
   cout << eObject.operator int() << endl;
}
```

此示例显示了更复杂的情况。 下面的示例生成 C4250。

```cpp
// C4250_c.cpp
// compile with: /W2 /EHsc
#include <iostream>
using namespace std;

class V {
public:
   virtual int f() {
      return 1024;
   }
};

class B : virtual public V {
public:
   int b() {
      return f(); // B::b() calls V::f()
   }
};

class M : virtual public V {
public:
   int f() {
      return 7;
   }
};

// because of dominance, f() is M::f() inside D,
// changing the meaning of B::b's f() call inside a D
class D : public B, public M {};   // C4250

int main() {
   D d;
   cout << "value is: " << d.b();   // invokes M::f()
}
```
