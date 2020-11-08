---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 623ed0391ba36722cce26a42f1dd3d820cbd49f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014120"
---
# <span data-ttu-id="7a813-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="7a813-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="7a813-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a813-102">SYNOPSIS</span></span>
<span data-ttu-id="7a813-103">Megkapja a CosmosDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="7a813-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="7a813-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a813-104">SYNTAX</span></span>

### <span data-ttu-id="7a813-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7a813-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="7a813-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a813-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a813-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a813-107">DESCRIPTION</span></span>
<span data-ttu-id="7a813-108">A **Get-AzCosmosDBMongoDBCollection** parancsmag megkapja a CosmosDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="7a813-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="7a813-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7a813-109">EXAMPLES</span></span>

### <span data-ttu-id="7a813-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7a813-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName}  -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="7a813-111">Az erőforrás-objektum MongoIndexes-, _rid-, _ts-, _etag-tulajdonságokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="7a813-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="7a813-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a813-112">PARAMETERS</span></span>

### <span data-ttu-id="7a813-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7a813-113">-AccountName</span></span>
<span data-ttu-id="7a813-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="7a813-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7a813-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a813-115">-DatabaseName</span></span>
<span data-ttu-id="7a813-116">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7a813-116">Database name.</span></span>

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

### <span data-ttu-id="7a813-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a813-117">-DefaultProfile</span></span>
<span data-ttu-id="7a813-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a813-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a813-119">– Részletes</span><span class="sxs-lookup"><span data-stu-id="7a813-119">-Detailed</span></span>
<span data-ttu-id="7a813-120">Ha meg van határozva, akkor a parancsmag a megfelelő átviteli értékkel rendelkező gyűjteményt adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7a813-120">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a813-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a813-121">-InputObject</span></span>
<span data-ttu-id="7a813-122">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="7a813-122">Mongo Database object.</span></span>

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

### <span data-ttu-id="7a813-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a813-123">-Name</span></span>
<span data-ttu-id="7a813-124">Gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="7a813-124">Collection name.</span></span>

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

### <span data-ttu-id="7a813-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a813-125">-ResourceGroupName</span></span>
<span data-ttu-id="7a813-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a813-126">Name of resource group.</span></span>

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

### <span data-ttu-id="7a813-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a813-127">CommonParameters</span></span>
<span data-ttu-id="7a813-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a813-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a813-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7a813-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a813-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a813-130">INPUTS</span></span>

### <span data-ttu-id="7a813-131">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7a813-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="7a813-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a813-132">OUTPUTS</span></span>

### <span data-ttu-id="7a813-133">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="7a813-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="7a813-134">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7a813-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7a813-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a813-135">NOTES</span></span>

## <span data-ttu-id="7a813-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a813-136">RELATED LINKS</span></span>
