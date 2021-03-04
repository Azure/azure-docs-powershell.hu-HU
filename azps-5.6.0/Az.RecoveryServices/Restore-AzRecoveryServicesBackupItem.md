---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 3d3cbb196a287e24837c0e7b0e61b16eaa06ce95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942306"
---
# <span data-ttu-id="ae2b3-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ae2b3-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="ae2b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae2b3-102">SYNOPSIS</span></span>

<span data-ttu-id="ae2b3-103">Visszaállítja egy biztonsági másolat adatait és konfigurációját a megadott helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="ae2b3-104">A szükséges paraméterek a biztonsági másolat típusától függően változnak.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="ae2b3-105">Ugyanez a parancs használható az Azure Virtuális gépek, az Azure Virtuális gépeken futó adatbázisok és az Azure-fájlmegosztások visszaállításához is.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="ae2b3-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ae2b3-106">SYNTAX</span></span>

### <span data-ttu-id="ae2b3-107">AzureVMParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae2b3-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2b3-108">AzureVMManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae2b3-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2b3-109">AzureVMRestoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="ae2b3-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2b3-110">AzureVMUnManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae2b3-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2b3-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae2b3-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae2b3-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae2b3-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae2b3-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ae2b3-113">DESCRIPTION</span></span>

<span data-ttu-id="ae2b3-114">A **Restore-AzRecoveryServicesBackupItem** parancsmag visszaállítja egy Azure biztonságimásolat-elem adatait és konfigurációját egy megadott helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="ae2b3-115">**Biztonsági másolat az Azure VM-ről**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="ae2b3-116">Ezzel a paranccsal biztonsági másolatot készíthet az Azure virtuális gépeiről, és visszaállíthatja a lemezeket (mind felügyelt, mind nem felügyelt).</span><span class="sxs-lookup"><span data-stu-id="ae2b3-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="ae2b3-117">A visszaállítási művelet nem visszaállítja a teljes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="ae2b3-118">Ha ez egy felügyelt lemezen lévő virtuális gép, meg kell adni egy célerőforrás-csoportot a visszaállított lemezeket tároló helyként.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="ae2b3-119">Ha a célerőforrás-csoport meg van adva, és a pillanatképek a biztonságimásolat-házirendben megadott erőforráscsoportban vannak, a visszaállítási művelet azonnal meg fog jelenni, és a lemezeket helyi pillanatképekből kell létrehozni, és célerőforrás-csoportban kell tartani.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="ae2b3-120">Arra is van lehetőség, hogy nem felügyelt lemezként állítsa vissza őket, de ez kihasználja az Azure helyreállítási szolgáltatások tárolóban lévő adatokat, és így sokkal lassabb lesz.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="ae2b3-121">A virtuális gép konfigurációja és a virtuális gépnek a visszaállított lemezből való létrehozásához használható telepítősablon letölti a megadott tárfiókba.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="ae2b3-122">Ha ez egy nem felügyelt lemezes VIRTUÁLIS GÉP, akkor a pillanatfelvételek a lemez eredeti tárfiókban és/vagy a helyreállítási szolgáltatások tárolóban vannak.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="ae2b3-123">Ha a felhasználó lehetőséget ad az Eredeti tárfiók használatára a visszaállításhoz, akkor azonnali visszaállítás is lehetséges.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="ae2b3-124">Ellenkező esetben a rendszer adatokat hoz létre az Azure Helyreállítási szolgáltatások tárolóból, és a lemezeket a megadott tárfiókban hozza létre a virtuális gép és a telepítési sablon konfigurációja mellett.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae2b3-125">Az Azure VM alapértelmezés szerint minden lemezről biztonsági másolatot készít.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="ae2b3-126">Az Enable-Backup parancs használata során szelektíven biztonsági másolatot készíthet a kapcsolódó lemezről a kivételLista vagy az InclusionList paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="ae2b3-127">A lemezeket szelektíven visszaállító lehetőség csak akkor érhető el, ha az egyikről szelektíven biztonsági másolat is van.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="ae2b3-128">További információért tanulmányozza a különböző lehetséges paraméterkészleteket és paraméterszövegeket.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="ae2b3-129">Ha a -VaultId paramétert használja, akkor a -VaultLocation paramétert is használnia kell.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="ae2b3-130">**Biztonsági másolat az Azure-fájlok megosztásáról**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-130">**For Azure File share backup**</span></span>

