---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157779"
---
# <span data-ttu-id="d359a-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="d359a-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="d359a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d359a-102">SYNOPSIS</span></span>
<span data-ttu-id="d359a-103">Hivatkozási adatkészlet létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="d359a-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="d359a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d359a-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d359a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d359a-105">DESCRIPTION</span></span>
<span data-ttu-id="d359a-106">Hivatkozási adatkészlet létrehozása vagy frissítése a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="d359a-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="d359a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d359a-107">EXAMPLES</span></span>

### <span data-ttu-id="d359a-108">1. példa: Hivatkozási adatkészlet létrehozása egy adott környezethez</span><span class="sxs-lookup"><span data-stu-id="d359a-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="d359a-109">Ez a parancs egy adott környezet hivatkozási adatkészletét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="d359a-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="d359a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d359a-110">PARAMETERS</span></span>

### <span data-ttu-id="d359a-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="d359a-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="d359a-112">A hivatkozási adatkészlet kulcs-összehasonlítási viselkedése a tulajdonság használatával beállítható.</span><span class="sxs-lookup"><span data-stu-id="d359a-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="d359a-113">Az érték alapértelmezés szerint "Sorszám" – ez azt jelenti, hogy a program a kis- és nagybetűket megkülönböztetve hasonlítja össze a hivatkozási adatokat eseményekkel, illetve új hivatkozási adatok hozzáadása közben.</span><span class="sxs-lookup"><span data-stu-id="d359a-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="d359a-114">Ha a "OrdinalIgnoreCase" beállítás be van állítva, a kis- és nagybetűk összehasonlítása fog hasonlítani a kis- és nagybetűkre.</span><span class="sxs-lookup"><span data-stu-id="d359a-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

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

### <span data-ttu-id="d359a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d359a-115">-DefaultProfile</span></span>
<span data-ttu-id="d359a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d359a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d359a-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="d359a-117">-EnvironmentName</span></span>
<span data-ttu-id="d359a-118">A megadott erőforráscsoporthoz társított Time Series Insights környezet neve.</span><span class="sxs-lookup"><span data-stu-id="d359a-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="d359a-119">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="d359a-119">-KeyProperty</span></span>
<span data-ttu-id="d359a-120">A hivatkozási adatkészlet főbb tulajdonságainak listája.</span><span class="sxs-lookup"><span data-stu-id="d359a-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="d359a-121">A KEYPROPERTY tulajdonságokat a NOTES (JEGYZETEK) szakaszból építi ki, és hozzon létre egy kivonattáblát.</span><span class="sxs-lookup"><span data-stu-id="d359a-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="d359a-122">-Location</span><span class="sxs-lookup"><span data-stu-id="d359a-122">-Location</span></span>
<span data-ttu-id="d359a-123">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d359a-123">The location of the resource.</span></span>

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

### <span data-ttu-id="d359a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d359a-124">-Name</span></span>
<span data-ttu-id="d359a-125">A hivatkozási adatkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="d359a-125">Name of the reference data set.</span></span>

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

### <span data-ttu-id="d359a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d359a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d359a-127">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d359a-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="d359a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d359a-128">-SubscriptionId</span></span>
<span data-ttu-id="d359a-129">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d359a-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d359a-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d359a-130">-Tag</span></span>
<span data-ttu-id="d359a-131">Key-value pairs of additional properties for the resource.</span><span class="sxs-lookup"><span data-stu-id="d359a-131">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="d359a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d359a-132">-Confirm</span></span>
<span data-ttu-id="d359a-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d359a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d359a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d359a-134">-WhatIf</span></span>
<span data-ttu-id="d359a-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d359a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d359a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d359a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d359a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d359a-137">CommonParameters</span></span>
<span data-ttu-id="d359a-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d359a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d359a-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d359a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d359a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d359a-140">INPUTS</span></span>

## <span data-ttu-id="d359a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d359a-141">OUTPUTS</span></span>

### <span data-ttu-id="d359a-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="d359a-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="d359a-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d359a-143">NOTES</span></span>

<span data-ttu-id="d359a-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d359a-144">ALIASES</span></span>

<span data-ttu-id="d359a-145">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d359a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d359a-146">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="d359a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d359a-147">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d359a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d359a-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: A hivatkozási adatkészlet főbb tulajdonságainak listája.</span><span class="sxs-lookup"><span data-stu-id="d359a-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="d359a-149">`[Name <String>]`: A kulcstulajdonság neve.</span><span class="sxs-lookup"><span data-stu-id="d359a-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="d359a-150">`[Type <ReferenceDataKeyPropertyType?>]`: A kulcstulajdonság típusa.</span><span class="sxs-lookup"><span data-stu-id="d359a-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="d359a-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d359a-151">RELATED LINKS</span></span>

