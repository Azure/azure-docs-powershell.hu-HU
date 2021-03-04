---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 0472a24e15a05d1ea07639ee5495efc5feaaba6c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936641"
---
# <span data-ttu-id="70f9b-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="70f9b-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="70f9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="70f9b-103">Engedélyezi a biztonsági mentést egy megadott biztonságimásolat-védelmi házirendet megadva.</span><span class="sxs-lookup"><span data-stu-id="70f9b-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="70f9b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="70f9b-104">SYNTAX</span></span>

### <span data-ttu-id="70f9b-105">AzureVMComputeEnableProtection (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70f9b-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70f9b-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="70f9b-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70f9b-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="70f9b-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70f9b-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="70f9b-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70f9b-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="70f9b-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70f9b-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="70f9b-110">DESCRIPTION</span></span>
<span data-ttu-id="70f9b-111">Az **Enable-AzRecoveryServicesBackupProtection** parancsmag lehetővé teszi a biztonsági mentést azáltal, hogy társít egy védelmi házirendet az elemhez.</span><span class="sxs-lookup"><span data-stu-id="70f9b-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="70f9b-112">Ha a házirendazonosító nincs jelen, vagy a biztonságimásolat-elem nincs társítva egyetlen házirendhez sem, akkor ez a parancs egy házirendazonosítót vár.</span><span class="sxs-lookup"><span data-stu-id="70f9b-112">If policy ID is not present or the backup item is not associated with any policy, then this command will expect a policyID.</span></span>
<span data-ttu-id="70f9b-113">Az aktuális parancsmag használata előtt állítsa be a tároló környezetét a Set-AzRecoveryServicesVaultContext parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="70f9b-113">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="70f9b-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="70f9b-114">EXAMPLES</span></span>

### <span data-ttu-id="70f9b-115">1. példa: Biztonsági mentés védelmének engedélyezése egy elemhez</span><span class="sxs-lookup"><span data-stu-id="70f9b-115">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="70f9b-116">Az első parancsmag kap egy alapértelmezett házirendobjektumot, majd tárolja azt a $Pol változóban.</span><span class="sxs-lookup"><span data-stu-id="70f9b-116">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="70f9b-117">A második parancsmag megadja azokat a lemez-LUN-okat, amelyekről biztonsági adatokat kell biztonságiba $inclusionDiskLUNS változóban.</span><span class="sxs-lookup"><span data-stu-id="70f9b-117">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="70f9b-118">A harmadik parancsmag a V2VM nevű virtuális ARM biztonsági mentésvédelmi házirendet állítja be a $Pol.</span><span class="sxs-lookup"><span data-stu-id="70f9b-118">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="70f9b-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="70f9b-119">Example 2</span></span>

<span data-ttu-id="70f9b-120">Engedélyezi a biztonsági mentést egy megadott biztonságimásolat-védelmi házirendet megadva.</span><span class="sxs-lookup"><span data-stu-id="70f9b-120">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="70f9b-121">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="70f9b-121">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="70f9b-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70f9b-122">PARAMETERS</span></span>

### <span data-ttu-id="70f9b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f9b-123">-DefaultProfile</span></span>
<span data-ttu-id="70f9b-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70f9b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70f9b-125">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="70f9b-125">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="70f9b-126">Beállítás csak az operációs rendszer lemezei biztonsági mentéséhez</span><span class="sxs-lookup"><span data-stu-id="70f9b-126">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="70f9b-127">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="70f9b-127">-ExclusionDisksList</span></span>
<span data-ttu-id="70f9b-128">A biztonsági mentésből kihagyni, a többit pedig automatikusan tartalmazza a rendszer a lemez LUN-okkal.</span><span class="sxs-lookup"><span data-stu-id="70f9b-128">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="70f9b-129">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="70f9b-129">-InclusionDisksList</span></span>
<span data-ttu-id="70f9b-130">A biztonsági mentésbe foglalható lemez LUN-ok listája, a többit pedig az operációs rendszer lemeze kivételével automatikusan kizárja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="70f9b-130">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="70f9b-131">-Item</span><span class="sxs-lookup"><span data-stu-id="70f9b-131">-Item</span></span>
<span data-ttu-id="70f9b-132">Megadja azt a biztonságimásolat-elemet, amelynek a parancsmagja védelmet tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="70f9b-132">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="70f9b-133">**AzureRmRecoveryServicesBackupItem** beszerzéséhez használja a Get-AzRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70f9b-133">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="70f9b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="70f9b-134">-Name</span></span>
<span data-ttu-id="70f9b-135">A biztonsági másolat elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70f9b-135">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="70f9b-136">-Házirend</span><span class="sxs-lookup"><span data-stu-id="70f9b-136">-Policy</span></span>
<span data-ttu-id="70f9b-137">Ez a parancsmag által egy elemhez társítható védelmi házirendet ad meg.</span><span class="sxs-lookup"><span data-stu-id="70f9b-137">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="70f9b-138">**AzureRmRecoveryServicesBackupProtectionPolicy** objektum beszerzéséhez használja a Get-AzRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="70f9b-138">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="70f9b-139">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="70f9b-139">-ProtectableItem</span></span>
<span data-ttu-id="70f9b-140">A megadott házirendnek megfelelő elemet adja meg.</span><span class="sxs-lookup"><span data-stu-id="70f9b-140">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="70f9b-141">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="70f9b-141">-ResetExclusionSettings</span></span>
<span data-ttu-id="70f9b-142">Az elemhez társított lemezkizárási beállítás alaphelyzetbe állítása</span><span class="sxs-lookup"><span data-stu-id="70f9b-142">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="70f9b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70f9b-143">-ResourceGroupName</span></span>
<span data-ttu-id="70f9b-144">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70f9b-144">Specifies the name of the resource group.</span></span>
<span data-ttu-id="70f9b-145">Ezt a paramétert csak virtuális ARM adja meg.</span><span class="sxs-lookup"><span data-stu-id="70f9b-145">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="70f9b-146">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="70f9b-146">-StorageAccountName</span></span>
<span data-ttu-id="70f9b-147">Azure-fájlmegosztási tárfiók neve</span><span class="sxs-lookup"><span data-stu-id="70f9b-147">Azure file share storage account name</span></span>

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

### <span data-ttu-id="70f9b-148">-VaultId</span><span class="sxs-lookup"><span data-stu-id="70f9b-148">-VaultId</span></span>
<span data-ttu-id="70f9b-149">ARM helyreállítási szolgáltatások tárolójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="70f9b-149">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="70f9b-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70f9b-150">-Confirm</span></span>
<span data-ttu-id="70f9b-151">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="70f9b-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70f9b-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70f9b-152">-WhatIf</span></span>
<span data-ttu-id="70f9b-153">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="70f9b-153">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="70f9b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f9b-154">CommonParameters</span></span>
<span data-ttu-id="70f9b-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70f9b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f9b-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70f9b-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f9b-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70f9b-157">INPUTS</span></span>

### <span data-ttu-id="70f9b-158">System.String</span><span class="sxs-lookup"><span data-stu-id="70f9b-158">System.String</span></span>

### <span data-ttu-id="70f9b-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="70f9b-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="70f9b-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70f9b-160">OUTPUTS</span></span>

### <span data-ttu-id="70f9b-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="70f9b-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="70f9b-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="70f9b-162">NOTES</span></span>

## <span data-ttu-id="70f9b-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70f9b-163">RELATED LINKS</span></span>

[<span data-ttu-id="70f9b-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="70f9b-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="70f9b-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="70f9b-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


