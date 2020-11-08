---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: ab81c97048c64a08ab29877becfd44b690312a27
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182870"
---
# <span data-ttu-id="0513c-101">New-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="0513c-101">New-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="0513c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0513c-102">SYNOPSIS</span></span>
<span data-ttu-id="0513c-103">Új CosmosDB-Gremlin-gráfot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0513c-103">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="0513c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0513c-104">SYNTAX</span></span>

### <span data-ttu-id="0513c-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0513c-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String>
 -PartitionKeyPath <String[]> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0513c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0513c-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinGraph -Name <String> [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0513c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0513c-107">DESCRIPTION</span></span>
<span data-ttu-id="0513c-108">Új CosmosDB-Gremlin-gráfot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0513c-108">Creates a new CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="0513c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0513c-109">EXAMPLES</span></span>

### <span data-ttu-id="0513c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0513c-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="0513c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0513c-111">PARAMETERS</span></span>

### <span data-ttu-id="0513c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0513c-112">-AccountName</span></span>
<span data-ttu-id="0513c-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="0513c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0513c-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="0513c-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0513c-115">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="0513c-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0513c-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0513c-116">-Confirm</span></span>
<span data-ttu-id="0513c-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0513c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0513c-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0513c-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="0513c-119">PSConflictResolutionPolicy ConflictResolutionPolicy objektum, ha ez a tároló ConflictResolutionPolicy van beállítva.</span><span class="sxs-lookup"><span data-stu-id="0513c-119">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="0513c-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="0513c-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="0513c-121">Megadhatja az értékeket: LastWriterWins, egyéni, manuális.</span><span class="sxs-lookup"><span data-stu-id="0513c-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="0513c-122">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="0513c-122">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="0513c-123">Adja meg, hogy a típus LastWriterWins-e.</span><span class="sxs-lookup"><span data-stu-id="0513c-123">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="0513c-124">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="0513c-124">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="0513c-125">Adja meg, ha a típus egyéni.</span><span class="sxs-lookup"><span data-stu-id="0513c-125">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="0513c-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0513c-126">-DatabaseName</span></span>
<span data-ttu-id="0513c-127">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0513c-127">Database name.</span></span>

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

### <span data-ttu-id="0513c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0513c-128">-DefaultProfile</span></span>
<span data-ttu-id="0513c-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0513c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0513c-130">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="0513c-130">-IndexingPolicy</span></span>
<span data-ttu-id="0513c-131">Indexelő házirend-objektum a Microsoft. Azure. commands. CosmosDB. PSIndexingPolicy parancsot.</span><span class="sxs-lookup"><span data-stu-id="0513c-131">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="0513c-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0513c-132">-Name</span></span>
<span data-ttu-id="0513c-133">Gremlin-diagram neve.</span><span class="sxs-lookup"><span data-stu-id="0513c-133">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="0513c-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0513c-134">-ParentObject</span></span>
<span data-ttu-id="0513c-135">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="0513c-135">Gremlin Database object.</span></span>

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

### <span data-ttu-id="0513c-136">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="0513c-136">-PartitionKeyKind</span></span>
<span data-ttu-id="0513c-137">A particionáláshoz használt algoritmus típusa.</span><span class="sxs-lookup"><span data-stu-id="0513c-137">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="0513c-138">A lehetséges értékek a következők: "hash", "tartománnyal"</span><span class="sxs-lookup"><span data-stu-id="0513c-138">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="0513c-139">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="0513c-139">-PartitionKeyPath</span></span>
<span data-ttu-id="0513c-140">A Partition kulcs elérési útja (például "/Address/zipcode").</span><span class="sxs-lookup"><span data-stu-id="0513c-140">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="0513c-141">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="0513c-141">-PartitionKeyVersion</span></span>
<span data-ttu-id="0513c-142">A Partition Key definition verziója</span><span class="sxs-lookup"><span data-stu-id="0513c-142">The version of the partition key definition</span></span>

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

### <span data-ttu-id="0513c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0513c-143">-ResourceGroupName</span></span>
<span data-ttu-id="0513c-144">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0513c-144">Name of resource group.</span></span>

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

### <span data-ttu-id="0513c-145">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="0513c-145">-Throughput</span></span>
<span data-ttu-id="0513c-146">A Gremlin gráf (RU/s) átviteli sebessége</span><span class="sxs-lookup"><span data-stu-id="0513c-146">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="0513c-147">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="0513c-147">Default value is 400.</span></span>

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

### <span data-ttu-id="0513c-148">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="0513c-148">-TtlInSeconds</span></span>
<span data-ttu-id="0513c-149">Az alapértelmezett élettartam másodpercben</span><span class="sxs-lookup"><span data-stu-id="0513c-149">Default Ttl in seconds.</span></span>
<span data-ttu-id="0513c-150">Ha az érték hiányzik vagy a-1 érték van megadva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="0513c-150">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="0513c-151">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítási idő után lejárnak.</span><span class="sxs-lookup"><span data-stu-id="0513c-151">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="0513c-152">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="0513c-152">-UniqueKeyPolicy</span></span>
<span data-ttu-id="0513c-153">A UniqueKeyPolicy objektum a Microsoft. Azure. commands. CosmosDB. PSUniqueKeyPolicy parancsot írja be.</span><span class="sxs-lookup"><span data-stu-id="0513c-153">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="0513c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0513c-154">-WhatIf</span></span>
<span data-ttu-id="0513c-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0513c-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0513c-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0513c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0513c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0513c-157">CommonParameters</span></span>
<span data-ttu-id="0513c-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0513c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0513c-159">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0513c-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0513c-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0513c-160">INPUTS</span></span>

### <span data-ttu-id="0513c-161">Microsoft. Azure. Command. CosmosDB. models. PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="0513c-161">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="0513c-162">Microsoft. Azure. Command. CosmosDB. models. PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="0513c-162">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="0513c-163">Microsoft. Azure. Command. CosmosDB. models. PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="0513c-163">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="0513c-164">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0513c-164">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="0513c-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0513c-165">OUTPUTS</span></span>

### <span data-ttu-id="0513c-166">Microsoft. Azure. Command. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="0513c-166">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="0513c-167">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0513c-167">System.Exception</span></span>

## <span data-ttu-id="0513c-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0513c-168">NOTES</span></span>

## <span data-ttu-id="0513c-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0513c-169">RELATED LINKS</span></span>
