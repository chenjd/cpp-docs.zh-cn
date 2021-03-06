---
title: 远程生成事件 (Linux c + +)
ms.date: 9/26/2017
ms.assetid: 165d3690-5bd8-4b0b-bc66-8b699d85a61b
ms.openlocfilehash: 87647948b641fff7370003a59775a5680c176fb3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50653864"
---
# <a name="build-event-properties-linux-c"></a>生成事件属性 (Linux C++)

## <a name="pre-build-event"></a>预生成事件

属性 | 描述
--- | ---
命令行 | 指定让预生成事件工具运行的命令行。
描述 | 指定让预生成事件工具显示的说明。
在生成中使用 | 指定是否将该生成事件从当前配置的生成中排除。
要复制的其他文件 | 指定要复制到远程系统的其他文件。 根据需要，可使用类似 fulllocalpath1:=fullremotepath1;fulllocalpath2:=fullremotepath2 的语法以本地到远程的映射对形式提供列表，其中可将本地文件复制到远程系统的指定远程位置。

## <a name="pre-link-event"></a>预链接事件

属性 | 描述
--- | ---
命令行 | 指定让预链接事件工具运行的命令行。
描述 | 指定让预链接事件工具显示的说明。
在生成中使用 | 指定是否将该生成事件从当前配置的生成中排除。
要复制的其他文件 | 指定要复制到远程系统的其他文件。 根据需要，可使用类似 fulllocalpath1:=fullremotepath1;fulllocalpath2:=fullremotepath2 的语法以本地到远程的映射对形式提供列表，其中可将本地文件复制到远程系统的指定远程位置。

## <a name="post-build-event"></a>后期生成事件

属性 | 描述
--- | ---
命令行 | 指定让后期生成事件工具运行的命令行。
描述 | 指定让后期生成事件工具显示的说明。
在生成中使用 | 指定是否将该生成事件从当前配置的生成中排除。
要复制的其他文件 | 指定要复制到远程系统的其他文件。 根据需要，可使用类似 fulllocalpath1:=fullremotepath1;fulllocalpath2:=fullremotepath2 的语法以本地到远程的映射对形式提供列表，其中可将本地文件复制到远程系统的指定远程位置。

## <a name="remote-pre-build-event"></a>远程预先生成事件

属性 | 描述
--- | ---
命令行 | 指定让预生成事件工具在远程系统上运行的命令行。
描述 | 指定让预生成事件工具显示的说明。
在生成中使用 | 指定是否将该生成事件从当前配置的生成中排除。
要复制的其他文件 | 指定要从远程系统复制的其他文件。 根据需要，可使用类似 fullremotepath1:=fulllocalpath1;fullremotepath2:=fulllocalpath2 的语法以远程到本地的映射对形式提供列表，其中可将远程文件复制到本地计算机的指定位置。

## <a name="remote-pre-link-event"></a>远程预链接事件

属性 | 描述
--- | ---
命令行 | 指定让预链接事件工具在远程系统上运行的命令行。
描述 | 指定让预链接事件工具显示的说明。
在生成中使用 | 指定是否将该生成事件从当前配置的生成中排除。
要复制的其他文件 | 指定要从远程系统复制的其他文件。 根据需要，可使用类似 fullremotepath1:=fulllocalpath1;fullremotepath2:=fulllocalpath2 的语法以远程到本地的映射对形式提供列表，其中可将远程文件复制到本地计算机的指定位置。

## <a name="remote-post-build-event"></a>远程后期生成事件

属性 | 描述
--- | ---
命令行 | 指定让后期生成事件工具在远程系统上运行的命令行。
描述 | 指定让后期生成事件工具显示的说明。
在生成中使用 | 指定是否将该生成事件从当前配置的生成中排除。
要复制的其他文件 | 指定要从远程系统复制的其他文件。 根据需要，可使用类似 fullremotepath1:=fulllocalpath1;fullremotepath2:=fulllocalpath2 的语法以远程到本地的映射对形式提供列表，其中可将远程文件复制到本地计算机的指定位置。
