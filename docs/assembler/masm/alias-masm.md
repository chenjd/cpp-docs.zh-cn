---
title: ALIAS (MASM)
ms.date: 08/30/2018
f1_keywords:
- Alias
helpviewer_keywords:
- ALIAS directive
ms.assetid: d9725c49-58de-41da-ab01-b06a56cf5cf2
ms.openlocfilehash: ab00092f410d34119e876db4562e6d0709743d79
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50483494"
---
# <a name="alias-masm"></a>ALIAS (MASM)

**别名**指令创建一个函数的替代名称。  这样可以创建多个名称对于函数，或创建库，使链接器 (LINK.exe) 以将旧函数映射到一个新的函数。

## <a name="syntax"></a>语法

> 别名\<*别名*> = \<*实际名称*>

#### <a name="parameters"></a>参数

*实际名称*<br/>
函数或过程的实际名称。  在尖括号内是必需的。

*alias*<br/>
备用或别名的名称。  在尖括号内是必需的。

## <a name="see-also"></a>请参阅

[指令参考](../../assembler/masm/directives-reference.md)<br/>