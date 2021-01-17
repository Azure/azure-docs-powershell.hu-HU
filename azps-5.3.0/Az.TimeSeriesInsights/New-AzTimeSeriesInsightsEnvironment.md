---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467073"
---
# <span data-ttu-id="ed224-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="ed224-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="ed224-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed224-102">SYNOPSIS</span></span>
<span data-ttu-id="ed224-103">Hozzon létre egy környezetet a megadott előfizetési és erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="ed224-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="ed224-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ed224-104">SYNTAX</span></span>

### <span data-ttu-id="ed224-105">Gen1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed224-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ed224-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="ed224-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ed224-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ed224-107">DESCRIPTION</span></span>
<span data-ttu-id="ed224-108">Hozzon létre egy környezetet a megadott előfizetési és erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="ed224-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="ed224-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ed224-109">EXAMPLES</span></span>

### <span data-ttu-id="ed224-110">1. példa: Generációs1 idősorok elemzési környezetének létrehozása</span><span class="sxs-lookup"><span data-stu-id="ed224-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="ed224-111">Ez a parancs egy Gen1 idősorozat-elemzési környezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ed224-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="ed224-112">2. példa: A Gen2 idősorozatok elemzési környezetének létrehozása</span><span class="sxs-lookup"><span data-stu-id="ed224-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="ed224-113">Ez a parancs egy Gen2 idősorozat-elemzési környezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ed224-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="ed224-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed224-114">PARAMETERS</span></span>

### <span data-ttu-id="ed224-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed224-115">-AsJob</span></span>
<span data-ttu-id="ed224-116">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="ed224-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ed224-117">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="ed224-117">-Capacity</span></span>
<span data-ttu-id="ed224-118">A termékváltozat kapacitása.</span><span class="sxs-lookup"><span data-stu-id="ed224-118">The capacity of the sku.</span></span>
<span data-ttu-id="ed224-119">A Gen1 környezetek esetében ez az érték a létrehozásuk után módosítható úgy, hogy támogassa a környezetek méretének méretezését.</span><span class="sxs-lookup"><span data-stu-id="ed224-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed224-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="ed224-120">-DataRetentionTime</span></span>
<span data-ttu-id="ed224-121">Az adatmegőrzési idő.</span><span class="sxs-lookup"><span data-stu-id="ed224-121">The data retention time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed224-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed224-122">-DefaultProfile</span></span>
<span data-ttu-id="ed224-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed224-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed224-124">-Kind</span><span class="sxs-lookup"><span data-stu-id="ed224-124">-Kind</span></span>
<span data-ttu-id="ed224-125">A környezet fajtája.</span><span class="sxs-lookup"><span data-stu-id="ed224-125">The kind of the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed224-126">-Location</span><span class="sxs-lookup"><span data-stu-id="ed224-126">-Location</span></span>
<span data-ttu-id="ed224-127">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="ed224-127">The location of the resource.</span></span>

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

### <span data-ttu-id="ed224-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ed224-128">-Name</span></span>
<span data-ttu-id="ed224-129">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="ed224-129">Name of the environment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed224-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ed224-130">-NoWait</span></span>
<span data-ttu-id="ed224-131">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="ed224-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ed224-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="ed224-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="ed224-133">A környezetben az adatok partíciókhoz használt eseménytulajdonságok listája.</span><span class="sxs-lookup"><span data-stu-id="ed224-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="ed224-134">A felépítésről a PARTITIONKEYPROPERTY tulajdonságokAT és a kivonattáblát a NOTES (JEGYZETEK) című szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="ed224-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed224-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed224-135">-ResourceGroupName</span></span>
<span data-ttu-id="ed224-136">Egy Azure Resource-csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed224-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="ed224-137">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="ed224-137">-Sku</span></span>
<span data-ttu-id="ed224-138">A termékváltozat neve.</span><span class="sxs-lookup"><span data-stu-id="ed224-138">The name of this SKU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed224-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ed224-139">-StorageAccountKey</span></span>
<span data-ttu-id="ed224-140">Annak a felügyeleti kulcsnak az értéke, amely a Time Series Insights szolgáltatást írási hozzáférést biztosít a tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="ed224-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed224-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ed224-141">-StorageAccountName</span></span>
<span data-ttu-id="ed224-142">Annak a tárfióknak a neve, amely a környezet hosszú távú adatait fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="ed224-142">The name of the storage account that will hold the environment's long term data.</span></span>

```yaml
Type: System.String
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed224-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="ed224-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="ed224-144">A Time Series Insights szolgáltatás viselkedése a környezet kapacitásának túllépése esetén</span><span class="sxs-lookup"><span data-stu-id="ed224-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

```yaml
Type: System.String
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed224-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed224-145">-SubscriptionId</span></span>
<span data-ttu-id="ed224-146">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ed224-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="ed224-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed224-147">-Tag</span></span>
<span data-ttu-id="ed224-148">Key-value pairs of additional properties for the resource.</span><span class="sxs-lookup"><span data-stu-id="ed224-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="ed224-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="ed224-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="ed224-150">A környezet idősor-azonosítójának meghatározásához használt eseménytulajdonságok listája. Ennek létrehozásáról a TIMESERIESIDPROPERTY tulajdonságokat és a hash táblázatot hoz létre a NOTES (JEGYZETEK) szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="ed224-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed224-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="ed224-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="ed224-152">ISO8601 időből, amely megadja, hogy a környezet eseményei hány napig lesznek elérhetők a meleg tárolóból való lekérdezéshez.</span><span class="sxs-lookup"><span data-stu-id="ed224-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed224-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed224-153">-Confirm</span></span>
<span data-ttu-id="ed224-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ed224-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed224-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed224-155">-WhatIf</span></span>
<span data-ttu-id="ed224-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ed224-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed224-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed224-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed224-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed224-158">CommonParameters</span></span>
<span data-ttu-id="ed224-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed224-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed224-160">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed224-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed224-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed224-161">INPUTS</span></span>

## <span data-ttu-id="ed224-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed224-162">OUTPUTS</span></span>

### <span data-ttu-id="ed224-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="ed224-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="ed224-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ed224-164">NOTES</span></span>

<span data-ttu-id="ed224-165">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ed224-165">ALIASES</span></span>

<span data-ttu-id="ed224-166">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ed224-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ed224-167">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ed224-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ed224-168">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ed224-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ed224-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: A környezetben az adatok partíciókhoz használt eseménytulajdonságok listája.</span><span class="sxs-lookup"><span data-stu-id="ed224-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="ed224-170">`[Name <String>]`: A tulajdonság neve.</span><span class="sxs-lookup"><span data-stu-id="ed224-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="ed224-171">`[Type <PropertyType?>]`: A tulajdonság típusa.</span><span class="sxs-lookup"><span data-stu-id="ed224-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="ed224-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: A környezet idősor-azonosítójának meghatározásához használt eseménytulajdonságok listája.</span><span class="sxs-lookup"><span data-stu-id="ed224-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="ed224-173">`[Name <String>]`: A tulajdonság neve.</span><span class="sxs-lookup"><span data-stu-id="ed224-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="ed224-174">`[Type <PropertyType?>]`: A tulajdonság típusa.</span><span class="sxs-lookup"><span data-stu-id="ed224-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="ed224-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed224-175">RELATED LINKS</span></span>

