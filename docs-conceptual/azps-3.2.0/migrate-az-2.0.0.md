---
title: Migrálási útmutató az Az 2.0.0-s verziójához
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 2.0-s verziójában található kompatibilitástörő változások listáját.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 5f15d1a4f1e8416d7214aceb78494867fe4aad52
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182179"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="fdbf6-103">Migrálási útmutató az Az 2.0.0-s verziójához</span><span class="sxs-lookup"><span data-stu-id="fdbf6-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="fdbf6-104">Ez a dokumentum ismerteti, hogy milyen módosítások történtek az Az 1.0.0-s és 2.0.0-s verziója között</span><span class="sxs-lookup"><span data-stu-id="fdbf6-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="fdbf6-105">Tartalomjegyzék</span><span class="sxs-lookup"><span data-stu-id="fdbf6-105">Table of Contents</span></span>
- [<span data-ttu-id="fdbf6-106">A modul kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="fdbf6-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="fdbf6-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fdbf6-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="fdbf6-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fdbf6-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="fdbf6-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fdbf6-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="fdbf6-110">A modul kompatibilitástörő változásai</span><span class="sxs-lookup"><span data-stu-id="fdbf6-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="fdbf6-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="fdbf6-111">Az.Compute</span></span>

- <span data-ttu-id="fdbf6-112">A `New-AzAvailabilitySet` és `Update-AzAvailabilitySet` parancsmag `Managed` paraméterét a következő váltotta fel: ```Sku = Aligned```</span><span class="sxs-lookup"><span data-stu-id="fdbf6-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="fdbf6-113">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-114">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="fdbf6-115">A konzisztencia érdekében az `Image` paraméter el lett távolítva az `Update-AzImage` „ByName” és a „ByResourceId” paraméterkészleteiből</span><span class="sxs-lookup"><span data-stu-id="fdbf6-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="fdbf6-116">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-116">Before</span></span>

  <span data-ttu-id="fdbf6-117">Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott ImageName paramétert, így a paraméter eltávolítása nem befolyásolja a működését.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-118">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="fdbf6-119">A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Restart-AzVM` „ByObject” és „ByResourceId” paraméterkészleteiből</span><span class="sxs-lookup"><span data-stu-id="fdbf6-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="fdbf6-120">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-120">Before</span></span>

  <span data-ttu-id="fdbf6-121">Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-122">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="fdbf6-123">A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Start-AzVM` „ByObject” és „ByResourceId” paraméterkészleteiből</span><span class="sxs-lookup"><span data-stu-id="fdbf6-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="fdbf6-124">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-124">Before</span></span>

  <span data-ttu-id="fdbf6-125">Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-126">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="fdbf6-127">A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Stop-AzVM` „ByObject” és „ByResourceId” paraméterkészleteiből</span><span class="sxs-lookup"><span data-stu-id="fdbf6-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="fdbf6-128">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-128">Before</span></span>

  <span data-ttu-id="fdbf6-129">Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-130">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="fdbf6-131">A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Remove-AzVM` „ByObject” és „ByResourceId” paraméterkészleteiből</span><span class="sxs-lookup"><span data-stu-id="fdbf6-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="fdbf6-132">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-132">Before</span></span>

  <span data-ttu-id="fdbf6-133">Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-134">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="fdbf6-135">A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Set-AzVM` „ByObject” és „ByResourceId” paraméterkészleteiből</span><span class="sxs-lookup"><span data-stu-id="fdbf6-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="fdbf6-136">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-136">Before</span></span>

  <span data-ttu-id="fdbf6-137">Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-138">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="fdbf6-139">A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Save-AzVMImage` „ByObject” és „ByResourceId” paraméterkészleteiből</span><span class="sxs-lookup"><span data-stu-id="fdbf6-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="fdbf6-140">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-140">Before</span></span>
  <span data-ttu-id="fdbf6-141">Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="fdbf6-142">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="fdbf6-143">A ProtectionPolicy tulajdonság hozzá lett adva, hogy beágyazza a `ProtectFromScaleIn` tulajdonságot a következőbe: `PSVirtualMachineScaleSetVM`</span><span class="sxs-lookup"><span data-stu-id="fdbf6-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="fdbf6-144">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-145">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="fdbf6-146">Az ```EncryptionSettingsCollection``` tulajdonság hozzá lett adva, hogy belefoglalja az `EncryptionSettings` tulajdonságot a következőbe: `PSDisk`</span><span class="sxs-lookup"><span data-stu-id="fdbf6-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="fdbf6-147">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-147">Before</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-148">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-148">After</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="fdbf6-149">Az ```EncryptionSettingsCollection``` tulajdonság hozzá lett adva, hogy belefoglalja az `EncryptionSettings` tulajdonságot a következőbe: `PSSnapshot`</span><span class="sxs-lookup"><span data-stu-id="fdbf6-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="fdbf6-150">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-150">Before</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-151">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-151">After</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="fdbf6-152">`VirtualMachineProfile` tulajdonság eltávolítva a következőből: `PSVirtualMachineScaleSet`</span><span class="sxs-lookup"><span data-stu-id="fdbf6-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="fdbf6-153">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-154">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="fdbf6-155">A `Set-AzVMBootDiagnostic` parancsmag eltávolította az aliast a következőből: `Set-AzVMBootDiagnostics`</span><span class="sxs-lookup"><span data-stu-id="fdbf6-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="fdbf6-156">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-156">Before</span></span>

  <span data-ttu-id="fdbf6-157">Elavult alias használata</span><span class="sxs-lookup"><span data-stu-id="fdbf6-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-158">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="fdbf6-159">A `Export-AzLogAnalyticThrottledRequest` parancsmag eltávolította az aliast a következőből: `Export-AzLogAnalyticThrottledRequests`</span><span class="sxs-lookup"><span data-stu-id="fdbf6-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="fdbf6-160">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-160">Before</span></span>

  <span data-ttu-id="fdbf6-161">Elavult alias használata</span><span class="sxs-lookup"><span data-stu-id="fdbf6-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-162">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="fdbf6-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fdbf6-163">Az.HDInsight</span></span>

- <span data-ttu-id="fdbf6-164">A `Grant-AzHDInsightHttpServicesAccess` és a `Revoke-AzHDInsightHttpServicesAccess` parancsmag el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="fdbf6-165">Már nincs szükség rájuk, mivel a HTTP-hozzáférés mindig engedélyezve van a HDInsight-fürtökön.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="fdbf6-166">Új `Set-AzHDInsightGatewayCredential` parancsmag hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="fdbf6-167">A parancsmag használatával módosíthatja az átjáró HTTP-felhasználónevét és -jelszavát (a `Grant-AzHDInsightHttpServicesAccess` helyébe lép).</span><span class="sxs-lookup"><span data-stu-id="fdbf6-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="fdbf6-168">Frissült a `Get-AzHDInsightJobOutput` parancsmag, és mostantól támogatja a tárkulcshoz való részletes szerepköralapú hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="fdbf6-169">Ez nem érinti a HDInsight-fürt operátor, közreműködő vagy tulajdonos szerepkörrel rendelkező felhasználóit.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="fdbf6-170">A csak olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a `DefaultStorageAccountKey` paramétert.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="fdbf6-171">A szerepköralapú hozzáférés változásaival kapcsolatos további információért lásd: [aka.ms/hdi-config-update](http://aka.ms/hdi-config-update)</span><span class="sxs-lookup"><span data-stu-id="fdbf6-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](http://aka.ms/hdi-config-update)</span></span>

  #### <a name="before"></a><span data-ttu-id="fdbf6-172">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-173">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="fdbf6-174">A Get-AzHDInsightJobOutput parancsmaghoz csak olvasói szerepkörrel rendelkező felhasználók</span><span class="sxs-lookup"><span data-stu-id="fdbf6-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="fdbf6-175">Előtte</span><span class="sxs-lookup"><span data-stu-id="fdbf6-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="fdbf6-176">Utána</span><span class="sxs-lookup"><span data-stu-id="fdbf6-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="fdbf6-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="fdbf6-177">Az.Storage</span></span>

- <span data-ttu-id="fdbf6-178">A Blob, a Queue és a File parancsmagok által visszaadott típusok névterei `Microsoft.WindowsAzure.Storage`-ról `Microsoft.Azure.Storage`-ra módosultak.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="fdbf6-179">Bár ez a kompatibilitástörő változások szabályzata szerint technikailag nem számít kompatibilitástörő változásnak, előfordulhat, hogy végre kell hajtani néhány módosítást olyan kódokban, amelyek a Storage .Net SDK metódusaival kommunikálnak a parancsmagok által visszaadott objektumokkal.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="fdbf6-180">1\. példa:  Üzenet felvétele az üzenetsorba (a CloudQueueMessage objektumnévterének módosítása)</span><span class="sxs-lookup"><span data-stu-id="fdbf6-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="fdbf6-181">Előtte:</span><span class="sxs-lookup"><span data-stu-id="fdbf6-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="fdbf6-182">Utána:</span><span class="sxs-lookup"><span data-stu-id="fdbf6-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="fdbf6-183">2\. példa  Blob-/Fájlattribútumok lehívása az AccessCondition használatával (az AccessCondition objektumnévterének módosítása)</span><span class="sxs-lookup"><span data-stu-id="fdbf6-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="fdbf6-184">Előtte:</span><span class="sxs-lookup"><span data-stu-id="fdbf6-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="fdbf6-185">Utána:</span><span class="sxs-lookup"><span data-stu-id="fdbf6-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="fdbf6-186">Bár ez technikailag nem számít kompatibilitástörő változásnak, észrevehet néhány kimeneti különbséget a `New/Get/Set-AzStorageAccount` által visszaadott tárfiókok Sku.Name tulajdonságában.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="fdbf6-187">(A módosítás után a SkuName kimenete és bemenete egymáshoz lesz igazítva.)</span><span class="sxs-lookup"><span data-stu-id="fdbf6-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="fdbf6-188">„StandardLRS” -> „Standard_LRS”;</span><span class="sxs-lookup"><span data-stu-id="fdbf6-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="fdbf6-189">„StandardGRS” -> „Standard_GRS”;</span><span class="sxs-lookup"><span data-stu-id="fdbf6-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="fdbf6-190">„StandardRAGRS” -> „Standard_RAGRS”;</span><span class="sxs-lookup"><span data-stu-id="fdbf6-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="fdbf6-191">„StandardZRS” -> „Standard_ZRS”;</span><span class="sxs-lookup"><span data-stu-id="fdbf6-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="fdbf6-192">„PremiumLRS” -> „Premium_LRS”;</span><span class="sxs-lookup"><span data-stu-id="fdbf6-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="fdbf6-193">Megváltozott a szolgáltatás alapértelmezett viselkedése a tárfiókok altípus megadása nélküli létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="fdbf6-194">A korábbi verziókban a tárfiókok `Kind` megadása nélküli létrehozásakor a rendszer a tárfiók `Storage` altípusát használta. Az új verzióban a `StorageV2` a `Kind` alapértelmezett értéke.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="fdbf6-195">Ha létre kell hoznia egy V1-tárfiókot a „Storage” altípussal, adja hozzá a „-Kind Storage” paramétert.</span><span class="sxs-lookup"><span data-stu-id="fdbf6-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="fdbf6-196">Például: Tárfiók létrehozása (Alapértelmezett altípus módosítása)</span><span class="sxs-lookup"><span data-stu-id="fdbf6-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="fdbf6-197">Előtte:</span><span class="sxs-lookup"><span data-stu-id="fdbf6-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="fdbf6-198">Utána:</span><span class="sxs-lookup"><span data-stu-id="fdbf6-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```