<span data-ttu-id="ae2b3-131">Visszaállíthat egy teljes fájlmegosztást vagy egy adott/több fájlt/mappát a megosztáson.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="ae2b3-132">Visszaállíthatja az eredeti helyet vagy egy másik helyet.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="ae2b3-133">**Azure Workloads esetén**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-133">**For Azure Workloads**</span></span>

<span data-ttu-id="ae2b3-134">Sql-DBs-fájlokat visszaállíthat az Azure-virtuális gépeken</span><span class="sxs-lookup"><span data-stu-id="ae2b3-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="ae2b3-135">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ae2b3-135">EXAMPLES</span></span>

### <span data-ttu-id="ae2b3-136">1. példa: Egy biztonsági másolatból származó, felügyelt lemezről származó Azure VM lemezének visszaállítása egy adott helyreállítási pontból</span><span class="sxs-lookup"><span data-stu-id="ae2b3-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="ae2b3-137">Az első parancs lekérte a Helyreállítási szolgáltatások tárolót, és egy $vault tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="ae2b3-138">A második parancs lekérte az AzureVM típusú biztonságimásolat-elemet (V2VM) a "V2VM" névvel, és tárolja azt a $BackupItem változóban.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="ae2b3-139">A harmadik parancs a hét nappal korábbi dátumot kapja meg, majd a $StartDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="ae2b3-140">A negyedik parancs megkapja az aktuális dátumot, majd a $EndDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="ae2b3-141">Az ötödik parancs az adott biztonságimásolat-elem helyreállítási pontjainak listáját kapja meg, $StartDate és $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="ae2b3-142">Az utolsó parancs visszaállítja az összes lemezt a célerőforrás-csoport Target_RG, majd a DestRG erőforráscsoport tárolófiókjában biztosítja a VM konfigurációs adatait és a telepítési sablont.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="ae2b3-143">2. példa: Egy biztonsági másolatból származó, felügyelt lemezről származó Azure VM adott lemezének visszaállítása egy adott helyreállítási pontból</span><span class="sxs-lookup"><span data-stu-id="ae2b3-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="ae2b3-144">Az első parancs lekérte a Helyreállítási szolgáltatások tárolót, és egy $vault tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="ae2b3-145">A második parancs lekérte az AzureVM típusú biztonságimásolat-elemet (V2VM) a "V2VM" névvel, és tárolja azt a $BackupItem változóban.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="ae2b3-146">A harmadik parancs a hét nappal korábbi dátumot kapja meg, majd a $StartDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="ae2b3-147">A negyedik parancs megkapja az aktuális dátumot, majd a $EndDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="ae2b3-148">Az ötödik parancs az adott biztonságimásolat-elem helyreállítási pontjainak listáját kapja meg, $StartDate és $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="ae2b3-149">A hatodik parancs a visszaállítandó lemezlistát tárolja a restoreDiskLUN változóban.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="ae2b3-150">Az utolsó parancs visszaállítja a megadott LUN-okat a célerőforrás-csoport Target_RG-jára, majd a DestRG erőforráscsoport tárfiókjában adja meg a VM konfigurációs adatait és a telepítési sablont.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="ae2b3-151">3. példa: Felügyelt virtuális gép lemezeinek visszaállítása nem felügyelt lemezként</span><span class="sxs-lookup"><span data-stu-id="ae2b3-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="ae2b3-152">Az első parancs lekérte a RecoveryServices tárolót, és egy $vault tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="ae2b3-153">A második parancs lekérte a biztonságimásolat-elemet, majd a $BackupItem tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="ae2b3-154">A harmadik parancs a hét nappal korábbi dátumot kapja meg, majd a $StartDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="ae2b3-155">A negyedik parancs megkapja az aktuális dátumot, majd a $EndDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="ae2b3-156">Az ötödik parancs az adott biztonságimásolat-elem helyreállítási pontjainak listáját kapja meg, $StartDate és $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="ae2b3-157">A hatodik parancs a lemezeket nemmanaged lemezként visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="ae2b3-158">4. példa: Nemmanaged VM visszaállítása nemmanaged Disksként az eredeti tárfiók használatával</span><span class="sxs-lookup"><span data-stu-id="ae2b3-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="ae2b3-159">Az első parancs lekérte a RecoveryServices tárolót, és egy $vault tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="ae2b3-160">A második parancs lekérte a biztonságimásolat-elemet, majd a $BackupItem tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="ae2b3-161">A harmadik parancs a hét nappal korábbi dátumot kapja meg, majd a $StartDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="ae2b3-162">A negyedik parancs megkapja az aktuális dátumot, majd a $EndDate tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="ae2b3-163">Az ötödik parancs az adott biztonságimásolat-elem helyreállítási pontjainak listáját kapja meg, $StartDate és $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="ae2b3-164">A hatodik parancs a lemezeket nemmanaged lemezként visszaállítja az eredeti tárhelyfiókjukba.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="ae2b3-165">5. példa: AzureFileShare-elem több fájlának visszaállítása</span><span class="sxs-lookup"><span data-stu-id="ae2b3-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="ae2b3-166">Az első parancs lekérte a Helyreállítási szolgáltatások tárolót, és egy $vault tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="ae2b3-167">A második parancs lekérte a fileshareitem nevű biztonságimásolat-elemet, majd a $BackupItem tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="ae2b3-168">A harmadik parancs lekérte az adott biztonságimásolat-elem helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="ae2b3-169">A negyedik parancs megadja, hogy mely fájlokat kell visszaállítani és egy $files tárolja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="ae2b3-170">Az utolsó parancs visszaállítja a megadott fájlokat az eredeti helyére.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="ae2b3-171">6. példa: SQL DB visszaállítása egy Azure VM-en belül egy másik cél VIRTUÁLIS GÉPre egy külön teljes helyreállítási pont számára</span><span class="sxs-lookup"><span data-stu-id="ae2b3-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### <span data-ttu-id="ae2b3-172">7. példa: SQL DB visszaállítása egy Azure VM-en belül egy másik cél VM-re egy napló-helyreállítási ponthoz</span><span class="sxs-lookup"><span data-stu-id="ae2b3-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

