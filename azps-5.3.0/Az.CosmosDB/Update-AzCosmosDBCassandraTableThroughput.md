---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: f686a9923b8281029984a0fc84fcd5d51866256d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477370"
---
# <span data-ttu-id="f6b2f-101">Update-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="f6b2f-101">Update-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="f6b2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b2f-103">Frissíti a KétesDB-táblázat átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-103">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="f6b2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f6b2f-104">SYNTAX</span></span>

### <span data-ttu-id="f6b2f-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6b2f-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTableThroughput -KeyspaceName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6b2f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6b2f-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -ParentObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6b2f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6b2f-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTableThroughput [-Name <String>] -InputObject <PSCassandraTableGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6b2f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f6b2f-108">DESCRIPTION</span></span>
<span data-ttu-id="f6b2f-109">Frissíti a KétesDB-táblázat átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-109">Updates the throughput value of a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="f6b2f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f6b2f-110">EXAMPLES</span></span>

### <span data-ttu-id="f6b2f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="f6b2f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -KeyspaceName {myKeyspacename} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/tables/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="f6b2f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6b2f-112">PARAMETERS</span></span>

### <span data-ttu-id="f6b2f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f6b2f-113">-AccountName</span></span>
<span data-ttu-id="f6b2f-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f6b2f-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f6b2f-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f6b2f-116">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f6b2f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6b2f-117">-Confirm</span></span>
<span data-ttu-id="f6b2f-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6b2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b2f-119">-DefaultProfile</span></span>
<span data-ttu-id="f6b2f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6b2f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6b2f-121">-InputObject</span></span>
<span data-ttu-id="f6b2f-122">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="f6b2f-122">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="f6b2f-123">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="f6b2f-123">-KeyspaceName</span></span>
<span data-ttu-id="f6b2f-124">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="f6b2f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f6b2f-125">-Name</span></span>
<span data-ttu-id="f6b2f-126">Kéttáblás tábla neve.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-126">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="f6b2f-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f6b2f-127">-ParentObject</span></span>
<span data-ttu-id="f6b2f-128">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="f6b2f-128">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="f6b2f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6b2f-129">-ResourceGroupName</span></span>
<span data-ttu-id="f6b2f-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-130">Name of resource group.</span></span>

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

### <span data-ttu-id="f6b2f-131">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="f6b2f-131">-Throughput</span></span>
<span data-ttu-id="f6b2f-132">A Siandra Keyspace (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="f6b2f-133">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-133">Default value is 400.</span></span>

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

### <span data-ttu-id="f6b2f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6b2f-134">-WhatIf</span></span>
<span data-ttu-id="f6b2f-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6b2f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6b2f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b2f-137">CommonParameters</span></span>
<span data-ttu-id="f6b2f-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6b2f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b2f-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6b2f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b2f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6b2f-140">INPUTS</span></span>

### <span data-ttu-id="f6b2f-141">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f6b2f-141">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="f6b2f-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6b2f-142">OUTPUTS</span></span>

### <span data-ttu-id="f6b2f-143">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f6b2f-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f6b2f-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f6b2f-144">NOTES</span></span>

## <span data-ttu-id="f6b2f-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6b2f-145">RELATED LINKS</span></span>
