---
title: 禁用旧代码分析
ms.date: 10/04/2019
description: 了解如何在 Visual Studio 中打开和关闭二进制代码分析。 请参阅如何在托管代码项目中配置此功能。
ms.custom: SEO-VS-2020
ms.topic: how-to
author: mikejo5000
ms.author: mikejo
manager: jmartens
ms.openlocfilehash: c10aa602c2c9af3c51812073d62d5bd9bff06664
ms.sourcegitcommit: ae6d47b09a439cd0e13180f5e89510e3e347fd47
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2021
ms.locfileid: "99860069"
---
# <a name="how-to-enable-and-disable-binary-code-analysis-for-managed-code"></a>如何：启用和禁用托管代码的二进制代码分析

你可以配置旧代码分析 (二进制分析) ，以便在每次生成托管代码项目之后运行。 对于每个生成配置，也可以具有不同的设置，例如 "调试" 和 "发布"。

> [!NOTE]
> 旧版分析不适用于较新的项目类型，如 .NET Core 和 .NET Standard 应用。 这些项目使用 [基于 .NET Compiler Platform 的代码分析器](roslyn-analyzers-overview.md) 来分析活动和生成时的代码。 有关在这些项目中禁用源代码分析的信息，请参阅 [如何禁用源代码分析](disable-code-analysis.md)。

启用或禁用旧代码分析：

1. 在 **解决方案资源管理器** 中，选择并按住 (或右键单击项目) ，然后选择 " **属性**"。

2. 在项目的 "属性" 对话框中，请参阅 " **代码分析** " 选项卡。

3. 在 **配置** 中指定生成类型，并在 **平台** 中指定目标平台。 仅 (Non-.NET Core/.NET Standard 项目。 ) 

::: moniker range="vs-2017"

4. 若要启用或禁用自动代码分析，请选中或清除 " **生成时启用代码分析** " 复选框。

::: moniker-end

::: moniker range=">=vs-2019"

4. 若要启用或禁用自动代码分析，请在 **二进制分析器** 部分中选中或清除 "**生成时运行**" 复选框。

   ![在 Visual Studio 中对生成选项运行二进制代码分析](media/run-on-build-binary-analyzers.png)

::: moniker-end

> [!NOTE]
> 如果在生成时禁用二进制代码分析，则不会影响 [基于 .NET Compiler Platform 的代码分析器](roslyn-analyzers-overview.md)（如果将其安装为 NuGet 包，则该分析器始终在生成时执行）。 有关从这些分析器禁用分析的信息，请参阅 [如何禁用源代码分析](disable-code-analysis.md)。
