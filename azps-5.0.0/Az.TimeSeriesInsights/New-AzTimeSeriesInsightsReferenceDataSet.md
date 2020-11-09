---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303266"
---
# <span data-ttu-id="78faf-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="78faf-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="78faf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78faf-102">SYNOPSIS</span></span>
<span data-ttu-id="78faf-103">Hivatkozási adathalmaz létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="78faf-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="78faf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78faf-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="78faf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="78faf-105">DESCRIPTION</span></span>
<span data-ttu-id="78faf-106">Hivatkozási adathalmaz létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="78faf-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="78faf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="78faf-107">EXAMPLES</span></span>

### <span data-ttu-id="78faf-108">1. példa: a hivatkozási adathalmaz létrehozása meghatározott környezethez</span><span class="sxs-lookup"><span data-stu-id="78faf-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="78faf-109">Ez a parancs egy bizonyos környezethez hivatkozási adatkészletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="78faf-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="78faf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78faf-110">PARAMETERS</span></span>

### <span data-ttu-id="78faf-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="78faf-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="78faf-112">A hivatkozás az adathalmaz fő összehasonlító viselkedését a tulajdonság használatával állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="78faf-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="78faf-113">Alapértelmezés szerint az érték "sorszám", ami azt jelenti, hogy a kis-és nagybetűk összehasonlítása az eseményekkel való kapcsolódáskor vagy új hivatkozási adatok hozzáadásakor történik.</span><span class="sxs-lookup"><span data-stu-id="78faf-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="78faf-114">Ha a "OrdinalIgnoreCase" érték van beállítva, akkor a rendszer a kis-és nagybetűket is használja.</span><span class="sxs-lookup"><span data-stu-id="78faf-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.DataStringComparisonBehavior
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78faf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78faf-115">-DefaultProfile</span></span>
<span data-ttu-id="78faf-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78faf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78faf-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="78faf-117">-EnvironmentName</span></span>
<span data-ttu-id="78faf-118">A megadott erőforráscsoport által társított idősorozat-adatelemzési környezet neve.</span><span class="sxs-lookup"><span data-stu-id="78faf-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78faf-119">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="78faf-119">-KeyProperty</span></span>
<span data-ttu-id="78faf-120">A hivatkozási adatkészlet fő tulajdonságainak listája.</span><span class="sxs-lookup"><span data-stu-id="78faf-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="78faf-121">A kivitelezéshez tekintse meg a következőt: megjegyzések szakasz a tulajdonságok tulajdonságainak megjelenítéséhez, és hozzon létre egy kivonatoló táblázatot.</span><span class="sxs-lookup"><span data-stu-id="78faf-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetKeyProperty[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78faf-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="78faf-122">-Location</span></span>
<span data-ttu-id="78faf-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="78faf-123">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78faf-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="78faf-124">-Name</span></span>
<span data-ttu-id="78faf-125">A hivatkozás adatkészletének neve.</span><span class="sxs-lookup"><span data-stu-id="78faf-125">Name of the reference data set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78faf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78faf-126">-ResourceGroupName</span></span>
<span data-ttu-id="78faf-127">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="78faf-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78faf-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78faf-128">-SubscriptionId</span></span>
<span data-ttu-id="78faf-129">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="78faf-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78faf-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="78faf-130">-Tag</span></span>
<span data-ttu-id="78faf-131">Az erőforrás további tulajdonságainak kulcs-érték párjai</span><span class="sxs-lookup"><span data-stu-id="78faf-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="78faf-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78faf-132">-Confirm</span></span>
<span data-ttu-id="78faf-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78faf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78faf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78faf-134">-WhatIf</span></span>
<span data-ttu-id="78faf-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="78faf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78faf-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78faf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78faf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78faf-137">CommonParameters</span></span>
<span data-ttu-id="78faf-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78faf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78faf-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="78faf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78faf-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78faf-140">INPUTS</span></span>

## <span data-ttu-id="78faf-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78faf-141">OUTPUTS</span></span>

### <span data-ttu-id="78faf-142">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="78faf-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="78faf-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78faf-143">NOTES</span></span>

<span data-ttu-id="78faf-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="78faf-144">ALIASES</span></span>

<span data-ttu-id="78faf-145">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="78faf-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="78faf-146">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="78faf-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="78faf-147">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="78faf-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="78faf-148">IReferenceDataSetKeyProperty <[] >: a hivatkozási adatkészlet fő tulajdonságainak listája.</span><span class="sxs-lookup"><span data-stu-id="78faf-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="78faf-149">`[Name <String>]`: A Key tulajdonság neve.</span><span class="sxs-lookup"><span data-stu-id="78faf-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="78faf-150">`[Type <ReferenceDataKeyPropertyType?>]`: A kulcs tulajdonság típusa.</span><span class="sxs-lookup"><span data-stu-id="78faf-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="78faf-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78faf-151">RELATED LINKS</span></span>

