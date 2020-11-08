---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 69b115fab623d1a951fa2f77632a33fb437a3555
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013533"
---
# <span data-ttu-id="b4068-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b4068-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="b4068-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4068-102">SYNOPSIS</span></span>

<span data-ttu-id="b4068-103">Egy biztonsági elem adatainak és konfigurációjának visszaállítása a helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="b4068-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="b4068-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4068-104">SYNTAX</span></span>

### <span data-ttu-id="b4068-105">AzureVMParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4068-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4068-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4068-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4068-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4068-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4068-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4068-108">DESCRIPTION</span></span>

<span data-ttu-id="b4068-109">A **Restore-AzRecoveryServicesBackupItem** parancsmag visszaállítja az Azure Backup-elemek adatát és konfigurációját egy megadott helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="b4068-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="b4068-110">Ez a parancsmag a helyreállítási szolgáltatások boltozatról az ügyfél tárterületére való visszaállítást indítja el.</span><span class="sxs-lookup"><span data-stu-id="b4068-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="b4068-111">A visszaállítási művelet nem állítja vissza a teljes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="b4068-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="b4068-112">Ha a visszaállítási művelet befejezése után visszaállítja a távtárolású lemezeket az ügyfél-tároló fiókba, létre kell hoznia a virtuális gépet, és el kell indítania.</span><span class="sxs-lookup"><span data-stu-id="b4068-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="b4068-113">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="b4068-113">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="b4068-114">Megjegyzés: a parancsmag sikeres végrehajtásához a-VaultId paraméter-VaultLocation paraméteren kívül is használni kell.</span><span class="sxs-lookup"><span data-stu-id="b4068-114">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="b4068-115">Példák</span><span class="sxs-lookup"><span data-stu-id="b4068-115">EXAMPLES</span></span>

### <span data-ttu-id="b4068-116">1. példa: elem visszaállítása helyreállítási pontra</span><span class="sxs-lookup"><span data-stu-id="b4068-116">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetRG $ManagedDiskRG -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="b4068-117">Az első parancs a AzureVM típusú biztonsági tárolót kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b4068-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="b4068-118">A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Containerból, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b4068-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="b4068-119">A harmadik parancs hét nappal korábban kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b4068-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="b4068-120">A negyedik parancs a jelenlegi dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b4068-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="b4068-121">Az ötödik parancs beolvassa az $StartDate és a $EndDate által szűrt adott biztonsági másolat helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="b4068-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="b4068-122">Az itt megadott dátumtartomány az elmúlt 7 nap.</span><span class="sxs-lookup"><span data-stu-id="b4068-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="b4068-123">A hetedik parancs azt adja meg, hogy mely lemezek legyenek helyreállítva a helyreállítási pontból, és a $restoreDiskLUNs változóban legyenek tárolva.</span><span class="sxs-lookup"><span data-stu-id="b4068-123">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="b4068-124">Az utolsó parancs visszaállítja a lemezeket a TARGET Storage DestAccount a DestRG erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="b4068-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="b4068-125">2. példa: egy AzureFileShare-elem több fájljának visszaállítása</span><span class="sxs-lookup"><span data-stu-id="b4068-125">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="b4068-126">Az első parancs a AzureVM típusú biztonsági tárolót kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b4068-126">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="b4068-127">A második parancs a fileshareitem nevű biztonsági másolatot kapja, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b4068-127">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="b4068-128">A harmadik parancs beolvassa az adott biztonságimásolat-elem helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="b4068-128">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="b4068-129">A negyedik parancs spceifies, hogy mely fájlok legyenek visszaállíthatók és tárolva $files változóban.</span><span class="sxs-lookup"><span data-stu-id="b4068-129">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="b4068-130">Az utolsó parancs visszaállítja a megadott fájlokat az eredeti helyükre.</span><span class="sxs-lookup"><span data-stu-id="b4068-130">The last command restores the specified files to its original location.</span></span>

## <span data-ttu-id="b4068-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4068-131">PARAMETERS</span></span>

### <span data-ttu-id="b4068-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4068-132">-DefaultProfile</span></span>

<span data-ttu-id="b4068-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4068-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4068-134">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="b4068-134">-MultipleSourceFilePath</span></span>
<span data-ttu-id="b4068-135">Több fájlból álló fájl-megosztásból való visszaállításra használható.</span><span class="sxs-lookup"><span data-stu-id="b4068-135">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="b4068-136">A visszaállítandó elemek elérési útja a fájlmegosztás alatt.</span><span class="sxs-lookup"><span data-stu-id="b4068-136">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="b4068-137">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b4068-137">-RecoveryPoint</span></span>

<span data-ttu-id="b4068-138">Annak a helyreállítási pontnak a meghatározása, amelyre a virtuális gépet vissza szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="b4068-138">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="b4068-139">Ha **AzureRmRecoveryServicesBackupRecoveryPoint** objektumot szeretne beolvasni, használja a **Get-AzRecoveryServicesBackupRecoveryPoint** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b4068-139">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4068-140">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="b4068-140">-ResolveConflict</span></span>

<span data-ttu-id="b4068-141">Abban az esetben, ha a visszaállított elem a célhelyen is megtalálható, ezzel jelezheti, hogy felülírja-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="b4068-141">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="b4068-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b4068-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4068-143">Felülírja</span><span class="sxs-lookup"><span data-stu-id="b4068-143">Overwrite</span></span>
- <span data-ttu-id="b4068-144">Kihagyhatja</span><span class="sxs-lookup"><span data-stu-id="b4068-144">Skip</span></span>

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

