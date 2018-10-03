---
title: 模板策略和属性窗口 |Microsoft Docs
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
- Properties window, template policy
ms.assetid: 1d8019d3-5e57-47ba-b358-526b0796a63b
caps.latest.revision: 16
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 9f8b2085818c539fe0e751a63562496363b43555
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47483324"
---
# <a name="template-policy-and-the-properties-window"></a>模板策略和属性窗口
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

本主题的最新版本，请参阅[模板策略和属性窗口](https://docs.microsoft.com/visualstudio/extensibility/internals/template-policy-and-the-properties-window)。  
  
当一个项目，包含在企业级模板项目时，该企业级模板项目可以强制执行策略。 模板策略将成为一个约束系统，可用于设置属性的默认值、 隐藏属性、 添加属性，依次类推。  
  
 使用模板策略来控制显示的信息中**属性**窗口中是不同于实现<xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing>。 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing> 处理在组件级别的对象属性，而模板策略可用于限制在解决方案或项目级别的对象属性。 换而言之  
  
-   在实现方法<xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing>来确定中显示的内容**属性**为特定对象的窗口  
  
-   使用解决方案和项目级别模板策略来确定中显示的内容**属性**以前指定的对象的窗口  
  
 使用模板策略有选择地限制中的特定属性**属性**中选择窗口中的指定类型的项目项时**解决方案资源管理器**可能非常有益的所有成员开发团队处理项目。 例如，使用模板策略，可以设置所有的连接字符串信息在数据库中您的开发人员，使连接字符串，只读的。 在这种方式，可以提供简单的方法可确保每个开发人员使用正确的路径进行数据访问。  
  
## <a name="see-also"></a>请参阅  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPerPropertyBrowsing>   
 [扩展属性](../../extensibility/internals/extending-properties.md)
