---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017455"
---
# <span data-ttu-id="30d95-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="30d95-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="30d95-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30d95-102">SYNOPSIS</span></span>
<span data-ttu-id="30d95-103">A megadott nevű eseményforrás törlése a megadott előfizetésből, erőforrás csoportból és környezetből</span><span class="sxs-lookup"><span data-stu-id="30d95-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="30d95-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30d95-104">SYNTAX</span></span>

### <span data-ttu-id="30d95-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30d95-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="30d95-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="30d95-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30d95-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="30d95-107">DESCRIPTION</span></span>
<span data-ttu-id="30d95-108">A megadott nevű eseményforrás törlése a megadott előfizetésből, erőforrás csoportból és környezetből</span><span class="sxs-lookup"><span data-stu-id="30d95-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="30d95-109">Példák</span><span class="sxs-lookup"><span data-stu-id="30d95-109">EXAMPLES</span></span>

### <span data-ttu-id="30d95-110">1. példa: megadott eseményforrás eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="30d95-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="30d95-111">Ez egy adott eseményforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="30d95-111">This removes a specific event source.</span></span>

### <span data-ttu-id="30d95-112">2. példa: meghatározott eseményforrás eltávolítása objektumból</span><span class="sxs-lookup"><span data-stu-id="30d95-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="30d95-113">Ez egy adott eseményforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="30d95-113">This removes a specific event source.</span></span>

## <span data-ttu-id="30d95-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30d95-114">PARAMETERS</span></span>

### <span data-ttu-id="30d95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d95-115">-DefaultProfile</span></span>
<span data-ttu-id="30d95-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30d95-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30d95-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="30d95-117">-EnvironmentName</span></span>
<span data-ttu-id="30d95-118">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="30d95-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d95-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30d95-119">-InputObject</span></span>
<span data-ttu-id="30d95-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="30d95-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30d95-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="30d95-121">-Name</span></span>
<span data-ttu-id="30d95-122">A megadott környezethez társított idősorozat-adatforrások neve.</span><span class="sxs-lookup"><span data-stu-id="30d95-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d95-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30d95-123">-PassThru</span></span>
<span data-ttu-id="30d95-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="30d95-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="30d95-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d95-125">-ResourceGroupName</span></span>
<span data-ttu-id="30d95-126">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="30d95-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d95-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30d95-127">-SubscriptionId</span></span>
<span data-ttu-id="30d95-128">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="30d95-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d95-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="30d95-129">-Confirm</span></span>
<span data-ttu-id="30d95-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="30d95-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30d95-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30d95-131">-WhatIf</span></span>
<span data-ttu-id="30d95-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="30d95-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30d95-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30d95-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30d95-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d95-134">CommonParameters</span></span>
<span data-ttu-id="30d95-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30d95-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d95-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="30d95-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d95-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30d95-137">INPUTS</span></span>

### <span data-ttu-id="30d95-138">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="30d95-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="30d95-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30d95-139">OUTPUTS</span></span>

### <span data-ttu-id="30d95-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="30d95-140">System.Boolean</span></span>

## <span data-ttu-id="30d95-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30d95-141">NOTES</span></span>

<span data-ttu-id="30d95-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="30d95-142">ALIASES</span></span>

<span data-ttu-id="30d95-143">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="30d95-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="30d95-144">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="30d95-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="30d95-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="30d95-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="30d95-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="30d95-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="30d95-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="30d95-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="30d95-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="30d95-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="30d95-149">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="30d95-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="30d95-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="30d95-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="30d95-151">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="30d95-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="30d95-152">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="30d95-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="30d95-153">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="30d95-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="30d95-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30d95-154">RELATED LINKS</span></span>

