---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 4818f0bb179274181c998c4ad07ca013ade0a2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934426"
---
# <span data-ttu-id="9b382-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="9b382-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="9b382-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b382-102">SYNOPSIS</span></span>
<span data-ttu-id="9b382-103">Beveszi a 2010-es 2016-os Gremlin Graph-bemutatót.</span><span class="sxs-lookup"><span data-stu-id="9b382-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="9b382-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9b382-104">SYNTAX</span></span>

### <span data-ttu-id="9b382-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b382-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="9b382-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b382-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b382-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9b382-107">DESCRIPTION</span></span>
<span data-ttu-id="9b382-108">A **Get-AzCosmosDBGremlinGraph** parancsmag megkapja a MintakDB Gremlin Graph-tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="9b382-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="9b382-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9b382-109">EXAMPLES</span></span>

### <span data-ttu-id="9b382-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="9b382-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="9b382-111">Az Erőforrásobjektum az IndexingPolicy, a PartitionKey, a DefaultTtl, a UniqueKeyPolicy, a ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="9b382-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="9b382-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b382-112">PARAMETERS</span></span>

### <span data-ttu-id="9b382-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9b382-113">-AccountName</span></span>
<span data-ttu-id="9b382-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="9b382-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9b382-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9b382-115">-DatabaseName</span></span>
<span data-ttu-id="9b382-116">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9b382-116">Database name.</span></span>

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

### <span data-ttu-id="9b382-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b382-117">-DefaultProfile</span></span>
<span data-ttu-id="9b382-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b382-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b382-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9b382-119">-Name</span></span>
<span data-ttu-id="9b382-120">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="9b382-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="9b382-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9b382-121">-ParentObject</span></span>
<span data-ttu-id="9b382-122">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="9b382-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="9b382-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b382-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b382-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9b382-124">Name of resource group.</span></span>

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

### <span data-ttu-id="9b382-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b382-125">CommonParameters</span></span>
<span data-ttu-id="9b382-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b382-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b382-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b382-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b382-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b382-128">INPUTS</span></span>

### <span data-ttu-id="9b382-129">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9b382-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="9b382-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b382-130">OUTPUTS</span></span>

### <span data-ttu-id="9b382-131">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="9b382-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="9b382-132">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9b382-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9b382-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9b382-133">NOTES</span></span>

## <span data-ttu-id="9b382-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b382-134">RELATED LINKS</span></span>
