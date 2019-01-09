---
title: 内存管理：堆分配
ms.date: 11/04/2016
helpviewer_keywords:
- memory [MFC], detecting leaks
- delete operator [MFC], using with debug MFC
- heap allocation [MFC], described
- memory allocation [MFC], heap memory
- memory leaks [MFC], detecting
- new operator [MFC], using with debug MFC
- heap allocation [MFC]
- detecting memory leaks [MFC]
ms.assetid: a5d949c6-1b79-476e-9c66-513a558203d9
ms.openlocfilehash: 0c669fa611193b9a04e4854c84dec604e585991c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50641150"
---
# <a name="memory-management-heap-allocation"></a>内存管理：堆分配

堆被保留以用于程序的内存分配需求。 它是程序代码和堆栈之外的区域。 典型的 C 程序使用 malloc 函数和 free 函数来分配和释放堆内存。 MFC 的 Debug 版本提供了C ++内置运算符**new**和**delete**的修改版本，用于在堆内存中分配和释放对象。

当您使用**new**和**delete**而不是**malloc**和**free**时，您可以利用类库的内存管理调试增强功能，这对于检测内存泄漏非常有用。 使用 MFC 的 Release 版本构建程序时，**new**和**delete**运算符的标准版本提供了分配和释放内存的有效方法（MFC的Release版本不提供这些运算符的修改版本）。

请注意，堆上分配的对象的总大小仅受系统的可用虚拟内存的限制。

## <a name="see-also"></a>请参阅

[内存管理](../mfc/memory-management.md)

