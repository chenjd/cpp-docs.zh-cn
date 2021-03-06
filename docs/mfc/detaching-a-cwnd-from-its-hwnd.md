---
title: 将 CWnd 从其 HWND 中分离出来
ms.date: 11/04/2016
f1_keywords:
- CWnd
helpviewer_keywords:
- HWND, detaching CWnd from
- removing HWNDs from CWnds
- CWnd objects [MFC], detaching from HWND
- detaching CWnds from HWNDs
- Detach method (CWnd class)
ms.assetid: 6efadf84-0517-4a3f-acfd-216e088f19c6
ms.openlocfilehash: fe4d9efa6adcec51d5944755e4a8abb1cc0784e4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50653968"
---
# <a name="detaching-a-cwnd-from-its-hwnd"></a>将 CWnd 从其 HWND 中分离出来

如果需要绕过的对象-`HWND`关系，MFC 提供了另一个`CWnd`成员函数[分离](../mfc/reference/cwnd-class.md#detach)，这与 Windows 窗口断开连接的 c + + 窗口对象。 这可以防止析构函数销毁对象时销毁 Windows 窗口。

## <a name="what-do-you-want-to-know-more-about"></a>你想要了解更多信息

- [创建窗口](../mfc/creating-windows.md)

- [窗口析构序列](../mfc/window-destruction-sequence.md)

- [分配和取消分配窗口内存](../mfc/allocating-and-deallocating-window-memory.md)

## <a name="see-also"></a>请参阅

[窗口对象](../mfc/window-objects.md)

