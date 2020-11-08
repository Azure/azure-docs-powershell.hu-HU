---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 8998e9e2462e64dab3d2a96c739c93449e2e360c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025463"
---
# <span data-ttu-id="0fb09-101">New-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="0fb09-101">New-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="0fb09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fb09-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb09-103">Új CosmosDB hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0fb09-103">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0fb09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fb09-104">SYNTAX</span></span>

### <span data-ttu-id="0fb09-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0fb09-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fb09-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fb09-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBCassandraKeyspace -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fb09-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fb09-107">DESCRIPTION</span></span>
<span data-ttu-id="0fb09-108">Új CosmosDB hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0fb09-108">Creates a new CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="0fb09-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0fb09-109">EXAMPLES</span></span>

### <span data-ttu-id="0fb09-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0fb09-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="0fb09-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fb09-111">PARAMETERS</span></span>

### <span data-ttu-id="0fb09-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0fb09-112">-AccountName</span></span>
<span data-ttu-id="0fb09-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="0fb09-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0fb09-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="0fb09-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="0fb09-115">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="0fb09-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="0fb09-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0fb09-116">-Confirm</span></span>
<span data-ttu-id="0fb09-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0fb09-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fb09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb09-118">-DefaultProfile</span></span>
<span data-ttu-id="0fb09-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fb09-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fb09-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0fb09-120">-Name</span></span>
<span data-ttu-id="0fb09-121">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="0fb09-121">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="0fb09-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0fb09-122">-ParentObject</span></span>
<span data-ttu-id="0fb09-123">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="0fb09-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="0fb09-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fb09-124">-ResourceGroupName</span></span>
<span data-ttu-id="0fb09-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0fb09-125">Name of resource group.</span></span>

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

### <span data-ttu-id="0fb09-126">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="0fb09-126">-Throughput</span></span>
<span data-ttu-id="0fb09-127">A szóköz (RU/s) méretének átvitele.</span><span class="sxs-lookup"><span data-stu-id="0fb09-127">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="0fb09-128">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="0fb09-128">Default value is 400.</span></span>

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

### <span data-ttu-id="0fb09-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fb09-129">-WhatIf</span></span>
<span data-ttu-id="0fb09-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0fb09-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fb09-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fb09-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fb09-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb09-132">CommonParameters</span></span>
<span data-ttu-id="0fb09-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fb09-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb09-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0fb09-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb09-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fb09-135">INPUTS</span></span>

### <span data-ttu-id="0fb09-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0fb09-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0fb09-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fb09-137">OUTPUTS</span></span>

### <span data-ttu-id="0fb09-138">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="0fb09-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="0fb09-139">Microsoft. Azure. Command. CosmosDB. kivétellel. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="0fb09-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="0fb09-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fb09-140">NOTES</span></span>

## <span data-ttu-id="0fb09-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fb09-141">RELATED LINKS</span></span>
