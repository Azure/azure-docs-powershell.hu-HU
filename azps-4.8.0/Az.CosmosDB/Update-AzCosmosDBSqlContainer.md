---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185074"
---
# <span data-ttu-id="2c169-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="2c169-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="2c169-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c169-102">SYNOPSIS</span></span>
<span data-ttu-id="2c169-103">Frissíti a CosmosDB SQL-tárolót.</span><span class="sxs-lookup"><span data-stu-id="2c169-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="2c169-104">Ügyféloldali javítás műveletet hajt végre a meglévő tároló olvasásával.</span><span class="sxs-lookup"><span data-stu-id="2c169-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="2c169-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c169-105">SYNTAX</span></span>

### <span data-ttu-id="2c169-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c169-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c169-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c169-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c169-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c169-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c169-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c169-109">DESCRIPTION</span></span>
<span data-ttu-id="2c169-110">Frissíti a CosmosDB SQL-tárolót.</span><span class="sxs-lookup"><span data-stu-id="2c169-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="2c169-111">Ügyféloldali javítás műveletet hajt végre a meglévő tároló olvasásával.</span><span class="sxs-lookup"><span data-stu-id="2c169-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="2c169-112">Példák</span><span class="sxs-lookup"><span data-stu-id="2c169-112">EXAMPLES</span></span>

### <span data-ttu-id="2c169-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2c169-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="2c169-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c169-114">PARAMETERS</span></span>

### <span data-ttu-id="2c169-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2c169-115">-AccountName</span></span>
<span data-ttu-id="2c169-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="2c169-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2c169-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="2c169-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="2c169-118">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2c169-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="2c169-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c169-119">-Confirm</span></span>
<span data-ttu-id="2c169-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c169-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c169-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="2c169-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="2c169-122">PSSqlConflictResolutionPolicy ConflictResolutionPolicy objektum, ha ez a tároló ConflictResolutionPolicy van beállítva.</span><span class="sxs-lookup"><span data-stu-id="2c169-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSSqlConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c169-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="2c169-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="2c169-124">Megadhatja az értékeket: LastWriterWins, egyéni, manuális.</span><span class="sxs-lookup"><span data-stu-id="2c169-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="2c169-125">Ha a ConflictResolutionPolicy paraméterrel együtt az érték van megadva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="2c169-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="2c169-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="2c169-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="2c169-127">Adja meg, hogy a típus LastWriterWins-e.</span><span class="sxs-lookup"><span data-stu-id="2c169-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="2c169-128">Ha a ConflictResolutionPolicy paraméterrel együtt az érték van megadva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="2c169-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="2c169-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="2c169-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="2c169-130">Adja meg, ha a típus egyéni.</span><span class="sxs-lookup"><span data-stu-id="2c169-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="2c169-131">Ha a ConflictResolutionPolicy paraméterrel együtt az érték van megadva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="2c169-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="2c169-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c169-132">-DatabaseName</span></span>
<span data-ttu-id="2c169-133">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="2c169-133">Database name.</span></span>

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

### <span data-ttu-id="2c169-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c169-134">-DefaultProfile</span></span>
<span data-ttu-id="2c169-135">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c169-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c169-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="2c169-136">-IndexingPolicy</span></span>
<span data-ttu-id="2c169-137">Indexelő házirend-objektum a Microsoft. Azure. commands. CosmosDB. PSSqlIndexingPolicy parancsot.</span><span class="sxs-lookup"><span data-stu-id="2c169-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSSqlIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c169-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c169-138">-InputObject</span></span>
<span data-ttu-id="2c169-139">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="2c169-139">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c169-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c169-140">-Name</span></span>
<span data-ttu-id="2c169-141">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="2c169-141">Container name.</span></span>

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

### <span data-ttu-id="2c169-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2c169-142">-ParentObject</span></span>
<span data-ttu-id="2c169-143">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="2c169-143">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c169-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="2c169-144">-PartitionKeyKind</span></span>
<span data-ttu-id="2c169-145">A particionáláshoz használt algoritmus típusa.</span><span class="sxs-lookup"><span data-stu-id="2c169-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="2c169-146">A lehetséges értékek a következők: "hash", "tartománnyal"</span><span class="sxs-lookup"><span data-stu-id="2c169-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="2c169-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="2c169-147">-PartitionKeyPath</span></span>
<span data-ttu-id="2c169-148">A Partition kulcs elérési útja (például "/Address/zipcode").</span><span class="sxs-lookup"><span data-stu-id="2c169-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="2c169-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="2c169-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="2c169-150">A Partition Key definition verziója</span><span class="sxs-lookup"><span data-stu-id="2c169-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="2c169-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c169-151">-ResourceGroupName</span></span>
<span data-ttu-id="2c169-152">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2c169-152">Name of resource group.</span></span>

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

### <span data-ttu-id="2c169-153">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="2c169-153">-Throughput</span></span>
<span data-ttu-id="2c169-154">Az SQL-tároló (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="2c169-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="2c169-155">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="2c169-155">Default value is 400.</span></span>

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

### <span data-ttu-id="2c169-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="2c169-156">-TtlInSeconds</span></span>
<span data-ttu-id="2c169-157">Az alapértelmezett élettartam másodpercben</span><span class="sxs-lookup"><span data-stu-id="2c169-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="2c169-158">Ha az érték hiányzik vagy a-1 érték van megadva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="2c169-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="2c169-159">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítási idő után lejárnak.</span><span class="sxs-lookup"><span data-stu-id="2c169-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="2c169-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="2c169-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="2c169-161">A UniqueKeyPolicy objektum a Microsoft. Azure. commands. CosmosDB. PSSqlUniqueKeyPolicy parancsot írja be.</span><span class="sxs-lookup"><span data-stu-id="2c169-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSSqlUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c169-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c169-162">-WhatIf</span></span>
<span data-ttu-id="2c169-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c169-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c169-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c169-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c169-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c169-165">CommonParameters</span></span>
<span data-ttu-id="2c169-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c169-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c169-167">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2c169-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c169-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c169-168">INPUTS</span></span>

### <span data-ttu-id="2c169-169">Microsoft. Azure. Command. CosmosDB. models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="2c169-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="2c169-170">Microsoft. Azure. Command. CosmosDB. models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="2c169-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="2c169-171">Microsoft. Azure. Command. CosmosDB. models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="2c169-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="2c169-172">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2c169-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="2c169-173">Microsoft. Azure. Command. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="2c169-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="2c169-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c169-174">OUTPUTS</span></span>

### <span data-ttu-id="2c169-175">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2c169-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="2c169-176">Microsoft. Azure. Command. CosmosDB. kivétellel. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="2c169-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="2c169-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c169-177">NOTES</span></span>

## <span data-ttu-id="2c169-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c169-178">RELATED LINKS</span></span>
