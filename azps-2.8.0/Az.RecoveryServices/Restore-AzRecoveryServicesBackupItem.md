---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 87051d6e8c5dabe5a5e5c5138e06eda0de961219
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838540"
---
# <span data-ttu-id="504bc-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="504bc-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="504bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="504bc-102">SYNOPSIS</span></span>

<span data-ttu-id="504bc-103">Egy biztonsági elem adatainak és konfigurációjának visszaállítása a helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="504bc-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="504bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="504bc-104">SYNTAX</span></span>

### <span data-ttu-id="504bc-105">AzureVMParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="504bc-105">AzureVMParameterSet (Default)</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="504bc-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="504bc-106">AzureFileParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="504bc-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="504bc-107">AzureWorkloadParameterSet</span></span>

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="504bc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="504bc-108">DESCRIPTION</span></span>

<span data-ttu-id="504bc-109">A **Restore-AzRecoveryServicesBackupItem** parancsmag visszaállítja az Azure Backup-elemek adatát és konfigurációját egy megadott helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="504bc-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="504bc-110">Ez a parancsmag a helyreállítási szolgáltatások boltozatról az ügyfél tárterületére való visszaállítást indítja el.</span><span class="sxs-lookup"><span data-stu-id="504bc-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="504bc-111">A visszaállítási művelet nem állítja vissza a teljes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="504bc-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="504bc-112">Visszaállítja a lemez adatait és a konfigurációs információkat.</span><span class="sxs-lookup"><span data-stu-id="504bc-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="504bc-113">A visszaállítási művelet befejeződése után létre kell hoznia a virtuális gépet, és el kell indítania.</span><span class="sxs-lookup"><span data-stu-id="504bc-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="504bc-114">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="504bc-114">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="504bc-115">Megjegyzés: a parancsmag sikeres végrehajtásához a-VaultId paraméter-VaultLocation paraméteren kívül is használni kell.</span><span class="sxs-lookup"><span data-stu-id="504bc-115">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="504bc-116">Példák</span><span class="sxs-lookup"><span data-stu-id="504bc-116">EXAMPLES</span></span>

### <span data-ttu-id="504bc-117">1. példa: elem visszaállítása helyreállítási pontra</span><span class="sxs-lookup"><span data-stu-id="504bc-117">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="504bc-118">Az első parancs a AzureVM típusú biztonsági tárolót kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="504bc-118">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="504bc-119">A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Containerból, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="504bc-119">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="504bc-120">A harmadik parancs hét nappal korábban kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="504bc-120">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="504bc-121">A negyedik parancs a jelenlegi dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="504bc-121">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="504bc-122">Az ötödik parancs beolvassa az $StartDate és a $EndDate által szűrt adott biztonsági másolat helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="504bc-122">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="504bc-123">Az itt megadott dátumtartomány az elmúlt 7 nap.</span><span class="sxs-lookup"><span data-stu-id="504bc-123">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="504bc-124">Az utolsó parancs visszaállítja a lemezeket a TARGET Storage DestAccount a DestRG erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="504bc-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="504bc-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="504bc-125">PARAMETERS</span></span>

### <span data-ttu-id="504bc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="504bc-126">-DefaultProfile</span></span>

<span data-ttu-id="504bc-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="504bc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="504bc-128">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="504bc-128">-RecoveryPoint</span></span>

<span data-ttu-id="504bc-129">Annak a helyreállítási pontnak a meghatározása, amelyre a virtuális gépet vissza szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="504bc-129">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="504bc-130">Ha **AzureRmRecoveryServicesBackupRecoveryPoint** objektumot szeretne beolvasni, használja a **Get-AzRecoveryServicesBackupRecoveryPoint** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="504bc-130">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="504bc-131">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="504bc-131">-ResolveConflict</span></span>

<span data-ttu-id="504bc-132">Abban az esetben, ha a visszaállított elem a célhelyen is megtalálható, ezzel jelezheti, hogy felülírja-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="504bc-132">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="504bc-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="504bc-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="504bc-134">Felülírja</span><span class="sxs-lookup"><span data-stu-id="504bc-134">Overwrite</span></span>
- <span data-ttu-id="504bc-135">Kihagyhatja</span><span class="sxs-lookup"><span data-stu-id="504bc-135">Skip</span></span>

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

### <span data-ttu-id="504bc-136">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="504bc-136">-SourceFilePath</span></span>

