---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348989"
---
# <span data-ttu-id="22dc3-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="22dc3-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="22dc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="22dc3-103">Létrehoz egy új Fogavadb Gremlin Graph diagramot.</span><span class="sxs-lookup"><span data-stu-id="22dc3-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="22dc3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22dc3-104">SYNTAX</span></span>

### <span data-ttu-id="22dc3-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22dc3-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22dc3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22dc3-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22dc3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22dc3-107">DESCRIPTION</span></span>
<span data-ttu-id="22dc3-108">Létrehoz egy új Fogavadb Gremlin Graph diagramot.</span><span class="sxs-lookup"><span data-stu-id="22dc3-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="22dc3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22dc3-109">EXAMPLES</span></span>

### <span data-ttu-id="22dc3-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="22dc3-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="22dc3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22dc3-111">PARAMETERS</span></span>

### <span data-ttu-id="22dc3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22dc3-112">-AccountName</span></span>
<span data-ttu-id="22dc3-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="22dc3-113">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="22dc3-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="22dc3-115">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="22dc3-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22dc3-116">-Confirm</span></span>
<span data-ttu-id="22dc3-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22dc3-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="22dc3-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="22dc3-119">ConflictResolutionPolicy object of type PSConflictResolutionPolicy, ha ezt a tároló ConflictResolutionPolicy-ként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="22dc3-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="22dc3-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="22dc3-121">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="22dc3-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="22dc3-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="22dc3-123">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="22dc3-123">To be provided when the type is LastWriterWins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="22dc3-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="22dc3-125">Egyéni típushoz meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="22dc3-125">To be provided when the type is custom.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22dc3-126">-DatabaseName</span></span>
<span data-ttu-id="22dc3-127">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="22dc3-127">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22dc3-128">-DefaultProfile</span></span>
<span data-ttu-id="22dc3-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22dc3-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="22dc3-130">-IndexingPolicy</span></span>
<span data-ttu-id="22dc3-131">A Microsoft.Azure.Commands.Fogarasdb.PSIndexingPolicy típusú indexelési házirendobjektum.</span><span class="sxs-lookup"><span data-stu-id="22dc3-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

```yaml
Type: PSIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-132">-Name</span><span class="sxs-lookup"><span data-stu-id="22dc3-132">-Name</span></span>
<span data-ttu-id="22dc3-133">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="22dc3-133">Gremlin Graph Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="22dc3-134">-ParentObject</span></span>
<span data-ttu-id="22dc3-135">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="22dc3-135">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="22dc3-136">-PartitionKeyKind</span></span>
<span data-ttu-id="22dc3-137">A partíciókhoz használt algoritmus fajtája.</span><span class="sxs-lookup"><span data-stu-id="22dc3-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="22dc3-138">Lehetséges értékek: "Kivonat", "Tartomány"</span><span class="sxs-lookup"><span data-stu-id="22dc3-138">Possible values include: 'Hash', 'Range'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="22dc3-139">-PartitionKeyPath</span></span>
<span data-ttu-id="22dc3-140">Partition key Path, pl.: '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="22dc3-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="22dc3-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="22dc3-142">A partíciók kulcsdefiníciójának verziója</span><span class="sxs-lookup"><span data-stu-id="22dc3-142">The version of the partition key definition</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22dc3-143">-ResourceGroupName</span></span>
<span data-ttu-id="22dc3-144">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="22dc3-144">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-145">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="22dc3-145">-Throughput</span></span>
<span data-ttu-id="22dc3-146">A Gremlin Graph (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="22dc3-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="22dc3-147">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="22dc3-147">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="22dc3-148">-TtlInSeconds</span></span>
<span data-ttu-id="22dc3-149">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="22dc3-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="22dc3-150">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="22dc3-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="22dc3-151">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="22dc3-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="22dc3-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="22dc3-153">A Microsoft.Azure.Commands.FogasDB.PSUniqueKeyPolicy típusú UniqueKeyPolicy objektum.</span><span class="sxs-lookup"><span data-stu-id="22dc3-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

```yaml
Type: PSUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22dc3-154">-WhatIf</span></span>
<span data-ttu-id="22dc3-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22dc3-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22dc3-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22dc3-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dc3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22dc3-157">CommonParameters</span></span>
<span data-ttu-id="22dc3-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22dc3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22dc3-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22dc3-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22dc3-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22dc3-160">INPUTS</span></span>

### <span data-ttu-id="22dc3-161">Microsoft.Azure.Commands.CossDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="22dc3-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="22dc3-162">Microsoft.Azure.Commands.EzresDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="22dc3-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="22dc3-163">Microsoft.Azure.Commands.EzresDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="22dc3-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="22dc3-164">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="22dc3-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="22dc3-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22dc3-165">OUTPUTS</span></span>

### <span data-ttu-id="22dc3-166">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="22dc3-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="22dc3-167">System.Exception</span><span class="sxs-lookup"><span data-stu-id="22dc3-167">System.Exception</span></span>

## <span data-ttu-id="22dc3-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22dc3-168">NOTES</span></span>

## <span data-ttu-id="22dc3-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22dc3-169">RELATED LINKS</span></span>
