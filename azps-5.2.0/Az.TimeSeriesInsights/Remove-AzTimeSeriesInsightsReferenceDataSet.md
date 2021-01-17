---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 56173c8ca384c817912395a536583fb26e9dfa76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324572"
---
# <span data-ttu-id="a2713-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="a2713-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="a2713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2713-102">SYNOPSIS</span></span>
<span data-ttu-id="a2713-103">A megadott nevű hivatkozási adatkészlet törlése a megadott előfizetésben, erőforráscsoportban és környezetben</span><span class="sxs-lookup"><span data-stu-id="a2713-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="a2713-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2713-104">SYNTAX</span></span>

### <span data-ttu-id="a2713-105">Törlés (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2713-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2713-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a2713-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a2713-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2713-107">DESCRIPTION</span></span>
<span data-ttu-id="a2713-108">A megadott nevű hivatkozási adatkészlet törlése a megadott előfizetésben, erőforráscsoportban és környezetben</span><span class="sxs-lookup"><span data-stu-id="a2713-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="a2713-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2713-109">EXAMPLES</span></span>

### <span data-ttu-id="a2713-110">1. példa: Egy megadott hivatkozási adatkészlet eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="a2713-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="a2713-111">Ez a parancs eltávolít egy megadott hivatkozási adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="a2713-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="a2713-112">2. példa: Egy megadott hivatkozási adatkészlet eltávolítása objektum szerint</span><span class="sxs-lookup"><span data-stu-id="a2713-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="a2713-113">Ez a parancs eltávolít egy megadott hivatkozási adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="a2713-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="a2713-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2713-114">PARAMETERS</span></span>

### <span data-ttu-id="a2713-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2713-115">-DefaultProfile</span></span>
<span data-ttu-id="a2713-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2713-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2713-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a2713-117">-EnvironmentName</span></span>
<span data-ttu-id="a2713-118">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="a2713-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="a2713-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2713-119">-InputObject</span></span>
<span data-ttu-id="a2713-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a2713-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a2713-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a2713-121">-Name</span></span>
<span data-ttu-id="a2713-122">A megadott környezethez társított Time Series Insights hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="a2713-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2713-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2713-123">-PassThru</span></span>
<span data-ttu-id="a2713-124">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="a2713-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a2713-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2713-125">-ResourceGroupName</span></span>
<span data-ttu-id="a2713-126">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2713-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a2713-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2713-127">-SubscriptionId</span></span>
<span data-ttu-id="a2713-128">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a2713-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a2713-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2713-129">-Confirm</span></span>
<span data-ttu-id="a2713-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a2713-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2713-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2713-131">-WhatIf</span></span>
<span data-ttu-id="a2713-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a2713-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2713-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2713-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2713-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2713-134">CommonParameters</span></span>
<span data-ttu-id="a2713-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2713-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2713-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2713-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2713-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2713-137">INPUTS</span></span>

### <span data-ttu-id="a2713-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a2713-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a2713-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2713-139">OUTPUTS</span></span>

### <span data-ttu-id="a2713-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2713-140">System.Boolean</span></span>

## <span data-ttu-id="a2713-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2713-141">NOTES</span></span>

<span data-ttu-id="a2713-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a2713-142">ALIASES</span></span>

<span data-ttu-id="a2713-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a2713-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a2713-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a2713-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2713-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2713-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a2713-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a2713-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a2713-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="a2713-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a2713-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="a2713-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a2713-149">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a2713-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a2713-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a2713-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a2713-151">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="a2713-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a2713-152">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2713-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a2713-153">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a2713-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a2713-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2713-154">RELATED LINKS</span></span>