## <span data-ttu-id="ae2b3-173">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae2b3-173">PARAMETERS</span></span>

### <span data-ttu-id="ae2b3-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2b3-174">-DefaultProfile</span></span>

<span data-ttu-id="ae2b3-175">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae2b3-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="ae2b3-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="ae2b3-177">Több fájl visszaállítása fájlmegosztásból.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="ae2b3-178">A fájlmegosztáson belül visszaállítható elemek elérési útjai.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-178">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="ae2b3-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ae2b3-179">-RecoveryPoint</span></span>

<span data-ttu-id="ae2b3-180">Azt a helyreállítási pontot adja meg, amelybe vissza kell állítani a biztonságimásolat-elemet.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="ae2b3-181">**AzureRmRecoveryServicesBackupRecoveryPoint-objektum** beszerzéséhez használja a **Get-AzRecoveryServicesBackupRecoveryPoint** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="ae2b3-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="ae2b3-182">-ResolveConflict</span></span>

<span data-ttu-id="ae2b3-183">Abban az esetben, ha a visszaállított elem is létezik a célhelyen, ezzel a mezővel jelezheti, hogy felül kell-e írnia vagy sem.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="ae2b3-184">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="ae2b3-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae2b3-185">Felülírás</span><span class="sxs-lookup"><span data-stu-id="ae2b3-185">Overwrite</span></span>
- <span data-ttu-id="ae2b3-186">Kihagyás</span><span class="sxs-lookup"><span data-stu-id="ae2b3-186">Skip</span></span>

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

### <span data-ttu-id="ae2b3-187">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="ae2b3-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="ae2b3-188">Ezzel a kapcsolóval megadhatja, hogy a visszaállítás nem használt lemezként történt-e</span><span class="sxs-lookup"><span data-stu-id="ae2b3-188">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="ae2b3-189">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="ae2b3-189">-RestoreDiskList</span></span>
<span data-ttu-id="ae2b3-190">Adja meg, hogy mely lemezeket kell helyreállítani a biztonságiolt virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="ae2b3-190">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="ae2b3-191">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="ae2b3-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="ae2b3-192">Ezzel a kapcsolóval csak a biztonsági másolatokat tároló virtuális gép operációs rendszer lemezei állíthatók vissza</span><span class="sxs-lookup"><span data-stu-id="ae2b3-192">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="ae2b3-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="ae2b3-193">-SourceFilePath</span></span>

<span data-ttu-id="ae2b3-194">Egy adott elem fájlmegosztásból való visszaállításához használható.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="ae2b3-195">A fájlmegosztáson belül visszaállítani kívánt elem elérési útja.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-195">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="ae2b3-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="ae2b3-196">-SourceFileType</span></span>

<span data-ttu-id="ae2b3-197">Egy adott elem fájlmegosztásból való visszaállításához használható.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="ae2b3-198">A fájlmegosztáson belül visszaállítani kívánt elem típusa.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="ae2b3-199">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="ae2b3-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae2b3-200">Fájl</span><span class="sxs-lookup"><span data-stu-id="ae2b3-200">File</span></span>
- <span data-ttu-id="ae2b3-201">Címtár</span><span class="sxs-lookup"><span data-stu-id="ae2b3-201">Directory</span></span>

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

