---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 6c8debac9091d28091695847b36d0cbc1b219125
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838643"
---
# <span data-ttu-id="b9804-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b9804-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="b9804-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9804-102">SYNOPSIS</span></span>

<span data-ttu-id="b9804-103">Biztonságimásolat-elem biztonsági másolatának indítása</span><span class="sxs-lookup"><span data-stu-id="b9804-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="b9804-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9804-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9804-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9804-105">DESCRIPTION</span></span>

<span data-ttu-id="b9804-106">A **Backup-AzRecoveryServicesBackupItem** parancsmag egy olyan védett Azure biztonsági másolat biztonsági másolatát indítja el, amely nincs a biztonsági ütemtervhez kötve.</span><span class="sxs-lookup"><span data-stu-id="b9804-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="b9804-107">A kezdeti biztonsági mentés után azonnal elvégezheti a biztonsági mentést, ha az ütemezett biztonsági mentés után nem tud biztonsági másolatot indítani.</span><span class="sxs-lookup"><span data-stu-id="b9804-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="b9804-108">Állítsa be a boltozat környezetét a-VaultId paraméter használatával.</span><span class="sxs-lookup"><span data-stu-id="b9804-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="b9804-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b9804-109">EXAMPLES</span></span>

### <span data-ttu-id="b9804-110">1. példa: biztonsági másolat készítése biztonsági elemről</span><span class="sxs-lookup"><span data-stu-id="b9804-110">Example 1: Start a backup for a Backup item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="b9804-111">Az első parancs a AzureVM nevű pstestv2vm1 nevű tartalék tárolót kapja, majd a $NamedContainer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b9804-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="b9804-112">A második parancs a $NamedContainer tárolóhoz tartozó biztonsági másolatot kapja, majd a $Item változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b9804-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="b9804-113">Az utolsó parancs elindítja a biztonsági mentési feladatot a $Itemban.</span><span class="sxs-lookup"><span data-stu-id="b9804-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="b9804-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9804-114">PARAMETERS</span></span>

### <span data-ttu-id="b9804-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="b9804-115">-BackupType</span></span>

<span data-ttu-id="b9804-116">A végrehajtandó biztonsági másolat típusa</span><span class="sxs-lookup"><span data-stu-id="b9804-116">Type of backup to be performed</span></span>

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

### <span data-ttu-id="b9804-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9804-117">-DefaultProfile</span></span>

<span data-ttu-id="b9804-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9804-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9804-119">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="b9804-119">-EnableCompression</span></span>

<span data-ttu-id="b9804-120">Ha a tömörítés engedélyezésére van szükség</span><span class="sxs-lookup"><span data-stu-id="b9804-120">If enabling compression is required</span></span>

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

### <span data-ttu-id="b9804-121">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="b9804-121">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="b9804-122">A lejárat időpontját **datetime** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9804-122">Specifies an expiry time as a **DateTime** object.</span></span>

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

### <span data-ttu-id="b9804-123">-Elem</span><span class="sxs-lookup"><span data-stu-id="b9804-123">-Item</span></span>

<span data-ttu-id="b9804-124">Annak a biztonságimásolat-elemnek a megadása, amelyhez ez a parancsmag elindítja a biztonsági mentési műveletet.</span><span class="sxs-lookup"><span data-stu-id="b9804-124">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="b9804-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b9804-125">-VaultId</span></span>

<span data-ttu-id="b9804-126">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="b9804-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b9804-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9804-127">-Confirm</span></span>

<span data-ttu-id="b9804-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9804-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9804-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9804-129">-WhatIf</span></span>

<span data-ttu-id="b9804-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9804-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9804-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9804-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9804-132">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9804-132">-CommonParameters</span></span>

<span data-ttu-id="b9804-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9804-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9804-134">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b9804-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9804-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9804-135">INPUTS</span></span>

### <span data-ttu-id="b9804-136">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="b9804-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="b9804-137">System. null ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b9804-137">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b9804-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b9804-138">System.String</span></span>

## <span data-ttu-id="b9804-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9804-139">OUTPUTS</span></span>

### <span data-ttu-id="b9804-140">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="b9804-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b9804-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9804-141">NOTES</span></span>

## <span data-ttu-id="b9804-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9804-142">RELATED LINKS</span></span>

[<span data-ttu-id="b9804-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b9804-143">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="b9804-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b9804-144">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b9804-145">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b9804-145">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
