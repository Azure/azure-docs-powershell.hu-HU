---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: f4f42b257c5ce54085214c8cd9d2f79d9e8a6387
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195449"
---
# <span data-ttu-id="f2aa9-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="f2aa9-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="f2aa9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="f2aa9-103">A megadott névvel rendelkező környezet beolvasása a megadott előfizetés és erőforráscsoport szerint</span><span class="sxs-lookup"><span data-stu-id="f2aa9-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="f2aa9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2aa9-104">SYNTAX</span></span>

### <span data-ttu-id="f2aa9-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2aa9-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2aa9-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="f2aa9-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2aa9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2aa9-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2aa9-108">Lista</span><span class="sxs-lookup"><span data-stu-id="f2aa9-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f2aa9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2aa9-109">DESCRIPTION</span></span>
<span data-ttu-id="f2aa9-110">A megadott névvel rendelkező környezet beolvasása a megadott előfizetés és erőforráscsoport szerint</span><span class="sxs-lookup"><span data-stu-id="f2aa9-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="f2aa9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f2aa9-111">EXAMPLES</span></span>

### <span data-ttu-id="f2aa9-112">Példa 1: idősorozat-áttekintési környezet</span><span class="sxs-lookup"><span data-stu-id="f2aa9-112">Example 1: Get a time series insights environment</span></span>
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

<span data-ttu-id="f2aa9-113">Ez a parancs a következő idősorozatokat kapja meg: környezeti környezet.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="f2aa9-114">2. példa: az összes idősorozatban betekintést tartalmazó környezetek listája</span><span class="sxs-lookup"><span data-stu-id="f2aa9-114">Example 2: List all time series insights environments</span></span>
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

<span data-ttu-id="f2aa9-115">Ez a parancs felsorolja az összes idősort az erőforráscsoport környezetében.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="f2aa9-116">3. példa: idősorozatok beolvasása objektum szerinti környezettel</span><span class="sxs-lookup"><span data-stu-id="f2aa9-116">Example 3: Get a time series insights environment by object</span></span>
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

<span data-ttu-id="f2aa9-117">Ez a parancs az idősorokban észlelt környezetekkel foglalkozik.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="f2aa9-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2aa9-118">PARAMETERS</span></span>

### <span data-ttu-id="f2aa9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2aa9-119">-DefaultProfile</span></span>
<span data-ttu-id="f2aa9-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2aa9-121">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="f2aa9-121">-Expand</span></span>
<span data-ttu-id="f2aa9-122">A $expand = állapot beállítással a környezet belső szolgáltatásainak állapotát fogja tartalmazni az időbeli adatsorok szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

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

### <span data-ttu-id="f2aa9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2aa9-123">-InputObject</span></span>
<span data-ttu-id="f2aa9-124">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f2aa9-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f2aa9-125">-Name</span></span>
<span data-ttu-id="f2aa9-126">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="f2aa9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2aa9-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2aa9-128">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f2aa9-128">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f2aa9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2aa9-129">-SubscriptionId</span></span>
<span data-ttu-id="f2aa9-130">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="f2aa9-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f2aa9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2aa9-131">CommonParameters</span></span>
<span data-ttu-id="f2aa9-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2aa9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2aa9-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2aa9-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2aa9-134">INPUTS</span></span>

### <span data-ttu-id="f2aa9-135">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="f2aa9-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="f2aa9-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2aa9-136">OUTPUTS</span></span>

### <span data-ttu-id="f2aa9-137">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="f2aa9-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="f2aa9-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2aa9-138">NOTES</span></span>

<span data-ttu-id="f2aa9-139">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f2aa9-139">ALIASES</span></span>

<span data-ttu-id="f2aa9-140">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f2aa9-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2aa9-141">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2aa9-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2aa9-143">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f2aa9-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2aa9-144">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="f2aa9-145">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="f2aa9-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="f2aa9-146">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="f2aa9-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="f2aa9-147">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f2aa9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2aa9-148">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="f2aa9-149">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="f2aa9-150">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f2aa9-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f2aa9-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2aa9-151">RELATED LINKS</span></span>

