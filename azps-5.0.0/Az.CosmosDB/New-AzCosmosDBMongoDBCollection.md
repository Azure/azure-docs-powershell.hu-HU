---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299291"
---
# <span data-ttu-id="75752-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="75752-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="75752-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75752-102">SYNOPSIS</span></span>
<span data-ttu-id="75752-103">Új CosmosDB-MongoDB gyűjtemény létrehozása.</span><span class="sxs-lookup"><span data-stu-id="75752-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="75752-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75752-104">SYNTAX</span></span>

### <span data-ttu-id="75752-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75752-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75752-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75752-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75752-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="75752-107">DESCRIPTION</span></span>
<span data-ttu-id="75752-108">Új CosmosDB-MongoDB gyűjtemény létrehozása.</span><span class="sxs-lookup"><span data-stu-id="75752-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="75752-109">Példák</span><span class="sxs-lookup"><span data-stu-id="75752-109">EXAMPLES</span></span>

### <span data-ttu-id="75752-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="75752-110">Example 1</span></span>
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

## <span data-ttu-id="75752-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75752-111">PARAMETERS</span></span>

### <span data-ttu-id="75752-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75752-112">-AccountName</span></span>
<span data-ttu-id="75752-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="75752-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="75752-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="75752-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="75752-115">Az analitikai tárterület ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="75752-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="75752-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="75752-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="75752-117">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="75752-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="75752-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="75752-118">-Confirm</span></span>
<span data-ttu-id="75752-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="75752-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75752-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75752-120">-DatabaseName</span></span>
<span data-ttu-id="75752-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="75752-121">Database name.</span></span>

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

### <span data-ttu-id="75752-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75752-122">-DefaultProfile</span></span>
<span data-ttu-id="75752-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75752-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75752-124">– Index</span><span class="sxs-lookup"><span data-stu-id="75752-124">-Index</span></span>
<span data-ttu-id="75752-125">PSMongoIndex-objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="75752-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="75752-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75752-126">-Name</span></span>
<span data-ttu-id="75752-127">Gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="75752-127">Collection name.</span></span>

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

### <span data-ttu-id="75752-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="75752-128">-ParentObject</span></span>
<span data-ttu-id="75752-129">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="75752-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="75752-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75752-130">-ResourceGroupName</span></span>
<span data-ttu-id="75752-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="75752-131">Name of resource group.</span></span>

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

### <span data-ttu-id="75752-132">-Szilánk</span><span class="sxs-lookup"><span data-stu-id="75752-132">-Shard</span></span>
<span data-ttu-id="75752-133">A szilánkok kulcsának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="75752-133">Sharding key path.</span></span>

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

### <span data-ttu-id="75752-134">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="75752-134">-Throughput</span></span>
<span data-ttu-id="75752-135">Az SQL-tároló (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="75752-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="75752-136">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="75752-136">Default value is 400.</span></span>

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

### <span data-ttu-id="75752-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75752-137">-WhatIf</span></span>
<span data-ttu-id="75752-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="75752-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75752-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75752-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75752-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75752-140">CommonParameters</span></span>
<span data-ttu-id="75752-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75752-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75752-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="75752-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75752-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75752-143">INPUTS</span></span>

### <span data-ttu-id="75752-144">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="75752-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="75752-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75752-145">OUTPUTS</span></span>

### <span data-ttu-id="75752-146">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="75752-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="75752-147">Microsoft. Azure. Command. CosmosDB. kivétellel. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="75752-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="75752-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75752-148">NOTES</span></span>

## <span data-ttu-id="75752-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75752-149">RELATED LINKS</span></span>
