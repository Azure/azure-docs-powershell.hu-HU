---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 83c26ff0a05a88540563b7e3867c2e1d6ac12be0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014425"
---
# <span data-ttu-id="e2b4d-101">Set-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="e2b4d-101">Set-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="e2b4d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b4d-103">Új SQL-tárolót hoz létre vagy frissít egy meglévő CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-103">Creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="e2b4d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2b4d-104">SYNTAX</span></span>

### <span data-ttu-id="e2b4d-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2b4d-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2b4d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2b4d-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2b4d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2b4d-107">DESCRIPTION</span></span>
<span data-ttu-id="e2b4d-108">A **set-AzCosmosDBSqlContainer** parancsmag új, meglévő CosmosDB SQL-tárolót hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-108">The **Set-AzCosmosDBSqlContainer** cmdlet creates a new or updates an existing CosmosDB Sql Container.</span></span>

## <span data-ttu-id="e2b4d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e2b4d-109">EXAMPLES</span></span>

### <span data-ttu-id="e2b4d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e2b4d-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName} -PartitionKeyKind Hash -PartitionKeyPath {samplePath}

Name                     : {containerName}
Id                       : {containerId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="e2b4d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2b4d-111">PARAMETERS</span></span>

### <span data-ttu-id="e2b4d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e2b4d-112">-AccountName</span></span>
<span data-ttu-id="e2b4d-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e2b4d-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2b4d-114">-Confirm</span></span>
<span data-ttu-id="e2b4d-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2b4d-116">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e2b4d-116">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="e2b4d-117">PSSqlConflictResolutionPolicy ConflictResolutionPolicy objektum, ha ez a tároló ConflictResolutionPolicy van beállítva.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-117">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="e2b4d-118">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="e2b4d-118">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="e2b4d-119">Megadhatja az értékeket: LastWriterWins, egyéni, manuális.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="e2b4d-120">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="e2b4d-120">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="e2b4d-121">Adja meg, hogy a típus LastWriterWins-e.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-121">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="e2b4d-122">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="e2b4d-122">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="e2b4d-123">Adja meg, ha a típus egyéni.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-123">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="e2b4d-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e2b4d-124">-DatabaseName</span></span>
<span data-ttu-id="e2b4d-125">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-125">Database name.</span></span>

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

### <span data-ttu-id="e2b4d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b4d-126">-DefaultProfile</span></span>
<span data-ttu-id="e2b4d-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2b4d-128">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e2b4d-128">-IndexingPolicy</span></span>
<span data-ttu-id="e2b4d-129">Indexelő házirend-objektum a Microsoft. Azure. commands. CosmosDB. PSSqlIndexingPolicy parancsot.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-129">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="e2b4d-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2b4d-130">-InputObject</span></span>
<span data-ttu-id="e2b4d-131">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-131">Sql Database object.</span></span>

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

### <span data-ttu-id="e2b4d-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2b4d-132">-Name</span></span>
<span data-ttu-id="e2b4d-133">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-133">Container name.</span></span>

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

### <span data-ttu-id="e2b4d-134">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="e2b4d-134">-PartitionKeyKind</span></span>
<span data-ttu-id="e2b4d-135">A particionáláshoz használt algoritmus típusa.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-135">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="e2b4d-136">A lehetséges értékek a következők: "hash", "tartománnyal"</span><span class="sxs-lookup"><span data-stu-id="e2b4d-136">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="e2b4d-137">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="e2b4d-137">-PartitionKeyPath</span></span>
<span data-ttu-id="e2b4d-138">A Partition kulcs elérési útja (például "/Address/zipcode").</span><span class="sxs-lookup"><span data-stu-id="e2b4d-138">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="e2b4d-139">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e2b4d-139">-PartitionKeyVersion</span></span>
<span data-ttu-id="e2b4d-140">A Partition Key definition verziója</span><span class="sxs-lookup"><span data-stu-id="e2b4d-140">The version of the partition key definition</span></span>

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

### <span data-ttu-id="e2b4d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b4d-141">-ResourceGroupName</span></span>
<span data-ttu-id="e2b4d-142">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-142">Name of resource group.</span></span>

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

### <span data-ttu-id="e2b4d-143">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="e2b4d-143">-Throughput</span></span>
<span data-ttu-id="e2b4d-144">Az SQL-tároló (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-144">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="e2b4d-145">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-145">Default value is 400.</span></span>

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

### <span data-ttu-id="e2b4d-146">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="e2b4d-146">-TtlInSeconds</span></span>
<span data-ttu-id="e2b4d-147">Az alapértelmezett élettartam másodpercben</span><span class="sxs-lookup"><span data-stu-id="e2b4d-147">Default Ttl in seconds.</span></span>
<span data-ttu-id="e2b4d-148">Ha az érték hiányzik vagy a-1 érték van megadva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-148">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="e2b4d-149">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítási idő után lejárnak.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-149">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="e2b4d-150">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e2b4d-150">-UniqueKeyPolicy</span></span>
<span data-ttu-id="e2b4d-151">A UniqueKeyPolicy objektum a Microsoft. Azure. commands. CosmosDB. PSSqlUniqueKeyPolicy parancsot írja be.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-151">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="e2b4d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2b4d-152">-WhatIf</span></span>
<span data-ttu-id="e2b4d-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2b4d-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2b4d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b4d-155">CommonParameters</span></span>
<span data-ttu-id="e2b4d-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2b4d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b4d-157">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e2b4d-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b4d-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2b4d-158">INPUTS</span></span>

### <span data-ttu-id="e2b4d-159">Nincs</span><span class="sxs-lookup"><span data-stu-id="e2b4d-159">None</span></span>

## <span data-ttu-id="e2b4d-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2b4d-160">OUTPUTS</span></span>

### <span data-ttu-id="e2b4d-161">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e2b4d-161">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="e2b4d-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2b4d-162">NOTES</span></span>

## <span data-ttu-id="e2b4d-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2b4d-163">RELATED LINKS</span></span>