<span data-ttu-id="504bc-137">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="504bc-137">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="504bc-138">Annak az elemnek az elérési útvonala, amelyet a fájlmegosztás során vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="504bc-138">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="504bc-139">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="504bc-139">-SourceFileType</span></span>

<span data-ttu-id="504bc-140">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="504bc-140">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="504bc-141">Annak a fájlnak a típusa, amelyet vissza szeretne állítani a megosztáson belül.</span><span class="sxs-lookup"><span data-stu-id="504bc-141">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="504bc-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="504bc-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="504bc-143">Fájl</span><span class="sxs-lookup"><span data-stu-id="504bc-143">File</span></span>
- <span data-ttu-id="504bc-144">Directory</span><span class="sxs-lookup"><span data-stu-id="504bc-144">Directory</span></span>

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

### <span data-ttu-id="504bc-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="504bc-145">-StorageAccountName</span></span>

<span data-ttu-id="504bc-146">Az előfizetésben a TARGET Storage fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="504bc-146">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="504bc-147">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="504bc-147">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="504bc-148">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="504bc-148">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="504bc-149">Az előfizetésben a TARGET Storage-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="504bc-149">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="504bc-150">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="504bc-150">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="504bc-151">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="504bc-151">-TargetFileShareName</span></span>

<span data-ttu-id="504bc-152">Annak a fájlnak a megosztása, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="504bc-152">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="504bc-153">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="504bc-153">-TargetFolder</span></span>

<span data-ttu-id="504bc-154">A mappa, amelyben a megosztást vissza kell állítani a TargetFileShareName.</span><span class="sxs-lookup"><span data-stu-id="504bc-154">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="504bc-155">Ha a mentett tartalmat egy gyökérkönyvtárba szeretné visszaállítani, adja meg a cél mappa értékét üres karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="504bc-155">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="504bc-156">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="504bc-156">-TargetResourceGroupName</span></span>

<span data-ttu-id="504bc-157">Az erőforráscsoport, amelyre a kezelt lemezek visszaállíthatók.</span><span class="sxs-lookup"><span data-stu-id="504bc-157">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="504bc-158">A VM biztonsági másolatának a kezelt lemezekkel való megadására vonatkozó lehetőség</span><span class="sxs-lookup"><span data-stu-id="504bc-158">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="504bc-159">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="504bc-159">-TargetStorageAccountName</span></span>

<span data-ttu-id="504bc-160">Az a tárolási fiók, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="504bc-160">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="504bc-161">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="504bc-161">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="504bc-162">Ezt a kapcsolót akkor használja, ha a helyreállítási pontból származó lemezeket vissza szeretné állítani az eredeti tárolási fiókjába.</span><span class="sxs-lookup"><span data-stu-id="504bc-162">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="504bc-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="504bc-163">-VaultId</span></span>

<span data-ttu-id="504bc-164">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="504bc-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="504bc-165">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="504bc-165">-VaultLocation</span></span>

<span data-ttu-id="504bc-166">A helyreállítási szolgáltatások boltozatának helye.</span><span class="sxs-lookup"><span data-stu-id="504bc-166">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="504bc-167">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="504bc-167">-WLRecoveryConfig</span></span>

<span data-ttu-id="504bc-168">Helyreállítási konfiguráció</span><span class="sxs-lookup"><span data-stu-id="504bc-168">Recovery config</span></span>

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

### <span data-ttu-id="504bc-169">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="504bc-169">-Confirm</span></span>

<span data-ttu-id="504bc-170">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="504bc-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="504bc-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="504bc-171">-WhatIf</span></span>

<span data-ttu-id="504bc-172">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="504bc-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="504bc-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="504bc-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="504bc-174">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="504bc-174">-CommonParameters</span></span>

<span data-ttu-id="504bc-175">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="504bc-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="504bc-176">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="504bc-176">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="504bc-177">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="504bc-177">INPUTS</span></span>

### <span data-ttu-id="504bc-178">System. String</span><span class="sxs-lookup"><span data-stu-id="504bc-178">System.String</span></span>

### <span data-ttu-id="504bc-179">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="504bc-179">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="504bc-180">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="504bc-180">OUTPUTS</span></span>

### <span data-ttu-id="504bc-181">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="504bc-181">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="504bc-182">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="504bc-182">NOTES</span></span>

## <span data-ttu-id="504bc-183">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="504bc-183">RELATED LINKS</span></span>

[<span data-ttu-id="504bc-184">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="504bc-184">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="504bc-185">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="504bc-185">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="504bc-186">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="504bc-186">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
