---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 1fef5f018791fba9369ce7ab18a4b0c3a2440cc6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918026"
---
# <span data-ttu-id="87029-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="87029-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="87029-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87029-102">SYNOPSIS</span></span>
<span data-ttu-id="87029-103">Beveszi a megadott nevű hivatkozási adatkészletet a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="87029-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="87029-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="87029-104">SYNTAX</span></span>

### <span data-ttu-id="87029-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="87029-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="87029-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="87029-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="87029-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="87029-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="87029-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="87029-108">DESCRIPTION</span></span>
<span data-ttu-id="87029-109">Beveszi a megadott nevű hivatkozási adatkészletet a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="87029-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="87029-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="87029-110">EXAMPLES</span></span>

### <span data-ttu-id="87029-111">1. példa: A megadott környezetben található összes hivatkozási adatkészlet felsorolása</span><span class="sxs-lookup"><span data-stu-id="87029-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="87029-112">Ez a parancs felsorolja a megadott környezetben található összes hivatkozási adatkészletet.</span><span class="sxs-lookup"><span data-stu-id="87029-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="87029-113">2. példa: Megadott hivatkozási adatkészlet lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="87029-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="87029-114">Ez a parancs egy megadott hivatkozási adatkészletet kap.</span><span class="sxs-lookup"><span data-stu-id="87029-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="87029-115">3. példa: Megadott hivatkozási adatkészlet lekérte objektum szerint</span><span class="sxs-lookup"><span data-stu-id="87029-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="87029-116">Ez a parancs egy megadott hivatkozási adatkészletet kap.</span><span class="sxs-lookup"><span data-stu-id="87029-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="87029-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87029-117">PARAMETERS</span></span>

### <span data-ttu-id="87029-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87029-118">-DefaultProfile</span></span>
<span data-ttu-id="87029-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87029-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87029-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="87029-120">-EnvironmentName</span></span>
<span data-ttu-id="87029-121">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="87029-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87029-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87029-122">-InputObject</span></span>
<span data-ttu-id="87029-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="87029-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87029-124">-Name</span><span class="sxs-lookup"><span data-stu-id="87029-124">-Name</span></span>
<span data-ttu-id="87029-125">A megadott környezethez társított Time Series Insights hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="87029-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87029-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87029-126">-ResourceGroupName</span></span>
<span data-ttu-id="87029-127">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="87029-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87029-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87029-128">-SubscriptionId</span></span>
<span data-ttu-id="87029-129">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="87029-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87029-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87029-130">CommonParameters</span></span>
<span data-ttu-id="87029-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87029-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87029-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87029-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87029-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87029-133">INPUTS</span></span>

### <span data-ttu-id="87029-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="87029-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="87029-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87029-135">OUTPUTS</span></span>

### <span data-ttu-id="87029-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="87029-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="87029-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="87029-137">NOTES</span></span>

<span data-ttu-id="87029-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="87029-138">ALIASES</span></span>

<span data-ttu-id="87029-139">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="87029-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87029-140">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="87029-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87029-141">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87029-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87029-142">INPUTOBJECT: <ITimeSeriesInsightsIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="87029-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87029-143">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="87029-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="87029-144">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="87029-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="87029-145">`[EventSourceName <String>]`: A megadott környezethez társított Time Series Insights eseményforrás neve.</span><span class="sxs-lookup"><span data-stu-id="87029-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="87029-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="87029-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87029-147">`[ReferenceDataSetName <String>]`: A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="87029-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="87029-148">`[ResourceGroupName <String>]`: Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="87029-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="87029-149">`[SubscriptionId <String>]`: Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="87029-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="87029-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87029-150">RELATED LINKS</span></span>

