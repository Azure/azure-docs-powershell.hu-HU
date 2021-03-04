---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlContainer.md
ms.openlocfilehash: a36222b3a6cacf567fd0b5e7541c2dc53a44fa22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931249"
---
# <span data-ttu-id="e7d43-101">Update-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="e7d43-101">Update-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="e7d43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7d43-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d43-103">Frissíti aFrissítésekDB sql-tárolót.</span><span class="sxs-lookup"><span data-stu-id="e7d43-103">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="e7d43-104">Ügyféloldali javítást hajt végre a meglévő tároló olvasásával.</span><span class="sxs-lookup"><span data-stu-id="e7d43-104">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="e7d43-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e7d43-105">SYNTAX</span></span>

### <span data-ttu-id="e7d43-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7d43-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7d43-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7d43-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] -ParentObject <PSSqlDatabaseGetResults>
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7d43-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7d43-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlContainer [-Name <String>] [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>] [-AnalyticalStorageTtl <Int32>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7d43-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e7d43-109">DESCRIPTION</span></span>
<span data-ttu-id="e7d43-110">Frissíti aFrissítésekDB sql-tárolót.</span><span class="sxs-lookup"><span data-stu-id="e7d43-110">Updates the CosmosDB Sql Container.</span></span> <span data-ttu-id="e7d43-111">Ügyféloldali javítást hajt végre a meglévő tároló olvasásával.</span><span class="sxs-lookup"><span data-stu-id="e7d43-111">Performs a client side patch operation by reading the existing Container.</span></span>

## <span data-ttu-id="e7d43-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e7d43-112">EXAMPLES</span></span>

### <span data-ttu-id="e7d43-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="e7d43-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 800

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

## <span data-ttu-id="e7d43-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7d43-114">PARAMETERS</span></span>

### <span data-ttu-id="e7d43-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e7d43-115">-AccountName</span></span>
<span data-ttu-id="e7d43-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="e7d43-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e7d43-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="e7d43-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="e7d43-118">TTL analitikus tároláshoz (másodpercben).</span><span class="sxs-lookup"><span data-stu-id="e7d43-118">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="e7d43-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="e7d43-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="e7d43-120">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="e7d43-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="e7d43-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7d43-121">-Confirm</span></span>
<span data-ttu-id="e7d43-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e7d43-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d43-123">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e7d43-123">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="e7d43-124">ConflictResolutionPolicy object of type PSSqlConflictResolutionPolicy, ha ezt a tároló ConflictResolutionPolicy-ként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="e7d43-124">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="e7d43-125">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="e7d43-125">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="e7d43-126">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="e7d43-126">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="e7d43-127">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="e7d43-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="e7d43-128">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="e7d43-128">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="e7d43-129">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="e7d43-129">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="e7d43-130">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="e7d43-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="e7d43-131">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="e7d43-131">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="e7d43-132">Egyéni típushoz meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="e7d43-132">To be provided when the type is custom.</span></span>
<span data-ttu-id="e7d43-133">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="e7d43-133">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="e7d43-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7d43-134">-DatabaseName</span></span>
<span data-ttu-id="e7d43-135">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e7d43-135">Database name.</span></span>

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

### <span data-ttu-id="e7d43-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d43-136">-DefaultProfile</span></span>
<span data-ttu-id="e7d43-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7d43-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7d43-138">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e7d43-138">-IndexingPolicy</span></span>
<span data-ttu-id="e7d43-139">A Microsoft.Azure.Commands.Az indexelési házirend objektuma.Az indexelési házirendobjektum a Microsoft.Azure.Commands.AB.PSSqlIndexingPolicy típusú.</span><span class="sxs-lookup"><span data-stu-id="e7d43-139">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="e7d43-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7d43-140">-InputObject</span></span>
<span data-ttu-id="e7d43-141">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="e7d43-141">Sql Container object.</span></span>

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

### <span data-ttu-id="e7d43-142">-Name</span><span class="sxs-lookup"><span data-stu-id="e7d43-142">-Name</span></span>
<span data-ttu-id="e7d43-143">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="e7d43-143">Container name.</span></span>

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

### <span data-ttu-id="e7d43-144">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e7d43-144">-ParentObject</span></span>
<span data-ttu-id="e7d43-145">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="e7d43-145">Sql Database object.</span></span>

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

### <span data-ttu-id="e7d43-146">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="e7d43-146">-PartitionKeyKind</span></span>
<span data-ttu-id="e7d43-147">A partíciókhoz használt algoritmus fajtája.</span><span class="sxs-lookup"><span data-stu-id="e7d43-147">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="e7d43-148">Lehetséges értékek: "Kivonat", "Tartomány"</span><span class="sxs-lookup"><span data-stu-id="e7d43-148">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="e7d43-149">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="e7d43-149">-PartitionKeyPath</span></span>
<span data-ttu-id="e7d43-150">Partition key Path, pl.: '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="e7d43-150">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="e7d43-151">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e7d43-151">-PartitionKeyVersion</span></span>
<span data-ttu-id="e7d43-152">A partíciók kulcsdefiníciójának verziója</span><span class="sxs-lookup"><span data-stu-id="e7d43-152">The version of the partition key definition</span></span>

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

### <span data-ttu-id="e7d43-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d43-153">-ResourceGroupName</span></span>
<span data-ttu-id="e7d43-154">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e7d43-154">Name of resource group.</span></span>

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

### <span data-ttu-id="e7d43-155">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="e7d43-155">-Throughput</span></span>
<span data-ttu-id="e7d43-156">Az SQL-tároló (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="e7d43-156">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="e7d43-157">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="e7d43-157">Default value is 400.</span></span>

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

### <span data-ttu-id="e7d43-158">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="e7d43-158">-TtlInSeconds</span></span>
<span data-ttu-id="e7d43-159">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="e7d43-159">Default Ttl in seconds.</span></span>
<span data-ttu-id="e7d43-160">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="e7d43-160">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="e7d43-161">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="e7d43-161">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="e7d43-162">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e7d43-162">-UniqueKeyPolicy</span></span>
<span data-ttu-id="e7d43-163">UniqueKeyPolicy object of type Microsoft.Azure.Commands.CossDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="e7d43-163">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="e7d43-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d43-164">-WhatIf</span></span>
<span data-ttu-id="e7d43-165">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e7d43-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d43-166">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7d43-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d43-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d43-167">CommonParameters</span></span>
<span data-ttu-id="e7d43-168">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7d43-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d43-169">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7d43-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d43-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7d43-170">INPUTS</span></span>

### <span data-ttu-id="e7d43-171">Microsoft.Azure.Commands.EzresDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="e7d43-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="e7d43-172">Microsoft.Azure.Commands.CossDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e7d43-172">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="e7d43-173">Microsoft.Azure.Commands.EzresDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="e7d43-173">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="e7d43-174">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e7d43-174">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="e7d43-175">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e7d43-175">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="e7d43-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7d43-176">OUTPUTS</span></span>

### <span data-ttu-id="e7d43-177">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="e7d43-177">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="e7d43-178">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="e7d43-178">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="e7d43-179">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e7d43-179">NOTES</span></span>

## <span data-ttu-id="e7d43-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7d43-180">RELATED LINKS</span></span>
