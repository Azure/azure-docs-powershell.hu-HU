---
title: Migrálási útmutató az Az 2.0.0-s verziójához
description: Ebben a migrálási útmutatóban megtalálja az Azure PowerShell Az 2.0-s verziójában található kompatibilitástörő változások listáját.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 133769c09f74e1d0d90eff0c6c4bdbb90d1ebe24
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/10/2020
ms.locfileid: "79035702"
---
# <a name="migration-guide-for-az-200"></a>Migrálási útmutató az Az 2.0.0-s verziójához

Ez a dokumentum ismerteti, hogy milyen módosítások történtek az Az 1.0.0-s és 2.0.0-s verziója között 

## <a name="table-of-contents"></a>Tartalomjegyzék
- [A modul kompatibilitástörő változásai](#module-breaking-changes)
  - [Az.Compute](#azcompute)
  - [Az.HDInsight](#azhdinsight)
  - [Az.Storage](#azstorage)

## <a name="module-breaking-changes"></a>A modul kompatibilitástörő változásai

### <a name="azcompute"></a>Az.Compute

- A `New-AzAvailabilitySet` és `Update-AzAvailabilitySet` parancsmag `Managed` paraméterét a következő váltotta fel: ```Sku = Aligned```

  #### <a name="before"></a>Előtte

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a>Utána

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- A konzisztencia érdekében az `Image` paraméter el lett távolítva az `Update-AzImage` „ByName” és a „ByResourceId” paraméterkészleteiből 
  
  #### <a name="before"></a>Előtte

  Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott ImageName paramétert, így a paraméter eltávolítása nem befolyásolja a működését.

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a>Utána

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Restart-AzVM` „ByObject” és „ByResourceId” paraméterkészleteiből
  
  #### <a name="before"></a>Előtte

  Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Utána

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Start-AzVM` „ByObject” és „ByResourceId” paraméterkészleteiből
  
  #### <a name="before"></a>Előtte

  Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Utána

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Stop-AzVM` „ByObject” és „ByResourceId” paraméterkészleteiből
  
  #### <a name="before"></a>Előtte

  Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Utána

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Remove-AzVM` „ByObject” és „ByResourceId” paraméterkészleteiből
  
  #### <a name="before"></a>Előtte

  Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a>Utána

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Set-AzVM` „ByObject” és „ByResourceId” paraméterkészleteiből
  
  #### <a name="before"></a>Előtte

  Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a>Utána

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- A konzisztencia érdekében a `Name` paraméter el lett távolítva a `Save-AzVMImage` „ByObject” és „ByResourceId” paraméterkészleteiből 
  
  #### <a name="before"></a>Előtte
  Vegye figyelembe, hogy az alábbi kód működik, de nem használja az átadott Name paramétert, így a paraméter eltávolítása nem befolyásolja a működését.
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a>Utána
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- A ProtectionPolicy tulajdonság hozzá lett adva, hogy beágyazza a `ProtectFromScaleIn` tulajdonságot a következőbe: `PSVirtualMachineScaleSetVM`

  #### <a name="before"></a>Előtte

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a>Utána

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- Az ```EncryptionSettingsCollection``` tulajdonság hozzá lett adva, hogy belefoglalja az `EncryptionSettings` tulajdonságot a következőbe: `PSDisk`

  #### <a name="before"></a>Előtte

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

  #### <a name="after"></a>Utána

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

- Az ```EncryptionSettingsCollection``` tulajdonság hozzá lett adva, hogy belefoglalja az `EncryptionSettings` tulajdonságot a következőbe: `PSSnapshot`

  #### <a name="before"></a>Előtte

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

  #### <a name="after"></a>Utána

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

- `VirtualMachineProfile` tulajdonság eltávolítva a következőből: `PSVirtualMachineScaleSet`

  #### <a name="before"></a>Előtte

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a>Utána

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- A `Set-AzVMBootDiagnostic` parancsmag eltávolította az aliast a következőből: `Set-AzVMBootDiagnostics`

  #### <a name="before"></a>Előtte

  Elavult alias használata

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a>Utána

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- A `Export-AzLogAnalyticThrottledRequest` parancsmag eltávolította az aliast a következőből: `Export-AzLogAnalyticThrottledRequests`

  #### <a name="before"></a>Előtte

  Elavult alias használata

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a>Utána

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a>Az.HDInsight

- A `Grant-AzHDInsightHttpServicesAccess` és a `Revoke-AzHDInsightHttpServicesAccess` parancsmag el lett távolítva. Már nincs szükség rájuk, mivel a HTTP-hozzáférés mindig engedélyezve van a HDInsight-fürtökön.
- Új `Set-AzHDInsightGatewayCredential` parancsmag hozzáadva. A parancsmag használatával módosíthatja az átjáró HTTP-felhasználónevét és -jelszavát (a `Grant-AzHDInsightHttpServicesAccess` helyébe lép).
- Frissült a `Get-AzHDInsightJobOutput` parancsmag, és mostantól támogatja a tárkulcshoz való részletes szerepköralapú hozzáférést.
    - Ez nem érinti a HDInsight-fürt operátor, közreműködő vagy tulajdonos szerepkörrel rendelkező felhasználóit.
    - A csak olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a `DefaultStorageAccountKey` paramétert.

A szerepköralapú hozzáférés változásaival kapcsolatos további információért lásd: [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)

  #### <a name="before"></a>Előtte

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a>Utána

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a>A Get-AzHDInsightJobOutput parancsmaghoz csak olvasói szerepkörrel rendelkező felhasználók

  ####  <a name="before"></a>Előtte

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a>Utána

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a>Az.Storage

- A Blob, a Queue és a File parancsmagok által visszaadott típusok névterei `Microsoft.WindowsAzure.Storage`-ról `Microsoft.Azure.Storage`-ra módosultak.  Bár ez a kompatibilitástörő változások szabályzata szerint technikailag nem számít kompatibilitástörő változásnak, előfordulhat, hogy végre kell hajtani néhány módosítást olyan kódokban, amelyek a Storage .Net SDK metódusaival kommunikálnak a parancsmagok által visszaadott objektumokkal.

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a>1\. példa:  Üzenet felvétele az üzenetsorba (a CloudQueueMessage objektumnévterének módosítása)

  Előtte: 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  Utána:

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a>2\. példa  Blob-/Fájlattribútumok lehívása az AccessCondition használatával (az AccessCondition objektumnévterének módosítása)

  Előtte: 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  Utána:

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- Bár ez technikailag nem számít kompatibilitástörő változásnak, észrevehet néhány kimeneti különbséget a `New/Get/Set-AzStorageAccount` által visszaadott tárfiókok Sku.Name tulajdonságában. (A módosítás után a SkuName kimenete és bemenete egymáshoz lesz igazítva.)
  - „StandardLRS” -> „Standard_LRS”;
  - „StandardGRS” -> „Standard_GRS”;
  - „StandardRAGRS” -> „Standard_RAGRS”;
  - „StandardZRS” -> „Standard_ZRS”;
  - „PremiumLRS” -> „Premium_LRS”;

- Megváltozott a szolgáltatás alapértelmezett viselkedése a tárfiókok altípus megadása nélküli létrehozásakor.  A korábbi verziókban a tárfiókok `Kind` megadása nélküli létrehozásakor a rendszer a tárfiók `Storage` altípusát használta. Az új verzióban a `StorageV2` a `Kind` alapértelmezett értéke. Ha létre kell hoznia egy V1-tárfiókot a „Storage” altípussal, adja hozzá a „-Kind Storage” paramétert.

  #### <a name="example--create-a-storage-account-default-kind-change"></a>Például: Tárfiók létrehozása (Alapértelmezett altípus módosítása)  

  Előtte:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  Utána:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
