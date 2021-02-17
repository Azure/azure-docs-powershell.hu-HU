---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207550"
---
# <span data-ttu-id="a1fc6-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="a1fc6-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="a1fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="a1fc6-103">Frissíti a hivatkozási adatkészletet a megadott névvel a megadott előfizetésben, erőforráscsoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="a1fc6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1fc6-104">SYNTAX</span></span>

### <span data-ttu-id="a1fc6-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1fc6-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a1fc6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a1fc6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a1fc6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1fc6-107">DESCRIPTION</span></span>
<span data-ttu-id="a1fc6-108">Frissíti a hivatkozási adatkészletet a megadott névvel a megadott előfizetésben, erőforráscsoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="a1fc6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1fc6-109">EXAMPLES</span></span>

### <span data-ttu-id="a1fc6-110">1. példa: Egy megadott hivatkozási adatkészlet frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="a1fc6-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a1fc6-111">Ez a parancs frissíti a megadott hivatkozási adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="a1fc6-112">2. példa: Egy megadott hivatkozási adatkészlet frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="a1fc6-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="a1fc6-113">Ez a parancs frissíti a megadott hivatkozási adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="a1fc6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1fc6-114">PARAMETERS</span></span>

### <span data-ttu-id="a1fc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1fc6-115">-DefaultProfile</span></span>
<span data-ttu-id="a1fc6-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1fc6-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a1fc6-117">-EnvironmentName</span></span>
<span data-ttu-id="a1fc6-118">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="a1fc6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1fc6-119">-InputObject</span></span>
<span data-ttu-id="a1fc6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a1fc6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a1fc6-121">-Name</span></span>
<span data-ttu-id="a1fc6-122">A megadott környezethez társított Time Series Insights hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="a1fc6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1fc6-123">-ResourceGroupName</span></span>
<span data-ttu-id="a1fc6-124">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a1fc6-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1fc6-125">-SubscriptionId</span></span>
<span data-ttu-id="a1fc6-126">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a1fc6-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1fc6-127">-Tag</span></span>
<span data-ttu-id="a1fc6-128">A hivatkozási adatkészlet további tulajdonságainak kulcsértékei.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="a1fc6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1fc6-129">-Confirm</span></span>
<span data-ttu-id="a1fc6-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1fc6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1fc6-131">-WhatIf</span></span>
<span data-ttu-id="a1fc6-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1fc6-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1fc6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1fc6-134">CommonParameters</span></span>
<span data-ttu-id="a1fc6-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1fc6-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1fc6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1fc6-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1fc6-137">INPUTS</span></span>

### <span data-ttu-id="a1fc6-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a1fc6-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a1fc6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1fc6-139">OUTPUTS</span></span>

### <span data-ttu-id="a1fc6-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="a1fc6-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="a1fc6-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1fc6-141">NOTES</span></span>

<span data-ttu-id="a1fc6-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a1fc6-142">ALIASES</span></span>

<span data-ttu-id="a1fc6-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a1fc6-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1fc6-144">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1fc6-145">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1fc6-146">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a1fc6-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a1fc6-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a1fc6-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="a1fc6-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a1fc6-149">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a1fc6-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a1fc6-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a1fc6-151">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a1fc6-152">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a1fc6-153">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a1fc6-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a1fc6-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1fc6-154">RELATED LINKS</span></span>

