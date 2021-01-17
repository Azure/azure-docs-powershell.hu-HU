---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323662"
---
# <span data-ttu-id="3fefe-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="3fefe-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="3fefe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fefe-102">SYNOPSIS</span></span>
<span data-ttu-id="3fefe-103">Frissíti aFrissítésekDB Gremlin adatbázist.</span><span class="sxs-lookup"><span data-stu-id="3fefe-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="3fefe-104">Ügyféloldali javítást hajt végre a meglévő adatbázis olvasásával.</span><span class="sxs-lookup"><span data-stu-id="3fefe-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="3fefe-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3fefe-105">SYNTAX</span></span>

### <span data-ttu-id="3fefe-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3fefe-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fefe-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fefe-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fefe-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fefe-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3fefe-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3fefe-109">DESCRIPTION</span></span>
<span data-ttu-id="3fefe-110">Frissíti aFrissítésekDB Gremlin adatbázist.</span><span class="sxs-lookup"><span data-stu-id="3fefe-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="3fefe-111">Ügyféloldali javítást hajt végre a meglévő adatbázis olvasásával.</span><span class="sxs-lookup"><span data-stu-id="3fefe-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="3fefe-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3fefe-112">EXAMPLES</span></span>

### <span data-ttu-id="3fefe-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="3fefe-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="3fefe-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fefe-114">PARAMETERS</span></span>

### <span data-ttu-id="3fefe-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3fefe-115">-AccountName</span></span>
<span data-ttu-id="3fefe-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="3fefe-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3fefe-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="3fefe-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="3fefe-118">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="3fefe-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="3fefe-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fefe-119">-Confirm</span></span>
<span data-ttu-id="3fefe-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3fefe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fefe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fefe-121">-DefaultProfile</span></span>
<span data-ttu-id="3fefe-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3fefe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fefe-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fefe-123">-InputObject</span></span>
<span data-ttu-id="3fefe-124">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="3fefe-124">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fefe-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3fefe-125">-Name</span></span>
<span data-ttu-id="3fefe-126">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3fefe-126">Database name.</span></span>

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

### <span data-ttu-id="3fefe-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3fefe-127">-ParentObject</span></span>
<span data-ttu-id="3fefe-128">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="3fefe-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="3fefe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fefe-129">-ResourceGroupName</span></span>
<span data-ttu-id="3fefe-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3fefe-130">Name of resource group.</span></span>

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

### <span data-ttu-id="3fefe-131">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="3fefe-131">-Throughput</span></span>
<span data-ttu-id="3fefe-132">A Gremlin-adatbázis (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="3fefe-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="3fefe-133">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="3fefe-133">Default value is 400.</span></span>

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

### <span data-ttu-id="3fefe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fefe-134">-WhatIf</span></span>
<span data-ttu-id="3fefe-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3fefe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fefe-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3fefe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fefe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fefe-137">CommonParameters</span></span>
<span data-ttu-id="3fefe-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fefe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fefe-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fefe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fefe-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3fefe-140">INPUTS</span></span>

### <span data-ttu-id="3fefe-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="3fefe-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="3fefe-142">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3fefe-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="3fefe-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fefe-143">OUTPUTS</span></span>

### <span data-ttu-id="3fefe-144">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3fefe-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="3fefe-145">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="3fefe-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="3fefe-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3fefe-146">NOTES</span></span>

## <span data-ttu-id="3fefe-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3fefe-147">RELATED LINKS</span></span>
