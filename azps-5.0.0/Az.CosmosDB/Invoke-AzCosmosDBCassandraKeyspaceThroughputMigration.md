---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbcassandrakeyspacethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration.md
ms.openlocfilehash: a5e636f37b032411069b3e6c9a85226eb751705e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299450"
---
# <span data-ttu-id="222ac-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="222ac-101">Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration</span></span>

## <span data-ttu-id="222ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="222ac-102">SYNOPSIS</span></span>
<span data-ttu-id="222ac-103">Ezzel a beállítással áttelepítheti az automatikus méretezést a manuális átviteli sebességre, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="222ac-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="222ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="222ac-104">SYNTAX</span></span>

### <span data-ttu-id="222ac-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="222ac-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="222ac-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="222ac-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="222ac-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="222ac-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration [-Name <String>]
 -InputObject <PSCassandraKeyspaceGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="222ac-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="222ac-108">DESCRIPTION</span></span>
<span data-ttu-id="222ac-109">A ThroughpyteType paraméter határozza meg, hogy milyen átviteli sebességet szeretne áttelepíteni.</span><span class="sxs-lookup"><span data-stu-id="222ac-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="222ac-110">Példák</span><span class="sxs-lookup"><span data-stu-id="222ac-110">EXAMPLES</span></span>

### <span data-ttu-id="222ac-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="222ac-111">Example 1</span></span>
```powershell
PS C:\> $NewKeyspace =  New-AzCosmosDBCassandraKeyspace -AccountName myAccountName -ResourceGroupName myRgName -Name myKeyspaceName -Throughput  700
$AutoscaleThroughput = Invoke-AzCosmosDBCassandraKeyspaceThroughputMigration -InputObject $NewKeyspace -ThroughputType Autoscale
```

## <span data-ttu-id="222ac-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="222ac-112">PARAMETERS</span></span>

### <span data-ttu-id="222ac-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="222ac-113">-AccountName</span></span>
<span data-ttu-id="222ac-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="222ac-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="222ac-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="222ac-115">-Confirm</span></span>
<span data-ttu-id="222ac-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="222ac-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="222ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="222ac-117">-DefaultProfile</span></span>
<span data-ttu-id="222ac-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="222ac-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="222ac-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="222ac-119">-InputObject</span></span>
<span data-ttu-id="222ac-120">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="222ac-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="222ac-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="222ac-121">-Name</span></span>
<span data-ttu-id="222ac-122">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="222ac-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="222ac-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="222ac-123">-ParentObject</span></span>
<span data-ttu-id="222ac-124">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="222ac-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="222ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="222ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="222ac-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="222ac-126">Name of resource group.</span></span>

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

### <span data-ttu-id="222ac-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="222ac-127">-ThroughputType</span></span>
<span data-ttu-id="222ac-128">Az áttelepítéshez használandó átviteli típus.</span><span class="sxs-lookup"><span data-stu-id="222ac-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="222ac-129">Lehetséges értékek: automatikus méretezés, kézi.</span><span class="sxs-lookup"><span data-stu-id="222ac-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="222ac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="222ac-130">-WhatIf</span></span>
<span data-ttu-id="222ac-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="222ac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="222ac-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="222ac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="222ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="222ac-133">CommonParameters</span></span>
<span data-ttu-id="222ac-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="222ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="222ac-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="222ac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="222ac-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="222ac-136">INPUTS</span></span>

### <span data-ttu-id="222ac-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="222ac-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="222ac-138">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="222ac-138">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="222ac-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="222ac-139">OUTPUTS</span></span>

### <span data-ttu-id="222ac-140">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="222ac-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="222ac-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="222ac-141">NOTES</span></span>

## <span data-ttu-id="222ac-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="222ac-142">RELATED LINKS</span></span>
