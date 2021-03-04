---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 9dcce9640500b1fa1aeebea8f5f3169e0a527b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939082"
---
# <span data-ttu-id="e6f1f-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="e6f1f-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="e6f1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f1f-103">Törli a megadott nevű eseményforrást a megadott előfizetésben, erőforráscsoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="e6f1f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6f1f-104">SYNTAX</span></span>

### <span data-ttu-id="e6f1f-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6f1f-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e6f1f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e6f1f-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e6f1f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6f1f-107">DESCRIPTION</span></span>
<span data-ttu-id="e6f1f-108">Törli a megadott nevű eseményforrást a megadott előfizetésben, erőforráscsoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="e6f1f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6f1f-109">EXAMPLES</span></span>

### <span data-ttu-id="e6f1f-110">1. példa: Egy megadott eseményforrás eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="e6f1f-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="e6f1f-111">Ezzel eltávolít egy adott eseményforrást.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-111">This removes a specific event source.</span></span>

### <span data-ttu-id="e6f1f-112">2. példa: Egy megadott eseményforrás eltávolítása objektum alapján</span><span class="sxs-lookup"><span data-stu-id="e6f1f-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="e6f1f-113">Ezzel eltávolít egy adott eseményforrást.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-113">This removes a specific event source.</span></span>

## <span data-ttu-id="e6f1f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6f1f-114">PARAMETERS</span></span>

### <span data-ttu-id="e6f1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f1f-115">-DefaultProfile</span></span>
<span data-ttu-id="e6f1f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6f1f-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e6f1f-117">-EnvironmentName</span></span>
<span data-ttu-id="e6f1f-118">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="e6f1f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6f1f-119">-InputObject</span></span>
<span data-ttu-id="e6f1f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e6f1f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e6f1f-121">-Name</span></span>
<span data-ttu-id="e6f1f-122">A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="e6f1f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6f1f-123">-PassThru</span></span>
<span data-ttu-id="e6f1f-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="e6f1f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e6f1f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f1f-125">-ResourceGroupName</span></span>
<span data-ttu-id="e6f1f-126">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="e6f1f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6f1f-127">-SubscriptionId</span></span>
<span data-ttu-id="e6f1f-128">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e6f1f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6f1f-129">-Confirm</span></span>
<span data-ttu-id="e6f1f-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f1f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f1f-131">-WhatIf</span></span>
<span data-ttu-id="e6f1f-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f1f-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f1f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f1f-134">CommonParameters</span></span>
<span data-ttu-id="e6f1f-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f1f-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6f1f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f1f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6f1f-137">INPUTS</span></span>

### <span data-ttu-id="e6f1f-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e6f1f-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e6f1f-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6f1f-139">OUTPUTS</span></span>

### <span data-ttu-id="e6f1f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6f1f-140">System.Boolean</span></span>

## <span data-ttu-id="e6f1f-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6f1f-141">NOTES</span></span>

<span data-ttu-id="e6f1f-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e6f1f-142">ALIASES</span></span>

<span data-ttu-id="e6f1f-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e6f1f-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e6f1f-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e6f1f-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e6f1f-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e6f1f-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e6f1f-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e6f1f-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="e6f1f-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e6f1f-149">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e6f1f-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e6f1f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e6f1f-151">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e6f1f-152">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e6f1f-153">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e6f1f-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e6f1f-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6f1f-154">RELATED LINKS</span></span>

