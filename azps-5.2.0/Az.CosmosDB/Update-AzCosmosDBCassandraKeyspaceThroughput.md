---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 43dcbd97047ef72104a3b000f760b49aa3dfaab6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344646"
---
# <span data-ttu-id="0b05e-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="0b05e-101">Update-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="0b05e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b05e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b05e-103">Frissíti a MintakDB kulcstér átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="0b05e-103">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0b05e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0b05e-104">SYNTAX</span></span>

### <span data-ttu-id="0b05e-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0b05e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b05e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b05e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b05e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b05e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspaceThroughput [-Name <String>] -InputObject <PSCassandraKeyspaceGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b05e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0b05e-108">DESCRIPTION</span></span>
<span data-ttu-id="0b05e-109">Frissíti a MintakDB kulcstér átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="0b05e-109">Updates the throughput value of a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0b05e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0b05e-110">EXAMPLES</span></span>

### <span data-ttu-id="0b05e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="0b05e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspaceThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myKeyspaceName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/cassandraKeyspace/{myKeyspaceName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="0b05e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b05e-112">PARAMETERS</span></span>

### <span data-ttu-id="0b05e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0b05e-113">-AccountName</span></span>
<span data-ttu-id="0b05e-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="0b05e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0b05e-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="0b05e-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0b05e-116">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="0b05e-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0b05e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b05e-117">-Confirm</span></span>
<span data-ttu-id="0b05e-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0b05e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b05e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b05e-119">-DefaultProfile</span></span>
<span data-ttu-id="0b05e-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0b05e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b05e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b05e-121">-InputObject</span></span>
<span data-ttu-id="0b05e-122">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="0b05e-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0b05e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0b05e-123">-Name</span></span>
<span data-ttu-id="0b05e-124">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="0b05e-124">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="0b05e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0b05e-125">-ParentObject</span></span>
<span data-ttu-id="0b05e-126">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="0b05e-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0b05e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b05e-127">-ResourceGroupName</span></span>
<span data-ttu-id="0b05e-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0b05e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="0b05e-129">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="0b05e-129">-Throughput</span></span>
<span data-ttu-id="0b05e-130">A Siandra Keyspace (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="0b05e-130">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="0b05e-131">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="0b05e-131">Default value is 400.</span></span>

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

### <span data-ttu-id="0b05e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b05e-132">-WhatIf</span></span>
<span data-ttu-id="0b05e-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0b05e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b05e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0b05e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b05e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b05e-135">CommonParameters</span></span>
<span data-ttu-id="0b05e-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b05e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b05e-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b05e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b05e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b05e-138">INPUTS</span></span>

### <span data-ttu-id="0b05e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0b05e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0b05e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0b05e-140">OUTPUTS</span></span>

### <span data-ttu-id="0b05e-141">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0b05e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0b05e-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0b05e-142">NOTES</span></span>

## <span data-ttu-id="0b05e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0b05e-143">RELATED LINKS</span></span>
