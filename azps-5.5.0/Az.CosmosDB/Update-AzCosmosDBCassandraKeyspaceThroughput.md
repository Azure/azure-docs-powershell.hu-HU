---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144450"
---
# <span data-ttu-id="da6d0-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="da6d0-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="da6d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="da6d0-103">Frissíti a MintakDB kulcstér átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="da6d0-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="da6d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da6d0-104">SYNTAX</span></span>

### <span data-ttu-id="da6d0-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da6d0-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da6d0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da6d0-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da6d0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da6d0-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da6d0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da6d0-108">DESCRIPTION</span></span>
<span data-ttu-id="da6d0-109">Frissíti a MintakDB kulcstér átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="da6d0-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="da6d0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da6d0-110">EXAMPLES</span></span>

### <span data-ttu-id="da6d0-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="da6d0-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="da6d0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da6d0-112">PARAMETERS</span></span>

### <span data-ttu-id="da6d0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="da6d0-113">-AccountName</span></span>
<span data-ttu-id="da6d0-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="da6d0-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="da6d0-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="da6d0-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="da6d0-116">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="da6d0-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="da6d0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da6d0-117">-Confirm</span></span>
<span data-ttu-id="da6d0-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="da6d0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da6d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da6d0-119">-DefaultProfile</span></span>
<span data-ttu-id="da6d0-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da6d0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da6d0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da6d0-121">-InputObject</span></span>
<span data-ttu-id="da6d0-122">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="da6d0-122">CosmosDB Account object</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da6d0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="da6d0-123">-Name</span></span>
<span data-ttu-id="da6d0-124">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="da6d0-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="da6d0-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="da6d0-125">-ParentObject</span></span>
<span data-ttu-id="da6d0-126">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="da6d0-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="da6d0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da6d0-127">-ResourceGroupName</span></span>
<span data-ttu-id="da6d0-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="da6d0-128">Name of resource group.</span></span>

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

### <span data-ttu-id="da6d0-129">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="da6d0-129">-Throughput</span></span>
<span data-ttu-id="da6d0-130">A Siandra Keyspace (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="da6d0-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="da6d0-131">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="da6d0-131">Default value is 400.</span></span>

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

### <span data-ttu-id="da6d0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da6d0-132">-WhatIf</span></span>
<span data-ttu-id="da6d0-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="da6d0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da6d0-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da6d0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da6d0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da6d0-135">CommonParameters</span></span>
<span data-ttu-id="da6d0-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da6d0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da6d0-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da6d0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da6d0-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da6d0-138">INPUTS</span></span>

### <span data-ttu-id="da6d0-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="da6d0-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="da6d0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da6d0-140">OUTPUTS</span></span>

### <span data-ttu-id="da6d0-141">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="da6d0-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="da6d0-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da6d0-142">NOTES</span></span>

## <span data-ttu-id="da6d0-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da6d0-143">RELATED LINKS</span></span>
