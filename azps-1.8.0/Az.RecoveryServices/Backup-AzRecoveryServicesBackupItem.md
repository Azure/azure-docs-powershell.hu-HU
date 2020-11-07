---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 58a4ae793a221a693ffb91c03f024292d364666b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669763"
---
# <span data-ttu-id="b5a40-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b5a40-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="b5a40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5a40-102">SYNOPSIS</span></span>
<span data-ttu-id="b5a40-103">Biztonságimásolat-elem biztonsági másolatának indítása</span><span class="sxs-lookup"><span data-stu-id="b5a40-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="b5a40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5a40-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5a40-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5a40-105">DESCRIPTION</span></span>
<span data-ttu-id="b5a40-106">A **Backup-AzRecoveryServicesBackupItem** parancsmag egy olyan védett Azure biztonsági másolat biztonsági másolatát indítja el, amely nincs a biztonsági ütemtervhez kötve.</span><span class="sxs-lookup"><span data-stu-id="b5a40-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="b5a40-107">A kezdeti biztonsági mentés után azonnal elvégezheti a biztonsági mentést, ha az ütemezett biztonsági mentés után nem tud biztonsági másolatot indítani.</span><span class="sxs-lookup"><span data-stu-id="b5a40-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="b5a40-108">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="b5a40-108">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b5a40-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b5a40-109">EXAMPLES</span></span>

### <span data-ttu-id="b5a40-110">1. példa: biztonsági másolat készítése biztonsági elemről</span><span class="sxs-lookup"><span data-stu-id="b5a40-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="b5a40-111">Az első parancs a AzureVM nevű pstestv2vm1 nevű tartalék tárolót kapja, majd a $NamedContainer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b5a40-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="b5a40-112">A második parancs a $NamedContainer tárolóhoz tartozó biztonsági másolatot kapja, majd a $Item változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b5a40-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="b5a40-113">Az utolsó parancs elindítja a biztonsági mentési feladatot a $Itemban.</span><span class="sxs-lookup"><span data-stu-id="b5a40-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="b5a40-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5a40-114">PARAMETERS</span></span>

### <span data-ttu-id="b5a40-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="b5a40-115">-BackupType</span></span>
<span data-ttu-id="b5a40-116">A végrehajtandó biztonsági másolat típusa</span><span class="sxs-lookup"><span data-stu-id="b5a40-116">Type of backup to be performed</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a40-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5a40-117">-DefaultProfile</span></span>
<span data-ttu-id="b5a40-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5a40-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5a40-119">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="b5a40-119">-EnableCompression</span></span>
<span data-ttu-id="b5a40-120">Ha a tömörítés engedélyezésére van szükség</span><span class="sxs-lookup"><span data-stu-id="b5a40-120">If enabling compression is required</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5a40-121">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="b5a40-121">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="b5a40-122">A lejárat időpontját **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5a40-122">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a40-123">-Elem</span><span class="sxs-lookup"><span data-stu-id="b5a40-123">-Item</span></span>
<span data-ttu-id="b5a40-124">Annak a biztonságimásolat-elemnek a megadása, amelyhez ez a parancsmag elindítja a biztonsági mentési műveletet.</span><span class="sxs-lookup"><span data-stu-id="b5a40-124">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5a40-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b5a40-125">-VaultId</span></span>
<span data-ttu-id="b5a40-126">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="b5a40-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b5a40-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b5a40-127">-Confirm</span></span>
<span data-ttu-id="b5a40-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5a40-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5a40-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5a40-129">-WhatIf</span></span>
<span data-ttu-id="b5a40-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b5a40-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5a40-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5a40-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5a40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5a40-132">CommonParameters</span></span>
<span data-ttu-id="b5a40-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5a40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5a40-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5a40-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5a40-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5a40-135">INPUTS</span></span>

### <span data-ttu-id="b5a40-136">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="b5a40-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="b5a40-137">System. null ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b5a40-137">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b5a40-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b5a40-138">System.String</span></span>

## <span data-ttu-id="b5a40-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5a40-139">OUTPUTS</span></span>

### <span data-ttu-id="b5a40-140">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="b5a40-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b5a40-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5a40-141">NOTES</span></span>

## <span data-ttu-id="b5a40-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5a40-142">RELATED LINKS</span></span>

[<span data-ttu-id="b5a40-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b5a40-143">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="b5a40-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b5a40-144">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b5a40-145">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b5a40-145">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)


