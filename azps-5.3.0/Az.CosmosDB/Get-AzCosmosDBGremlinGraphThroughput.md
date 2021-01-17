---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraphthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraphThroughput.md
ms.openlocfilehash: 1c29b8fd4f81f67b5eaae9de06d055e5e1a2dace
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477521"
---
# <span data-ttu-id="3521b-101">Get-AzCosmosDBGremlinGraphThroughput</span><span class="sxs-lookup"><span data-stu-id="3521b-101">Get-AzCosmosDBGremlinGraphThroughput</span></span>

## <span data-ttu-id="3521b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3521b-102">SYNOPSIS</span></span>
<span data-ttu-id="3521b-103">A 2016-os Gremlin Graph-diagram átviteli sebességét kapja.</span><span class="sxs-lookup"><span data-stu-id="3521b-103">Gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="3521b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3521b-104">SYNTAX</span></span>

### <span data-ttu-id="3521b-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3521b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3521b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3521b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraphThroughput [-Name <String>] -InputObject <PSGremlinGraphGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3521b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3521b-107">DESCRIPTION</span></span>
<span data-ttu-id="3521b-108">A **Get-AzCosmosDBGremlinGraphThroughput** parancsmag kapja meg a sebességet a Fogdb Gremlin Graph-ban.</span><span class="sxs-lookup"><span data-stu-id="3521b-108">The **Get-AzCosmosDBGremlinGraphThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="3521b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3521b-109">EXAMPLES</span></span>

### <span data-ttu-id="3521b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="3521b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraphThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="3521b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3521b-111">PARAMETERS</span></span>

### <span data-ttu-id="3521b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3521b-112">-AccountName</span></span>
<span data-ttu-id="3521b-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="3521b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3521b-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3521b-114">-Confirm</span></span>
<span data-ttu-id="3521b-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3521b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3521b-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3521b-116">-DatabaseName</span></span>
<span data-ttu-id="3521b-117">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3521b-117">Database name.</span></span>

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

### <span data-ttu-id="3521b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3521b-118">-DefaultProfile</span></span>
<span data-ttu-id="3521b-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3521b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3521b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3521b-120">-InputObject</span></span>
<span data-ttu-id="3521b-121">Gremlin Graph-objektum.</span><span class="sxs-lookup"><span data-stu-id="3521b-121">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="3521b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3521b-122">-Name</span></span>
<span data-ttu-id="3521b-123">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="3521b-123">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="3521b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3521b-124">-ResourceGroupName</span></span>
<span data-ttu-id="3521b-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3521b-125">Name of resource group.</span></span>

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

### <span data-ttu-id="3521b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3521b-126">-WhatIf</span></span>
<span data-ttu-id="3521b-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3521b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3521b-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3521b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3521b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3521b-129">CommonParameters</span></span>
<span data-ttu-id="3521b-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3521b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3521b-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3521b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3521b-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3521b-132">INPUTS</span></span>

### <span data-ttu-id="3521b-133">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="3521b-133">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="3521b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3521b-134">OUTPUTS</span></span>

### <span data-ttu-id="3521b-135">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3521b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3521b-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3521b-136">NOTES</span></span>

## <span data-ttu-id="3521b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3521b-137">RELATED LINKS</span></span>
