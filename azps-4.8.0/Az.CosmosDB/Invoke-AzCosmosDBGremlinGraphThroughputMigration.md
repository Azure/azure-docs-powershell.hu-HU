---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16a477febeb5c0272f3e8cc36f577b0659f4826f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185091"
---
# <span data-ttu-id="93530-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="93530-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="93530-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93530-102">SYNOPSIS</span></span>
<span data-ttu-id="93530-103">Ezzel a beállítással áttelepítheti az automatikus méretezést a manuális átviteli sebességre, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="93530-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="93530-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93530-104">SYNTAX</span></span>

### <span data-ttu-id="93530-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93530-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93530-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93530-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93530-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93530-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93530-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="93530-108">DESCRIPTION</span></span>
<span data-ttu-id="93530-109">A ThroughpyteType paraméter határozza meg, hogy milyen átviteli sebességet szeretne áttelepíteni.</span><span class="sxs-lookup"><span data-stu-id="93530-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="93530-110">Példák</span><span class="sxs-lookup"><span data-stu-id="93530-110">EXAMPLES</span></span>

### <span data-ttu-id="93530-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="93530-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```


## <span data-ttu-id="93530-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93530-112">PARAMETERS</span></span>

### <span data-ttu-id="93530-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="93530-113">-AccountName</span></span>
<span data-ttu-id="93530-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="93530-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="93530-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="93530-115">-Confirm</span></span>
<span data-ttu-id="93530-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93530-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93530-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="93530-117">-DatabaseName</span></span>
<span data-ttu-id="93530-118">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="93530-118">Database name.</span></span>

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

### <span data-ttu-id="93530-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93530-119">-DefaultProfile</span></span>
<span data-ttu-id="93530-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93530-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93530-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93530-121">-InputObject</span></span>
<span data-ttu-id="93530-122">Gremlin gráf objektum.</span><span class="sxs-lookup"><span data-stu-id="93530-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93530-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="93530-123">-Name</span></span>
<span data-ttu-id="93530-124">Gremlin-diagram neve.</span><span class="sxs-lookup"><span data-stu-id="93530-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="93530-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="93530-125">-ParentObject</span></span>
<span data-ttu-id="93530-126">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="93530-126">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93530-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93530-127">-ResourceGroupName</span></span>
<span data-ttu-id="93530-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="93530-128">Name of resource group.</span></span>

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

### <span data-ttu-id="93530-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="93530-129">-ThroughputType</span></span>
<span data-ttu-id="93530-130">Az áttelepítéshez használandó átviteli típus.</span><span class="sxs-lookup"><span data-stu-id="93530-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="93530-131">Lehetséges értékek: automatikus méretezés, kézi.</span><span class="sxs-lookup"><span data-stu-id="93530-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="93530-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93530-132">-WhatIf</span></span>
<span data-ttu-id="93530-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="93530-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93530-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93530-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93530-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93530-135">CommonParameters</span></span>
<span data-ttu-id="93530-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93530-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93530-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="93530-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93530-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93530-138">INPUTS</span></span>

### <span data-ttu-id="93530-139">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="93530-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="93530-140">Microsoft. Azure. Command. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="93530-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="93530-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93530-141">OUTPUTS</span></span>

### <span data-ttu-id="93530-142">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="93530-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="93530-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93530-143">NOTES</span></span>

## <span data-ttu-id="93530-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93530-144">RELATED LINKS</span></span>
