---
title: Az Azure PowerShell Az modul bemutatása
description: Bemutatkozik az új Azure PowerShell-modul, az Az, amely az AzureRM modult váltja le.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882292"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="a32f8-103">Az új Azure PowerShell Az modul bemutatása</span><span class="sxs-lookup"><span data-stu-id="a32f8-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="a32f8-104">2018 decemberétől az Azure PowerShell Az modul általánosan elérhetővé vált, és mostantól az Azure-ral való kommunikációhoz használható PowerShell modul is elérhető.</span><span class="sxs-lookup"><span data-stu-id="a32f8-104">Starting in December 2018, the Azure PowerShell Az module is in general release and now the intended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="a32f8-105">Az Az rövidebb parancsokat és nagyobb stabilitást kínál, valamint több platformot is támogat.</span><span class="sxs-lookup"><span data-stu-id="a32f8-105">Az offers shorter commands, improved stability, and cross-platform support.</span></span> <span data-ttu-id="a32f8-106">Emellett funkcióparitást és egyszerű áttelepítési útvonalat biztosít az AzureRM-ről.</span><span class="sxs-lookup"><span data-stu-id="a32f8-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="a32f8-107">Az Az a .NET Standard-kódtárat használja, ami azt jelenti, hogy fut a PowerShell 5-ös és PowerShell 6-os verziókon is.</span><span class="sxs-lookup"><span data-stu-id="a32f8-107">Az uses the .NET Standard library, which means it runs on PowerShell 5 and PowerShell 6.</span></span>
<span data-ttu-id="a32f8-108">Mivel a PowerShell 6 Linux, macOS és Windows rendszeren is fut, az Azure PowerShell mostantól minden platformon elérhető.</span><span class="sxs-lookup"><span data-stu-id="a32f8-108">Since PowerShell 6 can run on Linux, macOS, and Windows, Azure PowerShell is now available for all platforms.</span></span>
<span data-ttu-id="a32f8-109">A .NET Standard használatával az Azure PowerShell kódbázisa egységesíthető, és mindez csak minimális hatással van a felhasználókra.</span><span class="sxs-lookup"><span data-stu-id="a32f8-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="a32f8-110">Az Az egy új modul, ezért a verziószámozás vissza lett állítva 1.0.0-ra.</span><span class="sxs-lookup"><span data-stu-id="a32f8-110">Az is a new module, so the version has been reset to 1.0.0.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="a32f8-111">Frissítés az Az modulra</span><span class="sxs-lookup"><span data-stu-id="a32f8-111">Upgrade to Az</span></span>

<span data-ttu-id="a32f8-112">Minden felhasználónak javasoljuk, hogy frissítsen az új Az modulra.</span><span class="sxs-lookup"><span data-stu-id="a32f8-112">It's recommended that all users upgrade to the new Az module.</span></span> <span data-ttu-id="a32f8-113">Ehhez tegye a következőket:</span><span class="sxs-lookup"><span data-stu-id="a32f8-113">To do so:</span></span>

* <span data-ttu-id="a32f8-114">__AJÁNLOTT__: [Távolítsa el az Azure PowerShell AzureRM modult.](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="a32f8-114">__RECOMMENDED__: [Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span></span>
* [<span data-ttu-id="a32f8-115">Telepítse az Azure PowerShell Az modult.</span><span class="sxs-lookup"><span data-stu-id="a32f8-115">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="a32f8-116">Engedélyezze a kompatibilitási módot, hogy aliasokat adjon az AzureRM-parancsmagokhoz az `Enable-AzureRMAlias` paranccsal, amíg meg nem ismeri az új parancskészletet.</span><span class="sxs-lookup"><span data-stu-id="a32f8-116">Enable compatibility mode to add aliases for AzureRM cmdlets with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span> <span data-ttu-id="a32f8-117">__Csak__ akkor engedélyezze az aliasokat, ha nincs telepítve az AzureRM.</span><span class="sxs-lookup"><span data-stu-id="a32f8-117">__Only__ enable aliases if you do not have AzureRM installed.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="a32f8-118">Meglévő szkriptek áttelepítése az Az modulba</span><span class="sxs-lookup"><span data-stu-id="a32f8-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="a32f8-119">A jelentősebb frissítések kényelmetlenek tudnak lenni.</span><span class="sxs-lookup"><span data-stu-id="a32f8-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="a32f8-120">Az Az modul kompatibilitási módjával azonban továbbra is használhatja a meglévő szkripteket, miközben az új szintaxis frissítésein dolgozik.</span><span class="sxs-lookup"><span data-stu-id="a32f8-120">However, the Az module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="a32f8-121">Az `Enable-AzureRmAlias` parancsmaggal engedélyezheti az AzureRM kompatibilitási módját.</span><span class="sxs-lookup"><span data-stu-id="a32f8-121">Use the `Enable-AzureRmAlias` cmdlet to enable the AzureRM compatibility mode.</span></span> <span data-ttu-id="a32f8-122">Ez a parancsmag az AzureRM-parancsmagneveket az új Az-parancsmagnevek aliasaként definiálja.</span><span class="sxs-lookup"><span data-stu-id="a32f8-122">This cmdlet defines AzureRM cmdlet names as aliases for the new Az cmdlet names.</span></span>

<span data-ttu-id="a32f8-123">Az új parancsmagnevek úgy lettek kidolgozva, hogy könnyen megjegyezhetők legyenek.</span><span class="sxs-lookup"><span data-stu-id="a32f8-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="a32f8-124">A parancsmagnevekben az `AzureRm` és az `Azure` helyett az `Az` használható.</span><span class="sxs-lookup"><span data-stu-id="a32f8-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="a32f8-125">Például a régi `New-AzureRMVm` parancs megfelelője a `New-AzVm` parancs lett.</span><span class="sxs-lookup"><span data-stu-id="a32f8-125">For example, the old command `New-AzureRMVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="a32f8-126">Az áttelepítési folyamat teljes leírását [az AzureRM modulból az Az modulba való áttelepítést ismertető szakaszban találja](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="a32f8-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="a32f8-127">Az AzureRM jövőbeli támogatottsága</span><span class="sxs-lookup"><span data-stu-id="a32f8-127">The future of support for AzureRM</span></span>

<span data-ttu-id="a32f8-128">A meglévő AzureRM modul nem bővül újabb parancsmagokkal vagy funkciókkal.</span><span class="sxs-lookup"><span data-stu-id="a32f8-128">The existing AzureRM module will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="a32f8-129">Azonban az AzureRM hivatalos karbantartása és hibajavítása 2020 decemberéig nem szűnik meg.</span><span class="sxs-lookup"><span data-stu-id="a32f8-129">However, AzureRM is still officially maintained and will get bug fixes up through December 2020.</span></span> <span data-ttu-id="a32f8-130">Az Azure legfrissebb szolgáltatásainak és funkcióinak használatához térjen át az Az modul használatára.</span><span class="sxs-lookup"><span data-stu-id="a32f8-130">To keep up with the latest Azure services and features, switch to the Az module.</span></span>
