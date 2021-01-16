---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362821"
---
# <span data-ttu-id="af1f9-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="af1f9-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="af1f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af1f9-102">SYNOPSIS</span></span>
<span data-ttu-id="af1f9-103">Létrehoz egy új 2016.010.010 000 000 000 000 000 00</span><span class="sxs-lookup"><span data-stu-id="af1f9-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="af1f9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="af1f9-104">SYNTAX</span></span>

### <span data-ttu-id="af1f9-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af1f9-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af1f9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af1f9-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af1f9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="af1f9-107">DESCRIPTION</span></span>
<span data-ttu-id="af1f9-108">Létrehoz egy új 2016.010.010 000 000 000 000 000 00</span><span class="sxs-lookup"><span data-stu-id="af1f9-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="af1f9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="af1f9-109">EXAMPLES</span></span>

### <span data-ttu-id="af1f9-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="af1f9-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="af1f9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af1f9-111">PARAMETERS</span></span>

### <span data-ttu-id="af1f9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="af1f9-112">-AccountName</span></span>
<span data-ttu-id="af1f9-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="af1f9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="af1f9-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="af1f9-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="af1f9-115">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="af1f9-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="af1f9-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af1f9-116">-Confirm</span></span>
<span data-ttu-id="af1f9-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="af1f9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af1f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af1f9-118">-DefaultProfile</span></span>
<span data-ttu-id="af1f9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af1f9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af1f9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="af1f9-120">-Name</span></span>
<span data-ttu-id="af1f9-121">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="af1f9-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="af1f9-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="af1f9-122">-ParentObject</span></span>
<span data-ttu-id="af1f9-123">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="af1f9-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="af1f9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af1f9-124">-ResourceGroupName</span></span>
<span data-ttu-id="af1f9-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="af1f9-125">Name of resource group.</span></span>

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

### <span data-ttu-id="af1f9-126">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="af1f9-126">-Throughput</span></span>
<span data-ttu-id="af1f9-127">A Siandra Keyspace (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="af1f9-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="af1f9-128">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="af1f9-128">Default value is 400.</span></span>

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

### <span data-ttu-id="af1f9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af1f9-129">-WhatIf</span></span>
<span data-ttu-id="af1f9-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="af1f9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af1f9-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af1f9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af1f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af1f9-132">CommonParameters</span></span>
<span data-ttu-id="af1f9-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af1f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af1f9-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af1f9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af1f9-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af1f9-135">INPUTS</span></span>

### <span data-ttu-id="af1f9-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="af1f9-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="af1f9-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af1f9-137">OUTPUTS</span></span>

### <span data-ttu-id="af1f9-138">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="af1f9-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="af1f9-139">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="af1f9-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="af1f9-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="af1f9-140">NOTES</span></span>

## <span data-ttu-id="af1f9-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af1f9-141">RELATED LINKS</span></span>
