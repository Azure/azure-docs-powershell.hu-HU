---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 8c27df120b17805a72e7ed50497448a8f3f58461
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009190"
---
# <span data-ttu-id="06209-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="06209-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="06209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06209-102">SYNOPSIS</span></span>
<span data-ttu-id="06209-103">Beveszi a MongoDB Collection 20165-et, és beveszi a 2016-os MongoDB-gyűjtemény Átviteli sebesség tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="06209-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="06209-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="06209-104">SYNTAX</span></span>

### <span data-ttu-id="06209-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06209-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06209-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06209-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06209-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="06209-107">DESCRIPTION</span></span>
<span data-ttu-id="06209-108">A **Get-AzCosmosDBMongoDBCollectionThroughput** parancsmag a MongoDB Collection átviteli tulajdonságokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="06209-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="06209-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="06209-109">EXAMPLES</span></span>

### <span data-ttu-id="06209-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="06209-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="06209-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06209-111">PARAMETERS</span></span>

### <span data-ttu-id="06209-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="06209-112">-AccountName</span></span>
<span data-ttu-id="06209-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="06209-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="06209-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06209-114">-Confirm</span></span>
<span data-ttu-id="06209-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="06209-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06209-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06209-116">-DatabaseName</span></span>
<span data-ttu-id="06209-117">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="06209-117">Database name.</span></span>

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

### <span data-ttu-id="06209-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06209-118">-DefaultProfile</span></span>
<span data-ttu-id="06209-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06209-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06209-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06209-120">-InputObject</span></span>
<span data-ttu-id="06209-121">Ha ezt adja meg, akkor a parancsmag a megfelelő átviteli sebességet adja vissza a gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="06209-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="06209-122">-Name</span><span class="sxs-lookup"><span data-stu-id="06209-122">-Name</span></span>
<span data-ttu-id="06209-123">Gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="06209-123">Collection name.</span></span>

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

### <span data-ttu-id="06209-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06209-124">-ResourceGroupName</span></span>
<span data-ttu-id="06209-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="06209-125">Name of resource group.</span></span>

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

### <span data-ttu-id="06209-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06209-126">-WhatIf</span></span>
<span data-ttu-id="06209-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="06209-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06209-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06209-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06209-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06209-129">CommonParameters</span></span>
<span data-ttu-id="06209-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06209-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06209-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06209-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06209-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06209-132">INPUTS</span></span>

### <span data-ttu-id="06209-133">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="06209-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="06209-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06209-134">OUTPUTS</span></span>

### <span data-ttu-id="06209-135">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="06209-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="06209-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="06209-136">NOTES</span></span>

## <span data-ttu-id="06209-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06209-137">RELATED LINKS</span></span>
