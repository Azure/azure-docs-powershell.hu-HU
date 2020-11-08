---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184203"
---
# <span data-ttu-id="b6e45-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="b6e45-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="b6e45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6e45-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e45-103">A CosmosDB Gremlin gráf átviteli sebességét kapja.</span><span class="sxs-lookup"><span data-stu-id="b6e45-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b6e45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6e45-104">SYNTAX</span></span>

### <span data-ttu-id="b6e45-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6e45-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6e45-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6e45-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6e45-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6e45-107">DESCRIPTION</span></span>
<span data-ttu-id="b6e45-108">A **Get-AzCosmosDBGremlinGraphThroughput** parancsmag a CosmosDB Gremlin gráf átviteli sebességét kapja.</span><span class="sxs-lookup"><span data-stu-id="b6e45-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="b6e45-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b6e45-109">EXAMPLES</span></span>

### <span data-ttu-id="b6e45-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b6e45-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="b6e45-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6e45-111">PARAMETERS</span></span>

### <span data-ttu-id="b6e45-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6e45-112">-AccountName</span></span>
<span data-ttu-id="b6e45-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="b6e45-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b6e45-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6e45-114">-Confirm</span></span>
<span data-ttu-id="b6e45-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6e45-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6e45-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b6e45-116">-DatabaseName</span></span>
<span data-ttu-id="b6e45-117">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b6e45-117">Database name.</span></span>

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

### <span data-ttu-id="b6e45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e45-118">-DefaultProfile</span></span>
<span data-ttu-id="b6e45-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6e45-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6e45-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6e45-120">-InputObject</span></span>
<span data-ttu-id="b6e45-121">Gremlin gráf objektum.</span><span class="sxs-lookup"><span data-stu-id="b6e45-121">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e45-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6e45-122">-Name</span></span>
<span data-ttu-id="b6e45-123">Gremlin-diagram neve.</span><span class="sxs-lookup"><span data-stu-id="b6e45-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="b6e45-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6e45-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6e45-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b6e45-125">Name of resource group.</span></span>

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

### <span data-ttu-id="b6e45-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6e45-126">-WhatIf</span></span>
<span data-ttu-id="b6e45-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6e45-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6e45-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6e45-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6e45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e45-129">CommonParameters</span></span>
<span data-ttu-id="b6e45-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6e45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e45-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b6e45-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e45-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6e45-132">INPUTS</span></span>

### <span data-ttu-id="b6e45-133">Microsoft. Azure. Command. CosmosDB. models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="b6e45-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="b6e45-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6e45-134">OUTPUTS</span></span>

### <span data-ttu-id="b6e45-135">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b6e45-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b6e45-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6e45-136">NOTES</span></span>

## <span data-ttu-id="b6e45-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6e45-137">RELATED LINKS</span></span>
