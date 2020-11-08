---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: ee1527beb11db3027a416277ed04a444dda90af0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012183"
---
# <span data-ttu-id="91d7b-101">Update-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="91d7b-101">Update-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="91d7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="91d7b-103">Frissíti a CosmosDB Gremlin gráf átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="91d7b-103">Updates the throughput value of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="91d7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91d7b-104">SYNTAX</span></span>

### <span data-ttu-id="91d7b-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91d7b-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91d7b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91d7b-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91d7b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91d7b-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinGraphThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSGremlinGraphGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91d7b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="91d7b-108">EXAMPLES</span></span>

### <span data-ttu-id="91d7b-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="91d7b-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinGraphThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myGraphName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabase/{mydatabaseName}/graphs/{myGraphName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="91d7b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91d7b-110">PARAMETERS</span></span>

### <span data-ttu-id="91d7b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="91d7b-111">-AccountName</span></span>
<span data-ttu-id="91d7b-112">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="91d7b-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="91d7b-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91d7b-113">-Confirm</span></span>
<span data-ttu-id="91d7b-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91d7b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91d7b-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="91d7b-115">-DatabaseName</span></span>
<span data-ttu-id="91d7b-116">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="91d7b-116">Database name.</span></span>

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

### <span data-ttu-id="91d7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d7b-117">-DefaultProfile</span></span>
<span data-ttu-id="91d7b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91d7b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91d7b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91d7b-119">-InputObject</span></span>
<span data-ttu-id="91d7b-120">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="91d7b-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="91d7b-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91d7b-121">-Name</span></span>
<span data-ttu-id="91d7b-122">Gremlin-diagram neve.</span><span class="sxs-lookup"><span data-stu-id="91d7b-122">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="91d7b-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="91d7b-123">-ParentObject</span></span>
<span data-ttu-id="91d7b-124">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="91d7b-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="91d7b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91d7b-125">-ResourceGroupName</span></span>
<span data-ttu-id="91d7b-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="91d7b-126">Name of resource group.</span></span>

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

### <span data-ttu-id="91d7b-127">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="91d7b-127">-Throughput</span></span>
<span data-ttu-id="91d7b-128">A Gremlin gráf (RU/s) átviteli sebessége</span><span class="sxs-lookup"><span data-stu-id="91d7b-128">The throughput of Gremlin Graph (RU/s).</span></span>
<span data-ttu-id="91d7b-129">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="91d7b-129">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d7b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91d7b-130">-WhatIf</span></span>
<span data-ttu-id="91d7b-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91d7b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91d7b-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91d7b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91d7b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d7b-133">CommonParameters</span></span>
<span data-ttu-id="91d7b-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91d7b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d7b-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="91d7b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d7b-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91d7b-136">INPUTS</span></span>

### <span data-ttu-id="91d7b-137">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="91d7b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="91d7b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91d7b-138">OUTPUTS</span></span>

### <span data-ttu-id="91d7b-139">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="91d7b-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="91d7b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91d7b-140">NOTES</span></span>

## <span data-ttu-id="91d7b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91d7b-141">RELATED LINKS</span></span>
