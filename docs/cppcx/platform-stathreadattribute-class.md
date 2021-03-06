---
description: 了解详细信息： Platform：： STAThreadAttribute 类
title: Platform::STAThreadAttribute 类
ms.date: 12/30/2016
ms.topic: reference
f1_keywords:
- COLLECTION/Platform::Platform
- COLLECTION/Platform::Platform::STAThreadAttribute constructor 1
- COLLECTION/Platform::Platform::STAThreadAttribute::Equals
- COLLECTION/Platform::Platform::STAThreadAttribute::GetHashCode
- COLLECTION/Platform::Platform::STAThreadAttribute::ToString
helpviewer_keywords:
- Platform::STAThreadAttribute Class
ms.assetid: f97960fc-e673-4d9e-910a-54c8415411c4
ms.openlocfilehash: a1c235ef9a171e650c960df184b081c4b6511cf1
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97307998"
---
# <a name="platformstathreadattribute-class"></a>Platform::STAThreadAttribute 类

指示应用程序的线程模型是单线程单元 (STA)。

## <a name="syntax"></a>语法

```
public ref class STAThreadAttribute sealed : Attribute
```

### <a name="members"></a>成员

### <a name="public-constructors"></a>公共构造函数

|“属性”|描述|
|----------|-----------------|
|[STAThreadAttribute 构造函数 1](#ctor)|初始化类的新实例。|

### <a name="public-methods"></a>公共方法

STAThreadAttribute 属性继承自 [Platform：： Object 类](../cppcx/platform-object-class.md)。 STAThreadAttribute 还会重载或具有以下成员：

|名称|描述|
|----------|-----------------|
|[STAThreadAttribute::Equals](#equals)|确定指定对象是否等于当前对象。|
|[STAThreadAttribute::GetHashCode](#gethashcode)|返回此实例的哈希代码。|
|[STAThreadAttribute::ToString](#tostring)|返回表示当前对象的字符串。|

## <a name="inheritance-hierarchy"></a>继承层次结构

`Platform`

### <a name="requirements"></a>要求

**标头：** 集合。h

**命名空间：** Platform

## <a name="stathreadattribute-constructor"></a><a name="ctor"></a> STAThreadAttribute constructor

初始化 STAThreadAttribute 类的新实例。

### <a name="syntax"></a>语法

```cpp
public:STAThreadAttribute();
```

## <a name="stathreadattributeequals"></a><a name="equals"></a> STAThreadAttribute：： Equals

确定指定对象是否等于当前对象。

### <a name="syntax"></a>语法

```cpp
public:virtual override bool Equals( Object^ obj );
```

### <a name="parameters"></a>参数

*obj*<br/>
要比较的对象。

### <a name="return-value"></a>返回值

**`true`** 如果对象相等，则为; 否则为。否则为 **`false`** 。

## <a name="stathreadattributegethashcode"></a><a name="gethashcode"></a> STAThreadAttribute：： GetHashCode

返回此实例的哈希代码。

### <a name="syntax"></a>语法

```cpp
public:int GetHashCode();
```

### <a name="return-value"></a>返回值

此实例的哈希代码。

## <a name="stathreadattributetostring"></a><a name="tostring"></a> STAThreadAttribute：： ToString

返回表示当前对象的字符串。

### <a name="syntax"></a>语法

```cpp
public:String^ ToString();
```

### <a name="return-value"></a>返回值

表示当前对象的字符串。

## <a name="see-also"></a>请参阅

[平台命名空间](platform-namespace-c-cx.md)
