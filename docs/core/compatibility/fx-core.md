---
title: 从 .NET Framework 到 .NET Core 的中断性变更
description: 列出了从 .NET Framework 到 .NET Core 的中断性变更。
ms.date: 12/18/2019
ms.openlocfilehash: 6959bffab62cabc524062231db989de45c8c1498
ms.sourcegitcommit: ed3f926b6cdd372037bbcc214dc8f08a70366390
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2020
ms.locfileid: "76116487"
---
# <a name="breaking-changes-for-migration-from-net-framework-to-net-core"></a><span data-ttu-id="8b053-103">从 .NET Framework 迁移到 .NET Core 的中断性变更</span><span class="sxs-lookup"><span data-stu-id="8b053-103">Breaking changes for migration from .NET Framework to .NET Core</span></span>

<span data-ttu-id="8b053-104">若要将应用从 .NET Framework 迁移到 .NET Core，本文中列出的中断性变更可能会影响你。</span><span class="sxs-lookup"><span data-stu-id="8b053-104">If you're migrating an app from .NET Framework to .NET Core, the breaking changes listed in this article may affect you.</span></span> <span data-ttu-id="8b053-105">中断性变更按类别进行分组，并且在这些类别中按引入的 .NET Core 版本进行分组。</span><span class="sxs-lookup"><span data-stu-id="8b053-105">Breaking changes are grouped by category, and within those categories, by the version of .NET Core they were introduced in.</span></span>

> [!NOTE]
> <span data-ttu-id="8b053-106">本文不是 .NET Framework 与 .NET Core 之间的中断性变更的完整列表。</span><span class="sxs-lookup"><span data-stu-id="8b053-106">This article is not a complete list of breaking changes between .NET Framework and .NET Core.</span></span> <span data-ttu-id="8b053-107">在我们发现最重要的中断性变更时，会将其添加到此处。</span><span class="sxs-lookup"><span data-stu-id="8b053-107">The most important breaking changes are added here as we become aware of them.</span></span>

## <a name="corefx"></a><span data-ttu-id="8b053-108">CoreFx</span><span class="sxs-lookup"><span data-stu-id="8b053-108">CoreFx</span></span>

