---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 4ae0f9c046cc1383dddeb790e8277dc2429b173b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466664"
---
# <span data-ttu-id="e5f11-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e5f11-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="e5f11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f11-102">SYNOPSIS</span></span>

<span data-ttu-id="e5f11-103">Biztonsági másolat készítése biztonsági másolat készítése.</span><span class="sxs-lookup"><span data-stu-id="e5f11-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="e5f11-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5f11-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5f11-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5f11-105">DESCRIPTION</span></span>

<span data-ttu-id="e5f11-106">A **Backup-AzRecoveryServicesBackupItem** parancsmag biztonsági másolatot készít a védett Azure biztonsági másolatról.</span><span class="sxs-lookup"><span data-stu-id="e5f11-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="e5f11-107">A parancsmag használatával a védelem engedélyezése után azonnal biztonsági másolatot is készíthet, illetve biztonsági másolatot is kezdhet, ha az ütemezett biztonsági másolat meghibásodik.</span><span class="sxs-lookup"><span data-stu-id="e5f11-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="e5f11-108">Ez a parancsmag egyéni adatmegőrzéshez is használható lejárati dátummal vagy anélkül – további részletekért tanulmányozza a paraméterek súgószövegét.</span><span class="sxs-lookup"><span data-stu-id="e5f11-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="e5f11-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5f11-109">EXAMPLES</span></span>

### <span data-ttu-id="e5f11-110">1. példa: Biztonsági másolat készítése biztonsági másolat készítése</span><span class="sxs-lookup"><span data-stu-id="e5f11-110">Example 1: Start a backup for a Backup item</span></span>

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

<span data-ttu-id="e5f11-111">Az első parancs lekérte a pstestv2vm1 nevű AzureVM típusú biztonságimásolat-tárolót, majd a $NamedContainer tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5f11-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="e5f11-112">A második parancs lekérte a biztonságimásolat-elemet a $NamedContainer tárolóhoz, majd a $Item tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5f11-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="e5f11-113">Az utolsó parancs elindítja a biztonságimásolat-elemet a $Item.</span><span class="sxs-lookup"><span data-stu-id="e5f11-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="e5f11-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="e5f11-114">Example 2</span></span>

<span data-ttu-id="e5f11-115">Biztonsági másolat készítése biztonsági másolat készítése.</span><span class="sxs-lookup"><span data-stu-id="e5f11-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="e5f11-116">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="e5f11-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="e5f11-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5f11-117">PARAMETERS</span></span>

### <span data-ttu-id="e5f11-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="e5f11-118">-BackupType</span></span>

<span data-ttu-id="e5f11-119">A biztonsági másolat hajtható végre</span><span class="sxs-lookup"><span data-stu-id="e5f11-119">Type of backup to be performed</span></span>

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

### <span data-ttu-id="e5f11-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f11-120">-DefaultProfile</span></span>

<span data-ttu-id="e5f11-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5f11-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5f11-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="e5f11-122">-EnableCompression</span></span>

<span data-ttu-id="e5f11-123">Ha a tömörítés engedélyezése kötelező</span><span class="sxs-lookup"><span data-stu-id="e5f11-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="e5f11-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="e5f11-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="e5f11-125">A helyreállítási pont lejárati idejét adja meg DateTime-objektumként, ha semmi sem veszi igénybe az alapértelmezett 30 napos értéket.</span><span class="sxs-lookup"><span data-stu-id="e5f11-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="e5f11-126">Virtuális gépre, SQL-re (csak Copy-only-full backup type) és AFS biztonságimásolat-elemekre vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="e5f11-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

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

### <span data-ttu-id="e5f11-127">-Item</span><span class="sxs-lookup"><span data-stu-id="e5f11-127">-Item</span></span>

<span data-ttu-id="e5f11-128">Egy biztonságimásolat-elemet ad meg, amelynek a parancsmagja biztonsági másolatot készít.</span><span class="sxs-lookup"><span data-stu-id="e5f11-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="e5f11-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e5f11-129">-VaultId</span></span>

<span data-ttu-id="e5f11-130">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e5f11-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e5f11-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5f11-131">-Confirm</span></span>

<span data-ttu-id="e5f11-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e5f11-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f11-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f11-133">-WhatIf</span></span>

<span data-ttu-id="e5f11-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e5f11-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="e5f11-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f11-135">CommonParameters</span></span>
<span data-ttu-id="e5f11-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5f11-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f11-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5f11-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f11-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5f11-138">INPUTS</span></span>

### <span data-ttu-id="e5f11-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="e5f11-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="e5f11-140">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e5f11-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e5f11-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e5f11-141">System.String</span></span>

## <span data-ttu-id="e5f11-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5f11-142">OUTPUTS</span></span>

### <span data-ttu-id="e5f11-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="e5f11-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e5f11-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5f11-144">NOTES</span></span>

## <span data-ttu-id="e5f11-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5f11-145">RELATED LINKS</span></span>

[<span data-ttu-id="e5f11-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e5f11-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="e5f11-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e5f11-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="e5f11-148">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e5f11-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
