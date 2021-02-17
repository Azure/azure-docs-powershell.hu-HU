---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbgremlingraphthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBGremlinGraphThroughputMigration.md
ms.openlocfilehash: 16817d4af40ddd27a8838f40618758686af26a58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164090"
---
# <span data-ttu-id="c8f83-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="c8f83-101">Invoke-AzCosmosDBGremlinGraphThroughputMigration</span></span>

## <span data-ttu-id="c8f83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8f83-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f83-103">Ezzel a funkcióval az automatikus skálás átviteli sebességet manuális átviteli sebességre, illetve fordítva.</span><span class="sxs-lookup"><span data-stu-id="c8f83-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="c8f83-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c8f83-104">SYNTAX</span></span>

### <span data-ttu-id="c8f83-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8f83-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8f83-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f83-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8f83-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8f83-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBGremlinGraphThroughputMigration [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8f83-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c8f83-108">DESCRIPTION</span></span>
<span data-ttu-id="c8f83-109">Az ThroughpyteType paraméter azt az átviteli sebességet határozza meg, amelybe át szeretne áttérni.</span><span class="sxs-lookup"><span data-stu-id="c8f83-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="c8f83-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c8f83-110">EXAMPLES</span></span>

### <span data-ttu-id="c8f83-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c8f83-111">Example 1</span></span>
```powershell
PS C:\>  $NewGraph =  New-AzCosmosDBGremlinGraph -AccountName myAccountName -ResourceGroupName myRgName -Name myGraphName -Throughput 700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBGremlinGraphThroughputMigration -InputObject $NewGraph -ThroughputType Autoscale
```

## <span data-ttu-id="c8f83-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8f83-112">PARAMETERS</span></span>

### <span data-ttu-id="c8f83-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c8f83-113">-AccountName</span></span>
<span data-ttu-id="c8f83-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="c8f83-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c8f83-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8f83-115">-Confirm</span></span>
<span data-ttu-id="c8f83-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c8f83-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8f83-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8f83-117">-DatabaseName</span></span>
<span data-ttu-id="c8f83-118">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="c8f83-118">Database name.</span></span>

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

### <span data-ttu-id="c8f83-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f83-119">-DefaultProfile</span></span>
<span data-ttu-id="c8f83-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8f83-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8f83-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8f83-121">-InputObject</span></span>
<span data-ttu-id="c8f83-122">Gremlin Graph-objektum.</span><span class="sxs-lookup"><span data-stu-id="c8f83-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="c8f83-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c8f83-123">-Name</span></span>
<span data-ttu-id="c8f83-124">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="c8f83-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="c8f83-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c8f83-125">-ParentObject</span></span>
<span data-ttu-id="c8f83-126">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="c8f83-126">Gremlin Database object.</span></span>

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

### <span data-ttu-id="c8f83-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8f83-127">-ResourceGroupName</span></span>
<span data-ttu-id="c8f83-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c8f83-128">Name of resource group.</span></span>

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

### <span data-ttu-id="c8f83-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="c8f83-129">-ThroughputType</span></span>
<span data-ttu-id="c8f83-130">Az áttűnni megfelelő átviteli sebesség típusa.</span><span class="sxs-lookup"><span data-stu-id="c8f83-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="c8f83-131">Lehetséges értékek: Automatikus méretezés, Kézi.</span><span class="sxs-lookup"><span data-stu-id="c8f83-131">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="c8f83-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8f83-132">-WhatIf</span></span>
<span data-ttu-id="c8f83-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c8f83-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8f83-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8f83-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8f83-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f83-135">CommonParameters</span></span>
<span data-ttu-id="c8f83-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f83-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f83-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8f83-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f83-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8f83-138">INPUTS</span></span>

### <span data-ttu-id="c8f83-139">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="c8f83-139">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="c8f83-140">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="c8f83-140">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="c8f83-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8f83-141">OUTPUTS</span></span>

### <span data-ttu-id="c8f83-142">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c8f83-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c8f83-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c8f83-143">NOTES</span></span>

## <span data-ttu-id="c8f83-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8f83-144">RELATED LINKS</span></span>
