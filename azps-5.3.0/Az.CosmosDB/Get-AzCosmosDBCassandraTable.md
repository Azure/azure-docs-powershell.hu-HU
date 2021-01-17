---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 8994cab45a10f874d0c544f231e20c27a01039f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480618"
---
# <span data-ttu-id="99a4c-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="99a4c-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="99a4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="99a4c-103">2016.01.012-es táblázatot kap.</span><span class="sxs-lookup"><span data-stu-id="99a4c-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="99a4c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="99a4c-104">SYNTAX</span></span>

### <span data-ttu-id="99a4c-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99a4c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99a4c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99a4c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99a4c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="99a4c-107">DESCRIPTION</span></span>
<span data-ttu-id="99a4c-108">A **Get-AzCosmosDBCassandraTable** parancsmag létrehoz egy újat, vagy frissíti a már meglévő, a 2010-es És a 365555556655556655444444444.omktókat.</span><span class="sxs-lookup"><span data-stu-id="99a4c-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="99a4c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="99a4c-109">EXAMPLES</span></span>

### <span data-ttu-id="99a4c-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="99a4c-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="99a4c-111">{{ Get-AzCosmosDBCassandraTable egy meglévő 100000000000000000000000000000000000000000000</span><span class="sxs-lookup"><span data-stu-id="99a4c-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="99a4c-112">Bontsa ki az erőforrást a DefaultTtl, a Séma, a _etag, a _ts és a _rid be.}}</span><span class="sxs-lookup"><span data-stu-id="99a4c-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="99a4c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99a4c-113">PARAMETERS</span></span>

### <span data-ttu-id="99a4c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="99a4c-114">-AccountName</span></span>
<span data-ttu-id="99a4c-115">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="99a4c-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="99a4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a4c-116">-DefaultProfile</span></span>
<span data-ttu-id="99a4c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99a4c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99a4c-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="99a4c-118">-KeyspaceName</span></span>
<span data-ttu-id="99a4c-119">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="99a4c-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="99a4c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="99a4c-120">-Name</span></span>
<span data-ttu-id="99a4c-121">Kéttáblás tábla neve.</span><span class="sxs-lookup"><span data-stu-id="99a4c-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="99a4c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="99a4c-122">-ParentObject</span></span>
<span data-ttu-id="99a4c-123">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="99a4c-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="99a4c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99a4c-124">-ResourceGroupName</span></span>
<span data-ttu-id="99a4c-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="99a4c-125">Name of resource group.</span></span>

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

### <span data-ttu-id="99a4c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a4c-126">CommonParameters</span></span>
<span data-ttu-id="99a4c-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99a4c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a4c-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99a4c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a4c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99a4c-129">INPUTS</span></span>

### <span data-ttu-id="99a4c-130">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="99a4c-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="99a4c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99a4c-131">OUTPUTS</span></span>

### <span data-ttu-id="99a4c-132">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="99a4c-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="99a4c-133">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="99a4c-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="99a4c-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="99a4c-134">NOTES</span></span>

## <span data-ttu-id="99a4c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99a4c-135">RELATED LINKS</span></span>
