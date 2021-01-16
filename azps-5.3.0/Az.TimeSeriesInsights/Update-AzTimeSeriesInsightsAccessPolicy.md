---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383065"
---
# <span data-ttu-id="0375d-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0375d-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="0375d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0375d-102">SYNOPSIS</span></span>
<span data-ttu-id="0375d-103">Frissíti a hozzáférési házirendet a megadott névvel a megadott előfizetésben, erőforráscsoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="0375d-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="0375d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0375d-104">SYNTAX</span></span>

### <span data-ttu-id="0375d-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0375d-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0375d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0375d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0375d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0375d-107">DESCRIPTION</span></span>
<span data-ttu-id="0375d-108">Frissíti a hozzáférési házirendet a megadott névvel a megadott előfizetésben, erőforráscsoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="0375d-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="0375d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0375d-109">EXAMPLES</span></span>

### <span data-ttu-id="0375d-110">1. példa: Egy megadott hozzáférési házirend frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="0375d-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="0375d-111">Ez a parancs frissíti a megadott hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="0375d-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="0375d-112">2. példa: Megadott hozzáférési házirend frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="0375d-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="0375d-113">Ez a parancs frissíti a megadott hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="0375d-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="0375d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0375d-114">PARAMETERS</span></span>

### <span data-ttu-id="0375d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0375d-115">-DefaultProfile</span></span>
<span data-ttu-id="0375d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0375d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0375d-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0375d-117">-Description</span></span>
<span data-ttu-id="0375d-118">A hozzáférési házirend leírása.</span><span class="sxs-lookup"><span data-stu-id="0375d-118">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0375d-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="0375d-119">-EnvironmentName</span></span>
<span data-ttu-id="0375d-120">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="0375d-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="0375d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0375d-121">-InputObject</span></span>
<span data-ttu-id="0375d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0375d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0375d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0375d-123">-Name</span></span>
<span data-ttu-id="0375d-124">A megadott környezethez társított Time Series Insights hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="0375d-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0375d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0375d-125">-ResourceGroupName</span></span>
<span data-ttu-id="0375d-126">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0375d-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="0375d-127">-Szerepkör</span><span class="sxs-lookup"><span data-stu-id="0375d-127">-Role</span></span>
<span data-ttu-id="0375d-128">A környezetben hozzárendelt szerepkörök listája.</span><span class="sxs-lookup"><span data-stu-id="0375d-128">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0375d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0375d-129">-SubscriptionId</span></span>
<span data-ttu-id="0375d-130">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0375d-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0375d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0375d-131">-Confirm</span></span>
<span data-ttu-id="0375d-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0375d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0375d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0375d-133">-WhatIf</span></span>
<span data-ttu-id="0375d-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0375d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0375d-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0375d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0375d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0375d-136">CommonParameters</span></span>
<span data-ttu-id="0375d-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0375d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0375d-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0375d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0375d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0375d-139">INPUTS</span></span>

### <span data-ttu-id="0375d-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="0375d-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="0375d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0375d-141">OUTPUTS</span></span>

### <span data-ttu-id="0375d-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="0375d-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="0375d-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0375d-143">NOTES</span></span>

<span data-ttu-id="0375d-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0375d-144">ALIASES</span></span>

<span data-ttu-id="0375d-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="0375d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0375d-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="0375d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0375d-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0375d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0375d-148">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0375d-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0375d-149">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="0375d-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="0375d-150">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="0375d-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="0375d-151">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0375d-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="0375d-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0375d-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0375d-153">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="0375d-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="0375d-154">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0375d-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="0375d-155">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0375d-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="0375d-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0375d-156">RELATED LINKS</span></span>

