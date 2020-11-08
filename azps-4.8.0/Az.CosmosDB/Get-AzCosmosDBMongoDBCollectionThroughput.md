---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182393"
---
# <span data-ttu-id="ad190-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="ad190-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="ad190-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad190-102">SYNOPSIS</span></span>
<span data-ttu-id="ad190-103">Beolvassa a MongoDB-gyűjtemény CosmosDB-átviteli tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="ad190-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="ad190-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad190-104">SYNTAX</span></span>

### <span data-ttu-id="ad190-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad190-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad190-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad190-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad190-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad190-107">DESCRIPTION</span></span>
<span data-ttu-id="ad190-108">A **Get-AzCosmosDBMongoDBCollectionThroughput** parancsmag az MongoDB-gyűjtemény átviteli tulajdonságait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ad190-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="ad190-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ad190-109">EXAMPLES</span></span>

### <span data-ttu-id="ad190-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad190-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="ad190-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad190-111">PARAMETERS</span></span>

### <span data-ttu-id="ad190-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ad190-112">-AccountName</span></span>
<span data-ttu-id="ad190-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ad190-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ad190-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad190-114">-Confirm</span></span>
<span data-ttu-id="ad190-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad190-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad190-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ad190-116">-DatabaseName</span></span>
<span data-ttu-id="ad190-117">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ad190-117">Database name.</span></span>

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

### <span data-ttu-id="ad190-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad190-118">-DefaultProfile</span></span>
<span data-ttu-id="ad190-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad190-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad190-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad190-120">-InputObject</span></span>
<span data-ttu-id="ad190-121">Ha meg van határozva, akkor a parancsmag a megfelelő átviteli értékkel rendelkező gyűjteményt adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ad190-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad190-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad190-122">-Name</span></span>
<span data-ttu-id="ad190-123">Gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="ad190-123">Collection name.</span></span>

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

### <span data-ttu-id="ad190-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad190-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad190-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ad190-125">Name of resource group.</span></span>

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

### <span data-ttu-id="ad190-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad190-126">-WhatIf</span></span>
<span data-ttu-id="ad190-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad190-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad190-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad190-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad190-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad190-129">CommonParameters</span></span>
<span data-ttu-id="ad190-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad190-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad190-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad190-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad190-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad190-132">INPUTS</span></span>

### <span data-ttu-id="ad190-133">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="ad190-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="ad190-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad190-134">OUTPUTS</span></span>

### <span data-ttu-id="ad190-135">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ad190-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ad190-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad190-136">NOTES</span></span>

## <span data-ttu-id="ad190-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad190-137">RELATED LINKS</span></span>
