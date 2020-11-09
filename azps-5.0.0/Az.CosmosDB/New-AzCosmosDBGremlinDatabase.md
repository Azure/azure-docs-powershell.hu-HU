---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 535d6aa9f2ea6538e6b00f1334ce1114fad89f81
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299348"
---
# <span data-ttu-id="daadb-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="daadb-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="daadb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="daadb-102">SYNOPSIS</span></span>
<span data-ttu-id="daadb-103">Új CosmosDB-Gremlin adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="daadb-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="daadb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="daadb-104">SYNTAX</span></span>

### <span data-ttu-id="daadb-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="daadb-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daadb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="daadb-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="daadb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="daadb-107">DESCRIPTION</span></span>
<span data-ttu-id="daadb-108">Új CosmosDB-Gremlin adatbázist hoz létre.</span><span class="sxs-lookup"><span data-stu-id="daadb-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="daadb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="daadb-109">EXAMPLES</span></span>

### <span data-ttu-id="daadb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="daadb-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="daadb-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="daadb-111">PARAMETERS</span></span>

### <span data-ttu-id="daadb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="daadb-112">-AccountName</span></span>
<span data-ttu-id="daadb-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="daadb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="daadb-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="daadb-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="daadb-115">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="daadb-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="daadb-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="daadb-116">-Confirm</span></span>
<span data-ttu-id="daadb-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="daadb-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daadb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daadb-118">-DefaultProfile</span></span>
<span data-ttu-id="daadb-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="daadb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daadb-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="daadb-120">-Name</span></span>
<span data-ttu-id="daadb-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="daadb-121">Database name.</span></span>

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

### <span data-ttu-id="daadb-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="daadb-122">-ParentObject</span></span>
<span data-ttu-id="daadb-123">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="daadb-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="daadb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daadb-124">-ResourceGroupName</span></span>
<span data-ttu-id="daadb-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="daadb-125">Name of resource group.</span></span>

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

### <span data-ttu-id="daadb-126">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="daadb-126">-Throughput</span></span>
<span data-ttu-id="daadb-127">Az Gremlin-adatbázis (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="daadb-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="daadb-128">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="daadb-128">Default value is 400.</span></span>

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

### <span data-ttu-id="daadb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daadb-129">-WhatIf</span></span>
<span data-ttu-id="daadb-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="daadb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daadb-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="daadb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daadb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daadb-132">CommonParameters</span></span>
<span data-ttu-id="daadb-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="daadb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daadb-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="daadb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daadb-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="daadb-135">INPUTS</span></span>

### <span data-ttu-id="daadb-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="daadb-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="daadb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="daadb-137">OUTPUTS</span></span>

### <span data-ttu-id="daadb-138">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="daadb-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="daadb-139">Microsoft. Azure. Command. CosmosDB. kivétellel. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="daadb-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="daadb-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="daadb-140">NOTES</span></span>

## <span data-ttu-id="daadb-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="daadb-141">RELATED LINKS</span></span>
