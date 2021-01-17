---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382995"
---
# <span data-ttu-id="e9776-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="e9776-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="e9776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9776-102">SYNOPSIS</span></span>
<span data-ttu-id="e9776-103">Frissíti a hivatkozási adatkészletet a megadott névvel a megadott előfizetésben, erőforráscsoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="e9776-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="e9776-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9776-104">SYNTAX</span></span>

### <span data-ttu-id="e9776-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9776-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e9776-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e9776-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e9776-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9776-107">DESCRIPTION</span></span>
<span data-ttu-id="e9776-108">Frissíti a hivatkozási adatkészletet a megadott névvel a megadott előfizetésben, erőforráscsoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="e9776-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="e9776-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9776-109">EXAMPLES</span></span>

### <span data-ttu-id="e9776-110">1. példa: Egy megadott hivatkozási adatkészlet frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="e9776-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="e9776-111">Ez a parancs frissíti a megadott hivatkozási adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="e9776-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="e9776-112">2. példa: Egy megadott hivatkozási adatkészlet frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="e9776-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="e9776-113">Ez a parancs frissíti a megadott hivatkozási adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="e9776-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="e9776-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9776-114">PARAMETERS</span></span>

### <span data-ttu-id="e9776-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9776-115">-DefaultProfile</span></span>
<span data-ttu-id="e9776-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9776-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9776-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e9776-117">-EnvironmentName</span></span>
<span data-ttu-id="e9776-118">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="e9776-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="e9776-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9776-119">-InputObject</span></span>
<span data-ttu-id="e9776-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e9776-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e9776-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e9776-121">-Name</span></span>
<span data-ttu-id="e9776-122">A megadott környezethez társított Time Series Insights hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="e9776-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9776-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9776-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9776-124">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e9776-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="e9776-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9776-125">-SubscriptionId</span></span>
<span data-ttu-id="e9776-126">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e9776-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e9776-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9776-127">-Tag</span></span>
<span data-ttu-id="e9776-128">A hivatkozási adatkészlet további tulajdonságainak kulcsértékei.</span><span class="sxs-lookup"><span data-stu-id="e9776-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="e9776-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9776-129">-Confirm</span></span>
<span data-ttu-id="e9776-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e9776-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9776-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9776-131">-WhatIf</span></span>
<span data-ttu-id="e9776-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e9776-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9776-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e9776-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9776-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9776-134">CommonParameters</span></span>
<span data-ttu-id="e9776-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9776-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9776-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9776-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9776-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9776-137">INPUTS</span></span>

### <span data-ttu-id="e9776-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e9776-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e9776-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9776-139">OUTPUTS</span></span>

### <span data-ttu-id="e9776-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="e9776-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="e9776-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9776-141">NOTES</span></span>

<span data-ttu-id="e9776-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e9776-142">ALIASES</span></span>

<span data-ttu-id="e9776-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e9776-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e9776-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e9776-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e9776-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e9776-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e9776-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e9776-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e9776-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="e9776-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e9776-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="e9776-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e9776-149">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e9776-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e9776-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e9776-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e9776-151">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="e9776-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e9776-152">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e9776-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e9776-153">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e9776-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e9776-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9776-154">RELATED LINKS</span></span>

