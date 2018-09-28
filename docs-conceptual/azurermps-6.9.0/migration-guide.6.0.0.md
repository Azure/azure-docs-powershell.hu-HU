---
title: A Microsoft Azure PowerShell 6.0.0 kompatibilitástörő változásai
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell 6-os verziójában található kompatibilitástörő változások listáját.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 227bec0f7eb24b0941e9e21d37524b290c4b83a5
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178510"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="8ab95-103">A Microsoft Azure PowerShell 6.0.0 kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

<span data-ttu-id="8ab95-104">Ez a dokumentum egyrészt értesítőül szolgál a használhatatlanná tévő változtatásokról, másrészt egy migrálási útmutató az Azure PowerShell-parancsmagok felhasználóinak.</span><span class="sxs-lookup"><span data-stu-id="8ab95-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="8ab95-105">Minden szakasz tárgyalja a használhatatlanná tévő változások okát, valamint a legkisebb ellenállással járó migrálási módot is.</span><span class="sxs-lookup"><span data-stu-id="8ab95-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="8ab95-106">A körülmények részletesebb leírásáért tekintse meg az egyes változásokhoz tartozó lekérési kérelmeket.</span><span class="sxs-lookup"><span data-stu-id="8ab95-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="8ab95-107">Tartalomjegyzék</span><span class="sxs-lookup"><span data-stu-id="8ab95-107">Table of Contents</span></span>

