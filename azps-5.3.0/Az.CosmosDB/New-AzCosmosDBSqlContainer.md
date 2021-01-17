---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477422"
---
# <span data-ttu-id="cea12-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="cea12-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="cea12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cea12-102">SYNOPSIS</span></span>
<span data-ttu-id="cea12-103">Létrehoz egy új tárolót a 2010.012.012.0125-201</span><span class="sxs-lookup"><span data-stu-id="cea12-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="cea12-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cea12-104">SYNTAX</span></span>

### <span data-ttu-id="cea12-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cea12-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cea12-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cea12-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cea12-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cea12-107">DESCRIPTION</span></span>
<span data-ttu-id="cea12-108">Létrehoz egy új tárolót a 2010.012.012.0125-201</span><span class="sxs-lookup"><span data-stu-id="cea12-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="cea12-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cea12-109">EXAMPLES</span></span>

### <span data-ttu-id="cea12-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="cea12-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="cea12-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cea12-111">PARAMETERS</span></span>

### <span data-ttu-id="cea12-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cea12-112">-AccountName</span></span>
<span data-ttu-id="cea12-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="cea12-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cea12-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="cea12-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="cea12-115">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="cea12-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="cea12-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cea12-116">-Confirm</span></span>
<span data-ttu-id="cea12-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cea12-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea12-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="cea12-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="cea12-119">ConflictResolutionPolicy object of type PSSqlConflictResolutionPolicy, ha ezt a tároló ConflictResolutionPolicy-ként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="cea12-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="cea12-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="cea12-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="cea12-121">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="cea12-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="cea12-122">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="cea12-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="cea12-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="cea12-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="cea12-124">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="cea12-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="cea12-125">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="cea12-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="cea12-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="cea12-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="cea12-127">Egyéni típushoz meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="cea12-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="cea12-128">Ha a ConflictResolutionPolicy paraméterrel együtt meg van adva, akkor a program figyelmen kívül hagyja.</span><span class="sxs-lookup"><span data-stu-id="cea12-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="cea12-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cea12-129">-DatabaseName</span></span>
<span data-ttu-id="cea12-130">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="cea12-130">Database name.</span></span>

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

### <span data-ttu-id="cea12-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea12-131">-DefaultProfile</span></span>
<span data-ttu-id="cea12-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cea12-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cea12-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="cea12-133">-IndexingPolicy</span></span>
<span data-ttu-id="cea12-134">A Microsoft.Azure.Commands.Az indexelési házirend objektuma.Az indexelési házirendobjektum a Microsoft.Azure.Commands.AB.PSSqlIndexingPolicy típusú.</span><span class="sxs-lookup"><span data-stu-id="cea12-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

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

### <span data-ttu-id="cea12-135">-Name</span><span class="sxs-lookup"><span data-stu-id="cea12-135">-Name</span></span>
<span data-ttu-id="cea12-136">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="cea12-136">Container name.</span></span>

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

### <span data-ttu-id="cea12-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cea12-137">-ParentObject</span></span>
<span data-ttu-id="cea12-138">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="cea12-138">Sql Database object.</span></span>

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

### <span data-ttu-id="cea12-139">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="cea12-139">-PartitionKeyKind</span></span>
<span data-ttu-id="cea12-140">A partíciókhoz használt algoritmus fajtája.</span><span class="sxs-lookup"><span data-stu-id="cea12-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="cea12-141">Lehetséges értékek: "Kivonat", "Tartomány"</span><span class="sxs-lookup"><span data-stu-id="cea12-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="cea12-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="cea12-142">-PartitionKeyPath</span></span>
<span data-ttu-id="cea12-143">Partition key Path, pl.: '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="cea12-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="cea12-144">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="cea12-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="cea12-145">A partíciók kulcsdefiníciójának verziója</span><span class="sxs-lookup"><span data-stu-id="cea12-145">The version of the partition key definition</span></span>

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

### <span data-ttu-id="cea12-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cea12-146">-ResourceGroupName</span></span>
<span data-ttu-id="cea12-147">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cea12-147">Name of resource group.</span></span>

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

### <span data-ttu-id="cea12-148">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="cea12-148">-Throughput</span></span>
<span data-ttu-id="cea12-149">Az SQL-tároló (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="cea12-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="cea12-150">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="cea12-150">Default value is 400.</span></span>

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

### <span data-ttu-id="cea12-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="cea12-151">-TtlInSeconds</span></span>
<span data-ttu-id="cea12-152">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="cea12-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="cea12-153">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="cea12-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="cea12-154">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="cea12-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="cea12-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="cea12-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="cea12-156">UniqueKeyPolicy object of type Microsoft.Azure.Commands.CossDB.PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="cea12-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="cea12-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea12-157">-WhatIf</span></span>
<span data-ttu-id="cea12-158">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cea12-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea12-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cea12-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea12-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea12-160">CommonParameters</span></span>
<span data-ttu-id="cea12-161">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cea12-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea12-162">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cea12-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea12-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cea12-163">INPUTS</span></span>

### <span data-ttu-id="cea12-164">Microsoft.Azure.Commands.EzresDB.Models.PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="cea12-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="cea12-165">Microsoft.Azure.Commands.CossDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="cea12-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="cea12-166">Microsoft.Azure.Commands.EzresDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="cea12-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="cea12-167">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="cea12-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="cea12-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cea12-168">OUTPUTS</span></span>

### <span data-ttu-id="cea12-169">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="cea12-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="cea12-170">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="cea12-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="cea12-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cea12-171">NOTES</span></span>

## <span data-ttu-id="cea12-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cea12-172">RELATED LINKS</span></span>
