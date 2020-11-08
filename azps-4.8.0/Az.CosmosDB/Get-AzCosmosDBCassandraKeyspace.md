---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182399"
---
# <span data-ttu-id="36ccc-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="36ccc-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="36ccc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="36ccc-103">Beolvassa a CosmosDB Cassandra szóköz billentyűt.</span><span class="sxs-lookup"><span data-stu-id="36ccc-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="36ccc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36ccc-104">SYNTAX</span></span>

### <span data-ttu-id="36ccc-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36ccc-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36ccc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36ccc-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36ccc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="36ccc-107">DESCRIPTION</span></span>
<span data-ttu-id="36ccc-108">A **Get-AzCosmosDBCassandraKeyspace** parancsmag új vagy frissített CosmosDB hoz létre.</span><span class="sxs-lookup"><span data-stu-id="36ccc-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="36ccc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="36ccc-109">EXAMPLES</span></span>

### <span data-ttu-id="36ccc-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="36ccc-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="36ccc-111">A Get-AzCosmosDBCassandraKeyspace egy meglévő CassandraKeyspace tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="36ccc-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="36ccc-112">Az erőforrás kibontásával kibonthatja a _etagt, _tst _rid tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="36ccc-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="36ccc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36ccc-113">PARAMETERS</span></span>

### <span data-ttu-id="36ccc-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36ccc-114">-AccountName</span></span>
<span data-ttu-id="36ccc-115">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="36ccc-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="36ccc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ccc-116">-DefaultProfile</span></span>
<span data-ttu-id="36ccc-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36ccc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36ccc-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36ccc-118">-Name</span></span>
<span data-ttu-id="36ccc-119">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="36ccc-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="36ccc-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="36ccc-120">-ParentObject</span></span>
<span data-ttu-id="36ccc-121">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="36ccc-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36ccc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ccc-122">-ResourceGroupName</span></span>
<span data-ttu-id="36ccc-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="36ccc-123">Name of resource group.</span></span>

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

### <span data-ttu-id="36ccc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ccc-124">CommonParameters</span></span>
<span data-ttu-id="36ccc-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36ccc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ccc-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="36ccc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ccc-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36ccc-127">INPUTS</span></span>

### <span data-ttu-id="36ccc-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="36ccc-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="36ccc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36ccc-129">OUTPUTS</span></span>

### <span data-ttu-id="36ccc-130">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="36ccc-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="36ccc-131">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="36ccc-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="36ccc-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36ccc-132">NOTES</span></span>

## <span data-ttu-id="36ccc-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36ccc-133">RELATED LINKS</span></span>
