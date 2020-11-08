---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 7dbafdececffe1a5e96c2c39dfb6d63f05961622
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025082"
---
# <span data-ttu-id="170f7-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="170f7-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="170f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="170f7-102">SYNOPSIS</span></span>

<span data-ttu-id="170f7-103">Egy biztonsági elem adatainak és konfigurációjának visszaállítása a helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="170f7-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="170f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="170f7-104">SYNTAX</span></span>

### <span data-ttu-id="170f7-105">AzureVMParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="170f7-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170f7-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="170f7-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170f7-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="170f7-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="170f7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="170f7-108">DESCRIPTION</span></span>

<span data-ttu-id="170f7-109">A **Restore-AzRecoveryServicesBackupItem** parancsmag visszaállítja az Azure Backup-elemek adatát és konfigurációját egy megadott helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="170f7-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="170f7-110">Ez a parancsmag a helyreállítási szolgáltatások boltozatról az ügyfél tárterületére való visszaállítást indítja el.</span><span class="sxs-lookup"><span data-stu-id="170f7-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="170f7-111">A visszaállítási művelet nem állítja vissza a teljes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="170f7-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="170f7-112">Ha a visszaállítási művelet befejezése után visszaállítja a távtárolású lemezeket az ügyfél-tároló fiókba, létre kell hoznia a virtuális gépet, és el kell indítania.</span><span class="sxs-lookup"><span data-stu-id="170f7-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="170f7-113">További tudnivalókért tekintse át a refter és a paraméter szövegét.</span><span class="sxs-lookup"><span data-stu-id="170f7-113">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="170f7-114">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="170f7-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="170f7-115">Megjegyzés: a parancsmag sikeres végrehajtásához a-VaultId paraméter-VaultLocation paraméteren kívül is használni kell.</span><span class="sxs-lookup"><span data-stu-id="170f7-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="170f7-116">Példák</span><span class="sxs-lookup"><span data-stu-id="170f7-116">EXAMPLES</span></span>

### <span data-ttu-id="170f7-117">1. példa: elem visszaállítása helyreállítási pontra</span><span class="sxs-lookup"><span data-stu-id="170f7-117">Example 1: Restore an item to a recovery point</span></span>

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

<span data-ttu-id="170f7-118">Az első parancs a AzureVM típusú biztonsági tárolót kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="170f7-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="170f7-119">A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Containerból, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="170f7-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="170f7-120">A harmadik parancs hét nappal korábban kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="170f7-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="170f7-121">A negyedik parancs a jelenlegi dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="170f7-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="170f7-122">Az ötödik parancs beolvassa az $StartDate és a $EndDate által szűrt adott biztonsági másolat helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="170f7-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="170f7-123">Az itt megadott dátumtartomány az elmúlt 7 nap.</span><span class="sxs-lookup"><span data-stu-id="170f7-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="170f7-124">A hetedik parancs azt adja meg, hogy mely lemezek legyenek helyreállítva a helyreállítási pontból, és a $restoreDiskLUNs változóban legyenek tárolva.</span><span class="sxs-lookup"><span data-stu-id="170f7-124">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="170f7-125">Az utolsó parancs visszaállítja a lemezeket a TARGET Storage DestAccount a DestRG erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="170f7-125">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="170f7-126">2. példa: egy AzureFileShare-elem több fájljának visszaállítása</span><span class="sxs-lookup"><span data-stu-id="170f7-126">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="170f7-127">Az első parancs a AzureVM típusú biztonsági tárolót kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="170f7-127">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="170f7-128">A második parancs a fileshareitem nevű biztonsági másolatot kapja, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="170f7-128">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="170f7-129">A harmadik parancs beolvassa az adott biztonságimásolat-elem helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="170f7-129">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="170f7-130">A negyedik parancs spceifies, hogy mely fájlok legyenek visszaállíthatók és tárolva $files változóban.</span><span class="sxs-lookup"><span data-stu-id="170f7-130">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="170f7-131">Az utolsó parancs visszaállítja a megadott fájlokat az eredeti helyükre.</span><span class="sxs-lookup"><span data-stu-id="170f7-131">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="170f7-132">3. példa</span><span class="sxs-lookup"><span data-stu-id="170f7-132">Example 3</span></span>

