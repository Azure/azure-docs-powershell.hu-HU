---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185075"
---
# <span data-ttu-id="bd595-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="bd595-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="bd595-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd595-102">SYNOPSIS</span></span>
<span data-ttu-id="bd595-103">Frissíti egy CosmosDB MongoDB-gyűjtemény átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="bd595-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="bd595-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd595-104">SYNTAX</span></span>

### <span data-ttu-id="bd595-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bd595-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd595-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd595-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd595-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd595-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd595-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd595-108">DESCRIPTION</span></span>
<span data-ttu-id="bd595-109">Frissíti egy CosmosDB MongoDB-gyűjtemény átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="bd595-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="bd595-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bd595-110">EXAMPLES</span></span>

### <span data-ttu-id="bd595-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bd595-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="bd595-112">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="bd595-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="bd595-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd595-113">PARAMETERS</span></span>

### <span data-ttu-id="bd595-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bd595-114">-AccountName</span></span>
<span data-ttu-id="bd595-115">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="bd595-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bd595-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="bd595-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="bd595-117">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="bd595-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="bd595-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bd595-118">-Confirm</span></span>
<span data-ttu-id="bd595-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bd595-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd595-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd595-120">-DatabaseName</span></span>
<span data-ttu-id="bd595-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="bd595-121">Database name.</span></span>

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

### <span data-ttu-id="bd595-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd595-122">-DefaultProfile</span></span>
<span data-ttu-id="bd595-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd595-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd595-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd595-124">-InputObject</span></span>
<span data-ttu-id="bd595-125">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="bd595-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="bd595-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd595-126">-Name</span></span>
<span data-ttu-id="bd595-127">Gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="bd595-127">Collection name.</span></span>

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

### <span data-ttu-id="bd595-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bd595-128">-ParentObject</span></span>
<span data-ttu-id="bd595-129">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="bd595-129">Mongo Database object.</span></span>

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

### <span data-ttu-id="bd595-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd595-130">-ResourceGroupName</span></span>
<span data-ttu-id="bd595-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bd595-131">Name of resource group.</span></span>

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

### <span data-ttu-id="bd595-132">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="bd595-132">-Throughput</span></span>
<span data-ttu-id="bd595-133">Az SQL-tároló (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="bd595-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="bd595-134">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="bd595-134">Default value is 400.</span></span>

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

### <span data-ttu-id="bd595-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd595-135">-WhatIf</span></span>
<span data-ttu-id="bd595-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bd595-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd595-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd595-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd595-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd595-138">CommonParameters</span></span>
<span data-ttu-id="bd595-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd595-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd595-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bd595-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd595-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd595-141">INPUTS</span></span>

### <span data-ttu-id="bd595-142">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="bd595-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="bd595-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd595-143">OUTPUTS</span></span>

### <span data-ttu-id="bd595-144">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bd595-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bd595-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd595-145">NOTES</span></span>

## <span data-ttu-id="bd595-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd595-146">RELATED LINKS</span></span>