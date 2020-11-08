---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185995"
---
# <span data-ttu-id="e0ff6-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0ff6-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="e0ff6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ff6-103">A megadott néven frissíti a hozzáférési házirendet a megadott előfizetésben, erőforrás csoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="e0ff6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0ff6-104">SYNTAX</span></span>

### <span data-ttu-id="e0ff6-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e0ff6-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e0ff6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e0ff6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0ff6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0ff6-107">DESCRIPTION</span></span>
<span data-ttu-id="e0ff6-108">A megadott néven frissíti a hozzáférési házirendet a megadott előfizetésben, erőforrás csoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="e0ff6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e0ff6-109">EXAMPLES</span></span>

### <span data-ttu-id="e0ff6-110">Példa 1: meghatározott hozzáférési házirend frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="e0ff6-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="e0ff6-111">Ez a parancs frissíti a megadott hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="e0ff6-112">2. példa: meghatározott hozzáférési házirend frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="e0ff6-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="e0ff6-113">Ez a parancs frissíti a megadott hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="e0ff6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0ff6-114">PARAMETERS</span></span>

### <span data-ttu-id="e0ff6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ff6-115">-DefaultProfile</span></span>
<span data-ttu-id="e0ff6-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0ff6-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e0ff6-117">-Description</span></span>
<span data-ttu-id="e0ff6-118">A hozzáférési házirend leírása.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-118">An description of the access policy.</span></span>

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

### <span data-ttu-id="e0ff6-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="e0ff6-119">-EnvironmentName</span></span>
<span data-ttu-id="e0ff6-120">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="e0ff6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0ff6-121">-InputObject</span></span>
<span data-ttu-id="e0ff6-122">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e0ff6-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0ff6-123">-Name</span></span>
<span data-ttu-id="e0ff6-124">A megadott környezethez társított idősorok elérési házirendjének neve.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

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

### <span data-ttu-id="e0ff6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ff6-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0ff6-126">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e0ff6-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="e0ff6-127">-Role (szerepkör)</span><span class="sxs-lookup"><span data-stu-id="e0ff6-127">-Role</span></span>
<span data-ttu-id="e0ff6-128">Azon szerepkörök listája, amelyeket a megbízó a környezetre kiosztott.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-128">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="e0ff6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0ff6-129">-SubscriptionId</span></span>
<span data-ttu-id="e0ff6-130">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="e0ff6-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e0ff6-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0ff6-131">-Confirm</span></span>
<span data-ttu-id="e0ff6-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0ff6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0ff6-133">-WhatIf</span></span>
<span data-ttu-id="e0ff6-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0ff6-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0ff6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ff6-136">CommonParameters</span></span>
<span data-ttu-id="e0ff6-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0ff6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ff6-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ff6-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0ff6-139">INPUTS</span></span>

### <span data-ttu-id="e0ff6-140">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="e0ff6-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="e0ff6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0ff6-141">OUTPUTS</span></span>

### <span data-ttu-id="e0ff6-142">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="e0ff6-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="e0ff6-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0ff6-143">NOTES</span></span>

<span data-ttu-id="e0ff6-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e0ff6-144">ALIASES</span></span>

<span data-ttu-id="e0ff6-145">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="e0ff6-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0ff6-146">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0ff6-147">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0ff6-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="e0ff6-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e0ff6-149">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="e0ff6-150">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="e0ff6-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="e0ff6-151">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="e0ff6-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="e0ff6-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e0ff6-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e0ff6-153">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="e0ff6-154">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="e0ff6-155">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e0ff6-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e0ff6-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0ff6-156">RELATED LINKS</span></span>

