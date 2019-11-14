---
title: Az Azure PowerShell telepítése MSI-vel
description: Az Azure PowerShell telepítése a PowerShellGet nélkül, MSI használatával
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 566ea4b9ac9398b063cc3567c482a67834de36f5
ms.sourcegitcommit: ad7677d703a8512d371d3123dc7e541156b95cb8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/23/2019
ms.locfileid: "72821503"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="c3ecf-103">Az Azure PowerShell telepítése Windows rendszeren MSI-vel</span><span class="sxs-lookup"><span data-stu-id="c3ecf-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="c3ecf-104">Ez a cikk bemutatja, hogyan telepíthető az Azure PowerShell Windows rendszeren egy MSI-telepítő használatával.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="c3ecf-105">Az MSI-telepítő olyan környezetekhez érhető el, ahol a PowerShell-galériát tűzfal blokkolhatja, vagy ha offline telepítőre van szükség.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="c3ecf-106">Az Azure PowerShell telepítésének ajánlott módja a PowerShellGet használata.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="c3ecf-107">Útmutatás az Azure PowerShell PowerShellGet segítségével való telepítéséhez: [Az Azure PowerShell telepítése a PowerShellGet segítségével](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="c3ecf-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ecf-108">Követelmények</span><span class="sxs-lookup"><span data-stu-id="c3ecf-108">Requirements</span></span>

<span data-ttu-id="c3ecf-109">Az Azure PowerShell MSI-telepítője __csak__ a PowerShell 5.1-hez, Windows rendszeren használható.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-109">The MSI installer for Azure PowerShell works __only__ for PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="c3ecf-110">Nem Windows-platformokon vagy a PowerShell újabb verzióival való telepítéshez [telepítsen a PowerShellGet használatával](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="c3ecf-110">For installation on non-Windows platforms or later versions of powershell, [Install with PowerShellGet](install-az-ps.md).</span></span>
<span data-ttu-id="c3ecf-111">A PowerShell verziójának megtekintéséhez futtassa az alábbi parancsot:</span><span class="sxs-lookup"><span data-stu-id="c3ecf-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="c3ecf-112">Az Azure PowerShell PowerShell 5.1-ben való használatához a következőkre van szükség:</span><span class="sxs-lookup"><span data-stu-id="c3ecf-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="c3ecf-113">Frissítsen a [Windows PowerShell 5.1-re](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell), ha szükséges.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-113">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="c3ecf-114">Ha Windows 10 rendszert használ, már telepítve van a PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="c3ecf-115">Telepítse a [.NET-keretrendszer 4.7.2-es vagy újabb verzióját](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="c3ecf-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="c3ecf-116">Telepítés vagy frissítés Windows rendszeren az MSI-csomaggal</span><span class="sxs-lookup"><span data-stu-id="c3ecf-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="c3ecf-117">A Windowshoz készült Azure PowerShell telepíthető a [GitHubról](https://github.com/Azure/azure-powershell/releases/tag/v1.8.0-April2019) elérhető MSI-fájllal is.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-117">Azure PowerShell for Windows is installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v1.8.0-April2019).</span></span> <span data-ttu-id="c3ecf-118">Ha az Azure-modulok korábbi verziói már telepítve vannak MSI-ként, a telepítő automatikusan eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-118">If you have installed earlier versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="c3ecf-119">Az MSI-csomag a következő helyre telepíti a modulokat: `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-119">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="c3ecf-120">Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-120">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="c3ecf-121">Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module Az` segítségével.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-121">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="c3ecf-122">A modul felépítéséből adódóan ez akár egy percig is eltarthat.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-122">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="c3ecf-123">Ezt a lépést minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-123">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="c3ecf-124">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-124">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="c3ecf-125">Visszajelzés küldése</span><span class="sxs-lookup"><span data-stu-id="c3ecf-125">Provide feedback</span></span>

<span data-ttu-id="c3ecf-126">Ha hibát észlel az Azure PowerShellben, [jelentse be a problémát a GitHubon](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="c3ecf-126">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="c3ecf-127">A parancssorból a [Send-Feedback](/powershell/module/az.accounts/send-feedback) parancsmaggal küldhet visszajelzést.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-127">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c3ecf-128">További lépések</span><span class="sxs-lookup"><span data-stu-id="c3ecf-128">Next Steps</span></span>

<span data-ttu-id="c3ecf-129">Az Azure PowerShell-modulokról és azok funkcióiról az [Azure PowerShell használatának első lépéseit](get-started-azureps.md) ismertető szakaszban talál további információt.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="c3ecf-130">Ha ismeri az Azure PowerShellt, és az AzureRM-ből végez migrálást, tekintse meg [az AzureRM modulból az Az modulba való áttelepítést](migrate-from-azurerm-to-az.md) ismertető szakaszt.</span><span class="sxs-lookup"><span data-stu-id="c3ecf-130">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>