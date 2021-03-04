---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 1c4e0fa2a8e204ee3b0dad160d3cfb54f58b4323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930641"
---
# <span data-ttu-id="c1468-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="c1468-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="c1468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1468-102">SYNOPSIS</span></span>
<span data-ttu-id="c1468-103">Hivatkozási adatkészlet létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="c1468-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="c1468-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c1468-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1468-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c1468-105">DESCRIPTION</span></span>
<span data-ttu-id="c1468-106">Hivatkozási adatkészlet létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="c1468-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="c1468-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c1468-107">EXAMPLES</span></span>

### <span data-ttu-id="c1468-108">1. példa: Hivatkozási adatkészlet létrehozása egy adott környezethez</span><span class="sxs-lookup"><span data-stu-id="c1468-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="c1468-109">Ez a parancs egy adott környezet hivatkozási adatkészletét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="c1468-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="c1468-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1468-110">PARAMETERS</span></span>

### <span data-ttu-id="c1468-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="c1468-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="c1468-112">A hivatkozási adatkészlet kulcs-összehasonlítási viselkedése a tulajdonság használatával beállítható.</span><span class="sxs-lookup"><span data-stu-id="c1468-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="c1468-113">Az érték alapértelmezés szerint "Sorszám" – ez azt jelenti, hogy a program a kis- és nagybetűket megkülönböztetve hasonlítja össze a hivatkozási adatokat az eseményekkel, illetve új hivatkozási adatok hozzáadása közben.</span><span class="sxs-lookup"><span data-stu-id="c1468-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="c1468-114">Ha a "OrdinalIgnoreCase" beállítás be van állítva, a kis- és nagybetűk összehasonlítása ad meg.</span><span class="sxs-lookup"><span data-stu-id="c1468-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

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

### <span data-ttu-id="c1468-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1468-115">-DefaultProfile</span></span>
<span data-ttu-id="c1468-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1468-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1468-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="c1468-117">-EnvironmentName</span></span>
<span data-ttu-id="c1468-118">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="c1468-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="c1468-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="c1468-119">-KeyProperty</span></span>
<span data-ttu-id="c1468-120">A hivatkozási adatkészlet főbb tulajdonságainak listája.</span><span class="sxs-lookup"><span data-stu-id="c1468-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="c1468-121">Ennek létrehozásához a KEYPROPERTY tulajdonságokat és a kivonattáblát a NOTES (JEGYZETEK) szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="c1468-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="c1468-122">-Location</span><span class="sxs-lookup"><span data-stu-id="c1468-122">-Location</span></span>
<span data-ttu-id="c1468-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="c1468-123">The location of the resource.</span></span>

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

### <span data-ttu-id="c1468-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c1468-124">-Name</span></span>
<span data-ttu-id="c1468-125">A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="c1468-125">Name of the reference data set.</span></span>

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

### <span data-ttu-id="c1468-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1468-126">-ResourceGroupName</span></span>
<span data-ttu-id="c1468-127">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c1468-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="c1468-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1468-128">-SubscriptionId</span></span>
<span data-ttu-id="c1468-129">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c1468-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c1468-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1468-130">-Tag</span></span>
<span data-ttu-id="c1468-131">Key-value pairs of additional properties for the resource.</span><span class="sxs-lookup"><span data-stu-id="c1468-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="c1468-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1468-132">-Confirm</span></span>
<span data-ttu-id="c1468-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c1468-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1468-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1468-134">-WhatIf</span></span>
<span data-ttu-id="c1468-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c1468-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1468-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c1468-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1468-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1468-137">CommonParameters</span></span>
<span data-ttu-id="c1468-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1468-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1468-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1468-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1468-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1468-140">INPUTS</span></span>

## <span data-ttu-id="c1468-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1468-141">OUTPUTS</span></span>

### <span data-ttu-id="c1468-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="c1468-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="c1468-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c1468-143">NOTES</span></span>

<span data-ttu-id="c1468-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c1468-144">ALIASES</span></span>

<span data-ttu-id="c1468-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="c1468-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c1468-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="c1468-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1468-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c1468-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c1468-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: A hivatkozási adatkészlet főbb tulajdonságainak listája.</span><span class="sxs-lookup"><span data-stu-id="c1468-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="c1468-149">`[Name <String>]`: A kulcstulajdonság neve.</span><span class="sxs-lookup"><span data-stu-id="c1468-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="c1468-150">`[Type <ReferenceDataKeyPropertyType?>]`: A kulcstulajdonság típusa.</span><span class="sxs-lookup"><span data-stu-id="c1468-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="c1468-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1468-151">RELATED LINKS</span></span>