### <span data-ttu-id="ae2b3-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ae2b3-202">-StorageAccountName</span></span>

<span data-ttu-id="ae2b3-203">Az előfizetésben a célként megadott tárfiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="ae2b3-204">A visszaállítási folyamat részeként ez a parancsmag ebben a Tárfiókban tárolja a lemezeket és a konfigurációs adatokat.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="ae2b3-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae2b3-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="ae2b3-206">Annak az erőforráscsoportnak a neve, amely az előfizetésben a céltárfiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="ae2b3-207">A visszaállítási folyamat részeként ez a parancsmag ebben a Tárfiókban tárolja a lemezeket és a konfigurációs adatokat.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="ae2b3-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="ae2b3-208">-TargetFileShareName</span></span>

<span data-ttu-id="ae2b3-209">Az a fájlmegosztás, amelyre a fájlmegosztást vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-209">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="ae2b3-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="ae2b3-210">-TargetFolder</span></span>

<span data-ttu-id="ae2b3-211">Az a mappa, amelyben a fájlmegosztást vissza kell állítani a TargetFileShareName fájlon belül.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="ae2b3-212">Ha a biztonsági másolat tartalmát vissza kell állítani egy gyökérmappába, a célmappa értékeit adja meg üres karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="ae2b3-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae2b3-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="ae2b3-214">Az erőforráscsoport, amelybe a felügyelt lemezeket visszaállítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ae2b3-215">Virtuális gép felügyelt lemezekkel való biztonsági mentésére alkalmazható</span><span class="sxs-lookup"><span data-stu-id="ae2b3-215">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="ae2b3-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ae2b3-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="ae2b3-217">Az a tárfiók, amelybe vissza kell állítani a fájlmegosztást.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-217">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="ae2b3-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae2b3-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="ae2b3-219">Akkor használja ezt a kapcsolót, ha a helyreállítási pontról származó lemezeket vissza kell állítani az eredeti tárhelyfiókjukba.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="ae2b3-220">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="ae2b3-220">-DiskEncryptionSetId</span></span> 

<span data-ttu-id="ae2b3-221">A visszaállított lemezeket titkosító DES-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-221">The DES ID to encrypt the restored disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMManagedDiskParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b3-222">-RestoreToSecondaryRegion</span><span class="sxs-lookup"><span data-stu-id="ae2b3-222">-RestoreToSecondaryRegion</span></span>

<span data-ttu-id="ae2b3-223">Ezzel a kapcsolóval elindíthatja a régióközi visszaállítást a másodlagos régióra.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-223">Use this switch to trigger the Cross region restore to secondary region.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIaasVM
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae2b3-224">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ae2b3-224">-VaultId</span></span>

<span data-ttu-id="ae2b3-225">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-225">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ae2b3-226">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="ae2b3-226">-VaultLocation</span></span>

<span data-ttu-id="ae2b3-227">A helyreállítási szolgáltatások tárolója.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-227">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ae2b3-228">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="ae2b3-228">-WLRecoveryConfig</span></span>

<span data-ttu-id="ae2b3-229">Helyreállítási konfigurációs</span><span class="sxs-lookup"><span data-stu-id="ae2b3-229">Recovery config</span></span>

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

### <span data-ttu-id="ae2b3-230">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae2b3-230">-Confirm</span></span>

<span data-ttu-id="ae2b3-231">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-231">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae2b3-232">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae2b3-232">-WhatIf</span></span>

<span data-ttu-id="ae2b3-233">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-233">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="ae2b3-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2b3-234">CommonParameters</span></span>
<span data-ttu-id="ae2b3-235">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2b3-236">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae2b3-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2b3-237">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae2b3-237">INPUTS</span></span>

### <span data-ttu-id="ae2b3-238">System.String</span><span class="sxs-lookup"><span data-stu-id="ae2b3-238">System.String</span></span>

### <span data-ttu-id="ae2b3-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="ae2b3-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="ae2b3-240">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae2b3-240">OUTPUTS</span></span>

### <span data-ttu-id="ae2b3-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="ae2b3-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ae2b3-242">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ae2b3-242">NOTES</span></span>

## <span data-ttu-id="ae2b3-243">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae2b3-243">RELATED LINKS</span></span>

[<span data-ttu-id="ae2b3-244">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ae2b3-244">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="ae2b3-245">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ae2b3-245">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="ae2b3-246">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ae2b3-246">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
