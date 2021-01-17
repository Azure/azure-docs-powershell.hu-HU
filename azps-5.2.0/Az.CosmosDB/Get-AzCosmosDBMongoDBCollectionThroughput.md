---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 0b6b24b0e8c759ca4263d46cf9fe922cd27829e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332670"
---
# <span data-ttu-id="851ea-101">Get-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="851ea-101">Get-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="851ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="851ea-102">SYNOPSIS</span></span>
<span data-ttu-id="851ea-103">A MongoDB Gyűjtemény 2010-es átviteli sebességtulajdonságát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="851ea-103">Gets the CosmosDB throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="851ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="851ea-104">SYNTAX</span></span>

### <span data-ttu-id="851ea-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="851ea-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="851ea-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="851ea-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="851ea-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="851ea-107">DESCRIPTION</span></span>
<span data-ttu-id="851ea-108">A **Get-AzCosmosDBMongoDBCollectionThroughput** parancsmag a MongoDB Collection átviteli tulajdonságokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="851ea-108">The **Get-AzCosmosDBMongoDBCollectionThroughput** cmdlet gets the throughput properties of MongoDB Collection.</span></span>

## <span data-ttu-id="851ea-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="851ea-109">EXAMPLES</span></span>

### <span data-ttu-id="851ea-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="851ea-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBCollectionThroughput -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {databaseName} -Name {collectionName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="851ea-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="851ea-111">PARAMETERS</span></span>

### <span data-ttu-id="851ea-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="851ea-112">-AccountName</span></span>
<span data-ttu-id="851ea-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="851ea-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="851ea-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="851ea-114">-Confirm</span></span>
<span data-ttu-id="851ea-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="851ea-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="851ea-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="851ea-116">-DatabaseName</span></span>
<span data-ttu-id="851ea-117">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="851ea-117">Database name.</span></span>

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

### <span data-ttu-id="851ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="851ea-118">-DefaultProfile</span></span>
<span data-ttu-id="851ea-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="851ea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="851ea-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="851ea-120">-InputObject</span></span>
<span data-ttu-id="851ea-121">Ha ezt adja meg, akkor a parancsmag a megfelelő átviteli sebességet adja vissza a gyűjteményben.</span><span class="sxs-lookup"><span data-stu-id="851ea-121">If provided then, the cmdlet returns the collection with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="851ea-122">-Name</span><span class="sxs-lookup"><span data-stu-id="851ea-122">-Name</span></span>
<span data-ttu-id="851ea-123">Gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="851ea-123">Collection name.</span></span>

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

### <span data-ttu-id="851ea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="851ea-124">-ResourceGroupName</span></span>
<span data-ttu-id="851ea-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="851ea-125">Name of resource group.</span></span>

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

### <span data-ttu-id="851ea-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="851ea-126">-WhatIf</span></span>
<span data-ttu-id="851ea-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="851ea-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="851ea-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="851ea-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="851ea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="851ea-129">CommonParameters</span></span>
<span data-ttu-id="851ea-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="851ea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="851ea-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="851ea-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="851ea-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="851ea-132">INPUTS</span></span>

### <span data-ttu-id="851ea-133">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="851ea-133">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="851ea-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="851ea-134">OUTPUTS</span></span>

### <span data-ttu-id="851ea-135">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="851ea-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="851ea-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="851ea-136">NOTES</span></span>

## <span data-ttu-id="851ea-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="851ea-137">RELATED LINKS</span></span>
