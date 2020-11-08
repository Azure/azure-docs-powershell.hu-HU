---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBCassandraTable.md
ms.openlocfilehash: e79353d5265a2d58b72e49ee1978ea92599bed39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014439"
---
# <span data-ttu-id="e15d1-101">Set-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="e15d1-101">Set-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="e15d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e15d1-102">SYNOPSIS</span></span>
<span data-ttu-id="e15d1-103">A CosmosDB Cassandra (Cassandra) táblát állítja be.</span><span class="sxs-lookup"><span data-stu-id="e15d1-103">Sets the CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="e15d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e15d1-104">SYNTAX</span></span>

### <span data-ttu-id="e15d1-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e15d1-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>] -Schema <PSCassandraSchema>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e15d1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e15d1-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBCassandraTable -Name <String> [-Throughput <Int32>] [-TtlInSeconds <Int32>]
 -Schema <PSCassandraSchema> -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e15d1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e15d1-107">DESCRIPTION</span></span>
<span data-ttu-id="e15d1-108">A **set-AzCosmosDBCassandraTable** parancsmag a CosmosDB Cassandra szóköz billentyűt állítja be.</span><span class="sxs-lookup"><span data-stu-id="e15d1-108">The **Set-AzCosmosDBCassandraTable** cmdlet sets the CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="e15d1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e15d1-109">EXAMPLES</span></span>

### <span data-ttu-id="e15d1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e15d1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBCassandraTable -ResourceGroupName {rgName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
Name        Id    Resource
----        --    -------
{name}     {id}   Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="e15d1-111">Az erőforrás-objektum a _rid, az _ts, a _etag, a DefaultTtl és a séma tulajdonságainak értékét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e15d1-111">Resource object contains the values of the _rid, _ts, _etag, DefaultTtl and Schema properties.</span></span>

## <span data-ttu-id="e15d1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e15d1-112">PARAMETERS</span></span>

### <span data-ttu-id="e15d1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e15d1-113">-AccountName</span></span>
<span data-ttu-id="e15d1-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e15d1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e15d1-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e15d1-115">-Confirm</span></span>
<span data-ttu-id="e15d1-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e15d1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e15d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e15d1-117">-DefaultProfile</span></span>
<span data-ttu-id="e15d1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e15d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e15d1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e15d1-119">-InputObject</span></span>
<span data-ttu-id="e15d1-120">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="e15d1-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="e15d1-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="e15d1-121">-KeyspaceName</span></span>
<span data-ttu-id="e15d1-122">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="e15d1-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="e15d1-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e15d1-123">-Name</span></span>
<span data-ttu-id="e15d1-124">A táblázat neve: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="e15d1-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="e15d1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e15d1-125">-ResourceGroupName</span></span>
<span data-ttu-id="e15d1-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e15d1-126">Name of resource group.</span></span>

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

### <span data-ttu-id="e15d1-127">-Schema (séma)</span><span class="sxs-lookup"><span data-stu-id="e15d1-127">-Schema</span></span>
<span data-ttu-id="e15d1-128">PSCassandraSchema objektum</span><span class="sxs-lookup"><span data-stu-id="e15d1-128">PSCassandraSchema object.</span></span>
<span data-ttu-id="e15d1-129">Az objektum létrehozásához használja a New-AzCosmosDBCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="e15d1-129">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e15d1-130">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="e15d1-130">-Throughput</span></span>
<span data-ttu-id="e15d1-131">A szóköz (RU/s) méretének átvitele.</span><span class="sxs-lookup"><span data-stu-id="e15d1-131">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="e15d1-132">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="e15d1-132">Default value is 400.</span></span>

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

### <span data-ttu-id="e15d1-133">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="e15d1-133">-TtlInSeconds</span></span>
<span data-ttu-id="e15d1-134">Az alapértelmezett élettartam másodpercben</span><span class="sxs-lookup"><span data-stu-id="e15d1-134">Default Ttl in seconds.</span></span>
<span data-ttu-id="e15d1-135">Ha az érték hiányzik vagy a-1 érték van megadva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="e15d1-135">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="e15d1-136">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítási idő után lejárnak.</span><span class="sxs-lookup"><span data-stu-id="e15d1-136">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="e15d1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e15d1-137">-WhatIf</span></span>
<span data-ttu-id="e15d1-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e15d1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e15d1-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e15d1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e15d1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e15d1-140">CommonParameters</span></span>
<span data-ttu-id="e15d1-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e15d1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e15d1-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e15d1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e15d1-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e15d1-143">INPUTS</span></span>

### <span data-ttu-id="e15d1-144">Microsoft. Azure. Command. CosmosDB. models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="e15d1-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="e15d1-145">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="e15d1-145">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="e15d1-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e15d1-146">OUTPUTS</span></span>

### <span data-ttu-id="e15d1-147">Microsoft. Azure. Command. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="e15d1-147">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="e15d1-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e15d1-148">NOTES</span></span>

## <span data-ttu-id="e15d1-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e15d1-149">RELATED LINKS</span></span>
