---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7b52c6064f7dd692b732558b682290e8612f383c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846986"
---
# <span data-ttu-id="ba6bf-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ba6bf-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="ba6bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6bf-103">Lehetővé teszi a biztonsági mentést egy megadott biztonsági házirenddel rendelkező elemhez.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="ba6bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba6bf-104">SYNTAX</span></span>

### <span data-ttu-id="ba6bf-105">AzureVMComputeEnableProtection (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba6bf-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba6bf-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="ba6bf-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba6bf-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="ba6bf-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba6bf-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="ba6bf-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba6bf-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="ba6bf-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba6bf-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba6bf-110">DESCRIPTION</span></span>
<span data-ttu-id="ba6bf-111">Az **enable-AzRecoveryServicesBackupProtection** parancsmag az Azure Backup Protection házirendjét állítja be egy elemen.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="ba6bf-112">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ba6bf-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ba6bf-113">EXAMPLES</span></span>

### <span data-ttu-id="ba6bf-114">1. példa: biztonsági védelem engedélyezése egy elemhez</span><span class="sxs-lookup"><span data-stu-id="ba6bf-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="ba6bf-115">Az első parancsmag alapértelmezett házirend-objektumot kap, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="ba6bf-116">A második parancsmag azt adja meg, hogy a rendszer milyen partíciókat szeretne biztonsági másolatot készíteni, és az $inclusionDiskLUNS változóban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="ba6bf-117">A harmadik parancsmag a V2VM nevű ARM virtuális gép biztonsági mentési házirendjét a $Pol házirend segítségével állítja be.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="ba6bf-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba6bf-118">PARAMETERS</span></span>

### <span data-ttu-id="ba6bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6bf-119">-DefaultProfile</span></span>
<span data-ttu-id="ba6bf-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba6bf-121">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="ba6bf-121">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="ba6bf-122">Csak a biztonsági másolat csak a biztonsági másolatba való beállítás megadása</span><span class="sxs-lookup"><span data-stu-id="ba6bf-122">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="ba6bf-123">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="ba6bf-123">-ExclusionDisksList</span></span>
<span data-ttu-id="ba6bf-124">A biztonsági másolatban kizárandó Disk LUN-lista</span><span class="sxs-lookup"><span data-stu-id="ba6bf-124">List of Disk LUNs to exclude in backup</span></span>

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

### <span data-ttu-id="ba6bf-125">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="ba6bf-125">-InclusionDisksList</span></span>
<span data-ttu-id="ba6bf-126">A biztonsági másolatba felvenni kívánt lemezpartíciók listája</span><span class="sxs-lookup"><span data-stu-id="ba6bf-126">List of Disk LUNs to include in backup</span></span>

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

### <span data-ttu-id="ba6bf-127">-Elem</span><span class="sxs-lookup"><span data-stu-id="ba6bf-127">-Item</span></span>
<span data-ttu-id="ba6bf-128">Annak a biztonsági másolatnak a biztonsági másolatát adja meg, amelyhez ez a parancsmag engedélyezi a védelmet.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-128">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="ba6bf-129">Ha **AzureRmRecoveryServicesBackupItem** szeretne beolvasni, használja az Get-AzRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-129">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="ba6bf-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba6bf-130">-Name</span></span>
<span data-ttu-id="ba6bf-131">A biztonságimásolat-elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-131">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="ba6bf-132">-Házirend</span><span class="sxs-lookup"><span data-stu-id="ba6bf-132">-Policy</span></span>
<span data-ttu-id="ba6bf-133">Azt a védelmi házirendet adja meg, amelyet a parancsmag társít egy elemhez.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-133">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="ba6bf-134">**AzureRmRecoveryServicesBackupProtectionPolicy** objektum beolvasásához használja az Get-AzRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-134">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="ba6bf-135">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ba6bf-135">-ProtectableItem</span></span>
<span data-ttu-id="ba6bf-136">A feladat állapotának szűrése értékkel.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-136">Filter value for status of job.</span></span>

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

### <span data-ttu-id="ba6bf-137">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="ba6bf-137">-ResetExclusionSettings</span></span>
<span data-ttu-id="ba6bf-138">Az elemhez társított lemezterület-kizárási beállítás visszaállítása</span><span class="sxs-lookup"><span data-stu-id="ba6bf-138">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="ba6bf-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba6bf-139">-ResourceGroupName</span></span>
<span data-ttu-id="ba6bf-140">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-140">Specifies the name of the resource group.</span></span>
<span data-ttu-id="ba6bf-141">Ezt a paramétert csak a ARM virtuális gépek esetében adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-141">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="ba6bf-142">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="ba6bf-142">-ServiceName</span></span>
<span data-ttu-id="ba6bf-143">A szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-143">Specifies the service name.</span></span>
<span data-ttu-id="ba6bf-144">Ezt a paramétert csak az ASM virtuális gépek esetében adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-144">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba6bf-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ba6bf-145">-StorageAccountName</span></span>
<span data-ttu-id="ba6bf-146">Azure fájlmegosztás tárolási fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="ba6bf-146">Azure file share storage account name</span></span>

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

### <span data-ttu-id="ba6bf-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ba6bf-147">-VaultId</span></span>
<span data-ttu-id="ba6bf-148">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="ba6bf-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ba6bf-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba6bf-149">-Confirm</span></span>
<span data-ttu-id="ba6bf-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba6bf-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba6bf-151">-WhatIf</span></span>
<span data-ttu-id="ba6bf-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba6bf-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba6bf-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6bf-154">CommonParameters</span></span>
<span data-ttu-id="ba6bf-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba6bf-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6bf-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ba6bf-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6bf-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba6bf-157">INPUTS</span></span>

### <span data-ttu-id="ba6bf-158">System. String</span><span class="sxs-lookup"><span data-stu-id="ba6bf-158">System.String</span></span>

### <span data-ttu-id="ba6bf-159">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="ba6bf-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="ba6bf-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba6bf-160">OUTPUTS</span></span>

### <span data-ttu-id="ba6bf-161">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="ba6bf-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ba6bf-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba6bf-162">NOTES</span></span>

## <span data-ttu-id="ba6bf-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba6bf-163">RELATED LINKS</span></span>

[<span data-ttu-id="ba6bf-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ba6bf-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="ba6bf-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ba6bf-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


