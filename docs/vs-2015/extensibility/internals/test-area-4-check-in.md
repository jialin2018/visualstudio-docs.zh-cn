---
title: 测试区域 4： 签入 |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- source control [Visual Studio SDK], checking items in
- source control plug-ins, checking items in
ms.assetid: d0329fa8-7a8d-4d30-b67b-6f2a97b75a30
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 740ddbfbc24dacaa23200cac1632bf3cf4aef828
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47470271"
---
# <a name="test-area-4-check-in"></a>测试区域 4：签入
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

本主题的最新版本，请参阅[测试区域 4： 签入](https://docs.microsoft.com/visualstudio/extensibility/internals/test-area-4-check-in)。  
  
此源代码管理插件的测试部分覆盖了将已更新的项目发送到的版本存储区通过**签入**命令。  
  
## <a name="command-menu-access"></a>命令菜单访问  
 以下[!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]测试用例中使用集成的开发环境菜单路径。  
  
##### <a name="check-in"></a>登记：  
 **文件**，**源控件**，**签入**。  
  
 **文件**，**签入**。  
  
 快捷菜单中，**签入**。  
  
## <a name="common-expected-behavior"></a>常见的预期的行为  
  
-   项目和文件添加到解决方案或项目源代码管理下的出现在**签入**对话框和**挂起的签入**窗口。  
  
-   在签入后添加的项显示在源代码管理中。  
  
-   后签入中，已更新的项目的正确版本控制的存储中。  
  
## <a name="test-cases"></a>测试用例  
 以下是有关签入测试区域的特定测试用例。  
  
### <a name="case-4a-modified-items"></a>Case 4a： 修改项目  
 描述如何使用操作中检查更新已修改的源控件下的文件。  
  
|操作|测试步骤|若要验证的预期的结果|  
|------------|----------------|--------------------------------|  
|修改已签出的文本文件，请在文件中仅检查 (**签入**对话框)|1.使用文本文件创建一个新的项目。<br />2.将解决方案添加到源代码管理。<br />3.请查看并修改的文本文件。<br />4.签入通过签入对话框中 (**文件**，**源代码管理**，**签入**)。|常见的预期的行为。|  
|修改已签出的文本文件，请在文件中仅检查 (**挂起的签入**窗口)|1.使用文本文件创建一个新的项目。<br />2.将解决方案添加到源代码管理。<br />3.请查看并修改的文本文件。<br />4.通过签入**挂起的签入**窗口。|常见的预期的行为。|  
  
### <a name="case-4b-adding-files"></a>Case 4b： 将文件添加  
 将文件添加到项目或解决方案的项，当项目或解决方案必须也更改。 因此父文件同时签出以及必须签入才能完成添加。  
  
|操作|测试步骤|若要验证的预期的结果|  
|------------|----------------|--------------------------------|  
|将一个文本文件添加并签入所有内容 (**签入**对话框)|1.创建新项目。<br />2.将解决方案添加到源代码管理。<br />3.将文本文件添加到项目。<br />4.如果系统提示您，接受签出的项目。<br />5.选择中的解决方案**解决方案资源管理器**。<br />6.通过签入**签入**对话框。|常见的预期的行为。|  
|将一个文本文件添加并签入所有内容 (**挂起的签入**窗口)|1.创建新项目。<br />2.将解决方案添加到源代码管理。<br />3.将文本文件添加到项目。<br />4.如果系统提示您，接受签出的项目。<br />5.从解决方案签入**挂起的签入**窗口。|常见的预期的行为|  
  
### <a name="case-4c-adding-projects"></a>Case 4c： 添加项目  
 向解决方案添加一个项目，该解决方案还必须将更改。 因此解决方案文件同时签出以及必须签入才能完成添加。  
  
|操作|测试步骤|若要验证的预期的结果|  
|------------|----------------|--------------------------------|  
|将项目添加到源代码管理下的空白解决方案 (**签入**对话框)|1.创建空解决方案。<br />2.将解决方案添加到源代码管理。<br />3.添加新项目。<br />4.如果系统提示您，接受签出的解决方案。<br />5.通过签入**签入**对话框。|常见的预期的行为。|  
|将项目添加到源代码管理下的空白解决方案 (**挂起的签入**窗口)|1.创建空解决方案。<br />2.将解决方案添加到源代码管理。<br />3.添加新项目。<br />4.如果系统提示您，接受签出的解决方案。<br />5.从解决方案签入**挂起的签入**窗口。|常见的预期的行为。|  
  
## <a name="see-also"></a>请参阅  
 [源代码管理插件的测试指南](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)
