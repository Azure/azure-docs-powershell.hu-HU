---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: b454f77bc3ad00ddf604e13672d61a7445c44fed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491882"
---
# <span data-ttu-id="c9089-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c9089-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="c9089-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9089-102">SYNOPSIS</span></span>
<span data-ttu-id="c9089-103">Egy biztonsági elem adatainak és konfigurációjának visszaállítása a helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="c9089-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9089-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9089-104">SYNTAX</span></span>

### <span data-ttu-id="c9089-105">AzureVMParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9089-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9089-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9089-106">AzureFileParameterSet</span></span>
```
Restore-AzureRmRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 -ResolveConflict <RestoreFSResolveConfictOption> [-SourceFilePath <String>] [-SourceFileType <SourceFileType>]
 [-TargetStorageAccountName <String>] [-TargetFileShareName <String>] [-TargetFolder <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9089-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9089-107">DESCRIPTION</span></span>
<span data-ttu-id="c9089-108">A **Restore-AzureRmRecoveryServicesBackupItem** parancsmag visszaállítja az Azure Backup-elemek adatát és konfigurációját egy megadott helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="c9089-108">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="c9089-109">Ez a parancsmag a helyreállítási szolgáltatások boltozatról az ügyfél tárterületére való visszaállítást indítja el.</span><span class="sxs-lookup"><span data-stu-id="c9089-109">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="c9089-110">A visszaállítási művelet nem állítja vissza a teljes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="c9089-110">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="c9089-111">Visszaállítja a lemez adatait és a konfigurációs információkat.</span><span class="sxs-lookup"><span data-stu-id="c9089-111">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="c9089-112">A visszaállítási művelet befejeződése után létre kell hoznia a virtuális gépet, és el kell indítania.</span><span class="sxs-lookup"><span data-stu-id="c9089-112">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="c9089-113">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="c9089-113">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c9089-114">Példák</span><span class="sxs-lookup"><span data-stu-id="c9089-114">EXAMPLES</span></span>

### <span data-ttu-id="c9089-115">1. példa: elem visszaállítása helyreállítási pontra</span><span class="sxs-lookup"><span data-stu-id="c9089-115">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="c9089-116">Az első parancs a AzureVM típusú biztonsági tárolót kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c9089-116">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c9089-117">A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Containerból, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c9089-117">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="c9089-118">A harmadik parancs hét nappal korábban kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c9089-118">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="c9089-119">A negyedik parancs a jelenlegi dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c9089-119">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="c9089-120">Az ötödik parancs beolvassa az $StartDate és a $EndDate által szűrt adott biztonsági másolat helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="c9089-120">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="c9089-121">Az itt megadott dátumtartomány az elmúlt 7 nap.</span><span class="sxs-lookup"><span data-stu-id="c9089-121">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="c9089-122">Az utolsó parancs visszaállítja a lemezeket a TARGET Storage DestAccount a DestRG erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="c9089-122">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="c9089-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9089-123">PARAMETERS</span></span>

### <span data-ttu-id="c9089-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9089-124">-DefaultProfile</span></span>
<span data-ttu-id="c9089-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9089-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9089-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c9089-126">-RecoveryPoint</span></span>
<span data-ttu-id="c9089-127">Annak a helyreállítási pontnak a meghatározása, amelyre a virtuális gépet vissza szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="c9089-127">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="c9089-128">**AzureRmRecoveryServicesBackupRecoveryPoint** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupRecoveryPoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c9089-128">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9089-129">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="c9089-129">-ResolveConflict</span></span>
<span data-ttu-id="c9089-130">Abban az esetben, ha a visszaállított elem a célhelyen is megtalálható, ezzel jelezheti, hogy felülírja-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="c9089-130">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConfictOption
Parameter Sets: AzureFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9089-131">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="c9089-131">-SourceFilePath</span></span>
<span data-ttu-id="c9089-132">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="c9089-132">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="c9089-133">Annak az elemnek az elérési útvonala, amelyet a fájlmegosztás során vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c9089-133">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="c9089-134">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="c9089-134">-SourceFileType</span></span>
<span data-ttu-id="c9089-135">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="c9089-135">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="c9089-136">Annak az elemnek az elérési útvonala, amelyet a fájlmegosztás során vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c9089-136">The path of the item to be restored within the file share.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9089-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c9089-137">-StorageAccountName</span></span>
<span data-ttu-id="c9089-138">Az előfizetésben a TARGET Storage fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9089-138">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="c9089-139">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="c9089-139">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9089-140">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9089-140">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="c9089-141">Az előfizetésben a TARGET Storage-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9089-141">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="c9089-142">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="c9089-142">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9089-143">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="c9089-143">-TargetFileShareName</span></span>
<span data-ttu-id="c9089-144">Annak a fájlnak a megosztása, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c9089-144">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="c9089-145">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="c9089-145">-TargetFolder</span></span>
<span data-ttu-id="c9089-146">A mappa, amelyben a megosztást vissza szeretné állítani a targetFileShareName. hagyja üresen az üres változót a root mappa alatti visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="c9089-146">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="c9089-147">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9089-147">-TargetResourceGroupName</span></span>
<span data-ttu-id="c9089-148">Az erőforráscsoport, amelyre a kezelt lemezek visszaállíthatók.</span><span class="sxs-lookup"><span data-stu-id="c9089-148">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="c9089-149">A VM biztonsági másolatának a kezelt lemezekkel való megadására vonatkozó lehetőség</span><span class="sxs-lookup"><span data-stu-id="c9089-149">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="c9089-150">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c9089-150">-TargetStorageAccountName</span></span>
<span data-ttu-id="c9089-151">Az a tárolási fiók, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c9089-151">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="c9089-152">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9089-152">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="c9089-153">Ezt a kapcsolót akkor használja, ha a helyreállítási pontból származó lemezeket vissza szeretné állítani az eredeti tárolási fiókjába.</span><span class="sxs-lookup"><span data-stu-id="c9089-153">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="c9089-154">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c9089-154">-VaultId</span></span>
<span data-ttu-id="c9089-155">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="c9089-155">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c9089-156">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="c9089-156">-VaultLocation</span></span>
<span data-ttu-id="c9089-157">A helyreállítási szolgáltatások boltozatának helye.</span><span class="sxs-lookup"><span data-stu-id="c9089-157">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c9089-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9089-158">-Confirm</span></span>
<span data-ttu-id="c9089-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9089-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9089-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9089-160">-WhatIf</span></span>
<span data-ttu-id="c9089-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9089-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9089-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9089-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9089-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9089-163">CommonParameters</span></span>
<span data-ttu-id="c9089-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9089-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9089-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9089-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9089-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9089-166">INPUTS</span></span>

### <span data-ttu-id="c9089-167">System. String</span><span class="sxs-lookup"><span data-stu-id="c9089-167">System.String</span></span>
<span data-ttu-id="c9089-168">Paraméterek: VaultId (ByValue), VaultLocation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c9089-168">Parameters: VaultId (ByValue), VaultLocation (ByValue)</span></span>

### <span data-ttu-id="c9089-169">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="c9089-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="c9089-170">Paraméterek: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c9089-170">Parameters: RecoveryPoint (ByValue)</span></span>

## <span data-ttu-id="c9089-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9089-171">OUTPUTS</span></span>

### <span data-ttu-id="c9089-172">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="c9089-172">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c9089-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9089-173">NOTES</span></span>

## <span data-ttu-id="c9089-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9089-174">RELATED LINKS</span></span>

[<span data-ttu-id="c9089-175">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c9089-175">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="c9089-176">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c9089-176">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="c9089-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c9089-177">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


