---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356774"
---
# <span data-ttu-id="a19ef-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a19ef-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="a19ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a19ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a19ef-103">Replikációs házirend létrehozására vonatkozó művelet</span><span class="sxs-lookup"><span data-stu-id="a19ef-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="a19ef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a19ef-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a19ef-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a19ef-105">DESCRIPTION</span></span>
<span data-ttu-id="a19ef-106">Replikációs házirend létrehozására vonatkozó művelet</span><span class="sxs-lookup"><span data-stu-id="a19ef-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="a19ef-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a19ef-107">EXAMPLES</span></span>

### <span data-ttu-id="a19ef-108">1. példa: Replikációs házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="a19ef-108">Example 1: Create a replication policy</span></span>
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

<span data-ttu-id="a19ef-109">Házirendet hoz létre a VmWare Cbt-hoz</span><span class="sxs-lookup"><span data-stu-id="a19ef-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="a19ef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a19ef-110">PARAMETERS</span></span>

### <span data-ttu-id="a19ef-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a19ef-111">-AsJob</span></span>
<span data-ttu-id="a19ef-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="a19ef-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a19ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19ef-113">-DefaultProfile</span></span>
<span data-ttu-id="a19ef-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a19ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a19ef-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a19ef-115">-NoWait</span></span>
<span data-ttu-id="a19ef-116">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="a19ef-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a19ef-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="a19ef-117">-PolicyName</span></span>
<span data-ttu-id="a19ef-118">Replikációs házirend neve</span><span class="sxs-lookup"><span data-stu-id="a19ef-118">Replication policy name</span></span>

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

### <span data-ttu-id="a19ef-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="a19ef-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="a19ef-120">A ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="a19ef-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="a19ef-121">Ennek létrehozásáról a NOTES (PROVIDERSPECIFICINPUT) tulajdonságokat és egy kivonattáblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a19ef-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a19ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a19ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="a19ef-123">Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.</span><span class="sxs-lookup"><span data-stu-id="a19ef-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="a19ef-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a19ef-124">-ResourceName</span></span>
<span data-ttu-id="a19ef-125">A helyreállítási szolgáltatások tárolója neve.</span><span class="sxs-lookup"><span data-stu-id="a19ef-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="a19ef-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a19ef-126">-SubscriptionId</span></span>
<span data-ttu-id="a19ef-127">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a19ef-127">The subscription Id.</span></span>

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

### <span data-ttu-id="a19ef-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a19ef-128">-Confirm</span></span>
<span data-ttu-id="a19ef-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a19ef-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a19ef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a19ef-130">-WhatIf</span></span>
<span data-ttu-id="a19ef-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a19ef-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a19ef-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a19ef-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a19ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19ef-133">CommonParameters</span></span>
<span data-ttu-id="a19ef-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a19ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19ef-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a19ef-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19ef-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a19ef-136">INPUTS</span></span>

## <span data-ttu-id="a19ef-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a19ef-137">OUTPUTS</span></span>

### <span data-ttu-id="a19ef-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="a19ef-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="a19ef-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a19ef-139">NOTES</span></span>

<span data-ttu-id="a19ef-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a19ef-140">ALIASES</span></span>

<span data-ttu-id="a19ef-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a19ef-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a19ef-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a19ef-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a19ef-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a19ef-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a19ef-144">PROVIDERSPECIFICINPUT: <IPolicyProviderSpecificInput> The ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="a19ef-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="a19ef-145">`[InstanceType <String>]`: Az osztály típusa.</span><span class="sxs-lookup"><span data-stu-id="a19ef-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="a19ef-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a19ef-146">RELATED LINKS</span></span>

