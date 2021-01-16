---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372370"
---
# <span data-ttu-id="bcb1d-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="bcb1d-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="bcb1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcb1d-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb1d-103">Frissíti aFrissítésekDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="bcb1d-104">Ügyféloldali javítást hajt végre a meglévő gyűjtemény elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="bcb1d-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bcb1d-105">SYNTAX</span></span>

### <span data-ttu-id="bcb1d-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bcb1d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcb1d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcb1d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcb1d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcb1d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcb1d-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bcb1d-109">DESCRIPTION</span></span>
<span data-ttu-id="bcb1d-110">Frissíti aFrissítésekDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="bcb1d-111">Ügyféloldali javítást hajt végre a meglévő gyűjtemény elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="bcb1d-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bcb1d-112">EXAMPLES</span></span>

### <span data-ttu-id="bcb1d-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="bcb1d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="bcb1d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcb1d-114">PARAMETERS</span></span>

### <span data-ttu-id="bcb1d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bcb1d-115">-AccountName</span></span>
<span data-ttu-id="bcb1d-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bcb1d-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="bcb1d-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="bcb1d-118">TTL analitikus tároláshoz.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="bcb1d-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="bcb1d-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="bcb1d-120">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="bcb1d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcb1d-121">-Confirm</span></span>
<span data-ttu-id="bcb1d-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcb1d-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bcb1d-123">-DatabaseName</span></span>
<span data-ttu-id="bcb1d-124">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-124">Database name.</span></span>

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

### <span data-ttu-id="bcb1d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb1d-125">-DefaultProfile</span></span>
<span data-ttu-id="bcb1d-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcb1d-127">-Index</span><span class="sxs-lookup"><span data-stu-id="bcb1d-127">-Index</span></span>
<span data-ttu-id="bcb1d-128">PSMongoIndex-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="bcb1d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcb1d-129">-InputObject</span></span>
<span data-ttu-id="bcb1d-130">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-130">Sql Container object.</span></span>

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

### <span data-ttu-id="bcb1d-131">-Name</span><span class="sxs-lookup"><span data-stu-id="bcb1d-131">-Name</span></span>
<span data-ttu-id="bcb1d-132">Gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-132">Collection name.</span></span>

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

### <span data-ttu-id="bcb1d-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bcb1d-133">-ParentObject</span></span>
<span data-ttu-id="bcb1d-134">Mongo Adatbázis objektum.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="bcb1d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb1d-135">-ResourceGroupName</span></span>
<span data-ttu-id="bcb1d-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-136">Name of resource group.</span></span>

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

### <span data-ttu-id="bcb1d-137">-Shard</span><span class="sxs-lookup"><span data-stu-id="bcb1d-137">-Shard</span></span>
<span data-ttu-id="bcb1d-138">Sharding key path.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-138">Sharding key path.</span></span>

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

### <span data-ttu-id="bcb1d-139">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="bcb1d-139">-Throughput</span></span>
<span data-ttu-id="bcb1d-140">Az SQL-tároló (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="bcb1d-141">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-141">Default value is 400.</span></span>

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

### <span data-ttu-id="bcb1d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcb1d-142">-WhatIf</span></span>
<span data-ttu-id="bcb1d-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcb1d-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcb1d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb1d-145">CommonParameters</span></span>
<span data-ttu-id="bcb1d-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb1d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb1d-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcb1d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb1d-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcb1d-148">INPUTS</span></span>

### <span data-ttu-id="bcb1d-149">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bcb1d-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="bcb1d-150">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="bcb1d-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="bcb1d-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcb1d-151">OUTPUTS</span></span>

### <span data-ttu-id="bcb1d-152">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="bcb1d-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="bcb1d-153">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="bcb1d-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="bcb1d-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bcb1d-154">NOTES</span></span>

## <span data-ttu-id="bcb1d-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcb1d-155">RELATED LINKS</span></span>
