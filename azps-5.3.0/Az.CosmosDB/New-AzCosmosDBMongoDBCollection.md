---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480568"
---
# <span data-ttu-id="5e584-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="5e584-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="5e584-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e584-102">SYNOPSIS</span></span>
<span data-ttu-id="5e584-103">Létrehoz egy új MellőDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="5e584-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5e584-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e584-104">SYNTAX</span></span>

### <span data-ttu-id="5e584-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e584-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e584-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e584-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e584-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e584-107">DESCRIPTION</span></span>
<span data-ttu-id="5e584-108">Létrehoz egy új MellőDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="5e584-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5e584-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e584-109">EXAMPLES</span></span>

### <span data-ttu-id="5e584-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="5e584-110">Example 1</span></span>
```powershell
PS C:\> 
        $ttlInSeconds = 604800
        $index1 = New-AzCosmosDBMongoDBIndex -Key @("partitionkey1", "partitionkey2") -Unique 1
>>      $index2 = New-AzCosmosDBMongoDBIndex -Key @("_ts") -TtlInSeconds $ttlInSeconds

New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2 -Shard myShardKey

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="5e584-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e584-111">PARAMETERS</span></span>

### <span data-ttu-id="5e584-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5e584-112">-AccountName</span></span>
<span data-ttu-id="5e584-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="5e584-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5e584-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="5e584-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="5e584-115">TTL analitikus tároláshoz.</span><span class="sxs-lookup"><span data-stu-id="5e584-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="5e584-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="5e584-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="5e584-117">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="5e584-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="5e584-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e584-118">-Confirm</span></span>
<span data-ttu-id="5e584-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5e584-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e584-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e584-120">-DatabaseName</span></span>
<span data-ttu-id="5e584-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="5e584-121">Database name.</span></span>

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

### <span data-ttu-id="5e584-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e584-122">-DefaultProfile</span></span>
<span data-ttu-id="5e584-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e584-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e584-124">-Index</span><span class="sxs-lookup"><span data-stu-id="5e584-124">-Index</span></span>
<span data-ttu-id="5e584-125">PSMongoIndex-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="5e584-125">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e584-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5e584-126">-Name</span></span>
<span data-ttu-id="5e584-127">Gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="5e584-127">Collection name.</span></span>

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

### <span data-ttu-id="5e584-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5e584-128">-ParentObject</span></span>
<span data-ttu-id="5e584-129">Mongo Adatbázis objektum.</span><span class="sxs-lookup"><span data-stu-id="5e584-129">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e584-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e584-130">-ResourceGroupName</span></span>
<span data-ttu-id="5e584-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5e584-131">Name of resource group.</span></span>

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

### <span data-ttu-id="5e584-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="5e584-132">-Shard</span></span>
<span data-ttu-id="5e584-133">Sharding key path.</span><span class="sxs-lookup"><span data-stu-id="5e584-133">Sharding key path.</span></span>

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

### <span data-ttu-id="5e584-134">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="5e584-134">-Throughput</span></span>
<span data-ttu-id="5e584-135">Az SQL-tároló (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="5e584-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="5e584-136">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="5e584-136">Default value is 400.</span></span>

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

### <span data-ttu-id="5e584-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e584-137">-WhatIf</span></span>
<span data-ttu-id="5e584-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5e584-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e584-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e584-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e584-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e584-140">CommonParameters</span></span>
<span data-ttu-id="5e584-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e584-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e584-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e584-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e584-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e584-143">INPUTS</span></span>

### <span data-ttu-id="5e584-144">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5e584-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="5e584-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e584-145">OUTPUTS</span></span>

### <span data-ttu-id="5e584-146">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="5e584-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="5e584-147">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="5e584-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="5e584-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e584-148">NOTES</span></span>

## <span data-ttu-id="5e584-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e584-149">RELATED LINKS</span></span>
