---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 52e4a9b76adc8c8980ab20951278435894a303bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187212"
---
# <span data-ttu-id="7e47b-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7e47b-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="7e47b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e47b-102">SYNOPSIS</span></span>

<span data-ttu-id="7e47b-103">Egy biztonsági elem adatainak és konfigurációjának visszaállítása a helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="7e47b-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="7e47b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e47b-104">SYNTAX</span></span>

### <span data-ttu-id="7e47b-105">AzureVMParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e47b-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e47b-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e47b-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e47b-107">AzureVMRestoreAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="7e47b-107">AzureVMRestoreAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e47b-108">AzureVMTargetRGParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e47b-108">AzureVMTargetRGParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e47b-109">AzureVMUseOSAParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e47b-109">AzureVMUseOSAParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e47b-110">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e47b-110">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e47b-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e47b-111">DESCRIPTION</span></span>

<span data-ttu-id="7e47b-112">A **Restore-AzRecoveryServicesBackupItem** parancsmag visszaállítja az Azure Backup-elemek adatát és konfigurációját egy megadott helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="7e47b-112">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="7e47b-113">Ez a parancsmag a helyreállítási szolgáltatások boltozatról az ügyfél tárterületére való visszaállítást indítja el.</span><span class="sxs-lookup"><span data-stu-id="7e47b-113">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="7e47b-114">A visszaállítási művelet nem állítja vissza a teljes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="7e47b-114">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="7e47b-115">Ha a visszaállítási művelet befejezése után visszaállítja a távtárolású lemezeket az ügyfél-tároló fiókba, létre kell hoznia a virtuális gépet, és el kell indítania.</span><span class="sxs-lookup"><span data-stu-id="7e47b-115">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="7e47b-116">További tudnivalókért tekintse át a refter és a paraméter szövegét.</span><span class="sxs-lookup"><span data-stu-id="7e47b-116">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="7e47b-117">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="7e47b-117">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="7e47b-118">Megjegyzés: a parancsmag sikeres végrehajtásához a-VaultId paraméter-VaultLocation paraméteren kívül is használni kell.</span><span class="sxs-lookup"><span data-stu-id="7e47b-118">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="7e47b-119">Példák</span><span class="sxs-lookup"><span data-stu-id="7e47b-119">EXAMPLES</span></span>

### <span data-ttu-id="7e47b-120">1. példa: elem visszaállítása helyreállítási pontra</span><span class="sxs-lookup"><span data-stu-id="7e47b-120">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="7e47b-121">Az első parancs megkapja a RecoveryServices boltozatot, és $vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-121">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="7e47b-122">A második parancs beolvassa a biztonsági másolat elemeit, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-122">The second command gets the Backup items and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="7e47b-123">A harmadik parancs hét nappal korábban kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-123">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="7e47b-124">A negyedik parancs a jelenlegi dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-124">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="7e47b-125">Az ötödik parancs beolvassa az $StartDate és a $EndDate által szűrt adott biztonsági másolat helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="7e47b-125">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="7e47b-126">A hatodik parancs azt adja meg, hogy mely lemezek legyenek helyreállítva a helyreállítási pontból, és a $restoreDiskLUNs változóban legyenek tárolva.</span><span class="sxs-lookup"><span data-stu-id="7e47b-126">The sixth command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="7e47b-127">Az utolsó parancs visszaállítja a lemezeket a TARGET Storage DestAccount a DestRG erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="7e47b-127">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="7e47b-128">2. példa: egy AzureFileShare-elem több fájljának visszaállítása</span><span class="sxs-lookup"><span data-stu-id="7e47b-128">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="7e47b-129">Az első parancs a AzureVM típusú biztonsági tárolót kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-129">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="7e47b-130">A második parancs a fileshareitem nevű biztonsági másolatot kapja, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-130">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="7e47b-131">A harmadik parancs beolvassa az adott biztonságimásolat-elem helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="7e47b-131">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="7e47b-132">A negyedik parancs spceifies, hogy mely fájlok legyenek visszaállíthatók és tárolva $files változóban.</span><span class="sxs-lookup"><span data-stu-id="7e47b-132">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="7e47b-133">Az utolsó parancs visszaállítja a megadott fájlokat az eredeti helyükre.</span><span class="sxs-lookup"><span data-stu-id="7e47b-133">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="7e47b-134">3. példa</span><span class="sxs-lookup"><span data-stu-id="7e47b-134">Example 3</span></span>

