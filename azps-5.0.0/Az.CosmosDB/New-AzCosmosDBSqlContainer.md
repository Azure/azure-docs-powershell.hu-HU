---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299267"
---
# <span data-ttu-id="78173-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="78173-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="78173-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78173-102">SYNOPSIS</span></span>
<span data-ttu-id="78173-103">Új CosmosDB SQL-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="78173-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="78173-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78173-104">SYNTAX</span></span>

### <span data-ttu-id="78173-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78173-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78173-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78173-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78173-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="78173-107">DESCRIPTION</span></span>
<span data-ttu-id="78173-108">Új CosmosDB SQL-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="78173-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="78173-109">Példák</span><span class="sxs-lookup"><span data-stu-id="78173-109">EXAMPLES</span></span>

### <span data-ttu-id="78173-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="78173-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="78173-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78173-111">PARAMETERS</span></span>

### <span data-ttu-id="78173-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78173-112">-AccountName</span></span>
<span data-ttu-id="78173-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="78173-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="78173-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="78173-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="78173-115">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="78173-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="78173-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78173-116">-Confirm</span></span>
<span data-ttu-id="78173-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78173-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78173-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="78173-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="78173-119">PSSqlConflictResolutionPolicy ConflictResolutionPolicy objektum, ha ez a tároló ConflictResolutionPolicy van beállítva.</span><span class="sxs-lookup"><span data-stu-id="78173-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="78173-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="78173-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="78173-121">Megadhatja az értékeket: LastWriterWins, egyéni, manuális.</span><span class="sxs-lookup"><span data-stu-id="78173-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="78173-122">Ha a ConflictResolutionPolicy paraméterrel együtt az érték van megadva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="78173-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="78173-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="78173-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="78173-124">Adja meg, hogy a típus LastWriterWins-e.</span><span class="sxs-lookup"><span data-stu-id="78173-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="78173-125">Ha a ConflictResolutionPolicy paraméterrel együtt az érték van megadva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="78173-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="78173-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="78173-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="78173-127">Adja meg, ha a típus egyéni.</span><span class="sxs-lookup"><span data-stu-id="78173-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="78173-128">Ha a ConflictResolutionPolicy paraméterrel együtt az érték van megadva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="78173-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="78173-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78173-129">-DatabaseName</span></span>
<span data-ttu-id="78173-130">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="78173-130">Database name.</span></span>

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

### <span data-ttu-id="78173-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78173-131">-DefaultProfile</span></span>
<span data-ttu-id="78173-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78173-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78173-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="78173-133">-IndexingPolicy</span></span>
<span data-ttu-id="78173-134">Indexelő házirend-objektum a Microsoft. Azure. commands. CosmosDB. PSSqlIndexingPolicy parancsot.</span><span class="sxs-lookup"><span data-stu-id="78173-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="78173-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="78173-135">-Name</span></span>
<span data-ttu-id="78173-136">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="78173-136">Container name.</span></span>

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

### <span data-ttu-id="78173-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="78173-137">-ParentObject</span></span>
<span data-ttu-id="78173-138">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="78173-138">Sql Database object.</span></span>

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

### <span data-ttu-id="78173-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="78173-139">-PartitionKeyKind</span></span>
<span data-ttu-id="78173-140">A particionáláshoz használt algoritmus típusa.</span><span class="sxs-lookup"><span data-stu-id="78173-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="78173-141">A lehetséges értékek a következők: "hash", "tartománnyal"</span><span class="sxs-lookup"><span data-stu-id="78173-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="78173-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="78173-142">-PartitionKeyPath</span></span>
<span data-ttu-id="78173-143">A Partition kulcs elérési útja (például "/Address/zipcode").</span><span class="sxs-lookup"><span data-stu-id="78173-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="78173-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="78173-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="78173-145">A Partition Key definition verziója</span><span class="sxs-lookup"><span data-stu-id="78173-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="78173-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78173-146">-ResourceGroupName</span></span>
<span data-ttu-id="78173-147">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="78173-147">Name of resource group.</span></span>

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

### <span data-ttu-id="78173-148">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="78173-148">-Throughput</span></span>
<span data-ttu-id="78173-149">Az SQL-tároló (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="78173-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="78173-150">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="78173-150">Default value is 400.</span></span>

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

### <span data-ttu-id="78173-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="78173-151">-TtlInSeconds</span></span>
<span data-ttu-id="78173-152">Az alapértelmezett élettartam másodpercben</span><span class="sxs-lookup"><span data-stu-id="78173-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="78173-153">Ha az érték hiányzik vagy a-1 érték van megadva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="78173-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="78173-154">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítási idő után lejárnak.</span><span class="sxs-lookup"><span data-stu-id="78173-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="78173-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="78173-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="78173-156">A UniqueKeyPolicy objektum a Microsoft. Azure. commands. CosmosDB. PSSqlUniqueKeyPolicy parancsot írja be.</span><span class="sxs-lookup"><span data-stu-id="78173-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="78173-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78173-157">-WhatIf</span></span>
<span data-ttu-id="78173-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="78173-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78173-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78173-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78173-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78173-160">CommonParameters</span></span>
<span data-ttu-id="78173-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78173-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78173-162">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="78173-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78173-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78173-163">INPUTS</span></span>

### <span data-ttu-id="78173-164">Microsoft. Azure. Command. CosmosDB. models. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="78173-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="78173-165">Microsoft. Azure. Command. CosmosDB. models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="78173-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="78173-166">Microsoft. Azure. Command. CosmosDB. models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="78173-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="78173-167">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="78173-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="78173-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78173-168">OUTPUTS</span></span>

### <span data-ttu-id="78173-169">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="78173-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="78173-170">Microsoft. Azure. Command. CosmosDB. kivétellel. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="78173-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="78173-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78173-171">NOTES</span></span>

## <span data-ttu-id="78173-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78173-172">RELATED LINKS</span></span>
