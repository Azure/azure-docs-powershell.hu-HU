---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: bb73bd88abf677f9855d934a995f3f9107e44b4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931978"
---
# <span data-ttu-id="41dbc-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="41dbc-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="41dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="41dbc-103">Beveszi a 2016-os MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="41dbc-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="41dbc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="41dbc-104">SYNTAX</span></span>

### <span data-ttu-id="41dbc-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41dbc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="41dbc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41dbc-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41dbc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="41dbc-107">DESCRIPTION</span></span>
<span data-ttu-id="41dbc-108">A **Get-AzCosmosDBMongoDBCollection** parancsmag megkapja aCsoportosDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="41dbc-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="41dbc-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="41dbc-109">EXAMPLES</span></span>

### <span data-ttu-id="41dbc-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="41dbc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="41dbc-111">Az erőforrásobjektum MongoIndexes, _rid, _ts, _etag tulajdonságokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="41dbc-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="41dbc-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="41dbc-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="41dbc-113">Ez a példa beolvassa a lekért gyűjtemény ShardKey kulcsát</span><span class="sxs-lookup"><span data-stu-id="41dbc-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="41dbc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41dbc-114">PARAMETERS</span></span>

### <span data-ttu-id="41dbc-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="41dbc-115">-AccountName</span></span>
<span data-ttu-id="41dbc-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="41dbc-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="41dbc-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="41dbc-117">-DatabaseName</span></span>
<span data-ttu-id="41dbc-118">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="41dbc-118">Database name.</span></span>

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

### <span data-ttu-id="41dbc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41dbc-119">-DefaultProfile</span></span>
<span data-ttu-id="41dbc-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41dbc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41dbc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="41dbc-121">-Name</span></span>
<span data-ttu-id="41dbc-122">Gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="41dbc-122">Collection name.</span></span>

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

### <span data-ttu-id="41dbc-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="41dbc-123">-ParentObject</span></span>
<span data-ttu-id="41dbc-124">Mongo Adatbázis objektum.</span><span class="sxs-lookup"><span data-stu-id="41dbc-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="41dbc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41dbc-125">-ResourceGroupName</span></span>
<span data-ttu-id="41dbc-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="41dbc-126">Name of resource group.</span></span>

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

### <span data-ttu-id="41dbc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41dbc-127">CommonParameters</span></span>
<span data-ttu-id="41dbc-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41dbc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41dbc-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41dbc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41dbc-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41dbc-130">INPUTS</span></span>

### <span data-ttu-id="41dbc-131">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="41dbc-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="41dbc-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41dbc-132">OUTPUTS</span></span>

### <span data-ttu-id="41dbc-133">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="41dbc-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="41dbc-134">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="41dbc-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="41dbc-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="41dbc-135">NOTES</span></span>

## <span data-ttu-id="41dbc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41dbc-136">RELATED LINKS</span></span>
