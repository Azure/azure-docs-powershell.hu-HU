---
title: Az Azure PowerShell telepítésének egyéb módjai
description: Az Azure PowerShell telepítése a PowerShellGet nélkül
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 55a89861c3bcca41b940d34d945cd43690331f3e
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83385762"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="bc889-103">Az Azure PowerShell telepítése Windows rendszeren MSI-vel vagy a Webplatform-telepítővel</span><span class="sxs-lookup"><span data-stu-id="bc889-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="bc889-104">Ez a cikk bemutatja, hogyan telepíthető az Azure PowerShell Windows rendszeren egy MSI-telepítő vagy Webplatform-telepítő (WebPI) használatával.</span><span class="sxs-lookup"><span data-stu-id="bc889-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="bc889-105">Csak akkor alkalmazza ezeket a telepítési módszereket, ha a rendszer számára szükséges.</span><span class="sxs-lookup"><span data-stu-id="bc889-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="bc889-106">Az Azure PowerShell Windows rendszeren való telepítésének ajánlott módja a PowerShellGet használata.</span><span class="sxs-lookup"><span data-stu-id="bc889-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="bc889-107">Útmutatás az Azure PowerShell PowerShellGet segítségével való telepítéséhez: [Az Azure PowerShell telepítése a PowerShellGet segítségével](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="bc889-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="bc889-108">Telepítés vagy frissítés Windows rendszeren az MSI-csomaggal</span><span class="sxs-lookup"><span data-stu-id="bc889-108">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="bc889-109">Az Azure PowerShell telepíthető a [GitHubról](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018) elérhető MSI-fájllal is.</span><span class="sxs-lookup"><span data-stu-id="bc889-109">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="bc889-110">Ha az Azure-modulok korábbi verziói már telepítve vannak MSI-ként, a telepítő automatikusan eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="bc889-110">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="bc889-111">Az MSI-csomag a következő helyre telepíti a modulokat: `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="bc889-111">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="bc889-112">Az `AzureRM` és az `Azure` modul is telepítve lesz.</span><span class="sxs-lookup"><span data-stu-id="bc889-112">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="bc889-113">Ha a klasszikus Azure üzemi modellt használja, csak az `Azure` modult használja.</span><span class="sxs-lookup"><span data-stu-id="bc889-113">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="bc889-114">Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `AzureRM` modult az aktuális PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="bc889-114">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="bc889-115">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="bc889-115">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="bc889-116">Az `AzureRM` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.</span><span class="sxs-lookup"><span data-stu-id="bc889-116">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="bc889-117">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [felhasználói hitelesítő adatok a PowerShell-munkamenetek között történő megőrzését](context-persistence.md) ismertető részt.</span><span class="sxs-lookup"><span data-stu-id="bc889-117">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="bc889-118">Telepítés vagy frissítés Windows rendszeren a Webplatform-telepítővel</span><span class="sxs-lookup"><span data-stu-id="bc889-118">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="bc889-119">Töltse le az [Azure PowerShell WebPI csomagot](https://aka.ms/webpi-azps), és indítsa el a telepítést.</span><span class="sxs-lookup"><span data-stu-id="bc889-119">Download the [Azure PowerShell WebPI package](https://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="bc889-120">Ha az Azure-modulok korábbi verziói már telepítve vannak MSI-ből vagy WebPI-vel, a telepítő automatikusan eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="bc889-120">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="bc889-121">A modulok az `${env:ProgramFiles}\WindowsPowerShell\Modules` helyre lesznek telepítve.</span><span class="sxs-lookup"><span data-stu-id="bc889-121">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="bc889-122">Az `AzureRM` és az `Azure` modul is telepítve lesz.</span><span class="sxs-lookup"><span data-stu-id="bc889-122">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="bc889-123">Ha a klasszikus Azure üzemi modellt használja, csak az `Azure` modult használja.</span><span class="sxs-lookup"><span data-stu-id="bc889-123">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="bc889-124">Az Azure PowerShell használatának megkezdéséhez be kell tölteni az `AzureRM` modult az aktuális PowerShell-munkamenetbe az [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) parancsmaggal, majd be kell jelentkezni az Azure-beli hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="bc889-124">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="bc889-125">Ezeket a lépéseket minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="bc889-125">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="bc889-126">Az `AzureRM` modul automatikus importálásához be kell állítani egy PowerShell-profilt, amelyről a [profilokat ismertető](/powershell/module/microsoft.powershell.core/about/about_profiles) részben tudhat meg többet.</span><span class="sxs-lookup"><span data-stu-id="bc889-126">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="bc889-127">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a munkamenetek között, tekintse meg a [felhasználói hitelesítő adatok a PowerShell-munkamenetek között történő megőrzését](context-persistence.md) ismertető részt.</span><span class="sxs-lookup"><span data-stu-id="bc889-127">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