- [<span data-ttu-id="8b053-109">UseShellExecute 默认值更改</span><span class="sxs-lookup"><span data-stu-id="8b053-109">Change in default value of UseShellExecute</span></span>](#change-in-default-value-of-useshellexecute)

### <a name="net-core-21"></a><span data-ttu-id="8b053-110">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="8b053-110">.NET Core 2.1</span></span>

[!INCLUDE[Process.Start changes](~/includes/core-changes/corefx/2.1/process-start-changes.md)]

***

## <a name="windows-forms"></a><span data-ttu-id="8b053-111">Windows 窗体</span><span class="sxs-lookup"><span data-stu-id="8b053-111">Windows Forms</span></span>

<span data-ttu-id="8b053-112">已在 .NET Core 的版本 3.0 中添加 Windows 窗体支持。</span><span class="sxs-lookup"><span data-stu-id="8b053-112">Windows Forms support was added to .NET Core in version 3.0.</span></span> <span data-ttu-id="8b053-113">如果将 Windows 窗体应用从 .NET Framework 迁移到 .NET Core，此处列出的中断性变更可能会影响你的应用。</span><span class="sxs-lookup"><span data-stu-id="8b053-113">If you're migrating a Windows Forms app from .NET Framework to .NET Core, the breaking changes listed here may affect your app.</span></span>

- [<span data-ttu-id="8b053-114">已删除的控件</span><span class="sxs-lookup"><span data-stu-id="8b053-114">Removed controls</span></span>](#removed-controls)
- [<span data-ttu-id="8b053-115">如果显示工具提示，则不引发 CellFormatting 事件</span><span class="sxs-lookup"><span data-stu-id="8b053-115">CellFormatting event not raised if tooltip is shown</span></span>](#cellformatting-event-not-raised-if-tooltip-is-shown)
- [<span data-ttu-id="8b053-116">Control.DefaultFont 已更改为 Segoe UI 9 pt</span><span class="sxs-lookup"><span data-stu-id="8b053-116">Control.DefaultFont changed to Segoe UI 9 pt</span></span>](#default-control-font-changed-to-segoe-ui-9-pt)
- [<span data-ttu-id="8b053-117">FolderBrowserDialog 的现代化</span><span class="sxs-lookup"><span data-stu-id="8b053-117">Modernization of the FolderBrowserDialog</span></span>](#modernization-of-the-folderbrowserdialog)
- [<span data-ttu-id="8b053-118">已从一些 Windows 窗体类型中删除 SerializableAttribute</span><span class="sxs-lookup"><span data-stu-id="8b053-118">SerializableAttribute removed from some Windows Forms types</span></span>](#serializableattribute-removed-from-some-windows-forms-types)
- [<span data-ttu-id="8b053-119">不支持 AllowUpdateChildControlIndexForTabControls 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8b053-119">AllowUpdateChildControlIndexForTabControls compatibility switch not supported</span></span>](#allowupdatechildcontrolindexfortabcontrols-compatibility-switch-not-supported)
- [<span data-ttu-id="8b053-120">不支持 DomainUpDown.UseLegacyScrolling 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8b053-120">DomainUpDown.UseLegacyScrolling compatibility switch not supported</span></span>](#domainupdownuselegacyscrolling-compatibility-switch-not-supported)
- [<span data-ttu-id="8b053-121">不支持 DoNotLoadLatestRichEditControl 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8b053-121">DoNotLoadLatestRichEditControl compatibility switch not supported</span></span>](#donotloadlatestricheditcontrol-compatibility-switch-not-supported)
- [<span data-ttu-id="8b053-122">不支持 DoNotSupportSelectAllShortcutInMultilineTextBox 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8b053-122">DoNotSupportSelectAllShortcutInMultilineTextBox compatibility switch not supported</span></span>](#donotsupportselectallshortcutinmultilinetextbox-compatibility-switch-not-supported)
- [<span data-ttu-id="8b053-123">不支持 DontSupportReentrantFilterMessage 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8b053-123">DontSupportReentrantFilterMessage compatibility switch not supported</span></span>](#dontsupportreentrantfiltermessage-compatibility-switch-not-supported)
- [<span data-ttu-id="8b053-124">不支持 EnableVisualStyleValidation 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8b053-124">EnableVisualStyleValidation compatibility switch not supported</span></span>](#enablevisualstylevalidation-compatibility-switch-not-supported)
- [<span data-ttu-id="8b053-125">不支持 UseLegacyContextMenuStripSourceControlValue 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8b053-125">UseLegacyContextMenuStripSourceControlValue compatibility switch not supported</span></span>](#uselegacycontextmenustripsourcecontrolvalue-compatibility-switch-not-supported)
- [<span data-ttu-id="8b053-126">不支持 UseLegacyImages 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8b053-126">UseLegacyImages compatibility switch not supported</span></span>](#uselegacyimages-compatibility-switch-not-supported)
- [<span data-ttu-id="8b053-127">更改 AccessibleObject.RuntimeIDFirstItem 的访问权限</span><span class="sxs-lookup"><span data-stu-id="8b053-127">Change of access for AccessibleObject.RuntimeIDFirstItem</span></span>](#change-of-access-for-accessibleobjectruntimeidfirstitem)
- [<span data-ttu-id="8b053-128">已 Windows 窗体中删除重复的 API</span><span class="sxs-lookup"><span data-stu-id="8b053-128">Duplicated APIs removed from Windows Forms</span></span>](#duplicated-apis-removed-from-windows-forms)

### <a name="net-core-31"></a><span data-ttu-id="8b053-129">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="8b053-129">.NET Core 3.1</span></span>

[!INCLUDE[Removed controls](~/includes/core-changes/windowsforms/3.1/remove-controls-3.1.md)]

***

[!INCLUDE[CellFormatting event](~/includes/core-changes/windowsforms/3.1/cellformatting-event-not-raised.md)]

***

### <a name="net-core-30"></a><span data-ttu-id="8b053-130">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="8b053-130">.NET Core 3.0</span></span>

[!INCLUDE[Control.DefaultFont changed to Segoe UI 9 pt](~/includes/core-changes/windowsforms/3.0/control-defaultfont-changed.md)]

***

[!INCLUDE[Modernization of the FolderBrowserDialog](~/includes/core-changes/windowsforms/3.0/modernized-folderbrowserdialog.md)]

***

[!INCLUDE[SerializableAttribute removed from some Windows Forms types](~/includes/core-changes/windowsforms/3.0/remove-serializationattribute.md)]

***

[!INCLUDE[AllowUpdateChildControlIndexForTabControls compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-allowupdatechildcontrolindexfortabcontrols.md)]

***

[!INCLUDE[DomainUpDown.UseLegacyScrolling compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-uselegacyscrolling.md)]

***

[!INCLUDE[DoNotLoadLatestRichEditControl compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-donotloadlatestricheditcontrol.md)]

***

[!INCLUDE[DoNotSupportSelectAllShortcutInMultilineTextBox compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-donotsupportselectallshortcutinmultilinetextbox.md)]

***

[!INCLUDE[DontSupportReentrantFilterMessage compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-dontsupportreentrantfiltermessage.md)]

***

[!INCLUDE[EnableVisualStyleValidation compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-enablevisualstylevalidation.md)]

***

[!INCLUDE[UseLegacyContextMenuStripSourceControlValue compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-uselegacycontextmenustripsourcecontrolvalue.md)]

***

[!INCLUDE[UseLegacyImages compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-uselegacyimages.md)]

***

[!INCLUDE[Change of access for AccessibleObject.RuntimeIDFirstItem](~/includes/core-changes/windowsforms/3.0/changed-access-for-runtimeidfirstitem.md)]

***

[!INCLUDE[Duplicated APIs removed from Windows Forms](~/includes/core-changes/windowsforms/3.0/remove-duplicated-apis.md)]

***

## <a name="see-also"></a><span data-ttu-id="8b053-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="8b053-131">See also</span></span>

- [<span data-ttu-id="8b053-132">始终在 .NET Core 上引发异常的 API</span><span class="sxs-lookup"><span data-stu-id="8b053-132">APIs that always throw exceptions on .NET Core</span></span>](unsupported-apis.md)
- [<span data-ttu-id="8b053-133">.NET Framework 技术在 .NET Core 上不可用</span><span class="sxs-lookup"><span data-stu-id="8b053-133">.NET Framework technologies unavailable on .NET Core</span></span>](../porting/net-framework-tech-unavailable.md)