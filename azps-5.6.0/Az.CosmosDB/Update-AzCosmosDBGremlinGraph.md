---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 500bd1203f7f70b5749986a6b4ff1ab8d5978185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931281"
---
# <span data-ttu-id="eb006-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="eb006-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="eb006-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb006-102">SYNOPSIS</span></span>
<span data-ttu-id="eb006-103">Frissíti aTervsDB Gremlin Graphot.</span><span class="sxs-lookup"><span data-stu-id="eb006-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="eb006-104">Ügyféloldali javítást hajt végre a meglévő Grafikon olvasása segítségével.</span><span class="sxs-lookup"><span data-stu-id="eb006-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="eb006-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eb006-105">SYNTAX</span></span>

### <span data-ttu-id="eb006-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb006-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb006-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb006-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb006-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb006-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb006-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eb006-109">DESCRIPTION</span></span>
<span data-ttu-id="eb006-110">Frissíti aTervsDB Gremlin Graphot.</span><span class="sxs-lookup"><span data-stu-id="eb006-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="eb006-111">Ügyféloldali javítást hajt végre a meglévő Grafikon olvasása segítségével.</span><span class="sxs-lookup"><span data-stu-id="eb006-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="eb006-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eb006-112">EXAMPLES</span></span>

### <span data-ttu-id="eb006-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="eb006-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="eb006-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb006-114">PARAMETERS</span></span>

### <span data-ttu-id="eb006-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb006-115">-AccountName</span></span>
<span data-ttu-id="eb006-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="eb006-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="eb006-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="eb006-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="eb006-118">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="eb006-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="eb006-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb006-119">-Confirm</span></span>
<span data-ttu-id="eb006-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eb006-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb006-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="eb006-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="eb006-122">ConflictResolutionPolicy object of type PSConflictResolutionPolicy, ha ezt a tároló ConflictResolutionPolicy-ként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="eb006-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="eb006-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="eb006-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="eb006-124">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="eb006-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="eb006-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="eb006-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="eb006-126">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="eb006-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="eb006-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="eb006-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="eb006-128">Egyéni típushoz meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="eb006-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="eb006-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb006-129">-DatabaseName</span></span>
<span data-ttu-id="eb006-130">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="eb006-130">Database name.</span></span>

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

### <span data-ttu-id="eb006-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb006-131">-DefaultProfile</span></span>
<span data-ttu-id="eb006-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb006-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb006-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="eb006-133">-IndexingPolicy</span></span>
<span data-ttu-id="eb006-134">A Microsoft.Azure.Commands.Fogarasdb.PSIndexingPolicy típusú indexelési házirendobjektum.</span><span class="sxs-lookup"><span data-stu-id="eb006-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="eb006-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb006-135">-InputObject</span></span>
<span data-ttu-id="eb006-136">Gremlin Graph-objektum.</span><span class="sxs-lookup"><span data-stu-id="eb006-136">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb006-137">-Name</span><span class="sxs-lookup"><span data-stu-id="eb006-137">-Name</span></span>
<span data-ttu-id="eb006-138">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="eb006-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="eb006-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="eb006-139">-ParentObject</span></span>
<span data-ttu-id="eb006-140">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="eb006-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="eb006-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="eb006-141">-PartitionKeyKind</span></span>
<span data-ttu-id="eb006-142">A partíciókhoz használt algoritmus fajtája.</span><span class="sxs-lookup"><span data-stu-id="eb006-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="eb006-143">Lehetséges értékek: "Kivonat", "Tartomány"</span><span class="sxs-lookup"><span data-stu-id="eb006-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="eb006-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="eb006-144">-PartitionKeyPath</span></span>
<span data-ttu-id="eb006-145">Partition key Path, pl.: '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="eb006-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb006-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="eb006-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="eb006-147">A partíciók kulcsdefiníciójának verziója</span><span class="sxs-lookup"><span data-stu-id="eb006-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="eb006-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb006-148">-ResourceGroupName</span></span>
<span data-ttu-id="eb006-149">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eb006-149">Name of resource group.</span></span>

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

### <span data-ttu-id="eb006-150">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="eb006-150">-Throughput</span></span>
<span data-ttu-id="eb006-151">A Gremlin Graph (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="eb006-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="eb006-152">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="eb006-152">Default value is 400.</span></span>

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

### <span data-ttu-id="eb006-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="eb006-153">-TtlInSeconds</span></span>
<span data-ttu-id="eb006-154">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="eb006-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="eb006-155">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="eb006-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="eb006-156">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="eb006-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="eb006-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="eb006-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="eb006-158">A Microsoft.Azure.Commands.FogasDB.PSUniqueKeyPolicy típusú UniqueKeyPolicy objektum.</span><span class="sxs-lookup"><span data-stu-id="eb006-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="eb006-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb006-159">-WhatIf</span></span>
<span data-ttu-id="eb006-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eb006-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb006-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb006-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb006-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb006-162">CommonParameters</span></span>
<span data-ttu-id="eb006-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb006-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb006-164">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb006-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb006-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb006-165">INPUTS</span></span>

### <span data-ttu-id="eb006-166">Microsoft.Azure.Commands.CossDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="eb006-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="eb006-167">Microsoft.Azure.Commands.EzresDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="eb006-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="eb006-168">Microsoft.Azure.Commands.EzresDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="eb006-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="eb006-169">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="eb006-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="eb006-170">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="eb006-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="eb006-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb006-171">OUTPUTS</span></span>

### <span data-ttu-id="eb006-172">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="eb006-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="eb006-173">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="eb006-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="eb006-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eb006-174">NOTES</span></span>

## <span data-ttu-id="eb006-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb006-175">RELATED LINKS</span></span>
