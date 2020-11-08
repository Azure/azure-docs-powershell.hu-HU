---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: e87487e55ce285aa5c430dabaa274ee70c34ba00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180717"
---
# <span data-ttu-id="c28b6-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="c28b6-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="c28b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c28b6-102">SYNOPSIS</span></span>
<span data-ttu-id="c28b6-103">Frissíti az eseményforrás és a megadott nevű nevet a megadott előfizetésben, erőforrás csoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="c28b6-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="c28b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c28b6-104">SYNTAX</span></span>

### <span data-ttu-id="c28b6-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c28b6-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c28b6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c28b6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c28b6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c28b6-107">DESCRIPTION</span></span>
<span data-ttu-id="c28b6-108">Frissíti az eseményforrás és a megadott nevű nevet a megadott előfizetésben, erőforrás csoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="c28b6-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="c28b6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c28b6-109">EXAMPLES</span></span>

### <span data-ttu-id="c28b6-110">Példa 1: megadott eseményforrás frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="c28b6-110">Example 1: Update a specified event source by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup -Tag @{"tgk"="001"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="c28b6-111">Ez a parancs frissíti az adott esemény forrását.</span><span class="sxs-lookup"><span data-stu-id="c28b6-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="c28b6-112">3. példa: adott eseményforrás frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="c28b6-112">Example 3: Update a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Update-AzTimeSeriesInsightsEventSource -InputObject $es -Tag @{"tgb"="002"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="c28b6-113">Ez a parancs frissíti az adott esemény forrását.</span><span class="sxs-lookup"><span data-stu-id="c28b6-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="c28b6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c28b6-114">PARAMETERS</span></span>

### <span data-ttu-id="c28b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c28b6-115">-DefaultProfile</span></span>
<span data-ttu-id="c28b6-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c28b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c28b6-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="c28b6-117">-EnvironmentName</span></span>
<span data-ttu-id="c28b6-118">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="c28b6-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="c28b6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c28b6-119">-InputObject</span></span>
<span data-ttu-id="c28b6-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c28b6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c28b6-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c28b6-121">-Name</span></span>
<span data-ttu-id="c28b6-122">A megadott környezethez társított idősorozat-adatforrások neve.</span><span class="sxs-lookup"><span data-stu-id="c28b6-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28b6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c28b6-123">-ResourceGroupName</span></span>
<span data-ttu-id="c28b6-124">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c28b6-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="c28b6-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c28b6-125">-SubscriptionId</span></span>
<span data-ttu-id="c28b6-126">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="c28b6-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c28b6-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="c28b6-127">-Tag</span></span>
<span data-ttu-id="c28b6-128">Az eseményforrás további tulajdonságainak kulcs-érték pároka</span><span class="sxs-lookup"><span data-stu-id="c28b6-128">Key-value pairs of additional properties for the event source.</span></span>

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

### <span data-ttu-id="c28b6-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c28b6-129">-Confirm</span></span>
<span data-ttu-id="c28b6-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c28b6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c28b6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c28b6-131">-WhatIf</span></span>
<span data-ttu-id="c28b6-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c28b6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c28b6-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c28b6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c28b6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28b6-134">CommonParameters</span></span>
<span data-ttu-id="c28b6-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c28b6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28b6-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c28b6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28b6-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c28b6-137">INPUTS</span></span>

### <span data-ttu-id="c28b6-138">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="c28b6-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="c28b6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c28b6-139">OUTPUTS</span></span>

### <span data-ttu-id="c28b6-140">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="c28b6-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="c28b6-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c28b6-141">NOTES</span></span>

<span data-ttu-id="c28b6-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c28b6-142">ALIASES</span></span>

<span data-ttu-id="c28b6-143">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="c28b6-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c28b6-144">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c28b6-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c28b6-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="c28b6-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c28b6-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="c28b6-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c28b6-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="c28b6-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="c28b6-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="c28b6-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="c28b6-149">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="c28b6-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="c28b6-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="c28b6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c28b6-151">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="c28b6-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="c28b6-152">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c28b6-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="c28b6-153">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c28b6-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="c28b6-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c28b6-154">RELATED LINKS</span></span>

