---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 2da3a5729673abde6ad54ea66f1b5fbd9f089db9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014122"
---
# <span data-ttu-id="049d2-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="049d2-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="049d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="049d2-102">SYNOPSIS</span></span>
<span data-ttu-id="049d2-103">Megkapja a CosmosDB Gremlin gráfot.</span><span class="sxs-lookup"><span data-stu-id="049d2-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="049d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="049d2-104">SYNTAX</span></span>

### <span data-ttu-id="049d2-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="049d2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="049d2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="049d2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -InputObject <PSGremlinDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="049d2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="049d2-107">DESCRIPTION</span></span>
<span data-ttu-id="049d2-108">A **Get-AzCosmosDBGremlinGraph** parancsmag a CosmosDB Gremlin diagram tulajdonságait kapja.</span><span class="sxs-lookup"><span data-stu-id="049d2-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="049d2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="049d2-109">EXAMPLES</span></span>

### <span data-ttu-id="049d2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="049d2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="049d2-111">Az erőforrás-objektum IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etagt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="049d2-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="049d2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="049d2-112">PARAMETERS</span></span>

### <span data-ttu-id="049d2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="049d2-113">-AccountName</span></span>
<span data-ttu-id="049d2-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="049d2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="049d2-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="049d2-115">-DatabaseName</span></span>
<span data-ttu-id="049d2-116">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="049d2-116">Database name.</span></span>

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

### <span data-ttu-id="049d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="049d2-117">-DefaultProfile</span></span>
<span data-ttu-id="049d2-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="049d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="049d2-119">– Részletes</span><span class="sxs-lookup"><span data-stu-id="049d2-119">-Detailed</span></span>
<span data-ttu-id="049d2-120">Ha meg van határozva, akkor a parancsmag a megfelelő átviteli értékkel rendelkező Gremlin-diagramot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="049d2-120">If provided then, the cmdlet returns the Gremlin Graph with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="049d2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="049d2-121">-InputObject</span></span>
<span data-ttu-id="049d2-122">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="049d2-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="049d2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="049d2-123">-Name</span></span>
<span data-ttu-id="049d2-124">Gremlin-diagram neve.</span><span class="sxs-lookup"><span data-stu-id="049d2-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="049d2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="049d2-125">-ResourceGroupName</span></span>
<span data-ttu-id="049d2-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="049d2-126">Name of resource group.</span></span>

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

### <span data-ttu-id="049d2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049d2-127">CommonParameters</span></span>
<span data-ttu-id="049d2-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="049d2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049d2-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="049d2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049d2-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="049d2-130">INPUTS</span></span>

### <span data-ttu-id="049d2-131">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="049d2-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="049d2-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="049d2-132">OUTPUTS</span></span>

### <span data-ttu-id="049d2-133">Microsoft. Azure. Command. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="049d2-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="049d2-134">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="049d2-134">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="049d2-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="049d2-135">NOTES</span></span>

## <span data-ttu-id="049d2-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="049d2-136">RELATED LINKS</span></span>
