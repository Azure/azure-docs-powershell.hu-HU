---
title: Az Azure PowerShell telepítése MSI-vel
description: Az Azure PowerShell telepítése a PowerShellGet nélkül, MSI használatával
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 193e8c5d14f1bf2fe9c84a9da2defac50be97ec7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "91833277"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="7c404-103">Az Azure PowerShell telepítése Windows rendszeren MSI-vel</span><span class="sxs-lookup"><span data-stu-id="7c404-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="7c404-104">Ez a cikk bemutatja, hogyan telepíthető az Azure PowerShell Windows rendszeren egy MSI-telepítő használatával.</span><span class="sxs-lookup"><span data-stu-id="7c404-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="7c404-105">Az MSI-telepítő olyan környezetekhez érhető el, ahol a PowerShell-galériát tűzfal blokkolhatja, vagy ha offline telepítőre van szükség.</span><span class="sxs-lookup"><span data-stu-id="7c404-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="7c404-106">Az Azure PowerShell telepítésének ajánlott módja a PowerShellGet használata.</span><span class="sxs-lookup"><span data-stu-id="7c404-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="7c404-107">Útmutatás az Azure PowerShell PowerShellGet segítségével való telepítéséhez: [Az Azure PowerShell telepítése a PowerShellGet segítségével](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="7c404-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c404-108">Követelmények</span><span class="sxs-lookup"><span data-stu-id="7c404-108">Requirements</span></span>

<span data-ttu-id="7c404-109">A Windows MSI-telepítője csak a PowerShell 5.1-hez telepíti az Azure PowerShellt.</span><span class="sxs-lookup"><span data-stu-id="7c404-109">The MSI installer on Windows is designed to install Azure PowerShell for PowerShell 5.1 only.</span></span> <span data-ttu-id="7c404-110">Nem Windows-platformokon vagy a PowerShell újabb verzióival való telepítéshez a [telepítést a PowerShellGet használatával](install-az-ps.md) végezze el.</span><span class="sxs-lookup"><span data-stu-id="7c404-110">For installation on non-Windows platforms or later versions of PowerShell, [Install with PowerShellGet](install-az-ps.md).</span></span> <span data-ttu-id="7c404-111">A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="7c404-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="7c404-112">Az Azure PowerShell PowerShell 5.1-ben való használatához a következőkre van szükség:</span><span class="sxs-lookup"><span data-stu-id="7c404-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="7c404-113">Frissítsen a [Windows PowerShell 5.1-re](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell), ha szükséges.</span><span class="sxs-lookup"><span data-stu-id="7c404-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="7c404-114">Ha Windows 10 rendszert használ, már telepítve van a PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7c404-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="7c404-115">Telepítse a [.NET-keretrendszer 4.7.2-es vagy újabb verzióját](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="7c404-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="7c404-116">Telepítés vagy frissítés Windows rendszeren az MSI-csomaggal</span><span class="sxs-lookup"><span data-stu-id="7c404-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="7c404-117">Az Azure PowerShell MSI-csomagja a [GitHubon](https://github.com/Azure/azure-powershell/releases) érhető el:</span><span class="sxs-lookup"><span data-stu-id="7c404-117">The MSI package for Azure PowerShell is available from [GitHub](https://github.com/Azure/azure-powershell/releases):</span></span>

1. <span data-ttu-id="7c404-118">Nyissa meg a következőt: https://github.com/Azure/azure-powershell/releases.</span><span class="sxs-lookup"><span data-stu-id="7c404-118">Go to https://github.com/Azure/azure-powershell/releases.</span></span>
2. <span data-ttu-id="7c404-119">Keresse meg az Azure PowerShell legújabb katalógusmodulját (ezek időrendi sorrendben jelennek meg, és általában csak név nélküli kiadásverziók, például „4.7.0”).</span><span class="sxs-lookup"><span data-stu-id="7c404-119">Look for the most recent Gallery Module for Azure PowerShell (these are listed chronologically and are typically just a release version with no name like "4.7.0").</span></span>
3. <span data-ttu-id="7c404-120">Görgessen le a javítási jegyzetek aljára, és kattintson az „Eszközök” melletti nyílra az MSI-beállítások megtekintéséhez.</span><span class="sxs-lookup"><span data-stu-id="7c404-120">Scroll down to the bottom of the patch notes and click on the arrow next to "Assets" to reveal the MSI options.</span></span>
4. <span data-ttu-id="7c404-121">A letöltés indításához kattintson a kívánt Az-Cmdlets MSI-re.</span><span class="sxs-lookup"><span data-stu-id="7c404-121">Click on the Az-Cmdlets MSI of your choice to start the download.</span></span>

<span data-ttu-id="7c404-122">Ha az MSI-vel telepítette az Azure PowerShell korábbi verzióit, a telepítő automatikusan eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="7c404-122">If you have installed earlier versions of Azure PowerShell using the MSI, the installer automatically removes them.</span></span> <span data-ttu-id="7c404-123">Az MSI-csomag a következő helyre telepíti a modulokat: `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="7c404-123">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="7c404-124">Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="7c404-124">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="7c404-125">Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module Az` segítségével.</span><span class="sxs-lookup"><span data-stu-id="7c404-125">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="7c404-126">A modul felépítéséből adódóan ez akár egy percig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="7c404-126">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="7c404-127">Ezt a lépést minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="7c404-127">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="7c404-128">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="7c404-128">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="7c404-129">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="7c404-129">Provide feedback</span></span>

<span data-ttu-id="7c404-130">Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="7c404-130">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="7c404-131">A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="7c404-131">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7c404-132">Következő lépések</span><span class="sxs-lookup"><span data-stu-id="7c404-132">Next Steps</span></span>

<span data-ttu-id="7c404-133">Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.</span><span class="sxs-lookup"><span data-stu-id="7c404-133">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="7c404-134">Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="7c404-134">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>