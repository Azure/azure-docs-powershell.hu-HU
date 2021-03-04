---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 86e143455f287bef8bff4b391f7f40aa01fba99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936553"
---
# <span data-ttu-id="54275-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="54275-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="54275-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54275-102">SYNOPSIS</span></span>
<span data-ttu-id="54275-103">Frissíti a környezetet a megadott névvel a megadott előfizetési és erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="54275-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="54275-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="54275-104">SYNTAX</span></span>

### <span data-ttu-id="54275-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="54275-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="54275-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="54275-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54275-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="54275-107">DESCRIPTION</span></span>
<span data-ttu-id="54275-108">Frissíti a környezetet a megadott névvel a megadott előfizetési és erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="54275-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="54275-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="54275-109">EXAMPLES</span></span>

### <span data-ttu-id="54275-110">1. példa: A Generációs1 idősorozatok elemzési környezetének frissítése</span><span class="sxs-lookup"><span data-stu-id="54275-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="54275-111">Ez a parancs frissíti a Gen1 idősorok elemzési környezetét.</span><span class="sxs-lookup"><span data-stu-id="54275-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="54275-112">2. példa: A Gen1 idősorok elemzési környezetének frissítése</span><span class="sxs-lookup"><span data-stu-id="54275-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="54275-113">Ez a parancs frissíti a Gen1 idősorok elemzési környezetét.</span><span class="sxs-lookup"><span data-stu-id="54275-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="54275-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54275-114">PARAMETERS</span></span>

### <span data-ttu-id="54275-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54275-115">-AsJob</span></span>
<span data-ttu-id="54275-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="54275-116">Run the command as a job</span></span>

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

### <span data-ttu-id="54275-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54275-117">-DefaultProfile</span></span>
<span data-ttu-id="54275-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54275-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54275-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54275-119">-InputObject</span></span>
<span data-ttu-id="54275-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="54275-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54275-121">-Name</span><span class="sxs-lookup"><span data-stu-id="54275-121">-Name</span></span>
<span data-ttu-id="54275-122">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="54275-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54275-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="54275-123">-NoWait</span></span>
<span data-ttu-id="54275-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="54275-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="54275-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54275-125">-ResourceGroupName</span></span>
<span data-ttu-id="54275-126">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="54275-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54275-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54275-127">-SubscriptionId</span></span>
<span data-ttu-id="54275-128">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="54275-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54275-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="54275-129">-Tag</span></span>
<span data-ttu-id="54275-130">A környezet további tulajdonságainak kulcsértékes párja.</span><span class="sxs-lookup"><span data-stu-id="54275-130">Key-value pairs of additional properties for the environment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54275-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54275-131">-Confirm</span></span>
<span data-ttu-id="54275-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="54275-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54275-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54275-133">-WhatIf</span></span>
<span data-ttu-id="54275-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="54275-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54275-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54275-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54275-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54275-136">CommonParameters</span></span>
<span data-ttu-id="54275-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54275-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54275-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54275-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54275-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54275-139">INPUTS</span></span>

### <span data-ttu-id="54275-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="54275-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="54275-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54275-141">OUTPUTS</span></span>

### <span data-ttu-id="54275-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="54275-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="54275-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="54275-143">NOTES</span></span>

<span data-ttu-id="54275-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="54275-144">ALIASES</span></span>

<span data-ttu-id="54275-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="54275-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="54275-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="54275-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54275-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="54275-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="54275-148">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="54275-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="54275-149">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="54275-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="54275-150">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="54275-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="54275-151">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="54275-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="54275-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="54275-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="54275-153">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="54275-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="54275-154">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="54275-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="54275-155">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="54275-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="54275-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54275-156">RELATED LINKS</span></span>

