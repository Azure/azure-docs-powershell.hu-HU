---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 4ae0f9c046cc1383dddeb790e8277dc2429b173b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182200"
---
# <span data-ttu-id="96eca-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="96eca-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="96eca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96eca-102">SYNOPSIS</span></span>

<span data-ttu-id="96eca-103">Biztonságimásolat-elem biztonsági másolatának indítása</span><span class="sxs-lookup"><span data-stu-id="96eca-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="96eca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96eca-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96eca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96eca-105">DESCRIPTION</span></span>

<span data-ttu-id="96eca-106">A **Backup-AzRecoveryServicesBackupItem** parancsmag ad hoc biztonsági másolatot a védett Azure Backup elemről.</span><span class="sxs-lookup"><span data-stu-id="96eca-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="96eca-107">E parancsmag használatával a biztonsági mentést követően közvetlenül biztonsági másolatot készíthet, vagy biztonsági másolatot készíthet, ha az ütemezett biztonsági mentés nem sikerült.</span><span class="sxs-lookup"><span data-stu-id="96eca-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="96eca-108">Ezt a parancsmagot az egyéni adatmegőrzési művelet lejárati dátumát is használhatja, ha további információra van szüksége a paraméterekkel kapcsolatos súgó szövegben.</span><span class="sxs-lookup"><span data-stu-id="96eca-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="96eca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="96eca-109">EXAMPLES</span></span>

### <span data-ttu-id="96eca-110">1. példa: biztonsági másolat készítése biztonsági elemről</span><span class="sxs-lookup"><span data-stu-id="96eca-110">Example 1: Start a backup for a Backup item</span></span>

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

<span data-ttu-id="96eca-111">Az első parancs a AzureVM nevű pstestv2vm1 nevű tartalék tárolót kapja, majd a $NamedContainer változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="96eca-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="96eca-112">A második parancs a $NamedContainer tárolóhoz tartozó biztonsági másolatot kapja, majd a $Item változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="96eca-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="96eca-113">Az utolsó parancs elindítja a biztonsági mentési feladatot a $Itemban.</span><span class="sxs-lookup"><span data-stu-id="96eca-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="96eca-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="96eca-114">Example 2</span></span>

<span data-ttu-id="96eca-115">Biztonságimásolat-elem biztonsági másolatának indítása</span><span class="sxs-lookup"><span data-stu-id="96eca-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="96eca-116">autogenerated</span><span class="sxs-lookup"><span data-stu-id="96eca-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="96eca-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96eca-117">PARAMETERS</span></span>

### <span data-ttu-id="96eca-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="96eca-118">-BackupType</span></span>

<span data-ttu-id="96eca-119">A végrehajtandó biztonsági másolat típusa</span><span class="sxs-lookup"><span data-stu-id="96eca-119">Type of backup to be performed</span></span>

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

### <span data-ttu-id="96eca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96eca-120">-DefaultProfile</span></span>

<span data-ttu-id="96eca-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96eca-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96eca-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="96eca-122">-EnableCompression</span></span>

<span data-ttu-id="96eca-123">Ha a tömörítés engedélyezésére van szükség</span><span class="sxs-lookup"><span data-stu-id="96eca-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="96eca-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="96eca-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="96eca-125">A helyreállítási pont lejárati időpontját DateTime-objektumként adja meg, ha semmi sem adja meg a 30 nap alapértelmezett értékét.</span><span class="sxs-lookup"><span data-stu-id="96eca-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="96eca-126">A VM, az SQL (csak másolat csak a teljes biztonsági másolat típusa), az AFS biztonsági másolat elemekre alkalmazható.</span><span class="sxs-lookup"><span data-stu-id="96eca-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

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

### <span data-ttu-id="96eca-127">-Elem</span><span class="sxs-lookup"><span data-stu-id="96eca-127">-Item</span></span>

<span data-ttu-id="96eca-128">Annak a biztonságimásolat-elemnek a megadása, amelyhez ez a parancsmag elindítja a biztonsági mentési műveletet.</span><span class="sxs-lookup"><span data-stu-id="96eca-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="96eca-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="96eca-129">-VaultId</span></span>

<span data-ttu-id="96eca-130">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="96eca-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="96eca-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96eca-131">-Confirm</span></span>

<span data-ttu-id="96eca-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96eca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96eca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96eca-133">-WhatIf</span></span>

<span data-ttu-id="96eca-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96eca-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="96eca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96eca-135">CommonParameters</span></span>
<span data-ttu-id="96eca-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96eca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96eca-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="96eca-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96eca-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96eca-138">INPUTS</span></span>

### <span data-ttu-id="96eca-139">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="96eca-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="96eca-140">System. null ' 1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96eca-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="96eca-141">System. String</span><span class="sxs-lookup"><span data-stu-id="96eca-141">System.String</span></span>

## <span data-ttu-id="96eca-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96eca-142">OUTPUTS</span></span>

### <span data-ttu-id="96eca-143">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="96eca-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="96eca-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96eca-144">NOTES</span></span>

## <span data-ttu-id="96eca-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96eca-145">RELATED LINKS</span></span>

[<span data-ttu-id="96eca-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="96eca-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="96eca-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="96eca-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="96eca-148">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="96eca-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
