---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 4a9a5595345b44eaf3a3b44d9d9ba1d8895a6376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931338"
---
# <span data-ttu-id="df28d-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="df28d-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="df28d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df28d-102">SYNOPSIS</span></span>
<span data-ttu-id="df28d-103">Frissíti a 2010.02.012.012.</span><span class="sxs-lookup"><span data-stu-id="df28d-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="df28d-104">Ügyféloldali javítást hajt végre a meglévő Keyspace felolvassa.</span><span class="sxs-lookup"><span data-stu-id="df28d-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="df28d-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df28d-105">SYNTAX</span></span>

### <span data-ttu-id="df28d-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df28d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df28d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df28d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df28d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df28d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df28d-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df28d-109">DESCRIPTION</span></span>
<span data-ttu-id="df28d-110">Frissíti a 2010.02.012.012.</span><span class="sxs-lookup"><span data-stu-id="df28d-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="df28d-111">Ügyféloldali javítást hajt végre a meglévő Keyspace felolvassa.</span><span class="sxs-lookup"><span data-stu-id="df28d-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="df28d-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df28d-112">EXAMPLES</span></span>

### <span data-ttu-id="df28d-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="df28d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="df28d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df28d-114">PARAMETERS</span></span>

### <span data-ttu-id="df28d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="df28d-115">-AccountName</span></span>
<span data-ttu-id="df28d-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="df28d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="df28d-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="df28d-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="df28d-118">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="df28d-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="df28d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df28d-119">-Confirm</span></span>
<span data-ttu-id="df28d-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="df28d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df28d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df28d-121">-DefaultProfile</span></span>
<span data-ttu-id="df28d-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df28d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df28d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df28d-123">-InputObject</span></span>
<span data-ttu-id="df28d-124">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="df28d-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="df28d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="df28d-125">-Name</span></span>
<span data-ttu-id="df28d-126">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="df28d-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="df28d-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="df28d-127">-ParentObject</span></span>
<span data-ttu-id="df28d-128">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="df28d-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="df28d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df28d-129">-ResourceGroupName</span></span>
<span data-ttu-id="df28d-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="df28d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="df28d-131">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="df28d-131">-Throughput</span></span>
<span data-ttu-id="df28d-132">A Siandra Keyspace (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="df28d-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="df28d-133">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="df28d-133">Default value is 400.</span></span>

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

### <span data-ttu-id="df28d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df28d-134">-WhatIf</span></span>
<span data-ttu-id="df28d-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="df28d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df28d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df28d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df28d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df28d-137">CommonParameters</span></span>
<span data-ttu-id="df28d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df28d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df28d-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df28d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df28d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df28d-140">INPUTS</span></span>

### <span data-ttu-id="df28d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="df28d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="df28d-142">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="df28d-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="df28d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df28d-143">OUTPUTS</span></span>

### <span data-ttu-id="df28d-144">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="df28d-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="df28d-145">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="df28d-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="df28d-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df28d-146">NOTES</span></span>

## <span data-ttu-id="df28d-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df28d-147">RELATED LINKS</span></span>
