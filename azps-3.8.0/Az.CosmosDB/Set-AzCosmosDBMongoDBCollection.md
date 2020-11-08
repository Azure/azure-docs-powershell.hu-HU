---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 33aa465024591436d80b34b765c90badfb0f1662
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014437"
---
# <span data-ttu-id="b0ca1-101">Set-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="b0ca1-101">Set-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="b0ca1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="b0ca1-103">A CosmosDB MongoDB gyűjteményét állítja be.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-103">Sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="b0ca1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0ca1-104">SYNTAX</span></span>

### <span data-ttu-id="b0ca1-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0ca1-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-Throughput <Int32>] [-Shard <String>] [-Index <PSMongoIndex[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0ca1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0ca1-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBCollection -Name <String> [-Throughput <Int32>] [-Shard <String>]
 [-Index <PSMongoIndex[]>] -InputObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0ca1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0ca1-107">DESCRIPTION</span></span>
<span data-ttu-id="b0ca1-108">A **set-AzCosmosDBMongoDBCollection** parancsmag a CosmosDB MongoDB gyűjteményét állítja be.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-108">The **Set-AzCosmosDBMongoDBCollection** cmdlet sets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="b0ca1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b0ca1-109">EXAMPLES</span></span>

### <span data-ttu-id="b0ca1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b0ca1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="b0ca1-111">Az erőforrás-objektum MongoIndexes-, _rid-, _ts-, _etag-tulajdonságokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="b0ca1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0ca1-112">PARAMETERS</span></span>

### <span data-ttu-id="b0ca1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b0ca1-113">-AccountName</span></span>
<span data-ttu-id="b0ca1-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b0ca1-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b0ca1-115">-Confirm</span></span>
<span data-ttu-id="b0ca1-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0ca1-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0ca1-117">-DatabaseName</span></span>
<span data-ttu-id="b0ca1-118">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-118">Database name.</span></span>

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

### <span data-ttu-id="b0ca1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0ca1-119">-DefaultProfile</span></span>
<span data-ttu-id="b0ca1-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0ca1-121">– Index</span><span class="sxs-lookup"><span data-stu-id="b0ca1-121">-Index</span></span>
<span data-ttu-id="b0ca1-122">PSMongoIndex-objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="b0ca1-122">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="b0ca1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0ca1-123">-InputObject</span></span>
<span data-ttu-id="b0ca1-124">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="b0ca1-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b0ca1-125">-Name</span></span>
<span data-ttu-id="b0ca1-126">Gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="b0ca1-126">Collection name.</span></span>

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

### <span data-ttu-id="b0ca1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0ca1-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0ca1-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-128">Name of resource group.</span></span>

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

### <span data-ttu-id="b0ca1-129">-Szilánk</span><span class="sxs-lookup"><span data-stu-id="b0ca1-129">-Shard</span></span>
<span data-ttu-id="b0ca1-130">A szilánkok kulcsának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-130">Sharding key path.</span></span>

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

### <span data-ttu-id="b0ca1-131">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="b0ca1-131">-Throughput</span></span>
<span data-ttu-id="b0ca1-132">Az SQL-tároló (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-132">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="b0ca1-133">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-133">Default value is 400.</span></span>

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

### <span data-ttu-id="b0ca1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0ca1-134">-WhatIf</span></span>
<span data-ttu-id="b0ca1-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0ca1-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0ca1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0ca1-137">CommonParameters</span></span>
<span data-ttu-id="b0ca1-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0ca1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0ca1-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b0ca1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0ca1-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0ca1-140">INPUTS</span></span>

### <span data-ttu-id="b0ca1-141">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b0ca1-141">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="b0ca1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0ca1-142">OUTPUTS</span></span>

### <span data-ttu-id="b0ca1-143">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="b0ca1-143">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="b0ca1-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0ca1-144">NOTES</span></span>

## <span data-ttu-id="b0ca1-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0ca1-145">RELATED LINKS</span></span>
