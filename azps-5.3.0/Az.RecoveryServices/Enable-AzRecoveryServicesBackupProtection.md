---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: f0147cea03d4b535102efd53af1a4d5f88338530
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384480"
---
# <span data-ttu-id="7ead4-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7ead4-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="7ead4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ead4-102">SYNOPSIS</span></span>
<span data-ttu-id="7ead4-103">Engedélyezi a biztonsági mentést egy megadott biztonságimásolat-védelmi házirendet be nem véő elemhez.</span><span class="sxs-lookup"><span data-stu-id="7ead4-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="7ead4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ead4-104">SYNTAX</span></span>

### <span data-ttu-id="7ead4-105">AzureVMComputeEnableProtection (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ead4-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ead4-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="7ead4-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ead4-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="7ead4-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ead4-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="7ead4-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ead4-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="7ead4-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ead4-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ead4-110">DESCRIPTION</span></span>
<span data-ttu-id="7ead4-111">Az **Enable-AzRecoveryServicesBackupProtection** parancsmag lehetővé teszi a biztonsági mentést azáltal, hogy társít egy védelmi házirendet az elemhez.</span><span class="sxs-lookup"><span data-stu-id="7ead4-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="7ead4-112">Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="7ead4-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7ead4-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ead4-113">EXAMPLES</span></span>

### <span data-ttu-id="7ead4-114">1. példa: Biztonsági mentés védelmének engedélyezése egy elemhez</span><span class="sxs-lookup"><span data-stu-id="7ead4-114">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="7ead4-115">Az első parancsmag kap egy alapértelmezett házirendobjektumot, majd tárolja azt a $Pol változóban.</span><span class="sxs-lookup"><span data-stu-id="7ead4-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="7ead4-116">A második parancsmag megadja azokat a lemez-LUN-okat, amelyekről biztonsági adatokat kell biztonságiba $inclusionDiskLUNS változóban.</span><span class="sxs-lookup"><span data-stu-id="7ead4-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="7ead4-117">A harmadik parancsmag a V2VM nevű virtuális ARM biztonsági mentésvédelmi házirendet állítja be a $Pol.</span><span class="sxs-lookup"><span data-stu-id="7ead4-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="7ead4-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="7ead4-118">Example 2</span></span>

<span data-ttu-id="7ead4-119">Engedélyezi a biztonsági mentést egy megadott biztonságimásolat-védelmi házirendet be nem véő elemhez.</span><span class="sxs-lookup"><span data-stu-id="7ead4-119">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="7ead4-120">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="7ead4-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="7ead4-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ead4-121">PARAMETERS</span></span>

### <span data-ttu-id="7ead4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ead4-122">-DefaultProfile</span></span>
<span data-ttu-id="7ead4-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ead4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ead4-124">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="7ead4-124">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="7ead4-125">Beállítás csak az operációs rendszer lemezeiről való biztonsági mentéshez</span><span class="sxs-lookup"><span data-stu-id="7ead4-125">Option to specify to backup OS disks only</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-126">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="7ead4-126">-ExclusionDisksList</span></span>
<span data-ttu-id="7ead4-127">A biztonsági mentésből kihagyni, a többit pedig automatikusan tartalmazza a rendszer a lemez LUN-okkal.</span><span class="sxs-lookup"><span data-stu-id="7ead4-127">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-128">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="7ead4-128">-InclusionDisksList</span></span>
<span data-ttu-id="7ead4-129">A biztonsági mentésbe foglalható lemez LUN-ok listája, a többit pedig az operációs rendszer lemeze kivételével automatikusan kizárja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="7ead4-129">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-130">-Item</span><span class="sxs-lookup"><span data-stu-id="7ead4-130">-Item</span></span>
<span data-ttu-id="7ead4-131">Azt a biztonságimásolat-elemet adja meg, amelynek a parancsmagja védelmet tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="7ead4-131">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="7ead4-132">**AzureRmRecoveryServicesBackupItem** beszerzéséhez használja a Get-AzRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7ead4-132">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-133">-Name</span><span class="sxs-lookup"><span data-stu-id="7ead4-133">-Name</span></span>
<span data-ttu-id="7ead4-134">A biztonsági másolat elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ead4-134">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-135">-Házirend</span><span class="sxs-lookup"><span data-stu-id="7ead4-135">-Policy</span></span>
<span data-ttu-id="7ead4-136">Ez a parancsmag által egy elemhez társítható védelmi házirendet ad meg.</span><span class="sxs-lookup"><span data-stu-id="7ead4-136">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="7ead4-137">**AzureRmRecoveryServicesBackupProtectionPolicy** objektum beszerzéséhez használja a Get-AzRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7ead4-137">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-138">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7ead4-138">-ProtectableItem</span></span>
<span data-ttu-id="7ead4-139">A megadott házirendnek megfelelő elemet adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ead4-139">Specifies the item to be protected with the given policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-140">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="7ead4-140">-ResetExclusionSettings</span></span>
<span data-ttu-id="7ead4-141">Az elemhez társított lemezkizárási beállítás alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="7ead4-141">Specifies to reset disk exclusion setting associated with the item</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ead4-142">-ResourceGroupName</span></span>
<span data-ttu-id="7ead4-143">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ead4-143">Specifies the name of the resource group.</span></span>
<span data-ttu-id="7ead4-144">Ezt a paramétert csak virtuális ARM meg.</span><span class="sxs-lookup"><span data-stu-id="7ead4-144">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7ead4-145">-StorageAccountName</span></span>
<span data-ttu-id="7ead4-146">Azure-fájlmegosztási tárfiók neve</span><span class="sxs-lookup"><span data-stu-id="7ead4-146">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7ead4-147">-VaultId</span></span>
<span data-ttu-id="7ead4-148">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7ead4-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7ead4-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ead4-149">-Confirm</span></span>
<span data-ttu-id="7ead4-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7ead4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ead4-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ead4-151">-WhatIf</span></span>
<span data-ttu-id="7ead4-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7ead4-152">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="7ead4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ead4-153">CommonParameters</span></span>
<span data-ttu-id="7ead4-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ead4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ead4-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ead4-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ead4-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ead4-156">INPUTS</span></span>

### <span data-ttu-id="7ead4-157">System.String</span><span class="sxs-lookup"><span data-stu-id="7ead4-157">System.String</span></span>

### <span data-ttu-id="7ead4-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="7ead4-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="7ead4-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ead4-159">OUTPUTS</span></span>

### <span data-ttu-id="7ead4-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="7ead4-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="7ead4-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ead4-161">NOTES</span></span>

## <span data-ttu-id="7ead4-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ead4-162">RELATED LINKS</span></span>

[<span data-ttu-id="7ead4-163">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7ead4-163">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="7ead4-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ead4-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


