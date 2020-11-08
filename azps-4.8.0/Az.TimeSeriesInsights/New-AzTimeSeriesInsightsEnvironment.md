---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183445"
---
# <span data-ttu-id="d2117-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="d2117-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="d2117-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2117-102">SYNOPSIS</span></span>
<span data-ttu-id="d2117-103">A megadott előfizetés és erőforráscsoport környezetének létrehozása</span><span class="sxs-lookup"><span data-stu-id="d2117-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="d2117-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2117-104">SYNTAX</span></span>

### <span data-ttu-id="d2117-105">Gen1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2117-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2117-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="d2117-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d2117-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2117-107">DESCRIPTION</span></span>
<span data-ttu-id="d2117-108">A megadott előfizetés és erőforráscsoport környezetének létrehozása</span><span class="sxs-lookup"><span data-stu-id="d2117-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="d2117-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d2117-109">EXAMPLES</span></span>

### <span data-ttu-id="d2117-110">Példa 1: Gen1-idősorozat létrehozása – elemzések környezete</span><span class="sxs-lookup"><span data-stu-id="d2117-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="d2117-111">Ez a parancs Gen1-adatsort hoz létre a betekintési környezetben.</span><span class="sxs-lookup"><span data-stu-id="d2117-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="d2117-112">2. példa: Gen2-idősorozat létrehozása – környezet</span><span class="sxs-lookup"><span data-stu-id="d2117-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="d2117-113">Ez a parancs Gen2-adatsort hoz létre a betekintési környezetben.</span><span class="sxs-lookup"><span data-stu-id="d2117-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="d2117-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2117-114">PARAMETERS</span></span>

### <span data-ttu-id="d2117-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2117-115">-AsJob</span></span>
<span data-ttu-id="d2117-116">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="d2117-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d2117-117">-Kapacitás</span><span class="sxs-lookup"><span data-stu-id="d2117-117">-Capacity</span></span>
<span data-ttu-id="d2117-118">Az SKU kapacitása.</span><span class="sxs-lookup"><span data-stu-id="d2117-118">The capacity of the sku.</span></span>
<span data-ttu-id="d2117-119">A Gen1-környezetek esetében ezt az értéket úgy módosíthatja, hogy a létrehozásuk után is támogassa a környezetek méretét.</span><span class="sxs-lookup"><span data-stu-id="d2117-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

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

### <span data-ttu-id="d2117-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="d2117-120">-DataRetentionTime</span></span>
<span data-ttu-id="d2117-121">Az adatmegőrzési idő.</span><span class="sxs-lookup"><span data-stu-id="d2117-121">The data retention time.</span></span>

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

### <span data-ttu-id="d2117-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2117-122">-DefaultProfile</span></span>
<span data-ttu-id="d2117-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2117-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2117-124">-Kind</span><span class="sxs-lookup"><span data-stu-id="d2117-124">-Kind</span></span>
<span data-ttu-id="d2117-125">A környezet fajtája.</span><span class="sxs-lookup"><span data-stu-id="d2117-125">The kind of the environment.</span></span>

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

### <span data-ttu-id="d2117-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="d2117-126">-Location</span></span>
<span data-ttu-id="d2117-127">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="d2117-127">The location of the resource.</span></span>

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

### <span data-ttu-id="d2117-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d2117-128">-Name</span></span>
<span data-ttu-id="d2117-129">A környezet neve</span><span class="sxs-lookup"><span data-stu-id="d2117-129">Name of the environment</span></span>

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

### <span data-ttu-id="d2117-130">-Várva</span><span class="sxs-lookup"><span data-stu-id="d2117-130">-NoWait</span></span>
<span data-ttu-id="d2117-131">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="d2117-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d2117-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="d2117-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="d2117-133">Az esemény tulajdonságainak listája, amelyet a környezet adatainak particionálásakor fog használni.</span><span class="sxs-lookup"><span data-stu-id="d2117-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="d2117-134">A kivitelezéshez tekintse meg a PARTITIONKEYPROPERTY tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d2117-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2117-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2117-135">-ResourceGroupName</span></span>
<span data-ttu-id="d2117-136">Azure-erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d2117-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="d2117-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="d2117-137">-Sku</span></span>
<span data-ttu-id="d2117-138">Ennek a SKU-nak a neve.</span><span class="sxs-lookup"><span data-stu-id="d2117-138">The name of this SKU.</span></span>

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

