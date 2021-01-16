---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338945"
---
# <span data-ttu-id="65f4e-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="65f4e-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="65f4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="65f4e-103">Törli a megadott nevű eseményforrást a megadott előfizetésben, erőforráscsoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="65f4e-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="65f4e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="65f4e-104">SYNTAX</span></span>

### <span data-ttu-id="65f4e-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65f4e-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="65f4e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="65f4e-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="65f4e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="65f4e-107">DESCRIPTION</span></span>
<span data-ttu-id="65f4e-108">Törli a megadott nevű eseményforrást a megadott előfizetésben, erőforráscsoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="65f4e-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="65f4e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="65f4e-109">EXAMPLES</span></span>

### <span data-ttu-id="65f4e-110">1. példa: Egy megadott eseményforrás eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="65f4e-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="65f4e-111">Ezzel eltávolít egy adott eseményforrást.</span><span class="sxs-lookup"><span data-stu-id="65f4e-111">This removes a specific event source.</span></span>

### <span data-ttu-id="65f4e-112">2. példa: Egy megadott eseményforrás eltávolítása objektum alapján</span><span class="sxs-lookup"><span data-stu-id="65f4e-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="65f4e-113">Ezzel eltávolít egy adott eseményforrást.</span><span class="sxs-lookup"><span data-stu-id="65f4e-113">This removes a specific event source.</span></span>

## <span data-ttu-id="65f4e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65f4e-114">PARAMETERS</span></span>

### <span data-ttu-id="65f4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f4e-115">-DefaultProfile</span></span>
<span data-ttu-id="65f4e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65f4e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65f4e-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="65f4e-117">-EnvironmentName</span></span>
<span data-ttu-id="65f4e-118">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="65f4e-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="65f4e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65f4e-119">-InputObject</span></span>
<span data-ttu-id="65f4e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="65f4e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="65f4e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="65f4e-121">-Name</span></span>
<span data-ttu-id="65f4e-122">A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="65f4e-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="65f4e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65f4e-123">-PassThru</span></span>
<span data-ttu-id="65f4e-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="65f4e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="65f4e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65f4e-125">-ResourceGroupName</span></span>
<span data-ttu-id="65f4e-126">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="65f4e-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="65f4e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65f4e-127">-SubscriptionId</span></span>
<span data-ttu-id="65f4e-128">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="65f4e-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="65f4e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65f4e-129">-Confirm</span></span>
<span data-ttu-id="65f4e-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="65f4e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65f4e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65f4e-131">-WhatIf</span></span>
<span data-ttu-id="65f4e-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="65f4e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65f4e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65f4e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65f4e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f4e-134">CommonParameters</span></span>
<span data-ttu-id="65f4e-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65f4e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f4e-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65f4e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f4e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65f4e-137">INPUTS</span></span>

### <span data-ttu-id="65f4e-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="65f4e-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="65f4e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65f4e-139">OUTPUTS</span></span>

### <span data-ttu-id="65f4e-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65f4e-140">System.Boolean</span></span>

## <span data-ttu-id="65f4e-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="65f4e-141">NOTES</span></span>

<span data-ttu-id="65f4e-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="65f4e-142">ALIASES</span></span>

<span data-ttu-id="65f4e-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="65f4e-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="65f4e-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="65f4e-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="65f4e-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="65f4e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="65f4e-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="65f4e-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="65f4e-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="65f4e-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="65f4e-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="65f4e-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="65f4e-149">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="65f4e-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="65f4e-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="65f4e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="65f4e-151">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="65f4e-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="65f4e-152">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="65f4e-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="65f4e-153">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="65f4e-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="65f4e-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65f4e-154">RELATED LINKS</span></span>

