---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: b65443b2fc8d8b97b4b0598e0bfbb3afb9d1b925
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943066"
---
# <span data-ttu-id="b6379-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="b6379-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="b6379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6379-102">SYNOPSIS</span></span>
<span data-ttu-id="b6379-103">Létrehoz egy új TárolóDB Gremlin-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="b6379-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="b6379-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b6379-104">SYNTAX</span></span>

### <span data-ttu-id="b6379-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6379-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6379-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6379-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6379-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b6379-107">DESCRIPTION</span></span>
<span data-ttu-id="b6379-108">Létrehoz egy új TárolóDB Gremlin-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="b6379-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="b6379-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b6379-109">EXAMPLES</span></span>

### <span data-ttu-id="b6379-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b6379-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="b6379-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6379-111">PARAMETERS</span></span>

### <span data-ttu-id="b6379-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6379-112">-AccountName</span></span>
<span data-ttu-id="b6379-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="b6379-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b6379-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b6379-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b6379-115">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="b6379-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b6379-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6379-116">-Confirm</span></span>
<span data-ttu-id="b6379-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b6379-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6379-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6379-118">-DefaultProfile</span></span>
<span data-ttu-id="b6379-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6379-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6379-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b6379-120">-Name</span></span>
<span data-ttu-id="b6379-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b6379-121">Database name.</span></span>

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

### <span data-ttu-id="b6379-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b6379-122">-ParentObject</span></span>
<span data-ttu-id="b6379-123">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="b6379-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b6379-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6379-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6379-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b6379-125">Name of resource group.</span></span>

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

### <span data-ttu-id="b6379-126">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="b6379-126">-Throughput</span></span>
<span data-ttu-id="b6379-127">A Gremlin-adatbázis (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="b6379-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="b6379-128">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="b6379-128">Default value is 400.</span></span>

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

### <span data-ttu-id="b6379-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6379-129">-WhatIf</span></span>
<span data-ttu-id="b6379-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b6379-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6379-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6379-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6379-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6379-132">CommonParameters</span></span>
<span data-ttu-id="b6379-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6379-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6379-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6379-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6379-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6379-135">INPUTS</span></span>

### <span data-ttu-id="b6379-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b6379-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b6379-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6379-137">OUTPUTS</span></span>

### <span data-ttu-id="b6379-138">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b6379-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="b6379-139">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="b6379-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="b6379-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b6379-140">NOTES</span></span>

## <span data-ttu-id="b6379-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6379-141">RELATED LINKS</span></span>
