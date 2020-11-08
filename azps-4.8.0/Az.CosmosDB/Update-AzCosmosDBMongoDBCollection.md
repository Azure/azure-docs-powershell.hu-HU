---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 9440e3541e5022ffbbe328ac81859d2ababa6209
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182862"
---
# <span data-ttu-id="d0acd-101">Update-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="d0acd-101">Update-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="d0acd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0acd-102">SYNOPSIS</span></span>
<span data-ttu-id="d0acd-103">Frissíti a CosmosDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="d0acd-103">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="d0acd-104">Ügyféloldali javítás műveletet hajt végre a meglévő gyűjtemény elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="d0acd-104">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="d0acd-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0acd-105">SYNTAX</span></span>

### <span data-ttu-id="d0acd-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0acd-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-Shard <String>]
 [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0acd-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0acd-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0acd-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0acd-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollection [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-Shard <String>] [-AnalyticalStorageTtl <Int32>] [-Index <PSMongoIndex[]>]
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0acd-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0acd-109">DESCRIPTION</span></span>
<span data-ttu-id="d0acd-110">Frissíti a CosmosDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="d0acd-110">Updates the CosmosDB MongoDB Collection.</span></span> <span data-ttu-id="d0acd-111">Ügyféloldali javítás műveletet hajt végre a meglévő gyűjtemény elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="d0acd-111">Performs a client side patch operation by reading the existing Collection.</span></span>

## <span data-ttu-id="d0acd-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d0acd-112">EXAMPLES</span></span>

### <span data-ttu-id="d0acd-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d0acd-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -DatabaseName myDatabaseName -Name myCollectionName -Index $index1,$index2

Name     : collection1
Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/mongodbDatabases/myDatabaseName/collect
           ions/myCollectionName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetPropertiesResource
```

## <span data-ttu-id="d0acd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0acd-114">PARAMETERS</span></span>

### <span data-ttu-id="d0acd-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d0acd-115">-AccountName</span></span>
<span data-ttu-id="d0acd-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d0acd-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d0acd-117">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="d0acd-117">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="d0acd-118">Az analitikai tárterület ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="d0acd-118">TTL for Analytical Storage.</span></span>

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

### <span data-ttu-id="d0acd-119">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d0acd-119">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d0acd-120">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="d0acd-120">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d0acd-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d0acd-121">-Confirm</span></span>
<span data-ttu-id="d0acd-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d0acd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0acd-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0acd-123">-DatabaseName</span></span>
<span data-ttu-id="d0acd-124">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d0acd-124">Database name.</span></span>

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

### <span data-ttu-id="d0acd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0acd-125">-DefaultProfile</span></span>
<span data-ttu-id="d0acd-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0acd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0acd-127">– Index</span><span class="sxs-lookup"><span data-stu-id="d0acd-127">-Index</span></span>
<span data-ttu-id="d0acd-128">PSMongoIndex-objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="d0acd-128">Array of PSMongoIndex objects.</span></span>

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

### <span data-ttu-id="d0acd-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0acd-129">-InputObject</span></span>
<span data-ttu-id="d0acd-130">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="d0acd-130">Sql Container object.</span></span>

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

### <span data-ttu-id="d0acd-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0acd-131">-Name</span></span>
<span data-ttu-id="d0acd-132">Gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="d0acd-132">Collection name.</span></span>

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

### <span data-ttu-id="d0acd-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d0acd-133">-ParentObject</span></span>
<span data-ttu-id="d0acd-134">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="d0acd-134">Mongo Database object.</span></span>

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

### <span data-ttu-id="d0acd-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0acd-135">-ResourceGroupName</span></span>
<span data-ttu-id="d0acd-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d0acd-136">Name of resource group.</span></span>

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

### <span data-ttu-id="d0acd-137">-Szilánk</span><span class="sxs-lookup"><span data-stu-id="d0acd-137">-Shard</span></span>
<span data-ttu-id="d0acd-138">A szilánkok kulcsának elérési útja.</span><span class="sxs-lookup"><span data-stu-id="d0acd-138">Sharding key path.</span></span>

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

### <span data-ttu-id="d0acd-139">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="d0acd-139">-Throughput</span></span>
<span data-ttu-id="d0acd-140">Az SQL-tároló (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="d0acd-140">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="d0acd-141">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="d0acd-141">Default value is 400.</span></span>

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

### <span data-ttu-id="d0acd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0acd-142">-WhatIf</span></span>
<span data-ttu-id="d0acd-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d0acd-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0acd-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0acd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0acd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0acd-145">CommonParameters</span></span>
<span data-ttu-id="d0acd-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0acd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0acd-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d0acd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0acd-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0acd-148">INPUTS</span></span>

### <span data-ttu-id="d0acd-149">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d0acd-149">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="d0acd-150">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="d0acd-150">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="d0acd-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0acd-151">OUTPUTS</span></span>

### <span data-ttu-id="d0acd-152">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="d0acd-152">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

### <span data-ttu-id="d0acd-153">Microsoft. Azure. Command. CosmosDB. kivétellel. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d0acd-153">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d0acd-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0acd-154">NOTES</span></span>

## <span data-ttu-id="d0acd-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0acd-155">RELATED LINKS</span></span>
