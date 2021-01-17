---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345702"
---
# <span data-ttu-id="89bbc-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="89bbc-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="89bbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="89bbc-103">Frissíti a környezetet a megadott névvel a megadott előfizetési és erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="89bbc-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="89bbc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89bbc-104">SYNTAX</span></span>

### <span data-ttu-id="89bbc-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89bbc-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="89bbc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="89bbc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="89bbc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89bbc-107">DESCRIPTION</span></span>
<span data-ttu-id="89bbc-108">Frissíti a környezetet a megadott névvel a megadott előfizetési és erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="89bbc-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="89bbc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89bbc-109">EXAMPLES</span></span>

### <span data-ttu-id="89bbc-110">1. példa: A Generációs1 idősorozatok elemzési környezetének frissítése</span><span class="sxs-lookup"><span data-stu-id="89bbc-110">Example 1: Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="89bbc-111">Ez a parancs frissíti a Gen1 idősorok elemzési környezetét.</span><span class="sxs-lookup"><span data-stu-id="89bbc-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="89bbc-112">2. példa: A Generációs1 idősorok elemzési környezetének frissítése</span><span class="sxs-lookup"><span data-stu-id="89bbc-112">Example 2:  Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="89bbc-113">Ez a parancs frissíti a Gen1 idősorok elemzési környezetét.</span><span class="sxs-lookup"><span data-stu-id="89bbc-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="89bbc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89bbc-114">PARAMETERS</span></span>

### <span data-ttu-id="89bbc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89bbc-115">-AsJob</span></span>
<span data-ttu-id="89bbc-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="89bbc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="89bbc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89bbc-117">-DefaultProfile</span></span>
<span data-ttu-id="89bbc-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89bbc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89bbc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89bbc-119">-InputObject</span></span>
<span data-ttu-id="89bbc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="89bbc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="89bbc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="89bbc-121">-Name</span></span>
<span data-ttu-id="89bbc-122">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="89bbc-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="89bbc-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="89bbc-123">-NoWait</span></span>
<span data-ttu-id="89bbc-124">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="89bbc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="89bbc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89bbc-125">-ResourceGroupName</span></span>
<span data-ttu-id="89bbc-126">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="89bbc-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="89bbc-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89bbc-127">-SubscriptionId</span></span>
<span data-ttu-id="89bbc-128">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="89bbc-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="89bbc-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="89bbc-129">-Tag</span></span>
<span data-ttu-id="89bbc-130">A környezet további tulajdonságainak kulcsértékes párja.</span><span class="sxs-lookup"><span data-stu-id="89bbc-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="89bbc-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89bbc-131">-Confirm</span></span>
<span data-ttu-id="89bbc-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="89bbc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89bbc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89bbc-133">-WhatIf</span></span>
<span data-ttu-id="89bbc-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="89bbc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89bbc-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89bbc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89bbc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89bbc-136">CommonParameters</span></span>
<span data-ttu-id="89bbc-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89bbc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89bbc-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89bbc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89bbc-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89bbc-139">INPUTS</span></span>

### <span data-ttu-id="89bbc-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="89bbc-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="89bbc-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89bbc-141">OUTPUTS</span></span>

### <span data-ttu-id="89bbc-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="89bbc-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="89bbc-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89bbc-143">NOTES</span></span>

<span data-ttu-id="89bbc-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="89bbc-144">ALIASES</span></span>

<span data-ttu-id="89bbc-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="89bbc-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89bbc-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="89bbc-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89bbc-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89bbc-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89bbc-148">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="89bbc-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89bbc-149">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="89bbc-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="89bbc-150">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="89bbc-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="89bbc-151">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="89bbc-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="89bbc-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="89bbc-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89bbc-153">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="89bbc-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="89bbc-154">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="89bbc-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="89bbc-155">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="89bbc-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="89bbc-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89bbc-156">RELATED LINKS</span></span>

