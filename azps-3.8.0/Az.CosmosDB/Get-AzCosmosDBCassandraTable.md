---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: ca78194e0e47b07d2d0d061829bf4db38d85632a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014127"
---
# <span data-ttu-id="9b1c2-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="9b1c2-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="9b1c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b1c2-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1c2-103">CosmosDB Cassandra-táblázatot kap.</span><span class="sxs-lookup"><span data-stu-id="9b1c2-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="9b1c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b1c2-104">SYNTAX</span></span>

### <span data-ttu-id="9b1c2-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b1c2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b1c2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b1c2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b1c2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b1c2-107">DESCRIPTION</span></span>
<span data-ttu-id="9b1c2-108">A **Get-AzCosmosDBCassandraTable** parancsmag új vagy frissített CosmosDB hoz létre.</span><span class="sxs-lookup"><span data-stu-id="9b1c2-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="9b1c2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9b1c2-109">EXAMPLES</span></span>

### <span data-ttu-id="9b1c2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9b1c2-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="9b1c2-111">{{Get-AzCosmosDBCassandraTable egy meglévő CassandraKeyspace tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9b1c2-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="9b1c2-112">Az erőforrás kibontásával kibonthatja a DefaultTtl, a sémát, a _etagt, a _tst _rid tulajdonságokat.}}</span><span class="sxs-lookup"><span data-stu-id="9b1c2-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="9b1c2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b1c2-113">PARAMETERS</span></span>

### <span data-ttu-id="9b1c2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9b1c2-114">-AccountName</span></span>
<span data-ttu-id="9b1c2-115">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="9b1c2-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9b1c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1c2-116">-DefaultProfile</span></span>
<span data-ttu-id="9b1c2-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b1c2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b1c2-118">– Részletes</span><span class="sxs-lookup"><span data-stu-id="9b1c2-118">-Detailed</span></span>
<span data-ttu-id="9b1c2-119">Ha meg van határozva, akkor a parancsmag a megfelelő átviteli értékkel rendelkező Cassandra (Cassandra) táblázatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9b1c2-119">If provided then, the cmdlet returns the Cassandra Table with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="9b1c2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b1c2-120">-InputObject</span></span>
<span data-ttu-id="9b1c2-121">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="9b1c2-121">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1c2-122">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="9b1c2-122">-KeyspaceName</span></span>
<span data-ttu-id="9b1c2-123">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="9b1c2-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="9b1c2-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9b1c2-124">-Name</span></span>
<span data-ttu-id="9b1c2-125">A táblázat neve: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="9b1c2-125">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="9b1c2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b1c2-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b1c2-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9b1c2-127">Name of resource group.</span></span>

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

### <span data-ttu-id="9b1c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1c2-128">CommonParameters</span></span>
<span data-ttu-id="9b1c2-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b1c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1c2-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9b1c2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1c2-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b1c2-131">INPUTS</span></span>

### <span data-ttu-id="9b1c2-132">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="9b1c2-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="9b1c2-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b1c2-133">OUTPUTS</span></span>

### <span data-ttu-id="9b1c2-134">Microsoft. Azure. Command. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="9b1c2-134">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="9b1c2-135">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9b1c2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9b1c2-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b1c2-136">NOTES</span></span>

## <span data-ttu-id="9b1c2-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b1c2-137">RELATED LINKS</span></span>
