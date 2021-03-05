---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 464dbb54a96f7f543607cd2f053a0e7360eba344
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013670"
---
# <span data-ttu-id="fc7b4-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="fc7b4-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="fc7b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc7b4-102">SYNOPSIS</span></span>
<span data-ttu-id="fc7b4-103">Létrehoz egy új Fogavadb Gremlin Graph diagramot.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="fc7b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc7b4-104">SYNTAX</span></span>

### <span data-ttu-id="fc7b4-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc7b4-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc7b4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc7b4-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc7b4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc7b4-107">DESCRIPTION</span></span>
<span data-ttu-id="fc7b4-108">Létrehoz egy új Fogavadb Gremlin Graph diagramot.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="fc7b4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc7b4-109">EXAMPLES</span></span>

### <span data-ttu-id="fc7b4-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="fc7b4-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="fc7b4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc7b4-111">PARAMETERS</span></span>

### <span data-ttu-id="fc7b4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc7b4-112">-AccountName</span></span>
<span data-ttu-id="fc7b4-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fc7b4-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="fc7b4-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="fc7b4-115">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="fc7b4-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc7b4-116">-Confirm</span></span>
<span data-ttu-id="fc7b4-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc7b4-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fc7b4-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="fc7b4-119">ConflictResolutionPolicy object of type PSConflictResolutionPolicy, ha ezt a tároló ConflictResolutionPolicy-ként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="fc7b4-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="fc7b4-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="fc7b4-121">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="fc7b4-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="fc7b4-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="fc7b4-123">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="fc7b4-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="fc7b4-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="fc7b4-125">Egyéni típushoz meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="fc7b4-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc7b4-126">-DatabaseName</span></span>
<span data-ttu-id="fc7b4-127">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-127">Database name.</span></span>

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

### <span data-ttu-id="fc7b4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7b4-128">-DefaultProfile</span></span>
<span data-ttu-id="fc7b4-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc7b4-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="fc7b4-130">-IndexingPolicy</span></span>
<span data-ttu-id="fc7b4-131">A Microsoft.Azure.Commands.Fogarasdb.PSIndexingPolicy típusú indexelési házirendobjektum.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="fc7b4-132">-Name</span><span class="sxs-lookup"><span data-stu-id="fc7b4-132">-Name</span></span>
<span data-ttu-id="fc7b4-133">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="fc7b4-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fc7b4-134">-ParentObject</span></span>
<span data-ttu-id="fc7b4-135">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="fc7b4-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="fc7b4-136">-PartitionKeyKind</span></span>
<span data-ttu-id="fc7b4-137">A partíciókhoz használt algoritmus fajtája.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="fc7b4-138">Lehetséges értékek: "Kivonat", "Tartomány"</span><span class="sxs-lookup"><span data-stu-id="fc7b4-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="fc7b4-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="fc7b4-139">-PartitionKeyPath</span></span>
<span data-ttu-id="fc7b4-140">Partition key Path, pl.: '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="fc7b4-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="fc7b4-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="fc7b4-142">A partíciók kulcsdefiníciójának verziója</span><span class="sxs-lookup"><span data-stu-id="fc7b4-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="fc7b4-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc7b4-143">-ResourceGroupName</span></span>
<span data-ttu-id="fc7b4-144">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-144">Name of resource group.</span></span>

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

### <span data-ttu-id="fc7b4-145">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="fc7b4-145">-Throughput</span></span>
<span data-ttu-id="fc7b4-146">A Gremlin Graph (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="fc7b4-147">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-147">Default value is 400.</span></span>

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

### <span data-ttu-id="fc7b4-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="fc7b4-148">-TtlInSeconds</span></span>
<span data-ttu-id="fc7b4-149">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="fc7b4-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="fc7b4-150">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="fc7b4-151">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="fc7b4-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="fc7b4-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="fc7b4-153">A Microsoft.Azure.Commands.FogasDB.PSUniqueKeyPolicy típusú UniqueKeyPolicy objektum.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="fc7b4-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc7b4-154">-WhatIf</span></span>
<span data-ttu-id="fc7b4-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc7b4-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc7b4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7b4-157">CommonParameters</span></span>
<span data-ttu-id="fc7b4-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc7b4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7b4-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc7b4-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7b4-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc7b4-160">INPUTS</span></span>

### <span data-ttu-id="fc7b4-161">Microsoft.Azure.Commands.CossDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="fc7b4-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="fc7b4-162">Microsoft.Azure.Commands.EzresDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="fc7b4-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="fc7b4-163">Microsoft.Azure.Commands.EzresDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="fc7b4-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="fc7b4-164">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fc7b4-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="fc7b4-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc7b4-165">OUTPUTS</span></span>

### <span data-ttu-id="fc7b4-166">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="fc7b4-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="fc7b4-167">System.Exception</span><span class="sxs-lookup"><span data-stu-id="fc7b4-167">System.Exception</span></span>

## <span data-ttu-id="fc7b4-168">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc7b4-168">NOTES</span></span>

## <span data-ttu-id="fc7b4-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc7b4-169">RELATED LINKS</span></span>
