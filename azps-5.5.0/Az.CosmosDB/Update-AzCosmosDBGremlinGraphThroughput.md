---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148483"
---
# <span data-ttu-id="03c17-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="03c17-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="03c17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c17-102">SYNOPSIS</span></span>
<span data-ttu-id="03c17-103">Frissíti aTervsDB Gremlin Graph átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="03c17-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="03c17-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03c17-104">SYNTAX</span></span>

### <span data-ttu-id="03c17-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03c17-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c17-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03c17-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c17-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03c17-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c17-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03c17-108">DESCRIPTION</span></span>
<span data-ttu-id="03c17-109">Frissíti aTervsDB Gremlin Graph átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="03c17-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="03c17-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03c17-110">EXAMPLES</span></span>

### <span data-ttu-id="03c17-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="03c17-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="03c17-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03c17-112">PARAMETERS</span></span>

### <span data-ttu-id="03c17-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="03c17-113">-AccountName</span></span>
<span data-ttu-id="03c17-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="03c17-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="03c17-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="03c17-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="03c17-116">Maximális átviteli sebesség, ha engedélyezve van az automatikus méretezés.</span><span class="sxs-lookup"><span data-stu-id="03c17-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="03c17-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03c17-117">-Confirm</span></span>
<span data-ttu-id="03c17-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="03c17-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c17-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="03c17-119">-DatabaseName</span></span>
<span data-ttu-id="03c17-120">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="03c17-120">Database name.</span></span>

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

### <span data-ttu-id="03c17-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c17-121">-DefaultProfile</span></span>
<span data-ttu-id="03c17-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03c17-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c17-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03c17-123">-InputObject</span></span>
<span data-ttu-id="03c17-124">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="03c17-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="03c17-125">-Name</span><span class="sxs-lookup"><span data-stu-id="03c17-125">-Name</span></span>
<span data-ttu-id="03c17-126">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="03c17-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="03c17-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="03c17-127">-ParentObject</span></span>
<span data-ttu-id="03c17-128">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="03c17-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="03c17-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c17-129">-ResourceGroupName</span></span>
<span data-ttu-id="03c17-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="03c17-130">Name of resource group.</span></span>

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

### <span data-ttu-id="03c17-131">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="03c17-131">-Throughput</span></span>
<span data-ttu-id="03c17-132">A Gremlin Graph (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="03c17-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="03c17-133">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="03c17-133">Default value is 400.</span></span>

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

### <span data-ttu-id="03c17-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c17-134">-WhatIf</span></span>
<span data-ttu-id="03c17-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="03c17-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c17-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="03c17-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c17-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c17-137">CommonParameters</span></span>
<span data-ttu-id="03c17-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03c17-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c17-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03c17-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c17-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03c17-140">INPUTS</span></span>

### <span data-ttu-id="03c17-141">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="03c17-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="03c17-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03c17-142">OUTPUTS</span></span>

### <span data-ttu-id="03c17-143">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="03c17-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="03c17-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03c17-144">NOTES</span></span>

## <span data-ttu-id="03c17-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03c17-145">RELATED LINKS</span></span>
