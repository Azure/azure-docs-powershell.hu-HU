---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbcollectionthroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBCollectionThroughputMigration.md
ms.openlocfilehash: e2f1449536f9b4db5b743c1a1e352e427ae86821
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299432"
---
# <span data-ttu-id="75fa6-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="75fa6-101">Invoke-AzCosmosDBMongoDBCollectionThroughputMigration</span></span>

## <span data-ttu-id="75fa6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="75fa6-103">Ezzel a beállítással áttelepítheti az automatikus méretezést a manuális átviteli sebességre, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="75fa6-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="75fa6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75fa6-104">SYNTAX</span></span>

### <span data-ttu-id="75fa6-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75fa6-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75fa6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75fa6-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -ParentObject <PSMongoDBDatabaseGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75fa6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75fa6-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBCollectionThroughputMigration [-Name <String>]
 -InputObject <PSMongoDBCollectionGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75fa6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="75fa6-108">DESCRIPTION</span></span>
<span data-ttu-id="75fa6-109">A ThroughpyteType paraméter határozza meg, hogy milyen átviteli sebességet szeretne áttelepíteni.</span><span class="sxs-lookup"><span data-stu-id="75fa6-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="75fa6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="75fa6-110">EXAMPLES</span></span>

### <span data-ttu-id="75fa6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="75fa6-111">Example 1</span></span>
```powershell
PS C:\> $NewCollection =  New-AzCosmosDBMongoDBCollection -AccountName myAccountName -ResourceGroupName myRgName -Name myCollectionName -Throughput  700 -DatabaseName myDbName
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBCollectionThroughputMigration -InputObject $NewCollection -ThroughputType Autoscale
```


## <span data-ttu-id="75fa6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75fa6-112">PARAMETERS</span></span>

### <span data-ttu-id="75fa6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75fa6-113">-AccountName</span></span>
<span data-ttu-id="75fa6-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="75fa6-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="75fa6-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="75fa6-115">-Confirm</span></span>
<span data-ttu-id="75fa6-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="75fa6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75fa6-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75fa6-117">-DatabaseName</span></span>
<span data-ttu-id="75fa6-118">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="75fa6-118">Database name.</span></span>

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

### <span data-ttu-id="75fa6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75fa6-119">-DefaultProfile</span></span>
<span data-ttu-id="75fa6-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75fa6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75fa6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75fa6-121">-InputObject</span></span>
<span data-ttu-id="75fa6-122">Mongo gyűjtemény objektuma.</span><span class="sxs-lookup"><span data-stu-id="75fa6-122">Mongo Collection object.</span></span>

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

### <span data-ttu-id="75fa6-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75fa6-123">-Name</span></span>
<span data-ttu-id="75fa6-124">Gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="75fa6-124">Collection name.</span></span>

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

### <span data-ttu-id="75fa6-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="75fa6-125">-ParentObject</span></span>
<span data-ttu-id="75fa6-126">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="75fa6-126">Mongo Database object.</span></span>

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

### <span data-ttu-id="75fa6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75fa6-127">-ResourceGroupName</span></span>
<span data-ttu-id="75fa6-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="75fa6-128">Name of resource group.</span></span>

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

### <span data-ttu-id="75fa6-129">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="75fa6-129">-ThroughputType</span></span>
<span data-ttu-id="75fa6-130">Az áttelepítéshez használandó átviteli típus.</span><span class="sxs-lookup"><span data-stu-id="75fa6-130">Throughput type to migrate to.</span></span>
<span data-ttu-id="75fa6-131">Lehetséges értékek: automatikus méretezés, kézi.</span><span class="sxs-lookup"><span data-stu-id="75fa6-131">Possible values are: Autoscale, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75fa6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75fa6-132">-WhatIf</span></span>
<span data-ttu-id="75fa6-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="75fa6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75fa6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75fa6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75fa6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75fa6-135">CommonParameters</span></span>
<span data-ttu-id="75fa6-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75fa6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75fa6-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="75fa6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75fa6-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75fa6-138">INPUTS</span></span>

### <span data-ttu-id="75fa6-139">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="75fa6-139">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="75fa6-140">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="75fa6-140">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="75fa6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75fa6-141">OUTPUTS</span></span>

### <span data-ttu-id="75fa6-142">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="75fa6-142">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="75fa6-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75fa6-143">NOTES</span></span>

## <span data-ttu-id="75fa6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75fa6-144">RELATED LINKS</span></span>
