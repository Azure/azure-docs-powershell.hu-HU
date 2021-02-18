---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 1919b3075b24e96edce93c8d3611f3864d3f9391
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204655"
---
# <span data-ttu-id="5bba2-101">Get-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="5bba2-101">Get-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="5bba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bba2-102">SYNOPSIS</span></span>
<span data-ttu-id="5bba2-103">Beveszi a 2016-os MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="5bba2-103">Gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5bba2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5bba2-104">SYNTAX</span></span>

### <span data-ttu-id="5bba2-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5bba2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollection -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="5bba2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bba2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollection [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bba2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5bba2-107">DESCRIPTION</span></span>
<span data-ttu-id="5bba2-108">A **Get-AzCosmosDBMongoDBCollection** parancsmag megkapja a TamakDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="5bba2-108">The **Get-AzCosmosDBMongoDBCollection** cmdlet gets the CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5bba2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5bba2-109">EXAMPLES</span></span>

### <span data-ttu-id="5bba2-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="5bba2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

<span data-ttu-id="5bba2-111">Az erőforrásobjektum MongoIndexes, _rid, _ts, _etag tulajdonságokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="5bba2-111">Resource Object contains MongoIndexes, _rid, _ts, _etag properties.</span></span>

### <span data-ttu-id="5bba2-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="5bba2-112">Example 2</span></span>
```powershell
PS C:\> (Get-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -Database {dbName} -Name {collectionName}).Resource.ShardKey 

Key           Value
----          ----- 
<ShardKey>    <Value>
```

<span data-ttu-id="5bba2-113">Ez a példa beolvassa a lekért gyűjtemény ShardKey kulcsát.</span><span class="sxs-lookup"><span data-stu-id="5bba2-113">This example gets the ShardKey of the retrieved collection</span></span>

## <span data-ttu-id="5bba2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bba2-114">PARAMETERS</span></span>

### <span data-ttu-id="5bba2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5bba2-115">-AccountName</span></span>
<span data-ttu-id="5bba2-116">A Külön db-adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="5bba2-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5bba2-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5bba2-117">-DatabaseName</span></span>
<span data-ttu-id="5bba2-118">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="5bba2-118">Database name.</span></span>

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

### <span data-ttu-id="5bba2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bba2-119">-DefaultProfile</span></span>
<span data-ttu-id="5bba2-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bba2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bba2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5bba2-121">-Name</span></span>
<span data-ttu-id="5bba2-122">Gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="5bba2-122">Collection name.</span></span>

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

### <span data-ttu-id="5bba2-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5bba2-123">-ParentObject</span></span>
<span data-ttu-id="5bba2-124">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="5bba2-124">Mongo Database object.</span></span>

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

### <span data-ttu-id="5bba2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bba2-125">-ResourceGroupName</span></span>
<span data-ttu-id="5bba2-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5bba2-126">Name of resource group.</span></span>

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

### <span data-ttu-id="5bba2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bba2-127">CommonParameters</span></span>
<span data-ttu-id="5bba2-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bba2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bba2-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bba2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bba2-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bba2-130">INPUTS</span></span>

### <span data-ttu-id="5bba2-131">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5bba2-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="5bba2-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bba2-132">OUTPUTS</span></span>

### <span data-ttu-id="5bba2-133">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="5bba2-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="5bba2-134">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5bba2-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5bba2-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5bba2-135">NOTES</span></span>

## <span data-ttu-id="5bba2-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bba2-136">RELATED LINKS</span></span>
