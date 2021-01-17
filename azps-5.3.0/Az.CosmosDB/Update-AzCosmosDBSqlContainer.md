---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 85f220c7745f28a2786e9a26edc86baa129c3c3c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480523"
---
# <span data-ttu-id="637a4-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="637a4-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="637a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="637a4-102">SYNOPSIS</span></span>
<span data-ttu-id="637a4-103">Frissíti aFrissítésekDB sql-tárolót.</span><span class="sxs-lookup"><span data-stu-id="637a4-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="637a4-104">Ügyféloldali javítást hajt végre a meglévő tároló olvasásával.</span><span class="sxs-lookup"><span data-stu-id="637a4-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="637a4-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="637a4-105">SYNTAX</span></span>

### <span data-ttu-id="637a4-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="637a4-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="637a4-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="637a4-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="637a4-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="637a4-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="637a4-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="637a4-109">DESCRIPTION</span></span>
<span data-ttu-id="637a4-110">Frissíti aFrissítésekDB sql-tárolót.</span><span class="sxs-lookup"><span data-stu-id="637a4-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="637a4-111">Ügyféloldali javítást hajt végre a meglévő tároló olvasásával.</span><span class="sxs-lookup"><span data-stu-id="637a4-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="637a4-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="637a4-112">EXAMPLES</span></span>

### <span data-ttu-id="637a4-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="637a4-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="637a4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="637a4-114">PARAMETERS</span></span>

### <span data-ttu-id="637a4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="637a4-115">-AccountName</span></span>
<span data-ttu-id="637a4-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="637a4-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="637a4-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="637a4-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="637a4-118">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="637a4-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="637a4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="637a4-119">-Confirm</span></span>
<span data-ttu-id="637a4-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="637a4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="637a4-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="637a4-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="637a4-122">ConflictResolutionPolicy object of type PSSqlConflictResolutionPolicy, ha ezt a tároló ConflictResolutionPolicy-ként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="637a4-122">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="637a4-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="637a4-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="637a4-124">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="637a4-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="637a4-125">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="637a4-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="637a4-126">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="637a4-126">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="637a4-127">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="637a4-127">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="637a4-128">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="637a4-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="637a4-129">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="637a4-129">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="637a4-130">Egyéni típushoz meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="637a4-130">To be provided when the type is custom.</span></span>
<span data-ttu-id="637a4-131">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="637a4-131">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="637a4-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="637a4-132">-DatabaseName</span></span>
<span data-ttu-id="637a4-133">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="637a4-133">Database name.</span></span>

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

### <span data-ttu-id="637a4-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="637a4-134">-DefaultProfile</span></span>
<span data-ttu-id="637a4-135">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="637a4-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="637a4-136">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="637a4-136">-IndexingPolicy</span></span>
<span data-ttu-id="637a4-137">A Microsoft.Azure.Commands.Az indexelési házirend objektuma.Az indexelési házirendobjektum a Microsoft.Azure.Commands.AB.PSSqlIndexingPolicy típusú.</span><span class="sxs-lookup"><span data-stu-id="637a4-137">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="637a4-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="637a4-138">-InputObject</span></span>
<span data-ttu-id="637a4-139">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="637a4-139">Sql Container object.</span></span>

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

### <span data-ttu-id="637a4-140">-Name</span><span class="sxs-lookup"><span data-stu-id="637a4-140">-Name</span></span>
<span data-ttu-id="637a4-141">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="637a4-141">Container name.</span></span>

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

### <span data-ttu-id="637a4-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="637a4-142">-ParentObject</span></span>
<span data-ttu-id="637a4-143">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="637a4-143">Sql Database object.</span></span>

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

### <span data-ttu-id="637a4-144">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="637a4-144">-PartitionKeyKind</span></span>
<span data-ttu-id="637a4-145">A partíciókhoz használt algoritmus fajtája.</span><span class="sxs-lookup"><span data-stu-id="637a4-145">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="637a4-146">Lehetséges értékek: "Kivonat", "Tartomány"</span><span class="sxs-lookup"><span data-stu-id="637a4-146">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="637a4-147">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="637a4-147">-PartitionKeyPath</span></span>
<span data-ttu-id="637a4-148">Partition key Path, pl.: '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="637a4-148">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="637a4-149">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="637a4-149">-PartitionKeyVersion</span></span>
<span data-ttu-id="637a4-150">A partíciók kulcsdefiníciójának verziója</span><span class="sxs-lookup"><span data-stu-id="637a4-150">The version of the partition key definition</span></span>

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

### <span data-ttu-id="637a4-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="637a4-151">-ResourceGroupName</span></span>
<span data-ttu-id="637a4-152">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="637a4-152">Name of resource group.</span></span>

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

### <span data-ttu-id="637a4-153">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="637a4-153">-Throughput</span></span>
<span data-ttu-id="637a4-154">Az SQL-tároló (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="637a4-154">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="637a4-155">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="637a4-155">Default value is 400.</span></span>

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

### <span data-ttu-id="637a4-156">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="637a4-156">-TtlInSeconds</span></span>
<span data-ttu-id="637a4-157">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="637a4-157">Default Ttl in seconds.</span></span>
<span data-ttu-id="637a4-158">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="637a4-158">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="637a4-159">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="637a4-159">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="637a4-160">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="637a4-160">-UniqueKeyPolicy</span></span>
<span data-ttu-id="637a4-161">UniqueKeyPolicy object of type Microsoft.Azure.Commands.CossDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="637a4-161">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="637a4-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="637a4-162">-WhatIf</span></span>
<span data-ttu-id="637a4-163">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="637a4-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="637a4-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="637a4-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="637a4-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="637a4-165">CommonParameters</span></span>
<span data-ttu-id="637a4-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="637a4-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="637a4-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="637a4-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="637a4-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="637a4-168">INPUTS</span></span>

### <span data-ttu-id="637a4-169">Microsoft.Azure.Commands.EzresDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="637a4-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="637a4-170">Microsoft.Azure.Commands.CossDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="637a4-170">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="637a4-171">Microsoft.Azure.Commands.EzresDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="637a4-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="637a4-172">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="637a4-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="637a4-173">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="637a4-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="637a4-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="637a4-174">OUTPUTS</span></span>

### <span data-ttu-id="637a4-175">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="637a4-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="637a4-176">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="637a4-176">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="637a4-177">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="637a4-177">NOTES</span></span>

## <span data-ttu-id="637a4-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="637a4-178">RELATED LINKS</span></span>
