---
title: 输出参数
ms.date: 10/24/2018
helpviewer_keywords:
- OLE DB, stored procedures
- stored procedures, calling
- stored procedures, parameters
- procedure calls
- procedure calls, stored procedures
ms.assetid: 4f7c2700-1c2d-42f3-8c9f-7e83962b2442
ms.openlocfilehash: 575bc2c347275bfb96f64e60f35379629b4eac18
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2018
ms.locfileid: "50614534"
---
# <a name="output-parameters"></a>输出参数

调用存储的过程是类似于运行 SQL 命令。 主要区别是存储的过程使用输出参数 （或"输出"） 和返回值。

在以下存储过程中，第一个？ 是返回值 （电话），第二个？ 是输入的参数 （名称）：

```cpp
DEFINE_COMMAND_EX(CMySProcAccessor, _T("{ ? = SELECT phone FROM shippers WHERE name = ? }"))
```

参数映射中指定 in 和 out 参数：

```cpp
BEGIN_PARAM_MAP(CMySProcAccessor)
   SET_PARAM_TYPE(DBPARAMIO_OUTPUT)
   COLUMN_ENTRY(1, m_Phone)   // Phone is the return value
   SET_PARAM_TYPE(DBPARAMIO_INPUT)
   COLUMN_ENTRY(2, m_Name)   // Name is the input parameter
END_PARAM_MAP()
```

应用程序必须处理从存储过程返回的输出。 不同的 OLE DB 访问接口返回输出参数和返回结果处理期间的不同时间的值。 例如，Microsoft OLE DB 访问接口的 SQL Server (SQLOLEDB) 不提供输出参数和返回之前的代码后使用者检索或取消存储过程返回的结果集。 从服务器中的最后一个的 TDS 数据包返回输出。

## <a name="row-count"></a>行计数

如果使用 OLE DB 使用者模板来执行具有输出的存储的过程，直到关闭的行集不是设置行计数。

例如，请考虑使用带有行集和输出参数为存储的过程：

```sql
create procedure sp_test
   @_rowcount integer output
as
   select top 50 * from test
   @_rowcount = @@rowcount
return 0
```

`@_rowcount`带有报告从测试表返回行数。 但是，此存储的过程限制为 50 的行数。 例如，如果在测试中有 100 行，行计数将是 50 （因为此代码检索只显示前 50 行）。 如果表中仅 30 行，行计数将为 30。 请务必调用`Close`或`CloseAll`来填充带有之前提取其值。

## <a name="see-also"></a>请参阅

[使用存储过程](../../data/oledb/using-stored-procedures.md)