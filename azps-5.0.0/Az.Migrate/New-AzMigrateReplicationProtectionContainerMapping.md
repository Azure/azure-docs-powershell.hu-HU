---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194345"
---
# <span data-ttu-id="c926e-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c926e-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="c926e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c926e-102">SYNOPSIS</span></span>
<span data-ttu-id="c926e-103">A védelmi tároló megfeleltetését létrehozó művelet.</span><span class="sxs-lookup"><span data-stu-id="c926e-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="c926e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c926e-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c926e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c926e-105">DESCRIPTION</span></span>
<span data-ttu-id="c926e-106">A védelmi tároló megfeleltetését létrehozó művelet.</span><span class="sxs-lookup"><span data-stu-id="c926e-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="c926e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c926e-107">EXAMPLES</span></span>

### <span data-ttu-id="c926e-108">Példa 1: megfeleltetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="c926e-108">Example 1: Create a mapping</span></span>
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

<span data-ttu-id="c926e-109">Megfeleltetés létrehozása</span><span class="sxs-lookup"><span data-stu-id="c926e-109">Create a mapping</span></span>

## <span data-ttu-id="c926e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c926e-110">PARAMETERS</span></span>

### <span data-ttu-id="c926e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c926e-111">-AsJob</span></span>
<span data-ttu-id="c926e-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="c926e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c926e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c926e-113">-DefaultProfile</span></span>
<span data-ttu-id="c926e-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c926e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c926e-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="c926e-115">-FabricName</span></span>
<span data-ttu-id="c926e-116">A szövet neve.</span><span class="sxs-lookup"><span data-stu-id="c926e-116">Fabric name.</span></span>

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

### <span data-ttu-id="c926e-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="c926e-117">-MappingName</span></span>
<span data-ttu-id="c926e-118">Védelmi tároló megfeleltetésének neve.</span><span class="sxs-lookup"><span data-stu-id="c926e-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="c926e-119">-Várva</span><span class="sxs-lookup"><span data-stu-id="c926e-119">-NoWait</span></span>
<span data-ttu-id="c926e-120">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="c926e-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c926e-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="c926e-121">-PolicyId</span></span>
<span data-ttu-id="c926e-122">Alkalmazható házirend.</span><span class="sxs-lookup"><span data-stu-id="c926e-122">Applicable policy.</span></span>

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

### <span data-ttu-id="c926e-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="c926e-123">-ProtectionContainerName</span></span>
<span data-ttu-id="c926e-124">Védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="c926e-124">Protection container name.</span></span>

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

### <span data-ttu-id="c926e-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="c926e-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="c926e-126">A párosításhoz szükséges speciális bemenet.</span><span class="sxs-lookup"><span data-stu-id="c926e-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="c926e-127">A kivitelezéshez tekintse meg a PROVIDERSPECIFICINPUT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c926e-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c926e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c926e-128">-ResourceGroupName</span></span>
<span data-ttu-id="c926e-129">Annak az erőforráscsoportnek a neve, amelyben a helyreállítási szolgáltatások boltozata található.</span><span class="sxs-lookup"><span data-stu-id="c926e-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="c926e-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c926e-130">-ResourceName</span></span>
<span data-ttu-id="c926e-131">A helyreállítási szolgáltatások boltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="c926e-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="c926e-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c926e-132">-SubscriptionId</span></span>
<span data-ttu-id="c926e-133">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="c926e-133">The subscription Id.</span></span>

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

### <span data-ttu-id="c926e-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="c926e-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="c926e-135">A cél egyedi védelmi tároló neve.</span><span class="sxs-lookup"><span data-stu-id="c926e-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="c926e-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c926e-136">-Confirm</span></span>
<span data-ttu-id="c926e-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c926e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c926e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c926e-138">-WhatIf</span></span>
<span data-ttu-id="c926e-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c926e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c926e-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c926e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c926e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c926e-141">CommonParameters</span></span>
<span data-ttu-id="c926e-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c926e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c926e-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c926e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c926e-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c926e-144">INPUTS</span></span>

## <span data-ttu-id="c926e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c926e-145">OUTPUTS</span></span>

### <span data-ttu-id="c926e-146">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c926e-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="c926e-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c926e-147">NOTES</span></span>

<span data-ttu-id="c926e-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c926e-148">ALIASES</span></span>

<span data-ttu-id="c926e-149">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="c926e-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c926e-150">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c926e-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c926e-151">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c926e-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c926e-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> : szolgáltató specifikus bemenet a párosításhoz.</span><span class="sxs-lookup"><span data-stu-id="c926e-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="c926e-153">`[InstanceType <String>]`: Az osztály típusa.</span><span class="sxs-lookup"><span data-stu-id="c926e-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="c926e-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c926e-154">RELATED LINKS</span></span>

