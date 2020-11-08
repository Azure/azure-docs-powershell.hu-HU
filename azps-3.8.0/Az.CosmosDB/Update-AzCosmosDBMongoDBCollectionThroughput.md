---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 605998d6bc5ae8b647b3644dc71b8063f0881910
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012184"
---
# <span data-ttu-id="86238-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="86238-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="86238-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86238-102">SYNOPSIS</span></span>
<span data-ttu-id="86238-103">Frissíti egy CosmosDB MongoDB-gyűjtemény átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="86238-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="86238-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86238-104">SYNTAX</span></span>

### <span data-ttu-id="86238-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86238-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86238-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86238-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86238-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86238-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBCollectionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86238-108">Példák</span><span class="sxs-lookup"><span data-stu-id="86238-108">EXAMPLES</span></span>

### <span data-ttu-id="86238-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="86238-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="86238-110">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="86238-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="86238-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86238-111">PARAMETERS</span></span>

### <span data-ttu-id="86238-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="86238-112">-AccountName</span></span>
<span data-ttu-id="86238-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="86238-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="86238-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86238-114">-Confirm</span></span>
<span data-ttu-id="86238-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86238-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86238-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86238-116">-DatabaseName</span></span>
<span data-ttu-id="86238-117">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="86238-117">Database name.</span></span>

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

### <span data-ttu-id="86238-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86238-118">-DefaultProfile</span></span>
<span data-ttu-id="86238-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86238-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86238-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86238-120">-InputObject</span></span>
<span data-ttu-id="86238-121">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="86238-121">Mongo Database object.</span></span>

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

### <span data-ttu-id="86238-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="86238-122">-Name</span></span>
<span data-ttu-id="86238-123">Gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="86238-123">Collection name.</span></span>

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

### <span data-ttu-id="86238-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="86238-124">-ParentObject</span></span>
<span data-ttu-id="86238-125">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="86238-125">Mongo Database object.</span></span>

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

### <span data-ttu-id="86238-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86238-126">-ResourceGroupName</span></span>
<span data-ttu-id="86238-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="86238-127">Name of resource group.</span></span>

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

### <span data-ttu-id="86238-128">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="86238-128">-Throughput</span></span>
<span data-ttu-id="86238-129">Az SQL-tároló (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="86238-129">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="86238-130">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="86238-130">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86238-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86238-131">-WhatIf</span></span>
<span data-ttu-id="86238-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86238-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86238-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86238-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86238-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86238-134">CommonParameters</span></span>
<span data-ttu-id="86238-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86238-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86238-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="86238-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86238-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86238-137">INPUTS</span></span>

### <span data-ttu-id="86238-138">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="86238-138">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="86238-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86238-139">OUTPUTS</span></span>

### <span data-ttu-id="86238-140">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="86238-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="86238-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86238-141">NOTES</span></span>

## <span data-ttu-id="86238-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86238-142">RELATED LINKS</span></span>
