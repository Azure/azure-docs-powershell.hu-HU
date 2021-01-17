---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: b69640eb2af37ce0ef48ca3841c3cadcc0c3a57b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329373"
---
# <span data-ttu-id="01247-101">Update-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="01247-101">Update-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="01247-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01247-102">SYNOPSIS</span></span>
<span data-ttu-id="01247-103">Frissíti aTervsDB Gremlin Graphot.</span><span class="sxs-lookup"><span data-stu-id="01247-103">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="01247-104">Ügyféloldali javítást hajt végre a meglévő Grafikon olvasása segítségével.</span><span class="sxs-lookup"><span data-stu-id="01247-104">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="01247-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01247-105">SYNTAX</span></span>

### <span data-ttu-id="01247-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01247-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01247-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01247-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01247-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01247-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraph [-Name <String>] [-IndexingPolicy <PSIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] [-PartitionKeyKind <String>] [-PartitionKeyPath <String[]>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-UniqueKeyPolicy <PSUniqueKeyPolicy>] [-ConflictResolutionPolicyMode <String>]
 [-ConflictResolutionPolicyPath <String>] [-ConflictResolutionPolicyProcedure <String>]
 [-ConflictResolutionPolicy <PSConflictResolutionPolicy>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01247-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01247-109">DESCRIPTION</span></span>
<span data-ttu-id="01247-110">Frissíti aTervsDB Gremlin Graphot.</span><span class="sxs-lookup"><span data-stu-id="01247-110">Updates the CosmosDB Gremlin Graph.</span></span> <span data-ttu-id="01247-111">Ügyféloldali javítást hajt végre a meglévő Grafikon olvasása segítségével.</span><span class="sxs-lookup"><span data-stu-id="01247-111">Performs a client side patch operation by reading the existing Graph.</span></span>

## <span data-ttu-id="01247-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01247-112">EXAMPLES</span></span>

### <span data-ttu-id="01247-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="01247-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraph -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -Throughput updatedThroughputValue

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName/graphs/myGraphName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

## <span data-ttu-id="01247-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01247-114">PARAMETERS</span></span>

### <span data-ttu-id="01247-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01247-115">-AccountName</span></span>
<span data-ttu-id="01247-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="01247-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="01247-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="01247-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="01247-118">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="01247-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="01247-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01247-119">-Confirm</span></span>
<span data-ttu-id="01247-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="01247-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01247-121">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="01247-121">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="01247-122">ConflictResolutionPolicy object of type PSConflictResolutionPolicy, ha ezt a tároló ConflictResolutionPolicy-ként van beállítva.</span><span class="sxs-lookup"><span data-stu-id="01247-122">ConflictResolutionPolicy Object of type PSConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

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

### <span data-ttu-id="01247-123">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="01247-123">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="01247-124">A következő értékek is létrehozhatók: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="01247-124">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="01247-125">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="01247-125">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="01247-126">Meg kell adni, ha a típus LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="01247-126">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="01247-127">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="01247-127">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="01247-128">Egyéni típushoz meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="01247-128">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="01247-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="01247-129">-DatabaseName</span></span>
<span data-ttu-id="01247-130">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="01247-130">Database name.</span></span>

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

### <span data-ttu-id="01247-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01247-131">-DefaultProfile</span></span>
<span data-ttu-id="01247-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01247-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01247-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="01247-133">-IndexingPolicy</span></span>
<span data-ttu-id="01247-134">A Microsoft.Azure.Commands.Fogarasdb.PSIndexingPolicy típusú indexelési házirendobjektum.</span><span class="sxs-lookup"><span data-stu-id="01247-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSIndexingPolicy.</span></span>

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

### <span data-ttu-id="01247-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01247-135">-InputObject</span></span>
<span data-ttu-id="01247-136">Gremlin Graph-objektum.</span><span class="sxs-lookup"><span data-stu-id="01247-136">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="01247-137">-Name</span><span class="sxs-lookup"><span data-stu-id="01247-137">-Name</span></span>
<span data-ttu-id="01247-138">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="01247-138">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="01247-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="01247-139">-ParentObject</span></span>
<span data-ttu-id="01247-140">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="01247-140">Gremlin Database object.</span></span>

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

### <span data-ttu-id="01247-141">-PartitionKeyKind</span><span class="sxs-lookup"><span data-stu-id="01247-141">-PartitionKeyKind</span></span>
<span data-ttu-id="01247-142">A partíciókhoz használt algoritmus fajtája.</span><span class="sxs-lookup"><span data-stu-id="01247-142">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="01247-143">Lehetséges értékek: "Kivonat", "Tartomány"</span><span class="sxs-lookup"><span data-stu-id="01247-143">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="01247-144">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="01247-144">-PartitionKeyPath</span></span>
<span data-ttu-id="01247-145">Partition key Path, pl.: '/address/zipcode'.</span><span class="sxs-lookup"><span data-stu-id="01247-145">Partition Key Path, e.g., '/address/zipcode'.</span></span>

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

### <span data-ttu-id="01247-146">-PartitionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="01247-146">-PartitionKeyVersion</span></span>
<span data-ttu-id="01247-147">A partíciók kulcsdefiníciójának verziója</span><span class="sxs-lookup"><span data-stu-id="01247-147">The version of the partition key definition</span></span>

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

### <span data-ttu-id="01247-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01247-148">-ResourceGroupName</span></span>
<span data-ttu-id="01247-149">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="01247-149">Name of resource group.</span></span>

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

### <span data-ttu-id="01247-150">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="01247-150">-Throughput</span></span>
<span data-ttu-id="01247-151">A Gremlin Graph (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="01247-151">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="01247-152">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="01247-152">Default value is 400.</span></span>

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

### <span data-ttu-id="01247-153">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="01247-153">-TtlInSeconds</span></span>
<span data-ttu-id="01247-154">Default Ttl in seconds. (Alapértelmezett ttl másodpercben).</span><span class="sxs-lookup"><span data-stu-id="01247-154">Default Ttl in seconds.</span></span>
<span data-ttu-id="01247-155">Ha az érték hiányzik vagy - 1 értékre van állítva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="01247-155">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="01247-156">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítás után n másodperccel lejárnak.</span><span class="sxs-lookup"><span data-stu-id="01247-156">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="01247-157">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="01247-157">-UniqueKeyPolicy</span></span>
<span data-ttu-id="01247-158">A Microsoft.Azure.Commands.FogasDB.PSUniqueKeyPolicy típusú UniqueKeyPolicy objektum.</span><span class="sxs-lookup"><span data-stu-id="01247-158">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSUniqueKeyPolicy.</span></span>

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

### <span data-ttu-id="01247-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01247-159">-WhatIf</span></span>
<span data-ttu-id="01247-160">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="01247-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01247-161">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01247-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01247-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01247-162">CommonParameters</span></span>
<span data-ttu-id="01247-163">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01247-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01247-164">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01247-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01247-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01247-165">INPUTS</span></span>

### <span data-ttu-id="01247-166">Microsoft.Azure.Commands.CossDB.Models.PSIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="01247-166">Microsoft.Azure.Commands.CosmosDB.Models.PSIndexingPolicy</span></span>

### <span data-ttu-id="01247-167">Microsoft.Azure.Commands.EzresDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="01247-167">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

### <span data-ttu-id="01247-168">Microsoft.Azure.Commands.EzresDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="01247-168">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

### <span data-ttu-id="01247-169">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="01247-169">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="01247-170">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="01247-170">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="01247-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01247-171">OUTPUTS</span></span>

### <span data-ttu-id="01247-172">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="01247-172">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="01247-173">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="01247-173">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="01247-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01247-174">NOTES</span></span>

## <span data-ttu-id="01247-175">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01247-175">RELATED LINKS</span></span>
