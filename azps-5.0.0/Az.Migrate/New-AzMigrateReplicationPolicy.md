---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187315"
---
# <span data-ttu-id="c235a-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="c235a-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="c235a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c235a-102">SYNOPSIS</span></span>
<span data-ttu-id="c235a-103">A replikációs házirend létrehozásának művelete</span><span class="sxs-lookup"><span data-stu-id="c235a-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="c235a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c235a-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c235a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c235a-105">DESCRIPTION</span></span>
<span data-ttu-id="c235a-106">A replikációs házirend létrehozásának művelete</span><span class="sxs-lookup"><span data-stu-id="c235a-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="c235a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c235a-107">EXAMPLES</span></span>

### <span data-ttu-id="c235a-108">Példa 1: replikációs házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="c235a-108">Example 1: Create a replication policy</span></span>
```powershell
PS C:\> $providerSpecificPolicy = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtPolicyCreationInput]::new()
PS C:\> $providerSpecificPolicy.AppConsistentFrequencyInMinute = 240
PS C:\> $providerSpecificPolicy.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificPolicy.RecoveryPointHistoryInMinute = 4320
PS C:\> $providerSpecificPolicy.CrashConsistentFrequencyInMinute = 60
PS C:\> New-AzMigrateReplicationPolicy -PolicyName TestPolicy -ResourceGroupName ResourceGroup -ResourceName VaultName -SubscriptionId SubscriptionId -ProviderSpecificInput $providerSpecificPolicy

Location Name       Type
-------- ----       ----
         TestPolicy Microsoft.RecoveryServices/vaults/replicationPolicies
         
```

<span data-ttu-id="c235a-109">Házirend létrehozása a VmWare CBT-hoz</span><span class="sxs-lookup"><span data-stu-id="c235a-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="c235a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c235a-110">PARAMETERS</span></span>

### <span data-ttu-id="c235a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c235a-111">-AsJob</span></span>
<span data-ttu-id="c235a-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="c235a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c235a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c235a-113">-DefaultProfile</span></span>
<span data-ttu-id="c235a-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c235a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c235a-115">-Várva</span><span class="sxs-lookup"><span data-stu-id="c235a-115">-NoWait</span></span>
<span data-ttu-id="c235a-116">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="c235a-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c235a-117">-Házirendnév</span><span class="sxs-lookup"><span data-stu-id="c235a-117">-PolicyName</span></span>
<span data-ttu-id="c235a-118">Replikációs házirend neve</span><span class="sxs-lookup"><span data-stu-id="c235a-118">Replication policy name</span></span>

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

### <span data-ttu-id="c235a-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="c235a-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="c235a-120">A ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="c235a-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="c235a-121">A kivitelezéshez tekintse meg a PROVIDERSPECIFICINPUT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c235a-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicyProviderSpecificInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c235a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c235a-122">-ResourceGroupName</span></span>
<span data-ttu-id="c235a-123">Annak az erőforráscsoportnek a neve, amelyben a helyreállítási szolgáltatások boltozata található.</span><span class="sxs-lookup"><span data-stu-id="c235a-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="c235a-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c235a-124">-ResourceName</span></span>
<span data-ttu-id="c235a-125">A helyreállítási szolgáltatások boltozatának neve.</span><span class="sxs-lookup"><span data-stu-id="c235a-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="c235a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c235a-126">-SubscriptionId</span></span>
<span data-ttu-id="c235a-127">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="c235a-127">The subscription Id.</span></span>

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

### <span data-ttu-id="c235a-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c235a-128">-Confirm</span></span>
<span data-ttu-id="c235a-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c235a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c235a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c235a-130">-WhatIf</span></span>
<span data-ttu-id="c235a-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c235a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c235a-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c235a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c235a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c235a-133">CommonParameters</span></span>
<span data-ttu-id="c235a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c235a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c235a-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c235a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c235a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c235a-136">INPUTS</span></span>

## <span data-ttu-id="c235a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c235a-137">OUTPUTS</span></span>

### <span data-ttu-id="c235a-138">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="c235a-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="c235a-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c235a-139">NOTES</span></span>

<span data-ttu-id="c235a-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c235a-140">ALIASES</span></span>

<span data-ttu-id="c235a-141">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="c235a-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c235a-142">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c235a-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c235a-143">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c235a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c235a-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> : a ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="c235a-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="c235a-145">`[InstanceType <String>]`: Az osztály típusa.</span><span class="sxs-lookup"><span data-stu-id="c235a-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="c235a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c235a-146">RELATED LINKS</span></span>

