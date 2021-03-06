---
description: 了解更多相关信息： Windows 套接字：流套接字
title: Windows 套接字：流套接字
ms.date: 11/04/2016
helpviewer_keywords:
- Windows Sockets [MFC], stream sockets
- sockets [MFC], stream sockets
- stream sockets [MFC]
ms.assetid: 31faaa34-a995-493f-a30b-b8115293d619
ms.openlocfilehash: b9e40be06ebb1de04466b5f13a46fe82fb3b0bd2
ms.sourcegitcommit: d6af41e42699628c3e2e6063ec7b03931a49a098
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97207639"
---
# <a name="windows-sockets-stream-sockets"></a>Windows 套接字：流套接字

本文介绍了作为两种可用的 Windows 套接字类型之一的流套接字。  (另一种类型是 [数据报套接字](../mfc/windows-sockets-datagram-sockets.md)。 ) 

流套接字适用于没有记录边界的数据流：可双向传输的字节流（应用程序是全双工的：它可以通过套接字进行传输和接收）。 流可以用于传递序列化的、无重复的数据。 （“序列化”表示数据包是按发送顺序传递的。 "无重复" 是指仅获取特定数据包一次。保证流消息 ) 接收，流非常适合处理大量数据。

网络传输层会将数据拆分或组合到大小合适的数据包中。 `CSocket` 类将为您处理打包和解包操作。

流基于显式连接：套接字 A 请求连接到套接字 B；套接字 B 接受或拒绝连接请求。

电话呼叫为流提供了一个很好的类比。 在正常情况下，接收方会按您说话的顺序听到您所说的内容，不会有重复或丢失。 例如，流套接字很合适文件传输协议 (FTP) 之类的实现，该协议可用于传输任意大小的 ASCII 或二进制文件。

当需要确保数据必须送达，且数据很大时，流套接字要优于数据报套接字。 有关流套接字的详细信息，请参阅 Windows 套接字规范。 Windows SDK 中提供了该规范。

若要向网络上的所有接收套接字广播，使用流套接字要优于旨在使用数据报套接字的应用程序，这是因为

- 广播模型会遇到网络洪水（或“风暴”）问题的限制。

- 随后采用的客户端-服务器模式更加高效。

- 流模型可提供可靠的数据传输，数据报模型则不能。

- 最终模型利用了在 Unicode 和 ANSI 套接字应用程序之间进行通信的能力，这种能力是 CArchive 类赋予 CSocket 类的。

    > [!NOTE]
    >  如果使用 `CSocket` 类，则必须使用流。 如果将套接字类型指定为 **SOCK_DGRAM**，则 MFC 断言会失败。

## <a name="see-also"></a>请参阅

[MFC 中的 Windows 套接字](../mfc/windows-sockets-in-mfc.md)<br/>
[Windows 套接字：背景](../mfc/windows-sockets-background.md)
