---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: f0147cea03d4b535102efd53af1a4d5f88338530
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301244"
---
# <span data-ttu-id="e89ad-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e89ad-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="e89ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e89ad-102">SYNOPSIS</span></span>
<span data-ttu-id="e89ad-103">Lehetővé teszi a biztonsági mentést egy megadott biztonsági házirenddel rendelkező elemhez.</span><span class="sxs-lookup"><span data-stu-id="e89ad-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="e89ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e89ad-104">SYNTAX</span></span>

### <span data-ttu-id="e89ad-105">AzureVMComputeEnableProtection (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e89ad-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e89ad-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="e89ad-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e89ad-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="e89ad-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e89ad-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="e89ad-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e89ad-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="e89ad-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e89ad-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="e89ad-110">DESCRIPTION</span></span>
<span data-ttu-id="e89ad-111">Az **enable-AzRecoveryServicesBackupProtection** parancsmag lehetővé teszi a biztonsági mentést, ha a védelmi házirendet az elemmel társítja.</span><span class="sxs-lookup"><span data-stu-id="e89ad-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="e89ad-112">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="e89ad-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e89ad-113">Példák</span><span class="sxs-lookup"><span data-stu-id="e89ad-113">EXAMPLES</span></span>

### <span data-ttu-id="e89ad-114">1. példa: biztonsági védelem engedélyezése egy elemhez</span><span class="sxs-lookup"><span data-stu-id="e89ad-114">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="e89ad-115">Az első parancsmag alapértelmezett házirend-objektumot kap, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e89ad-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="e89ad-116">A második parancsmag azt adja meg, hogy a rendszer milyen partíciókat szeretne biztonsági másolatot készíteni, és az $inclusionDiskLUNS változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="e89ad-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="e89ad-117">A harmadik parancsmag a V2VM nevű ARM virtuális gép biztonsági mentési házirendjét a $Pol házirend segítségével állítja be.</span><span class="sxs-lookup"><span data-stu-id="e89ad-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="e89ad-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="e89ad-118">Example 2</span></span>

<span data-ttu-id="e89ad-119">Lehetővé teszi a biztonsági mentést egy megadott biztonsági házirenddel rendelkező elemhez.</span><span class="sxs-lookup"><span data-stu-id="e89ad-119">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="e89ad-120">autogenerated</span><span class="sxs-lookup"><span data-stu-id="e89ad-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="e89ad-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e89ad-121">PARAMETERS</span></span>

### <span data-ttu-id="e89ad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e89ad-122">-DefaultProfile</span></span>
<span data-ttu-id="e89ad-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e89ad-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e89ad-124">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="e89ad-124">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="e89ad-125">Csak a biztonsági másolat csak a biztonsági másolatba való beállítás megadása</span><span class="sxs-lookup"><span data-stu-id="e89ad-125">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="e89ad-126">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="e89ad-126">-ExclusionDisksList</span></span>
<span data-ttu-id="e89ad-127">A biztonsági mentésben kizárandó és a többi rész automatikusan is megjelenik a biztonsági mentésben kihagyott lemezpartíció listájával.</span><span class="sxs-lookup"><span data-stu-id="e89ad-127">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="e89ad-128">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="e89ad-128">-InclusionDisksList</span></span>
<span data-ttu-id="e89ad-129">A biztonsági másolatban szerepeltetni kívánt, a többiekhez tartozó lemezpartíció listája automatikusan ki van zárva az operációs rendszer merevlemeze kivételével.</span><span class="sxs-lookup"><span data-stu-id="e89ad-129">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="e89ad-130">-Elem</span><span class="sxs-lookup"><span data-stu-id="e89ad-130">-Item</span></span>
<span data-ttu-id="e89ad-131">Annak a biztonsági másolatnak a biztonsági másolatát adja meg, amelyhez ez a parancsmag engedélyezi a védelmet.</span><span class="sxs-lookup"><span data-stu-id="e89ad-131">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="e89ad-132">Ha **AzureRmRecoveryServicesBackupItem** szeretne beolvasni, használja az Get-AzRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e89ad-132">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="e89ad-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e89ad-133">-Name</span></span>
<span data-ttu-id="e89ad-134">A biztonságimásolat-elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e89ad-134">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="e89ad-135">-Házirend</span><span class="sxs-lookup"><span data-stu-id="e89ad-135">-Policy</span></span>
<span data-ttu-id="e89ad-136">Azt a védelmi házirendet adja meg, amelyet a parancsmag társít egy elemhez.</span><span class="sxs-lookup"><span data-stu-id="e89ad-136">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="e89ad-137">**AzureRmRecoveryServicesBackupProtectionPolicy** objektum beolvasásához használja az Get-AzRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e89ad-137">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="e89ad-138">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e89ad-138">-ProtectableItem</span></span>
<span data-ttu-id="e89ad-139">A megadott házirenddel védett elemet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e89ad-139">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="e89ad-140">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="e89ad-140">-ResetExclusionSettings</span></span>
<span data-ttu-id="e89ad-141">Az elemhez társított lemezterület-kizárási beállítás visszaállítása</span><span class="sxs-lookup"><span data-stu-id="e89ad-141">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="e89ad-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e89ad-142">-ResourceGroupName</span></span>
<span data-ttu-id="e89ad-143">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e89ad-143">Specifies the name of the resource group.</span></span>
<span data-ttu-id="e89ad-144">Ezt a paramétert csak a ARM virtuális gépek esetében adja meg.</span><span class="sxs-lookup"><span data-stu-id="e89ad-144">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="e89ad-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e89ad-145">-StorageAccountName</span></span>
<span data-ttu-id="e89ad-146">Azure fájlmegosztás tárolási fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="e89ad-146">Azure file share storage account name</span></span>

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

### <span data-ttu-id="e89ad-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e89ad-147">-VaultId</span></span>
<span data-ttu-id="e89ad-148">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="e89ad-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e89ad-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e89ad-149">-Confirm</span></span>
<span data-ttu-id="e89ad-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e89ad-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e89ad-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e89ad-151">-WhatIf</span></span>
<span data-ttu-id="e89ad-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e89ad-152">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="e89ad-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e89ad-153">CommonParameters</span></span>
<span data-ttu-id="e89ad-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e89ad-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e89ad-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e89ad-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e89ad-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e89ad-156">INPUTS</span></span>

### <span data-ttu-id="e89ad-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e89ad-157">System.String</span></span>

### <span data-ttu-id="e89ad-158">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="e89ad-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="e89ad-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e89ad-159">OUTPUTS</span></span>

### <span data-ttu-id="e89ad-160">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="e89ad-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="e89ad-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e89ad-161">NOTES</span></span>

## <span data-ttu-id="e89ad-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e89ad-162">RELATED LINKS</span></span>

[<span data-ttu-id="e89ad-163">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e89ad-163">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="e89ad-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e89ad-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


