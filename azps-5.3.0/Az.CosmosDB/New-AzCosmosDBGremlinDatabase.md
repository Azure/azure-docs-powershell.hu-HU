---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 535d6aa9f2ea6538e6b00f1334ce1114fad89f81
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477457"
---
# <span data-ttu-id="2815c-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="2815c-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="2815c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2815c-102">SYNOPSIS</span></span>
<span data-ttu-id="2815c-103">Létrehoz egy új TárolóDB Gremlin-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="2815c-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="2815c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2815c-104">SYNTAX</span></span>

### <span data-ttu-id="2815c-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2815c-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2815c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2815c-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2815c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2815c-107">DESCRIPTION</span></span>
<span data-ttu-id="2815c-108">Létrehoz egy új TárolóDB Gremlin-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="2815c-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="2815c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2815c-109">EXAMPLES</span></span>

### <span data-ttu-id="2815c-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="2815c-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="2815c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2815c-111">PARAMETERS</span></span>

### <span data-ttu-id="2815c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2815c-112">-AccountName</span></span>
<span data-ttu-id="2815c-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="2815c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2815c-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="2815c-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="2815c-115">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="2815c-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="2815c-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2815c-116">-Confirm</span></span>
<span data-ttu-id="2815c-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2815c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2815c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2815c-118">-DefaultProfile</span></span>
<span data-ttu-id="2815c-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2815c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2815c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2815c-120">-Name</span></span>
<span data-ttu-id="2815c-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="2815c-121">Database name.</span></span>

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

### <span data-ttu-id="2815c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2815c-122">-ParentObject</span></span>
<span data-ttu-id="2815c-123">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="2815c-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2815c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2815c-124">-ResourceGroupName</span></span>
<span data-ttu-id="2815c-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2815c-125">Name of resource group.</span></span>

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

### <span data-ttu-id="2815c-126">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="2815c-126">-Throughput</span></span>
<span data-ttu-id="2815c-127">A Gremlin-adatbázis (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="2815c-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="2815c-128">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="2815c-128">Default value is 400.</span></span>

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

### <span data-ttu-id="2815c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2815c-129">-WhatIf</span></span>
<span data-ttu-id="2815c-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2815c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2815c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2815c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2815c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2815c-132">CommonParameters</span></span>
<span data-ttu-id="2815c-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2815c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2815c-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2815c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2815c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2815c-135">INPUTS</span></span>

### <span data-ttu-id="2815c-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2815c-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="2815c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2815c-137">OUTPUTS</span></span>

### <span data-ttu-id="2815c-138">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2815c-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="2815c-139">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="2815c-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="2815c-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2815c-140">NOTES</span></span>

## <span data-ttu-id="2815c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2815c-141">RELATED LINKS</span></span>
