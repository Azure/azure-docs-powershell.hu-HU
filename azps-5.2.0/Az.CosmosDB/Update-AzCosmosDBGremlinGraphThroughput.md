---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372383"
---
# <span data-ttu-id="83c2d-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="83c2d-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="83c2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="83c2d-103">Frissíti aTervsDB Gremlin Graph átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="83c2d-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="83c2d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83c2d-104">SYNTAX</span></span>

### <span data-ttu-id="83c2d-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83c2d-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83c2d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83c2d-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83c2d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83c2d-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83c2d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83c2d-108">DESCRIPTION</span></span>
<span data-ttu-id="83c2d-109">Frissíti aTervsDB Gremlin Graph átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="83c2d-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="83c2d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83c2d-110">EXAMPLES</span></span>

### <span data-ttu-id="83c2d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="83c2d-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="83c2d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83c2d-112">PARAMETERS</span></span>

### <span data-ttu-id="83c2d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="83c2d-113">-AccountName</span></span>
<span data-ttu-id="83c2d-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="83c2d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="83c2d-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="83c2d-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="83c2d-116">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="83c2d-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="83c2d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83c2d-117">-Confirm</span></span>
<span data-ttu-id="83c2d-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="83c2d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83c2d-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="83c2d-119">-DatabaseName</span></span>
<span data-ttu-id="83c2d-120">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="83c2d-120">Database name.</span></span>

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

### <span data-ttu-id="83c2d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c2d-121">-DefaultProfile</span></span>
<span data-ttu-id="83c2d-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83c2d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83c2d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83c2d-123">-InputObject</span></span>
<span data-ttu-id="83c2d-124">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="83c2d-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="83c2d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="83c2d-125">-Name</span></span>
<span data-ttu-id="83c2d-126">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="83c2d-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="83c2d-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="83c2d-127">-ParentObject</span></span>
<span data-ttu-id="83c2d-128">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="83c2d-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="83c2d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83c2d-129">-ResourceGroupName</span></span>
<span data-ttu-id="83c2d-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="83c2d-130">Name of resource group.</span></span>

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

### <span data-ttu-id="83c2d-131">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="83c2d-131">-Throughput</span></span>
<span data-ttu-id="83c2d-132">A Gremlin Graph (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="83c2d-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="83c2d-133">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="83c2d-133">Default value is 400.</span></span>

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

### <span data-ttu-id="83c2d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83c2d-134">-WhatIf</span></span>
<span data-ttu-id="83c2d-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="83c2d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83c2d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83c2d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83c2d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c2d-137">CommonParameters</span></span>
<span data-ttu-id="83c2d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83c2d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c2d-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83c2d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c2d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83c2d-140">INPUTS</span></span>

### <span data-ttu-id="83c2d-141">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="83c2d-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="83c2d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83c2d-142">OUTPUTS</span></span>

### <span data-ttu-id="83c2d-143">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="83c2d-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="83c2d-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83c2d-144">NOTES</span></span>

## <span data-ttu-id="83c2d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83c2d-145">RELATED LINKS</span></span>
