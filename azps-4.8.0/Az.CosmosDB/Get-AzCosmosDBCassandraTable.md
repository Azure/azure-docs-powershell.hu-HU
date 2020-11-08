---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185095"
---
# <span data-ttu-id="4d64a-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="4d64a-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="4d64a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d64a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d64a-103">CosmosDB Cassandra-táblázatot kap.</span><span class="sxs-lookup"><span data-stu-id="4d64a-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="4d64a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d64a-104">SYNTAX</span></span>

### <span data-ttu-id="4d64a-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d64a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d64a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d64a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d64a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d64a-107">DESCRIPTION</span></span>
<span data-ttu-id="4d64a-108">A **Get-AzCosmosDBCassandraTable** parancsmag új vagy frissített CosmosDB hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4d64a-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="4d64a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4d64a-109">EXAMPLES</span></span>

### <span data-ttu-id="4d64a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4d64a-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="4d64a-111">{{Get-AzCosmosDBCassandraTable egy meglévő CassandraKeyspace tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4d64a-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="4d64a-112">Az erőforrás kibontásával kibonthatja a DefaultTtl, a sémát, a _etagt, a _tst _rid tulajdonságokat.}}</span><span class="sxs-lookup"><span data-stu-id="4d64a-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="4d64a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d64a-113">PARAMETERS</span></span>

### <span data-ttu-id="4d64a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d64a-114">-AccountName</span></span>
<span data-ttu-id="4d64a-115">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="4d64a-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4d64a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d64a-116">-DefaultProfile</span></span>
<span data-ttu-id="4d64a-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d64a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d64a-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="4d64a-118">-KeyspaceName</span></span>
<span data-ttu-id="4d64a-119">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="4d64a-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="4d64a-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d64a-120">-Name</span></span>
<span data-ttu-id="4d64a-121">A táblázat neve: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4d64a-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="4d64a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4d64a-122">-ParentObject</span></span>
<span data-ttu-id="4d64a-123">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="4d64a-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="4d64a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d64a-124">-ResourceGroupName</span></span>
<span data-ttu-id="4d64a-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d64a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="4d64a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d64a-126">CommonParameters</span></span>
<span data-ttu-id="4d64a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d64a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d64a-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4d64a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d64a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d64a-129">INPUTS</span></span>

### <span data-ttu-id="4d64a-130">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4d64a-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="4d64a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d64a-131">OUTPUTS</span></span>

### <span data-ttu-id="4d64a-132">Microsoft. Azure. Command. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="4d64a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="4d64a-133">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4d64a-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4d64a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d64a-134">NOTES</span></span>

## <span data-ttu-id="4d64a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d64a-135">RELATED LINKS</span></span>
