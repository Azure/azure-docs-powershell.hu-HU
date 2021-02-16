---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166258"
---
# <span data-ttu-id="cb342-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="cb342-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="cb342-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb342-102">SYNOPSIS</span></span>
<span data-ttu-id="cb342-103">Beveszi a 2010-es 2016-os Gremlin Graph-bemutatót.</span><span class="sxs-lookup"><span data-stu-id="cb342-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="cb342-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb342-104">SYNTAX</span></span>

### <span data-ttu-id="cb342-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb342-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="cb342-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb342-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb342-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb342-107">DESCRIPTION</span></span>
<span data-ttu-id="cb342-108">A **Get-AzCosmosDBGremlinGraph** parancsmag megkapja a MintakDB Gremlin Graph-tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="cb342-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="cb342-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb342-109">EXAMPLES</span></span>

### <span data-ttu-id="cb342-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="cb342-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="cb342-111">Az Erőforrásobjektum az IndexingPolicy, a PartitionKey, a DefaultTtl, a UniqueKeyPolicy, a ConflictResolutionPolicy, _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="cb342-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="cb342-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb342-112">PARAMETERS</span></span>

### <span data-ttu-id="cb342-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cb342-113">-AccountName</span></span>
<span data-ttu-id="cb342-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="cb342-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cb342-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb342-115">-DatabaseName</span></span>
<span data-ttu-id="cb342-116">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="cb342-116">Database name.</span></span>

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

### <span data-ttu-id="cb342-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb342-117">-DefaultProfile</span></span>
<span data-ttu-id="cb342-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb342-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb342-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cb342-119">-Name</span></span>
<span data-ttu-id="cb342-120">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="cb342-120">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="cb342-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cb342-121">-ParentObject</span></span>
<span data-ttu-id="cb342-122">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="cb342-122">Gremlin Database object.</span></span>

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

### <span data-ttu-id="cb342-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb342-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb342-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cb342-124">Name of resource group.</span></span>

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

### <span data-ttu-id="cb342-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb342-125">CommonParameters</span></span>
<span data-ttu-id="cb342-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb342-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb342-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb342-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb342-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb342-128">INPUTS</span></span>

### <span data-ttu-id="cb342-129">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="cb342-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="cb342-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb342-130">OUTPUTS</span></span>

### <span data-ttu-id="cb342-131">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="cb342-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="cb342-132">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="cb342-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="cb342-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb342-133">NOTES</span></span>

## <span data-ttu-id="cb342-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb342-134">RELATED LINKS</span></span>
