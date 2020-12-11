---
title: " (代码分析的文档规则) "
description: 了解代码分析规则文档规则
ms.date: 09/16/2019
ms.topic: reference
f1_keywords:
- vs.codeanalysis.documentationrules
helpviewer_keywords:
- documentation rules
- managed code analysis rules, documentation rules
- warnings, documentation
author: mavasani
ms.author: mavasani
ms.openlocfilehash: 29d1734eec29bd00d456b4b00c48c2e8ef223441
ms.sourcegitcommit: 2e4adc490c1d2a705a0592b295d606b10b9f51f1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2020
ms.locfileid: "96590258"
---
# <a name="documentation-rules"></a><span data-ttu-id="d5d60-103">文档规则</span><span class="sxs-lookup"><span data-stu-id="d5d60-103">Documentation rules</span></span>

<span data-ttu-id="d5d60-104">文档规则支持通过对外部可见 Api 使用正确的 [XML 文档注释](../../../csharp/codedoc.md) 来编写正确的库。</span><span class="sxs-lookup"><span data-stu-id="d5d60-104">Documentation rules support writing well-documented libraries through the correct use of [XML documentation comments](../../../csharp/codedoc.md) for externally visible APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d5d60-105">在本节中</span><span class="sxs-lookup"><span data-stu-id="d5d60-105">In this section</span></span>

| <span data-ttu-id="d5d60-106">规则</span><span class="sxs-lookup"><span data-stu-id="d5d60-106">Rule</span></span> | <span data-ttu-id="d5d60-107">描述</span><span class="sxs-lookup"><span data-stu-id="d5d60-107">Description</span></span> |
| - | - |
| [<span data-ttu-id="d5d60-108">CA1200:不要使用带前缀的 cref 标记</span><span class="sxs-lookup"><span data-stu-id="d5d60-108">CA1200: Avoid using cref tags with a prefix</span></span>](ca1200.md) | <span data-ttu-id="d5d60-109">XML 文档标记中的 [cref](../../../csharp/programming-guide/xmldoc/cref-attribute.md) 特性表示 "代码引用"。</span><span class="sxs-lookup"><span data-stu-id="d5d60-109">The [cref](../../../csharp/programming-guide/xmldoc/cref-attribute.md) attribute in an XML documentation tag means "code reference".</span></span> <span data-ttu-id="d5d60-110">它指定标记的内部文本是一个代码元素，例如类型、方法或属性。</span><span class="sxs-lookup"><span data-stu-id="d5d60-110">It specifies that the inner text of the tag is a code element, such as a type, method, or property.</span></span> <span data-ttu-id="d5d60-111">避免使用 `cref` 带有前缀的标记，因为这会阻止编译器验证引用。</span><span class="sxs-lookup"><span data-stu-id="d5d60-111">Avoid using `cref` tags with prefixes, because it prevents the compiler from verifying references.</span></span> <span data-ttu-id="d5d60-112">它还可防止 Visual Studio 集成开发环境 (IDE) 在重构期间查找和更新这些符号引用。</span><span class="sxs-lookup"><span data-stu-id="d5d60-112">It also prevents the Visual Studio integrated development environment (IDE) from finding and updating these symbol references during refactorings.</span></span> |