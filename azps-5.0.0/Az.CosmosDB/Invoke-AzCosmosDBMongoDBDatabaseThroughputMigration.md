---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbmongodbdatabasethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration.md
ms.openlocfilehash: 1ba30d016b2ff8b143987961d08d68eacca16890
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299429"
---
# <span data-ttu-id="f55d7-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="f55d7-101">Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration</span></span>

## <span data-ttu-id="f55d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f55d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f55d7-103">Ezzel a beállítással áttelepítheti az automatikus méretezést a manuális átviteli sebességre, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="f55d7-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="f55d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f55d7-104">SYNTAX</span></span>

### <span data-ttu-id="f55d7-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f55d7-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -ResourceGroupName <String>
 -AccountName <String> -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f55d7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f55d7-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>]
 -ParentObject <PSDatabaseAccountGetResults> -ThroughputType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f55d7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f55d7-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f55d7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f55d7-108">DESCRIPTION</span></span>
<span data-ttu-id="f55d7-109">A ThroughpyteType paraméter határozza meg, hogy milyen átviteli sebességet szeretne áttelepíteni.</span><span class="sxs-lookup"><span data-stu-id="f55d7-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="f55d7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f55d7-110">EXAMPLES</span></span>

### <span data-ttu-id="f55d7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f55d7-111">Example 1</span></span>
```powershell
PS C:\>$NewMongodbDatabase =  New-AzCosmosDBMongoDBDatabase -AccountName myAccountName -ResourceGroupName myRgName -Name myDbName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBMongoDBDatabaseThroughputMigration -InputObject $NewMongodbDatabase -ThroughputType Autoscale
```


## <span data-ttu-id="f55d7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f55d7-112">PARAMETERS</span></span>

### <span data-ttu-id="f55d7-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f55d7-113">-AccountName</span></span>
<span data-ttu-id="f55d7-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f55d7-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f55d7-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f55d7-115">-Confirm</span></span>
<span data-ttu-id="f55d7-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f55d7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f55d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55d7-117">-DefaultProfile</span></span>
<span data-ttu-id="f55d7-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f55d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f55d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f55d7-119">-InputObject</span></span>
<span data-ttu-id="f55d7-120">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="f55d7-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f55d7-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f55d7-121">-Name</span></span>
<span data-ttu-id="f55d7-122">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f55d7-122">Database name.</span></span>

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

### <span data-ttu-id="f55d7-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f55d7-123">-ParentObject</span></span>
<span data-ttu-id="f55d7-124">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="f55d7-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f55d7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55d7-125">-ResourceGroupName</span></span>
<span data-ttu-id="f55d7-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f55d7-126">Name of resource group.</span></span>

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

### <span data-ttu-id="f55d7-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="f55d7-127">-ThroughputType</span></span>
<span data-ttu-id="f55d7-128">Az áttelepítéshez használandó átviteli típus.</span><span class="sxs-lookup"><span data-stu-id="f55d7-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="f55d7-129">Lehetséges értékek: automatikus méretezés, kézi.</span><span class="sxs-lookup"><span data-stu-id="f55d7-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="f55d7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f55d7-130">-WhatIf</span></span>
<span data-ttu-id="f55d7-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f55d7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f55d7-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f55d7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f55d7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55d7-133">CommonParameters</span></span>
<span data-ttu-id="f55d7-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f55d7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55d7-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f55d7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55d7-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f55d7-136">INPUTS</span></span>

### <span data-ttu-id="f55d7-137">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f55d7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="f55d7-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f55d7-138">OUTPUTS</span></span>

### <span data-ttu-id="f55d7-139">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f55d7-139">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f55d7-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f55d7-140">NOTES</span></span>

## <span data-ttu-id="f55d7-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f55d7-141">RELATED LINKS</span></span>
