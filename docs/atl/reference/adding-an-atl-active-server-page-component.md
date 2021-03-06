---
description: 了解详细信息：添加 ATL Active Server Page 组件
title: 添加 ATL Active Server Page 组件
ms.date: 05/09/2019
ms.assetid: 7be2204c-6e58-4099-8892-001b848c8987
ms.openlocfilehash: 4d56e7e55571ca477881175b5aa17e9a627edab6
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97165727"
---
# <a name="adding-an-atl-active-server-page-component"></a>添加 ATL Active Server Page 组件

::: moniker range="msvc-160"

ATL Active Server Page 组件向导在 Visual Studio 2019 及更高版本中不可用。

::: moniker-end

::: moniker range="<=msvc-150"

若要将活动模板库 (ATL) 对象添加到项目中，项目则必须已创建为 ATL COM 应用程序或者是包含 ATL 支持的 MFC 应用程序。 可以使用 [ATL 项目向导](../../atl/reference/atl-project-wizard.md)创建 ATL 应用程序，可以从[“添加类对话框”](../../ide/adding-a-class-visual-cpp.md#add-class-dialog-box)对话框中选择“向 MFC 添加 ATL 支持”，或者可以[将 ATL 对象添加到 MFC 应用程序](../../mfc/reference/adding-atl-support-to-your-mfc-project.md)来实现对 MFC 应用程序的 ATL 支持。

Active Server Pages 组件是 Internet Information Services 体系结构的一部分，此体系结构提供以下高级 Web 开发功能：

- 可以将 ASP 组件嵌入 HTML 页面中以创建独立于浏览器的动态内容。

- 可以使用 ASP 页面提供基于标准的数据库连接。

- 可以为基于 Web 的应用程序使用 ASP 错误处理功能。

## <a name="to-add-an-atl-active-server-pages-component-to-your-project"></a>将 ATL Active Server Pages 组件添加到项目中

1. 在“解决方案资源管理器”中，右键单击要向其添加 ATL Active Server Pages 组件的项目的名称。

1. 在快捷菜单中，单击 " **添加**"，然后单击 " **添加类**"。

1. 在[“添加类”](../../ide/adding-a-class-visual-cpp.md#add-class-dialog-box)对话框的“模板”窗格中，单击“ATL Active Server Page 组件”，然后单击“打开”以显示 [ATL Active Server Page 组件向导](../../atl/reference/atl-active-server-page-component-wizard.md)。

::: moniker-end

## <a name="see-also"></a>请参阅

[添加类](../../ide/adding-a-class-visual-cpp.md)<br/>
[在 ATL 项目中添加新接口](../../atl/reference/adding-a-new-interface-in-an-atl-project.md)<br/>
[向对象添加连接点](../../atl/adding-connection-points-to-an-object.md)<br/>
[添加方法](../../ide/adding-a-method-visual-cpp.md)<br/>
[MFC 类](../../mfc/reference/adding-an-mfc-class.md)<br/>
[添加一般 C++ 类](../../ide/adding-a-generic-cpp-class.md)
