---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299078"
---
# <span data-ttu-id="3ca50-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="3ca50-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="3ca50-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ca50-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca50-103">Frissíti egy CosmosDB Cassandra Table átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="3ca50-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="3ca50-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ca50-104">SYNTAX</span></span>

### <span data-ttu-id="3ca50-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ca50-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca50-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca50-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca50-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca50-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca50-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ca50-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca50-109">Frissíti egy CosmosDB Cassandra Table átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="3ca50-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="3ca50-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3ca50-110">EXAMPLES</span></span>

### <span data-ttu-id="3ca50-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3ca50-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="3ca50-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ca50-112">PARAMETERS</span></span>

### <span data-ttu-id="3ca50-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3ca50-113">-AccountName</span></span>
<span data-ttu-id="3ca50-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="3ca50-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3ca50-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="3ca50-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="3ca50-116">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="3ca50-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="3ca50-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ca50-117">-Confirm</span></span>
<span data-ttu-id="3ca50-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ca50-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca50-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca50-119">-DefaultProfile</span></span>
<span data-ttu-id="3ca50-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ca50-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca50-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ca50-121">-InputObject</span></span>
<span data-ttu-id="3ca50-122">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="3ca50-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="3ca50-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="3ca50-123">-KeyspaceName</span></span>
<span data-ttu-id="3ca50-124">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="3ca50-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="3ca50-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ca50-125">-Name</span></span>
<span data-ttu-id="3ca50-126">A táblázat neve: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="3ca50-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="3ca50-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3ca50-127">-ParentObject</span></span>
<span data-ttu-id="3ca50-128">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="3ca50-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="3ca50-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca50-129">-ResourceGroupName</span></span>
<span data-ttu-id="3ca50-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3ca50-130">Name of resource group.</span></span>

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

### <span data-ttu-id="3ca50-131">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="3ca50-131">-Throughput</span></span>
<span data-ttu-id="3ca50-132">A szóköz (RU/s) méretének átvitele.</span><span class="sxs-lookup"><span data-stu-id="3ca50-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="3ca50-133">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="3ca50-133">Default value is 400.</span></span>

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

### <span data-ttu-id="3ca50-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca50-134">-WhatIf</span></span>
<span data-ttu-id="3ca50-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ca50-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca50-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ca50-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca50-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca50-137">CommonParameters</span></span>
<span data-ttu-id="3ca50-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ca50-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca50-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3ca50-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca50-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ca50-140">INPUTS</span></span>

### <span data-ttu-id="3ca50-141">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="3ca50-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="3ca50-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ca50-142">OUTPUTS</span></span>

### <span data-ttu-id="3ca50-143">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3ca50-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3ca50-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ca50-144">NOTES</span></span>

## <span data-ttu-id="3ca50-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ca50-145">RELATED LINKS</span></span>
