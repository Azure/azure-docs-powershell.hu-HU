---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 7b773bd51a928c21761900cf1f6f8c34e73c2d0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144475"
---
# <span data-ttu-id="01b74-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="01b74-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="01b74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01b74-102">SYNOPSIS</span></span>
<span data-ttu-id="01b74-103">Létrehoz egy új Táblát, amely sql-tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="01b74-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="01b74-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01b74-104">SYNTAX</span></span>

### <span data-ttu-id="01b74-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01b74-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01b74-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01b74-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-AnalyticalStorageTtl <Int32>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01b74-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01b74-107">DESCRIPTION</span></span>
<span data-ttu-id="01b74-108">Létrehoz egy új Táblát, amely sql-tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="01b74-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="01b74-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01b74-109">EXAMPLES</span></span>

### <span data-ttu-id="01b74-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="01b74-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="01b74-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01b74-111">PARAMETERS</span></span>

### <span data-ttu-id="01b74-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01b74-112">-AccountName</span></span>
<span data-ttu-id="01b74-113">A Külön db-adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="01b74-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="01b74-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="01b74-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="01b74-115">TTL analitikus tároláshoz (másodpercben).</span><span class="sxs-lookup"><span data-stu-id="01b74-115">TTL for Analytical Storage (in Seconds).</span></span>

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

### <span data-ttu-id="01b74-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="01b74-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="01b74-117">Maximális átviteli sebesség, ha engedélyezve van az automatikus méretezés.</span><span class="sxs-lookup"><span data-stu-id="01b74-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="01b74-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01b74-118">-Confirm</span></span>
<span data-ttu-id="01b74-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="01b74-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01b74-120">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="01b74-120">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="01b74-121">ConflictResolutionPolicy object of type PSSqlConflictResolutionPolicy, ha ezt a tároló ConflictResolutionPolicy-ként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="01b74-121">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="01b74-122">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="01b74-122">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="01b74-123">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="01b74-123">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="01b74-124">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="01b74-124">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="01b74-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="01b74-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="01b74-126">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="01b74-126">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="01b74-127">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="01b74-127">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="01b74-128">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="01b74-128">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="01b74-129">A típus egyéni típusának meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="01b74-129">To be provided when the type is custom.</span></span>
<span data-ttu-id="01b74-130">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="01b74-130">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="01b74-131">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="01b74-131">-DatabaseName</span></span>
<span data-ttu-id="01b74-132">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="01b74-132">Database name.</span></span>

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

### <span data-ttu-id="01b74-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b74-133">-DefaultProfile</span></span>
<span data-ttu-id="01b74-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01b74-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01b74-135">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="01b74-135">-IndexingPolicy</span></span>
<span data-ttu-id="01b74-136">A Microsoft.Azure.Commands.Az indexelési házirend objektuma.Az indexelési házirendobjektum a Microsoft.Azure.Commands.AB.PSSqlIndexingPolicy típusú.</span><span class="sxs-lookup"><span data-stu-id="01b74-136">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="01b74-137">-Name</span><span class="sxs-lookup"><span data-stu-id="01b74-137">-Name</span></span>
<span data-ttu-id="01b74-138">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="01b74-138">Container name.</span></span>

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

### <span data-ttu-id="01b74-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="01b74-139">-ParentObject</span></span>
<span data-ttu-id="01b74-140">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="01b74-140">Sql Database object.</span></span>

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

### <span data-ttu-id="01b74-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="01b74-141">-PartitionKeyKind</span></span>
<span data-ttu-id="01b74-142">A partíciókhoz használt algoritmus fajtája.</span><span class="sxs-lookup"><span data-stu-id="01b74-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="01b74-143">Lehetséges értékek: "Kivonat", "Tartomány"</span><span class="sxs-lookup"><span data-stu-id="01b74-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="01b74-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="01b74-144">-PartitionKeyPath</span></span>
<span data-ttu-id="01b74-145">Partition key Path, pl.: '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="01b74-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="01b74-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="01b74-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="01b74-147">A partíciók kulcsdefiníciójának verziója</span><span class="sxs-lookup"><span data-stu-id="01b74-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="01b74-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01b74-148">-ResourceGroupName</span></span>
<span data-ttu-id="01b74-149">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="01b74-149">Name of resource group.</span></span>

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

### <span data-ttu-id="01b74-150">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="01b74-150">-Throughput</span></span>
<span data-ttu-id="01b74-151">Az SQL-tároló (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="01b74-151">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="01b74-152">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="01b74-152">Default value is 400.</span></span>

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

### <span data-ttu-id="01b74-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="01b74-153">-TtlInSeconds</span></span>
<span data-ttu-id="01b74-154">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="01b74-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="01b74-155">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="01b74-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="01b74-156">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="01b74-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="01b74-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="01b74-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="01b74-158">UniqueKeyPolicy object of type Microsoft.Azure.Commands.CossDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="01b74-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="01b74-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01b74-159">-WhatIf</span></span>
<span data-ttu-id="01b74-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="01b74-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01b74-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01b74-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01b74-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b74-162">CommonParameters</span></span>
<span data-ttu-id="01b74-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01b74-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b74-164">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01b74-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b74-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01b74-165">INPUTS</span></span>

### <span data-ttu-id="01b74-166">Microsoft.Azure.Commands.EzresDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="01b74-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="01b74-167">Microsoft.Azure.Commands.CossDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="01b74-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="01b74-168">Microsoft.Azure.Commands.EzresDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="01b74-168">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="01b74-169">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="01b74-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="01b74-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01b74-170">OUTPUTS</span></span>

### <span data-ttu-id="01b74-171">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="01b74-171">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="01b74-172">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="01b74-172">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="01b74-173">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01b74-173">NOTES</span></span>

## <span data-ttu-id="01b74-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01b74-174">RELATED LINKS</span></span>
