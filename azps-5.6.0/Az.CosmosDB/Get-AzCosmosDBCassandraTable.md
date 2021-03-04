---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 2d784a82974f47c67bae89d55042b81c9c83e273
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931985"
---
# <span data-ttu-id="bce5b-101">Get-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="bce5b-101">Get-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="bce5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bce5b-102">SYNOPSIS</span></span>
<span data-ttu-id="bce5b-103">2016.01.012-es táblázatot kap.</span><span class="sxs-lookup"><span data-stu-id="bce5b-103">Gets a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="bce5b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bce5b-104">SYNTAX</span></span>

### <span data-ttu-id="bce5b-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bce5b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTable -AccountName <String> -KeyspaceName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bce5b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bce5b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTable [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bce5b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bce5b-107">DESCRIPTION</span></span>
<span data-ttu-id="bce5b-108">A **Get-AzCosmosDBCassandraTable** parancsmag létrehoz egy újat, vagy frissíti a már meglévő, a AztandB kulcsteret.</span><span class="sxs-lookup"><span data-stu-id="bce5b-108">The **Get-AzCosmosDBCassandraTable** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="bce5b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bce5b-109">EXAMPLES</span></span>

### <span data-ttu-id="bce5b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="bce5b-110">Example 1</span></span>
```powershell
PS C:\> $table = Get-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="bce5b-111">{{ Get-AzCosmosDBCassandraTable egy meglévő 100000000000000000000000000000000000000000000</span><span class="sxs-lookup"><span data-stu-id="bce5b-111">{{ Get-AzCosmosDBCassandraTable gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="bce5b-112">Bontsa ki az erőforrást a DefaultTtl, a Séma, a _etag, a _ts és a _rid be.}}</span><span class="sxs-lookup"><span data-stu-id="bce5b-112">You can expand the Resource to get the DefaultTtl, Schema, _etag, _ts, _rid properties.}}</span></span>

## <span data-ttu-id="bce5b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bce5b-113">PARAMETERS</span></span>

### <span data-ttu-id="bce5b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bce5b-114">-AccountName</span></span>
<span data-ttu-id="bce5b-115">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="bce5b-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bce5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce5b-116">-DefaultProfile</span></span>
<span data-ttu-id="bce5b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bce5b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce5b-118">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="bce5b-118">-KeyspaceName</span></span>
<span data-ttu-id="bce5b-119">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="bce5b-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="bce5b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bce5b-120">-Name</span></span>
<span data-ttu-id="bce5b-121">Kéttáblás tábla neve.</span><span class="sxs-lookup"><span data-stu-id="bce5b-121">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="bce5b-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bce5b-122">-ParentObject</span></span>
<span data-ttu-id="bce5b-123">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="bce5b-123">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="bce5b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce5b-124">-ResourceGroupName</span></span>
<span data-ttu-id="bce5b-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bce5b-125">Name of resource group.</span></span>

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

### <span data-ttu-id="bce5b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce5b-126">CommonParameters</span></span>
<span data-ttu-id="bce5b-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce5b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce5b-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bce5b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce5b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bce5b-129">INPUTS</span></span>

### <span data-ttu-id="bce5b-130">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="bce5b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="bce5b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bce5b-131">OUTPUTS</span></span>

### <span data-ttu-id="bce5b-132">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="bce5b-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="bce5b-133">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bce5b-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bce5b-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bce5b-134">NOTES</span></span>

## <span data-ttu-id="bce5b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bce5b-135">RELATED LINKS</span></span>
