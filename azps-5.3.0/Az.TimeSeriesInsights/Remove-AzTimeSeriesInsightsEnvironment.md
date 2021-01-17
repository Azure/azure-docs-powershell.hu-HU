---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479305"
---
# <span data-ttu-id="386e5-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="386e5-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="386e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="386e5-102">SYNOPSIS</span></span>
<span data-ttu-id="386e5-103">Törli a megadott nevű környezetet a megadott előfizetési és erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="386e5-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="386e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="386e5-104">SYNTAX</span></span>

### <span data-ttu-id="386e5-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="386e5-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="386e5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="386e5-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="386e5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="386e5-107">DESCRIPTION</span></span>
<span data-ttu-id="386e5-108">Törli a megadott nevű környezetet a megadott előfizetési és erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="386e5-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="386e5-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="386e5-109">EXAMPLES</span></span>

### <span data-ttu-id="386e5-110">1. példa: Idősorok elemzési környezetének eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="386e5-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="386e5-111">Ez a parancs eltávolítja az idősorok elemzési környezetét.</span><span class="sxs-lookup"><span data-stu-id="386e5-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="386e5-112">2. példa: Idősorok elemzési környezetének eltávolítása objektumról objektumra</span><span class="sxs-lookup"><span data-stu-id="386e5-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="386e5-113">Ez a parancs eltávolítja az idősorok elemzési környezetét.</span><span class="sxs-lookup"><span data-stu-id="386e5-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="386e5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="386e5-114">PARAMETERS</span></span>

### <span data-ttu-id="386e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386e5-115">-DefaultProfile</span></span>
<span data-ttu-id="386e5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="386e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="386e5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="386e5-117">-InputObject</span></span>
<span data-ttu-id="386e5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="386e5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="386e5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="386e5-119">-Name</span></span>
<span data-ttu-id="386e5-120">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="386e5-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="386e5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="386e5-121">-PassThru</span></span>
<span data-ttu-id="386e5-122">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="386e5-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="386e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="386e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="386e5-124">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="386e5-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="386e5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="386e5-125">-SubscriptionId</span></span>
<span data-ttu-id="386e5-126">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="386e5-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="386e5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="386e5-127">-Confirm</span></span>
<span data-ttu-id="386e5-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="386e5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="386e5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="386e5-129">-WhatIf</span></span>
<span data-ttu-id="386e5-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="386e5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="386e5-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="386e5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="386e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386e5-132">CommonParameters</span></span>
<span data-ttu-id="386e5-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="386e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="386e5-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="386e5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386e5-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="386e5-135">INPUTS</span></span>

### <span data-ttu-id="386e5-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="386e5-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="386e5-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="386e5-137">OUTPUTS</span></span>

### <span data-ttu-id="386e5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="386e5-138">System.Boolean</span></span>

## <span data-ttu-id="386e5-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="386e5-139">NOTES</span></span>

<span data-ttu-id="386e5-140">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="386e5-140">ALIASES</span></span>

<span data-ttu-id="386e5-141">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="386e5-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="386e5-142">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="386e5-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="386e5-143">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="386e5-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="386e5-144">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="386e5-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="386e5-145">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="386e5-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="386e5-146">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="386e5-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="386e5-147">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="386e5-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="386e5-148">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="386e5-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="386e5-149">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="386e5-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="386e5-150">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="386e5-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="386e5-151">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="386e5-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="386e5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="386e5-152">RELATED LINKS</span></span>