<span data-ttu-id="7e47b-135">Egy biztonsági elem adatainak és konfigurációjának visszaállítása a helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="7e47b-135">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="7e47b-136">autogenerated</span><span class="sxs-lookup"><span data-stu-id="7e47b-136">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```
### <span data-ttu-id="7e47b-137">Példa 4: felügyelt virtuális gép visszaállítása kezelt lemezekként</span><span class="sxs-lookup"><span data-stu-id="7e47b-137">Example 4: Restore a managed VM as managed Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="7e47b-138">Az első parancs megkapja a RecoveryServices boltozatot, és $vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-138">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="7e47b-139">A második parancs a biztonsági másolatot kapja, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-139">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="7e47b-140">A harmadik parancs hét nappal korábban kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-140">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="7e47b-141">A negyedik parancs a jelenlegi dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-141">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="7e47b-142">Az ötödik parancs beolvassa az $StartDate és a $EndDate által szűrt adott biztonsági másolat helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="7e47b-142">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="7e47b-143">A hatodik parancs visszaállítja a lemezeket a megadott cél erőforráscsoporthoz tartozó kezelt lemezekként.</span><span class="sxs-lookup"><span data-stu-id="7e47b-143">The sixth command restores the disks as managed disks with the given target resource group.</span></span>

### <span data-ttu-id="7e47b-144">Példa 5: felügyelt VM visszaállítása nem felügyelt lemezekként</span><span class="sxs-lookup"><span data-stu-id="7e47b-144">Example 5: Restore a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="7e47b-145">Az első parancs megkapja a RecoveryServices boltozatot, és $vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-145">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="7e47b-146">A második parancs a biztonsági másolatot kapja, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-146">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="7e47b-147">A harmadik parancs hét nappal korábban kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-147">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="7e47b-148">A negyedik parancs a jelenlegi dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-148">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="7e47b-149">Az ötödik parancs beolvassa az $StartDate és a $EndDate által szűrt adott biztonsági másolat helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="7e47b-149">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="7e47b-150">A hatodik parancs visszaállítja a lemezeket nem felügyelt lemezekként.</span><span class="sxs-lookup"><span data-stu-id="7e47b-150">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="7e47b-151">Példa 6: nem felügyelt VM visszaállítása nem felügyelt lemezek esetén eredeti tárterület-fiókkal.</span><span class="sxs-lookup"><span data-stu-id="7e47b-151">Example 6: Restore an unmanaged VM as unmanaged Disks using original storage account.</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="7e47b-152">Az első parancs megkapja a RecoveryServices boltozatot, és $vault változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="7e47b-153">A második parancs a biztonsági másolatot kapja, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="7e47b-154">A harmadik parancs hét nappal korábban kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="7e47b-155">A negyedik parancs a jelenlegi dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e47b-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="7e47b-156">Az ötödik parancs beolvassa az $StartDate és a $EndDate által szűrt adott biztonsági másolat helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="7e47b-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="7e47b-157">A hatodik parancs visszaállítja a lemezeket nem felügyelt lemezekként a VM eredeti tárterület-fiókjával.</span><span class="sxs-lookup"><span data-stu-id="7e47b-157">The sixth command restores the disks as unmanaged disks using the original storage account of the VM.</span></span>

## <span data-ttu-id="7e47b-158">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e47b-158">PARAMETERS</span></span>

### <span data-ttu-id="7e47b-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e47b-159">-DefaultProfile</span></span>

<span data-ttu-id="7e47b-160">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e47b-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-161">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="7e47b-161">-MultipleSourceFilePath</span></span>
<span data-ttu-id="7e47b-162">Több fájlból álló fájl-megosztásból való visszaállításra használható.</span><span class="sxs-lookup"><span data-stu-id="7e47b-162">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="7e47b-163">A visszaállítandó elemek elérési útja a fájlmegosztás alatt.</span><span class="sxs-lookup"><span data-stu-id="7e47b-163">The paths of the items to be restored within the file share.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-164">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7e47b-164">-RecoveryPoint</span></span>

<span data-ttu-id="7e47b-165">Annak a helyreállítási pontnak a meghatározása, amelyre vissza szeretné állítani a biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="7e47b-165">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="7e47b-166">Ha **AzureRmRecoveryServicesBackupRecoveryPoint** objektumot szeretne beolvasni, használja a **Get-AzRecoveryServicesBackupRecoveryPoint** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7e47b-166">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-167">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="7e47b-167">-ResolveConflict</span></span>

<span data-ttu-id="7e47b-168">Abban az esetben, ha a visszaállított elem a célhelyen is megtalálható, ezzel jelezheti, hogy felülírja-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="7e47b-168">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="7e47b-169">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7e47b-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e47b-170">Felülírja</span><span class="sxs-lookup"><span data-stu-id="7e47b-170">Overwrite</span></span>
- <span data-ttu-id="7e47b-171">Kihagyhatja</span><span class="sxs-lookup"><span data-stu-id="7e47b-171">Skip</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-172">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="7e47b-172">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="7e47b-173">A nem felügyelt lemezek visszaállításához használja ezt a kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="7e47b-173">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-174">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="7e47b-174">-RestoreDiskList</span></span>
<span data-ttu-id="7e47b-175">Adja meg, hogy mely lemezek legyenek helyreállítva a VM biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="7e47b-175">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-176">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="7e47b-176">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="7e47b-177">E kapcsoló segítségével csak a VM-re mentett operációs rendszerek merevlemezeit állíthatja vissza</span><span class="sxs-lookup"><span data-stu-id="7e47b-177">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-178">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="7e47b-178">-SourceFilePath</span></span>

<span data-ttu-id="7e47b-179">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="7e47b-179">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="7e47b-180">Annak az elemnek az elérési útvonala, amelyet a fájlmegosztás során vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="7e47b-180">The path of the item to be restored within the file share.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-181">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="7e47b-181">-SourceFileType</span></span>

<span data-ttu-id="7e47b-182">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="7e47b-182">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="7e47b-183">Annak a fájlnak a típusa, amelyet vissza szeretne állítani a megosztáson belül.</span><span class="sxs-lookup"><span data-stu-id="7e47b-183">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="7e47b-184">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7e47b-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7e47b-185">Fájl</span><span class="sxs-lookup"><span data-stu-id="7e47b-185">File</span></span>
- <span data-ttu-id="7e47b-186">Directory</span><span class="sxs-lookup"><span data-stu-id="7e47b-186">Directory</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-187">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7e47b-187">-StorageAccountName</span></span>

<span data-ttu-id="7e47b-188">Az előfizetésben a TARGET Storage fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e47b-188">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="7e47b-189">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="7e47b-189">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-190">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e47b-190">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="7e47b-191">Az előfizetésben a TARGET Storage-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e47b-191">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="7e47b-192">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="7e47b-192">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-193">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="7e47b-193">-TargetFileShareName</span></span>

<span data-ttu-id="7e47b-194">Annak a fájlnak a megosztása, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="7e47b-194">The File Share to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-195">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="7e47b-195">-TargetFolder</span></span>

<span data-ttu-id="7e47b-196">A mappa, amelyben a megosztást vissza kell állítani a TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="7e47b-196">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="7e47b-197">Ha a mentett tartalmat egy gyökérkönyvtárba szeretné visszaállítani, adja meg a cél mappa értékét üres karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="7e47b-197">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-198">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e47b-198">-TargetResourceGroupName</span></span>

<span data-ttu-id="7e47b-199">Az erőforráscsoport, amelyre a kezelt lemezek visszaállíthatók.</span><span class="sxs-lookup"><span data-stu-id="7e47b-199">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="7e47b-200">A VM biztonsági másolatának a kezelt lemezekkel való megadására vonatkozó lehetőség</span><span class="sxs-lookup"><span data-stu-id="7e47b-200">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-201">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7e47b-201">-TargetStorageAccountName</span></span>

<span data-ttu-id="7e47b-202">Az a tárolási fiók, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="7e47b-202">The storage account to which the file share has to be restored to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-203">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e47b-203">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="7e47b-204">Ezt a kapcsolót akkor használja, ha a helyreállítási pontból származó lemezeket vissza szeretné állítani az eredeti tárolási fiókjába.</span><span class="sxs-lookup"><span data-stu-id="7e47b-204">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-205">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7e47b-205">-VaultId</span></span>

<span data-ttu-id="7e47b-206">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="7e47b-206">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-207">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="7e47b-207">-VaultLocation</span></span>

<span data-ttu-id="7e47b-208">A helyreállítási szolgáltatások boltozatának helye.</span><span class="sxs-lookup"><span data-stu-id="7e47b-208">Location of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-209">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="7e47b-209">-WLRecoveryConfig</span></span>

<span data-ttu-id="7e47b-210">Helyreállítási konfiguráció</span><span class="sxs-lookup"><span data-stu-id="7e47b-210">Recovery config</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-211">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7e47b-211">-Confirm</span></span>

<span data-ttu-id="7e47b-212">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7e47b-212">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e47b-213">-WhatIf</span></span>

<span data-ttu-id="7e47b-214">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7e47b-214">Shows what would happen if the cmdlet runs.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e47b-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e47b-215">CommonParameters</span></span>
<span data-ttu-id="7e47b-216">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e47b-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e47b-217">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7e47b-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e47b-218">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e47b-218">INPUTS</span></span>

### <span data-ttu-id="7e47b-219">System. String</span><span class="sxs-lookup"><span data-stu-id="7e47b-219">System.String</span></span>

### <span data-ttu-id="7e47b-220">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="7e47b-220">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="7e47b-221">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e47b-221">OUTPUTS</span></span>

### <span data-ttu-id="7e47b-222">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="7e47b-222">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="7e47b-223">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e47b-223">NOTES</span></span>

## <span data-ttu-id="7e47b-224">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e47b-224">RELATED LINKS</span></span>

[<span data-ttu-id="7e47b-225">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7e47b-225">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="7e47b-226">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7e47b-226">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="7e47b-227">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7e47b-227">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
