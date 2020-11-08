---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185741"
---
# <span data-ttu-id="3a588-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="3a588-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="3a588-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a588-102">SYNOPSIS</span></span>
<span data-ttu-id="3a588-103">Frissíti a környezetet a megadott néven a megadott előfizetés és erőforráscsoport szerint.</span><span class="sxs-lookup"><span data-stu-id="3a588-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="3a588-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a588-104">SYNTAX</span></span>

### <span data-ttu-id="3a588-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a588-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3a588-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3a588-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3a588-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a588-107">DESCRIPTION</span></span>
<span data-ttu-id="3a588-108">Frissíti a környezetet a megadott néven a megadott előfizetés és erőforráscsoport szerint.</span><span class="sxs-lookup"><span data-stu-id="3a588-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="3a588-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3a588-109">EXAMPLES</span></span>

### <span data-ttu-id="3a588-110">1. példa: Gen1-idősorozatok környezetbe való betekintésének frissítése</span><span class="sxs-lookup"><span data-stu-id="3a588-110">Example 1: Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="3a588-111">Ez a parancs frissíti a Gen1-adatsorozatok környezetének áttekintését.</span><span class="sxs-lookup"><span data-stu-id="3a588-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="3a588-112">2. példa: a Gen1-idősorozatok környezetének frissítése</span><span class="sxs-lookup"><span data-stu-id="3a588-112">Example 2:  Update a Gen1 time series insights environment</span></span>
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

<span data-ttu-id="3a588-113">Ez a parancs frissíti a Gen1-adatsorozatok környezetének áttekintését.</span><span class="sxs-lookup"><span data-stu-id="3a588-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="3a588-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a588-114">PARAMETERS</span></span>

### <span data-ttu-id="3a588-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a588-115">-AsJob</span></span>
<span data-ttu-id="3a588-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="3a588-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3a588-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a588-117">-DefaultProfile</span></span>
<span data-ttu-id="3a588-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a588-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a588-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a588-119">-InputObject</span></span>
<span data-ttu-id="3a588-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3a588-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a588-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3a588-121">-Name</span></span>
<span data-ttu-id="3a588-122">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="3a588-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="3a588-123">-Várva</span><span class="sxs-lookup"><span data-stu-id="3a588-123">-NoWait</span></span>
<span data-ttu-id="3a588-124">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="3a588-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3a588-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a588-125">-ResourceGroupName</span></span>
<span data-ttu-id="3a588-126">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3a588-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="3a588-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a588-127">-SubscriptionId</span></span>
<span data-ttu-id="3a588-128">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="3a588-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="3a588-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="3a588-129">-Tag</span></span>
<span data-ttu-id="3a588-130">A környezet további tulajdonságainak kulcs-érték párjai</span><span class="sxs-lookup"><span data-stu-id="3a588-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="3a588-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3a588-131">-Confirm</span></span>
<span data-ttu-id="3a588-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3a588-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a588-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a588-133">-WhatIf</span></span>
<span data-ttu-id="3a588-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3a588-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a588-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3a588-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a588-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a588-136">CommonParameters</span></span>
<span data-ttu-id="3a588-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a588-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a588-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3a588-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a588-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a588-139">INPUTS</span></span>

### <span data-ttu-id="3a588-140">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="3a588-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="3a588-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a588-141">OUTPUTS</span></span>

### <span data-ttu-id="3a588-142">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="3a588-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="3a588-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a588-143">NOTES</span></span>

<span data-ttu-id="3a588-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="3a588-144">ALIASES</span></span>

<span data-ttu-id="3a588-145">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="3a588-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a588-146">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="3a588-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a588-147">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="3a588-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a588-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="3a588-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a588-149">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="3a588-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="3a588-150">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="3a588-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="3a588-151">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="3a588-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="3a588-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="3a588-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a588-153">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="3a588-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="3a588-154">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3a588-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="3a588-155">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3a588-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="3a588-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a588-156">RELATED LINKS</span></span>

