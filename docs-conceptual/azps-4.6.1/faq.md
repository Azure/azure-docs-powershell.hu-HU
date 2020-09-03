---
title: Gyakori kérdések (GYIK)
description: Gyakori kérdések az Azure PowerShell-lel kapcsolatban.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239383"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="ddd51-103">Gyakori kérdések az Azure PowerShell-lel kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="ddd51-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="ddd51-104">Mi az az Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="ddd51-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="ddd51-105">Az Azure PowerShell olyan parancsmagok készletét kínálja, amelyekkel az Azure-erőforrások közvetlenül a PowerShell-lel kezelhetők.</span><span class="sxs-lookup"><span data-stu-id="ddd51-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="ddd51-106">2018 decemberében az Az PowerShell-modul általánosan elérhetővé vált.</span><span class="sxs-lookup"><span data-stu-id="ddd51-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="ddd51-107">Ma már ez az Azure használatához ajánlott PowerShell-modul.</span><span class="sxs-lookup"><span data-stu-id="ddd51-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="ddd51-108">Ha többet is meg szeretne tudni az Az PowerShell-modulról, olvassa el [az Azure PowerShell új Az moduljának ismertetését](/powershell/azure/new-azureps-module-az).</span><span class="sxs-lookup"><span data-stu-id="ddd51-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="ddd51-109">Hogyan tilthatom le a kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzeneteket az Azure PowerShellben?</span><span class="sxs-lookup"><span data-stu-id="ddd51-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="ddd51-110">Az Azure PowerShell kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzeneteinek letiltásához állítsa a `SuppressAzurePowerShellBreakingChangeWarnings` környezeti változót `true` értékre.</span><span class="sxs-lookup"><span data-stu-id="ddd51-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
