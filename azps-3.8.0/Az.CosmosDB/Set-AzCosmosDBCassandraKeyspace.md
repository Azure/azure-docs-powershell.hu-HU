---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: d1b0dcee6c4337a572f98a51cb03c3fcdcd6c84e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014440"
---
# <span data-ttu-id="406ac-101">Set-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="406ac-101">Set-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="406ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="406ac-102">SYNOPSIS</span></span>
<span data-ttu-id="406ac-103">A CosmosDB Cassandra szóköz billentyűt határozza meg.</span><span class="sxs-lookup"><span data-stu-id="406ac-103">Sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="406ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="406ac-104">SYNTAX</span></span>

### <span data-ttu-id="406ac-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="406ac-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="406ac-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="406ac-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="406ac-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="406ac-107">DESCRIPTION</span></span>
<span data-ttu-id="406ac-108">A **set-AzCosmosDBCassandraKeyspace** parancsmag a CosmosDB Cassandra szóköz billentyűt állítja be.</span><span class="sxs-lookup"><span data-stu-id="406ac-108">The **Set-AzCosmosDBCassandraKeyspace** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="406ac-109">Példák</span><span class="sxs-lookup"><span data-stu-id="406ac-109">EXAMPLES</span></span>

### <span data-ttu-id="406ac-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="406ac-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraKeyspace -ResourceGroupName {rgName} -AccountName {accountName} -Name {keyspaceName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

<span data-ttu-id="406ac-111">Az erőforrás-objektum a _rid, a _ts és a _etag tulajdonság értékét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="406ac-111">Resource object contains the values of the _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="406ac-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="406ac-112">PARAMETERS</span></span>

### <span data-ttu-id="406ac-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="406ac-113">-AccountName</span></span>
<span data-ttu-id="406ac-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="406ac-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="406ac-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="406ac-115">-Confirm</span></span>
<span data-ttu-id="406ac-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="406ac-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406ac-117">-DefaultProfile</span></span>
<span data-ttu-id="406ac-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="406ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="406ac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="406ac-119">-InputObject</span></span>
<span data-ttu-id="406ac-120">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="406ac-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="406ac-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="406ac-121">-Name</span></span>
<span data-ttu-id="406ac-122">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="406ac-122">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="406ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="406ac-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="406ac-124">Name of resource group.</span></span>

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

### <span data-ttu-id="406ac-125">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="406ac-125">-Throughput</span></span>
<span data-ttu-id="406ac-126">A szóköz (RU/s) méretének átvitele.</span><span class="sxs-lookup"><span data-stu-id="406ac-126">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="406ac-127">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="406ac-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406ac-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="406ac-128">-WhatIf</span></span>
<span data-ttu-id="406ac-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="406ac-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="406ac-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="406ac-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406ac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406ac-131">CommonParameters</span></span>
<span data-ttu-id="406ac-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="406ac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406ac-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="406ac-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406ac-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="406ac-134">INPUTS</span></span>

### <span data-ttu-id="406ac-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="406ac-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="406ac-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="406ac-136">OUTPUTS</span></span>

### <span data-ttu-id="406ac-137">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="406ac-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="406ac-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="406ac-138">NOTES</span></span>

## <span data-ttu-id="406ac-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="406ac-139">RELATED LINKS</span></span>
