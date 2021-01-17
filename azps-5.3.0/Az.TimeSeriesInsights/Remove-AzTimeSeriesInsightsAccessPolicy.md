---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479310"
---
# <span data-ttu-id="89eef-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="89eef-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="89eef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89eef-102">SYNOPSIS</span></span>
<span data-ttu-id="89eef-103">A megadott nevű hozzáférési házirend törlése a megadott előfizetésben, erőforráscsoportban és környezetben</span><span class="sxs-lookup"><span data-stu-id="89eef-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="89eef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89eef-104">SYNTAX</span></span>

### <span data-ttu-id="89eef-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89eef-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="89eef-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="89eef-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="89eef-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89eef-107">DESCRIPTION</span></span>
<span data-ttu-id="89eef-108">A megadott nevű hozzáférési házirend törlése a megadott előfizetésben, erőforráscsoportban és környezetben</span><span class="sxs-lookup"><span data-stu-id="89eef-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="89eef-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89eef-109">EXAMPLES</span></span>

### <span data-ttu-id="89eef-110">1. példa: Egy megadott hozzáférési házirend eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="89eef-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="89eef-111">Ez a parancs eltávolít egy megadott hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="89eef-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="89eef-112">2. példa: Megadott hozzáférési házirend eltávolítása objektum szerint</span><span class="sxs-lookup"><span data-stu-id="89eef-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="89eef-113">Ez a parancs eltávolít egy megadott hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="89eef-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="89eef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89eef-114">PARAMETERS</span></span>

### <span data-ttu-id="89eef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89eef-115">-DefaultProfile</span></span>
<span data-ttu-id="89eef-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89eef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89eef-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="89eef-117">-EnvironmentName</span></span>
<span data-ttu-id="89eef-118">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="89eef-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="89eef-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89eef-119">-InputObject</span></span>
<span data-ttu-id="89eef-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="89eef-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="89eef-121">-Name</span><span class="sxs-lookup"><span data-stu-id="89eef-121">-Name</span></span>
<span data-ttu-id="89eef-122">A megadott környezethez társított Time Series Insights hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="89eef-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89eef-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89eef-123">-PassThru</span></span>
<span data-ttu-id="89eef-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="89eef-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="89eef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89eef-125">-ResourceGroupName</span></span>
<span data-ttu-id="89eef-126">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="89eef-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="89eef-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89eef-127">-SubscriptionId</span></span>
<span data-ttu-id="89eef-128">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="89eef-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="89eef-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89eef-129">-Confirm</span></span>
<span data-ttu-id="89eef-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="89eef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89eef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89eef-131">-WhatIf</span></span>
<span data-ttu-id="89eef-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="89eef-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89eef-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89eef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89eef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89eef-134">CommonParameters</span></span>
<span data-ttu-id="89eef-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89eef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89eef-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89eef-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89eef-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89eef-137">INPUTS</span></span>

### <span data-ttu-id="89eef-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="89eef-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="89eef-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89eef-139">OUTPUTS</span></span>

### <span data-ttu-id="89eef-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89eef-140">System.Boolean</span></span>

## <span data-ttu-id="89eef-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89eef-141">NOTES</span></span>

<span data-ttu-id="89eef-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="89eef-142">ALIASES</span></span>

<span data-ttu-id="89eef-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="89eef-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="89eef-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="89eef-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89eef-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="89eef-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="89eef-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="89eef-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89eef-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="89eef-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="89eef-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="89eef-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="89eef-149">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="89eef-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="89eef-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="89eef-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89eef-151">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="89eef-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="89eef-152">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="89eef-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="89eef-153">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="89eef-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="89eef-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89eef-154">RELATED LINKS</span></span>

