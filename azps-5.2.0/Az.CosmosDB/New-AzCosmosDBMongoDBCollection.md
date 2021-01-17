---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346289"
---
# <span data-ttu-id="a5f2a-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="a5f2a-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="a5f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f2a-103">Létrehoz egy új MellőDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="a5f2a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5f2a-104">SYNTAX</span></span>

### <span data-ttu-id="a5f2a-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5f2a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5f2a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5f2a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5f2a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5f2a-107">DESCRIPTION</span></span>
<span data-ttu-id="a5f2a-108">Létrehoz egy új MellőDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="a5f2a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5f2a-109">EXAMPLES</span></span>

### <span data-ttu-id="a5f2a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a5f2a-110">Example 1</span></span>
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

## <span data-ttu-id="a5f2a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5f2a-111">PARAMETERS</span></span>

### <span data-ttu-id="a5f2a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5f2a-112">-AccountName</span></span>
<span data-ttu-id="a5f2a-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a5f2a-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="a5f2a-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="a5f2a-115">TTL analitikus tároláshoz.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="a5f2a-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="a5f2a-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="a5f2a-117">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="a5f2a-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5f2a-118">-Confirm</span></span>
<span data-ttu-id="a5f2a-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5f2a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a5f2a-120">-DatabaseName</span></span>
<span data-ttu-id="a5f2a-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-121">Database name.</span></span>

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

### <span data-ttu-id="a5f2a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f2a-122">-DefaultProfile</span></span>
<span data-ttu-id="a5f2a-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5f2a-124">-Index</span><span class="sxs-lookup"><span data-stu-id="a5f2a-124">-Index</span></span>
<span data-ttu-id="a5f2a-125">PSMongoIndex-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="a5f2a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a5f2a-126">-Name</span></span>
<span data-ttu-id="a5f2a-127">Gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-127">Collection name.</span></span>

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

### <span data-ttu-id="a5f2a-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a5f2a-128">-ParentObject</span></span>
<span data-ttu-id="a5f2a-129">Mongo Adatbázis objektum.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="a5f2a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5f2a-130">-ResourceGroupName</span></span>
<span data-ttu-id="a5f2a-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-131">Name of resource group.</span></span>

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

### <span data-ttu-id="a5f2a-132">-Shard</span><span class="sxs-lookup"><span data-stu-id="a5f2a-132">-Shard</span></span>
<span data-ttu-id="a5f2a-133">Sharding key path.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-133">Sharding key path.</span></span>

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

### <span data-ttu-id="a5f2a-134">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="a5f2a-134">-Throughput</span></span>
<span data-ttu-id="a5f2a-135">Az SQL-tároló (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="a5f2a-136">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-136">Default value is 400.</span></span>

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

### <span data-ttu-id="a5f2a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5f2a-137">-WhatIf</span></span>
<span data-ttu-id="a5f2a-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5f2a-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5f2a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f2a-140">CommonParameters</span></span>
<span data-ttu-id="a5f2a-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5f2a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f2a-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5f2a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f2a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5f2a-143">INPUTS</span></span>

### <span data-ttu-id="a5f2a-144">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="a5f2a-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="a5f2a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5f2a-145">OUTPUTS</span></span>

### <span data-ttu-id="a5f2a-146">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="a5f2a-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="a5f2a-147">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="a5f2a-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="a5f2a-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5f2a-148">NOTES</span></span>

## <span data-ttu-id="a5f2a-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5f2a-149">RELATED LINKS</span></span>
