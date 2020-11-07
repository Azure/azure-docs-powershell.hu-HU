---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 357256d1c1a754915cbebc978e5c4ccf4440ccf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679528"
---
# <span data-ttu-id="2a33c-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2a33c-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="2a33c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a33c-102">SYNOPSIS</span></span>
<span data-ttu-id="2a33c-103">Lehetővé teszi a biztonsági mentést egy megadott biztonsági házirenddel rendelkező elemhez.</span><span class="sxs-lookup"><span data-stu-id="2a33c-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a33c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a33c-104">SYNTAX</span></span>

### <span data-ttu-id="2a33c-105">AzureVMComputeEnableProtection (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2a33c-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a33c-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="2a33c-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a33c-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="2a33c-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 -StorageAccountName <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a33c-108">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="2a33c-108">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a33c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a33c-109">DESCRIPTION</span></span>
<span data-ttu-id="2a33c-110">Az **enable-AzureRmRecoveryServicesBackupProtection** parancsmag az Azure Backup Protection házirendjét állítja be egy elemen.</span><span class="sxs-lookup"><span data-stu-id="2a33c-110">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="2a33c-111">Állítsa be a boltozat környezetét az Set-AzureRmRecoveryServicesVaultContext parancsmag használatával, mielőtt az aktuális parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="2a33c-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2a33c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="2a33c-112">EXAMPLES</span></span>

### <span data-ttu-id="2a33c-113">1. példa: biztonsági védelem engedélyezése egy elemhez</span><span class="sxs-lookup"><span data-stu-id="2a33c-113">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="2a33c-114">Az első parancsmag alapértelmezett házirend-objektumot kap, majd a $Pol változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2a33c-114">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="2a33c-115">A második parancsmag a V2VM nevű ARM virtuális gép biztonsági mentési házirendjét a $Pol házirend segítségével állítja be.</span><span class="sxs-lookup"><span data-stu-id="2a33c-115">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="2a33c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a33c-116">PARAMETERS</span></span>

### <span data-ttu-id="2a33c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a33c-117">-DefaultProfile</span></span>
<span data-ttu-id="2a33c-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a33c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a33c-119">-Elem</span><span class="sxs-lookup"><span data-stu-id="2a33c-119">-Item</span></span>
<span data-ttu-id="2a33c-120">Annak a biztonsági másolatnak a biztonsági másolatát adja meg, amelyhez ez a parancsmag engedélyezi a védelmet.</span><span class="sxs-lookup"><span data-stu-id="2a33c-120">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="2a33c-121">Ha **AzureRmRecoveryServicesBackupItem** szeretne beolvasni, használja az Get-AzureRmRecoveryServicesBackupItem parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2a33c-121">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="2a33c-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2a33c-122">-Name</span></span>
<span data-ttu-id="2a33c-123">A biztonságimásolat-elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a33c-123">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="2a33c-124">-Házirend</span><span class="sxs-lookup"><span data-stu-id="2a33c-124">-Policy</span></span>
<span data-ttu-id="2a33c-125">Azt a védelmi házirendet adja meg, amelyet a parancsmag társít egy elemhez.</span><span class="sxs-lookup"><span data-stu-id="2a33c-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="2a33c-126">**AzureRmRecoveryServicesBackupProtectionPolicy** objektum beolvasásához használja az Get-AzureRmRecoveryServicesBackupProtectionPolicy parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2a33c-126">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="2a33c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a33c-127">-ResourceGroupName</span></span>
<span data-ttu-id="2a33c-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a33c-128">Specifies the name of the resource group.</span></span>
<span data-ttu-id="2a33c-129">Ezt a paramétert csak a ARM virtuális gépek esetében adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a33c-129">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="2a33c-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="2a33c-130">-ServiceName</span></span>
<span data-ttu-id="2a33c-131">A szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a33c-131">Specifies the service name.</span></span>
<span data-ttu-id="2a33c-132">Ezt a paramétert csak az ASM virtuális gépek esetében adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a33c-132">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="2a33c-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2a33c-133">-StorageAccountName</span></span>
<span data-ttu-id="2a33c-134">Azure fájlmegosztás tárolási fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="2a33c-134">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a33c-135">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2a33c-135">-VaultId</span></span>
<span data-ttu-id="2a33c-136">A helyreállítási szolgáltatások boltozatának azonosítója</span><span class="sxs-lookup"><span data-stu-id="2a33c-136">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2a33c-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2a33c-137">-Confirm</span></span>
<span data-ttu-id="2a33c-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a33c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a33c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a33c-139">-WhatIf</span></span>
<span data-ttu-id="2a33c-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2a33c-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a33c-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a33c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a33c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a33c-142">CommonParameters</span></span>
<span data-ttu-id="2a33c-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a33c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a33c-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a33c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a33c-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a33c-145">INPUTS</span></span>

### <span data-ttu-id="2a33c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2a33c-146">System.String</span></span>
<span data-ttu-id="2a33c-147">Paraméterek: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2a33c-147">Parameters: VaultId (ByValue)</span></span>

### <span data-ttu-id="2a33c-148">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="2a33c-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="2a33c-149">Paraméterek: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2a33c-149">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="2a33c-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a33c-150">OUTPUTS</span></span>

### <span data-ttu-id="2a33c-151">Microsoft. Azure. Command. RecoveryServices. backup. parancsmagok. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="2a33c-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2a33c-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a33c-152">NOTES</span></span>

## <span data-ttu-id="2a33c-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a33c-153">RELATED LINKS</span></span>

[<span data-ttu-id="2a33c-154">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2a33c-154">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="2a33c-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2a33c-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


