---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 56173c8ca384c817912395a536583fb26e9dfa76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180718"
---
# <span data-ttu-id="a8694-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="a8694-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="a8694-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8694-102">SYNOPSIS</span></span>
<span data-ttu-id="a8694-103">A megadott nevű hivatkozási adatok törlése a megadott előfizetéshez, erőforrás csoporthoz és környezethez</span><span class="sxs-lookup"><span data-stu-id="a8694-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="a8694-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8694-104">SYNTAX</span></span>

### <span data-ttu-id="a8694-105">Delete (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8694-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a8694-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a8694-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a8694-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8694-107">DESCRIPTION</span></span>
<span data-ttu-id="a8694-108">A megadott nevű hivatkozási adatok törlése a megadott előfizetéshez, erőforrás csoporthoz és környezethez</span><span class="sxs-lookup"><span data-stu-id="a8694-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="a8694-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a8694-109">EXAMPLES</span></span>

### <span data-ttu-id="a8694-110">Példa 1: megadott hivatkozási adatkészlet eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="a8694-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="a8694-111">Ez a parancs eltávolítja a megadott hivatkozási adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="a8694-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="a8694-112">2. példa: a megadott hivatkozási adatkészlet eltávolítása objektum alapján</span><span class="sxs-lookup"><span data-stu-id="a8694-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="a8694-113">Ez a parancs eltávolítja a megadott hivatkozási adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="a8694-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="a8694-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8694-114">PARAMETERS</span></span>

### <span data-ttu-id="a8694-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8694-115">-DefaultProfile</span></span>
<span data-ttu-id="a8694-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8694-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8694-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a8694-117">-EnvironmentName</span></span>
<span data-ttu-id="a8694-118">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="a8694-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="a8694-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8694-119">-InputObject</span></span>
<span data-ttu-id="a8694-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a8694-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a8694-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8694-121">-Name</span></span>
<span data-ttu-id="a8694-122">A megadott környezethez társított idősorokban szereplő hivatkozási adathalmaz neve.</span><span class="sxs-lookup"><span data-stu-id="a8694-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="a8694-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8694-123">-PassThru</span></span>
<span data-ttu-id="a8694-124">Igaz érték visszaadása a parancs sikeressége után</span><span class="sxs-lookup"><span data-stu-id="a8694-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a8694-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8694-125">-ResourceGroupName</span></span>
<span data-ttu-id="a8694-126">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a8694-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="a8694-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8694-127">-SubscriptionId</span></span>
<span data-ttu-id="a8694-128">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="a8694-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a8694-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8694-129">-Confirm</span></span>
<span data-ttu-id="a8694-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8694-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8694-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8694-131">-WhatIf</span></span>
<span data-ttu-id="a8694-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8694-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8694-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8694-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8694-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8694-134">CommonParameters</span></span>
<span data-ttu-id="a8694-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8694-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8694-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a8694-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8694-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8694-137">INPUTS</span></span>

### <span data-ttu-id="a8694-138">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="a8694-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="a8694-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8694-139">OUTPUTS</span></span>

### <span data-ttu-id="a8694-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8694-140">System.Boolean</span></span>

## <span data-ttu-id="a8694-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8694-141">NOTES</span></span>

<span data-ttu-id="a8694-142">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a8694-142">ALIASES</span></span>

<span data-ttu-id="a8694-143">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="a8694-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a8694-144">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="a8694-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a8694-145">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="a8694-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a8694-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="a8694-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a8694-147">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="a8694-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="a8694-148">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="a8694-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="a8694-149">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="a8694-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="a8694-150">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a8694-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a8694-151">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="a8694-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="a8694-152">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a8694-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="a8694-153">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a8694-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a8694-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8694-154">RELATED LINKS</span></span>

