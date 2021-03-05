---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 151b8a431183727dbfaec242705421ba775b0b99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011157"
---
# <span data-ttu-id="68763-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="68763-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="68763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68763-102">SYNOPSIS</span></span>
<span data-ttu-id="68763-103">A megadott nevű környezetet adja meg a megadott előfizetési és erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="68763-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="68763-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="68763-104">SYNTAX</span></span>

### <span data-ttu-id="68763-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="68763-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="68763-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="68763-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="68763-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="68763-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="68763-108">Lista</span><span class="sxs-lookup"><span data-stu-id="68763-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="68763-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="68763-109">DESCRIPTION</span></span>
<span data-ttu-id="68763-110">A megadott nevű környezetet adja meg a megadott előfizetési és erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="68763-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="68763-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="68763-111">EXAMPLES</span></span>

### <span data-ttu-id="68763-112">1. példa: Idősorok elemzési környezetének lekérte</span><span class="sxs-lookup"><span data-stu-id="68763-112">Example 1: Get a time series insights environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="68763-113">Ez a parancs idősorozat-elemzési környezetet kap.</span><span class="sxs-lookup"><span data-stu-id="68763-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="68763-114">2. példa: Az összes idősorozat-elemzési környezet felsorolása</span><span class="sxs-lookup"><span data-stu-id="68763-114">Example 2: List all time series insights environments</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup

DataAccessFqdn                      : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86.env.timeseries.azure.com
DataAccessId                        : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86
Id                                  : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/ 
                                      tsill
IngressState                        :
Kind                                : Gen2
Location                            : EastUs
Name                                : tsill
PropertyUsageState                  :
Sku                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                         : 1
SkuName                             : L1
StateDetailCode                     :
StateDetailCurrentCount             :
StateDetailMaxCount                 :
StateDetailMessage                  :
StorageConfigurationAccountName     : cdolauli
Tag                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimeSeriesIdProperty                : {ccc}
Type                                : Microsoft.TimeSeriesInsights/Environments
WarmStoreConfigurationDataRetention : 00:00:00

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
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="68763-115">Ez a parancs felsorolja az erőforráscsoportok összes idősorozat-elemzési környezetét.</span><span class="sxs-lookup"><span data-stu-id="68763-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="68763-116">3. példa: Idősorok elemzési környezetének lekérte objektumról objektumra</span><span class="sxs-lookup"><span data-stu-id="68763-116">Example 3: Get a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName tsi-test-i01k5l -Name tsi-envv8u56x 
PS C:\> Get-AzTimeSeriesInsightsEnvironment -InputObject $env

DataAccessFqdn               : d76a61f2-8a30-41a5-9587-f241eb9b48d9.env.timeseries.azure.com
DataAccessId                 : d76a61f2-8a30-41a5-9587-f241eb9b48d9
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x
IngressState                 :
Kind                         : Gen1
Location                     : eastus2
Name                         : tsi-envv8u56x
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 1
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="68763-117">Ez a parancs idősorozat-elemzési környezeteket kap.</span><span class="sxs-lookup"><span data-stu-id="68763-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="68763-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68763-118">PARAMETERS</span></span>

### <span data-ttu-id="68763-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68763-119">-DefaultProfile</span></span>
<span data-ttu-id="68763-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68763-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68763-121">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="68763-121">-Expand</span></span>
<span data-ttu-id="68763-122">A $expand=állapot beállításának része lesz a környezet belső szolgáltatásainak állapota az Idősor insights szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="68763-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68763-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68763-123">-InputObject</span></span>
<span data-ttu-id="68763-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="68763-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68763-125">-Name</span><span class="sxs-lookup"><span data-stu-id="68763-125">-Name</span></span>
<span data-ttu-id="68763-126">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="68763-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68763-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68763-127">-ResourceGroupName</span></span>
<span data-ttu-id="68763-128">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="68763-128">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68763-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68763-129">-SubscriptionId</span></span>
<span data-ttu-id="68763-130">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="68763-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68763-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68763-131">CommonParameters</span></span>
<span data-ttu-id="68763-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68763-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68763-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68763-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68763-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68763-134">INPUTS</span></span>

### <span data-ttu-id="68763-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="68763-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="68763-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68763-136">OUTPUTS</span></span>

### <span data-ttu-id="68763-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="68763-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="68763-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="68763-138">NOTES</span></span>

<span data-ttu-id="68763-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="68763-139">ALIASES</span></span>

<span data-ttu-id="68763-140">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="68763-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68763-141">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="68763-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68763-142">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="68763-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68763-143">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="68763-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="68763-144">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="68763-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="68763-145">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="68763-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="68763-146">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="68763-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="68763-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="68763-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="68763-148">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="68763-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="68763-149">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="68763-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="68763-150">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="68763-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="68763-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68763-151">RELATED LINKS</span></span>

