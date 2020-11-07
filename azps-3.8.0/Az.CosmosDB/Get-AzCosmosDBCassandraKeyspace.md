---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cd9c9ba5f46ec83cf9b804e103ad1038662ca271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845641"
---
# <span data-ttu-id="2e3e1-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="2e3e1-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="2e3e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3e1-103">Beolvassa a CosmosDB Cassandra szóköz billentyűt.</span><span class="sxs-lookup"><span data-stu-id="2e3e1-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="2e3e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e3e1-104">SYNTAX</span></span>

### <span data-ttu-id="2e3e1-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e3e1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e3e1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e3e1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e3e1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e3e1-107">DESCRIPTION</span></span>
<span data-ttu-id="2e3e1-108">A **Get-AzCosmosDBCassandraKeyspace** parancsmag új vagy frissített CosmosDB hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2e3e1-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="2e3e1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2e3e1-109">EXAMPLES</span></span>

### <span data-ttu-id="2e3e1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2e3e1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="2e3e1-111">A Get-AzCosmosDBCassandraKeyspace egy meglévő CassandraKeyspace tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2e3e1-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="2e3e1-112">Az erőforrás kibontásával kibonthatja a _etagt, _tst _rid tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2e3e1-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="2e3e1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e3e1-113">PARAMETERS</span></span>

### <span data-ttu-id="2e3e1-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2e3e1-114">-AccountName</span></span>
<span data-ttu-id="2e3e1-115">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="2e3e1-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2e3e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3e1-116">-DefaultProfile</span></span>
<span data-ttu-id="2e3e1-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e3e1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e3e1-118">– Részletes</span><span class="sxs-lookup"><span data-stu-id="2e3e1-118">-Detailed</span></span>
<span data-ttu-id="2e3e1-119">Ha meg van határozva, akkor a parancsmag a megfelelő átviteli értékkel rendelkező térközt adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="2e3e1-119">If provided then, the cmdlet returns the Keyspace with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="2e3e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e3e1-120">-InputObject</span></span>
<span data-ttu-id="2e3e1-121">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="2e3e1-121">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e3e1-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e3e1-122">-Name</span></span>
<span data-ttu-id="2e3e1-123">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="2e3e1-123">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="2e3e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e3e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="2e3e1-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2e3e1-125">Name of resource group.</span></span>

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

### <span data-ttu-id="2e3e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3e1-126">CommonParameters</span></span>
<span data-ttu-id="2e3e1-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e3e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3e1-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e3e1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3e1-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e3e1-129">INPUTS</span></span>

### <span data-ttu-id="2e3e1-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2e3e1-130">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="2e3e1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e3e1-131">OUTPUTS</span></span>

### <span data-ttu-id="2e3e1-132">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="2e3e1-132">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="2e3e1-133">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2e3e1-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2e3e1-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e3e1-134">NOTES</span></span>

## <span data-ttu-id="2e3e1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e3e1-135">RELATED LINKS</span></span>
