---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 633ea5263930db74cec3b926c655e54dec10a162
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299042"
---
# <span data-ttu-id="ef5de-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="ef5de-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="ef5de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef5de-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5de-103">Frissíti a CosmosDB Gremlin gráf átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="ef5de-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="ef5de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef5de-104">SYNTAX</span></span>

### <span data-ttu-id="ef5de-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef5de-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -DatabaseName <String> [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef5de-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef5de-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef5de-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef5de-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef5de-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef5de-108">DESCRIPTION</span></span>
<span data-ttu-id="ef5de-109">Frissíti a CosmosDB Gremlin gráf átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="ef5de-109">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="ef5de-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ef5de-110">EXAMPLES</span></span>

### <span data-ttu-id="ef5de-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ef5de-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="ef5de-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef5de-112">PARAMETERS</span></span>

### <span data-ttu-id="ef5de-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ef5de-113">-AccountName</span></span>
<span data-ttu-id="ef5de-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ef5de-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ef5de-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="ef5de-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="ef5de-116">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="ef5de-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="ef5de-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef5de-117">-Confirm</span></span>
<span data-ttu-id="ef5de-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef5de-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef5de-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef5de-119">-DatabaseName</span></span>
<span data-ttu-id="ef5de-120">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ef5de-120">Database name.</span></span>

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

### <span data-ttu-id="ef5de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef5de-121">-DefaultProfile</span></span>
<span data-ttu-id="ef5de-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef5de-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef5de-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef5de-123">-InputObject</span></span>
<span data-ttu-id="ef5de-124">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="ef5de-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="ef5de-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef5de-125">-Name</span></span>
<span data-ttu-id="ef5de-126">Gremlin-diagram neve.</span><span class="sxs-lookup"><span data-stu-id="ef5de-126">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="ef5de-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ef5de-127">-ParentObject</span></span>
<span data-ttu-id="ef5de-128">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="ef5de-128">Gremlin Database object.</span></span>

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

### <span data-ttu-id="ef5de-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5de-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef5de-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ef5de-130">Name of resource group.</span></span>

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

### <span data-ttu-id="ef5de-131">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="ef5de-131">-Throughput</span></span>
<span data-ttu-id="ef5de-132">A Gremlin gráf (RU/s) átviteli sebessége</span><span class="sxs-lookup"><span data-stu-id="ef5de-132">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="ef5de-133">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="ef5de-133">Default value is 400.</span></span>

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

### <span data-ttu-id="ef5de-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef5de-134">-WhatIf</span></span>
<span data-ttu-id="ef5de-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef5de-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef5de-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef5de-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef5de-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5de-137">CommonParameters</span></span>
<span data-ttu-id="ef5de-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef5de-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5de-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ef5de-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5de-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef5de-140">INPUTS</span></span>

### <span data-ttu-id="ef5de-141">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="ef5de-141">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="ef5de-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef5de-142">OUTPUTS</span></span>

### <span data-ttu-id="ef5de-143">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ef5de-143">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ef5de-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef5de-144">NOTES</span></span>

## <span data-ttu-id="ef5de-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef5de-145">RELATED LINKS</span></span>
