---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 2458c31ba75470c5d2b5bb2b73d817eb58c5bc61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931266"
---
# <span data-ttu-id="552d3-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="552d3-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="552d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="552d3-102">SYNOPSIS</span></span>
<span data-ttu-id="552d3-103">Frissíti aFrissítésekDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="552d3-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="552d3-104">Ügyféloldali javítást hajt végre a meglévő Gyűjtemény elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="552d3-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="552d3-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="552d3-105">SYNTAX</span></span>

### <span data-ttu-id="552d3-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="552d3-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="552d3-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="552d3-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="552d3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="552d3-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="552d3-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="552d3-109">DESCRIPTION</span></span>
<span data-ttu-id="552d3-110">Frissíti aFrissítésekDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="552d3-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="552d3-111">Ügyféloldali javítást hajt végre a meglévő Gyűjtemény elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="552d3-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="552d3-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="552d3-112">EXAMPLES</span></span>

### <span data-ttu-id="552d3-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="552d3-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="552d3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="552d3-114">PARAMETERS</span></span>

### <span data-ttu-id="552d3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="552d3-115">-AccountName</span></span>
<span data-ttu-id="552d3-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="552d3-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="552d3-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="552d3-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="552d3-118">TTL analitikus tároláshoz.</span><span class="sxs-lookup"><span data-stu-id="552d3-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="552d3-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="552d3-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="552d3-120">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="552d3-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="552d3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="552d3-121">-Confirm</span></span>
<span data-ttu-id="552d3-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="552d3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="552d3-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="552d3-123">-DatabaseName</span></span>
<span data-ttu-id="552d3-124">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="552d3-124">Database name.</span></span>

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

### <span data-ttu-id="552d3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="552d3-125">-DefaultProfile</span></span>
<span data-ttu-id="552d3-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="552d3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="552d3-127">-Index</span><span class="sxs-lookup"><span data-stu-id="552d3-127">-Index</span></span>
<span data-ttu-id="552d3-128">PSMongoIndex-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="552d3-128">Array of PSMongoIndex objects.</span></span>

```yaml
Type: PSMongoIndex[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="552d3-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="552d3-129">-InputObject</span></span>
<span data-ttu-id="552d3-130">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="552d3-130">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="552d3-131">-Name</span><span class="sxs-lookup"><span data-stu-id="552d3-131">-Name</span></span>
<span data-ttu-id="552d3-132">Gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="552d3-132">Collection name.</span></span>

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

### <span data-ttu-id="552d3-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="552d3-133">-ParentObject</span></span>
<span data-ttu-id="552d3-134">Mongo Adatbázis objektum.</span><span class="sxs-lookup"><span data-stu-id="552d3-134">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="552d3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="552d3-135">-ResourceGroupName</span></span>
<span data-ttu-id="552d3-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="552d3-136">Name of resource group.</span></span>

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

### <span data-ttu-id="552d3-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="552d3-137">-Shard</span></span>
<span data-ttu-id="552d3-138">Sharding key path.</span><span class="sxs-lookup"><span data-stu-id="552d3-138">Sharding key path.</span></span>

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

### <span data-ttu-id="552d3-139">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="552d3-139">-Throughput</span></span>
<span data-ttu-id="552d3-140">Az SQL-tároló (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="552d3-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="552d3-141">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="552d3-141">Default value is 400.</span></span>

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

### <span data-ttu-id="552d3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="552d3-142">-WhatIf</span></span>
<span data-ttu-id="552d3-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="552d3-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="552d3-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="552d3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="552d3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="552d3-145">CommonParameters</span></span>
<span data-ttu-id="552d3-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="552d3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="552d3-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="552d3-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="552d3-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="552d3-148">INPUTS</span></span>

### <span data-ttu-id="552d3-149">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="552d3-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="552d3-150">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="552d3-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="552d3-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="552d3-151">OUTPUTS</span></span>

### <span data-ttu-id="552d3-152">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="552d3-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="552d3-153">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="552d3-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="552d3-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="552d3-154">NOTES</span></span>

## <span data-ttu-id="552d3-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="552d3-155">RELATED LINKS</span></span>
