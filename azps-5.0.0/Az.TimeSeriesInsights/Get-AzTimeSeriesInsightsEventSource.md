---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187906"
---
# <span data-ttu-id="687d8-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="687d8-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="687d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="687d8-102">SYNOPSIS</span></span>
<span data-ttu-id="687d8-103">A megadott környezetben kapja meg az esemény forrását.</span><span class="sxs-lookup"><span data-stu-id="687d8-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="687d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="687d8-104">SYNTAX</span></span>

### <span data-ttu-id="687d8-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="687d8-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="687d8-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="687d8-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="687d8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="687d8-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="687d8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="687d8-108">DESCRIPTION</span></span>
<span data-ttu-id="687d8-109">A megadott környezetben kapja meg az esemény forrását.</span><span class="sxs-lookup"><span data-stu-id="687d8-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="687d8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="687d8-110">EXAMPLES</span></span>

### <span data-ttu-id="687d8-111">1. példa: az összes eseményforrás listázása a megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="687d8-111">Example 1: List all event sources under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001

ConsumerGroupName     : testgroup2
EventHubName          : hubname001
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.EventHub/namespaces/spacename001/eventhubs/hu 
                        bname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/estest001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus
Name                  : estest001
ServiceBusNamespace   : spacename001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="687d8-112">Ez a parancs felsorolja az összes eseményforrás a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="687d8-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="687d8-113">2. példa: megadott eseményforrás beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="687d8-113">Example 2: Get a specified event source by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001 -Name iots001

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="687d8-114">Ez a parancs egy adott esemény forrását kapja.</span><span class="sxs-lookup"><span data-stu-id="687d8-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="687d8-115">3. példa: meghatározott eseményforrás beszerzése objektum alapján</span><span class="sxs-lookup"><span data-stu-id="687d8-115">Example 3: Get a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsi-esrfyi9h
PS C:\> Get-AzTimeSeriesInsightsEventSource -InputObject $es

ConsumerGroupName     : tsi-test-i01k5l
EventHubName          : eventhubname-d2rvmp
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.EventHub/namespaces/eventhubspace-0t3khp/eventhubs/eventhubname-d2rvmp
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x/eventsources/tsi-esrfyi9h
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus2
Name                  : tsi-esrfyi9h
ServiceBusNamespace   : eventhubspace-0t3khp
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="687d8-116">Ez a parancs egy adott esemény forrását kapja.</span><span class="sxs-lookup"><span data-stu-id="687d8-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="687d8-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="687d8-117">PARAMETERS</span></span>

### <span data-ttu-id="687d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="687d8-118">-DefaultProfile</span></span>
<span data-ttu-id="687d8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="687d8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="687d8-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="687d8-120">-EnvironmentName</span></span>
<span data-ttu-id="687d8-121">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="687d8-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="687d8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="687d8-122">-InputObject</span></span>
<span data-ttu-id="687d8-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="687d8-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="687d8-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="687d8-124">-Name</span></span>
<span data-ttu-id="687d8-125">A megadott környezethez társított idősorozat-adatforrások neve.</span><span class="sxs-lookup"><span data-stu-id="687d8-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687d8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="687d8-126">-ResourceGroupName</span></span>
<span data-ttu-id="687d8-127">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="687d8-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="687d8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="687d8-128">-SubscriptionId</span></span>
<span data-ttu-id="687d8-129">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="687d8-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="687d8-130">CommonParameters</span></span>
<span data-ttu-id="687d8-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="687d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="687d8-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="687d8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="687d8-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="687d8-133">INPUTS</span></span>

### <span data-ttu-id="687d8-134">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="687d8-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="687d8-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="687d8-135">OUTPUTS</span></span>

### <span data-ttu-id="687d8-136">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="687d8-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="687d8-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="687d8-137">NOTES</span></span>

<span data-ttu-id="687d8-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="687d8-138">ALIASES</span></span>

<span data-ttu-id="687d8-139">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="687d8-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="687d8-140">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="687d8-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="687d8-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="687d8-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="687d8-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="687d8-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="687d8-143">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="687d8-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="687d8-144">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="687d8-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="687d8-145">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="687d8-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="687d8-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="687d8-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="687d8-147">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="687d8-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="687d8-148">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="687d8-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="687d8-149">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="687d8-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="687d8-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="687d8-150">RELATED LINKS</span></span>

