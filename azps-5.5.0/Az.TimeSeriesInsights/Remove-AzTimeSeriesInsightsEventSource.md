---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149827"
---
# <span data-ttu-id="85fc8-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="85fc8-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="85fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="85fc8-103">A megadott nevű eseményforrás törlése a megadott előfizetésben, erőforráscsoportban és környezetben</span><span class="sxs-lookup"><span data-stu-id="85fc8-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="85fc8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="85fc8-104">SYNTAX</span></span>

### <span data-ttu-id="85fc8-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="85fc8-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="85fc8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="85fc8-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="85fc8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="85fc8-107">DESCRIPTION</span></span>
<span data-ttu-id="85fc8-108">Törli a megadott nevű eseményforrást a megadott előfizetésben, erőforráscsoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="85fc8-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="85fc8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="85fc8-109">EXAMPLES</span></span>

### <span data-ttu-id="85fc8-110">1. példa: Egy megadott eseményforrás eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="85fc8-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="85fc8-111">Ezzel eltávolít egy adott eseményforrást.</span><span class="sxs-lookup"><span data-stu-id="85fc8-111">This removes a specific event source.</span></span>

### <span data-ttu-id="85fc8-112">2. példa: Egy megadott eseményforrás eltávolítása objektum alapján</span><span class="sxs-lookup"><span data-stu-id="85fc8-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="85fc8-113">Ezzel eltávolít egy adott eseményforrást.</span><span class="sxs-lookup"><span data-stu-id="85fc8-113">This removes a specific event source.</span></span>

## <span data-ttu-id="85fc8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85fc8-114">PARAMETERS</span></span>

### <span data-ttu-id="85fc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85fc8-115">-DefaultProfile</span></span>
<span data-ttu-id="85fc8-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85fc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85fc8-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="85fc8-117">-EnvironmentName</span></span>
<span data-ttu-id="85fc8-118">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="85fc8-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="85fc8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85fc8-119">-InputObject</span></span>
<span data-ttu-id="85fc8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="85fc8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="85fc8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="85fc8-121">-Name</span></span>
<span data-ttu-id="85fc8-122">A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="85fc8-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="85fc8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85fc8-123">-PassThru</span></span>
<span data-ttu-id="85fc8-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="85fc8-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="85fc8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85fc8-125">-ResourceGroupName</span></span>
<span data-ttu-id="85fc8-126">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="85fc8-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="85fc8-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85fc8-127">-SubscriptionId</span></span>
<span data-ttu-id="85fc8-128">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="85fc8-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="85fc8-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85fc8-129">-Confirm</span></span>
<span data-ttu-id="85fc8-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="85fc8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85fc8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85fc8-131">-WhatIf</span></span>
<span data-ttu-id="85fc8-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="85fc8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85fc8-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="85fc8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85fc8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85fc8-134">CommonParameters</span></span>
<span data-ttu-id="85fc8-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85fc8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85fc8-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85fc8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85fc8-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85fc8-137">INPUTS</span></span>

### <span data-ttu-id="85fc8-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="85fc8-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="85fc8-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85fc8-139">OUTPUTS</span></span>

### <span data-ttu-id="85fc8-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85fc8-140">System.Boolean</span></span>

## <span data-ttu-id="85fc8-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="85fc8-141">NOTES</span></span>

<span data-ttu-id="85fc8-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="85fc8-142">ALIASES</span></span>

<span data-ttu-id="85fc8-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="85fc8-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="85fc8-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="85fc8-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85fc8-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="85fc8-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="85fc8-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="85fc8-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="85fc8-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="85fc8-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="85fc8-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="85fc8-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="85fc8-149">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="85fc8-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="85fc8-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="85fc8-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="85fc8-151">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="85fc8-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="85fc8-152">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="85fc8-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="85fc8-153">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="85fc8-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="85fc8-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85fc8-154">RELATED LINKS</span></span>

