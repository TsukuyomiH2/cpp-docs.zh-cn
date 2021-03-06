---
description: 了解详细信息： (UAC) 的用户帐户控制如何影响应用程序
title: 用户帐户控制 (UAC) 如何影响应用程序
ms.date: 11/19/2018
helpviewer_keywords:
- UAC [C++]
- security [C++], User Account Control
- user accounts [C++]
- User Account Control [C++]
ms.assetid: 0d001870-253e-4989-b689-f78035953799
ms.openlocfilehash: 64196e0cac0a5b4edcf0b24fd95df2e5291ec45a
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97320061"
---
# <a name="how-user-account-control-uac-affects-your-application"></a>用户帐户控制 (UAC) 如何影响应用程序

用户帐户控制 (UAC) 是 Windows Vista 的一项功能，其中用户帐户具有有限的特权。 可以在下列站点找到关于 UAC 的详细信息：

- [最小特权环境中应用程序的开发人员最佳实践和指南](/windows/win32/uxguide/winenv-uac)

## <a name="building-projects-after-enabling-uac"></a>在启用 UAC 后生成项目

如果在禁用了 UAC 的情况下在 Windows Vista 上生成 Visual Studio c + + 项目，并且稍后启用了 UAC，则必须清除并重新生成项目，以使其能够正常工作。

## <a name="applications-that-require-administrative-privileges"></a>需要管理特权的应用程序

默认情况下，Visual C++ 链接器将 UAC 片段嵌入到执行级别为的应用程序的清单中 `asInvoker` 。 如果应用程序需要管理特权才能正确运行（例如，修改注册表的 HKLM 节点或者写入磁盘的受保护区域，如 Windows 目录），则必须修改应用程序。

第一种方法是修改清单的 UAC 片段，将执行级别更改为 *requireAdministrator*。 然后，应用程序在运行之前将提示用户提供管理凭据。 有关如何执行此操作的信息，请参阅 [/MANIFESTUAC (将 UAC 信息嵌入清单) ](../build/reference/manifestuac-embeds-uac-information-in-manifest.md)。

第二个选项是通过指定 `/MANIFESTUAC:NO` 链接器选项不将 UAC 片段嵌入到清单。 在这种情况下，应用程序将以虚拟化方式运行。 在应用程序结束后，对注册表或文件系统的任何更改将不会保留。

下面的流程图描述了应用程序的运行方式取决于是否启用了 UAC 和应用程序是否有 UAC 清单：

![Windows 加载程序行为](media/uacflowchart.png "Windows 加载程序行为")

## <a name="see-also"></a>请参阅

[安全最佳实践](security-best-practices-for-cpp.md)
