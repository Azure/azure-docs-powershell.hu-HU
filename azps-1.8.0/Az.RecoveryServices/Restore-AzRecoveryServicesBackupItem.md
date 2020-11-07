---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: eb54d22f74216dc883726d34df204ce80c711a22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669621"
---
# <span data-ttu-id="c9f6b-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c9f6b-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="c9f6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f6b-103">Egy biztonsági elem adatainak és konfigurációjának visszaállítása a helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="c9f6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9f6b-104">SYNTAX</span></span>

### <span data-ttu-id="c9f6b-105">AzureVMParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9f6b-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f6b-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9f6b-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9f6b-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9f6b-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9f6b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9f6b-108">DESCRIPTION</span></span>
<span data-ttu-id="c9f6b-109">A **Restore-AzRecoveryServicesBackupItem** parancsmag visszaállítja az Azure Backup-elemek adatát és konfigurációját egy megadott helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="c9f6b-110">Ez a parancsmag a helyreállítási szolgáltatások boltozatról az ügyfél tárterületére való visszaállítást indítja el.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="c9f6b-111">A visszaállítási művelet nem állítja vissza a teljes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="c9f6b-112">Visszaállítja a lemez adatait és a konfigurációs információkat.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="c9f6b-113">A visszaállítási művelet befejeződése után létre kell hoznia a virtuális gépet, és el kell indítania.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="c9f6b-114">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-114">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c9f6b-115">Példák</span><span class="sxs-lookup"><span data-stu-id="c9f6b-115">EXAMPLES</span></span>

### <span data-ttu-id="c9f6b-116">1. példa: elem visszaállítása helyreállítási pontra</span><span class="sxs-lookup"><span data-stu-id="c9f6b-116">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="c9f6b-117">Az első parancs a AzureVM típusú biztonsági tárolót kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c9f6b-118">A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Containerból, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="c9f6b-119">A harmadik parancs hét nappal korábban kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="c9f6b-120">A negyedik parancs a jelenlegi dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="c9f6b-121">Az ötödik parancs beolvassa az $StartDate és a $EndDate által szűrt adott biztonsági másolat helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="c9f6b-122">Az itt megadott dátumtartomány az elmúlt 7 nap.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="c9f6b-123">Az utolsó parancs visszaállítja a lemezeket a TARGET Storage DestAccount a DestRG erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-123">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="c9f6b-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9f6b-124">PARAMETERS</span></span>

### <span data-ttu-id="c9f6b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f6b-125">-DefaultProfile</span></span>
<span data-ttu-id="c9f6b-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9f6b-127">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c9f6b-127">-RecoveryPoint</span></span>
<span data-ttu-id="c9f6b-128">Annak a helyreállítási pontnak a meghatározása, amelyre a virtuális gépet vissza szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-128">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="c9f6b-129">**AzureRmRecoveryServicesBackupRecoveryPoint** objektum beolvasásához használja az Get-AzRecoveryServicesBackupRecoveryPoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-129">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

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

### <span data-ttu-id="c9f6b-130">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="c9f6b-130">-ResolveConflict</span></span>
<span data-ttu-id="c9f6b-131">Abban az esetben, ha a visszaállított elem a célhelyen is megtalálható, ezzel jelezheti, hogy felülírja-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-131">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

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

### <span data-ttu-id="c9f6b-132">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="c9f6b-132">-SourceFilePath</span></span>
<span data-ttu-id="c9f6b-133">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-133">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="c9f6b-134">Annak az elemnek az elérési útvonala, amelyet a fájlmegosztás során vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-134">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="c9f6b-135">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="c9f6b-135">-SourceFileType</span></span>
<span data-ttu-id="c9f6b-136">A fájl-megosztásból egy adott elemre való visszaállításhoz használható.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-136">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="c9f6b-137">Annak az elemnek az elérési útvonala, amelyet a fájlmegosztás során vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-137">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="c9f6b-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c9f6b-138">-StorageAccountName</span></span>
<span data-ttu-id="c9f6b-139">Az előfizetésben a TARGET Storage fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-139">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="c9f6b-140">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-140">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="c9f6b-141">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f6b-141">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="c9f6b-142">Az előfizetésben a TARGET Storage-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-142">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="c9f6b-143">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-143">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="c9f6b-144">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="c9f6b-144">-TargetFileShareName</span></span>
<span data-ttu-id="c9f6b-145">Annak a fájlnak a megosztása, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-145">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="c9f6b-146">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="c9f6b-146">-TargetFolder</span></span>
<span data-ttu-id="c9f6b-147">A mappa, amelyben a megosztást vissza szeretné állítani a targetFileShareName. hagyja üresen az üres változót a root mappa alatti visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-147">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="c9f6b-148">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f6b-148">-TargetResourceGroupName</span></span>
<span data-ttu-id="c9f6b-149">Az erőforráscsoport, amelyre a kezelt lemezek visszaállíthatók.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-149">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="c9f6b-150">A VM biztonsági másolatának a kezelt lemezekkel való megadására vonatkozó lehetőség</span><span class="sxs-lookup"><span data-stu-id="c9f6b-150">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="c9f6b-151">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c9f6b-151">-TargetStorageAccountName</span></span>
<span data-ttu-id="c9f6b-152">Az a tárolási fiók, amelyre a fájl megosztását vissza kell állítani.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-152">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="c9f6b-153">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c9f6b-153">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="c9f6b-154">Ezt a kapcsolót akkor használja, ha a helyreállítási pontból származó lemezeket vissza szeretné állítani az eredeti tárolási fiókjába.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-154">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="c9f6b-155">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c9f6b-155">-VaultId</span></span>
<span data-ttu-id="c9f6b-156">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="c9f6b-156">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c9f6b-157">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="c9f6b-157">-VaultLocation</span></span>
<span data-ttu-id="c9f6b-158">A helyreállítási szolgáltatások boltozatának helye.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-158">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c9f6b-159">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="c9f6b-159">-WLRecoveryConfig</span></span>
<span data-ttu-id="c9f6b-160">Helyreállítási konfiguráció</span><span class="sxs-lookup"><span data-stu-id="c9f6b-160">Recovery config</span></span>

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

### <span data-ttu-id="c9f6b-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9f6b-161">-Confirm</span></span>
<span data-ttu-id="c9f6b-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f6b-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f6b-163">-WhatIf</span></span>
<span data-ttu-id="c9f6b-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9f6b-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9f6b-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f6b-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f6b-166">CommonParameters</span></span>
<span data-ttu-id="c9f6b-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9f6b-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f6b-168">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9f6b-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f6b-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9f6b-169">INPUTS</span></span>

### <span data-ttu-id="c9f6b-170">System. String</span><span class="sxs-lookup"><span data-stu-id="c9f6b-170">System.String</span></span>

### <span data-ttu-id="c9f6b-171">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="c9f6b-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="c9f6b-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9f6b-172">OUTPUTS</span></span>

### <span data-ttu-id="c9f6b-173">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="c9f6b-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c9f6b-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9f6b-174">NOTES</span></span>

## <span data-ttu-id="c9f6b-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9f6b-175">RELATED LINKS</span></span>

[<span data-ttu-id="c9f6b-176">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c9f6b-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="c9f6b-177">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c9f6b-177">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="c9f6b-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c9f6b-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)