### <span data-ttu-id="d2117-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d2117-139">-StorageAccountKey</span></span>
<span data-ttu-id="d2117-140">Annak a kezelési kulcsnak az értéke, amely az idősorozat-betekintést nyújtja, a tárolási fiókhoz írási hozzáférést biztosít.</span><span class="sxs-lookup"><span data-stu-id="d2117-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

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

### <span data-ttu-id="d2117-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d2117-141">-StorageAccountName</span></span>
<span data-ttu-id="d2117-142">Annak a tárolási fióknak a neve, amely a környezet hosszú távú adatait fogja tárolni.</span><span class="sxs-lookup"><span data-stu-id="d2117-142">The name of the storage account that will hold the environment's long term data.</span></span>

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

### <span data-ttu-id="d2117-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="d2117-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="d2117-144">Az idősorozat-betekintési szolgáltatás működése a környezet kapacitásának túllépése esetén</span><span class="sxs-lookup"><span data-stu-id="d2117-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

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

### <span data-ttu-id="d2117-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2117-145">-SubscriptionId</span></span>
<span data-ttu-id="d2117-146">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="d2117-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d2117-147">-Címke</span><span class="sxs-lookup"><span data-stu-id="d2117-147">-Tag</span></span>
<span data-ttu-id="d2117-148">Az erőforrás további tulajdonságainak kulcs-érték párjai</span><span class="sxs-lookup"><span data-stu-id="d2117-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="d2117-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="d2117-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="d2117-150">Az esemény tulajdonságainak listája, amelyet a környezet idősorozat-azonosítójának definiálására fog használni. A kivitelezéshez tekintse meg a TIMESERIESIDPROPERTY tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d2117-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2117-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="d2117-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="d2117-152">A ISO8601 időszak adja meg, hogy hány napig maradnak elérhetők a környezet eseményei a meleg áruházban elérhető lekérdezésekhez.</span><span class="sxs-lookup"><span data-stu-id="d2117-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

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

### <span data-ttu-id="d2117-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d2117-153">-Confirm</span></span>
<span data-ttu-id="d2117-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d2117-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2117-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2117-155">-WhatIf</span></span>
<span data-ttu-id="d2117-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d2117-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2117-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2117-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2117-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2117-158">CommonParameters</span></span>
<span data-ttu-id="d2117-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2117-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2117-160">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d2117-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2117-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2117-161">INPUTS</span></span>

## <span data-ttu-id="d2117-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2117-162">OUTPUTS</span></span>

### <span data-ttu-id="d2117-163">Microsoft. Azure. PowerShell. parancsmagok. TimeSeriesInsights. modellek. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="d2117-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="d2117-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2117-164">NOTES</span></span>

<span data-ttu-id="d2117-165">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d2117-165">ALIASES</span></span>

<span data-ttu-id="d2117-166">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d2117-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2117-167">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d2117-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2117-168">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d2117-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2117-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty [] >: az esemény tulajdonságainak listája, amelyet a környezet adatainak particionálásakor fog használni.</span><span class="sxs-lookup"><span data-stu-id="d2117-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="d2117-170">`[Name <String>]`: A tulajdonság neve.</span><span class="sxs-lookup"><span data-stu-id="d2117-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="d2117-171">`[Type <PropertyType?>]`: A tulajdonság típusa.</span><span class="sxs-lookup"><span data-stu-id="d2117-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="d2117-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty [] >: az esemény tulajdonságainak listája, amelyet a környezet idősorozat-azonosítójának definiálására fog használni.</span><span class="sxs-lookup"><span data-stu-id="d2117-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="d2117-173">`[Name <String>]`: A tulajdonság neve.</span><span class="sxs-lookup"><span data-stu-id="d2117-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="d2117-174">`[Type <PropertyType?>]`: A tulajdonság típusa.</span><span class="sxs-lookup"><span data-stu-id="d2117-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="d2117-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2117-175">RELATED LINKS</span></span>

