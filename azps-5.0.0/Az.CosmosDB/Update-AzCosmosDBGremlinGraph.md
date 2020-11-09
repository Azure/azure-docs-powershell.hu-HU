---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299051"
---
# <span data-ttu-id="4181c-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="4181c-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="4181c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4181c-102">SYNOPSIS</span></span>
<span data-ttu-id="4181c-103">Frissíti a CosmosDB Gremlin gráfot.</span><span class="sxs-lookup"><span data-stu-id="4181c-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="4181c-104">Ügyféloldali javítás műveletet hajt végre a meglévő grafikon elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="4181c-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="4181c-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4181c-105">SYNTAX</span></span>

### <span data-ttu-id="4181c-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4181c-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4181c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4181c-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4181c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4181c-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4181c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4181c-109">DESCRIPTION</span></span>
<span data-ttu-id="4181c-110">Frissíti a CosmosDB Gremlin gráfot.</span><span class="sxs-lookup"><span data-stu-id="4181c-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="4181c-111">Ügyféloldali javítás műveletet hajt végre a meglévő grafikon elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="4181c-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="4181c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4181c-112">EXAMPLES</span></span>

### <span data-ttu-id="4181c-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4181c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="4181c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4181c-114">PARAMETERS</span></span>

### <span data-ttu-id="4181c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4181c-115">-AccountName</span></span>
<span data-ttu-id="4181c-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="4181c-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4181c-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="4181c-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="4181c-118">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="4181c-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="4181c-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4181c-119">-Confirm</span></span>
<span data-ttu-id="4181c-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4181c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4181c-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="4181c-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="4181c-122">PSConflictResolutionPolicy ConflictResolutionPolicy objektum, ha ez a tároló ConflictResolutionPolicy van beállítva.</span><span class="sxs-lookup"><span data-stu-id="4181c-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="4181c-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="4181c-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="4181c-124">Megadhatja az értékeket: LastWriterWins, egyéni, manuális.</span><span class="sxs-lookup"><span data-stu-id="4181c-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="4181c-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="4181c-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="4181c-126">Adja meg, hogy a típus LastWriterWins-e.</span><span class="sxs-lookup"><span data-stu-id="4181c-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="4181c-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="4181c-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="4181c-128">Adja meg, ha a típus egyéni.</span><span class="sxs-lookup"><span data-stu-id="4181c-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="4181c-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4181c-129">-DatabaseName</span></span>
<span data-ttu-id="4181c-130">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="4181c-130">Database name.</span></span>

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

### <span data-ttu-id="4181c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4181c-131">-DefaultProfile</span></span>
<span data-ttu-id="4181c-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4181c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4181c-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="4181c-133">-IndexingPolicy</span></span>
<span data-ttu-id="4181c-134">Indexelő házirend-objektum a Microsoft. Azure. commands. CosmosDB. PSIndexingPolicy parancsot.</span><span class="sxs-lookup"><span data-stu-id="4181c-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="4181c-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4181c-135">-InputObject</span></span>
<span data-ttu-id="4181c-136">Gremlin gráf objektum.</span><span class="sxs-lookup"><span data-stu-id="4181c-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="4181c-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4181c-137">-Name</span></span>
<span data-ttu-id="4181c-138">Gremlin-diagram neve.</span><span class="sxs-lookup"><span data-stu-id="4181c-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="4181c-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4181c-139">-ParentObject</span></span>
<span data-ttu-id="4181c-140">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="4181c-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="4181c-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="4181c-141">-PartitionKeyKind</span></span>
<span data-ttu-id="4181c-142">A particionáláshoz használt algoritmus típusa.</span><span class="sxs-lookup"><span data-stu-id="4181c-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="4181c-143">A lehetséges értékek a következők: "hash", "tartománnyal"</span><span class="sxs-lookup"><span data-stu-id="4181c-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="4181c-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="4181c-144">-PartitionKeyPath</span></span>
<span data-ttu-id="4181c-145">A Partition kulcs elérési útja (például "/Address/zipcode").</span><span class="sxs-lookup"><span data-stu-id="4181c-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="4181c-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="4181c-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="4181c-147">A Partition Key definition verziója</span><span class="sxs-lookup"><span data-stu-id="4181c-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="4181c-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4181c-148">-ResourceGroupName</span></span>
<span data-ttu-id="4181c-149">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4181c-149">Name of resource group.</span></span>

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

### <span data-ttu-id="4181c-150">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="4181c-150">-Throughput</span></span>
<span data-ttu-id="4181c-151">A Gremlin gráf (RU/s) átviteli sebessége</span><span class="sxs-lookup"><span data-stu-id="4181c-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="4181c-152">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="4181c-152">Default value is 400.</span></span>

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

### <span data-ttu-id="4181c-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="4181c-153">-TtlInSeconds</span></span>
<span data-ttu-id="4181c-154">Az alapértelmezett élettartam másodpercben</span><span class="sxs-lookup"><span data-stu-id="4181c-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="4181c-155">Ha az érték hiányzik vagy a-1 érték van megadva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="4181c-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="4181c-156">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítási idő után lejárnak.</span><span class="sxs-lookup"><span data-stu-id="4181c-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="4181c-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="4181c-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="4181c-158">A UniqueKeyPolicy objektum a Microsoft. Azure. commands. CosmosDB. PSUniqueKeyPolicy parancsot írja be.</span><span class="sxs-lookup"><span data-stu-id="4181c-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="4181c-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4181c-159">-WhatIf</span></span>
<span data-ttu-id="4181c-160">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4181c-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4181c-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4181c-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4181c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4181c-162">CommonParameters</span></span>
<span data-ttu-id="4181c-163">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4181c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4181c-164">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4181c-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4181c-165">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4181c-165">INPUTS</span></span>

### <span data-ttu-id="4181c-166">Microsoft. Azure. Command. CosmosDB. models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="4181c-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="4181c-167">Microsoft. Azure. Command. CosmosDB. models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="4181c-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="4181c-168">Microsoft. Azure. Command. CosmosDB. models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="4181c-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="4181c-169">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="4181c-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="4181c-170">Microsoft. Azure. Command. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="4181c-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="4181c-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4181c-171">OUTPUTS</span></span>

### <span data-ttu-id="4181c-172">Microsoft. Azure. Command. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="4181c-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="4181c-173">Microsoft. Azure. Command. CosmosDB. kivétellel. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="4181c-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="4181c-174">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4181c-174">NOTES</span></span>

## <span data-ttu-id="4181c-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4181c-175">RELATED LINKS</span></span>