- [<span data-ttu-id="8ab95-108">Általános kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="8ab95-108">General breaking changes</span></span>](#general-breaking-changes)
    - [<span data-ttu-id="8ab95-109">PowerShell minimálisan szükséges verziója: 5.0</span><span class="sxs-lookup"><span data-stu-id="8ab95-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
    - [<span data-ttu-id="8ab95-110">Környezet automatikus mentése alapértelmezés szerint engedélyezve</span><span class="sxs-lookup"><span data-stu-id="8ab95-110">Context autosaved enabled by default</span></span>](#context-autosave-enabled-by-default)
    - [<span data-ttu-id="8ab95-111">A Tags alias eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8ab95-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="8ab95-112">Az AzureRM.Compute-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="8ab95-113">Az AzureRM.DataLakeStore-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="8ab95-114">Az AzureRM.Dns-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="8ab95-115">Az AzureRM.Insights-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="8ab95-116">Az AzureRM.KeyVault-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="8ab95-117">Az AzureRM.Network-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="8ab95-118">Az AzureRM.RedisCache-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="8ab95-119">Az AzureRM.Resources-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="8ab95-120">Az AzureRM.Storage-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="8ab95-121">Eltávolított modulok</span><span class="sxs-lookup"><span data-stu-id="8ab95-121">Removed modules</span></span>](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="8ab95-122">Általános kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="8ab95-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="8ab95-123">PowerShell minimálisan szükséges verziója: 5.0</span><span class="sxs-lookup"><span data-stu-id="8ab95-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="8ab95-124">Korábban az Azure PowerShellnek _legalább_ a PowerShell 3.0-s verziójára volt szüksége bármely parancsmag futtatásához.</span><span class="sxs-lookup"><span data-stu-id="8ab95-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="8ab95-125">A továbbiakban ez a követelmény a PowerShell 5.0-s verziójára változik.</span><span class="sxs-lookup"><span data-stu-id="8ab95-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="8ab95-126">A PowerShell 5.0-s verziójára történő frissítéssel kapcsolatos információkért lásd [ezt a táblázatot](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="8ab95-126">For information on upgrading to PowerShell 5.0, please see [this table](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="8ab95-127">Környezet alapértelmezés szerinti automatikus mentése</span><span class="sxs-lookup"><span data-stu-id="8ab95-127">Context autosave enabled by default</span></span>

<span data-ttu-id="8ab95-128">A környezet automatikus mentése azon Azure-beli bejelentkezési adatok tárolását jelenti, amelyek a PowerShell új és eltérő munkamenetei között használhatók.</span><span class="sxs-lookup"><span data-stu-id="8ab95-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="8ab95-129">A környezet automatikus mentéséről további információt [ebben a dokumentumban](https://docs.microsoft.com/powershell/azure/context-persistence) talál.</span><span class="sxs-lookup"><span data-stu-id="8ab95-129">For more information on context autosave, please see [this document](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="8ab95-130">A környezet automatikus mentése le volt tiltva korábban alapértelmezés szerint le volt tiltva, ami azt jelentette, hogy a felhasználó Azure-beli hitelesítési adatait nem tárolta a rendszer a munkamenetek között, amíg a környezetmegőrzést engedélyező `Enable-AzureRmContextAutosave` parancsmag nem lett futtatva.</span><span class="sxs-lookup"><span data-stu-id="8ab95-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="8ab95-131">Ezután a környezet automatikus mentése alapértelmezés szerint engedélyezve lesz, ami azt jelenti, hogy a _környezet automatikus mentésére vonatkozó beállításokkal nem rendelkező felhasználók_ esetén a környezet a következő bejelentkezéstől kezdve lesz tárolva.</span><span class="sxs-lookup"><span data-stu-id="8ab95-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="8ab95-132">Ezt a funkciót a `Disable-AzureRmContextAutosave` parancsmag használatával lehet felülbírálni.</span><span class="sxs-lookup"><span data-stu-id="8ab95-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

<span data-ttu-id="8ab95-133">_Megjegyzés:_ A változás nem érinti azokat a felhasználókat, akik korábban letiltották a környezet automatikus mentését, vagy engedélyezték azt, és rendelkeznek meglévő környezettel</span><span class="sxs-lookup"><span data-stu-id="8ab95-133">_Note_: users that previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="8ab95-134">A Tags alias eltávolítása</span><span class="sxs-lookup"><span data-stu-id="8ab95-134">Removal of Tags alias</span></span>

<span data-ttu-id="8ab95-135">A `Tag` paraméter `Tags` aliasa több parancsmag esetén is el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8ab95-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="8ab95-136">Az alábbi lista tartalmazza az érintett modulokat (és a hozzájuk tartozó parancsmagokat):</span><span class="sxs-lookup"><span data-stu-id="8ab95-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="8ab95-137">Az AzureRM.Compute-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="8ab95-138">**Egyéb**</span><span class="sxs-lookup"><span data-stu-id="8ab95-138">**Miscellaneous**</span></span>
- <span data-ttu-id="8ab95-139">A `PSDisk` és `PSSnapshot` típus beágyazott termékváltozat-tulajdonsága `StandardLRS` és `PremiumLRS` értékről `Standard_LRS` és `Premium_LRS` értékre változott</span><span class="sxs-lookup"><span data-stu-id="8ab95-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="8ab95-140">A `PSVirtualMachine`, `PSVirtualMachineScaleSet` és `PSImage` típus beágyazott tárfióktípus-tulajdonsága `StandardLRS` és `PremiumLRS` értékről `Standard_LRS` és `Premium_LRS` értékre változott</span><span class="sxs-lookup"><span data-stu-id="8ab95-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="8ab95-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="8ab95-141">**Add-AzureRmImageDataDisk**</span></span>
- <span data-ttu-id="8ab95-142">A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="8ab95-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="8ab95-143">**Add-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="8ab95-144">A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="8ab95-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="8ab95-145">**Add-AzureRmVmssDataDisk**</span></span>
- <span data-ttu-id="8ab95-146">A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="8ab95-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="8ab95-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="8ab95-148">A `Managed` paraméter el lett távolítva, és helyébe a `Sku` lépett</span><span class="sxs-lookup"><span data-stu-id="8ab95-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="8ab95-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="8ab95-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="8ab95-150">A `SkuName` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="8ab95-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="8ab95-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="8ab95-152">A `SkuName` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="8ab95-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="8ab95-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="8ab95-154">A `SkuName` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="8ab95-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="8ab95-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="8ab95-156">A `SkuName` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="8ab95-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="8ab95-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="8ab95-158">A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="8ab95-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="8ab95-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="8ab95-160">A `DisableWAD` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="8ab95-161">A Microsoft Azure Diagnostics alapértelmezés szerint le van tiltva</span><span class="sxs-lookup"><span data-stu-id="8ab95-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="8ab95-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="8ab95-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="8ab95-163">A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="8ab95-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="8ab95-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="8ab95-165">A `StorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="8ab95-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="8ab95-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="8ab95-167">A `ManagedDisk` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="8ab95-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="8ab95-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="8ab95-169">A `ManagedDiskStorageAccountType` paraméter elfogadott értéke `StandardLRS` és `PremiumLRS` helyett `Standard_LRS` és `Premium_LRS` lett</span><span class="sxs-lookup"><span data-stu-id="8ab95-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="8ab95-170">Az AzureRM.DataLakeStore-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="8ab95-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="8ab95-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="8ab95-172">A `PerFileThreadCount` és a `ConcurrentFileCount` paraméter el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8ab95-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="8ab95-173">A továbbiakban a `Concurrency` paramétert használhatja</span><span class="sxs-lookup"><span data-stu-id="8ab95-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="8ab95-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="8ab95-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="8ab95-175">A `PerFileThreadCount` és a `ConcurrentFileCount` paraméter el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8ab95-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="8ab95-176">A továbbiakban a `Concurrency` paramétert használhatja</span><span class="sxs-lookup"><span data-stu-id="8ab95-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="8ab95-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="8ab95-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="8ab95-178">A `Clean` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-178">Parameter `Clean` was removed</span></span>

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="8ab95-179">Az AzureRM.Dns-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="8ab95-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="8ab95-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="8ab95-181">A `Force` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="8ab95-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="8ab95-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="8ab95-183">A `Force` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="8ab95-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="8ab95-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="8ab95-185">A `Force` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="8ab95-186">Az AzureRM.Insights-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="8ab95-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="8ab95-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="8ab95-188">A `AutoscaleProfiles` és `Notifications` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="8ab95-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="8ab95-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="8ab95-190">A `Categories` és `Locations` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="8ab95-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="8ab95-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="8ab95-192">A `Actions` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="8ab95-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="8ab95-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="8ab95-194">A `Actions` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="8ab95-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="8ab95-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="8ab95-196">A `MaxRecords` és `MaxEvents` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="8ab95-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="8ab95-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="8ab95-198">A `MetricNames` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="8ab95-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="8ab95-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="8ab95-200">A `CustomEmails` és `SendToServiceOwners` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="8ab95-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="8ab95-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="8ab95-202">A `Properties` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="8ab95-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="8ab95-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="8ab95-204">A `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` és `Webhooks` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="8ab95-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="8ab95-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="8ab95-206">A `Rules`, `ScheduleDays`, `ScheduleHours` és `ScheduleMinutes` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="8ab95-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="8ab95-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="8ab95-208">A `Properties` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="8ab95-209">Az AzureRM.KeyVault-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="8ab95-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="8ab95-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="8ab95-211">A `CertificatePolicy` paraméter használata kötelezővé vált.</span><span class="sxs-lookup"><span data-stu-id="8ab95-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="8ab95-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="8ab95-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="8ab95-213">A parancsmag többé már nem fogad olyan paramétereket, amelyek a hozzáférési jogkivonatot határozzák meg. Ehelyett a parancsmag lecseréli az olyan kifejezett jogkivonat-paramétereket, mint a `Service` és a `Permissions` egy általános `TemplateUri` paraméterre, amely egy máshol (valószínűleg Storage PowerShell-parancsmagokkal vagy a Storage-dokumentáció alapján manuálisan) meghatározott hozzáférési mintajogkivonatnak feleltethető meg. A parancsmag megőrzi a `ValidityPeriod` paramétert.</span><span class="sxs-lookup"><span data-stu-id="8ab95-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="8ab95-214">Az Azure Storage megosztott hozzáférési jogkivonatok létrehozásával kapcsolatos további információiért tekintse meg az alábbi dokumentációs oldalakat:</span><span class="sxs-lookup"><span data-stu-id="8ab95-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>
- <span data-ttu-id="8ab95-215">[SAS-szolgáltatás létrehozása] (https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)</span><span class="sxs-lookup"><span data-stu-id="8ab95-215">[Constructing a Service SAS] (https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)</span></span>
- <span data-ttu-id="8ab95-216">[SAS-fiók létrehozása] (https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)</span><span class="sxs-lookup"><span data-stu-id="8ab95-216">[Constructing an Account SAS] (https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)</span></span>

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

<span data-ttu-id="8ab95-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="8ab95-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="8ab95-218">A `IssuerProvider` paraméter használata kötelezővé vált.</span><span class="sxs-lookup"><span data-stu-id="8ab95-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="8ab95-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="8ab95-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="8ab95-220">A parancsmag kimenete `CertificateBundle` értékről `PSKeyVaultCertificate` értékre változott.</span><span class="sxs-lookup"><span data-stu-id="8ab95-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="8ab95-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="8ab95-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="8ab95-222">A `ResourceGroupName` el lett távolítva az `InputObject` paraméterkészletből, és ehelyett az `InputObject` paraméter `ResourceId` tulajdonságából lesz származtatva.</span><span class="sxs-lookup"><span data-stu-id="8ab95-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="8ab95-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="8ab95-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="8ab95-224">Az `all` engedély el lett távolítva a `PermissionsToKeys`, `PermissionsToSecrets` és `PermissionsToCertificates` esetén.</span><span class="sxs-lookup"><span data-stu-id="8ab95-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="8ab95-225">**Általános**</span><span class="sxs-lookup"><span data-stu-id="8ab95-225">**General**</span></span>
- <span data-ttu-id="8ab95-226">A `ValueFromPipelineByPropertyName` tulajdonság el lett távolítva az összes olyan parancsmagból, ahol az `InputObject` általi átirányítás engedélyezve volt.</span><span class="sxs-lookup"><span data-stu-id="8ab95-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span>  <span data-ttu-id="8ab95-227">Az érintett parancsmagok az alábbiak:</span><span class="sxs-lookup"><span data-stu-id="8ab95-227">The cmdlets affected are:</span></span>
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="8ab95-228">A `ConfirmImpact`-szintek el lettek távolítva az összes parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="8ab95-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="8ab95-229">Az érintett parancsmagok az alábbiak:</span><span class="sxs-lookup"><span data-stu-id="8ab95-229">The cmdlets affected are:</span></span>
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="8ab95-230">Az `IKeyVaultDataServiceClient` frissítve lett, ezáltal az összes tanúsítványművelet PS-típust ad vissza SDK-típus helyett.</span><span class="sxs-lookup"><span data-stu-id="8ab95-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="8ab95-231">Az érintett műveletek közé tartoznak az alábbiak:</span><span class="sxs-lookup"><span data-stu-id="8ab95-231">This includes:</span></span>
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="8ab95-232">Az AzureRM.Network-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="8ab95-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="8ab95-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="8ab95-234">A `ProbeEnabled` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="8ab95-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="8ab95-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="8ab95-236">A `AlloowGatewayTransit` paraméteralias el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="8ab95-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="8ab95-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="8ab95-238">A `ProbeEnabled` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="8ab95-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="8ab95-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="8ab95-240">A `ProbeEnabled` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="8ab95-241">Az AzureRM.RedisCache-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="8ab95-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="8ab95-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="8ab95-243">A `Subnet` és `VirtualNetwork` paraméter el lett távolítva, és a helyükbe a `SubnetId` lépett</span><span class="sxs-lookup"><span data-stu-id="8ab95-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="8ab95-244">A `RedisVersion` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="8ab95-245">A `MaxMemoryPolicy` paraméter el lett távolítva, és helyébe a `RedisConfiguration` lépett</span><span class="sxs-lookup"><span data-stu-id="8ab95-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="8ab95-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="8ab95-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="8ab95-247">A `MaxMemoryPolicy` paraméter el lett távolítva, és helyébe a `RedisConfiguration` lépett</span><span class="sxs-lookup"><span data-stu-id="8ab95-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="8ab95-248">Az AzureRM.Resources-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="8ab95-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="8ab95-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="8ab95-250">A parancsmag el lett távolítva, és a funkcióit mostantól a `Get-AzureRmResource` teszi elérhetővé</span><span class="sxs-lookup"><span data-stu-id="8ab95-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="8ab95-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="8ab95-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="8ab95-252">A parancsmag el lett távolítva, és a funkcióit mostantól a `Get-AzureRmResourceGroup` teszi elérhetővé</span><span class="sxs-lookup"><span data-stu-id="8ab95-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

<span data-ttu-id="8ab95-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="8ab95-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="8ab95-254">Az `AtScopeAndBelow` paraméter el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="8ab95-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="8ab95-255">Az AzureRM.Storage-parancsmagok kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="8ab95-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="8ab95-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="8ab95-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="8ab95-257">A `EnableEncryptionService` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="8ab95-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="8ab95-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="8ab95-259">Az `EnableEncryptionService` és a `DisableEncryptionService` paraméter el lett távolítva</span><span class="sxs-lookup"><span data-stu-id="8ab95-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="8ab95-260">Eltávolított modulok</span><span class="sxs-lookup"><span data-stu-id="8ab95-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="8ab95-261">A Server Management Tools szolgáltatás a [múlt évben ki lett vezetve](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), ezért az SMT megfelelő modulja, az `AzureRM.ServerManagement` el lett távolítva az `AzureRM`-ből, és a továbbiakban nem lesz érhető.</span><span class="sxs-lookup"><span data-stu-id="8ab95-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="8ab95-262">A `AzureRM.SiteRecovery` modult felváltja az `AzureRM.RecoveryServices.SiteRecovery`, ami az `AzureRM.SiteRecovery` modul bővebb tulajdonságokkal rendelkező változata, és új, a korábbiak működését biztosító parancsmagokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="8ab95-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="8ab95-263">A régi parancsmagok az újakba történő leképezésének listáját az alábbiakban találja:</span><span class="sxs-lookup"><span data-stu-id="8ab95-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="8ab95-264">Elavult parancsmag</span><span class="sxs-lookup"><span data-stu-id="8ab95-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="8ab95-265">Egyenértékű parancsmag</span><span class="sxs-lookup"><span data-stu-id="8ab95-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="8ab95-266">Aliasok</span><span class="sxs-lookup"><span data-stu-id="8ab95-266">Aliases</span></span>                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |