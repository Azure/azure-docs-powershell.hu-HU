---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandratablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraTableThroughputMigration.md
ms.openlocfilehash: b6199720d9ac59c608482632518b47829a7c0b9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185093"
---
# <span data-ttu-id="fb83f-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="fb83f-101">Invoke-AzCosmosDBCassandraTableThroughputMigration</span></span>

## <span data-ttu-id="fb83f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb83f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb83f-103">Ezzel a beállítással áttelepítheti az automatikus méretezést a manuális átviteli sebességre, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="fb83f-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="fb83f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb83f-104">SYNTAX</span></span>

### <span data-ttu-id="fb83f-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb83f-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration -KeyspaceName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb83f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb83f-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>]
 -ParentObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb83f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb83f-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraTableThroughputMigration [-Name <String>] -InputObject <PSCassandraTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb83f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb83f-108">DESCRIPTION</span></span>
<span data-ttu-id="fb83f-109">A ThroughpyteType paraméter határozza meg, hogy milyen átviteli sebességet szeretne áttelepíteni.</span><span class="sxs-lookup"><span data-stu-id="fb83f-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="fb83f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fb83f-110">EXAMPLES</span></span>

### <span data-ttu-id="fb83f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fb83f-111">Example 1</span></span>
```powershell
PS C:\>$NewTable =  New-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700 -KeyspaceName myKeyspaceName
      $AutoscaleThroughput = Invoke-AzCosmosDBCassandraTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="fb83f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb83f-112">PARAMETERS</span></span>

### <span data-ttu-id="fb83f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fb83f-113">-AccountName</span></span>
<span data-ttu-id="fb83f-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="fb83f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fb83f-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb83f-115">-Confirm</span></span>
<span data-ttu-id="fb83f-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb83f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb83f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb83f-117">-DefaultProfile</span></span>
<span data-ttu-id="fb83f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb83f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb83f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb83f-119">-InputObject</span></span>
<span data-ttu-id="fb83f-120">Cassandra Table objektum.</span><span class="sxs-lookup"><span data-stu-id="fb83f-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="fb83f-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="fb83f-121">-KeyspaceName</span></span>
<span data-ttu-id="fb83f-122">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="fb83f-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="fb83f-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb83f-123">-Name</span></span>
<span data-ttu-id="fb83f-124">A táblázat neve: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="fb83f-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="fb83f-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fb83f-125">-ParentObject</span></span>
<span data-ttu-id="fb83f-126">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="fb83f-126">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="fb83f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb83f-127">-ResourceGroupName</span></span>
<span data-ttu-id="fb83f-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb83f-128">Name of resource group.</span></span>

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

### <span data-ttu-id="fb83f-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="fb83f-129">-ThroughputType</span></span>
<span data-ttu-id="fb83f-130">Az áttelepítéshez használandó átviteli típus.</span><span class="sxs-lookup"><span data-stu-id="fb83f-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="fb83f-131">Lehetséges értékek: automatikus méretezés, kézi.</span><span class="sxs-lookup"><span data-stu-id="fb83f-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="fb83f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb83f-132">-WhatIf</span></span>
<span data-ttu-id="fb83f-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb83f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb83f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb83f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb83f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb83f-135">CommonParameters</span></span>
<span data-ttu-id="fb83f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb83f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb83f-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fb83f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb83f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb83f-138">INPUTS</span></span>

### <span data-ttu-id="fb83f-139">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="fb83f-139">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="fb83f-140">Microsoft. Azure. Command. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="fb83f-140">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="fb83f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb83f-141">OUTPUTS</span></span>

### <span data-ttu-id="fb83f-142">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fb83f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fb83f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb83f-143">NOTES</span></span>

## <span data-ttu-id="fb83f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb83f-144">RELATED LINKS</span></span>