### <span data-ttu-id="b4068-145">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="b4068-145">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="b4068-146">A nem felügyelt lemezek visszaállításához használja ezt a kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="b4068-146">Use this switch to specify to restore as unmanaged disks</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4068-147">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="b4068-147">-RestoreDiskList</span></span>
<span data-ttu-id="b4068-148">Adja meg, hogy mely lemezek legyenek helyreállítva a VM biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="b4068-148">Specify which disks to recover of the backed up VM</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4068-149">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="b4068-149">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="b4068-150">E kapcsoló segítségével csak a VM-re mentett operációs rendszerek merevlemezeit állíthatja vissza</span><span class="sxs-lookup"><span data-stu-id="b4068-150">Use this switch to restore only OS disks of a backed up VM</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4068-151">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="b4068-151">-SourceFilePath</span></span>

<span data-ttu-id="b4068-152">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="b4068-152">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="b4068-153">Annak az elemnek az elérési útvonala, amelyet a fájlmegosztás során vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="b4068-153">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="b4068-154">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="b4068-154">-SourceFileType</span></span>

<span data-ttu-id="b4068-155">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="b4068-155">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="b4068-156">Annak a fájlnak a típusa, amelyet vissza szeretne állítani a megosztáson belül.</span><span class="sxs-lookup"><span data-stu-id="b4068-156">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="b4068-157">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b4068-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4068-158">Fájl</span><span class="sxs-lookup"><span data-stu-id="b4068-158">File</span></span>
- <span data-ttu-id="b4068-159">Directory</span><span class="sxs-lookup"><span data-stu-id="b4068-159">Directory</span></span>

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

### <span data-ttu-id="b4068-160">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4068-160">-StorageAccountName</span></span>

<span data-ttu-id="b4068-161">Az előfizetésben a TARGET Storage fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4068-161">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="b4068-162">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="b4068-162">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4068-163">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4068-163">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="b4068-164">Az előfizetésben a TARGET Storage-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4068-164">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="b4068-165">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="b4068-165">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4068-166">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="b4068-166">-TargetFileShareName</span></span>

<span data-ttu-id="b4068-167">Annak a fájlnak a megosztása, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="b4068-167">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="b4068-168">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="b4068-168">-TargetFolder</span></span>

<span data-ttu-id="b4068-169">A mappa, amelyben a megosztást vissza kell állítani a TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="b4068-169">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="b4068-170">Ha a mentett tartalmat egy gyökérkönyvtárba szeretné visszaállítani, adja meg a cél mappa értékét üres karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="b4068-170">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="b4068-171">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4068-171">-TargetResourceGroupName</span></span>

<span data-ttu-id="b4068-172">Az erőforráscsoport, amelyre a kezelt lemezek visszaállíthatók.</span><span class="sxs-lookup"><span data-stu-id="b4068-172">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="b4068-173">A VM biztonsági másolatának a kezelt lemezekkel való megadására vonatkozó lehetőség</span><span class="sxs-lookup"><span data-stu-id="b4068-173">Applicable to backup of VM with managed disks</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4068-174">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4068-174">-TargetStorageAccountName</span></span>

<span data-ttu-id="b4068-175">Az a tárolási fiók, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="b4068-175">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="b4068-176">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4068-176">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="b4068-177">Ezt a kapcsolót akkor használja, ha a helyreállítási pontból származó lemezeket vissza szeretné állítani az eredeti tárolási fiókjába.</span><span class="sxs-lookup"><span data-stu-id="b4068-177">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4068-178">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b4068-178">-VaultId</span></span>

<span data-ttu-id="b4068-179">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="b4068-179">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b4068-180">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="b4068-180">-VaultLocation</span></span>

<span data-ttu-id="b4068-181">A helyreállítási szolgáltatások boltozatának helye.</span><span class="sxs-lookup"><span data-stu-id="b4068-181">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b4068-182">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="b4068-182">-WLRecoveryConfig</span></span>

<span data-ttu-id="b4068-183">Helyreállítási konfiguráció</span><span class="sxs-lookup"><span data-stu-id="b4068-183">Recovery config</span></span>

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

### <span data-ttu-id="b4068-184">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4068-184">-Confirm</span></span>

<span data-ttu-id="b4068-185">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4068-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4068-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4068-186">-WhatIf</span></span>

<span data-ttu-id="b4068-187">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4068-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4068-188">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4068-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4068-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4068-189">CommonParameters</span></span>
<span data-ttu-id="b4068-190">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4068-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4068-191">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4068-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4068-192">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4068-192">INPUTS</span></span>

### <span data-ttu-id="b4068-193">System. String</span><span class="sxs-lookup"><span data-stu-id="b4068-193">System.String</span></span>

### <span data-ttu-id="b4068-194">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="b4068-194">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="b4068-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4068-195">OUTPUTS</span></span>

### <span data-ttu-id="b4068-196">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="b4068-196">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b4068-197">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4068-197">NOTES</span></span>

## <span data-ttu-id="b4068-198">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4068-198">RELATED LINKS</span></span>

[<span data-ttu-id="b4068-199">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b4068-199">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b4068-200">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b4068-200">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b4068-201">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b4068-201">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
