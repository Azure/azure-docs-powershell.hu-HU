---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180716"
---
# <span data-ttu-id="5e4c7-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="5e4c7-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="5e4c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4c7-103">A megadott nevű hivatkozási adatkészletet frissíti a megadott előfizetésben, erőforrás csoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="5e4c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e4c7-104">SYNTAX</span></span>

### <span data-ttu-id="5e4c7-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e4c7-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e4c7-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5e4c7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e4c7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e4c7-107">DESCRIPTION</span></span>
<span data-ttu-id="5e4c7-108">A megadott nevű hivatkozási adatkészletet frissíti a megadott előfizetésben, erőforrás csoportban és környezetben.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="5e4c7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5e4c7-109">EXAMPLES</span></span>

### <span data-ttu-id="5e4c7-110">Példa 1: megadott hivatkozási adathalmaz frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="5e4c7-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="5e4c7-111">Ez a parancs frissíti a megadott hivatkozási adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="5e4c7-112">2. példa: a megadott hivatkozási adatkészlet frissítése objektum szerint</span><span class="sxs-lookup"><span data-stu-id="5e4c7-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="5e4c7-113">Ez a parancs frissíti a megadott hivatkozási adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="5e4c7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e4c7-114">PARAMETERS</span></span>

### <span data-ttu-id="5e4c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e4c7-115">-DefaultProfile</span></span>
<span data-ttu-id="5e4c7-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e4c7-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="5e4c7-117">-EnvironmentName</span></span>
<span data-ttu-id="5e4c7-118">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="5e4c7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e4c7-119">-InputObject</span></span>
<span data-ttu-id="5e4c7-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e4c7-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5e4c7-121">-Name</span></span>
<span data-ttu-id="5e4c7-122">A megadott környezethez társított idősorokban szereplő hivatkozási adathalmaz neve.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="5e4c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e4c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e4c7-124">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5e4c7-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="5e4c7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e4c7-125">-SubscriptionId</span></span>
<span data-ttu-id="5e4c7-126">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="5e4c7-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5e4c7-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="5e4c7-127">-Tag</span></span>
<span data-ttu-id="5e4c7-128">A hivatkozási adatkészlet további tulajdonságainak kulcs-érték párjai</span><span class="sxs-lookup"><span data-stu-id="5e4c7-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="5e4c7-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5e4c7-129">-Confirm</span></span>
<span data-ttu-id="5e4c7-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e4c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e4c7-131">-WhatIf</span></span>
<span data-ttu-id="5e4c7-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e4c7-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e4c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4c7-134">CommonParameters</span></span>
<span data-ttu-id="5e4c7-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e4c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e4c7-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4c7-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e4c7-137">INPUTS</span></span>

### <span data-ttu-id="5e4c7-138">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="5e4c7-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="5e4c7-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e4c7-139">OUTPUTS</span></span>

### <span data-ttu-id="5e4c7-140">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="5e4c7-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="5e4c7-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e4c7-141">NOTES</span></span>

<span data-ttu-id="5e4c7-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5e4c7-142">ALIASES</span></span>

<span data-ttu-id="5e4c7-143">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="5e4c7-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e4c7-144">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e4c7-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e4c7-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="5e4c7-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e4c7-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="5e4c7-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="5e4c7-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="5e4c7-149">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="5e4c7-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="5e4c7-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="5e4c7-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e4c7-151">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="5e4c7-152">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="5e4c7-153">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5e4c7-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="5e4c7-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e4c7-154">RELATED LINKS</span></span>

