---
title: Az Azure PowerShell telepítésének egyéb módjai
description: Az Azure PowerShell telepítése a PowerShellGet nélkül, MSI használatával
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 0976fd51b26010702d200cee445d93269405416c
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153841"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="24b09-103">Az Azure PowerShell telepítése Windows rendszeren MSI-vel</span><span class="sxs-lookup"><span data-stu-id="24b09-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="24b09-104">Ez a cikk bemutatja, hogyan telepíthető az Azure PowerShell Windows rendszeren egy MSI-telepítő használatával.</span><span class="sxs-lookup"><span data-stu-id="24b09-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="24b09-105">Csak akkor alkalmazza ezeket a telepítési módszereket, ha a rendszer számára szükséges.</span><span class="sxs-lookup"><span data-stu-id="24b09-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="24b09-106">Az Azure PowerShell Windows rendszeren való telepítésének ajánlott módja a PowerShellGet használata.</span><span class="sxs-lookup"><span data-stu-id="24b09-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="24b09-107">Útmutatás az Azure PowerShell PowerShellGet segítségével való telepítéséhez: [Az Azure PowerShell telepítése a PowerShellGet segítségével](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="24b09-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="24b09-108">A Webplatform-telepítőt használó telepítési módszer már nem érhető el az Azure PowerShell 6.x-es vagy újabb verzióihoz.</span><span class="sxs-lookup"><span data-stu-id="24b09-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="24b09-109">Ha a Webplatform-telepítőt kell használnia, fontolja meg helyette az MSI használatát, vagy telepítheti az Azure PowerShell egy korábbi verzióját.</span><span class="sxs-lookup"><span data-stu-id="24b09-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="24b09-110">Ha Linux- vagy macOS-környezetben végzi a telepítést, tekintse meg [Az Azure PowerShell telepítése macOS vagy Linux rendszeren](install-azurermps-maclinux.md) szakaszt.</span><span class="sxs-lookup"><span data-stu-id="24b09-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="24b09-111">Telepítés vagy frissítés Windows rendszeren az MSI-csomaggal</span><span class="sxs-lookup"><span data-stu-id="24b09-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="24b09-112">A Windows PowerShell 5.x verziójához készült Azure PowerShell telepíthető a [GitHubról](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018) elérhető MSI-fájllal is.</span><span class="sxs-lookup"><span data-stu-id="24b09-112">Azure PowerShell for Windows PowerShell 5.x can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span> <span data-ttu-id="24b09-113">Ha az Azure-modulok korábbi verziói már telepítve vannak MSI-ként, a telepítő automatikusan eltávolítja őket.</span><span class="sxs-lookup"><span data-stu-id="24b09-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="24b09-114">Az MSI-csomag a következő helyre telepíti a modulokat: `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="24b09-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="24b09-115">Az `AzureRM` és az `Azure` modul is telepítve lesz.</span><span class="sxs-lookup"><span data-stu-id="24b09-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="24b09-116">Ha a klasszikus Azure üzemi modellt használja, csak az `Azure` modult használja.</span><span class="sxs-lookup"><span data-stu-id="24b09-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="24b09-117">Az Azure PowerShell használatának megkezdéséhez jelentkezzen be Azure-beli hitelesítő adataival.</span><span class="sxs-lookup"><span data-stu-id="24b09-117">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="24b09-118">Ha letiltotta az automatikus modulbetöltést, manuálisan kell importálnia a modult a(z) `Import-Module AzureRM` segítségével.</span><span class="sxs-lookup"><span data-stu-id="24b09-118">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="24b09-119">A modul felépítéséből adódóan ez eltarthat néhány másodpercig.</span><span class="sxs-lookup"><span data-stu-id="24b09-119">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="24b09-120">Ezt a lépést minden új PowerShell-munkamenet esetében meg kell ismételni.</span><span class="sxs-lookup"><span data-stu-id="24b09-120">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="24b09-121">Ha szeretné megtudni, hogyan őrizheti meg az Azure-bejelentkezést a PowerShell-munkamenetek között, tekintse meg a [Felhasználói hitelesítő adatok megőrzése a PowerShell-munkamenetek között](context-persistence.md) című cikket.</span><span class="sxs-lookup"><span data-stu-id="24b09-121">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