<span data-ttu-id="170f7-133">Egy biztonsági elem adatainak és konfigurációjának visszaállítása a helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="170f7-133">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="170f7-134">autogenerated</span><span class="sxs-lookup"><span data-stu-id="170f7-134">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```

## <span data-ttu-id="170f7-135">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="170f7-135">PARAMETERS</span></span>

### <span data-ttu-id="170f7-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170f7-136">-DefaultProfile</span></span>

<span data-ttu-id="170f7-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="170f7-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="170f7-138">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="170f7-138">-MultipleSourceFilePath</span></span>
<span data-ttu-id="170f7-139">Több fájlból álló fájl-megosztásból való visszaállításra használható.</span><span class="sxs-lookup"><span data-stu-id="170f7-139">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="170f7-140">A visszaállítandó elemek elérési útja a fájlmegosztás alatt.</span><span class="sxs-lookup"><span data-stu-id="170f7-140">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="170f7-141">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="170f7-141">-RecoveryPoint</span></span>

<span data-ttu-id="170f7-142">Annak a helyreállítási pontnak a meghatározása, amelyre vissza szeretné állítani a biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="170f7-142">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="170f7-143">Ha **AzureRmRecoveryServicesBackupRecoveryPoint** objektumot szeretne beolvasni, használja a **Get-AzRecoveryServicesBackupRecoveryPoint** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="170f7-143">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="170f7-144">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="170f7-144">-ResolveConflict</span></span>

<span data-ttu-id="170f7-145">Abban az esetben, ha a visszaállított elem a célhelyen is megtalálható, ezzel jelezheti, hogy felülírja-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="170f7-145">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="170f7-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="170f7-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="170f7-147">Felülírja</span><span class="sxs-lookup"><span data-stu-id="170f7-147">Overwrite</span></span>
- <span data-ttu-id="170f7-148">Kihagyhatja</span><span class="sxs-lookup"><span data-stu-id="170f7-148">Skip</span></span>

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

### <span data-ttu-id="170f7-149">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="170f7-149">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="170f7-150">A nem felügyelt lemezek visszaállításához használja ezt a kapcsolót.</span><span class="sxs-lookup"><span data-stu-id="170f7-150">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="170f7-151">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="170f7-151">-RestoreDiskList</span></span>
<span data-ttu-id="170f7-152">Adja meg, hogy mely lemezek legyenek helyreállítva a VM biztonsági másolatból</span><span class="sxs-lookup"><span data-stu-id="170f7-152">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="170f7-153">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="170f7-153">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="170f7-154">E kapcsoló segítségével csak a VM-re mentett operációs rendszerek merevlemezeit állíthatja vissza</span><span class="sxs-lookup"><span data-stu-id="170f7-154">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="170f7-155">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="170f7-155">-SourceFilePath</span></span>

<span data-ttu-id="170f7-156">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="170f7-156">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="170f7-157">Annak az elemnek az elérési útvonala, amelyet a fájlmegosztás során vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="170f7-157">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="170f7-158">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="170f7-158">-SourceFileType</span></span>

<span data-ttu-id="170f7-159">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="170f7-159">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="170f7-160">Annak a fájlnak a típusa, amelyet vissza szeretne állítani a megosztáson belül.</span><span class="sxs-lookup"><span data-stu-id="170f7-160">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="170f7-161">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="170f7-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="170f7-162">Fájl</span><span class="sxs-lookup"><span data-stu-id="170f7-162">File</span></span>
- <span data-ttu-id="170f7-163">Directory</span><span class="sxs-lookup"><span data-stu-id="170f7-163">Directory</span></span>

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

### <span data-ttu-id="170f7-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="170f7-164">-StorageAccountName</span></span>

<span data-ttu-id="170f7-165">Az előfizetésben a TARGET Storage fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="170f7-165">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="170f7-166">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="170f7-166">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="170f7-167">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170f7-167">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="170f7-168">Az előfizetésben a TARGET Storage-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="170f7-168">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="170f7-169">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="170f7-169">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="170f7-170">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="170f7-170">-TargetFileShareName</span></span>

<span data-ttu-id="170f7-171">Annak a fájlnak a megosztása, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="170f7-171">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="170f7-172">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="170f7-172">-TargetFolder</span></span>

<span data-ttu-id="170f7-173">A mappa, amelyben a megosztást vissza kell állítani a TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="170f7-173">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="170f7-174">Ha a mentett tartalmat egy gyökérkönyvtárba szeretné visszaállítani, adja meg a cél mappa értékét üres karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="170f7-174">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="170f7-175">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170f7-175">-TargetResourceGroupName</span></span>

<span data-ttu-id="170f7-176">Az erőforráscsoport, amelyre a kezelt lemezek visszaállíthatók.</span><span class="sxs-lookup"><span data-stu-id="170f7-176">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="170f7-177">A VM biztonsági másolatának a kezelt lemezekkel való megadására vonatkozó lehetőség</span><span class="sxs-lookup"><span data-stu-id="170f7-177">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="170f7-178">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="170f7-178">-TargetStorageAccountName</span></span>

<span data-ttu-id="170f7-179">Az a tárolási fiók, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="170f7-179">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="170f7-180">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="170f7-180">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="170f7-181">Ezt a kapcsolót akkor használja, ha a helyreállítási pontból származó lemezeket vissza szeretné állítani az eredeti tárolási fiókjába.</span><span class="sxs-lookup"><span data-stu-id="170f7-181">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="170f7-182">-VaultId</span><span class="sxs-lookup"><span data-stu-id="170f7-182">-VaultId</span></span>

<span data-ttu-id="170f7-183">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="170f7-183">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="170f7-184">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="170f7-184">-VaultLocation</span></span>

<span data-ttu-id="170f7-185">A helyreállítási szolgáltatások boltozatának helye.</span><span class="sxs-lookup"><span data-stu-id="170f7-185">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="170f7-186">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="170f7-186">-WLRecoveryConfig</span></span>

<span data-ttu-id="170f7-187">Helyreállítási konfiguráció</span><span class="sxs-lookup"><span data-stu-id="170f7-187">Recovery config</span></span>

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

### <span data-ttu-id="170f7-188">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="170f7-188">-Confirm</span></span>

<span data-ttu-id="170f7-189">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="170f7-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="170f7-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="170f7-190">-WhatIf</span></span>

<span data-ttu-id="170f7-191">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="170f7-191">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="170f7-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170f7-192">CommonParameters</span></span>
<span data-ttu-id="170f7-193">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="170f7-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170f7-194">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="170f7-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170f7-195">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="170f7-195">INPUTS</span></span>

### <span data-ttu-id="170f7-196">System. String</span><span class="sxs-lookup"><span data-stu-id="170f7-196">System.String</span></span>

### <span data-ttu-id="170f7-197">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="170f7-197">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="170f7-198">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="170f7-198">OUTPUTS</span></span>

### <span data-ttu-id="170f7-199">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="170f7-199">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="170f7-200">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="170f7-200">NOTES</span></span>

## <span data-ttu-id="170f7-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="170f7-201">RELATED LINKS</span></span>

[<span data-ttu-id="170f7-202">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="170f7-202">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="170f7-203">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="170f7-203">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="170f7-204">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="170f7-204">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
