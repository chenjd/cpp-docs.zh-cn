---
title: “&lt;项目名&gt;属性页”对话框 ->“配置属性”->“清单工具”->“高级”
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCManifestTool.KeyFile
- VC.Project.VCManifestTool.UpdateFileHashes
- VC.Project.VCManifestTool.UpdateFileHashesSearchPath
- VC.Project.VCManifestTool.ValidateSignature
- VC.Project.VCManifestTool.KeyContainer
ms.assetid: 3d587366-05ea-4956-a978-313069660735
ms.openlocfilehash: 10da66c690106255d34c82b066f3450c5cc8a37a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50530554"
---
# <a name="advanced-manifest-tool-configuration-properties-ltprojectnamegt-property-pages-dialog-box"></a>“&lt;项目名&gt;属性页”对话框 ->“配置属性”->“清单工具”->“高级”

使用此对话框指定 [Mt.exe](https://msdn.microsoft.com/library/aa375649) 的高级选项。

若要访问此属性页对话框，请打开项目或属性表的属性页。 展开“配置属性”下的“清单工具节点”，然后选择“高级”。

## <a name="uielement-list"></a>UIElement 列表

- **更新文件哈希**

   使用 /hashupdate 选项，指定该清单工具将计算在 `<file>` 元素中指定的文件哈希，然后使用计算的值更新哈希特性。

- **更新文件哈希搜索路径**

   指定在 `<file>` 元素中引用的文件的搜索路径。 此选项也使用 /hashupdate 选项。

## <a name="see-also"></a>请参阅

[\<file> 元素](/visualstudio/deployment/file-element-clickonce-application)<br>
[ndptecclick](/visualstudio/deployment/clickonce-application-manifest)<br>
[清单工具属性页](../ide/manifest-tool-property-pages.md)<br>
[使用项目属性](../ide/working-with-project-properties.md)