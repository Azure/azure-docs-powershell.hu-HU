---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480535"
---
# <span data-ttu-id="028b2-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="028b2-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="028b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="028b2-102">SYNOPSIS</span></span>
<span data-ttu-id="028b2-103">Frissíti a 2010.02.012.012.</span><span class="sxs-lookup"><span data-stu-id="028b2-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="028b2-104">Ügyféloldali javítást hajt végre a meglévő Keyspace felolvassa.</span><span class="sxs-lookup"><span data-stu-id="028b2-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="028b2-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="028b2-105">SYNTAX</span></span>

### <span data-ttu-id="028b2-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="028b2-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="028b2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="028b2-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="028b2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="028b2-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="028b2-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="028b2-109">DESCRIPTION</span></span>
<span data-ttu-id="028b2-110">Frissíti a 2010.02.012.012.</span><span class="sxs-lookup"><span data-stu-id="028b2-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="028b2-111">Ügyféloldali javítást hajt végre a meglévő Keyspace felolvassa.</span><span class="sxs-lookup"><span data-stu-id="028b2-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="028b2-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="028b2-112">EXAMPLES</span></span>

### <span data-ttu-id="028b2-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="028b2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="028b2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="028b2-114">PARAMETERS</span></span>

### <span data-ttu-id="028b2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="028b2-115">-AccountName</span></span>
<span data-ttu-id="028b2-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="028b2-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="028b2-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="028b2-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="028b2-118">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="028b2-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="028b2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="028b2-119">-Confirm</span></span>
<span data-ttu-id="028b2-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="028b2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="028b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028b2-121">-DefaultProfile</span></span>
<span data-ttu-id="028b2-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="028b2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="028b2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="028b2-123">-InputObject</span></span>
<span data-ttu-id="028b2-124">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="028b2-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="028b2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="028b2-125">-Name</span></span>
<span data-ttu-id="028b2-126">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="028b2-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="028b2-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="028b2-127">-ParentObject</span></span>
<span data-ttu-id="028b2-128">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="028b2-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="028b2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="028b2-129">-ResourceGroupName</span></span>
<span data-ttu-id="028b2-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="028b2-130">Name of resource group.</span></span>

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

### <span data-ttu-id="028b2-131">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="028b2-131">-Throughput</span></span>
<span data-ttu-id="028b2-132">A Siandra Keyspace (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="028b2-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="028b2-133">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="028b2-133">Default value is 400.</span></span>

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

### <span data-ttu-id="028b2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="028b2-134">-WhatIf</span></span>
<span data-ttu-id="028b2-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="028b2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="028b2-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="028b2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="028b2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028b2-137">CommonParameters</span></span>
<span data-ttu-id="028b2-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="028b2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028b2-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="028b2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028b2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="028b2-140">INPUTS</span></span>

### <span data-ttu-id="028b2-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="028b2-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="028b2-142">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="028b2-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="028b2-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="028b2-143">OUTPUTS</span></span>

### <span data-ttu-id="028b2-144">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="028b2-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="028b2-145">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="028b2-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="028b2-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="028b2-146">NOTES</span></span>

## <span data-ttu-id="028b2-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="028b2-147">RELATED LINKS</span></span>
