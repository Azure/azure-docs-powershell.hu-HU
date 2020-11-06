---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/restore-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 6013531367f5996924da1776c0062ebb5ad02b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493060"
---
# <span data-ttu-id="e2126-101">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e2126-101">Restore-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="e2126-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2126-102">SYNOPSIS</span></span>
<span data-ttu-id="e2126-103">Egy biztonsági elem adatainak és konfigurációjának visszaállítása a helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="e2126-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2126-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2126-104">SYNTAX</span></span>

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2126-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2126-105">DESCRIPTION</span></span>
<span data-ttu-id="e2126-106">A **Restore-AzureRmRecoveryServicesBackupItem** parancsmag visszaállítja az Azure Backup-elemek adatát és konfigurációját egy megadott helyreállítási pontra.</span><span class="sxs-lookup"><span data-stu-id="e2126-106">The **Restore-AzureRmRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="e2126-107">Ez a parancsmag a helyreállítási szolgáltatások boltozatról az ügyfél tárterületére való visszaállítást indítja el.</span><span class="sxs-lookup"><span data-stu-id="e2126-107">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>

<span data-ttu-id="e2126-108">A visszaállítási művelet nem állítja vissza a teljes virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="e2126-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="e2126-109">Visszaállítja a lemez adatait és a konfigurációs információkat.</span><span class="sxs-lookup"><span data-stu-id="e2126-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="e2126-110">A visszaállítási művelet befejeződése után létre kell hoznia a virtuális gépet, és el kell indítania.</span><span class="sxs-lookup"><span data-stu-id="e2126-110">After the restore operation is finished, you must create the virtual machine and start it.</span></span>

<span data-ttu-id="e2126-111">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="e2126-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e2126-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e2126-112">EXAMPLES</span></span>

### <span data-ttu-id="e2126-113">1. példa: elem visszaállítása helyreállítási pontra</span><span class="sxs-lookup"><span data-stu-id="e2126-113">Example 1: Restore an item to a recovery point</span></span>
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

<span data-ttu-id="e2126-114">Az első parancs a AzureVM típusú biztonsági tárolót kapja, majd a $Container változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2126-114">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="e2126-115">A második parancs beolvassa a V2VM nevű biztonsági másolatot a $Containerból, majd a $BackupItem változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2126-115">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="e2126-116">A harmadik parancs hét nappal korábban kapja meg a dátumot, majd a $StartDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2126-116">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="e2126-117">A negyedik parancs a jelenlegi dátumot kapja, majd a $EndDate változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e2126-117">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="e2126-118">Az ötödik parancs beolvassa az $StartDate és a $EndDate által szűrt adott biztonsági másolat helyreállítási pontjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="e2126-118">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="e2126-119">Az itt megadott dátumtartomány az elmúlt 7 nap.</span><span class="sxs-lookup"><span data-stu-id="e2126-119">The date range specified is the last 7 days.</span></span>

<span data-ttu-id="e2126-120">Az utolsó parancs visszaállítja a lemezeket a TARGET Storage DestAccount a DestRG erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="e2126-120">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="e2126-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2126-121">PARAMETERS</span></span>

### <span data-ttu-id="e2126-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2126-122">-DefaultProfile</span></span>
<span data-ttu-id="e2126-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2126-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2126-124">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e2126-124">-RecoveryPoint</span></span>
<span data-ttu-id="e2126-125">Annak a helyreállítási pontnak a meghatározása, amelyre a virtuális gépet vissza szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="e2126-125">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="e2126-126">**AzureRmRecoveryServicesBackupRecoveryPoint** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupRecoveryPoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e2126-126">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzureRmRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2126-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e2126-127">-StorageAccountName</span></span>
<span data-ttu-id="e2126-128">Az előfizetésben a TARGET Storage fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2126-128">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="e2126-129">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="e2126-129">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2126-130">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2126-130">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="e2126-131">Az előfizetésben a TARGET Storage-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2126-131">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="e2126-132">A visszaállítási folyamat részeként ez a parancsmag tárolja a lemezeket és a konfigurációs információkat ebben a tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="e2126-132">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2126-133">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e2126-133">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="e2126-134">Ezt a kapcsolót akkor használja, ha a helyreállítási pontból származó lemezeket vissza szeretné állítani az eredeti tárolási fiókjába.</span><span class="sxs-lookup"><span data-stu-id="e2126-134">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2126-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2126-135">-Confirm</span></span>
<span data-ttu-id="e2126-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2126-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2126-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2126-137">-WhatIf</span></span>
<span data-ttu-id="e2126-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2126-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2126-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2126-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2126-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2126-140">CommonParameters</span></span>
<span data-ttu-id="e2126-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2126-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2126-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2126-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2126-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2126-143">INPUTS</span></span>

### <span data-ttu-id="e2126-144">RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="e2126-144">RecoveryPointBase</span></span>
<span data-ttu-id="e2126-145">A ' RecoveryPoint ' paraméter az "RecoveryPointBase" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e2126-145">Parameter 'RecoveryPoint' accepts value of type 'RecoveryPointBase' from the pipeline</span></span>

## <span data-ttu-id="e2126-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2126-146">OUTPUTS</span></span>

### <span data-ttu-id="e2126-147">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="e2126-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e2126-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2126-148">NOTES</span></span>

## <span data-ttu-id="e2126-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2126-149">RELATED LINKS</span></span>

[<span data-ttu-id="e2126-150">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e2126-150">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="e2126-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e2126-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="e2126-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e2126-152">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


