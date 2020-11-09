---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299576"
---
# <span data-ttu-id="7640f-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="7640f-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="7640f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7640f-102">SYNOPSIS</span></span>
<span data-ttu-id="7640f-103">Beolvassa a CosmosDB Cassandra szóköz billentyűt.</span><span class="sxs-lookup"><span data-stu-id="7640f-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="7640f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7640f-104">SYNTAX</span></span>

### <span data-ttu-id="7640f-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7640f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7640f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7640f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7640f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7640f-107">DESCRIPTION</span></span>
<span data-ttu-id="7640f-108">A **Get-AzCosmosDBCassandraKeyspace** parancsmag új vagy frissített CosmosDB hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7640f-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="7640f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7640f-109">EXAMPLES</span></span>

### <span data-ttu-id="7640f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7640f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="7640f-111">A Get-AzCosmosDBCassandraKeyspace egy meglévő CassandraKeyspace tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7640f-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="7640f-112">Az erőforrás kibontásával kibonthatja a _etagt, _tst _rid tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7640f-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="7640f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7640f-113">PARAMETERS</span></span>

### <span data-ttu-id="7640f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7640f-114">-AccountName</span></span>
<span data-ttu-id="7640f-115">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="7640f-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7640f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7640f-116">-DefaultProfile</span></span>
<span data-ttu-id="7640f-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7640f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7640f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7640f-118">-Name</span></span>
<span data-ttu-id="7640f-119">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="7640f-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="7640f-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7640f-120">-ParentObject</span></span>
<span data-ttu-id="7640f-121">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="7640f-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7640f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7640f-122">-ResourceGroupName</span></span>
<span data-ttu-id="7640f-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7640f-123">Name of resource group.</span></span>

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

### <span data-ttu-id="7640f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7640f-124">CommonParameters</span></span>
<span data-ttu-id="7640f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7640f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7640f-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7640f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7640f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7640f-127">INPUTS</span></span>

### <span data-ttu-id="7640f-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7640f-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="7640f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7640f-129">OUTPUTS</span></span>

### <span data-ttu-id="7640f-130">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="7640f-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="7640f-131">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="7640f-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7640f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7640f-132">NOTES</span></span>

## <span data-ttu-id="7640f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7640f-133">RELATED LINKS</span></span>
