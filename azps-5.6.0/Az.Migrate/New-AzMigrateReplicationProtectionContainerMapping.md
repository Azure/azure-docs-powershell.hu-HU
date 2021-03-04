---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: ddbc4b9176405dd3102ba82cbe1954a876c9c7f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932802"
---
# <span data-ttu-id="f233f-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f233f-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="f233f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f233f-102">SYNOPSIS</span></span>
<span data-ttu-id="f233f-103">A védelmi tároló megfeleltetésének létrehozására szolgáló művelet.</span><span class="sxs-lookup"><span data-stu-id="f233f-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="f233f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f233f-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f233f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f233f-105">DESCRIPTION</span></span>
<span data-ttu-id="f233f-106">A védelmi tároló megfeleltetésének létrehozására szolgáló művelet.</span><span class="sxs-lookup"><span data-stu-id="f233f-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="f233f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f233f-107">EXAMPLES</span></span>

### <span data-ttu-id="f233f-108">1. példa: Megfeleltetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="f233f-108">Example 1: Create a mapping</span></span>
```powershell
PS C:\> $providerSpecificInput = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtContainerMappingInput]::new()
PS C:\> $providerSpecificInput.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificInput.KeyVaultId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.KeyVault/vaults/migratekv846827101"
PS C:\> $providerSpecificInput.KeyVaultUri = "https://migratekv846827101.vault.azure.net"
PS C:\> $providerSpecificInput.ServiceBusConnectionStringSecretName = "ServiceBusConnectionString"
PS C:\> $providerSpecificInput.StorageAccountId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Storage/storageAccounts/migrategwsa846827101"
PS C:\> $providerSpecificInput.StorageAccountSasSecretName = "migrategwsa846827101-gwySas"
PS C:\> $providerSpecificInput.TargetLocation = "centraluseuap"

PS C:\> New-AzMigrateReplicationProtectionContainerMapping -FabricName "AzMigratePWSHTc8d1replicationfabric" -MappingName "containermapping" -ProtectionContainerName "AzMigratePWSHTc8d1replicationcontainer" -ResourceGroupName "azmigratepwshtestasr13072020" -ResourceName "AzMigrateTestProjectPWSH02aarsvault"  -PolicyId "/subscriptionsxxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy"  -ProviderSpecificInput $providerSpecificInput -TargetProtectionContainerId  "Microsoft Azure"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="f233f-109">Megfeleltetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="f233f-109">Create a mapping</span></span>

## <span data-ttu-id="f233f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f233f-110">PARAMETERS</span></span>

### <span data-ttu-id="f233f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f233f-111">-AsJob</span></span>
<span data-ttu-id="f233f-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="f233f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f233f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f233f-113">-DefaultProfile</span></span>
<span data-ttu-id="f233f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f233f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f233f-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="f233f-115">-FabricName</span></span>
<span data-ttu-id="f233f-116">Anyagnév.</span><span class="sxs-lookup"><span data-stu-id="f233f-116">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f233f-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="f233f-117">-MappingName</span></span>
<span data-ttu-id="f233f-118">Protection container mapping name.</span><span class="sxs-lookup"><span data-stu-id="f233f-118">Protection container mapping name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f233f-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f233f-119">-NoWait</span></span>
<span data-ttu-id="f233f-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="f233f-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f233f-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="f233f-121">-PolicyId</span></span>
<span data-ttu-id="f233f-122">Vonatkozó szabályzat.</span><span class="sxs-lookup"><span data-stu-id="f233f-122">Applicable policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f233f-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="f233f-123">-ProtectionContainerName</span></span>
<span data-ttu-id="f233f-124">Védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="f233f-124">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f233f-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="f233f-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="f233f-126">Szolgáltatóspecifikus bemenet a párosításhoz.</span><span class="sxs-lookup"><span data-stu-id="f233f-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="f233f-127">Ennek létrehozásáról a NOTES (PROVIDERSPECIFICINPUT) tulajdonságokat és egy kivonattáblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f233f-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IReplicationProviderSpecificContainerMappingInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f233f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f233f-128">-ResourceGroupName</span></span>
<span data-ttu-id="f233f-129">Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="f233f-129">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f233f-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f233f-130">-ResourceName</span></span>
<span data-ttu-id="f233f-131">A helyreállítási szolgáltatások tárolója neve.</span><span class="sxs-lookup"><span data-stu-id="f233f-131">The name of the recovery services vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f233f-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f233f-132">-SubscriptionId</span></span>
<span data-ttu-id="f233f-133">Azure-előfizetés azonosítója, amelyben a projekt létrejött.</span><span class="sxs-lookup"><span data-stu-id="f233f-133">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f233f-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="f233f-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="f233f-135">A cél egyedi védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="f233f-135">The target unique protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f233f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f233f-136">-Confirm</span></span>
<span data-ttu-id="f233f-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f233f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f233f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f233f-138">-WhatIf</span></span>
<span data-ttu-id="f233f-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f233f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f233f-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f233f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f233f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f233f-141">CommonParameters</span></span>
<span data-ttu-id="f233f-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f233f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f233f-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f233f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f233f-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f233f-144">INPUTS</span></span>

## <span data-ttu-id="f233f-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f233f-145">OUTPUTS</span></span>

### <span data-ttu-id="f233f-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f233f-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="f233f-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f233f-147">NOTES</span></span>

<span data-ttu-id="f233f-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f233f-148">ALIASES</span></span>

<span data-ttu-id="f233f-149">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="f233f-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f233f-150">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="f233f-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f233f-151">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f233f-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f233f-152">PROVIDERSPECIFICINPUT: <IReplicationProviderSpecificContainerMappingInput> Szolgáltatóspecifikus bemenet a párosításhoz.</span><span class="sxs-lookup"><span data-stu-id="f233f-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="f233f-153">`[InstanceType <String>]`: Az osztály típusa.</span><span class="sxs-lookup"><span data-stu-id="f233f-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="f233f-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f233f-154">RELATED LINKS</span></span>

