---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 9c3aff7edb26863f2843ef517c7ce0f08f91296f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014423"
---
# <span data-ttu-id="4038e-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="4038e-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="4038e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4038e-102">SYNOPSIS</span></span>
<span data-ttu-id="4038e-103">Frissíti egy CosmosDB Cassandra Table átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="4038e-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="4038e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4038e-104">SYNTAX</span></span>

### <span data-ttu-id="4038e-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4038e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String>
 -KeyspaceName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4038e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4038e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4038e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4038e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4038e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4038e-108">EXAMPLES</span></span>

### <span data-ttu-id="4038e-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4038e-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="4038e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4038e-110">PARAMETERS</span></span>

### <span data-ttu-id="4038e-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4038e-111">-AccountName</span></span>
<span data-ttu-id="4038e-112">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="4038e-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4038e-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4038e-113">-Confirm</span></span>
<span data-ttu-id="4038e-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4038e-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4038e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4038e-115">-DefaultProfile</span></span>
<span data-ttu-id="4038e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4038e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4038e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4038e-117">-InputObject</span></span>
<span data-ttu-id="4038e-118">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="4038e-118">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4038e-119">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="4038e-119">-KeyspaceName</span></span>
<span data-ttu-id="4038e-120">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="4038e-120">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="4038e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4038e-121">-Name</span></span>
<span data-ttu-id="4038e-122">A táblázat neve: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4038e-122">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="4038e-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4038e-123">-ParentObject</span></span>
<span data-ttu-id="4038e-124">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="4038e-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="4038e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4038e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4038e-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4038e-126">Name of resource group.</span></span>

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

### <span data-ttu-id="4038e-127">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="4038e-127">-Throughput</span></span>
<span data-ttu-id="4038e-128">A szóköz (RU/s) méretének átvitele.</span><span class="sxs-lookup"><span data-stu-id="4038e-128">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="4038e-129">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="4038e-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4038e-130">-WhatIf</span></span>
<span data-ttu-id="4038e-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4038e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4038e-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4038e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4038e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4038e-133">CommonParameters</span></span>
<span data-ttu-id="4038e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4038e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4038e-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4038e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4038e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4038e-136">INPUTS</span></span>

### <span data-ttu-id="4038e-137">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="4038e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="4038e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4038e-138">OUTPUTS</span></span>

### <span data-ttu-id="4038e-139">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4038e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4038e-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4038e-140">NOTES</span></span>

## <span data-ttu-id="4038e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4038e-141">RELATED LINKS</span></span>
