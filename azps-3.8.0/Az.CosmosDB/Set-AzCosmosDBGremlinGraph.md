---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: a8ccb3757786ca76fff15b1bf68d8dc7b477ebcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014438"
---
# <span data-ttu-id="b0a31-101">Set-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="b0a31-101">Set-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="b0a31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0a31-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a31-103">Beállítja a CosmosDB Gremlin gráfot.</span><span class="sxs-lookup"><span data-stu-id="b0a31-103">Sets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b0a31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0a31-104">SYNTAX</span></span>

### <span data-ttu-id="b0a31-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0a31-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a31-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a31-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0a31-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0a31-107">DESCRIPTION</span></span>
<span data-ttu-id="b0a31-108">A **set-AzCosmosDBGremlinGraph** parancsmag CosmosDB Gremlin-diagramot állít be.</span><span class="sxs-lookup"><span data-stu-id="b0a31-108">The **Set-AzCosmosDBGremlinGraph** cmdlet sets a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b0a31-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b0a31-109">EXAMPLES</span></span>

### <span data-ttu-id="b0a31-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b0a31-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName} -PartitionKeyPath {path}

Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="b0a31-111">Az erőforrás-objektum IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etagt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b0a31-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="b0a31-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0a31-112">PARAMETERS</span></span>

### <span data-ttu-id="b0a31-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0a31-113">-AccountName</span></span>
<span data-ttu-id="b0a31-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="b0a31-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b0a31-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b0a31-115">-Confirm</span></span>
<span data-ttu-id="b0a31-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b0a31-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0a31-117">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b0a31-117">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="b0a31-118">PSConflictResolutionPolicy ConflictResolutionPolicy objektum, ha ez a tároló ConflictResolutionPolicy van beállítva.</span><span class="sxs-lookup"><span data-stu-id="b0a31-118">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="b0a31-119">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="b0a31-119">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="b0a31-120">Megadhatja az értékeket: LastWriterWins, egyéni, manuális.</span><span class="sxs-lookup"><span data-stu-id="b0a31-120">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="b0a31-121">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="b0a31-121">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="b0a31-122">Adja meg, hogy a típus LastWriterWins-e.</span><span class="sxs-lookup"><span data-stu-id="b0a31-122">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="b0a31-123">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="b0a31-123">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="b0a31-124">Adja meg, ha a típus egyéni.</span><span class="sxs-lookup"><span data-stu-id="b0a31-124">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="b0a31-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0a31-125">-DatabaseName</span></span>
<span data-ttu-id="b0a31-126">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b0a31-126">Database name.</span></span>

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

### <span data-ttu-id="b0a31-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a31-127">-DefaultProfile</span></span>
<span data-ttu-id="b0a31-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0a31-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0a31-129">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="b0a31-129">-IndexingPolicy</span></span>
<span data-ttu-id="b0a31-130">Indexelő házirend-objektum a Microsoft. Azure. commands. CosmosDB. PSSqlIndexingPolicy parancsot.</span><span class="sxs-lookup"><span data-stu-id="b0a31-130">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="b0a31-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0a31-131">-InputObject</span></span>
<span data-ttu-id="b0a31-132">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="b0a31-132">Gremlin Database object.</span></span>

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

### <span data-ttu-id="b0a31-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b0a31-133">-Name</span></span>
<span data-ttu-id="b0a31-134">Gremlin-diagram neve.</span><span class="sxs-lookup"><span data-stu-id="b0a31-134">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b0a31-135">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="b0a31-135">-PartitionKeyKind</span></span>
<span data-ttu-id="b0a31-136">A particionáláshoz használt algoritmus típusa.</span><span class="sxs-lookup"><span data-stu-id="b0a31-136">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="b0a31-137">A lehetséges értékek a következők: "hash", "tartománnyal"</span><span class="sxs-lookup"><span data-stu-id="b0a31-137">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="b0a31-138">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="b0a31-138">-PartitionKeyPath</span></span>
<span data-ttu-id="b0a31-139">A Partition kulcs elérési útja (például "/Address/zipcode").</span><span class="sxs-lookup"><span data-stu-id="b0a31-139">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="b0a31-140">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="b0a31-140">-PartitionKeyVersion</span></span>
<span data-ttu-id="b0a31-141">A Partition Key definition verziója</span><span class="sxs-lookup"><span data-stu-id="b0a31-141">The version of the partition key definition</span></span>

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

### <span data-ttu-id="b0a31-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a31-142">-ResourceGroupName</span></span>
<span data-ttu-id="b0a31-143">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b0a31-143">Name of resource group.</span></span>

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

### <span data-ttu-id="b0a31-144">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="b0a31-144">-Throughput</span></span>
<span data-ttu-id="b0a31-145">A Gremlin gráf (RU/s) átviteli sebessége</span><span class="sxs-lookup"><span data-stu-id="b0a31-145">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="b0a31-146">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="b0a31-146">Default value is 400.</span></span>

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

### <span data-ttu-id="b0a31-147">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="b0a31-147">-TtlInSeconds</span></span>
<span data-ttu-id="b0a31-148">Az alapértelmezett élettartam másodpercben</span><span class="sxs-lookup"><span data-stu-id="b0a31-148">Default Ttl in seconds.</span></span>
<span data-ttu-id="b0a31-149">Ha az érték hiányzik vagy a-1 érték van megadva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="b0a31-149">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="b0a31-150">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítási idő után lejárnak.</span><span class="sxs-lookup"><span data-stu-id="b0a31-150">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="b0a31-151">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="b0a31-151">-UniqueKeyPolicy</span></span>
<span data-ttu-id="b0a31-152">A UniqueKeyPolicy objektum a Microsoft. Azure. commands. CosmosDB. PSSqlUniqueKeyPolicy parancsot írja be.</span><span class="sxs-lookup"><span data-stu-id="b0a31-152">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="b0a31-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0a31-153">-WhatIf</span></span>
<span data-ttu-id="b0a31-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b0a31-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0a31-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0a31-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0a31-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a31-156">CommonParameters</span></span>
<span data-ttu-id="b0a31-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0a31-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a31-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b0a31-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a31-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0a31-159">INPUTS</span></span>

### <span data-ttu-id="b0a31-160">Microsoft. Azure. Command. CosmosDB. models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="b0a31-160">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="b0a31-161">Microsoft. Azure. Command. CosmosDB. models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="b0a31-161">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="b0a31-162">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b0a31-162">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="b0a31-163">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0a31-163">OUTPUTS</span></span>

### <span data-ttu-id="b0a31-164">Microsoft. Azure. Command. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="b0a31-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="b0a31-165">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0a31-165">NOTES</span></span>

## <span data-ttu-id="b0a31-166">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0a31-166">RELATED LINKS</span></span>
