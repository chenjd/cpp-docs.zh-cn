---
title: 创建纯资源 DLL
ms.date: 11/04/2016
helpviewer_keywords:
- resource-only DLLs [C++], creating
- DLLs [C++], creating
ms.assetid: e6b1d4da-7275-467f-a58c-a0a8a5835199
ms.openlocfilehash: 9a31d4197e71fb6cf20a0ecfce778552357d7e06
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50612909"
---
# <a name="creating-a-resource-only-dll"></a>创建纯资源 DLL

纯资源 DLL 是一个 DLL 包含资源，如图标、 位图、 字符串和对话框。 使用纯资源 DLL 是共享相同的资源分到多个程序集的好方法。 它还是提供多种语言的本地化资源的应用程序的好方法 (请参阅[MFC 应用程序中的本地化资源： 附属 Dll](../build/localized-resources-in-mfc-applications-satellite-dlls.md))。

若要创建纯资源 DLL，请创建新的 Win32 DLL (非 MFC) 项目，并将资源添加到项目。

- 选择在 Win32 项目**新的项目**对话框框，并在 Win32 项目向导中指定的 DLL 项目类型。

- 为 DLL 创建一个包含资源 （如字符串或菜单） 的新资源脚本并保存.rc 文件。

- 上**项目**菜单上，单击**添加现有项**，然后将新的.rc 文件插入到项目。

- 指定[/NOENTRY](../build/reference/noentry-no-entry-point.md)链接器选项。 /NOENTRY 可防止链接器的引用链接`_main`dll; 需要此选项来创建纯资源 DLL。

- 生成 DLL。

使用纯资源 DLL 的应用程序应调用[LoadLibrary](../build/loadlibrary-and-afxloadlibrary.md)显式链接到 DLL。 若要访问的资源，调用泛型函数`FindResource`和`LoadResource`，这适用于任何类型的资源，或调用以下特定于资源的函数之一：

- `FormatMessage`

- `LoadAccelerators`

- `LoadBitmap`

- `LoadCursor`

- `LoadIcon`

- `LoadMenu`

- `LoadString`

应用程序应调用`FreeLibrary`完成时使用的资源。

## <a name="see-also"></a>请参阅

[使用资源文件](../windows/working-with-resource-files.md)<br/>
[Visual C++ 中的 DLL](../build/dlls-in-visual-cpp.md)