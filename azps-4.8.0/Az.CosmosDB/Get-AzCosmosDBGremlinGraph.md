---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184205"
---
# <span data-ttu-id="39062-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="39062-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="39062-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39062-102">SYNOPSIS</span></span>
<span data-ttu-id="39062-103">Megkapja a CosmosDB Gremlin gráfot.</span><span class="sxs-lookup"><span data-stu-id="39062-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="39062-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39062-104">SYNTAX</span></span>

### <span data-ttu-id="39062-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39062-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="39062-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39062-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39062-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="39062-107">DESCRIPTION</span></span>
<span data-ttu-id="39062-108">A **Get-AzCosmosDBGremlinGraph** parancsmag a CosmosDB Gremlin diagram tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="39062-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="39062-109">Példák</span><span class="sxs-lookup"><span data-stu-id="39062-109">EXAMPLES</span></span>

### <span data-ttu-id="39062-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="39062-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="39062-111">Az erőforrás-objektum IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etagt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="39062-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="39062-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39062-112">PARAMETERS</span></span>

### <span data-ttu-id="39062-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="39062-113">-AccountName</span></span>
<span data-ttu-id="39062-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="39062-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="39062-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="39062-115">-DatabaseName</span></span>
<span data-ttu-id="39062-116">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="39062-116">Database name.</span></span>

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

### <span data-ttu-id="39062-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39062-117">-DefaultProfile</span></span>
<span data-ttu-id="39062-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39062-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39062-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39062-119">-Name</span></span>
<span data-ttu-id="39062-120">Gremlin-diagram neve.</span><span class="sxs-lookup"><span data-stu-id="39062-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="39062-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="39062-121">-ParentObject</span></span>
<span data-ttu-id="39062-122">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="39062-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="39062-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39062-123">-ResourceGroupName</span></span>
<span data-ttu-id="39062-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="39062-124">Name of resource group.</span></span>

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

### <span data-ttu-id="39062-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39062-125">CommonParameters</span></span>
<span data-ttu-id="39062-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39062-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39062-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="39062-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39062-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39062-128">INPUTS</span></span>

### <span data-ttu-id="39062-129">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="39062-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="39062-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39062-130">OUTPUTS</span></span>

### <span data-ttu-id="39062-131">Microsoft. Azure. Command. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="39062-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="39062-132">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="39062-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="39062-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39062-133">NOTES</span></span>

## <span data-ttu-id="39062-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39062-134">RELATED LINKS</span></span>
