---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182567"
---
# <span data-ttu-id="5a8ba-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="5a8ba-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="5a8ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a8ba-102">SYNOPSIS</span></span>
<span data-ttu-id="5a8ba-103">Megkapja a CosmosDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="5a8ba-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5a8ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a8ba-104">SYNTAX</span></span>

### <span data-ttu-id="5a8ba-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a8ba-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="5a8ba-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a8ba-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a8ba-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a8ba-107">DESCRIPTION</span></span>
<span data-ttu-id="5a8ba-108">A **Get-AzCosmosDBMongoDBCollection** parancsmag megkapja a CosmosDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="5a8ba-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5a8ba-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5a8ba-109">EXAMPLES</span></span>

### <span data-ttu-id="5a8ba-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5a8ba-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="5a8ba-111">Az erőforrás-objektum MongoIndexes-, _rid-, _ts-, _etag-tulajdonságokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="5a8ba-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="5a8ba-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="5a8ba-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="5a8ba-113">Ez a példa a lekérdezett gyűjtemény ShardKey kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5a8ba-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="5a8ba-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a8ba-114">PARAMETERS</span></span>

### <span data-ttu-id="5a8ba-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5a8ba-115">-AccountName</span></span>
<span data-ttu-id="5a8ba-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="5a8ba-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5a8ba-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5a8ba-117">-DatabaseName</span></span>
<span data-ttu-id="5a8ba-118">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="5a8ba-118">Database name.</span></span>

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

### <span data-ttu-id="5a8ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a8ba-119">-DefaultProfile</span></span>
<span data-ttu-id="5a8ba-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a8ba-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a8ba-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5a8ba-121">-Name</span></span>
<span data-ttu-id="5a8ba-122">Gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="5a8ba-122">Collection name.</span></span>

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

### <span data-ttu-id="5a8ba-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5a8ba-123">-ParentObject</span></span>
<span data-ttu-id="5a8ba-124">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="5a8ba-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="5a8ba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a8ba-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a8ba-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5a8ba-126">Name of resource group.</span></span>

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

### <span data-ttu-id="5a8ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a8ba-127">CommonParameters</span></span>
<span data-ttu-id="5a8ba-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a8ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a8ba-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5a8ba-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a8ba-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a8ba-130">INPUTS</span></span>

### <span data-ttu-id="5a8ba-131">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5a8ba-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="5a8ba-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a8ba-132">OUTPUTS</span></span>

### <span data-ttu-id="5a8ba-133">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="5a8ba-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="5a8ba-134">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5a8ba-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5a8ba-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a8ba-135">NOTES</span></span>

## <span data-ttu-id="5a8ba-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a8ba-136">RELATED LINKS</span></span>
