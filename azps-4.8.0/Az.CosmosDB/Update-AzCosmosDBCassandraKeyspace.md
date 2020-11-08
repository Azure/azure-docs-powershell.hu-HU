---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: cff6f0bd099e8379e47f4100bd4b20a3b6eb36b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182372"
---
# <span data-ttu-id="c6c09-101">Update-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="c6c09-101">Update-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="c6c09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c6c09-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c09-103">A CosmosDB Cassandra szóköz frissítése</span><span class="sxs-lookup"><span data-stu-id="c6c09-103">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="c6c09-104">Ügyféloldali javítás műveletet hajt végre a meglévő térköz elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="c6c09-104">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="c6c09-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c6c09-105">SYNTAX</span></span>

### <span data-ttu-id="c6c09-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c6c09-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6c09-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6c09-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6c09-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6c09-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraKeyspace [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6c09-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c6c09-109">DESCRIPTION</span></span>
<span data-ttu-id="c6c09-110">A CosmosDB Cassandra szóköz frissítése</span><span class="sxs-lookup"><span data-stu-id="c6c09-110">Updates the CosmosDB Cassandra Keyspace.</span></span> <span data-ttu-id="c6c09-111">Ügyféloldali javítás műveletet hajt végre a meglévő térköz elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="c6c09-111">Performs a client side patch operation by reading the existing Keyspace.</span></span>

## <span data-ttu-id="c6c09-112">Példák</span><span class="sxs-lookup"><span data-stu-id="c6c09-112">EXAMPLES</span></span>

### <span data-ttu-id="c6c09-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c6c09-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput 600

Name     : myKeyspace
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetPropertiesResource
```

## <span data-ttu-id="c6c09-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c6c09-114">PARAMETERS</span></span>

### <span data-ttu-id="c6c09-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c6c09-115">-AccountName</span></span>
<span data-ttu-id="c6c09-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="c6c09-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c6c09-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c6c09-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c6c09-118">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="c6c09-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c6c09-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c6c09-119">-Confirm</span></span>
<span data-ttu-id="c6c09-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c6c09-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6c09-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c09-121">-DefaultProfile</span></span>
<span data-ttu-id="c6c09-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c6c09-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c09-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6c09-123">-InputObject</span></span>
<span data-ttu-id="c6c09-124">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="c6c09-124">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="c6c09-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c6c09-125">-Name</span></span>
<span data-ttu-id="c6c09-126">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="c6c09-126">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="c6c09-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c6c09-127">-ParentObject</span></span>
<span data-ttu-id="c6c09-128">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="c6c09-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c6c09-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c09-129">-ResourceGroupName</span></span>
<span data-ttu-id="c6c09-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c6c09-130">Name of resource group.</span></span>

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

### <span data-ttu-id="c6c09-131">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="c6c09-131">-Throughput</span></span>
<span data-ttu-id="c6c09-132">A szóköz (RU/s) méretének átvitele.</span><span class="sxs-lookup"><span data-stu-id="c6c09-132">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="c6c09-133">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="c6c09-133">Default value is 400.</span></span>

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

### <span data-ttu-id="c6c09-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6c09-134">-WhatIf</span></span>
<span data-ttu-id="c6c09-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c6c09-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6c09-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6c09-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6c09-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c09-137">CommonParameters</span></span>
<span data-ttu-id="c6c09-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c6c09-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c09-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c6c09-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c09-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6c09-140">INPUTS</span></span>

### <span data-ttu-id="c6c09-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c6c09-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="c6c09-142">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c6c09-142">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="c6c09-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6c09-143">OUTPUTS</span></span>

### <span data-ttu-id="c6c09-144">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="c6c09-144">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="c6c09-145">Microsoft. Azure. Command. CosmosDB. kivétellel. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c6c09-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="c6c09-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c6c09-146">NOTES</span></span>

## <span data-ttu-id="c6c09-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6c09-147">RELATED LINKS</span></span>
