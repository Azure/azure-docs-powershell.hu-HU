---
title: Azure PowerShell-szkriptek áttelepítése az AzureRM modulból az Az modulba
description: Ismerje meg a szkriptek az AzureRM modulból az új Az modulba való áttelepítésére szolgáló lépéseket és eszközöket.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753615"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a><span data-ttu-id="784a0-103">Az Azure PowerShell migrálása az AzureRM modulból az Az modulba</span><span class="sxs-lookup"><span data-stu-id="784a0-103">Migrate Azure PowerShell from AzureRM to Az</span></span>

<span data-ttu-id="784a0-104">Az AzureRM PowerShell-modul minden verziója elavult, de a támogatásuk még nem szűnt meg.</span><span class="sxs-lookup"><span data-stu-id="784a0-104">All versions of the AzureRM PowerShell module are outdated, but not out of support.</span></span> <span data-ttu-id="784a0-105">Mostantól az [Az PowerShell-modul](install-az-ps.md) használatát javasoljuk az Azure-ral folytatott interakciókhoz.</span><span class="sxs-lookup"><span data-stu-id="784a0-105">The [Az PowerShell module](install-az-ps.md) is now the recommended PowerShell module for interacting with Azure.</span></span>

<span data-ttu-id="784a0-106">Az AzureRM-parancsmagokhoz írt szkriptek nem működnek automatikusan az új modullal.</span><span class="sxs-lookup"><span data-stu-id="784a0-106">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="784a0-107">A váltás megkönnyítése érdekében lett kifejlesztve az [AzureRM és Az közötti migrálási eszközkészlet](https://github.com/Azure/azure-powershell-migration).</span><span class="sxs-lookup"><span data-stu-id="784a0-107">To make the transition easier, the [AzureRM to Az migration toolkit](https://github.com/Azure/azure-powershell-migration) was developed.</span></span> <span data-ttu-id="784a0-108">Az új parancskészletekre való áttérés soha nem egyszerű, ebben a cikkben azonban segítünk megismerkedni az Az PowerShell-modulra való átállás alapjaival.</span><span class="sxs-lookup"><span data-stu-id="784a0-108">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the Az PowerShell module.</span></span> <span data-ttu-id="784a0-109">Ha érdekli, miért jött létre az Az PowerShell-modul, olvassa el [az Azure PowerShell új Az moduljának ismertetését](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="784a0-109">To learn more about why the Az PowerShell module was created, see [Introducing the new Azure PowerShell Az module](new-azureps-module-az.md).</span></span>

<span data-ttu-id="784a0-110">Az AzureRM és az Az közötti kompatibilitástörő változások teljes listáját [az AzureRM és az Az közötti változások teljes listájában](migrate-az-1.0.0.md) találja.</span><span class="sxs-lookup"><span data-stu-id="784a0-110">To see the full list of breaking changes between AzureRM and Az, see the [full changes from AzureRM to Az](migrate-az-1.0.0.md).</span></span>

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="784a0-111">Annak ellenőrzése, hogy a meglévő szkriptek működnek-e az AzureRM legújabb kiadásával</span><span class="sxs-lookup"><span data-stu-id="784a0-111">Ensure existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="784a0-112">A migrálási lépések előtt ellenőrizze, hogy az AzureRM mely verziói vannak telepítve a rendszeren.</span><span class="sxs-lookup"><span data-stu-id="784a0-112">Before taking any migration steps, check which versions of AzureRM are installed on your system.</span></span>
<span data-ttu-id="784a0-113">Ezzel biztosíthatja, hogy a szkriptek már a legújabb kiadáson fussanak, és megtudhatja, hogy az AzureRM mely verzióit kell eltávolítania.</span><span class="sxs-lookup"><span data-stu-id="784a0-113">Doing so allows you to make sure scripts are already running on the latest release, and let you know which versions of AzureRM must be uninstalled.</span></span>

<span data-ttu-id="784a0-114">Az AzureRM telepített verziója/verziói megtekintéséhez futtassa a következő példaparancsot:</span><span class="sxs-lookup"><span data-stu-id="784a0-114">To check which version(s) of AzureRM you have installed, run the following example:</span></span>

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

<span data-ttu-id="784a0-115">Az AzureRM **legújabb** elérhető kiadása a **6.13.1-es** .</span><span class="sxs-lookup"><span data-stu-id="784a0-115">The **latest** available release of AzureRM is **6.13.1** .</span></span> <span data-ttu-id="784a0-116">Ha nincs telepítve ez a verzió, a meglévő szkriptek további módosítást is igényelhetnek az ebben a cikkben és a [kompatibilitástörő változások listájában](migrate-az-1.0.0.md) leírtakon túlmenően, hogy használni lehessen őket az Az modullal.</span><span class="sxs-lookup"><span data-stu-id="784a0-116">If you don't have this version installed, your existing scripts may need additional modifications to work with the Az module beyond what's described in this article and in the [breaking changes list](migrate-az-1.0.0.md).</span></span>

<span data-ttu-id="784a0-117">Ha a szkriptek nem működnek az AzureRM 6.13.1-es verziójával, frissítse őket az [AzureRM 5.x és 6.x migrálási útmutatója](/powershell/azure/azurerm/migration-guide.6.0.0) szerint.</span><span class="sxs-lookup"><span data-stu-id="784a0-117">If your scripts don't work with AzureRM 6.13.1, update them according to the [AzureRM 5.x to 6.x migration guide](/powershell/azure/azurerm/migration-guide.6.0.0).</span></span> <span data-ttu-id="784a0-118">Ha az AzureRM modul korábbi verzióját használja, mindegyik fő verzióhoz elérhető migrálási útmutató.</span><span class="sxs-lookup"><span data-stu-id="784a0-118">If you use an earlier version of the AzureRM module, there are migration guides available for each major version.</span></span>

## <a name="install-the-azurerm-to-az-migration-toolkit"></a><span data-ttu-id="784a0-119">Az AzureRM és Az közötti migrálási eszközkészlet telepítése</span><span class="sxs-lookup"><span data-stu-id="784a0-119">Install the AzureRM to Az migration toolkit</span></span>

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a><span data-ttu-id="784a0-120">PowerShell-szkriptek automatikus migrálása</span><span class="sxs-lookup"><span data-stu-id="784a0-120">Automatically migrate your PowerShell scripts</span></span>

<span data-ttu-id="784a0-121">Az AzureRM és Az közötti migrálási eszközkészlettel létrehozhat egy tervet, amely megállapítja, milyen módosításokat kell végrehajtani a szkripteken, mielőtt valóban módosítaná azokat és telepítené az Az PowerShell-modult.</span><span class="sxs-lookup"><span data-stu-id="784a0-121">With the AzureRM to Az migration toolkit, you can generate a plan to determine what changes will be performed on your scripts before making any modifications to them and before installing the Az PowerShell module.</span></span>

<span data-ttu-id="784a0-122">A [PowerShell-szkriptek az AzureRM modulból az Az PowerShell-modulba történő automatikus migrálásának](quickstart-migrate-azurerm-to-az-automatically.md) gyorsútmutatója végigvezet a PowerShell-szkriptek AzureRM-ből az Az PowerShell-modulba való automatikus frissítésének teljes folyamatán.</span><span class="sxs-lookup"><span data-stu-id="784a0-122">The [Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module](quickstart-migrate-azurerm-to-az-automatically.md) quickstart walks you through the entire process of automatically updating your PowerShell scripts from AzureRM to the Az PowerShell module.</span></span>

## <a name="next-steps"></a><span data-ttu-id="784a0-123">Következő lépések</span><span class="sxs-lookup"><span data-stu-id="784a0-123">Next steps</span></span>

<span data-ttu-id="784a0-124">[Az Azure PowerShell telepítése](install-az-ps.md)
[Az AzureRM eltávolítása](uninstall-az-ps.md#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="784a0-124">[Install Azure PowerShell](install-az-ps.md)
[Uninstall AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)</span></span>
