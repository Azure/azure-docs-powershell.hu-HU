---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlindatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinDatabaseThroughputMigration.md
ms.openlocfilehash: 84039f883937354cf8c8fae3c99bfbc6f73bb574
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182568"
---
# <span data-ttu-id="2527d-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="2527d-101">Invoke-AzCosmosDBGremlinDatabaseThroughputMigration</span></span>

## <span data-ttu-id="2527d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2527d-102">SYNOPSIS</span></span>
<span data-ttu-id="2527d-103">Ezzel a beállítással áttelepítheti az automatikus méretezést a manuális átviteli sebességre, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="2527d-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="2527d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2527d-104">SYNTAX</span></span>

### <span data-ttu-id="2527d-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2527d-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2527d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2527d-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2527d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2527d-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinDatabaseThroughputMigration [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2527d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2527d-108">DESCRIPTION</span></span>
<span data-ttu-id="2527d-109">A ThroughpyteType paraméter határozza meg, hogy milyen átviteli sebességet szeretne áttelepíteni.</span><span class="sxs-lookup"><span data-stu-id="2527d-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="2527d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2527d-110">EXAMPLES</span></span>

### <span data-ttu-id="2527d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2527d-111">Example 1</span></span>
```powershell
PS C:\> $NewDb =  New-AzCosmosDBGremlinDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinDatabaseThroughputMigration -InputObject $NewDb -ThroughputType Autoscale
```


## <span data-ttu-id="2527d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2527d-112">PARAMETERS</span></span>

### <span data-ttu-id="2527d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2527d-113">-AccountName</span></span>
<span data-ttu-id="2527d-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="2527d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2527d-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2527d-115">-Confirm</span></span>
<span data-ttu-id="2527d-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2527d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2527d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2527d-117">-DefaultProfile</span></span>
<span data-ttu-id="2527d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2527d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2527d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2527d-119">-InputObject</span></span>
<span data-ttu-id="2527d-120">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="2527d-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2527d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2527d-121">-Name</span></span>
<span data-ttu-id="2527d-122">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="2527d-122">Database name.</span></span>

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

### <span data-ttu-id="2527d-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2527d-123">-ParentObject</span></span>
<span data-ttu-id="2527d-124">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="2527d-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2527d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2527d-125">-ResourceGroupName</span></span>
<span data-ttu-id="2527d-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2527d-126">Name of resource group.</span></span>

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

### <span data-ttu-id="2527d-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="2527d-127">-ThroughputType</span></span>
<span data-ttu-id="2527d-128">Az áttelepítéshez használandó átviteli típus.</span><span class="sxs-lookup"><span data-stu-id="2527d-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="2527d-129">Lehetséges értékek: automatikus méretezés, kézi.</span><span class="sxs-lookup"><span data-stu-id="2527d-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="2527d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2527d-130">-WhatIf</span></span>
<span data-ttu-id="2527d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2527d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2527d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2527d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2527d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2527d-133">CommonParameters</span></span>
<span data-ttu-id="2527d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2527d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2527d-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2527d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2527d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2527d-136">INPUTS</span></span>

### <span data-ttu-id="2527d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="2527d-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="2527d-138">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2527d-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="2527d-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2527d-139">OUTPUTS</span></span>

### <span data-ttu-id="2527d-140">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2527d-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2527d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2527d-141">NOTES</span></span>

## <span data-ttu-id="2527d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2527d-142">RELATED LINKS</span></span>
