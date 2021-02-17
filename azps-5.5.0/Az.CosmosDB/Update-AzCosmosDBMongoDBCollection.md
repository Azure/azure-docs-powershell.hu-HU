---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163986"
---
# <span data-ttu-id="7aa51-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="7aa51-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="7aa51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aa51-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa51-103">Frissíti aFrissítésekDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="7aa51-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="7aa51-104">Ügyféloldali javítást hajt végre a meglévő gyűjtemény elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="7aa51-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="7aa51-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7aa51-105">SYNTAX</span></span>

### <span data-ttu-id="7aa51-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7aa51-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aa51-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7aa51-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7aa51-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7aa51-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7aa51-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7aa51-109">DESCRIPTION</span></span>
<span data-ttu-id="7aa51-110">Frissíti aFrissítésekDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="7aa51-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="7aa51-111">Ügyféloldali javítást hajt végre a meglévő gyűjtemény elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="7aa51-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="7aa51-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7aa51-112">EXAMPLES</span></span>

### <span data-ttu-id="7aa51-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="7aa51-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="7aa51-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7aa51-114">PARAMETERS</span></span>

### <span data-ttu-id="7aa51-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7aa51-115">-AccountName</span></span>
<span data-ttu-id="7aa51-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="7aa51-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7aa51-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="7aa51-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="7aa51-118">TTL analitikus tároláshoz.</span><span class="sxs-lookup"><span data-stu-id="7aa51-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="7aa51-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7aa51-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7aa51-120">Maximális átviteli sebesség, ha engedélyezve van az automatikus méretezés.</span><span class="sxs-lookup"><span data-stu-id="7aa51-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7aa51-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7aa51-121">-Confirm</span></span>
<span data-ttu-id="7aa51-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7aa51-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aa51-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7aa51-123">-DatabaseName</span></span>
<span data-ttu-id="7aa51-124">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7aa51-124">Database name.</span></span>

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

### <span data-ttu-id="7aa51-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa51-125">-DefaultProfile</span></span>
<span data-ttu-id="7aa51-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7aa51-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7aa51-127">-Index</span><span class="sxs-lookup"><span data-stu-id="7aa51-127">-Index</span></span>
<span data-ttu-id="7aa51-128">PSMongoIndex-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="7aa51-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="7aa51-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7aa51-129">-InputObject</span></span>
<span data-ttu-id="7aa51-130">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="7aa51-130">Sql Container object.</span></span>

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

### <span data-ttu-id="7aa51-131">-Name</span><span class="sxs-lookup"><span data-stu-id="7aa51-131">-Name</span></span>
<span data-ttu-id="7aa51-132">Gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="7aa51-132">Collection name.</span></span>

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

### <span data-ttu-id="7aa51-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7aa51-133">-ParentObject</span></span>
<span data-ttu-id="7aa51-134">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="7aa51-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="7aa51-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aa51-135">-ResourceGroupName</span></span>
<span data-ttu-id="7aa51-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7aa51-136">Name of resource group.</span></span>

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

### <span data-ttu-id="7aa51-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="7aa51-137">-Shard</span></span>
<span data-ttu-id="7aa51-138">Sharding key path.</span><span class="sxs-lookup"><span data-stu-id="7aa51-138">Sharding key path.</span></span>

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

### <span data-ttu-id="7aa51-139">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="7aa51-139">-Throughput</span></span>
<span data-ttu-id="7aa51-140">Az SQL-tároló (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="7aa51-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="7aa51-141">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="7aa51-141">Default value is 400.</span></span>

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

### <span data-ttu-id="7aa51-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aa51-142">-WhatIf</span></span>
<span data-ttu-id="7aa51-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7aa51-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aa51-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7aa51-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aa51-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa51-145">CommonParameters</span></span>
<span data-ttu-id="7aa51-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aa51-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa51-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7aa51-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa51-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7aa51-148">INPUTS</span></span>

### <span data-ttu-id="7aa51-149">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7aa51-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="7aa51-150">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="7aa51-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="7aa51-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aa51-151">OUTPUTS</span></span>

### <span data-ttu-id="7aa51-152">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="7aa51-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="7aa51-153">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="7aa51-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="7aa51-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7aa51-154">NOTES</span></span>

## <span data-ttu-id="7aa51-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7aa51-155">RELATED LINKS</span></span>
