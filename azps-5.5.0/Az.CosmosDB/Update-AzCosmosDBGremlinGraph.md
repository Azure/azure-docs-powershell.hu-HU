---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148498"
---
# <span data-ttu-id="6a6fc-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="6a6fc-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="6a6fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="6a6fc-103">Frissíti aTervsDB Gremlin Graphot.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="6a6fc-104">Ügyféloldali javítást hajt végre a meglévő Grafikon olvasása segítségével.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="6a6fc-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a6fc-105">SYNTAX</span></span>

### <span data-ttu-id="6a6fc-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a6fc-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a6fc-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a6fc-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a6fc-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a6fc-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a6fc-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a6fc-109">DESCRIPTION</span></span>
<span data-ttu-id="6a6fc-110">Frissíti aTervsDB Gremlin Graphot.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="6a6fc-111">Ügyféloldali javítást hajt végre a meglévő Grafikon olvasása segítségével.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="6a6fc-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a6fc-112">EXAMPLES</span></span>

### <span data-ttu-id="6a6fc-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="6a6fc-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="6a6fc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a6fc-114">PARAMETERS</span></span>

### <span data-ttu-id="6a6fc-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6a6fc-115">-AccountName</span></span>
<span data-ttu-id="6a6fc-116">A Külön db-adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6a6fc-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="6a6fc-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="6a6fc-118">Maximális átviteli sebesség, ha engedélyezve van az automatikus méretezés.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="6a6fc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a6fc-119">-Confirm</span></span>
<span data-ttu-id="6a6fc-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a6fc-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="6a6fc-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="6a6fc-122">ConflictResolutionPolicy object of type PSConflictResolutionPolicy, ha ezt a tároló ConflictResolutionPolicy-ként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="6a6fc-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="6a6fc-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="6a6fc-124">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="6a6fc-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="6a6fc-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="6a6fc-126">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="6a6fc-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="6a6fc-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="6a6fc-128">A típus egyéni típusának meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="6a6fc-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a6fc-129">-DatabaseName</span></span>
<span data-ttu-id="6a6fc-130">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-130">Database name.</span></span>

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

### <span data-ttu-id="6a6fc-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a6fc-131">-DefaultProfile</span></span>
<span data-ttu-id="6a6fc-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a6fc-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="6a6fc-133">-IndexingPolicy</span></span>
<span data-ttu-id="6a6fc-134">A Microsoft.Azure.Commands.Fogarasdb.PSIndexingPolicy típusú indexelési házirendobjektum.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="6a6fc-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a6fc-135">-InputObject</span></span>
<span data-ttu-id="6a6fc-136">Gremlin Graph-objektum.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="6a6fc-137">-Name</span><span class="sxs-lookup"><span data-stu-id="6a6fc-137">-Name</span></span>
<span data-ttu-id="6a6fc-138">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="6a6fc-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6a6fc-139">-ParentObject</span></span>
<span data-ttu-id="6a6fc-140">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="6a6fc-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="6a6fc-141">-PartitionKeyKind</span></span>
<span data-ttu-id="6a6fc-142">A partíciókhoz használt algoritmus fajtája.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="6a6fc-143">Lehetséges értékek: "Kivonat", "Tartomány"</span><span class="sxs-lookup"><span data-stu-id="6a6fc-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="6a6fc-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="6a6fc-144">-PartitionKeyPath</span></span>
<span data-ttu-id="6a6fc-145">Partition key Path, pl.: '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="6a6fc-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="6a6fc-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="6a6fc-147">A partíciók kulcsdefiníciójának verziója</span><span class="sxs-lookup"><span data-stu-id="6a6fc-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="6a6fc-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a6fc-148">-ResourceGroupName</span></span>
<span data-ttu-id="6a6fc-149">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-149">Name of resource group.</span></span>

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

### <span data-ttu-id="6a6fc-150">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="6a6fc-150">-Throughput</span></span>
<span data-ttu-id="6a6fc-151">A Gremlin Graph (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="6a6fc-152">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-152">Default value is 400.</span></span>

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

### <span data-ttu-id="6a6fc-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="6a6fc-153">-TtlInSeconds</span></span>
<span data-ttu-id="6a6fc-154">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="6a6fc-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="6a6fc-155">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="6a6fc-156">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="6a6fc-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="6a6fc-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="6a6fc-158">A Microsoft.Azure.Commands.FogasDB.PSUniqueKeyPolicy típusú UniqueKeyPolicy objektum.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="6a6fc-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a6fc-159">-WhatIf</span></span>
<span data-ttu-id="6a6fc-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a6fc-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a6fc-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a6fc-162">CommonParameters</span></span>
<span data-ttu-id="6a6fc-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a6fc-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a6fc-164">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a6fc-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a6fc-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a6fc-165">INPUTS</span></span>

### <span data-ttu-id="6a6fc-166">Microsoft.Azure.Commands.EzresDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="6a6fc-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="6a6fc-167">Microsoft.Azure.Commands.EzresDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="6a6fc-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="6a6fc-168">Microsoft.Azure.Commands.EzresDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="6a6fc-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="6a6fc-169">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="6a6fc-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="6a6fc-170">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="6a6fc-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="6a6fc-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a6fc-171">OUTPUTS</span></span>

### <span data-ttu-id="6a6fc-172">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="6a6fc-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="6a6fc-173">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="6a6fc-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="6a6fc-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a6fc-174">NOTES</span></span>

## <span data-ttu-id="6a6fc-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a6fc-175">RELATED LINKS</span></span>
