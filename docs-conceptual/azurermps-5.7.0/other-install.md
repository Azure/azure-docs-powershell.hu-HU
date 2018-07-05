---
title: Az Azure PowerShell telepítésének egyéb módjai
description: Az Azure PowerShell telepítése a PowerShellGet nélkül
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: f6c52b413aa2981dc24c7e60fe832e37dcbc8baa
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091452"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="19a8e-103">Az Azure PowerShell telepítése Windows rendszeren MSI-vel vagy a Webplatform-telepítővel</span><span class="sxs-lookup"><span data-stu-id="19a8e-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

<span data-ttu-id="19a8e-104">Ez a cikk bemutatja, hogyan telepíthető az Azure PowerShell Windows rendszeren egy MSI-telepítő vagy Webplatform-telepítő (WebPI) használatával.</span><span class="sxs-lookup"><span data-stu-id="19a8e-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="19a8e-105">Csak akkor alkalmazza ezeket a telepítési módszereket, ha a rendszer számára szükséges.</span><span class="sxs-lookup"><span data-stu-id="19a8e-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="19a8e-106">Az Azure PowerShell Windows rendszeren való telepítésének ajánlott módja a PowerShellGet használata.</span><span class="sxs-lookup"><span data-stu-id="19a8e-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="19a8e-107">Útmutatás az Azure PowerShell PowerShellGet segítségével való telepítéséhez: [Az Azure PowerShell telepítése a PowerShellGet segítségével](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="19a8e-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="19a8e-108">Az Azure PowerShell Docker-tárolóban történő futtatásához lásd: [Az Azure PowerShell futtatása Docker-tárolóban](azurerm-ps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="19a8e-108">To run Azure PowerShell in a Docker container, see [Run Azure PowerShell in Docker](azurerm-ps-in-docker.md).</span></span>

<span data-ttu-id="19a8e-109">Ha Linux- vagy macOS-környezetben végzi a telepítést, tekintse meg [Az Azure PowerShell telepítése macOS vagy Linux rendszeren](install-azurermps-maclinux.md) szakaszt.</span><span class="sxs-lookup"><span data-stu-id="19a8e-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="19a8e-110">Telepítés vagy frissítés Windows rendszeren az MSI-csomaggal</span><span class="sxs-lookup"><span data-stu-id="19a8e-110">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="19a8e-111">Az Azure PowerShell telepíthető a [GitHubról](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018) elérhető MSI-fájllal is.</span><span class="sxs-lookup"><span data-stu-id="19a8e-111">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="19a8e-112">Ha az Azure-modulok korábbi verziói már telepítve vannak MSI-ként, a telepítő automatikusan eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="19a8e-112">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="19a8e-113">Az MSI-csomag az `${env:ProgramFiles}\WindowsPowerShell\Modules` helyre telepíti a modulokat.</span><span class="sxs-lookup"><span data-stu-id="19a8e-113">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="19a8e-114">Az `AzureRM` és az `Azure` modul is telepítve lesz.</span><span class="sxs-lookup"><span data-stu-id="19a8e-114">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="19a8e-115">Ha a klasszikus Azure üzemi modellt használja, csak az `Azure` modult használja.</span><span class="sxs-lookup"><span data-stu-id="19a8e-115">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="19a8e-116">Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `AzureRM` modult az aktuális PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="19a8e-116">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="19a8e-117">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="19a8e-117">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="19a8e-118">Az `AzureRM` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.</span><span class="sxs-lookup"><span data-stu-id="19a8e-118">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="19a8e-119">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című részt.</span><span class="sxs-lookup"><span data-stu-id="19a8e-119">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="19a8e-120">Telepítés vagy frissítés Windows rendszeren a Webplatform-telepítővel</span><span class="sxs-lookup"><span data-stu-id="19a8e-120">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="19a8e-121">Töltse le az [Azure PowerShell WebPI csomagot](http://aka.ms/webpi-azps), és indítsa el a telepítést.</span><span class="sxs-lookup"><span data-stu-id="19a8e-121">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="19a8e-122">Ha az Azure-modulok korábbi verziói már telepítve vannak MSI-ből vagy WebPI-vel, a telepítő automatikusan eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="19a8e-122">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="19a8e-123">A modulok az `${env:ProgramFiles}\WindowsPowerShell\Modules` helyre lesznek telepítve.</span><span class="sxs-lookup"><span data-stu-id="19a8e-123">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="19a8e-124">Az `AzureRM` és az `Azure` modul is telepítve lesz.</span><span class="sxs-lookup"><span data-stu-id="19a8e-124">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="19a8e-125">Ha a klasszikus Azure üzemi modellt használja, csak az `Azure` modult használja.</span><span class="sxs-lookup"><span data-stu-id="19a8e-125">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="19a8e-126">Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `AzureRM` modult az aktuális PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="19a8e-126">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="19a8e-127">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="19a8e-127">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="19a8e-128">Az `AzureRM` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.</span><span class="sxs-lookup"><span data-stu-id="19a8e-128">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="19a8e-129">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című részt.</span><span class="sxs-lookup"><span data-stu-id="19a8e-129">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>