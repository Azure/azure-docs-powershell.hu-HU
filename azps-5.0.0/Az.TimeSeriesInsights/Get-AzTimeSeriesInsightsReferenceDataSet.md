---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187907"
---
# <span data-ttu-id="4dd7b-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="4dd7b-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="4dd7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4dd7b-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd7b-103">A megadott nevű hivatkozási adatkészletet kapja meg a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="4dd7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4dd7b-104">SYNTAX</span></span>

### <span data-ttu-id="4dd7b-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4dd7b-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4dd7b-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="4dd7b-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4dd7b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4dd7b-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4dd7b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4dd7b-108">DESCRIPTION</span></span>
<span data-ttu-id="4dd7b-109">A megadott nevű hivatkozási adatkészletet kapja meg a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="4dd7b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4dd7b-110">EXAMPLES</span></span>

### <span data-ttu-id="4dd7b-111">1. példa: az összes hivatkozási adathalmaz listázása a megadott környezetben</span><span class="sxs-lookup"><span data-stu-id="4dd7b-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="4dd7b-112">Ez a parancs felsorolja az összes hivatkozási adatkészletet a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="4dd7b-113">2. példa: megadott hivatkozási adatkészlet beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="4dd7b-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="4dd7b-114">Ez a parancs a megadott hivatkozási adatkészletet kapja.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="4dd7b-115">3. példa: az adott hivatkozási adatkészletet objektum alapján adja meg</span><span class="sxs-lookup"><span data-stu-id="4dd7b-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="4dd7b-116">Ez a parancs a megadott hivatkozási adatkészletet kapja.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="4dd7b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4dd7b-117">PARAMETERS</span></span>

### <span data-ttu-id="4dd7b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd7b-118">-DefaultProfile</span></span>
<span data-ttu-id="4dd7b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dd7b-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="4dd7b-120">-EnvironmentName</span></span>
<span data-ttu-id="4dd7b-121">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="4dd7b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dd7b-122">-InputObject</span></span>
<span data-ttu-id="4dd7b-123">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4dd7b-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4dd7b-124">-Name</span></span>
<span data-ttu-id="4dd7b-125">A megadott környezethez társított idősorokban szereplő hivatkozási adathalmaz neve.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="4dd7b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd7b-126">-ResourceGroupName</span></span>
<span data-ttu-id="4dd7b-127">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4dd7b-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="4dd7b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4dd7b-128">-SubscriptionId</span></span>
<span data-ttu-id="4dd7b-129">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="4dd7b-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="4dd7b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd7b-130">CommonParameters</span></span>
<span data-ttu-id="4dd7b-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4dd7b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd7b-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd7b-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dd7b-133">INPUTS</span></span>

### <span data-ttu-id="4dd7b-134">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="4dd7b-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="4dd7b-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dd7b-135">OUTPUTS</span></span>

### <span data-ttu-id="4dd7b-136">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="4dd7b-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="4dd7b-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4dd7b-137">NOTES</span></span>

<span data-ttu-id="4dd7b-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4dd7b-138">ALIASES</span></span>

<span data-ttu-id="4dd7b-139">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="4dd7b-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4dd7b-140">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4dd7b-141">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4dd7b-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="4dd7b-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4dd7b-143">`[AccessPolicyName <String>]`: A hozzáférési házirend neve.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="4dd7b-144">`[EnvironmentName <String>]`: A környezet neve</span><span class="sxs-lookup"><span data-stu-id="4dd7b-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="4dd7b-145">`[EventSourceName <String>]`: A megadott környezethez társított idősorozat-adatforrások neve</span><span class="sxs-lookup"><span data-stu-id="4dd7b-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="4dd7b-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="4dd7b-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4dd7b-147">`[ReferenceDataSetName <String>]`: A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="4dd7b-148">`[ResourceGroupName <String>]`: Egy Azure-erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="4dd7b-149">`[SubscriptionId <String>]`: Azure előfizetés-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4dd7b-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="4dd7b-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4dd7b-150">RELATED LINKS</span></span>

