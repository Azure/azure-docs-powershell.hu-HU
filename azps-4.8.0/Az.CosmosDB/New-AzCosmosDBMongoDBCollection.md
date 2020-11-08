---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 741d63bfe54c03eb101d74519251b67c5e1664b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184629"
---
# <span data-ttu-id="89da6-101">New-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="89da6-101">New-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="89da6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89da6-102">SYNOPSIS</span></span>
<span data-ttu-id="89da6-103">Új CosmosDB-MongoDB gyűjtemény létrehozása.</span><span class="sxs-lookup"><span data-stu-id="89da6-103">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="89da6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89da6-104">SYNTAX</span></span>

### <span data-ttu-id="89da6-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="89da6-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89da6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89da6-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89da6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="89da6-107">DESCRIPTION</span></span>
<span data-ttu-id="89da6-108">Új CosmosDB-MongoDB gyűjtemény létrehozása.</span><span class="sxs-lookup"><span data-stu-id="89da6-108">Creates a new CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="89da6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="89da6-109">EXAMPLES</span></span>

### <span data-ttu-id="89da6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="89da6-110">Example 1</span></span>
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

## <span data-ttu-id="89da6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89da6-111">PARAMETERS</span></span>

### <span data-ttu-id="89da6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="89da6-112">-AccountName</span></span>
<span data-ttu-id="89da6-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="89da6-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="89da6-114">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="89da6-114">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="89da6-115">Az analitikai tárterület ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="89da6-115">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="89da6-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="89da6-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="89da6-117">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="89da6-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="89da6-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89da6-118">-Confirm</span></span>
<span data-ttu-id="89da6-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89da6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89da6-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="89da6-120">-DatabaseName</span></span>
<span data-ttu-id="89da6-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="89da6-121">Database name.</span></span>

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

### <span data-ttu-id="89da6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89da6-122">-DefaultProfile</span></span>
<span data-ttu-id="89da6-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89da6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89da6-124">– Index</span><span class="sxs-lookup"><span data-stu-id="89da6-124">-Index</span></span>
<span data-ttu-id="89da6-125">PSMongoIndex-objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="89da6-125">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="89da6-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="89da6-126">-Name</span></span>
<span data-ttu-id="89da6-127">Gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="89da6-127">Collection name.</span></span>

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

### <span data-ttu-id="89da6-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="89da6-128">-ParentObject</span></span>
<span data-ttu-id="89da6-129">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="89da6-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="89da6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89da6-130">-ResourceGroupName</span></span>
<span data-ttu-id="89da6-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="89da6-131">Name of resource group.</span></span>

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

### <span data-ttu-id="89da6-132">-Szilánk</span><span class="sxs-lookup"><span data-stu-id="89da6-132">-Shard</span></span>
<span data-ttu-id="89da6-133">A szilánkok kulcsának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="89da6-133">Sharding key path.</span></span>

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

### <span data-ttu-id="89da6-134">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="89da6-134">-Throughput</span></span>
<span data-ttu-id="89da6-135">Az SQL-tároló (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="89da6-135">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="89da6-136">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="89da6-136">Default value is 400.</span></span>

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

### <span data-ttu-id="89da6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89da6-137">-WhatIf</span></span>
<span data-ttu-id="89da6-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89da6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89da6-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89da6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89da6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89da6-140">CommonParameters</span></span>
<span data-ttu-id="89da6-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89da6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89da6-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="89da6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89da6-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89da6-143">INPUTS</span></span>

### <span data-ttu-id="89da6-144">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="89da6-144">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="89da6-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89da6-145">OUTPUTS</span></span>

### <span data-ttu-id="89da6-146">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="89da6-146">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="89da6-147">Microsoft. Azure. Command. CosmosDB. kivétellel. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="89da6-147">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="89da6-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89da6-148">NOTES</span></span>

## <span data-ttu-id="89da6-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89da6-149">RELATED LINKS</span></span>
