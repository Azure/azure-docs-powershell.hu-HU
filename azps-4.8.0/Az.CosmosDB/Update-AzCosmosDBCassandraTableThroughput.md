---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184191"
---
# <span data-ttu-id="ca65f-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="ca65f-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="ca65f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca65f-102">SYNOPSIS</span></span>
<span data-ttu-id="ca65f-103">Frissíti egy CosmosDB Cassandra Table átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="ca65f-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="ca65f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca65f-104">SYNTAX</span></span>

### <span data-ttu-id="ca65f-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca65f-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca65f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca65f-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca65f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca65f-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca65f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca65f-108">DESCRIPTION</span></span>
<span data-ttu-id="ca65f-109">Frissíti egy CosmosDB Cassandra Table átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="ca65f-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="ca65f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ca65f-110">EXAMPLES</span></span>

### <span data-ttu-id="ca65f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ca65f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="ca65f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca65f-112">PARAMETERS</span></span>

### <span data-ttu-id="ca65f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ca65f-113">-AccountName</span></span>
<span data-ttu-id="ca65f-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ca65f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ca65f-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ca65f-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ca65f-116">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ca65f-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ca65f-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca65f-117">-Confirm</span></span>
<span data-ttu-id="ca65f-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca65f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca65f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca65f-119">-DefaultProfile</span></span>
<span data-ttu-id="ca65f-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca65f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca65f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca65f-121">-InputObject</span></span>
<span data-ttu-id="ca65f-122">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="ca65f-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="ca65f-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="ca65f-123">-KeyspaceName</span></span>
<span data-ttu-id="ca65f-124">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="ca65f-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="ca65f-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca65f-125">-Name</span></span>
<span data-ttu-id="ca65f-126">A táblázat neve: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ca65f-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="ca65f-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ca65f-127">-ParentObject</span></span>
<span data-ttu-id="ca65f-128">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="ca65f-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="ca65f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca65f-129">-ResourceGroupName</span></span>
<span data-ttu-id="ca65f-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ca65f-130">Name of resource group.</span></span>

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

### <span data-ttu-id="ca65f-131">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="ca65f-131">-Throughput</span></span>
<span data-ttu-id="ca65f-132">A szóköz (RU/s) méretének átvitele.</span><span class="sxs-lookup"><span data-stu-id="ca65f-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="ca65f-133">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="ca65f-133">Default value is 400.</span></span>

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

### <span data-ttu-id="ca65f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca65f-134">-WhatIf</span></span>
<span data-ttu-id="ca65f-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca65f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca65f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca65f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca65f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca65f-137">CommonParameters</span></span>
<span data-ttu-id="ca65f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca65f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca65f-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ca65f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca65f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca65f-140">INPUTS</span></span>

### <span data-ttu-id="ca65f-141">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="ca65f-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="ca65f-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca65f-142">OUTPUTS</span></span>

### <span data-ttu-id="ca65f-143">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ca65f-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ca65f-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca65f-144">NOTES</span></span>

## <span data-ttu-id="ca65f-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca65f-145">RELATED LINKS</span></span>
