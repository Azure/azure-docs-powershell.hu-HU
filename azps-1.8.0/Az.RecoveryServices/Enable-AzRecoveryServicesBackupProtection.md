---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7f29c0bef53d75be4f5b253e3a15bf78cbacd04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669750"
---
# <span data-ttu-id="73d79-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="73d79-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="73d79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73d79-102">SYNOPSIS</span></span>
<span data-ttu-id="73d79-103">Lehetővé teszi a biztonsági mentést egy megadott biztonsági házirenddel rendelkező elemhez.</span><span class="sxs-lookup"><span data-stu-id="73d79-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="73d79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73d79-104">SYNTAX</span></span>

### <span data-ttu-id="73d79-105">AzureVMComputeEnableProtection (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73d79-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ResourceGroupName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73d79-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="73d79-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73d79-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="73d79-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73d79-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="73d79-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73d79-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="73d79-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73d79-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="73d79-110">DESCRIPTION</span></span>
<span data-ttu-id="73d79-111">Az **enable-AzRecoveryServicesBackupProtection** parancsmag az Azure Backup Protection házirendjét állítja be egy elemen.</span><span class="sxs-lookup"><span data-stu-id="73d79-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="73d79-112">Állítsa be a boltozat környezetét az Set-AzRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="73d79-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="73d79-113">Példák</span><span class="sxs-lookup"><span data-stu-id="73d79-113">EXAMPLES</span></span>

### <span data-ttu-id="73d79-114">1. példa: biztonsági védelem engedélyezése egy elemhez</span><span class="sxs-lookup"><span data-stu-id="73d79-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="73d79-115">Az első parancsmag alapértelmezett házirend-objektumot kap, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="73d79-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="73d79-116">A második parancsmag a V2VM nevű ARM virtuális gép biztonsági mentési házirendjét a $Pol házirend segítségével állítja be.</span><span class="sxs-lookup"><span data-stu-id="73d79-116">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="73d79-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73d79-117">PARAMETERS</span></span>

### <span data-ttu-id="73d79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d79-118">-DefaultProfile</span></span>
<span data-ttu-id="73d79-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73d79-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73d79-120">-Elem</span><span class="sxs-lookup"><span data-stu-id="73d79-120">-Item</span></span>
<span data-ttu-id="73d79-121">Annak a biztonsági másolatnak a biztonsági másolatát adja meg, amelyhez ez a parancsmag engedélyezi a védelmet.</span><span class="sxs-lookup"><span data-stu-id="73d79-121">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="73d79-122">Ha **AzureRmRecoveryServicesBackupItem** szeretne beolvasni, használja az Get-AzRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="73d79-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="73d79-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73d79-123">-Name</span></span>
<span data-ttu-id="73d79-124">A biztonságimásolat-elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73d79-124">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="73d79-125">-Házirend</span><span class="sxs-lookup"><span data-stu-id="73d79-125">-Policy</span></span>
<span data-ttu-id="73d79-126">Azt a védelmi házirendet adja meg, amelyet a parancsmag társít egy elemhez.</span><span class="sxs-lookup"><span data-stu-id="73d79-126">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="73d79-127">**AzureRmRecoveryServicesBackupProtectionPolicy** objektum beolvasásához használja az Get-AzRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="73d79-127">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d79-128">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="73d79-128">-ProtectableItem</span></span>
<span data-ttu-id="73d79-129">A feladat állapotának szűrése értékkel.</span><span class="sxs-lookup"><span data-stu-id="73d79-129">Filter value for status of job.</span></span>

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

### <span data-ttu-id="73d79-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73d79-130">-ResourceGroupName</span></span>
<span data-ttu-id="73d79-131">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73d79-131">Specifies the name of the resource group.</span></span>
<span data-ttu-id="73d79-132">Ezt a paramétert csak a ARM virtuális gépek esetében adja meg.</span><span class="sxs-lookup"><span data-stu-id="73d79-132">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="73d79-133">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="73d79-133">-ServiceName</span></span>
<span data-ttu-id="73d79-134">A szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73d79-134">Specifies the service name.</span></span>
<span data-ttu-id="73d79-135">Ezt a paramétert csak az ASM virtuális gépek esetében adja meg.</span><span class="sxs-lookup"><span data-stu-id="73d79-135">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="73d79-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="73d79-136">-StorageAccountName</span></span>
<span data-ttu-id="73d79-137">Azure fájlmegosztás tárolási fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="73d79-137">Azure file share storage account name</span></span>

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

### <span data-ttu-id="73d79-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="73d79-138">-VaultId</span></span>
<span data-ttu-id="73d79-139">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="73d79-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="73d79-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="73d79-140">-Confirm</span></span>
<span data-ttu-id="73d79-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="73d79-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73d79-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73d79-142">-WhatIf</span></span>
<span data-ttu-id="73d79-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="73d79-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73d79-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73d79-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73d79-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d79-145">CommonParameters</span></span>
<span data-ttu-id="73d79-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73d79-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d79-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73d79-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d79-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73d79-148">INPUTS</span></span>

### <span data-ttu-id="73d79-149">System. String</span><span class="sxs-lookup"><span data-stu-id="73d79-149">System.String</span></span>

### <span data-ttu-id="73d79-150">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="73d79-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="73d79-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73d79-151">OUTPUTS</span></span>

### <span data-ttu-id="73d79-152">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="73d79-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="73d79-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73d79-153">NOTES</span></span>

## <span data-ttu-id="73d79-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73d79-154">RELATED LINKS</span></span>

[<span data-ttu-id="73d79-155">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="73d79-155">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="73d79-156">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="73d79-156">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


